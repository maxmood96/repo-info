## `xwiki:15-postgres-tomcat`

```console
$ docker pull xwiki@sha256:3a8e19ba79afe9e7308259d10558b875378fb8943a213456fc643d4950db241d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:15-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:cb4b9616dd542f5e03e0e8b4b90126952546e4a5f2fdfdd50d48ddefd4e9c9dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.1 MB (595141691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2a2f91e5fcf51597f50321de4a8e4122cf1117f4107e4f5da71996976b7d5a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 17 Jan 2024 13:37:13 GMT
ARG RELEASE
# Wed, 17 Jan 2024 13:37:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Jan 2024 13:37:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Jan 2024 13:37:13 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Jan 2024 13:37:13 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Wed, 17 Jan 2024 13:37:13 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 13:37:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 13:37:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 13:37:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 17 Jan 2024 13:37:13 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 13:37:13 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 17 Jan 2024 13:37:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 17 Jan 2024 13:37:13 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 17 Jan 2024 13:37:13 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 17 Jan 2024 13:37:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 17 Jan 2024 13:37:13 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 17 Jan 2024 13:37:13 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 13:37:13 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 17 Jan 2024 13:37:13 GMT
WORKDIR /usr/local/tomcat
# Wed, 17 Jan 2024 13:37:13 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 17 Jan 2024 13:37:13 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 17 Jan 2024 13:37:13 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 17 Jan 2024 13:37:13 GMT
ENV TOMCAT_MAJOR=9
# Wed, 17 Jan 2024 13:37:13 GMT
ENV TOMCAT_VERSION=9.0.85
# Wed, 17 Jan 2024 13:37:13 GMT
ENV TOMCAT_SHA512=06e239d15ff7b72017c1d0752ddb1be4651374f7c1391631ec5619f4981cb2911267bc6b044d6c71a2a74738f70d433b96418951439848121f1d874862ddd3de
# Wed, 17 Jan 2024 13:37:13 GMT
COPY dir:ed270554f73c50e3a5656608c6b46950600b8d6181b88100428b816ea0ba8f29 in /usr/local/tomcat 
# Wed, 17 Jan 2024 13:37:13 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 13:37:13 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 17 Jan 2024 13:37:13 GMT
EXPOSE 8080
# Wed, 17 Jan 2024 13:37:13 GMT
ENTRYPOINT []
# Wed, 17 Jan 2024 13:37:13 GMT
CMD ["catalina.sh" "run"]
# Wed, 17 Jan 2024 13:37:13 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 17 Jan 2024 13:37:13 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 17 Jan 2024 13:37:13 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 17 Jan 2024 13:37:13 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 17 Jan 2024 13:37:13 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 17 Jan 2024 13:37:13 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 17 Jan 2024 13:37:13 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Jan 2024 13:37:13 GMT
ENV XWIKI_VERSION=15.10.5
# Wed, 17 Jan 2024 13:37:13 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.10.5
# Wed, 17 Jan 2024 13:37:13 GMT
ENV XWIKI_DOWNLOAD_SHA256=3775334377ae7fb8bcf6a21e6eb099a8cfbea43044dc0716c01cb3b5117988a2
# Wed, 17 Jan 2024 13:37:13 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Wed, 17 Jan 2024 13:37:13 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/ # buildkit
# Wed, 17 Jan 2024 13:37:13 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Wed, 17 Jan 2024 13:37:13 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Wed, 17 Jan 2024 13:37:13 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Wed, 17 Jan 2024 13:37:13 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 17 Jan 2024 13:37:13 GMT
VOLUME [/usr/local/xwiki]
# Wed, 17 Jan 2024 13:37:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jan 2024 13:37:13 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:31bd5f451a847d651a0996256753a9b22a6ea8c65fefb010e77ea9c839fe2fac`  
		Last Modified: Thu, 25 Jan 2024 22:24:23 GMT  
		Size: 30.4 MB (30447882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26611c45681a8966387aee7b2e1494405e20bc5a46dc5da0af9228c45f8e8ec4`  
		Last Modified: Fri, 02 Feb 2024 07:50:10 GMT  
		Size: 17.5 MB (17458288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7657bba016afbc9b5b668492429479081862469157560f39c722fca733c6a4e7`  
		Last Modified: Fri, 02 Feb 2024 07:50:54 GMT  
		Size: 47.2 MB (47163193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c532b683186e5e796b6523fee32e214bd7eeda453b630d2322010697be91e8`  
		Last Modified: Fri, 02 Feb 2024 07:50:48 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e11da758202f5d3e080b1205b5f37c11a0ca72e8d428ba219b7d9d99befe18`  
		Last Modified: Fri, 02 Feb 2024 07:50:48 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd1e7b220ba3bc44242e84f32e06eafd9c47254bbdd6b0ca7ac59136fd3cc28`  
		Last Modified: Fri, 02 Feb 2024 12:48:13 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:409c34fdacf9278997b113c19cdc80caa870ab5867031e594c30e04e5e1d38db`  
		Last Modified: Fri, 02 Feb 2024 12:51:23 GMT  
		Size: 12.4 MB (12404639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f12e6d794f03fb4ed68877f5cf7aca8ddd07a22ae7314cae1c4d0868f0fd10c4`  
		Last Modified: Fri, 02 Feb 2024 12:51:22 GMT  
		Size: 458.4 KB (458434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43a9f7464929af5d153eb3dfdbc9a8c606a5bc8f62d8582116fb1be197657ff`  
		Last Modified: Fri, 02 Feb 2024 12:51:21 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55fea62acf1c8f33bb7dd07adf0cd44d42117b4a3ad12d538300484426b62a3e`  
		Last Modified: Fri, 02 Feb 2024 13:55:51 GMT  
		Size: 179.3 MB (179291553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e1ae1b7aa53c42514bd2dc6456e325c653542b02f76c12edad2946ac599ab6`  
		Last Modified: Fri, 02 Feb 2024 13:55:53 GMT  
		Size: 307.0 MB (306967005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acbe5b35efc13f2f090d1b7523f22b7767e4558cc9f892ef1d6236066fe215c3`  
		Last Modified: Fri, 02 Feb 2024 13:55:47 GMT  
		Size: 936.8 KB (936847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a9347a41abe21b4d32475a4a0074c87ee27d8d0b179151c2daa75f9f8dcd29a`  
		Last Modified: Fri, 02 Feb 2024 13:55:46 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1db63abd2e5cb55072b725f3ca71f0251fc0245cea90047144994b04db5d050`  
		Last Modified: Fri, 02 Feb 2024 13:55:48 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dda307e1514d6cfe6044208d0583dab4bb258c46dd9c4d8103534325212584e`  
		Last Modified: Fri, 02 Feb 2024 13:55:48 GMT  
		Size: 6.4 KB (6414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aae35844e66d5a28b704392952591c301edaf279fab6506f53b758d4232c196`  
		Last Modified: Fri, 02 Feb 2024 13:55:49 GMT  
		Size: 2.4 KB (2435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:15-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:6657931e4f34a2c5fdb48491c601d26785832b9968629b579db3b0402aaa91dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8085319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9727a5a729eda9c52456e838e55205101852796c8595a9ccd08a443366fd917`

```dockerfile
```

-	Layers:
	-	`sha256:fa4354b76a2b299f4d262e6359aa6383af8ff8c5b026687246a88aecdc259954`  
		Last Modified: Fri, 02 Feb 2024 13:55:48 GMT  
		Size: 8.0 MB (8045539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d1dc4d3ab4515f06ddb4e6cc1e23abeaf0f0c65aa71319996e8a0c703cd2df0`  
		Last Modified: Fri, 02 Feb 2024 13:55:46 GMT  
		Size: 39.8 KB (39780 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:15-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:ec6644851b8dde9a3f86f55388e49a452bcdfc7e33a03647592165edc5caf929
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.0 MB (589016277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32c62c80f87a3e4e5f684983705d98839f268307b3567bd728eb8399fab7cfb7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 17 Jan 2024 13:37:13 GMT
ARG RELEASE
# Wed, 17 Jan 2024 13:37:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Jan 2024 13:37:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Jan 2024 13:37:13 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Jan 2024 13:37:13 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Wed, 17 Jan 2024 13:37:13 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 13:37:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 13:37:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 13:37:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 17 Jan 2024 13:37:13 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 13:37:13 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 17 Jan 2024 13:37:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 17 Jan 2024 13:37:13 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 17 Jan 2024 13:37:13 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 17 Jan 2024 13:37:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 17 Jan 2024 13:37:13 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 17 Jan 2024 13:37:13 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 13:37:13 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 17 Jan 2024 13:37:13 GMT
WORKDIR /usr/local/tomcat
# Wed, 17 Jan 2024 13:37:13 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 17 Jan 2024 13:37:13 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 17 Jan 2024 13:37:13 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 17 Jan 2024 13:37:13 GMT
ENV TOMCAT_MAJOR=9
# Wed, 17 Jan 2024 13:37:13 GMT
ENV TOMCAT_VERSION=9.0.85
# Wed, 17 Jan 2024 13:37:13 GMT
ENV TOMCAT_SHA512=06e239d15ff7b72017c1d0752ddb1be4651374f7c1391631ec5619f4981cb2911267bc6b044d6c71a2a74738f70d433b96418951439848121f1d874862ddd3de
# Wed, 17 Jan 2024 13:37:13 GMT
COPY dir:101a21f8290e4b799c9f99499662dfc86926aa66787150c02f8bb6cc272d7fbd in /usr/local/tomcat 
# Wed, 17 Jan 2024 13:37:13 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 13:37:13 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 17 Jan 2024 13:37:13 GMT
EXPOSE 8080
# Wed, 17 Jan 2024 13:37:13 GMT
ENTRYPOINT []
# Wed, 17 Jan 2024 13:37:13 GMT
CMD ["catalina.sh" "run"]
# Wed, 17 Jan 2024 13:37:13 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 17 Jan 2024 13:37:13 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 17 Jan 2024 13:37:13 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 17 Jan 2024 13:37:13 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 17 Jan 2024 13:37:13 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 17 Jan 2024 13:37:13 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 17 Jan 2024 13:37:13 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Jan 2024 13:37:13 GMT
ENV XWIKI_VERSION=15.10.5
# Wed, 17 Jan 2024 13:37:13 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.10.5
# Wed, 17 Jan 2024 13:37:13 GMT
ENV XWIKI_DOWNLOAD_SHA256=3775334377ae7fb8bcf6a21e6eb099a8cfbea43044dc0716c01cb3b5117988a2
# Wed, 17 Jan 2024 13:37:13 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Wed, 17 Jan 2024 13:37:13 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/ # buildkit
# Wed, 17 Jan 2024 13:37:13 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Wed, 17 Jan 2024 13:37:13 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Wed, 17 Jan 2024 13:37:13 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Wed, 17 Jan 2024 13:37:13 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 17 Jan 2024 13:37:13 GMT
VOLUME [/usr/local/xwiki]
# Wed, 17 Jan 2024 13:37:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jan 2024 13:37:13 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:b90a30ba7a05123de8a1e1661ed0ddb6563ad55ca11133e21e3d19f7e6bce76a`  
		Last Modified: Fri, 26 Jan 2024 01:55:46 GMT  
		Size: 28.4 MB (28400102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d031894e4c0411af099ca88f2f4707adffb7144d8d3dc5d40457cededf240b5`  
		Last Modified: Fri, 02 Feb 2024 02:16:39 GMT  
		Size: 18.9 MB (18860666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a0007a9ef9bab7b317a14a0d8594647e9c47755fcb79f9fa388e560fab31690`  
		Last Modified: Fri, 02 Feb 2024 02:17:22 GMT  
		Size: 46.6 MB (46639311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917c6cc534cfc01e73da456384906c210ffa86f1df265b8ee7255561e2a7c5fa`  
		Last Modified: Fri, 02 Feb 2024 02:17:17 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7a0f038262842ffcfdab428e9f3a7a1d0dc2e49da53bdde76335cbc0c02b48`  
		Last Modified: Fri, 02 Feb 2024 02:17:17 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a15ffd3ea890ff20384b9803dee407357a8063bb1239abcfde036e1a2a22e17`  
		Last Modified: Fri, 02 Feb 2024 04:11:33 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7fe4808aaf16dbfd9e06055aba830d84eeb10946e56fb1429c81250ccce8836`  
		Last Modified: Fri, 02 Feb 2024 04:14:44 GMT  
		Size: 12.4 MB (12412651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222ea8a7cf368a3f03e7389c6a6b4e2bcfe1618378bd14046880ee212f0336f7`  
		Last Modified: Fri, 02 Feb 2024 04:14:43 GMT  
		Size: 457.1 KB (457148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c004c0bb331fe8e89ab0554e93da2d81f4f5482a473b6c68864b87330da9ab`  
		Last Modified: Fri, 02 Feb 2024 04:14:43 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62372099d3b5d6e754af501f3bac1c2e39cf50157d1049a45547080c239b625`  
		Last Modified: Sat, 03 Feb 2024 11:33:50 GMT  
		Size: 174.3 MB (174328656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7c72157558324b0663f82ab8494ced9dc35e36503483799254ee40521affcc9`  
		Last Modified: Sat, 03 Feb 2024 11:37:31 GMT  
		Size: 307.0 MB (306967049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b1a7d95251f2a74a6d321b75b2bde05a9ccc09e3a571ad168252eb7f8d057b`  
		Last Modified: Sat, 03 Feb 2024 11:37:25 GMT  
		Size: 936.9 KB (936852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22c4e966b796837489f1196898d38ed6e361efb112b391db8818514401079c6d`  
		Last Modified: Sat, 03 Feb 2024 11:37:25 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc0ac33c82b2d9e0f4733af3f1acbb2ddfe25e084a6394fdf3ee57288c370e2d`  
		Last Modified: Sat, 03 Feb 2024 11:37:25 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95b8c088f0832b39bcf58f5ff424bdf455b39dce1b633dacbba92525fa5397d`  
		Last Modified: Sat, 03 Feb 2024 11:37:26 GMT  
		Size: 6.4 KB (6418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e66ecad195ae80acf541adadeeb4a6a2e46596a71f593f2139db90031800b37`  
		Last Modified: Sat, 03 Feb 2024 11:37:26 GMT  
		Size: 2.4 KB (2429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:15-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:f8e5b9e8794369469c44fccfa450eeeeb6ae2ac14f3454a6ad5d03a8016775f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8190366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9c441376786647f9288b1cf883e4c28f74cd8e217ca2f5d4df9f4416473bdd7`

```dockerfile
```

-	Layers:
	-	`sha256:8b7cbbd909acb350f955de47db0cd80d4fa6903df67a0db8e89d4310b4ba6241`  
		Last Modified: Sat, 03 Feb 2024 11:37:25 GMT  
		Size: 8.2 MB (8152039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbbfacabbb0a5c51ba3ea4c86f677083313a695bd4c74392fe816eb422124977`  
		Last Modified: Sat, 03 Feb 2024 11:37:24 GMT  
		Size: 38.3 KB (38327 bytes)  
		MIME: application/vnd.in-toto+json
