# liquibase-mysql-docker/test

This directory contains a test to ensure the MySQL JDBC driver works with liquibase within the container.

At build-time this directory is copies into /opt/test_liquibase_mysql, and to validate the built image, DockerHub runs the [run_test.sh](./run_test.sh) script automatically via docker-compose.test.yml.
