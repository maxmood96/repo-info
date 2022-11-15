## `xwiki:mysql-tomcat`

```console
$ docker pull xwiki@sha256:df83cfb476544d65ac1055976c2c0504e5de454f9e9b15405b8f6cd5cb89ddcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:d8f5c819d087e7aad0b59aa5d6d0b7961ab96517c1c456bd0eb4729a9e6d9f68
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **593.5 MB (593546116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92afe63b79fb4e06e1ad1f6a0bcea3b32d8101bf92709e6a08a35b3da627c189`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 18:43:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 18:43:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 18:43:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 18:44:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 23:21:41 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Fri, 04 Nov 2022 23:22:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='bd6efe3290c8b5a42f695a55a26f3e3c9c284288574879d4b7089f31f5114177';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.17_8.tar.gz';          ;;        armhf|arm)          ESUM='8cf113d3d7fa808895c8d2e41bb890af21c47e38c2460e0588147a4bb8fc658d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.17_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='0ca3d806131ab5834c501f9c625bb0248cd528af361c704503348e9c9605bedf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.17_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='dd3b159a374086e65cb07c4ccb226c90f9c02ef929cba6f0b642171d7ed97fa4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.17_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='752616097e09d7f60a3ad8bd312f90eaf50ac72577e55df229fe6e8091148f79';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.17_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 04 Nov 2022 23:22:32 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Sat, 05 Nov 2022 01:35:16 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 05 Nov 2022 01:35:16 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 01:35:17 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sat, 05 Nov 2022 01:35:17 GMT
WORKDIR /usr/local/tomcat
# Sat, 05 Nov 2022 01:35:17 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 05 Nov 2022 01:35:17 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 05 Nov 2022 01:39:54 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Sat, 05 Nov 2022 01:39:54 GMT
ENV TOMCAT_MAJOR=9
# Tue, 15 Nov 2022 03:06:43 GMT
ENV TOMCAT_VERSION=9.0.69
# Tue, 15 Nov 2022 03:06:43 GMT
ENV TOMCAT_SHA512=8c883c54ce9ce43eba37756a6404cdf3477879883a3e6d146dc8a7aa5e0425f487466afe6b6da4a895927cb7cb59177b9379cec18000f2de12785be57408c779
# Tue, 15 Nov 2022 03:06:44 GMT
COPY dir:b1a33aa3993dbbfbebb33bd9aa546b60c2f2191abf1227f453d4e830f6deb35f in /usr/local/tomcat 
# Tue, 15 Nov 2022 03:06:48 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 03:06:49 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 15 Nov 2022 03:06:49 GMT
EXPOSE 8080
# Tue, 15 Nov 2022 03:06:49 GMT
CMD ["catalina.sh" "run"]
# Tue, 15 Nov 2022 09:40:51 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 15 Nov 2022 09:40:51 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 15 Nov 2022 09:40:52 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 15 Nov 2022 09:40:52 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 15 Nov 2022 09:40:52 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 15 Nov 2022 09:40:52 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 15 Nov 2022 09:42:49 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 09:42:50 GMT
ENV XWIKI_VERSION=14.9
# Tue, 15 Nov 2022 09:42:50 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.9
# Tue, 15 Nov 2022 09:42:50 GMT
ENV XWIKI_DOWNLOAD_SHA256=9a8639b590b2612c1603ac6788fe83b4d79dbaad484cc5c60230c00f16781460
# Tue, 15 Nov 2022 09:43:58 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 15 Nov 2022 09:43:59 GMT
ENV MYSQL_JDBC_VERSION=8.0.30
# Tue, 15 Nov 2022 09:43:59 GMT
ENV MYSQL_JDBC_SHA256=b5bf2f0987197c30adf74a9e419b89cda4c257da2d1142871f508416d5f2227a
# Tue, 15 Nov 2022 09:43:59 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.30
# Tue, 15 Nov 2022 09:43:59 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.30.jar
# Tue, 15 Nov 2022 09:43:59 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.30.jar
# Tue, 15 Nov 2022 09:44:00 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Tue, 15 Nov 2022 09:44:00 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 15 Nov 2022 09:44:00 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 15 Nov 2022 09:44:01 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 15 Nov 2022 09:44:01 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 15 Nov 2022 09:44:01 GMT
VOLUME [/usr/local/xwiki]
# Tue, 15 Nov 2022 09:44:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 09:44:01 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ced2591451da3a02e2b6bb44752b9e3f00d77789921be4df5082fb9f9880ad0`  
		Last Modified: Wed, 02 Nov 2022 18:48:43 GMT  
		Size: 12.4 MB (12439006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8f874ae8c08a9e69e5fbe6c5a64200a45386132a3203d1a9a7f1146d94cfbc`  
		Last Modified: Fri, 04 Nov 2022 23:29:33 GMT  
		Size: 46.6 MB (46629936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111b6c7486426c4b6989102c2ee5be856e8a58e20ab0a350b24a905d536e8e7f`  
		Last Modified: Fri, 04 Nov 2022 23:29:26 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f84dce457c6d4f7b7291fce05f8e77998a3a7722a54125a1f1d52ca83043b4`  
		Last Modified: Sat, 05 Nov 2022 01:50:51 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6c26749ee782392e38845ee2ba79b0da586ef6a45d8e7f29c7af14612278547`  
		Last Modified: Tue, 15 Nov 2022 03:19:57 GMT  
		Size: 12.2 MB (12200249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dddc6d9fa6024025b3fcfe729cab2dc544fb25476eca6e80b1af8e8d93bb0ee`  
		Last Modified: Tue, 15 Nov 2022 03:19:56 GMT  
		Size: 452.7 KB (452680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06637eebe5e72c8ad9019ad4eb4cdde1f11f7d4c24c7ed7374cf8966343aa2fb`  
		Last Modified: Tue, 15 Nov 2022 03:19:56 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4cb4ddba50f306884a407035c0c811ef30aaa1bd943babb2981a8bf9dad4c5`  
		Last Modified: Tue, 15 Nov 2022 09:50:23 GMT  
		Size: 178.3 MB (178340772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c4da5b7bdec0f7ddd01272cc1075bdd6cd2b4f4067a8f610a537e93195a4e2a`  
		Last Modified: Tue, 15 Nov 2022 09:50:16 GMT  
		Size: 310.7 MB (310670008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78754e0c4cd1b9d547faa12ad14516a762f066fe52bed176fa2ea270b7109ed4`  
		Last Modified: Tue, 15 Nov 2022 09:49:57 GMT  
		Size: 2.4 MB (2375235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fcb78aaa2dd2370fbc201180611b69557e449120ca52e7d67b6b7411d50ae8f`  
		Last Modified: Tue, 15 Nov 2022 09:49:57 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d202a6059555ca8ca5c7a3978d5bb391f97e9c1f87082b58e18e7b5581720e5`  
		Last Modified: Tue, 15 Nov 2022 09:49:57 GMT  
		Size: 2.3 KB (2309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:589df2a50362af45e9d1ac9d5933f6c8e39bd6155882d4814c9d14ccc4783a95`  
		Last Modified: Tue, 15 Nov 2022 09:49:57 GMT  
		Size: 6.0 KB (5999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d5962080c2452a06d86119483883bd8e27a9bf09aab6ba7ca6c896675c36d88`  
		Last Modified: Tue, 15 Nov 2022 09:49:57 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:mysql-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:7e3062b5ae722da83f6bfdef4b8ef5f46388d830ca25fa69d1d56c5d7cfbd371
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.8 MB (584801589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d07a2643800916253df5fa4cb4d6c259b3d2c8107a6d6cdda3854b4f15add97e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 02 Nov 2022 18:49:40 GMT
ADD file:a934fb007525d0b56966a52a22ab22560bf48b6e09917f05324042129d4d894a in / 
# Wed, 02 Nov 2022 18:49:40 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:44:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 19:44:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 19:44:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 19:44:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 22:40:54 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Fri, 04 Nov 2022 22:41:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='bd6efe3290c8b5a42f695a55a26f3e3c9c284288574879d4b7089f31f5114177';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.17_8.tar.gz';          ;;        armhf|arm)          ESUM='8cf113d3d7fa808895c8d2e41bb890af21c47e38c2460e0588147a4bb8fc658d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.17_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='0ca3d806131ab5834c501f9c625bb0248cd528af361c704503348e9c9605bedf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.17_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='dd3b159a374086e65cb07c4ccb226c90f9c02ef929cba6f0b642171d7ed97fa4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.17_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='752616097e09d7f60a3ad8bd312f90eaf50ac72577e55df229fe6e8091148f79';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.17_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 04 Nov 2022 22:41:34 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 04 Nov 2022 23:48:38 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 04 Nov 2022 23:48:38 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Nov 2022 23:48:38 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 04 Nov 2022 23:48:39 GMT
WORKDIR /usr/local/tomcat
# Fri, 04 Nov 2022 23:48:39 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 04 Nov 2022 23:48:39 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 04 Nov 2022 23:53:12 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 04 Nov 2022 23:53:12 GMT
ENV TOMCAT_MAJOR=9
# Tue, 15 Nov 2022 04:57:22 GMT
ENV TOMCAT_VERSION=9.0.69
# Tue, 15 Nov 2022 04:57:22 GMT
ENV TOMCAT_SHA512=8c883c54ce9ce43eba37756a6404cdf3477879883a3e6d146dc8a7aa5e0425f487466afe6b6da4a895927cb7cb59177b9379cec18000f2de12785be57408c779
# Tue, 15 Nov 2022 04:57:22 GMT
COPY dir:096b403a5f78b17e6b4bff63128a9c93941b97f22470991610dd641633d977f1 in /usr/local/tomcat 
# Tue, 15 Nov 2022 04:57:25 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 04:57:26 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 15 Nov 2022 04:57:26 GMT
EXPOSE 8080
# Tue, 15 Nov 2022 04:57:27 GMT
CMD ["catalina.sh" "run"]
# Tue, 15 Nov 2022 18:31:47 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 15 Nov 2022 18:31:47 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 15 Nov 2022 18:31:47 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 15 Nov 2022 18:31:47 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 15 Nov 2022 18:31:47 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 15 Nov 2022 18:31:47 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 15 Nov 2022 18:34:33 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 18:34:36 GMT
ENV XWIKI_VERSION=14.9
# Tue, 15 Nov 2022 18:34:36 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.9
# Tue, 15 Nov 2022 18:34:36 GMT
ENV XWIKI_DOWNLOAD_SHA256=9a8639b590b2612c1603ac6788fe83b4d79dbaad484cc5c60230c00f16781460
# Tue, 15 Nov 2022 18:35:18 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 15 Nov 2022 18:35:21 GMT
ENV MYSQL_JDBC_VERSION=8.0.30
# Tue, 15 Nov 2022 18:35:21 GMT
ENV MYSQL_JDBC_SHA256=b5bf2f0987197c30adf74a9e419b89cda4c257da2d1142871f508416d5f2227a
# Tue, 15 Nov 2022 18:35:21 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.30
# Tue, 15 Nov 2022 18:35:21 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.30.jar
# Tue, 15 Nov 2022 18:35:21 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.30.jar
# Tue, 15 Nov 2022 18:35:22 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Tue, 15 Nov 2022 18:35:22 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 15 Nov 2022 18:35:22 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 15 Nov 2022 18:35:22 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 15 Nov 2022 18:35:23 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 15 Nov 2022 18:35:23 GMT
VOLUME [/usr/local/xwiki]
# Tue, 15 Nov 2022 18:35:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 18:35:23 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:0509fae36eb0656f8bdb23f8ae64100d893bcea2563e97468d337e04d2d0410b`  
		Last Modified: Wed, 02 Nov 2022 18:50:21 GMT  
		Size: 28.4 MB (28382154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e502a1af2bcd98f5f0d2f5e4da1a0e7bbe07a2c548e2662f7d37dce5ae1df46c`  
		Last Modified: Wed, 02 Nov 2022 19:48:28 GMT  
		Size: 12.4 MB (12396330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc4598c07dd818f03a0378b0341a4a8e80f0152fbb3e7d5246ca4f466f42e611`  
		Last Modified: Fri, 04 Nov 2022 22:46:46 GMT  
		Size: 45.0 MB (44958470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715a937a1066f998b331fcd62256ad01a5571bdf46804e97825afc64f9ebb427`  
		Last Modified: Fri, 04 Nov 2022 22:46:41 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb623f082f74b2fa9fc2c4e3f3a4802875cb9753cfa26ed940201ce72bb56cb`  
		Last Modified: Sat, 05 Nov 2022 00:03:40 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33260b83200262bbd546be371ad3c1f50f5ae7228afb87982d6fa9d6b11bf26f`  
		Last Modified: Tue, 15 Nov 2022 05:10:19 GMT  
		Size: 12.2 MB (12207235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0955fb697ea9b30a1b4f95385464f646aa1525cb6efba648e22df84ebef6b2ee`  
		Last Modified: Tue, 15 Nov 2022 05:10:18 GMT  
		Size: 452.0 KB (452021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eddcf66f2083b1487296a0308e0b058917c97f614f12428d82d89662038dc2e`  
		Last Modified: Tue, 15 Nov 2022 05:10:18 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b494e9739298e8928c6c62fa97853f24c5686c66e16581fd0bb2c3f5116121aa`  
		Last Modified: Tue, 15 Nov 2022 18:41:42 GMT  
		Size: 173.3 MB (173347508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9921c8b2af1f61a1ea4272c4674cd1fa433c53c67c6a72173f4d8aba0bbb6b1`  
		Last Modified: Tue, 15 Nov 2022 18:41:38 GMT  
		Size: 310.7 MB (310670016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cf0eb2e7c27d7e3928571dbcab3727cbe408dc96523c057f533e2ff9f6f4f26`  
		Last Modified: Tue, 15 Nov 2022 18:41:23 GMT  
		Size: 2.4 MB (2375234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd899fb62060239a6d0dda3c35638ecb024d47e87e78932bf84f6cb811f3c57a`  
		Last Modified: Tue, 15 Nov 2022 18:41:23 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f716b0a91ab47694081938430c529c80323a2741e8c19d30e34e3a2571fa34ff`  
		Last Modified: Tue, 15 Nov 2022 18:41:23 GMT  
		Size: 2.3 KB (2310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e56d36aa03c1e34c1b7575073acc719da372662ff919607a2b6789a0e0a7141`  
		Last Modified: Tue, 15 Nov 2022 18:41:23 GMT  
		Size: 6.0 KB (5999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5557d6ae4e86cff997abd7b8c8d9567871702f7ae861b0ff81f2cba9afd80368`  
		Last Modified: Tue, 15 Nov 2022 18:41:23 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
