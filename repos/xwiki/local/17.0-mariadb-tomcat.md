# `xwiki:17-mariadb-tomcat`

## Docker Metadata

- Image ID: `sha256:186e51c03bb430141fd3296f89a012633a14e5f77887c85de420156f1d9f76d1`
- Created: `2025-01-28T17:13:32Z`
- Virtual Size: ~ 1.24 Gb  
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
  - `TOMCAT_VERSION=10.1.34`
  - `TOMCAT_SHA512=e29c4d0e26295d64dfeee399e7719b5baac2682ac0e7b53702f26d630fea761f93ddf60674dfe87c41ddd9b79d4938a6a533a280bb3d7fb83c2a1b7cd5da6b09`
  - `XWIKI_VERSION=17.0.0`
  - `XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/17.0.0`
  - `XWIKI_DOWNLOAD_SHA256=fd4d25b42c5645d87f7ed242967161ccb2648688948de93649a5ca11a1845c34`
  - `MARIADB_JDBC_VERSION=3.5.1`
  - `MARIADB_JDBC_SHA256=50a50c4a3c13c30dfbd40587f7ad9a496197d285ede0948641d9eee68fdf2106`
  - `MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.5.1`
  - `MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.5.1.jar`
  - `MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.5.1.jar`
- Labels:
  - `org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>`
  - `org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki`
  - `org.opencontainers.image.licenses=LGPL-2.1`
  - `org.opencontainers.image.ref.name=ubuntu`
  - `org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git`
  - `org.opencontainers.image.url=https://hub.docker.com/_/xwiki`
  - `org.opencontainers.image.vendor=xwiki.org`
  - `org.opencontainers.image.version=24.04`
