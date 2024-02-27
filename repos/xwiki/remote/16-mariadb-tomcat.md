## `xwiki:16-mariadb-tomcat`

```console
$ docker pull xwiki@sha256:5e6784be79b05ce64846e2c5558ffff0176a37ec36d608ab8a655a95440c75a8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:16-mariadb-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:21260beaa33936ccbfd3a09f8b7b27dc30f1d245c69262b54ec400cd2da11ab4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **593.8 MB (593802701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ca5a11440c448a4522eee675632ea7982f7e7dc159af3b5a44820e6e4820f2a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 01:38:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Feb 2024 01:38:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 01:38:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Feb 2024 01:40:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 01:40:28 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Fri, 16 Feb 2024 01:40:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Feb 2024 01:41:00 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Fri, 16 Feb 2024 01:41:00 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 16 Feb 2024 01:41:00 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Feb 2024 04:48:48 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 16 Feb 2024 04:48:48 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 04:48:48 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 16 Feb 2024 04:48:48 GMT
WORKDIR /usr/local/tomcat
# Fri, 16 Feb 2024 04:48:48 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 16 Feb 2024 04:48:48 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 16 Feb 2024 04:51:21 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 16 Feb 2024 04:51:22 GMT
ENV TOMCAT_MAJOR=9
# Wed, 21 Feb 2024 01:09:17 GMT
ENV TOMCAT_VERSION=9.0.86
# Wed, 21 Feb 2024 01:09:17 GMT
ENV TOMCAT_SHA512=e8a8000dbeba5ee266ec4bf77217574364ffd114c8b913816f2e7a5e4eab4d01d0be3f05c8fccefcb5c5d770308efe1983be80279b6ef6d122d6183288a8ee9c
# Wed, 21 Feb 2024 01:09:18 GMT
COPY dir:1817f6b73a6fe4d923d7f6cf1aa21c95626eef42af1889e1d0a51c69d1ecc970 in /usr/local/tomcat 
# Wed, 21 Feb 2024 01:09:22 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Feb 2024 01:09:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 21 Feb 2024 01:09:23 GMT
EXPOSE 8080
# Wed, 21 Feb 2024 01:09:23 GMT
ENTRYPOINT []
# Wed, 21 Feb 2024 01:09:23 GMT
CMD ["catalina.sh" "run"]
# Mon, 26 Feb 2024 13:14:55 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 26 Feb 2024 13:14:55 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 26 Feb 2024 13:14:55 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 26 Feb 2024 13:14:55 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 26 Feb 2024 13:14:55 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 26 Feb 2024 13:14:55 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 26 Feb 2024 13:14:55 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Feb 2024 13:14:55 GMT
ENV XWIKI_VERSION=16.1.0
# Mon, 26 Feb 2024 13:14:55 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.1.0
# Mon, 26 Feb 2024 13:14:55 GMT
ENV XWIKI_DOWNLOAD_SHA256=e236fc101710a0bfefed2328cc66652e265f21ab40dd30e6b7ce52300da744d5
# Mon, 26 Feb 2024 13:14:55 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 26 Feb 2024 13:14:55 GMT
ENV MARIADB_JDBC_VERSION=3.3.2
# Mon, 26 Feb 2024 13:14:55 GMT
ENV MARIADB_JDBC_SHA256=2a67ef3cc1ca481965a0e7f2d4174d126f3464d02b4055a441261fad8c196769
# Mon, 26 Feb 2024 13:14:55 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.3.2
# Mon, 26 Feb 2024 13:14:55 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.3.2.jar
# Mon, 26 Feb 2024 13:14:55 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.3.2.jar
# Mon, 26 Feb 2024 13:14:55 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Mon, 26 Feb 2024 13:14:55 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 26 Feb 2024 13:14:55 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 26 Feb 2024 13:14:55 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 26 Feb 2024 13:14:55 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 26 Feb 2024 13:14:55 GMT
VOLUME [/usr/local/xwiki]
# Mon, 26 Feb 2024 13:14:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Feb 2024 13:14:55 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f947fdc0fc4be68d9f9c4c3912a92df875230cdd8267c01077167a69114f54`  
		Last Modified: Fri, 16 Feb 2024 01:44:10 GMT  
		Size: 17.5 MB (17458484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5374706a264d34f054909a042d958bf140f3624be56e6ca8ee2bd40c4650ae91`  
		Last Modified: Fri, 16 Feb 2024 01:44:40 GMT  
		Size: 47.2 MB (47163245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9aeff6b625d796ae065d95dd069d3f2c999314b436332616a6e3b9397038891`  
		Last Modified: Fri, 16 Feb 2024 01:44:33 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82faf7b7220dc5dd434962b0d3b1d9f4630792cabb13615559a9cf093d4afb88`  
		Last Modified: Fri, 16 Feb 2024 01:44:33 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b633af09da77b3268755d4a1d9c430a50ad0a131e1b2ecdb997e3ee6a86978f`  
		Last Modified: Fri, 16 Feb 2024 05:02:20 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54fc5dc00b8a0ff1c4c96565d5c87fa8e9aa254b3047454ba5a19d4a2a834043`  
		Last Modified: Wed, 21 Feb 2024 01:34:35 GMT  
		Size: 12.4 MB (12411786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f377b6536232adf2c23b2d9282473726a58f99a99ec67aed49905d42011cec4`  
		Last Modified: Wed, 21 Feb 2024 01:34:33 GMT  
		Size: 458.6 KB (458584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b56a51973ca9dedb84d83b0b25381985672720d95f8f56997161fbbb86c6d18`  
		Last Modified: Wed, 21 Feb 2024 01:34:33 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b4b91c80633c3fc0971823bb9d623ee1fe0c318a31dc46df990991cf6d20ba`  
		Last Modified: Mon, 26 Feb 2024 19:51:19 GMT  
		Size: 178.3 MB (178348692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b51a17cba7ecb2514de6eee37cebe9a7895f6ded4ed4dd92c8e46f602840fab9`  
		Last Modified: Mon, 26 Feb 2024 19:51:21 GMT  
		Size: 306.9 MB (306883002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b36ddfafbca129cff0feb39b4e4d1bcae38fd2805b2238def98afa1d64e5331`  
		Last Modified: Mon, 26 Feb 2024 19:51:16 GMT  
		Size: 615.1 KB (615138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4da7cd2a521bdc2a04e2b795337710e0703339d69419c6f74e455ea9dcacf4`  
		Last Modified: Mon, 26 Feb 2024 19:51:16 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9bfa05908fd7fb7e1819d9fb72ba2b8fd768458255ceef14d3aaa77f380856`  
		Last Modified: Mon, 26 Feb 2024 19:51:17 GMT  
		Size: 2.3 KB (2309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499be3f1d029e013e6ca8e56bfe4af3e236d7f9fe5a658e3a0628d9b426bfe2f`  
		Last Modified: Mon, 26 Feb 2024 19:51:17 GMT  
		Size: 6.4 KB (6406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a4ebfa759560aaa8d28efe1cb3354a20fed23fca09c6cf4ce4f6aef1f5d1e1c`  
		Last Modified: Mon, 26 Feb 2024 19:51:18 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:16-mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:b1cb0a654209884ce07eb78d186a959872fac08a04b2e75fb6ed368c6ad2854f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9097014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fc4e6f2add4e1e9798928cd712b2731568f0691f9fa362d7ad796ea224407aa`

```dockerfile
```

-	Layers:
	-	`sha256:254a1adaf031fa0c8934b9f510952b18403b5c8db455ca0e4f49d72dee00b01f`  
		Last Modified: Mon, 26 Feb 2024 19:51:16 GMT  
		Size: 9.1 MB (9055390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b61a01a92d26b192680c1fb252125b97e95ec916635097a3441f7e5064d5746`  
		Last Modified: Mon, 26 Feb 2024 19:51:16 GMT  
		Size: 41.6 KB (41624 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:16-mariadb-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:b2acd53282fda84a266d627f74d57f552bab12659107c0e6f9137a546e4eeb70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **587.7 MB (587673741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f478ee6f94506d6f2503acf08ac8d53e801d31bc0e99e76312b8524a0b10486`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 13 Feb 2024 10:08:34 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:08:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:08:48 GMT
ADD file:8d91b8bd386e0cc3407396da8cb35fad29dc5025c641db58739e8c0b3fd77ef0 in / 
# Tue, 13 Feb 2024 10:08:49 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 04:51:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Feb 2024 04:51:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 04:51:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Feb 2024 04:52:49 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 04:52:49 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Fri, 16 Feb 2024 04:53:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Feb 2024 04:53:10 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Fri, 16 Feb 2024 04:53:10 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 16 Feb 2024 04:53:10 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Feb 2024 07:29:55 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 16 Feb 2024 07:29:55 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 07:29:56 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 16 Feb 2024 07:29:56 GMT
WORKDIR /usr/local/tomcat
# Fri, 16 Feb 2024 07:29:56 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 16 Feb 2024 07:29:56 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 16 Feb 2024 07:31:59 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 16 Feb 2024 07:31:59 GMT
ENV TOMCAT_MAJOR=9
# Wed, 21 Feb 2024 02:20:56 GMT
ENV TOMCAT_VERSION=9.0.86
# Wed, 21 Feb 2024 02:20:56 GMT
ENV TOMCAT_SHA512=e8a8000dbeba5ee266ec4bf77217574364ffd114c8b913816f2e7a5e4eab4d01d0be3f05c8fccefcb5c5d770308efe1983be80279b6ef6d122d6183288a8ee9c
# Wed, 21 Feb 2024 02:20:57 GMT
COPY dir:52aed3e3fb48dd428e971cb85f8f92f0846f944a70308bc72289f696b56b8f42 in /usr/local/tomcat 
# Wed, 21 Feb 2024 02:21:01 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Feb 2024 02:21:02 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 21 Feb 2024 02:21:02 GMT
EXPOSE 8080
# Wed, 21 Feb 2024 02:21:03 GMT
ENTRYPOINT []
# Wed, 21 Feb 2024 02:21:03 GMT
CMD ["catalina.sh" "run"]
# Mon, 26 Feb 2024 13:14:55 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 26 Feb 2024 13:14:55 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 26 Feb 2024 13:14:55 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 26 Feb 2024 13:14:55 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 26 Feb 2024 13:14:55 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 26 Feb 2024 13:14:55 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 26 Feb 2024 13:14:55 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Feb 2024 13:14:55 GMT
ENV XWIKI_VERSION=16.1.0
# Mon, 26 Feb 2024 13:14:55 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.1.0
# Mon, 26 Feb 2024 13:14:55 GMT
ENV XWIKI_DOWNLOAD_SHA256=e236fc101710a0bfefed2328cc66652e265f21ab40dd30e6b7ce52300da744d5
# Mon, 26 Feb 2024 13:14:55 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 26 Feb 2024 13:14:55 GMT
ENV MARIADB_JDBC_VERSION=3.3.2
# Mon, 26 Feb 2024 13:14:55 GMT
ENV MARIADB_JDBC_SHA256=2a67ef3cc1ca481965a0e7f2d4174d126f3464d02b4055a441261fad8c196769
# Mon, 26 Feb 2024 13:14:55 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.3.2
# Mon, 26 Feb 2024 13:14:55 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.3.2.jar
# Mon, 26 Feb 2024 13:14:55 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.3.2.jar
# Mon, 26 Feb 2024 13:14:55 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Mon, 26 Feb 2024 13:14:55 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 26 Feb 2024 13:14:55 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 26 Feb 2024 13:14:55 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 26 Feb 2024 13:14:55 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 26 Feb 2024 13:14:55 GMT
VOLUME [/usr/local/xwiki]
# Mon, 26 Feb 2024 13:14:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Feb 2024 13:14:55 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:3e5db86eb9ec9d504e578b563fa89da9e71500cd4403efe3f4f9a567bdf34e85`  
		Last Modified: Tue, 13 Feb 2024 17:23:16 GMT  
		Size: 28.4 MB (28400321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1bac6b544c281c39df6cde20776732e9b89dbfbbbb49870c60c9af5ef1df471`  
		Last Modified: Fri, 16 Feb 2024 04:55:46 GMT  
		Size: 18.9 MB (18860590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:244992bb9e51f456f3e5c927182054789a275d47eba65099182705a8e1952dc2`  
		Last Modified: Fri, 16 Feb 2024 04:56:12 GMT  
		Size: 46.6 MB (46639325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e543faa97f71ea4edea5a6153e1b82e4e9143354356435ca0a085c427b9b07e`  
		Last Modified: Fri, 16 Feb 2024 04:56:06 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b734e973751dd4636bc278f0ef5ee31fc8e10cc65a07ebd5ef57aa728870187`  
		Last Modified: Fri, 16 Feb 2024 04:56:06 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834bcd95e101783ee58afe3b6ea7c1050d27b18b749f6b70e0bcbce490b2298e`  
		Last Modified: Fri, 16 Feb 2024 07:41:13 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08260b115c6a7540dd9078e15a0b3abe0c1e3d241dd8efd8ff6fe43840322f9`  
		Last Modified: Wed, 21 Feb 2024 02:43:35 GMT  
		Size: 12.4 MB (12418084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df99f020bb771bfb916b40a084c375b7b9d6aba87791b0679dd27408096b7e7`  
		Last Modified: Wed, 21 Feb 2024 02:43:34 GMT  
		Size: 457.1 KB (457128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41fe064b4c9bb6147a50153ae6ce913ccec8ecefc141098f8cfa404dccfe968`  
		Last Modified: Wed, 21 Feb 2024 02:43:34 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f942220408c5601f78916ffb6c0b523503ae28b04b2f8ffa2416021fb769ec`  
		Last Modified: Wed, 21 Feb 2024 05:54:58 GMT  
		Size: 173.4 MB (173386551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e80f42960c03d4ae7745ba75926f7cedaa3577da7f3a081ce0ece053a937bad`  
		Last Modified: Mon, 26 Feb 2024 20:02:15 GMT  
		Size: 306.9 MB (306882902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b548c45b27d0f3caf9e11ed76204b0e3f36fbb8bc40bf8a9be0f157f9dd5379`  
		Last Modified: Mon, 26 Feb 2024 20:04:35 GMT  
		Size: 615.1 KB (615139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8050e15f74852301523a66af4d61056db8525b8d7f4d47cc32b8bfa69abb97d`  
		Last Modified: Mon, 26 Feb 2024 20:04:34 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b567b94986be52f2929456ac59a18fc9f785e54ca20ffbb0068a35533ab2dd6`  
		Last Modified: Mon, 26 Feb 2024 20:04:34 GMT  
		Size: 2.3 KB (2310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7278c61b6b2589f36ce675e98c2090594cde7283b1d922d088bffe6f5a9c652c`  
		Last Modified: Mon, 26 Feb 2024 20:04:35 GMT  
		Size: 6.4 KB (6411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:901024a1f8c54f086d5802d0e1203f54de286360b4ff2e3b24ec9fc3f0454b5f`  
		Last Modified: Mon, 26 Feb 2024 20:04:35 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:16-mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:d21a5e96c61a4492dfecbf61ecbeb13dc58d13be78d51060e7b0fa6e8c8ee2f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9191991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26af816ba3835b948cba4764b8caab5a12637939e4efc475c3251a5037354246`

```dockerfile
```

-	Layers:
	-	`sha256:1e4d0045e5d8f7e1b1c1248066053c80516f3f771c486600fd0ab93bf6a89068`  
		Last Modified: Mon, 26 Feb 2024 20:04:34 GMT  
		Size: 9.2 MB (9151818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5beb52eb9481708b63fbcf50130c890c82f1e0aad830a310839026aa4fbfd99`  
		Last Modified: Mon, 26 Feb 2024 20:04:34 GMT  
		Size: 40.2 KB (40173 bytes)  
		MIME: application/vnd.in-toto+json
