## `xwiki:16-mariadb-tomcat`

```console
$ docker pull xwiki@sha256:8762c0feb3faa4c28f4b4e878f398effeebce7feeb008fec9b8d0bd90c6ed79c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:16-mariadb-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:17abc63a46b06143eed1061ea5c7cffbd8620a5c70fb191b95213f1513e44c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **576.6 MB (576589268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85767af1a24174b567feebe0c02a1098c4bf1e325076bc14f3890f8afdb343e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 19 Jun 2024 14:03:42 GMT
ARG RELEASE
# Wed, 19 Jun 2024 14:03:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 19 Jun 2024 14:03:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 19 Jun 2024 14:03:42 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 19 Jun 2024 14:03:42 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Wed, 19 Jun 2024 14:03:42 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ccfa23c25790475c84df983cc5f729b94c04d9ea9863912deb15c6266782cf16';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bcb1b7b8ad68c93093f09b591b7cb17161d39891f7d29d33a586f5a328603707';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        armhf|arm)          ESUM='2e06401aa3aa7a825d73a6af8e9462449b1a86e7705b793dc8ec90423b602ee2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='884b5cb817e50010b4d0a3252afb6a80db18995af19bbd16a37348b2c37949bc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='67dd46352ba94f273579a04ef0756408b06db82b1b4ddf050045c226212f76fd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 19 Jun 2024 14:03:42 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 19 Jun 2024 14:03:42 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Jun 2024 14:03:42 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 19 Jun 2024 14:03:42 GMT
WORKDIR /usr/local/tomcat
# Wed, 19 Jun 2024 14:03:42 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 19 Jun 2024 14:03:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 19 Jun 2024 14:03:42 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 19 Jun 2024 14:03:42 GMT
ENV TOMCAT_MAJOR=9
# Wed, 19 Jun 2024 14:03:42 GMT
ENV TOMCAT_VERSION=9.0.90
# Wed, 19 Jun 2024 14:03:42 GMT
ENV TOMCAT_SHA512=e77b47d7ded86da81018d38c4f728f5f804c1a65bb941a138a7989b69c859031e88d113ccf4fc3a409062ee24511fa5ccf15dfad333f570838ee2a36dae23e19
# Wed, 19 Jun 2024 14:03:42 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 19 Jun 2024 14:03:42 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Jun 2024 14:03:42 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 19 Jun 2024 14:03:42 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 19 Jun 2024 14:03:42 GMT
ENTRYPOINT []
# Wed, 19 Jun 2024 14:03:42 GMT
CMD ["catalina.sh" "run"]
# Wed, 26 Jun 2024 09:06:21 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 26 Jun 2024 09:06:21 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 26 Jun 2024 09:06:21 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 26 Jun 2024 09:06:21 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 26 Jun 2024 09:06:21 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 26 Jun 2024 09:06:21 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 26 Jun 2024 09:06:21 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
ENV XWIKI_VERSION=16.5.0
# Wed, 26 Jun 2024 09:06:21 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.5.0
# Wed, 26 Jun 2024 09:06:21 GMT
ENV XWIKI_DOWNLOAD_SHA256=0997ff4cfe16928996218963fad74d7a564c1aa75c7e8434e7cd25bd471ecd5a
# Wed, 26 Jun 2024 09:06:21 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
ENV MARIADB_JDBC_VERSION=3.4.0
# Wed, 26 Jun 2024 09:06:21 GMT
ENV MARIADB_JDBC_SHA256=d83970dcda3198ca480e59b38e9e7055df09833e40d898c8ec5778a1e767f93b
# Wed, 26 Jun 2024 09:06:21 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.4.0
# Wed, 26 Jun 2024 09:06:21 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.4.0.jar
# Wed, 26 Jun 2024 09:06:21 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.4.0.jar
# Wed, 26 Jun 2024 09:06:21 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
VOLUME [/usr/local/xwiki]
# Wed, 26 Jun 2024 09:06:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Jun 2024 09:06:21 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:9b857f539cb142c9aa2201a17bb8e1cd5cf12edd4a65adf5732fe9f4343964cf`  
		Last Modified: Fri, 28 Jun 2024 01:17:21 GMT  
		Size: 30.4 MB (30439866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708ff3b02f8b7b7711302f65e71cb2abbb60946f996f61dec11ce5788fc08f11`  
		Last Modified: Tue, 02 Jul 2024 06:00:37 GMT  
		Size: 12.9 MB (12871067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ea69141092d083d2011e4bef99d88179238845830f3d13a4e385c22865b7d3`  
		Last Modified: Tue, 02 Jul 2024 06:02:20 GMT  
		Size: 47.3 MB (47256035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d590beb7c559e52929bdee57763bf9b4d6993efef2a777ce420cefdbefbf6fc`  
		Last Modified: Tue, 02 Jul 2024 06:02:13 GMT  
		Size: 162.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb850744c99279a291a7993996d6f9a8b25a5cec4bfad603897080ded3217e1b`  
		Last Modified: Tue, 02 Jul 2024 06:02:13 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a7afe74b6fed6887c816a067579be91ed25ca75523bf75fcfad98cef52543f`  
		Last Modified: Tue, 02 Jul 2024 09:33:31 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76d6552fe8eceff7e6e34f9e939690a80683bd6c24bb7bdfbc93c59a2a7f562`  
		Last Modified: Tue, 02 Jul 2024 09:33:31 GMT  
		Size: 12.4 MB (12448230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27f204c7216753af1cfefc04ec89965a3dddc744bc44e0ffed00d1d786c73bc3`  
		Last Modified: Tue, 02 Jul 2024 09:33:31 GMT  
		Size: 217.8 KB (217827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ec09c1d42bc349fb2a009e99ba2435ccecd7d522a3bb69e635bf35495ac53e`  
		Last Modified: Tue, 02 Jul 2024 10:05:54 GMT  
		Size: 178.4 MB (178436154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5055b556d918f371cd88c6f77465c7a8c0ad5509ccbca7f52ac319795f567a21`  
		Last Modified: Tue, 02 Jul 2024 10:05:56 GMT  
		Size: 294.3 MB (294265725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d39e6d13a3e07ecfe53a64223e53b968ca953567d3b38830e9d8360b45d40c9`  
		Last Modified: Tue, 02 Jul 2024 10:05:49 GMT  
		Size: 640.6 KB (640645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e7f8855ffd57ce751d757af8d0eed2acc2c2daaaf095e04033b2b53078e023`  
		Last Modified: Tue, 02 Jul 2024 10:05:49 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f592fd5ccdbbb39a4abeac171191098ded2cc4cfa9d41edf0752b86ef87d67d3`  
		Last Modified: Tue, 02 Jul 2024 10:05:50 GMT  
		Size: 2.3 KB (2309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752fb5c62d11dd1a4c3ff76578273e5bc03adf8e9f47eec57e4f3a3249633cd5`  
		Last Modified: Tue, 02 Jul 2024 10:05:51 GMT  
		Size: 6.5 KB (6527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6056a831072737ba71b9bcf378c471a361841409d5978596755eb37a352bb1a`  
		Last Modified: Tue, 02 Jul 2024 10:05:51 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:16-mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:55c88aa21e7762cd2d9c20e2a81b5d60592825b890231eae204d834715c20feb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8925033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cda4d2ba2717819aa71c1ac20b3f8c392de3813c033f058d4ad4a5207d18b892`

```dockerfile
```

-	Layers:
	-	`sha256:c2ed05e53839e56bceb8377f2cdf56b8039c2d8216b69b9743e8608e79ac9c41`  
		Last Modified: Tue, 02 Jul 2024 10:05:50 GMT  
		Size: 8.9 MB (8883743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7467e9ec05431a86e6eb0c78b362c956e69e95a4c749f944097c852aa2f0d98`  
		Last Modified: Tue, 02 Jul 2024 10:05:49 GMT  
		Size: 41.3 KB (41290 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:16-mariadb-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:84d8a73b137cb38a2ad915fa97e208accf25bb5f8e48abdefdc9780dfa69e68b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **571.6 MB (571632566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecac2016a7c257149d8f86718ad77a8fbecc26139c16ece3969d9ef6ba5e1e58`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ccfa23c25790475c84df983cc5f729b94c04d9ea9863912deb15c6266782cf16';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bcb1b7b8ad68c93093f09b591b7cb17161d39891f7d29d33a586f5a328603707';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        armhf|arm)          ESUM='2e06401aa3aa7a825d73a6af8e9462449b1a86e7705b793dc8ec90423b602ee2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='884b5cb817e50010b4d0a3252afb6a80db18995af19bbd16a37348b2c37949bc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='67dd46352ba94f273579a04ef0756408b06db82b1b4ddf050045c226212f76fd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 19 Jun 2024 14:03:42 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 19 Jun 2024 14:03:42 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Jun 2024 14:03:42 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 19 Jun 2024 14:03:42 GMT
WORKDIR /usr/local/tomcat
# Wed, 19 Jun 2024 14:03:42 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 19 Jun 2024 14:03:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 19 Jun 2024 14:03:42 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 19 Jun 2024 14:03:42 GMT
ENV TOMCAT_MAJOR=9
# Wed, 19 Jun 2024 14:03:42 GMT
ENV TOMCAT_VERSION=9.0.90
# Wed, 19 Jun 2024 14:03:42 GMT
ENV TOMCAT_SHA512=e77b47d7ded86da81018d38c4f728f5f804c1a65bb941a138a7989b69c859031e88d113ccf4fc3a409062ee24511fa5ccf15dfad333f570838ee2a36dae23e19
# Wed, 19 Jun 2024 14:03:42 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 19 Jun 2024 14:03:42 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Jun 2024 14:03:42 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 19 Jun 2024 14:03:42 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 19 Jun 2024 14:03:42 GMT
ENTRYPOINT []
# Wed, 19 Jun 2024 14:03:42 GMT
CMD ["catalina.sh" "run"]
# Wed, 26 Jun 2024 09:06:21 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 26 Jun 2024 09:06:21 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 26 Jun 2024 09:06:21 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 26 Jun 2024 09:06:21 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 26 Jun 2024 09:06:21 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 26 Jun 2024 09:06:21 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 26 Jun 2024 09:06:21 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
ENV XWIKI_VERSION=16.5.0
# Wed, 26 Jun 2024 09:06:21 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.5.0
# Wed, 26 Jun 2024 09:06:21 GMT
ENV XWIKI_DOWNLOAD_SHA256=0997ff4cfe16928996218963fad74d7a564c1aa75c7e8434e7cd25bd471ecd5a
# Wed, 26 Jun 2024 09:06:21 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
ENV MARIADB_JDBC_VERSION=3.4.0
# Wed, 26 Jun 2024 09:06:21 GMT
ENV MARIADB_JDBC_SHA256=d83970dcda3198ca480e59b38e9e7055df09833e40d898c8ec5778a1e767f93b
# Wed, 26 Jun 2024 09:06:21 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.4.0
# Wed, 26 Jun 2024 09:06:21 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.4.0.jar
# Wed, 26 Jun 2024 09:06:21 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.4.0.jar
# Wed, 26 Jun 2024 09:06:21 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
VOLUME [/usr/local/xwiki]
# Wed, 26 Jun 2024 09:06:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Jun 2024 09:06:21 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd918abfec0657ade8aeeffe2722e92948e13fa403fd238ae22b1a9881e9402`  
		Last Modified: Wed, 05 Jun 2024 04:55:01 GMT  
		Size: 12.8 MB (12847839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa963c04773e39efb3eb3c080a80fe1bccbf8410a480f24229a7a06fc307c532`  
		Last Modified: Wed, 05 Jun 2024 04:57:44 GMT  
		Size: 46.7 MB (46716398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382cfd76d96df44a0a5e200f1841a3fc8d1bdbfa5fb655a2f2795bc3b4e16ec3`  
		Last Modified: Wed, 05 Jun 2024 04:57:38 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0792dc21c67221e401d3c4b78ebea1705a045fbcc6461558ac50bfbe911989a`  
		Last Modified: Wed, 05 Jun 2024 04:57:38 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be592c65af922b27726abd96af5a0cfe9be1a73f8bf397b7088c1a3fa9f04a44`  
		Last Modified: Fri, 28 Jun 2024 22:00:21 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76799d6c646f3750c8e6a7264d880633888d1e2ba50241c0e50817f4417ac73c`  
		Last Modified: Fri, 28 Jun 2024 22:01:46 GMT  
		Size: 12.5 MB (12454654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6550921e61de2eb092056a96013235258b488c63295d9f955bec3605a9719637`  
		Last Modified: Fri, 28 Jun 2024 22:01:46 GMT  
		Size: 2.8 MB (2806589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efadff25994e1217c725a8fffa89548682ee194dd571e8df2f22870af1c62908`  
		Last Modified: Fri, 28 Jun 2024 22:54:59 GMT  
		Size: 173.5 MB (173484700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a7c17b450dc8a11547f57600aa5a246cb6eee460bdcc254695bdc6c9300354`  
		Last Modified: Fri, 28 Jun 2024 22:55:00 GMT  
		Size: 294.3 MB (294265724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3b02afa66e4f55b1f6b4ba8e1c35349436ed69772b2c8b38666865bf33d015`  
		Last Modified: Fri, 28 Jun 2024 22:57:25 GMT  
		Size: 640.6 KB (640646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e65ab8207755945f4fe72c40d4d40775238f358b0e95cabce0cb51c7fcc2458`  
		Last Modified: Fri, 28 Jun 2024 22:57:24 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed928a1c31a0c5c22fa77a35c28149e8b390af9789e0b9c7eace65b1910b4574`  
		Last Modified: Fri, 28 Jun 2024 22:57:25 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba76176f41f22f5a3fbd063d4dee783aa0e3c69120f18b462deba3074cdba960`  
		Last Modified: Fri, 28 Jun 2024 22:57:25 GMT  
		Size: 6.5 KB (6530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbaa35d37cc41f144f1976fe05bb0d9abe4c96b34f07e03cd24f95aabceb0f7d`  
		Last Modified: Fri, 28 Jun 2024 22:57:25 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:16-mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:c4e59215d5ed37fe9cce41ae5e6e1290dfdac16eaae0b4ef976ef62a0eb9a701
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8928005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a71fc6890dfeba76ab4d3d52fbcf7dd2a742ec2628253f009aabe2bfd8788c20`

```dockerfile
```

-	Layers:
	-	`sha256:49f0d7daa8a543f6c28bdcba3a90794fcc7bf206c63235d2a5dcf2f67311acb7`  
		Last Modified: Fri, 28 Jun 2024 22:57:25 GMT  
		Size: 8.9 MB (8886058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee8e12ab17f2ed6350514a6869c343105be6a4639478bd5328913e151ff49148`  
		Last Modified: Fri, 28 Jun 2024 22:57:24 GMT  
		Size: 41.9 KB (41947 bytes)  
		MIME: application/vnd.in-toto+json
