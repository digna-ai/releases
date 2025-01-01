## Integrating Digna into ETL Processes

Digna can be seamlessly integrated into ETL (Extract, Transform, Load) processes through two primary methods: the Command Line Interface (CLI) and the REST API. Below, each method is described in detail with examples for usage.

### 1. Integration via Command Line Interface (CLI)

The Digna CLI provides a straightforward way to trigger inspections directly from the command line. This is especially useful for automated scripts or batch processes within your ETL pipeline.

#### Example Command:

```bash
$ dignacli inspect ProjectDemo 2025-01-01 2025-01-01
```

This command runs an inspection for the entire `ProjectDemo` project for the date `2025-01-01`.

#### Additional Information:
- For a full description of the CLI functionality, you can run the help command:
  ```bash
  $ dignacli inspect --help
  ```
- Refer to the Digna Command Line Interface documentation for detailed usage and options.

The CLI is ideal for scenarios where minimal setup is needed, and inspections can be executed directly by leveraging predefined configurations.

### 2. Integration via REST API

For more programmatic control and integration flexibility, Digna provides a comprehensive REST API. The OpenAPI documentation for your Digna instance can be accessed at:

```plaintext
(http|https)://<ip-address-or-hostname-of-your-digna-backend>:8082/docs
```

For example, assuming the Digna backend is running locally with the default `DIGNA_APP_PORT` set to `8082`:

```plaintext
http://localhost:8082/docs
```

#### Key Endpoints for Integration:

1. **Login**
   - Endpoint: `POST /oauth2/password/token`
   - Example request:

     ```bash
     curl -X 'POST' \
       'http://localhost:8082/oauth2/password/token' \
       -H 'accept: application/json' \
       -H 'Content-Type: application/x-www-form-urlencoded' \
       -d 'grant_type=password&username=user%40company.abc&password=pwd'
     ```

     **Notes:**
     - The `-d` data portion is URL-encoded (e.g., `@` in the username is replaced with `%40`).
     - Replace `user%40company.abc` and `pwd` with the actual username and password credentials.

2. **Retrieving Project and Data Source IDs**
   - For further requests, the `<project_id>` and `<data_source_id>` are required. You can manually retrieve these IDs from the Digna frontend or programmatically using the following endpoints:
     - `GET /projects`
     - `GET /projects/<project_id>/data-sources`

      ![image](https://github.com/user-attachments/assets/9c6317a9-ed23-4e2c-a90f-82882ca37e12)

3. **Start an Inspection**
   - Endpoint: `PUT /projects/{project_id}/data-sources/{data_source_id}/inspection-statuses`
   - Query Parameters: `start_date` and `end_date`.
   - Example usage can be found in the API documentation.

4. **Get Alert Status**
   - For overall alert status:
     - Endpoint: `GET /projects/{project_id}/data-sources/{data_source_id}/inspection-statuses`
   - For detailed alert status (per individual check):
     - Endpoint: `GET /projects/{project_id}/data-sources/{data_source_id}/sub-attributes/inspection-statuses`

The REST API is particularly suited for dynamic, fine-grained control of inspections and alert retrieval, making it a powerful tool for deeply integrated ETL workflows.

---

By leveraging either the CLI or REST API, Digna can be effectively incorporated into your ETL processes to ensure robust data quality checks and alerting mechanisms.
