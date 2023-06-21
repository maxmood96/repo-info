## `xwiki:lts-mysql`

```console
$ docker pull xwiki@sha256:2d11c6c357bf7d1c3f3a37588fe4fac71fd92a6dc1e43b017ff542af5d8acfd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:lts-mysql` - linux; amd64

```console
$ docker pull xwiki@sha256:423198e9f5ed2c5e1d8d8ea344e0d1308eb7ddbcff0dc3262b31ebe25babd447
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.3 MB (590269805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a458810ae659d872bd0f5bba4c3d429431e7da38e6735ed01d49511686b8829`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:15:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:15:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:15:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:16:14 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:17:05 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Fri, 16 Jun 2023 02:17:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Jun 2023 02:17:38 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 16 Jun 2023 04:34:54 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 16 Jun 2023 04:34:54 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 04:34:55 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 16 Jun 2023 04:34:55 GMT
WORKDIR /usr/local/tomcat
# Fri, 16 Jun 2023 04:34:55 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 16 Jun 2023 04:34:55 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 16 Jun 2023 04:37:42 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 16 Jun 2023 04:37:42 GMT
ENV TOMCAT_MAJOR=9
# Fri, 16 Jun 2023 04:37:42 GMT
ENV TOMCAT_VERSION=9.0.76
# Fri, 16 Jun 2023 04:37:42 GMT
ENV TOMCAT_SHA512=028163cbe15367f0ab60e086b0ebc8d774e62d126d82ae9152f863d4680e280b11c9503e3b51ee7089ca9bea1bfa5b535b244a727a3021e5fa72dd7e9569af9a
# Fri, 16 Jun 2023 04:37:42 GMT
COPY dir:d68ada5df83c00e64f2bc5fad7f7e78285704dda3af250e863e1e0a3a7acaa1f in /usr/local/tomcat 
# Fri, 16 Jun 2023 04:37:46 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 04:37:47 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 16 Jun 2023 04:37:47 GMT
EXPOSE 8080
# Fri, 16 Jun 2023 04:37:47 GMT
CMD ["catalina.sh" "run"]
# Fri, 16 Jun 2023 10:07:29 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 16 Jun 2023 10:07:29 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 16 Jun 2023 10:07:29 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 16 Jun 2023 10:07:29 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 16 Jun 2023 10:07:29 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 16 Jun 2023 10:07:29 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 16 Jun 2023 10:11:16 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 21 Jun 2023 00:28:48 GMT
ENV XWIKI_VERSION=14.10.13
# Wed, 21 Jun 2023 00:28:48 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.13
# Wed, 21 Jun 2023 00:28:48 GMT
ENV XWIKI_DOWNLOAD_SHA256=5883ffdbc10865043778f3caa48fbca900129cf41c76ee6fdafba74769c928d4
# Wed, 21 Jun 2023 00:29:27 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 21 Jun 2023 00:29:28 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Wed, 21 Jun 2023 00:29:28 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Wed, 21 Jun 2023 00:29:28 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Wed, 21 Jun 2023 00:29:28 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Wed, 21 Jun 2023 00:29:28 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Wed, 21 Jun 2023 00:29:29 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Wed, 21 Jun 2023 00:29:29 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 21 Jun 2023 00:29:29 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 21 Jun 2023 00:29:29 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 21 Jun 2023 00:29:30 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 21 Jun 2023 00:29:30 GMT
VOLUME [/usr/local/xwiki]
# Wed, 21 Jun 2023 00:29:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jun 2023 00:29:30 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:3f94e4e483ea634d7ab0b63649b8f72f8b721d4c626297fd0edae0abea1df9e9`  
		Last Modified: Tue, 06 Jun 2023 11:46:33 GMT  
		Size: 30.4 MB (30431039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3b6b86b9b9ec784135c9a4adac0cdf59f8b0812134b00402f67714b92e13d6`  
		Last Modified: Fri, 16 Jun 2023 02:20:59 GMT  
		Size: 12.5 MB (12495197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906feab3d1ffe6f8d194544b36d7e399e813e77a2df6678380a6b4c5a18aec2f`  
		Last Modified: Fri, 16 Jun 2023 02:22:53 GMT  
		Size: 46.7 MB (46666394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9358731a04ce4ffb43ea1162e0684391b355b508420d45ae7921eb8cab9c10db`  
		Last Modified: Fri, 16 Jun 2023 02:22:47 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8227a7bb3d2b11b0faf224f49fb0d8fc994b6a8d902d8bc6eb3478490aea1816`  
		Last Modified: Fri, 16 Jun 2023 04:49:05 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:091107a5723c6be4efbe464ce52499163a7f46616c82788b102b12a7163dd8e4`  
		Last Modified: Fri, 16 Jun 2023 04:51:23 GMT  
		Size: 12.3 MB (12269602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d295a6de01da4fb5525c7f30018b23d903a9c05f3e14b3258053900c0696c0c`  
		Last Modified: Fri, 16 Jun 2023 04:51:22 GMT  
		Size: 454.6 KB (454597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac31a8386f6ec9e8c4c67f00eae10e5bdbef376212ce7c553f3f27636884a5f0`  
		Last Modified: Fri, 16 Jun 2023 04:51:22 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b0f77c508c593bc448e39233cdd117797ff0ef9d90cbda04c0f019d256f970`  
		Last Modified: Fri, 16 Jun 2023 10:16:06 GMT  
		Size: 178.3 MB (178335543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdcefc19ef09aec3150a3f5ffbeb1e48adef622942aefff1ded37b6f834b1d57`  
		Last Modified: Wed, 21 Jun 2023 00:31:16 GMT  
		Size: 307.3 MB (307261161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:680ae75b0bc076a3900ad1aae06f76adf6d2ea9da52dc66acc7383f3bbdc544d`  
		Last Modified: Wed, 21 Jun 2023 00:31:00 GMT  
		Size: 2.3 MB (2343667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58710e244cbccb42a7a162ab2993039bbd99e4b992e12d9e2a67cf40c7281500`  
		Last Modified: Wed, 21 Jun 2023 00:31:00 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b71f8f45188405740a0c3cf7239727a7f34f44e302f6d2450db28435f790b99`  
		Last Modified: Wed, 21 Jun 2023 00:30:59 GMT  
		Size: 2.3 KB (2298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27d8ae3aa44fe5013960b82b2cee33a3ca914f02bbbefdf6e6de146043beb42a`  
		Last Modified: Wed, 21 Jun 2023 00:31:00 GMT  
		Size: 6.0 KB (6012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8202443866adbfb8d7b5844692c7481c31a95522d9345e96a919a239839abec4`  
		Last Modified: Wed, 21 Jun 2023 00:30:59 GMT  
		Size: 2.5 KB (2495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:lts-mysql` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:c0c128f4d3fa7394cf852d2fbbda2adc03482be52f9a51c08af63ca71ab3f2f2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.6 MB (581573276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a153af2b3b136dff9a404e748ec919f886effa1786bb92099d297bc402eb14c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 05 Jun 2023 17:11:17 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:11:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:11:19 GMT
ADD file:1043594b482384e967c94378b65ec4bc7a38190649a94f0325b7fb00be0a623e in / 
# Mon, 05 Jun 2023 17:11:19 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:45:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:45:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:45:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:46:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:46:41 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Fri, 16 Jun 2023 02:47:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Jun 2023 02:47:11 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 16 Jun 2023 06:03:56 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 16 Jun 2023 06:03:56 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 06:03:57 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 16 Jun 2023 06:03:57 GMT
WORKDIR /usr/local/tomcat
# Fri, 16 Jun 2023 06:03:57 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 16 Jun 2023 06:03:57 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 16 Jun 2023 06:06:03 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 16 Jun 2023 06:06:03 GMT
ENV TOMCAT_MAJOR=9
# Fri, 16 Jun 2023 06:06:03 GMT
ENV TOMCAT_VERSION=9.0.76
# Fri, 16 Jun 2023 06:06:03 GMT
ENV TOMCAT_SHA512=028163cbe15367f0ab60e086b0ebc8d774e62d126d82ae9152f863d4680e280b11c9503e3b51ee7089ca9bea1bfa5b535b244a727a3021e5fa72dd7e9569af9a
# Fri, 16 Jun 2023 06:06:03 GMT
COPY dir:ade7cc9ad5c9e30d6dd85f01942565a28f1c051dbaec50c5d97968ad63e754ee in /usr/local/tomcat 
# Fri, 16 Jun 2023 06:06:07 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 06:06:08 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 16 Jun 2023 06:06:08 GMT
EXPOSE 8080
# Fri, 16 Jun 2023 06:06:08 GMT
CMD ["catalina.sh" "run"]
# Fri, 16 Jun 2023 08:35:02 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 16 Jun 2023 08:35:02 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 16 Jun 2023 08:35:02 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 16 Jun 2023 08:35:02 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 16 Jun 2023 08:35:02 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 16 Jun 2023 08:35:03 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 16 Jun 2023 08:37:02 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 21 Jun 2023 00:26:04 GMT
ENV XWIKI_VERSION=14.10.13
# Wed, 21 Jun 2023 00:26:04 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.13
# Wed, 21 Jun 2023 00:26:04 GMT
ENV XWIKI_DOWNLOAD_SHA256=5883ffdbc10865043778f3caa48fbca900129cf41c76ee6fdafba74769c928d4
# Wed, 21 Jun 2023 00:26:44 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 21 Jun 2023 00:26:46 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Wed, 21 Jun 2023 00:26:46 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Wed, 21 Jun 2023 00:26:46 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Wed, 21 Jun 2023 00:26:46 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Wed, 21 Jun 2023 00:26:46 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Wed, 21 Jun 2023 00:26:47 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Wed, 21 Jun 2023 00:26:47 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 21 Jun 2023 00:26:47 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 21 Jun 2023 00:26:48 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 21 Jun 2023 00:26:48 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 21 Jun 2023 00:26:48 GMT
VOLUME [/usr/local/xwiki]
# Wed, 21 Jun 2023 00:26:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jun 2023 00:26:48 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:a1df1d4a17c6a461a5967be8a40f1158e55e0ae4dc3b3b7ae64f57cae69eb7e7`  
		Last Modified: Wed, 07 Jun 2023 02:07:18 GMT  
		Size: 28.4 MB (28389201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a707fe2fc3c87da15576bd7b678fe8f2591ad481cc638b8cfe52664b47d2cf`  
		Last Modified: Fri, 16 Jun 2023 02:49:56 GMT  
		Size: 12.5 MB (12454449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e5488ab47450fbd12fc724963811b99580bfe1e5f44267a03736f0adea506b`  
		Last Modified: Fri, 16 Jun 2023 02:51:36 GMT  
		Size: 45.0 MB (45009402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2dbf45ca92463ef69ad1ef7fb34bb5123ea7a7fdfe4f745d3728e89f260617`  
		Last Modified: Fri, 16 Jun 2023 02:51:31 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd63c7176205cf09ac548a367dddd2f6f019a7d200c8afd95f8806dd6e47cf49`  
		Last Modified: Fri, 16 Jun 2023 06:15:57 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec810a75a4132859409a64079a8a3388cb47f6cf638cec13415a9bdca18179bd`  
		Last Modified: Fri, 16 Jun 2023 06:18:10 GMT  
		Size: 12.3 MB (12275748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f82a4b0d8f6c942299bcc19dacf123e877cb30d4a358faca910fd1e9917a14c`  
		Last Modified: Fri, 16 Jun 2023 06:18:09 GMT  
		Size: 454.1 KB (454065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa40c7c4be196f78a1f23cd4b958024a8c3d48953124bb018f4631fb06e1696c`  
		Last Modified: Fri, 16 Jun 2023 06:18:09 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b18d0affa9f4dbdfae82ef0d4e03f23989200b105e1d2da696dff48a97732af0`  
		Last Modified: Fri, 16 Jun 2023 08:41:40 GMT  
		Size: 173.4 MB (173372940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cd55f5a520d0bb849d7629fa1758c810a680ce0d55f4dd30e696dce57f67e2c`  
		Last Modified: Wed, 21 Jun 2023 00:28:24 GMT  
		Size: 307.3 MB (307261181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93698cb45575440adea7fdc0854ddbf5b84e927eb612ea7fbd21c3f17f7b278b`  
		Last Modified: Wed, 21 Jun 2023 00:28:10 GMT  
		Size: 2.3 MB (2343672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d931d0b3d0e89b8c8fb82d629d516efd8a80b0f2612a8cd9bb3c2ab1987106`  
		Last Modified: Wed, 21 Jun 2023 00:28:10 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1df6eb3de6e5f0a4912a360241b81a32a0472f37f91cda50eccab582c41304c3`  
		Last Modified: Wed, 21 Jun 2023 00:28:10 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd44137161cfea0642051ebcaae43f252ef1ed2adad77e2bfb974f27f101b97f`  
		Last Modified: Wed, 21 Jun 2023 00:28:10 GMT  
		Size: 6.0 KB (6015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15f029e489d1c2e5bc89e99f24a89a24b81108369ed757e7653138eb7d924cab`  
		Last Modified: Wed, 21 Jun 2023 00:28:10 GMT  
		Size: 2.5 KB (2497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
