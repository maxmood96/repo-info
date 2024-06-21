## `xwiki:15-mariadb-tomcat`

```console
$ docker pull xwiki@sha256:182be881152770f2e09bc21053fdc9d03e50073e42b5a2677a9c1d4b0de31103
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:15-mariadb-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:e4ce94a608485cd34077bbe05d04b5e91927fb43fd3f9aa7aea182b06aed91b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.5 MB (589523517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fcf9e305ee72dc30af96370fb102d581040edbda6f58e64b5acf425e60fe3cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 27 May 2024 13:30:04 GMT
ARG RELEASE
# Mon, 27 May 2024 13:30:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 May 2024 13:30:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 May 2024 13:30:04 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 27 May 2024 13:30:04 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 27 May 2024 13:30:04 GMT
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
# Mon, 27 May 2024 13:30:04 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 27 May 2024 13:30:04 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 27 May 2024 13:30:04 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 27 May 2024 13:30:04 GMT
WORKDIR /usr/local/tomcat
# Mon, 27 May 2024 13:30:04 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 27 May 2024 13:30:04 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 27 May 2024 13:30:04 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Mon, 27 May 2024 13:30:04 GMT
ENV TOMCAT_MAJOR=9
# Mon, 27 May 2024 13:30:04 GMT
ENV TOMCAT_VERSION=9.0.90
# Mon, 27 May 2024 13:30:04 GMT
ENV TOMCAT_SHA512=e77b47d7ded86da81018d38c4f728f5f804c1a65bb941a138a7989b69c859031e88d113ccf4fc3a409062ee24511fa5ccf15dfad333f570838ee2a36dae23e19
# Mon, 27 May 2024 13:30:04 GMT
COPY dir:2df9bb79b245ef48cbc57c6bf2da0649de462747be0398216fa4b2b0a49e8963 in /usr/local/tomcat 
# Mon, 27 May 2024 13:30:04 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Mon, 27 May 2024 13:30:04 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Mon, 27 May 2024 13:30:04 GMT
EXPOSE 8080
# Mon, 27 May 2024 13:30:04 GMT
ENTRYPOINT []
# Mon, 27 May 2024 13:30:04 GMT
CMD ["catalina.sh" "run"]
# Mon, 27 May 2024 13:30:04 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 27 May 2024 13:30:04 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 27 May 2024 13:30:04 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 27 May 2024 13:30:04 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 27 May 2024 13:30:04 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 27 May 2024 13:30:04 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 27 May 2024 13:30:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 27 May 2024 13:30:04 GMT
ENV XWIKI_VERSION=15.10.10
# Mon, 27 May 2024 13:30:04 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.10.10
# Mon, 27 May 2024 13:30:04 GMT
ENV XWIKI_DOWNLOAD_SHA256=fda9b5b4c1f471dc47e8cf2cb72b7550dbe6d6772887201be94c522a13b6078e
# Mon, 27 May 2024 13:30:04 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 27 May 2024 13:30:04 GMT
ENV MARIADB_JDBC_VERSION=3.3.3
# Mon, 27 May 2024 13:30:04 GMT
ENV MARIADB_JDBC_SHA256=89d71a6ffd800c032b23e588108688d391631f0aba962ba2381cc82cb111b796
# Mon, 27 May 2024 13:30:04 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.3.3
# Mon, 27 May 2024 13:30:04 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.3.3.jar
# Mon, 27 May 2024 13:30:04 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.3.3.jar
# Mon, 27 May 2024 13:30:04 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Mon, 27 May 2024 13:30:04 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 27 May 2024 13:30:04 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 27 May 2024 13:30:04 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 27 May 2024 13:30:04 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 27 May 2024 13:30:04 GMT
VOLUME [/usr/local/xwiki]
# Mon, 27 May 2024 13:30:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 May 2024 13:30:04 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab7f202453ac8b8def634e399240ab2bd7247e2f125fbddd2dbaaa8fa4ce555`  
		Last Modified: Wed, 05 Jun 2024 04:58:06 GMT  
		Size: 12.9 MB (12904817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee59ca42def8dda96caccd58b671902e65195492ee8e5daa263e1e948033adc3`  
		Last Modified: Wed, 05 Jun 2024 05:01:21 GMT  
		Size: 47.3 MB (47256057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce2282f972ff7152adb0a2c757ddd63cf0c38d489c7d7952d7aa88ab1804bc5`  
		Last Modified: Wed, 05 Jun 2024 05:01:15 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a9e456ba828f8cfc067a64b3717c10e4c0709fc1f0b95e5a5efd3ee816e643`  
		Last Modified: Wed, 05 Jun 2024 05:01:15 GMT  
		Size: 733.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf4892f7e4550fc70dba9049d20a75e7eee29216fc7246e9610f72a3bfc77ce`  
		Last Modified: Wed, 05 Jun 2024 08:23:47 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6824fc91fce6990f3c5461944dc0c65989a6cbc42fcaa2946a347272fb3152f7`  
		Last Modified: Fri, 21 Jun 2024 03:23:39 GMT  
		Size: 12.4 MB (12448147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d54fb7690ec1a8b492dfcf461476d39b87855e7e7f6a5e4923e50d310130f5d9`  
		Last Modified: Fri, 21 Jun 2024 03:23:38 GMT  
		Size: 456.3 KB (456339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40439d1d569bf93eea762a027af4886a8863a9775307e07bd2f472f76eeaa115`  
		Last Modified: Fri, 21 Jun 2024 03:23:38 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98a8a50e1a27269f5296e39bf9b9d85bcf1ebdfc5b1dd113b2057df9fd2884d`  
		Last Modified: Fri, 21 Jun 2024 04:01:22 GMT  
		Size: 178.4 MB (178436420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9c590046268386874c3d5ea4fa5ed5fad8482cd41b9d4469a11470f19278d00`  
		Last Modified: Fri, 21 Jun 2024 04:01:24 GMT  
		Size: 306.9 MB (306948784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d3ee798f3944a8ba5c3830da25e438a13613293e57c59740091c64c2cca505`  
		Last Modified: Fri, 21 Jun 2024 04:01:19 GMT  
		Size: 620.0 KB (619999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d51bcbefe408dbbf9be95cd110287145ebf934a2c85e5a61870e055e4288e2d1`  
		Last Modified: Fri, 21 Jun 2024 04:01:18 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02be1fda818c68e9ed48ff5e05bd793daf516f9f443d24fb9bf351b082c432a5`  
		Last Modified: Fri, 21 Jun 2024 04:01:20 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e69cd653a7c49ef9adabde4dd1fa45479be9ac419d1d49714fb7f2a732827d`  
		Last Modified: Fri, 21 Jun 2024 04:01:20 GMT  
		Size: 6.4 KB (6414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4517dcef8ca89e2ebc50783969240e905428987464a9f447e208c964f9c702a2`  
		Last Modified: Fri, 21 Jun 2024 04:01:21 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:15-mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:5717bd618ff8617e7336fabb6fd1ce5e3236e5144b4b91b167b433bc6921aca7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8932885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e44a2c43ebb65cae2c425b8462a4de9876c0be555053ab8c70097b039360ce8b`

```dockerfile
```

-	Layers:
	-	`sha256:6c8141720f0536260d7024f48857ba5ec3d87c5984b79b1b3eae7bad817b074e`  
		Last Modified: Fri, 21 Jun 2024 04:01:19 GMT  
		Size: 8.9 MB (8892899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf0bb308015842ec90f34de3e23833dda6ee7b8d587277e7fb0bc4f20dcec7c3`  
		Last Modified: Fri, 21 Jun 2024 04:01:18 GMT  
		Size: 40.0 KB (39986 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:15-mariadb-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:0af480d58c04e6cd5386ae5ba4ff97f3f5c68b808f9dd9c2818de5bff7ec074e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.9 MB (581946896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a580fb76d367afe7bcf6352257ace3e67427819f9ccb31b51d3762f17ce4d8d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 27 May 2024 13:30:04 GMT
ARG RELEASE
# Mon, 27 May 2024 13:30:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 May 2024 13:30:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 May 2024 13:30:04 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 27 May 2024 13:30:04 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 27 May 2024 13:30:04 GMT
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
# Mon, 27 May 2024 13:30:04 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 27 May 2024 13:30:04 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 27 May 2024 13:30:04 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 27 May 2024 13:30:04 GMT
WORKDIR /usr/local/tomcat
# Mon, 27 May 2024 13:30:04 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 27 May 2024 13:30:04 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 27 May 2024 13:30:04 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Mon, 27 May 2024 13:30:04 GMT
ENV TOMCAT_MAJOR=9
# Mon, 27 May 2024 13:30:04 GMT
ENV TOMCAT_VERSION=9.0.90
# Mon, 27 May 2024 13:30:04 GMT
ENV TOMCAT_SHA512=e77b47d7ded86da81018d38c4f728f5f804c1a65bb941a138a7989b69c859031e88d113ccf4fc3a409062ee24511fa5ccf15dfad333f570838ee2a36dae23e19
# Mon, 27 May 2024 13:30:04 GMT
COPY dir:f1c8ea4bbef7f8fcbb6baccde13eb9f00f71605c817e41238c6fdc3ab9036a00 in /usr/local/tomcat 
# Mon, 27 May 2024 13:30:04 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Mon, 27 May 2024 13:30:04 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Mon, 27 May 2024 13:30:04 GMT
EXPOSE 8080
# Mon, 27 May 2024 13:30:04 GMT
ENTRYPOINT []
# Mon, 27 May 2024 13:30:04 GMT
CMD ["catalina.sh" "run"]
# Mon, 27 May 2024 13:30:04 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 27 May 2024 13:30:04 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 27 May 2024 13:30:04 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 27 May 2024 13:30:04 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 27 May 2024 13:30:04 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 27 May 2024 13:30:04 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 27 May 2024 13:30:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 27 May 2024 13:30:04 GMT
ENV XWIKI_VERSION=15.10.10
# Mon, 27 May 2024 13:30:04 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.10.10
# Mon, 27 May 2024 13:30:04 GMT
ENV XWIKI_DOWNLOAD_SHA256=fda9b5b4c1f471dc47e8cf2cb72b7550dbe6d6772887201be94c522a13b6078e
# Mon, 27 May 2024 13:30:04 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 27 May 2024 13:30:04 GMT
ENV MARIADB_JDBC_VERSION=3.3.3
# Mon, 27 May 2024 13:30:04 GMT
ENV MARIADB_JDBC_SHA256=89d71a6ffd800c032b23e588108688d391631f0aba962ba2381cc82cb111b796
# Mon, 27 May 2024 13:30:04 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.3.3
# Mon, 27 May 2024 13:30:04 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.3.3.jar
# Mon, 27 May 2024 13:30:04 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.3.3.jar
# Mon, 27 May 2024 13:30:04 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Mon, 27 May 2024 13:30:04 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 27 May 2024 13:30:04 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 27 May 2024 13:30:04 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 27 May 2024 13:30:04 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 27 May 2024 13:30:04 GMT
VOLUME [/usr/local/xwiki]
# Mon, 27 May 2024 13:30:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 May 2024 13:30:04 GMT
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
	-	`sha256:63d9376e25e5ba92936ed244a6a17f40e0e94193fe0dc8f60206086fbde34bd1`  
		Last Modified: Wed, 05 Jun 2024 07:34:27 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a31be934b42c9438aabd8a3bf297a8128769973fb30856ff874bf74cfdbec92c`  
		Last Modified: Fri, 21 Jun 2024 01:40:29 GMT  
		Size: 12.5 MB (12454566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583af122ce35b5b703ea987b6b2abaf0bb387ca16647aff6f5743631487a2182`  
		Last Modified: Fri, 21 Jun 2024 01:40:28 GMT  
		Size: 456.8 KB (456818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51db09b79e04b8e82902c0ad98a2ce9d236e0dab599a4eaab3f45332e4f844c`  
		Last Modified: Fri, 21 Jun 2024 01:40:28 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3644095e00f1a3c270391eaad23c2370ee890d62b70f938a76c7b52c42afa90c`  
		Last Modified: Fri, 21 Jun 2024 12:01:56 GMT  
		Size: 173.5 MB (173486544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51e1827967fb8596f0e2232b304e2933505c121409964899ab9d7c35c5d9147a`  
		Last Modified: Fri, 21 Jun 2024 12:05:48 GMT  
		Size: 306.9 MB (306948748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2834f1c12b9e0eaeba6164ea3f966cbfabf2835bdab7b6e300a886dba392c38c`  
		Last Modified: Fri, 21 Jun 2024 12:07:47 GMT  
		Size: 620.0 KB (620001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1200de28b3c76d1613c7c08865fa04eb1eff889a2a9bc8bd4ae793c6beca8565`  
		Last Modified: Fri, 21 Jun 2024 12:07:47 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6619e274709e329dac45649bad2f223cb2b1b60a65b9121bf4e24b1603e7f96d`  
		Last Modified: Fri, 21 Jun 2024 12:07:47 GMT  
		Size: 2.3 KB (2309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad3ebd7b5083916c95feca381c012348088b4dbbf59ac0d797e4ac4f0f3dd6d`  
		Last Modified: Fri, 21 Jun 2024 12:07:47 GMT  
		Size: 6.4 KB (6417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3acc8f9e2945cba42dcf5866a9e5bd0b3d2db214f21c75c3af217572adb1b5b`  
		Last Modified: Fri, 21 Jun 2024 12:07:48 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:15-mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:d137a9ebe0516bdaf52e39f8ca412bb426b6e1f479bd72bf20c4eb10960e8700
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8933762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e11dff7950dc13b5980808c6173016d83e34acae66cd8cf67b641599432f7fc`

```dockerfile
```

-	Layers:
	-	`sha256:4f3303ebeec2402d0f0f381090d07b734bf3b15174291e9ebc1f7d79048b1cdb`  
		Last Modified: Fri, 21 Jun 2024 12:07:48 GMT  
		Size: 8.9 MB (8893461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b9ba6d28c44cd723da5e3254256f027d75ae5c9309eacfda36b201bbc01ada4`  
		Last Modified: Fri, 21 Jun 2024 12:07:47 GMT  
		Size: 40.3 KB (40301 bytes)  
		MIME: application/vnd.in-toto+json
