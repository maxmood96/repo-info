## `xwiki:14-mariadb-tomcat`

```console
$ docker pull xwiki@sha256:0188bcd0155138c683bb32b38d644447d3bea8dfcb40b8074368c6de8bccd80f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:14-mariadb-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:178a1221b79565fe6eb95fde993849d6cc5eb560ecab1b857c4fe68f9236c1ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.1 MB (596050768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b9e0bf094c406adf2020c4e32e139516d534c25787617b509b9251c1147c88f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 05 Dec 2023 14:34:12 GMT
ARG RELEASE
# Tue, 05 Dec 2023 14:34:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 05 Dec 2023 14:34:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 05 Dec 2023 14:34:12 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 05 Dec 2023 14:34:12 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Tue, 05 Dec 2023 14:34:12 GMT
CMD ["/bin/bash"]
# Tue, 05 Dec 2023 14:34:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 05 Dec 2023 14:34:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 14:34:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 05 Dec 2023 14:34:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Tue, 05 Dec 2023 14:34:12 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Tue, 05 Dec 2023 14:34:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 05 Dec 2023 14:34:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Tue, 05 Dec 2023 14:34:12 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Tue, 05 Dec 2023 14:34:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 05 Dec 2023 14:34:12 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 05 Dec 2023 14:34:12 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 14:34:12 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 05 Dec 2023 14:34:12 GMT
WORKDIR /usr/local/tomcat
# Tue, 05 Dec 2023 14:34:12 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 05 Dec 2023 14:34:12 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 05 Dec 2023 14:34:12 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 05 Dec 2023 14:34:12 GMT
ENV TOMCAT_MAJOR=9
# Tue, 05 Dec 2023 14:34:12 GMT
ENV TOMCAT_VERSION=9.0.85
# Tue, 05 Dec 2023 14:34:12 GMT
ENV TOMCAT_SHA512=06e239d15ff7b72017c1d0752ddb1be4651374f7c1391631ec5619f4981cb2911267bc6b044d6c71a2a74738f70d433b96418951439848121f1d874862ddd3de
# Tue, 05 Dec 2023 14:34:12 GMT
COPY dir:ed270554f73c50e3a5656608c6b46950600b8d6181b88100428b816ea0ba8f29 in /usr/local/tomcat 
# Tue, 05 Dec 2023 14:34:12 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Dec 2023 14:34:12 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 05 Dec 2023 14:34:12 GMT
EXPOSE 8080
# Tue, 05 Dec 2023 14:34:12 GMT
ENTRYPOINT []
# Tue, 05 Dec 2023 14:34:12 GMT
CMD ["catalina.sh" "run"]
# Tue, 05 Dec 2023 14:34:12 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 05 Dec 2023 14:34:12 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 05 Dec 2023 14:34:12 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 05 Dec 2023 14:34:12 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 05 Dec 2023 14:34:12 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 05 Dec 2023 14:34:12 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 05 Dec 2023 14:34:12 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 14:34:12 GMT
ENV XWIKI_VERSION=14.10.20
# Tue, 05 Dec 2023 14:34:12 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.20
# Tue, 05 Dec 2023 14:34:12 GMT
ENV XWIKI_DOWNLOAD_SHA256=c418601676d61893ccb9e066b1f2bcce56717b49e5c2456656b6960db6bd6e4c
# Tue, 05 Dec 2023 14:34:12 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Tue, 05 Dec 2023 14:34:12 GMT
ENV MARIADB_JDBC_VERSION=3.3.0
# Tue, 05 Dec 2023 14:34:12 GMT
ENV MARIADB_JDBC_SHA256=8262c79463e6b0932f60f55b61ca14087fdcafb117caa87259cd3a64409cd4fa
# Tue, 05 Dec 2023 14:34:12 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.3.0
# Tue, 05 Dec 2023 14:34:12 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.3.0.jar
# Tue, 05 Dec 2023 14:34:12 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.3.0.jar
# Tue, 05 Dec 2023 14:34:12 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Tue, 05 Dec 2023 14:34:12 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Tue, 05 Dec 2023 14:34:12 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Tue, 05 Dec 2023 14:34:12 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Tue, 05 Dec 2023 14:34:12 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 05 Dec 2023 14:34:12 GMT
VOLUME [/usr/local/xwiki]
# Tue, 05 Dec 2023 14:34:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Dec 2023 14:34:12 GMT
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
	-	`sha256:24c45e6545ce9cd3f123ff5fa607e0918c238e710afca97338e2bac26857b129`  
		Last Modified: Fri, 02 Feb 2024 13:55:29 GMT  
		Size: 178.3 MB (178348701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b810aba4e908706d4fce06263a130bf2d89211ae0234dae79cbe23c49b2d38a6`  
		Last Modified: Fri, 02 Feb 2024 13:55:30 GMT  
		Size: 309.2 MB (309150238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a5ed7acb3f67c5bc998d3e021828b0270a3d4f7e36835545380d7ddce63f347`  
		Last Modified: Fri, 02 Feb 2024 13:55:26 GMT  
		Size: 606.0 KB (605971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:911d40a4ae6239e73dc08b2c1a387fb9899e127d5ee382289709aadddd0b4d16`  
		Last Modified: Fri, 02 Feb 2024 13:55:26 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1411b761d2369d96dc1796b9d63cec06468313d4351f2e0ef29bafbbd749bc7b`  
		Last Modified: Fri, 02 Feb 2024 13:55:27 GMT  
		Size: 2.3 KB (2312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44061880d226454039ea88be250bb2183d51885c8da6be69fae396d624ec2e95`  
		Last Modified: Fri, 02 Feb 2024 13:55:27 GMT  
		Size: 6.1 KB (6130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f8309d32efffc28cf40d815e01bac41836a50d5dfd71ee8b75c4637c2dc093c`  
		Last Modified: Fri, 02 Feb 2024 13:55:28 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:14-mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:1093f40039133593d0e15590a5b1423489c25224e303ff0ac390ef330d409105
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8063194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:020326d51842aa8fb0cbe19dbdf736c47108515b2fe6b495596d5ba02bd67e51`

```dockerfile
```

-	Layers:
	-	`sha256:52bbbebab2d62f37300b76873e693673e0a6c081f0370e34539faef02da1e82e`  
		Last Modified: Fri, 02 Feb 2024 13:55:26 GMT  
		Size: 8.0 MB (8022502 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcae5ed046ffc2461241b2fed97794633253ff056cc2a6c1d854a0261b2393de`  
		Last Modified: Fri, 02 Feb 2024 13:55:26 GMT  
		Size: 40.7 KB (40692 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:14-mariadb-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:385669ddcf440e239cc889e16a2d3ff5d6e6c454a77f37333907cd46070afc3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.3 MB (592279877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19af22cdaf7cc83d141d654bcda00987fb06f9dfe63be9e0c29a9dfc133cf011`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 05 Dec 2023 14:34:12 GMT
ARG RELEASE
# Tue, 05 Dec 2023 14:34:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 05 Dec 2023 14:34:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 05 Dec 2023 14:34:12 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 05 Dec 2023 14:34:12 GMT
ADD file:5703a6689620ec495e864cfc12e80f8b2ee9e69b1a7b7365bf80955ba05a53ab in / 
# Tue, 05 Dec 2023 14:34:12 GMT
CMD ["/bin/bash"]
# Tue, 05 Dec 2023 14:34:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 05 Dec 2023 14:34:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 14:34:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 05 Dec 2023 14:34:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Tue, 05 Dec 2023 14:34:12 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Tue, 05 Dec 2023 14:34:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 05 Dec 2023 14:34:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Tue, 05 Dec 2023 14:34:12 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Tue, 05 Dec 2023 14:34:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 05 Dec 2023 14:34:12 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 05 Dec 2023 14:34:12 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 14:34:12 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 05 Dec 2023 14:34:12 GMT
WORKDIR /usr/local/tomcat
# Tue, 05 Dec 2023 14:34:12 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 05 Dec 2023 14:34:12 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 05 Dec 2023 14:34:12 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 05 Dec 2023 14:34:12 GMT
ENV TOMCAT_MAJOR=9
# Tue, 05 Dec 2023 14:34:12 GMT
ENV TOMCAT_VERSION=9.0.85
# Tue, 05 Dec 2023 14:34:12 GMT
ENV TOMCAT_SHA512=06e239d15ff7b72017c1d0752ddb1be4651374f7c1391631ec5619f4981cb2911267bc6b044d6c71a2a74738f70d433b96418951439848121f1d874862ddd3de
# Tue, 05 Dec 2023 14:34:12 GMT
COPY dir:fac5a5afc569d5adf17bf7792973d601dab2d975286add0d651627e7655eba99 in /usr/local/tomcat 
# Tue, 05 Dec 2023 14:34:12 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Dec 2023 14:34:12 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 05 Dec 2023 14:34:12 GMT
EXPOSE 8080
# Tue, 05 Dec 2023 14:34:12 GMT
ENTRYPOINT []
# Tue, 05 Dec 2023 14:34:12 GMT
CMD ["catalina.sh" "run"]
# Tue, 05 Dec 2023 14:34:12 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 05 Dec 2023 14:34:12 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 05 Dec 2023 14:34:12 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 05 Dec 2023 14:34:12 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 05 Dec 2023 14:34:12 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 05 Dec 2023 14:34:12 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 05 Dec 2023 14:34:12 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 14:34:12 GMT
ENV XWIKI_VERSION=14.10.20
# Tue, 05 Dec 2023 14:34:12 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.20
# Tue, 05 Dec 2023 14:34:12 GMT
ENV XWIKI_DOWNLOAD_SHA256=c418601676d61893ccb9e066b1f2bcce56717b49e5c2456656b6960db6bd6e4c
# Tue, 05 Dec 2023 14:34:12 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Tue, 05 Dec 2023 14:34:12 GMT
ENV MARIADB_JDBC_VERSION=3.3.0
# Tue, 05 Dec 2023 14:34:12 GMT
ENV MARIADB_JDBC_SHA256=8262c79463e6b0932f60f55b61ca14087fdcafb117caa87259cd3a64409cd4fa
# Tue, 05 Dec 2023 14:34:12 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.3.0
# Tue, 05 Dec 2023 14:34:12 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.3.0.jar
# Tue, 05 Dec 2023 14:34:12 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.3.0.jar
# Tue, 05 Dec 2023 14:34:12 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Tue, 05 Dec 2023 14:34:12 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Tue, 05 Dec 2023 14:34:12 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Tue, 05 Dec 2023 14:34:12 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Tue, 05 Dec 2023 14:34:12 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 05 Dec 2023 14:34:12 GMT
VOLUME [/usr/local/xwiki]
# Tue, 05 Dec 2023 14:34:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Dec 2023 14:34:12 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:bc8daefb9978b7f23cfc73ae68e998e85ee72a68588997321b1697cb0b9926df`  
		Last Modified: Thu, 11 Jan 2024 22:46:38 GMT  
		Size: 28.4 MB (28399616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6a2be6e4013cffcaae1614f67dca08e0c8d56b9d2da9051ae71c48b43a409a`  
		Last Modified: Wed, 17 Jan 2024 07:02:15 GMT  
		Size: 18.9 MB (18860096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c758562b2b3e61329aca1af5bb5fa0700d9b5f7cf4e68faa8e2235d15dccfd1a`  
		Last Modified: Wed, 24 Jan 2024 20:52:24 GMT  
		Size: 46.6 MB (46639344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12285b9bc0b75c36f5f58bb0cba487613706fb4718325baccbf6a0d2eb157be6`  
		Last Modified: Wed, 24 Jan 2024 20:52:19 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c24226ebd43098c00c6e2715c22788dde6531777752b1ae35e81c95623edeae`  
		Last Modified: Thu, 25 Jan 2024 19:43:16 GMT  
		Size: 733.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:291d1cfe01ca64a1f4b5ce99e3952e5e9f33883e28003c8338a45a3c4591524d`  
		Last Modified: Thu, 25 Jan 2024 21:51:33 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2409b92e56bb07b3bc3a5f86040c6de2c6d4bb8aff746ebd680937b280c4f9c3`  
		Last Modified: Thu, 25 Jan 2024 21:54:31 GMT  
		Size: 12.4 MB (12412630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34fe23bd787b1047bcc544af859234e454dc5cb060fdb6efa3033727bf767ac7`  
		Last Modified: Thu, 25 Jan 2024 21:54:31 GMT  
		Size: 2.8 MB (2811661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f6955886a62584457ae226ac9598bdb10f499bb2204bbd2c1999ffc6aa02377`  
		Last Modified: Thu, 25 Jan 2024 21:54:30 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d9efa9df242bc17ee07972380af06a565c6de3eae9d3f59a66d44b65907397`  
		Last Modified: Fri, 26 Jan 2024 17:47:51 GMT  
		Size: 173.4 MB (173386840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e81a4f1717a058d90608a375f79f480c0faf81cb35de58b42e54b2ca25b73df7`  
		Last Modified: Fri, 26 Jan 2024 18:35:52 GMT  
		Size: 309.2 MB (309150305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e645abaa85d184b9e194538f3496d001d23d6f0f890adbfe0e7bf810983b0aad`  
		Last Modified: Fri, 26 Jan 2024 18:39:10 GMT  
		Size: 606.0 KB (605966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec52a0e1c8801674b192da8d9135b7c62d6aa94c9992bbb9d0d4414df5c2fcd`  
		Last Modified: Fri, 26 Jan 2024 18:39:10 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9ef20349713308aa7738c8599dd88e0ae306970756a64499585244d4e3f7f5`  
		Last Modified: Fri, 26 Jan 2024 18:39:11 GMT  
		Size: 2.3 KB (2312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba16f90162fbb9ea17f7703ad0501b039d5b01530beb6dc66887a1aa5b902d`  
		Last Modified: Fri, 26 Jan 2024 18:39:11 GMT  
		Size: 6.1 KB (6129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5ed950d8aabf5afeaa93b8b1c168ddb75827f6dc4f3ddc2177646d5245f863`  
		Last Modified: Fri, 26 Jan 2024 18:39:11 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:14-mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:7739a143161090edc03114a5334340fd8a9be44f1580e7b37c82aed0a630a26b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8147510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc32e55240818dc6c77608363da1c6c7a151deb25104c3aa755f933dc092cd84`

```dockerfile
```

-	Layers:
	-	`sha256:78c7269ddce65f81e1465923b4bd1985914b23af54a1570ef1b36c525d3c4e94`  
		Last Modified: Fri, 26 Jan 2024 18:39:11 GMT  
		Size: 8.1 MB (8108267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4534e3b61be7388e57d62da71e7be970332cf6f1c7f6826585f7750175330d3`  
		Last Modified: Fri, 26 Jan 2024 18:39:10 GMT  
		Size: 39.2 KB (39243 bytes)  
		MIME: application/vnd.in-toto+json
