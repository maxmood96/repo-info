# `sonarqube:2025.1.0-datacenter-search`

## Docker Metadata

- Image ID: `sha256:aa8f786b616180afc4ad3e18ef4c2e3cd2e78b20807aa70f69f14b315a702e82`
- Created: `2025-01-20T15:15:41Z`
- Virtual Size: ~ 1.45 Gb  
  (total size of all layers on-disk)
- Arch: `linux`/`amd64`
- Entrypoint: `["/opt/sonarqube/docker/run.sh"]`
- Command: `["/opt/sonarqube/docker/sonar.sh"]`
- Environment:
  - `PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin`
  - `JAVA_HOME=/opt/java/openjdk`
  - `LANG=en_US.UTF-8`
  - `LANGUAGE=en_US:en`
  - `LC_ALL=en_US.UTF-8`
  - `JAVA_VERSION=jdk-17.0.14+7`
  - `DOCKER_RUNNING=true`
  - `SONARQUBE_HOME=/opt/sonarqube`
  - `SONAR_VERSION=2025.1.0.102418`
  - `SQ_DATA_DIR=/opt/sonarqube/data`
  - `SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions`
  - `SQ_LOGS_DIR=/opt/sonarqube/logs`
  - `SQ_TEMP_DIR=/opt/sonarqube/temp`
  - `SONAR_CLUSTER_NODE_TYPE=search`
  - `SONAR_CLUSTER_ENABLED=true`
  - `ES_TMPDIR=/opt/sonarqube/temp`
- Labels:
  - `io.k8s.description=SonarQube Server is a self-managed, automatic code review tool that systematically helps you deliver Clean Code.`
  - `io.openshift.min-cpu=400m`
  - `io.openshift.min-memory=2048M`
  - `io.openshift.non-scalable=false`
  - `io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code`
  - `org.opencontainers.image.ref.name=ubuntu`
  - `org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube`
  - `org.opencontainers.image.version=24.04`
