# `sonarqube:10.8.1-enterprise`

## Docker Metadata

- Image ID: `sha256:66b064a5294646d205b607d3db8f69701deb8fae8530988ad8908a13b01cf415`
- Created: `2025-01-07T15:07:53Z`
- Virtual Size: ~ 1.40 Gb  
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
  - `SONAR_VERSION=10.8.1.101195`
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
