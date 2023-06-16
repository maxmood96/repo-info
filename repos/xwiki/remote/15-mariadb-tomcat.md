## `xwiki:15-mariadb-tomcat`

```console
$ docker pull xwiki@sha256:a71b6830c6b0fbfbdac1a5c38c475d5eb407971e324512e86e29fbe2f9d8429d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:15-mariadb-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:7d5b0b15ea0e96030027b7cac69aff7a51b79d4f83d6bed8e4417857da81a89f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **588.0 MB (588039272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03c5ba73085068a0d5fb034f7bb324bbcc1fea7441c2b397eea26a09737d5091`
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
# Fri, 16 Jun 2023 10:11:17 GMT
ENV XWIKI_VERSION=15.4
# Fri, 16 Jun 2023 10:11:17 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.4
# Fri, 16 Jun 2023 10:11:17 GMT
ENV XWIKI_DOWNLOAD_SHA256=f24def5b4e3f97c56ed03d5983766028676d6ce205bd60d3798352be5a050505
# Fri, 16 Jun 2023 10:11:57 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 16 Jun 2023 10:13:31 GMT
ENV MARIADB_JDBC_VERSION=3.1.4
# Fri, 16 Jun 2023 10:13:31 GMT
ENV MARIADB_JDBC_SHA256=eb88b5d727d82e25117e2b6fabcec1daf734633b0a576456c73215884c189ad4
# Fri, 16 Jun 2023 10:13:31 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.1.4
# Fri, 16 Jun 2023 10:13:32 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.1.4.jar
# Fri, 16 Jun 2023 10:13:32 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.1.4.jar
# Fri, 16 Jun 2023 10:13:32 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Fri, 16 Jun 2023 10:13:32 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 16 Jun 2023 10:13:33 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 16 Jun 2023 10:13:33 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 16 Jun 2023 10:13:33 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 16 Jun 2023 10:13:33 GMT
VOLUME [/usr/local/xwiki]
# Fri, 16 Jun 2023 10:13:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jun 2023 10:13:33 GMT
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
	-	`sha256:0c80f9e73d670c33d5fe706e60a513004a81d3035decf77bfd10f09b12761b37`  
		Last Modified: Fri, 16 Jun 2023 10:15:59 GMT  
		Size: 306.8 MB (306779726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9c74e14b2d260215b88a8f5b38dbaf60ca75436dd31fa55767a3661e5f0593`  
		Last Modified: Fri, 16 Jun 2023 10:17:26 GMT  
		Size: 594.6 KB (594551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7233cd593a469ab22cdbb0b96a1923c224edb5c7c5afb93cb2805e4ddecb5086`  
		Last Modified: Fri, 16 Jun 2023 10:17:26 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:146d8e31efe996e04f601eaf2174fede6f20fa2722872e7e29c9ca4635598eb5`  
		Last Modified: Fri, 16 Jun 2023 10:17:26 GMT  
		Size: 2.3 KB (2312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40922519664f9afd9c5f1fd4453b8535a543a86bdb79a1d897f324c13acf0a45`  
		Last Modified: Fri, 16 Jun 2023 10:17:26 GMT  
		Size: 6.0 KB (5997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034a808158393b89616b1f1a027a4ece7db042538d3def080a8987141bcccdfa`  
		Last Modified: Fri, 16 Jun 2023 10:17:26 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:15-mariadb-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:35de7569e8d91e0962477eae82e8a52f99ab98b95b39269ce20764e942a9f4f2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.3 MB (579342609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90c689be720173c0c75c36386347991355762a3166d257a2bcd6cccb6e2ef25a`
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
# Fri, 16 Jun 2023 08:37:05 GMT
ENV XWIKI_VERSION=15.4
# Fri, 16 Jun 2023 08:37:05 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.4
# Fri, 16 Jun 2023 08:37:05 GMT
ENV XWIKI_DOWNLOAD_SHA256=f24def5b4e3f97c56ed03d5983766028676d6ce205bd60d3798352be5a050505
# Fri, 16 Jun 2023 08:37:45 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 16 Jun 2023 08:39:18 GMT
ENV MARIADB_JDBC_VERSION=3.1.4
# Fri, 16 Jun 2023 08:39:18 GMT
ENV MARIADB_JDBC_SHA256=eb88b5d727d82e25117e2b6fabcec1daf734633b0a576456c73215884c189ad4
# Fri, 16 Jun 2023 08:39:18 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.1.4
# Fri, 16 Jun 2023 08:39:18 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.1.4.jar
# Fri, 16 Jun 2023 08:39:18 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.1.4.jar
# Fri, 16 Jun 2023 08:39:19 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Fri, 16 Jun 2023 08:39:19 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 16 Jun 2023 08:39:19 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 16 Jun 2023 08:39:19 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 16 Jun 2023 08:39:19 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 16 Jun 2023 08:39:19 GMT
VOLUME [/usr/local/xwiki]
# Fri, 16 Jun 2023 08:39:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jun 2023 08:39:20 GMT
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
	-	`sha256:f03776b4882b6f6d330e510053310c11bf6f4dd035683bdb06458c992b9641c0`  
		Last Modified: Fri, 16 Jun 2023 08:41:35 GMT  
		Size: 306.8 MB (306779625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ad6cd045a587271d516b83ff187fa523a4642964be244d1735e7070f86cb17`  
		Last Modified: Fri, 16 Jun 2023 08:42:45 GMT  
		Size: 594.6 KB (594551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98f9b1c4481d86cb06c52e08087181c250fdf873eef521f25e6e48d27ee69144`  
		Last Modified: Fri, 16 Jun 2023 08:42:45 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf326391c2a5c413e913d1f0269a15ff2a1c44103e49e919707e782a4aac7711`  
		Last Modified: Fri, 16 Jun 2023 08:42:45 GMT  
		Size: 2.3 KB (2314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38a086dfe99c5696f6d01298eff0de3205062d5fb1cc3683e4b7500709832df1`  
		Last Modified: Fri, 16 Jun 2023 08:42:45 GMT  
		Size: 6.0 KB (6001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf9cd931d464a82d7a5bdbf9871f36d0ddc5c2136e156fa3e305d20b50f68f2d`  
		Last Modified: Fri, 16 Jun 2023 08:42:45 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
