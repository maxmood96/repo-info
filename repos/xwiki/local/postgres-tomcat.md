# `xwiki:17-postgres-tomcat`

## Docker Metadata

- Image ID: `sha256:f9c602274ee674bc7611618dbf79c95d094622f6421148c6a65f51810a4cc74c`
- Created: `2025-01-28T17:13:32Z`
- Virtual Size: ~ 1.27 Gb  
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
  - `JAVA_VERSION=jdk-21.0.6+7`
  - `CATALINA_HOME=/usr/local/tomcat`
  - `TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib`
  - `LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib`
  - `TOMCAT_MAJOR=10`
  - `TOMCAT_VERSION=10.1.35`
  - `TOMCAT_SHA512=814500908e139fd984bbacf10ccf8ad400d129ce23a7ba47b771f0ca308b148e23a58c83eb924653f62ca2a0696c87fc6128c7a81def18b04c2f0c01f08009b9`
  - `XWIKI_VERSION=17.0.0`
  - `XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/17.0.0`
  - `XWIKI_DOWNLOAD_SHA256=fd4d25b42c5645d87f7ed242967161ccb2648688948de93649a5ca11a1845c34`
  - `POSTGRES_JDBC_VERSION=42.7.4`
  - `POSTGRES_JDBC_SHA256=188976721ead8e8627eb6d8389d500dccc0c9bebd885268a3047180274a6031e`
  - `POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.4`
  - `POSTGRES_JDBC_ARTIFACT=postgresql-42.7.4.jar`
  - `POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.4.jar`
- Labels:
  - `org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>`
  - `org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki`
  - `org.opencontainers.image.licenses=LGPL-2.1`
  - `org.opencontainers.image.ref.name=ubuntu`
  - `org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git`
  - `org.opencontainers.image.url=https://hub.docker.com/_/xwiki`
  - `org.opencontainers.image.vendor=xwiki.org`
  - `org.opencontainers.image.version=24.04`
