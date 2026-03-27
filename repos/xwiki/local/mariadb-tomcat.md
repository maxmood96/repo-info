# `xwiki:18-mariadb-tomcat`

## Docker Metadata

- Image ID: `sha256:cd55f8aa3a3d1fd4920fd22f5308e97235ab7b8844b14fb6a0d2d94bf8d7d4dc`
- Created: `2026-03-23T22:11:17.344306609Z`
- Virtual Size: ~ 1.33 Gb  
  (total size of all layers on-disk)
- Arch: `linux`/`amd64`
- Entrypoint: `["docker-entrypoint.sh"]`
- Command: `["xwiki"]`
- Environment:
  - `PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin`
  - `JAVA_HOME=/opt/java/openjdk`
  - `LANG=en_US.UTF-8`
  - `LANGUAGE=en_US:en`
  - `LC_ALL=en_US.UTF-8`
  - `JAVA_VERSION=jdk-21.0.10+7`
  - `CATALINA_HOME=/usr/local/tomcat`
  - `TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib`
  - `LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib`
  - `TOMCAT_MAJOR=10`
  - `TOMCAT_VERSION=10.1.53`
  - `TOMCAT_SHA512=0b21ad1e61b3163125866e8f5f317b23886998fccb4398f305c39a0bc1f688f6c566ab040da9f559ab50af4d699bda771d1ca89e229ead052336559a25753b45`
  - `XWIKI_VERSION=18.1.0`
  - `XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/18.1.0`
  - `XWIKI_DOWNLOAD_SHA256=0f7d70d190ebf20483b3afd79b006050bbe4618ca1dab02bc74e1c3202bd63c0`
  - `MARIADB_JDBC_VERSION=3.5.7`
  - `MARIADB_JDBC_SHA256=07bb1229dc184f3313a5aef4c5a6b3207c8dbaa09db4a26814c936f004b4c526`
  - `MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.5.7`
  - `MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.5.7.jar`
  - `MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.5.7.jar`
- Labels:
  - `org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>`
  - `org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki`
  - `org.opencontainers.image.licenses=LGPL-2.1`
  - `org.opencontainers.image.ref.name=ubuntu`
  - `org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git`
  - `org.opencontainers.image.url=https://hub.docker.com/_/xwiki`
  - `org.opencontainers.image.vendor=xwiki.org`
  - `org.opencontainers.image.version=24.04`
