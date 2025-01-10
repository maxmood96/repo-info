# `sonarqube:25.1.0.102122-community`

## Docker Metadata

- Image ID: `sha256:78b14e602462cc8273b80bb913877fde9db6f7e00f05689a29881c87d7653d31`
- Created: `2025-01-07T15:07:53Z`
- Virtual Size: ~ 1.17 Gb  
  (total size of all layers on-disk)
- Arch: `linux`/`amd64`
- Entrypoint: `["/opt/sonarqube/docker/entrypoint.sh"]`
- Environment:
  - `PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin`
  - `JAVA_HOME=/opt/java/openjdk`
  - `LANG=en_US.UTF-8`
  - `LANGUAGE=en_US:en`
  - `LC_ALL=en_US.UTF-8`
  - `JAVA_VERSION=jdk-17.0.13+11`
  - `DOCKER_RUNNING=true`
  - `SONARQUBE_HOME=/opt/sonarqube`
  - `SONAR_VERSION=25.1.0.102122`
  - `SQ_DATA_DIR=/opt/sonarqube/data`
  - `SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions`
  - `SQ_LOGS_DIR=/opt/sonarqube/logs`
  - `SQ_TEMP_DIR=/opt/sonarqube/temp`
  - `ES_TMPDIR=/opt/sonarqube/temp`
- Labels:
  - `io.k8s.description=SonarQube is a self-managed, automatic code review tool that systematically helps you deliver Clean Code.`
  - `io.openshift.min-cpu=400m`
  - `io.openshift.min-memory=2048M`
  - `io.openshift.non-scalable=true`
  - `io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code`
  - `org.opencontainers.image.ref.name=ubuntu`
  - `org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube`
  - `org.opencontainers.image.version=24.04`
