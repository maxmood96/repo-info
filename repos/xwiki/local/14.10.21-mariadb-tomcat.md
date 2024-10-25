# `xwiki:14-mariadb-tomcat`

## Docker Metadata

- Image ID: `sha256:fe360dc5192172cb7a375bd81d3979361cc3262533ab5f01df9e2ddde71dd966`
- Created: `2024-02-13T09:10:03Z`
- Virtual Size: ~ 1.21 Gb  
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
  - `JAVA_VERSION=jdk-17.0.13+11`
  - `CATALINA_HOME=/usr/local/tomcat`
  - `TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib`
  - `LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib`
  - `GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243`
  - `TOMCAT_MAJOR=9`
  - `TOMCAT_VERSION=9.0.96`
  - `TOMCAT_SHA512=ef3ac81debbc3a519c43d1fdb1c88ab26a8052af424d81bceccfbd6e663050a06d7aad7960fd5d11c17849829daebbebf33d92ac1158902283d0e534514aab93`
  - `XWIKI_VERSION=14.10.21`
  - `XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.21`
  - `XWIKI_DOWNLOAD_SHA256=72a634e2aeb085878dce2629a3e5e6136887d0c22712dcee5a284be8143135ea`
  - `MARIADB_JDBC_VERSION=3.3.2`
  - `MARIADB_JDBC_SHA256=2a67ef3cc1ca481965a0e7f2d4174d126f3464d02b4055a441261fad8c196769`
  - `MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.3.2`
  - `MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.3.2.jar`
  - `MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.3.2.jar`
- Labels:
  - `org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>`
  - `org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki`
  - `org.opencontainers.image.licenses=LGPL-2.1`
  - `org.opencontainers.image.ref.name=ubuntu`
  - `org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git`
  - `org.opencontainers.image.url=https://hub.docker.com/_/xwiki`
  - `org.opencontainers.image.vendor=xwiki.org`
  - `org.opencontainers.image.version=24.04`
