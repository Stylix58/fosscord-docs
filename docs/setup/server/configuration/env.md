# Environment Variables

Below is a list of environment variables used by {{ project.name }}.
You can set environment variables easily by creating an `.env` file
in the `{{ project.name.lower() }}-server` folder, with the format `NAME=VALUE` with each on new lines.

| Name                       | Value          | Description                                                                                                          |
| -------------------------- | -------------- | -------------------------------------------------------------------------------------------------------------------- |
| THREADS                    | number         | Number of threads to run {{ project.name }} on when using bundle. Make sure you've enabled RabbitMQ if using more than one     |
| PORT                       | number         | Port to listen on. Used by all components, including bundle. If using bundle, all components run under the same port |
| DATABASE                   | string         | Database connection string. Defaults to SQlite3 at project root                                                      |
| CONFIG_PATH                | string         | File path for JSON config, if not using `config` db table                                                            |
| WS_LOGEVENTS               | boolean        | If set, log websocket events except messages from gateway                                                            |
| WS_VERBOSE                 | boolean        | If set, log websocket messages sent/received by gateway                                                              |
| WS_DUMP                    | boolean        | If set, dump websocket messages sent/received to disk                                                                |
| CDN                        | string         | Lowest priority value for public CDN annoucements                                                                    |
| GATEWAY                    | string         | Lowest priority value for public gateway annoucements                                                                |
| STORAGE_LOCATION           | string         | CDN storage location. File path or S3 bucktet                                                                        |
| STORAGE_PROVIDER           | "s3" or "file" | CDN storage provider                                                                                                 |
| STORAGE_BUCKET             | string         | S3 bucket name                                                                                                       |
| STORAGE_REGION             | string         | S3 storage region                                                                                                    |
| DB_LOGGING                 | boolean        | if "true" logs all SQL queries to the terminal                                                                        |

## Docker

These environment variables should be set in the environment `~/.profile` or with an `export`

| Name              | Value  | Description                                                     |
| ----------------- | ------ | --------------------------------------------------------------- |
| POSTGRES_USER     | string | Postgressql database username                                  |
| POSTGRES_PASSWORD | string | Postgressql database password                                   |
| POSTGRES_DATABASE | string | Database connection string. Defaults to SQlite3 at project root |
| S3_BUCKET         | string | CDN storage location. S3 bucktet                                |
| S3_BUCKET_NAME    | string | S3 bucket                                                       |
| S3_BUCKET_REGION  | string | S3 storage region                                               |
