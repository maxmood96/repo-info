## `xwiki:stable-mysql-tomcat`

```console
$ docker pull xwiki@sha256:8d7d31b5ba8a5951601ec99df704bccee63e94592a810ee19d6f24b167a4190d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:stable-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:45409b0ffc5e3cf3498037ec1b11461cc57a045d52e1032de907088a14a27c0f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.3 MB (592262781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a37b7bfbfdcae90f8b22aed66a94042dcf26e9ae7fa6679c3e48e766ac3a5e4a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 22 May 2023 17:45:50 GMT
ARG RELEASE
# Mon, 22 May 2023 17:45:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:45:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:45:50 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:45:52 GMT
ADD file:2fd2684e989d275c95e18b6f6e9ccf57ca1382ecd8faf4a66961ede28102dedf in / 
# Mon, 22 May 2023 17:45:52 GMT
CMD ["/bin/bash"]
# Fri, 02 Jun 2023 01:42:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Jun 2023 01:42:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 01:42:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Jun 2023 01:43:03 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 01:43:39 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Fri, 02 Jun 2023 01:44:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 02 Jun 2023 01:44:07 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Sun, 04 Jun 2023 16:55:35 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sun, 04 Jun 2023 16:55:35 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 04 Jun 2023 16:55:35 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sun, 04 Jun 2023 16:55:35 GMT
WORKDIR /usr/local/tomcat
# Sun, 04 Jun 2023 16:55:35 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sun, 04 Jun 2023 16:55:36 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sun, 04 Jun 2023 16:57:10 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Sun, 04 Jun 2023 16:57:10 GMT
ENV TOMCAT_MAJOR=9
# Sun, 04 Jun 2023 16:57:10 GMT
ENV TOMCAT_VERSION=9.0.75
# Sun, 04 Jun 2023 16:57:11 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Sun, 04 Jun 2023 16:57:11 GMT
COPY dir:1a80cba47c440e295efc9e7d8b5d2a176083b42ac8e2147c3112117a9e208e8b in /usr/local/tomcat 
# Sun, 04 Jun 2023 16:57:15 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Sun, 04 Jun 2023 16:57:16 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Sun, 04 Jun 2023 16:57:16 GMT
EXPOSE 8080
# Sun, 04 Jun 2023 16:57:16 GMT
CMD ["catalina.sh" "run"]
# Sun, 04 Jun 2023 17:29:50 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Sun, 04 Jun 2023 17:29:50 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Sun, 04 Jun 2023 17:29:50 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Sun, 04 Jun 2023 17:29:50 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Sun, 04 Jun 2023 17:29:50 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Sun, 04 Jun 2023 17:29:50 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Sun, 04 Jun 2023 17:31:06 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Sun, 04 Jun 2023 17:31:07 GMT
ENV XWIKI_VERSION=15.4
# Sun, 04 Jun 2023 17:31:07 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.4
# Sun, 04 Jun 2023 17:31:07 GMT
ENV XWIKI_DOWNLOAD_SHA256=f24def5b4e3f97c56ed03d5983766028676d6ce205bd60d3798352be5a050505
# Sun, 04 Jun 2023 17:31:46 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Sun, 04 Jun 2023 17:31:47 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Sun, 04 Jun 2023 17:31:47 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Sun, 04 Jun 2023 17:31:47 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Sun, 04 Jun 2023 17:31:47 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Sun, 04 Jun 2023 17:31:47 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Sun, 04 Jun 2023 17:31:48 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Sun, 04 Jun 2023 17:31:48 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Sun, 04 Jun 2023 17:31:48 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Sun, 04 Jun 2023 17:31:49 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Sun, 04 Jun 2023 17:31:49 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Sun, 04 Jun 2023 17:31:49 GMT
VOLUME [/usr/local/xwiki]
# Sun, 04 Jun 2023 17:31:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 04 Jun 2023 17:31:49 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:d1669123f28121211977ed38e663dca1a397c0c001e5386598b96c89b1b1cd51`  
		Last Modified: Mon, 22 May 2023 20:49:59 GMT  
		Size: 30.4 MB (30430275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7723b4ddeaefdff460e5e80fa453e1cc3a321b38d941490f9670da9ac646375b`  
		Last Modified: Fri, 02 Jun 2023 01:46:39 GMT  
		Size: 12.5 MB (12493726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42e8f29e341c2149d867915e16854b80377147f6a9051f61d5d926ccb70dbe17`  
		Last Modified: Fri, 02 Jun 2023 01:47:46 GMT  
		Size: 46.7 MB (46666187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b4e47f3a63c4e338b2efb84d399d9807797b5705ffb8ca8ce9c8214cff3e137`  
		Last Modified: Fri, 02 Jun 2023 01:47:40 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5be4cbf958f0b2c2d0a7a700e3e5fc426dc018b5921f4dce4c3c2e05eb63c3d2`  
		Last Modified: Sun, 04 Jun 2023 17:04:49 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73fbb012430c19e27d21c694e1b0d7a3615b09bd5e282c55f5d0a23dcec76295`  
		Last Modified: Sun, 04 Jun 2023 17:06:37 GMT  
		Size: 12.2 MB (12236714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:005952b2cdfc1bbd34f010bc6ee776a31152593affa0023672580bcacd64c1a6`  
		Last Modified: Sun, 04 Jun 2023 17:06:36 GMT  
		Size: 3.0 MB (2966245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65bb9b9612e2c38d320bb9081d1d4d2cde45efd2b519208eedf63e32ebd97cad`  
		Last Modified: Sun, 04 Jun 2023 17:06:35 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4136ae28feaaaba0ed11f13542411f6ca95b84060ccf2c3fb6f68a8884ffed7c`  
		Last Modified: Sun, 04 Jun 2023 17:35:51 GMT  
		Size: 178.3 MB (178333639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3a16b4fe0289c1690e76770817be4d1ec06769fcc4505552f0ffbd772e5837a`  
		Last Modified: Sun, 04 Jun 2023 17:35:44 GMT  
		Size: 306.8 MB (306779708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e75efdc5145a7071188bb20f1edb5c01c334257f3e153237f83d0e28affabde`  
		Last Modified: Sun, 04 Jun 2023 17:35:27 GMT  
		Size: 2.3 MB (2343673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81bd9aeff677d0857be8501e13ac65d03670dc4044cd732c93d06f2fc41201f5`  
		Last Modified: Sun, 04 Jun 2023 17:35:26 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09950e0b2ff2a5f9c793f1e1b24dc87a08abd2c031e8d62c18e762fb77a8d7c5`  
		Last Modified: Sun, 04 Jun 2023 17:35:26 GMT  
		Size: 2.3 KB (2310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65bd35755b7779ed28e0af0916bc828a9b67b1d93ce708e29b432b9ccdb0f6e9`  
		Last Modified: Sun, 04 Jun 2023 17:35:26 GMT  
		Size: 6.0 KB (5996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6f762205be081c25a67a94391872ee4a44cbaab039e6c01b2bbb9509771251f`  
		Last Modified: Sun, 04 Jun 2023 17:35:26 GMT  
		Size: 2.5 KB (2502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:stable-mysql-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:a8859b4201b0ff577cd0186b4063fd10938053f3e392a327ebf0d7489711fc44
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.4 MB (583385612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dabafcc9f82ea9339b08143546f86bf1556e5ead84e3fc7214ee364ed5a0f72f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 22 May 2023 17:53:00 GMT
ARG RELEASE
# Mon, 22 May 2023 17:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:53:01 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:53:07 GMT
ADD file:f0435ed8dcf91cc69ec63b6b16d9efac56e5a6a7ec518e1fcc3df7457d3113ed in / 
# Mon, 22 May 2023 17:53:08 GMT
CMD ["/bin/bash"]
# Thu, 01 Jun 2023 23:18:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Jun 2023 23:18:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Jun 2023 23:18:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 01 Jun 2023 23:18:44 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 01 Jun 2023 23:19:07 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 01 Jun 2023 23:19:30 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 01 Jun 2023 23:19:31 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 02 Jun 2023 01:57:47 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 02 Jun 2023 01:57:47 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 01:57:48 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 02 Jun 2023 01:57:48 GMT
WORKDIR /usr/local/tomcat
# Fri, 02 Jun 2023 01:57:48 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 02 Jun 2023 01:57:48 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 02 Jun 2023 01:59:05 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 02 Jun 2023 01:59:05 GMT
ENV TOMCAT_MAJOR=9
# Fri, 02 Jun 2023 01:59:05 GMT
ENV TOMCAT_VERSION=9.0.75
# Fri, 02 Jun 2023 01:59:05 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Fri, 02 Jun 2023 01:59:05 GMT
COPY dir:6772160db6f147cd31589cbb67d4cc64fba9465bcc14e4e3f07be9451759501e in /usr/local/tomcat 
# Fri, 02 Jun 2023 01:59:09 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 01:59:10 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 02 Jun 2023 01:59:10 GMT
EXPOSE 8080
# Fri, 02 Jun 2023 01:59:10 GMT
CMD ["catalina.sh" "run"]
# Fri, 02 Jun 2023 03:24:00 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 02 Jun 2023 03:24:00 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 02 Jun 2023 03:24:00 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 02 Jun 2023 03:24:00 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 02 Jun 2023 03:24:00 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 02 Jun 2023 03:24:00 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 02 Jun 2023 03:25:42 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 03:25:45 GMT
ENV XWIKI_VERSION=15.4
# Fri, 02 Jun 2023 03:25:45 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.4
# Fri, 02 Jun 2023 03:25:45 GMT
ENV XWIKI_DOWNLOAD_SHA256=f24def5b4e3f97c56ed03d5983766028676d6ce205bd60d3798352be5a050505
# Fri, 02 Jun 2023 03:26:26 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 02 Jun 2023 03:26:28 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Fri, 02 Jun 2023 03:26:28 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Fri, 02 Jun 2023 03:26:28 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Fri, 02 Jun 2023 03:26:28 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Fri, 02 Jun 2023 03:26:28 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Fri, 02 Jun 2023 03:26:29 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 02 Jun 2023 03:26:29 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 02 Jun 2023 03:26:29 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 02 Jun 2023 03:26:29 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 02 Jun 2023 03:26:29 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 02 Jun 2023 03:26:29 GMT
VOLUME [/usr/local/xwiki]
# Fri, 02 Jun 2023 03:26:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Jun 2023 03:26:30 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:6c7698a779f6d8c45a39a6721fb5cce267d66ff8ab5181c55aa6d02c8ddacd01`  
		Last Modified: Tue, 23 May 2023 02:05:13 GMT  
		Size: 28.4 MB (28389044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f90f9c81eab3c275d75f3cf9f4840e195cfa7c5372d500bfeb5a040f3fc88262`  
		Last Modified: Thu, 01 Jun 2023 23:21:25 GMT  
		Size: 12.5 MB (12452855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6fcc328ac0affca0471a6a1d24001fbf5d6927268b63108576c160df5647af7`  
		Last Modified: Thu, 01 Jun 2023 23:22:22 GMT  
		Size: 45.0 MB (45009479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cf5c29166d38f94500a3660aa3baef35070a8822a01cc0d45dd1ca1e9ace769`  
		Last Modified: Thu, 01 Jun 2023 23:22:18 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c37df8cc9a991ed50f676003a7c9f6ebeeaa4b5b28a42b6126522c569938d544`  
		Last Modified: Fri, 02 Jun 2023 02:06:06 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e19b4e105eebc0ba47bb90c9ef63b8c9b604e0cee4eab1fb482a68b3664586`  
		Last Modified: Fri, 02 Jun 2023 02:07:50 GMT  
		Size: 12.2 MB (12242189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4850a1ed957a95b8a94a2957ccd1b4ed1227f7c8997a70eed6f9ff693b648e8e`  
		Last Modified: Fri, 02 Jun 2023 02:07:50 GMT  
		Size: 2.8 MB (2806582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c42a0a43520047ad78ac489284036db953e98cca2d1d4bd31b523bd0c6ba28`  
		Last Modified: Fri, 02 Jun 2023 02:07:49 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:616eeb0d98e442348091228bd6eca84c2670b963a7ea7bd083875cb0d3a97862`  
		Last Modified: Fri, 02 Jun 2023 03:30:20 GMT  
		Size: 173.3 MB (173349470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3294b0658c293f95f1b4c42dace3400a7c838d608ba7e56b604f1e0e221d011a`  
		Last Modified: Fri, 02 Jun 2023 03:30:15 GMT  
		Size: 306.8 MB (306779696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d857c6edde344c3fbf44cc189f3f5a8ea6b4ef625d3a19045c9c485bf1730d`  
		Last Modified: Fri, 02 Jun 2023 03:30:02 GMT  
		Size: 2.3 MB (2343675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0da99bba1d28c6aa28a0cf723b6603a86869a48bcbfeeba949ffd164b55e178b`  
		Last Modified: Fri, 02 Jun 2023 03:30:01 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e5e80cd7d8361eb4e69a4119de93b3b927170ba29d94c26a426066da324e492`  
		Last Modified: Fri, 02 Jun 2023 03:30:01 GMT  
		Size: 2.3 KB (2311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d00b3930db265f04e1d44e6e3901e5eb2e7a65e73d89f2d34804923390057731`  
		Last Modified: Fri, 02 Jun 2023 03:30:01 GMT  
		Size: 6.0 KB (5996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb3f39098700d45a0c5ebafe07440a744a37668b3b033191fe4a698950d06c0`  
		Last Modified: Fri, 02 Jun 2023 03:30:01 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
