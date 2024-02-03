## `xwiki:mariadb-tomcat`

```console
$ docker pull xwiki@sha256:04eeac1f352f4d16879170ac3f23263536b31b891c9497d8bc3dc09d1ebe693b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:mariadb-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:c4ba9ce959693dd4034fa9449b0d2195779cb2c1c6fec0413823fedfcb1c991e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **593.7 MB (593661700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16131ec737da4769665b11a4b32d42048d3ee0f962301e83b4ef85a7115c83f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 25 Jan 2024 17:54:38 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:54:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:54:40 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Thu, 25 Jan 2024 17:54:41 GMT
CMD ["/bin/bash"]
# Mon, 29 Jan 2024 16:20:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 29 Jan 2024 16:20:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Jan 2024 16:20:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 29 Jan 2024 16:20:26 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Mon, 29 Jan 2024 16:20:26 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Mon, 29 Jan 2024 16:20:26 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Mon, 29 Jan 2024 16:20:26 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Mon, 29 Jan 2024 16:20:26 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Mon, 29 Jan 2024 16:20:26 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 29 Jan 2024 16:20:26 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 29 Jan 2024 16:20:26 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Jan 2024 16:20:26 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 29 Jan 2024 16:20:26 GMT
WORKDIR /usr/local/tomcat
# Mon, 29 Jan 2024 16:20:26 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 29 Jan 2024 16:20:26 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 29 Jan 2024 16:20:26 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Mon, 29 Jan 2024 16:20:26 GMT
ENV TOMCAT_MAJOR=9
# Mon, 29 Jan 2024 16:20:26 GMT
ENV TOMCAT_VERSION=9.0.85
# Mon, 29 Jan 2024 16:20:26 GMT
ENV TOMCAT_SHA512=06e239d15ff7b72017c1d0752ddb1be4651374f7c1391631ec5619f4981cb2911267bc6b044d6c71a2a74738f70d433b96418951439848121f1d874862ddd3de
# Mon, 29 Jan 2024 16:20:26 GMT
COPY dir:ed270554f73c50e3a5656608c6b46950600b8d6181b88100428b816ea0ba8f29 in /usr/local/tomcat 
# Mon, 29 Jan 2024 16:20:26 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Mon, 29 Jan 2024 16:20:26 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Mon, 29 Jan 2024 16:20:26 GMT
EXPOSE 8080
# Mon, 29 Jan 2024 16:20:26 GMT
ENTRYPOINT []
# Mon, 29 Jan 2024 16:20:26 GMT
CMD ["catalina.sh" "run"]
# Mon, 29 Jan 2024 16:20:26 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 29 Jan 2024 16:20:26 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 29 Jan 2024 16:20:26 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 29 Jan 2024 16:20:26 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 29 Jan 2024 16:20:26 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 29 Jan 2024 16:20:26 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 29 Jan 2024 16:20:26 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Jan 2024 16:20:26 GMT
ENV XWIKI_VERSION=16.0.0
# Mon, 29 Jan 2024 16:20:26 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.0.0
# Mon, 29 Jan 2024 16:20:26 GMT
ENV XWIKI_DOWNLOAD_SHA256=955c175d0ac0e7039eeafd8569d87ad8a7967092ad8d018decb80a42a7eb941f
# Mon, 29 Jan 2024 16:20:26 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 29 Jan 2024 16:20:26 GMT
ENV MARIADB_JDBC_VERSION=3.3.2
# Mon, 29 Jan 2024 16:20:26 GMT
ENV MARIADB_JDBC_SHA256=2a67ef3cc1ca481965a0e7f2d4174d126f3464d02b4055a441261fad8c196769
# Mon, 29 Jan 2024 16:20:26 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.3.2
# Mon, 29 Jan 2024 16:20:26 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.3.2.jar
# Mon, 29 Jan 2024 16:20:26 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.3.2.jar
# Mon, 29 Jan 2024 16:20:26 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Mon, 29 Jan 2024 16:20:26 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 29 Jan 2024 16:20:26 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 29 Jan 2024 16:20:26 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 29 Jan 2024 16:20:26 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 29 Jan 2024 16:20:26 GMT
VOLUME [/usr/local/xwiki]
# Mon, 29 Jan 2024 16:20:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jan 2024 16:20:26 GMT
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
	-	`sha256:bdf7a48c96fa8b2dfb5a8b8ef4b33f6dafea0cc503d58c216a8c40c306e03c8b`  
		Last Modified: Fri, 02 Feb 2024 13:55:25 GMT  
		Size: 178.3 MB (178348760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f9dea6785d88eb56a4a773b3fc1d0b239b0fb57d1b6fd8b21cfdf501898ae0`  
		Last Modified: Fri, 02 Feb 2024 13:55:29 GMT  
		Size: 306.8 MB (306751655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe386e23620572b6fab0a692475642fcebc9d34eedb6c4495728cac9d239ddbd`  
		Last Modified: Fri, 02 Feb 2024 13:55:24 GMT  
		Size: 615.1 KB (615137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7154dd5c6bc8b275080b4967f1560d08ced0370292f4159412fdebfb1309baed`  
		Last Modified: Fri, 02 Feb 2024 13:55:24 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad8e0a573dafe3eb66279e02f04abb4d1e3c45c081020cf86b474996ea39ac77`  
		Last Modified: Fri, 02 Feb 2024 13:55:25 GMT  
		Size: 2.3 KB (2311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60837c2a6c4a92dc9eb0226c931468b62107d52e7c7551147fa33cc6d91ddec`  
		Last Modified: Fri, 02 Feb 2024 13:55:25 GMT  
		Size: 6.4 KB (6423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb27a5b1ba2ccb98f017187f60a7e5a1c6ec385157af3402481591c6825b46f`  
		Last Modified: Fri, 02 Feb 2024 13:55:26 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:5749254544acac355842960ba67db3609c66844b2b0c19b51c9a3ff164aa5e0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8075796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:892e4ffefa1073d09da51aa5dc3070c31159876e1f5a460059b6e2611d812094`

```dockerfile
```

-	Layers:
	-	`sha256:9542729f46264630cbbf8a5f761629e539c85c085de4154b33b7b386e72e426c`  
		Last Modified: Fri, 02 Feb 2024 13:55:22 GMT  
		Size: 8.0 MB (8034173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23901f490dccef4e3228f2635d2dcfee113d6efd8159255eaf6c0e9ebd87e8b8`  
		Last Modified: Fri, 02 Feb 2024 13:55:22 GMT  
		Size: 41.6 KB (41623 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:mariadb-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:be2cacc46ff8e6b997a99a6e4bc84c7d3da87f38511e3e9bf495fa6334399d31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.9 MB (589890691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd109a0e4a1924ee9355c124cea9be55938b335256b1b1448ec951713b2891f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 11 Jan 2024 17:03:13 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:03:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:03:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:03:13 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:03:15 GMT
ADD file:5703a6689620ec495e864cfc12e80f8b2ee9e69b1a7b7365bf80955ba05a53ab in / 
# Thu, 11 Jan 2024 17:03:15 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 06:57:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 06:57:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 06:57:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 17 Jan 2024 06:59:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:42:30 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 24 Jan 2024 20:43:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 20:43:49 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Thu, 25 Jan 2024 19:40:09 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Thu, 25 Jan 2024 19:40:09 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 21:36:23 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 25 Jan 2024 21:36:23 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 21:36:24 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 25 Jan 2024 21:36:24 GMT
WORKDIR /usr/local/tomcat
# Thu, 25 Jan 2024 21:36:24 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 25 Jan 2024 21:36:24 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 25 Jan 2024 21:38:22 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 25 Jan 2024 21:38:22 GMT
ENV TOMCAT_MAJOR=9
# Thu, 25 Jan 2024 21:38:22 GMT
ENV TOMCAT_VERSION=9.0.85
# Thu, 25 Jan 2024 21:38:22 GMT
ENV TOMCAT_SHA512=06e239d15ff7b72017c1d0752ddb1be4651374f7c1391631ec5619f4981cb2911267bc6b044d6c71a2a74738f70d433b96418951439848121f1d874862ddd3de
# Thu, 25 Jan 2024 21:38:22 GMT
COPY dir:fac5a5afc569d5adf17bf7792973d601dab2d975286add0d651627e7655eba99 in /usr/local/tomcat 
# Thu, 25 Jan 2024 21:38:26 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 21:38:27 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 25 Jan 2024 21:38:27 GMT
EXPOSE 8080
# Thu, 25 Jan 2024 21:38:27 GMT
ENTRYPOINT []
# Thu, 25 Jan 2024 21:38:28 GMT
CMD ["catalina.sh" "run"]
# Mon, 29 Jan 2024 16:20:26 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 29 Jan 2024 16:20:26 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 29 Jan 2024 16:20:26 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 29 Jan 2024 16:20:26 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 29 Jan 2024 16:20:26 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 29 Jan 2024 16:20:26 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 29 Jan 2024 16:20:26 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Jan 2024 16:20:26 GMT
ENV XWIKI_VERSION=16.0.0
# Mon, 29 Jan 2024 16:20:26 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.0.0
# Mon, 29 Jan 2024 16:20:26 GMT
ENV XWIKI_DOWNLOAD_SHA256=955c175d0ac0e7039eeafd8569d87ad8a7967092ad8d018decb80a42a7eb941f
# Mon, 29 Jan 2024 16:20:26 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 29 Jan 2024 16:20:26 GMT
ENV MARIADB_JDBC_VERSION=3.3.2
# Mon, 29 Jan 2024 16:20:26 GMT
ENV MARIADB_JDBC_SHA256=2a67ef3cc1ca481965a0e7f2d4174d126f3464d02b4055a441261fad8c196769
# Mon, 29 Jan 2024 16:20:26 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.3.2
# Mon, 29 Jan 2024 16:20:26 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.3.2.jar
# Mon, 29 Jan 2024 16:20:26 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.3.2.jar
# Mon, 29 Jan 2024 16:20:26 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Mon, 29 Jan 2024 16:20:26 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 29 Jan 2024 16:20:26 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 29 Jan 2024 16:20:26 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 29 Jan 2024 16:20:26 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 29 Jan 2024 16:20:26 GMT
VOLUME [/usr/local/xwiki]
# Mon, 29 Jan 2024 16:20:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jan 2024 16:20:26 GMT
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
	-	`sha256:5f18f6a1285d2bb5e61233269e3f214b971605be98d70901dddf58e299b18f65`  
		Last Modified: Mon, 29 Jan 2024 21:38:09 GMT  
		Size: 306.8 MB (306751642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:910ce676f64f9427a810b907b305ae4787a467242190f866ac6477c77900cb12`  
		Last Modified: Mon, 29 Jan 2024 21:40:37 GMT  
		Size: 615.1 KB (615141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b67918cfe9c18d17d5bac792604d37f328190083977d2f10cabaf249d4135101`  
		Last Modified: Mon, 29 Jan 2024 21:40:37 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb432c9c7449fd7b60c528438ba89f7f40672e1e82d8bc9a7c44cfa594aa6cd`  
		Last Modified: Mon, 29 Jan 2024 21:40:37 GMT  
		Size: 2.3 KB (2313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aae61b133bc0a044764b8cca432ba0bf4da573ede1f8a05ea0d36c8ff872153`  
		Last Modified: Mon, 29 Jan 2024 21:40:38 GMT  
		Size: 6.4 KB (6427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8da2a2217a3a9ac7f31fd9e0974f7d5fbfa10282cb4d8f8eeb91bbffb71e9b8`  
		Last Modified: Mon, 29 Jan 2024 21:40:38 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:6e43168f1f236d58995cbee52c702e918f0e1ebd7b172dfb7d0142ad9df9a925
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8160125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f058cccd3ca9bb3247a5a242beccc23cc26665eac9e8774c2d266c4e4d08adb9`

```dockerfile
```

-	Layers:
	-	`sha256:85fa9319c2d4d0228657bb688f8c6bc8735d11a26f85d4162c8602d630082bb0`  
		Last Modified: Mon, 29 Jan 2024 21:40:37 GMT  
		Size: 8.1 MB (8119944 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc4eb544c82eb78a181708bd4f60e7ee9746ff3a1ddca080b7fcb35a95a015ca`  
		Last Modified: Mon, 29 Jan 2024 21:40:37 GMT  
		Size: 40.2 KB (40181 bytes)  
		MIME: application/vnd.in-toto+json
