# airflow_macos

## instructions
- mkdir airflow_macos
- cd airflow_macos
- curl -LfO 'https://airflow.apache.org/docs/apache-airflow/stable/docker-compose.yaml'
- edit line 124 "8080:8080" to "7070:8080"
- echo -e "AIRFLOW_UID=$(id -u)\nAIRFLOW_GID=0" > .env
- mkdir -p dags logs plugins
- docker compose up airflow-init
- docker compose up -d
- go to http://localhost:7070 login as airflow/airflow
- docker compose down
- docker compose down --volumes --remove-orphans
