## `xwiki:postgres-tomcat`

```console
$ docker pull xwiki@sha256:b73eba14eee90d540de90cfe437c5d3f7e8812717b85e4cdf741e35f48c6142b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:2bd9354d893095db36615998a1550605428eed7d44ac0d52a1bbb280f61b9a0c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **582.8 MB (582756044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bd54b0f10afe7fe0aaa9d86ddc5174205b6a2242ef104c0ae2487dd025731cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:25 GMT
ADD file:11157b07dde10107f3f6f2b892c869ea83868475d5825167b5f466a7e410eb05 in / 
# Mon, 06 Jun 2022 22:21:26 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:13:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:13:45 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:14:36 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 00:15:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:15:08 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:15:08 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 28 Jun 2022 00:53:13 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 28 Jun 2022 00:53:13 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jun 2022 00:53:14 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 28 Jun 2022 00:53:14 GMT
WORKDIR /usr/local/tomcat
# Tue, 28 Jun 2022 00:53:14 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 28 Jun 2022 00:53:14 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 28 Jun 2022 01:01:41 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 28 Jun 2022 01:01:41 GMT
ENV TOMCAT_MAJOR=9
# Tue, 28 Jun 2022 01:01:41 GMT
ENV TOMCAT_VERSION=9.0.64
# Tue, 28 Jun 2022 01:01:41 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Tue, 28 Jun 2022 01:01:42 GMT
COPY dir:3930fd28811d9ff8c252dc61af1acc3fb90c82f96a05ddab37a704889908b7d5 in /usr/local/tomcat 
# Tue, 28 Jun 2022 01:01:46 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 28 Jun 2022 01:01:47 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 28 Jun 2022 01:01:47 GMT
EXPOSE 8080
# Tue, 28 Jun 2022 01:01:47 GMT
CMD ["catalina.sh" "run"]
# Tue, 28 Jun 2022 02:34:30 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 28 Jun 2022 02:34:30 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 28 Jun 2022 02:34:30 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 28 Jun 2022 02:34:30 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 28 Jun 2022 02:34:31 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 28 Jun 2022 02:34:31 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 28 Jun 2022 02:38:34 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Wed, 29 Jun 2022 18:38:27 GMT
ENV XWIKI_VERSION=14.5
# Wed, 29 Jun 2022 18:38:27 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.5
# Wed, 29 Jun 2022 18:38:27 GMT
ENV XWIKI_DOWNLOAD_SHA256=fdf6397ebb0036920953d5e7f6d3896b3b8744517b8f00822c31380c24a3e170
# Wed, 29 Jun 2022 18:39:05 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 29 Jun 2022 18:39:06 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Wed, 29 Jun 2022 18:39:06 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 29 Jun 2022 18:39:06 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 29 Jun 2022 18:39:07 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 29 Jun 2022 18:39:07 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 29 Jun 2022 18:39:07 GMT
VOLUME [/usr/local/xwiki]
# Wed, 29 Jun 2022 18:39:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Jun 2022 18:39:07 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:405f018f9d1d0f351c196b841a7c7f226fb8ea448acd6339a9ed8741600275a2`  
		Last Modified: Wed, 01 Jun 2022 03:03:39 GMT  
		Size: 30.4 MB (30423715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c045aca8dd90fbfb1afd1343ec6ce2e08ab62f20e8943d3e313dd745e22ee37`  
		Last Modified: Tue, 07 Jun 2022 00:19:41 GMT  
		Size: 12.1 MB (12116064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:106421360c5cd72b7fd60bc22e213e0b164520c4f38b59358ff4badc098623d5`  
		Last Modified: Tue, 07 Jun 2022 00:21:50 GMT  
		Size: 43.3 MB (43267270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba85ff342cb69c26bcd1a2828d05d82f4622ef9fcc3ff0651092f12d986a5b7`  
		Last Modified: Tue, 07 Jun 2022 00:21:44 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae6ced498c69b2fb1b3a2165254635e3cc1fee3efe9aa8db1693e7716880a141`  
		Last Modified: Tue, 28 Jun 2022 01:20:59 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0101086fc53ce89193416bba986f4262f8b39c136e452b14abc94c54ea116cec`  
		Last Modified: Tue, 28 Jun 2022 01:30:46 GMT  
		Size: 12.2 MB (12180849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7736e38bb6bdf25cacb3ecb1c8e2b152d1bcf0c5f6a839e60b328d238d323ad3`  
		Last Modified: Tue, 28 Jun 2022 01:30:45 GMT  
		Size: 3.0 MB (2959170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0c76df09fa389d90ddb20c84f70331c10103b8fe2e9e1cd128a19900e8b0e8`  
		Last Modified: Tue, 28 Jun 2022 01:30:45 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd1c1206126542f0b02356f1339e7df25663ab08895bd441574b1f0ca860ae3e`  
		Last Modified: Tue, 28 Jun 2022 02:43:18 GMT  
		Size: 179.7 MB (179693072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd57839bf3b2724beadd734132aedcca789a53c6128c3ab4984dfec42491f97`  
		Last Modified: Wed, 29 Jun 2022 18:41:23 GMT  
		Size: 301.2 MB (301166420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81860da280bb38db2c415d62a24dd8312f4c3d511472cc6a4e3b5b01a901444`  
		Last Modified: Wed, 29 Jun 2022 18:41:05 GMT  
		Size: 936.8 KB (936849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4448e065eb52cbc53389a728af82c2210f4f5633dc34c618d47701a69647a3f`  
		Last Modified: Wed, 29 Jun 2022 18:41:05 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc6d174b63be0ad1a5622908db27333132434cbc96d41611af5685f3559d6c6`  
		Last Modified: Wed, 29 Jun 2022 18:41:05 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9668290fca88bd45bf14d71a0dde0f11bb6b5252a1e7fd7aaa1fe13bf139f617`  
		Last Modified: Wed, 29 Jun 2022 18:41:05 GMT  
		Size: 5.9 KB (5871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d0467b259a4f5284773d4d07639bcd2207535b5dc82219e0db72fb25af98b5b`  
		Last Modified: Wed, 29 Jun 2022 18:41:05 GMT  
		Size: 2.5 KB (2501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:81687566df65cf1ffef175b0c6d2a6af7d821e23e629f03ca976e01fabf1852f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **573.9 MB (573863460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a25bb45f6facf2e11e01783ceaad2d0e8900654efe92711ea100c4d62cdb32c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:32 GMT
ADD file:20805b983efd5443e34ebdfb7795010e5684eb1ca1ffea30a3e61e0089c0eee8 in / 
# Tue, 07 Jun 2022 01:25:32 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 06:34:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 06:34:49 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:35:54 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 06:36:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:36:28 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:36:29 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 28 Jun 2022 01:17:40 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 28 Jun 2022 01:17:40 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jun 2022 01:17:41 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 28 Jun 2022 01:17:42 GMT
WORKDIR /usr/local/tomcat
# Tue, 28 Jun 2022 01:17:43 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 28 Jun 2022 01:17:44 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 28 Jun 2022 01:30:02 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 28 Jun 2022 01:30:03 GMT
ENV TOMCAT_MAJOR=9
# Tue, 28 Jun 2022 01:30:04 GMT
ENV TOMCAT_VERSION=9.0.64
# Tue, 28 Jun 2022 01:30:05 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Tue, 28 Jun 2022 01:30:07 GMT
COPY dir:1227788927c6696239176ee756c81fcad123495a654042c4454a9ebfd6b515cc in /usr/local/tomcat 
# Tue, 28 Jun 2022 01:30:14 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 28 Jun 2022 01:30:16 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 28 Jun 2022 01:30:17 GMT
EXPOSE 8080
# Tue, 28 Jun 2022 01:30:18 GMT
CMD ["catalina.sh" "run"]
# Tue, 28 Jun 2022 03:46:17 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 28 Jun 2022 03:46:18 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 28 Jun 2022 03:46:19 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 28 Jun 2022 03:46:20 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 28 Jun 2022 03:46:21 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 28 Jun 2022 03:46:22 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 28 Jun 2022 03:48:35 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Wed, 29 Jun 2022 17:41:44 GMT
ENV XWIKI_VERSION=14.5
# Wed, 29 Jun 2022 17:41:45 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.5
# Wed, 29 Jun 2022 17:41:46 GMT
ENV XWIKI_DOWNLOAD_SHA256=fdf6397ebb0036920953d5e7f6d3896b3b8744517b8f00822c31380c24a3e170
# Wed, 29 Jun 2022 17:42:28 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 29 Jun 2022 17:42:29 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Wed, 29 Jun 2022 17:42:30 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 29 Jun 2022 17:42:31 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 29 Jun 2022 17:42:32 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 29 Jun 2022 17:42:33 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 29 Jun 2022 17:42:33 GMT
VOLUME [/usr/local/xwiki]
# Wed, 29 Jun 2022 17:42:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Jun 2022 17:42:35 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:ed02c6ade914c2962413c1ad2ccc86ed8d1512098f2c87fe7bafa8e1b5293185`  
		Last Modified: Thu, 02 Jun 2022 08:38:25 GMT  
		Size: 28.4 MB (28378212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05aeb470f3c462a081767db5b92aa49a956ba558fd0474c8aa38f2197af012ab`  
		Last Modified: Tue, 07 Jun 2022 06:42:05 GMT  
		Size: 12.1 MB (12078242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c297abb448f33015be27b107b9f8cf65913f603a04a1cfad0e2666fdeab48bc`  
		Last Modified: Tue, 07 Jun 2022 06:44:32 GMT  
		Size: 41.6 MB (41608331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7441efe2a5c7d6ff9883de0fb49763ec7f056a65da14fb5e895dafcaed7db85e`  
		Last Modified: Tue, 07 Jun 2022 06:44:26 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f9c580d62af0ff5116ac217334f3eb761e957bd18731d31dab4dc1d3bb8b554`  
		Last Modified: Tue, 28 Jun 2022 02:00:57 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8cbd2f0254e94cd49f82798b4833d5ee00780c2febbe1796bf816061c6b8cf2`  
		Last Modified: Tue, 28 Jun 2022 02:12:05 GMT  
		Size: 12.2 MB (12187749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:380b6c7b7d3d14cc658bf573d76dfd592b655c1f50c0aa330f37f8949480f1e6`  
		Last Modified: Tue, 28 Jun 2022 02:12:04 GMT  
		Size: 2.8 MB (2794925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17d7d2d980aead8cb8476d4b77a0ee6294f715f43fb8223665a2b6a875ddd420`  
		Last Modified: Tue, 28 Jun 2022 03:55:20 GMT  
		Size: 174.7 MB (174700209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16c65c4e7c4f1d55744507a8fdd150eb82c435ae1dbddca08306496bdacdcb5c`  
		Last Modified: Wed, 29 Jun 2022 17:46:02 GMT  
		Size: 301.2 MB (301166497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c8519f0d0823220fdb732306dcc29bfa01de31ff93bb5d2742a6fd6f4c75dd`  
		Last Modified: Wed, 29 Jun 2022 17:45:39 GMT  
		Size: 936.8 KB (936849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f12a0cb1bf9f65e7efe75c2cc89a9212007da7f4d6488a33c9b73dacc96c9e`  
		Last Modified: Wed, 29 Jun 2022 17:45:39 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c33d5c093466eb5bc89782ffeda9f423569fe4084630826fcd48c5095323f641`  
		Last Modified: Wed, 29 Jun 2022 17:45:39 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4def4059c3fcc79a87c442924613e5af86c087438b012e4bf0c5da24d3f8e0b6`  
		Last Modified: Wed, 29 Jun 2022 17:45:39 GMT  
		Size: 5.9 KB (5870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:148098e57d6f7def82ba26827e966c81813d93b6ccea444c7816f6b41553b2e0`  
		Last Modified: Wed, 29 Jun 2022 17:45:39 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
