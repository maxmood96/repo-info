# `xwiki:16-mariadb-tomcat`

## Docker Metadata

- Image ID: `sha256:dc9d70977c655301cbf28840cfcc1f90eb87fb2df161f8c0432a70edd588964a`
- Created: `2024-12-10T13:44:08Z`
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
  - `TOMCAT_VERSION=9.0.98`
  - `TOMCAT_SHA512=07d87286e8ee84bb291069c596cf36233e56a14e3ecb6d65eea0fa7c7042ce5e75f5db31f210b96b6b25b80b34e626dd26c5a6ed5c052384a8587d62658b5e16`
  - `XWIKI_VERSION=16.10.1`
  - `XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.10.1`
  - `XWIKI_DOWNLOAD_SHA256=f9f365da951626711ec44aebd0276517d8fe1522b1c209c0d3af9c302071ee6e`
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
