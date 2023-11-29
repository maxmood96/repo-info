## `xwiki:stable-mysql`

```console
$ docker pull xwiki@sha256:95a70c76f7a7417826659dbac224a0f4971f8c2a5f917b4c3c6ce9b23d8f4a4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:stable-mysql` - linux; amd64

```console
$ docker pull xwiki@sha256:79fc911f554b48582e9f70571c77505d7d255811ce9d372c92e4c6d61fd1507f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **598.2 MB (598173794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:476696b3f6a84e512b8adf29998c20ae61605571c4796f15659491e2a02c0f1c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 05 Oct 2023 07:33:30 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:33:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:33:32 GMT
ADD file:63d5ab3ef0aab308c0e71cb67292c5467f60deafa9b0418cbb220affcd078444 in / 
# Thu, 05 Oct 2023 07:33:32 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 05:51:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 05:51:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 05:51:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 30 Oct 2023 23:27:44 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Mon, 30 Oct 2023 23:27:44 GMT
ENV JAVA_VERSION=jdk-17.0.9+9
# Mon, 30 Oct 2023 23:29:18 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='05b192f81ed478178ba953a2a779b67fc5a810acadb633ad69f8c4412399edb8';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.9_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c37f729200b572884b8f8e157852c739be728d61d9a1da0f920104876d324733';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.9_9.tar.gz';          ;;        armhf|arm)          ESUM='5ae1f8cae358e41083a6b44f53c6f0daeb657f83c293da6c8733f68278e13703';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.9_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='79c85ecf1320c67b828310167e1ced62e402bc86a5d47ca9cc7bfa3b708cb07a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.9_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c4f2249bee785aa8c754741aa24d035e02b4e6d844e35b2b20030374d8fbab75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.9_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Mon, 30 Oct 2023 23:29:19 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Mon, 30 Oct 2023 23:29:19 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Mon, 30 Oct 2023 23:29:19 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 31 Oct 2023 03:37:14 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 31 Oct 2023 03:37:14 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:37:14 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 31 Oct 2023 03:37:14 GMT
WORKDIR /usr/local/tomcat
# Tue, 31 Oct 2023 03:37:14 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 31 Oct 2023 03:37:14 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 31 Oct 2023 03:39:32 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 31 Oct 2023 03:39:32 GMT
ENV TOMCAT_MAJOR=9
# Fri, 17 Nov 2023 01:51:01 GMT
ENV TOMCAT_VERSION=9.0.83
# Fri, 17 Nov 2023 01:51:01 GMT
ENV TOMCAT_SHA512=3f022ec8552bce1b72eb85d0778c93052ccb00226de3302544ec844ab93a9991e19c2db56ed06c18f03e5d75f34a46cedac46ae83bdd225518a55c62fc69ea04
# Fri, 17 Nov 2023 01:51:01 GMT
COPY dir:b6e1a8757fb2a3ef38131285ce5c3e899c192beceb72b241a4c35cd6322a0630 in /usr/local/tomcat 
# Fri, 17 Nov 2023 01:51:27 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 17 Nov 2023 01:51:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 17 Nov 2023 01:51:28 GMT
EXPOSE 8080
# Fri, 17 Nov 2023 01:51:28 GMT
ENTRYPOINT []
# Fri, 17 Nov 2023 01:51:28 GMT
CMD ["catalina.sh" "run"]
# Fri, 17 Nov 2023 03:44:25 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 17 Nov 2023 03:44:25 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 17 Nov 2023 03:44:25 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 17 Nov 2023 03:44:25 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 17 Nov 2023 03:44:25 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 17 Nov 2023 03:44:25 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 17 Nov 2023 03:44:51 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 28 Nov 2023 23:43:14 GMT
ENV XWIKI_VERSION=15.10
# Tue, 28 Nov 2023 23:43:14 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.10
# Tue, 28 Nov 2023 23:43:14 GMT
ENV XWIKI_DOWNLOAD_SHA256=6f8b932c2a2a82acad5695675e1846d4421207c1820e415006750385e0981ece
# Tue, 28 Nov 2023 23:43:54 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 28 Nov 2023 23:43:55 GMT
ENV MYSQL_JDBC_VERSION=8.2.0
# Tue, 28 Nov 2023 23:43:55 GMT
ENV MYSQL_JDBC_SHA256=06f14fbd664d0e382347489e66495ca27ab7e6c2e1d9969a496931736197465f
# Tue, 28 Nov 2023 23:43:55 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.2.0
# Tue, 28 Nov 2023 23:43:55 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.2.0.jar
# Tue, 28 Nov 2023 23:43:55 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.2.0.jar
# Tue, 28 Nov 2023 23:43:56 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Tue, 28 Nov 2023 23:43:56 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 28 Nov 2023 23:43:56 GMT
COPY file:5f2a4ed869db1db1cb3a7b1d056ce086793eaabda6970493836040aa3d66ed8a in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 28 Nov 2023 23:43:57 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 28 Nov 2023 23:43:57 GMT
COPY file:b4aa3ce54fbec701991ab2ba0888227771ac09202a9e4ba777edbd49ed958e27 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 28 Nov 2023 23:43:57 GMT
VOLUME [/usr/local/xwiki]
# Tue, 28 Nov 2023 23:43:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Nov 2023 23:43:57 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:43f89b94cd7df92a2f7e565b8fb1b7f502eff2cd225508cbd7ea2d36a9a3a601`  
		Last Modified: Thu, 05 Oct 2023 08:42:10 GMT  
		Size: 30.4 MB (30439111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4452d37e1e46888f8dbbf8283d09e03f1bec00021532334441fe00c95aa8b15`  
		Last Modified: Mon, 30 Oct 2023 23:36:06 GMT  
		Size: 17.5 MB (17454768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cae6cc00f059e812c753a4a45b4a388d14bb714a104ec8b33c31436807f31055`  
		Last Modified: Mon, 30 Oct 2023 23:37:50 GMT  
		Size: 47.1 MB (47149391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfaec5da5e638ca5d7247c8697d0721bdac4826945748d0239718f23f657abc5`  
		Last Modified: Mon, 30 Oct 2023 23:37:44 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7dcc43773c1bcab928db7ca63abd5a20c525148ae1b63c03bfdcdef7e03153`  
		Last Modified: Mon, 30 Oct 2023 23:37:44 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6729bb2516f9ee1f23d3c6b1a60b651eb413c43b62cdc554de84df2590085216`  
		Last Modified: Tue, 31 Oct 2023 03:53:25 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5abd3b406207b67cea45616a0f3398220a4b45a469f1f14f5c5bdef4b2f35e20`  
		Last Modified: Fri, 17 Nov 2023 02:09:18 GMT  
		Size: 12.4 MB (12391471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11bea609136cd16081c1a3aaca29e377bb4b844074278006408baae7f88efd57`  
		Last Modified: Fri, 17 Nov 2023 02:09:17 GMT  
		Size: 3.0 MB (2970855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52c81efba92eebab5d197fa544a2e5612bf514bd18f152836a57a5802f198041`  
		Last Modified: Fri, 17 Nov 2023 02:09:16 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c03a6e83eb10956d0d77c0502173800b8478ec89ea1a8aac784d45723b9245f2`  
		Last Modified: Fri, 17 Nov 2023 03:51:48 GMT  
		Size: 178.6 MB (178573863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7893a579941fafeaf3cad869d1bea83c14b1abb2af583676900d0ec48fa01335`  
		Last Modified: Tue, 28 Nov 2023 23:45:53 GMT  
		Size: 306.8 MB (306829701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991095681781139fef0c8c921c86f07c521a03024ae407032ad47fe4915655b1`  
		Last Modified: Tue, 28 Nov 2023 23:45:37 GMT  
		Size: 2.4 MB (2350947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:831086d8a2123f9414b31336203f0df6d2b6113a7bb75a297c1c77b132918214`  
		Last Modified: Tue, 28 Nov 2023 23:45:36 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48fa299acb244c0597d72c9e5e06993e735fc173d816228fda8b69728171a79a`  
		Last Modified: Tue, 28 Nov 2023 23:45:36 GMT  
		Size: 2.4 KB (2368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18af8dec06f9609426a914a5a82c8f6e733766fbfcf675588026484c3afbd51`  
		Last Modified: Tue, 28 Nov 2023 23:45:36 GMT  
		Size: 6.3 KB (6297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72eb1bd9ca9035cfdd28fceb8a028f39b30019a59d7818069b469bc6d5578468`  
		Last Modified: Tue, 28 Nov 2023 23:45:36 GMT  
		Size: 2.5 KB (2483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:stable-mysql` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:0ed131773d7917a0792630886c47d43bac92e51d092a29405019074dd874d77c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.9 MB (591911509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bf72fc297fd81c03658c967ef773c2057abf3d7a01f04269127803cdc2c4004`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 05 Oct 2023 07:32:20 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:32:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:32:22 GMT
ADD file:f8594e26831508c318e42c8dfd9942041031087b8de1bf3fec11fd75b8b30fd4 in / 
# Thu, 05 Oct 2023 07:32:22 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 02:46:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 02:46:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 02:46:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 30 Oct 2023 23:44:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Mon, 30 Oct 2023 23:44:05 GMT
ENV JAVA_VERSION=jdk-17.0.9+9
# Mon, 30 Oct 2023 23:45:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='05b192f81ed478178ba953a2a779b67fc5a810acadb633ad69f8c4412399edb8';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.9_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c37f729200b572884b8f8e157852c739be728d61d9a1da0f920104876d324733';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.9_9.tar.gz';          ;;        armhf|arm)          ESUM='5ae1f8cae358e41083a6b44f53c6f0daeb657f83c293da6c8733f68278e13703';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.9_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='79c85ecf1320c67b828310167e1ced62e402bc86a5d47ca9cc7bfa3b708cb07a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.9_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c4f2249bee785aa8c754741aa24d035e02b4e6d844e35b2b20030374d8fbab75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.9_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Mon, 30 Oct 2023 23:45:35 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Mon, 30 Oct 2023 23:45:35 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Mon, 30 Oct 2023 23:45:35 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 31 Oct 2023 02:56:13 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 31 Oct 2023 02:56:14 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 02:56:14 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 31 Oct 2023 02:56:14 GMT
WORKDIR /usr/local/tomcat
# Tue, 31 Oct 2023 02:56:14 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 31 Oct 2023 02:56:14 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 31 Oct 2023 02:58:17 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 31 Oct 2023 02:58:17 GMT
ENV TOMCAT_MAJOR=9
# Fri, 17 Nov 2023 02:16:24 GMT
ENV TOMCAT_VERSION=9.0.83
# Fri, 17 Nov 2023 02:16:24 GMT
ENV TOMCAT_SHA512=3f022ec8552bce1b72eb85d0778c93052ccb00226de3302544ec844ab93a9991e19c2db56ed06c18f03e5d75f34a46cedac46ae83bdd225518a55c62fc69ea04
# Fri, 17 Nov 2023 02:16:24 GMT
COPY dir:3d6975406d5c02f80e9cf7d7f1d0b3d166d08756088d7d8662050a94f9373d14 in /usr/local/tomcat 
# Fri, 17 Nov 2023 02:16:28 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 17 Nov 2023 02:16:29 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 17 Nov 2023 02:16:29 GMT
EXPOSE 8080
# Fri, 17 Nov 2023 02:16:29 GMT
ENTRYPOINT []
# Fri, 17 Nov 2023 02:16:29 GMT
CMD ["catalina.sh" "run"]
# Fri, 17 Nov 2023 03:56:37 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 17 Nov 2023 03:56:37 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 17 Nov 2023 03:56:38 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 17 Nov 2023 03:56:38 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 17 Nov 2023 03:56:38 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 17 Nov 2023 03:56:38 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 17 Nov 2023 03:57:00 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 29 Nov 2023 00:12:08 GMT
ENV XWIKI_VERSION=15.10
# Wed, 29 Nov 2023 00:12:08 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.10
# Wed, 29 Nov 2023 00:12:08 GMT
ENV XWIKI_DOWNLOAD_SHA256=6f8b932c2a2a82acad5695675e1846d4421207c1820e415006750385e0981ece
# Wed, 29 Nov 2023 00:12:48 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 29 Nov 2023 00:12:50 GMT
ENV MYSQL_JDBC_VERSION=8.2.0
# Wed, 29 Nov 2023 00:12:50 GMT
ENV MYSQL_JDBC_SHA256=06f14fbd664d0e382347489e66495ca27ab7e6c2e1d9969a496931736197465f
# Wed, 29 Nov 2023 00:12:50 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.2.0
# Wed, 29 Nov 2023 00:12:50 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.2.0.jar
# Wed, 29 Nov 2023 00:12:50 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.2.0.jar
# Wed, 29 Nov 2023 00:12:51 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Wed, 29 Nov 2023 00:12:51 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 29 Nov 2023 00:12:51 GMT
COPY file:5f2a4ed869db1db1cb3a7b1d056ce086793eaabda6970493836040aa3d66ed8a in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 29 Nov 2023 00:12:52 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 29 Nov 2023 00:12:52 GMT
COPY file:b4aa3ce54fbec701991ab2ba0888227771ac09202a9e4ba777edbd49ed958e27 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 29 Nov 2023 00:12:52 GMT
VOLUME [/usr/local/xwiki]
# Wed, 29 Nov 2023 00:12:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Nov 2023 00:12:52 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:895d322e8e5957c04af3ab7b3431f2a562182d34167c6e159e02044150a66967`  
		Last Modified: Thu, 05 Oct 2023 08:57:30 GMT  
		Size: 28.4 MB (28391939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69f494a0917249ff640404cd9965fcd6a5ed5b7725fc21ff44518307f60c8e0a`  
		Last Modified: Mon, 30 Oct 2023 23:50:44 GMT  
		Size: 18.9 MB (18858788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cf992ac9f7594e95247c785c373702afa5ebbf20db8b34fad80efa1ff3e0736`  
		Last Modified: Mon, 30 Oct 2023 23:52:03 GMT  
		Size: 46.6 MB (46623965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652d455f0a073aa4bc59de2e451f4c5a2ad6d6d9cb13538ef955d11e722e6c45`  
		Last Modified: Mon, 30 Oct 2023 23:51:58 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fce918b0b707b682534041104ace8701cb441f12b5ce2fb5e983bfe29694385`  
		Last Modified: Mon, 30 Oct 2023 23:51:58 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efa512d8c7aada52b2d7bd906e3bae22e22f3025a7ed09a1f0adf9e2b9c7aaf6`  
		Last Modified: Tue, 31 Oct 2023 03:09:48 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d0be96d9e26d4bdaa466f154ab63b4a65317928dc740d9487407598c11e3881`  
		Last Modified: Fri, 17 Nov 2023 02:31:17 GMT  
		Size: 12.4 MB (12398006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc049231212f55a65b295577715e3690a784553575cd5e5b272daa633ad31048`  
		Last Modified: Fri, 17 Nov 2023 02:31:16 GMT  
		Size: 2.8 MB (2812548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb37d870ea6b50484f6c05999bbe6fc08a9a027f71da0811fe80d6032245fa8c`  
		Last Modified: Fri, 17 Nov 2023 02:31:16 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dc3def3af1bfd82ec9717c9d6310d7a39abab36f3c53a9e88cf4fb6c716d4b7`  
		Last Modified: Fri, 17 Nov 2023 04:03:48 GMT  
		Size: 173.6 MB (173631985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71a9236affcdd034b772eb0771e71e210c9a8721edecbf0b905a414b713d1c53`  
		Last Modified: Wed, 29 Nov 2023 00:14:51 GMT  
		Size: 306.8 MB (306829637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d836ead8f5d0c849813263cddf0a96aa508987c028e71d50cf05582c5f13abf7`  
		Last Modified: Wed, 29 Nov 2023 00:14:37 GMT  
		Size: 2.4 MB (2350958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b74f4048b7901f213babcf1f9ef232fc24be43d93367a8e8b772d90a839631dc`  
		Last Modified: Wed, 29 Nov 2023 00:14:37 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528f302282afc98fe7567815d8b5b7bdd307a279a9bc4f81025bc6dd0a9cba14`  
		Last Modified: Wed, 29 Nov 2023 00:14:37 GMT  
		Size: 2.4 KB (2369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d93087c660eb3dd1728c5a151b72aa2bbc63b0954e8809cd73c4a77acc032065`  
		Last Modified: Wed, 29 Nov 2023 00:14:37 GMT  
		Size: 6.3 KB (6298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5366c7e9f7c9c9e8ff805fc1640e407ce8a42ad9ec632821753daf26c8ea51d3`  
		Last Modified: Wed, 29 Nov 2023 00:14:37 GMT  
		Size: 2.5 KB (2479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
