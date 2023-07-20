<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `xwiki`

-	[`xwiki:14`](#xwiki14)
-	[`xwiki:14-mariadb-tomcat`](#xwiki14-mariadb-tomcat)
-	[`xwiki:14-mysql-tomcat`](#xwiki14-mysql-tomcat)
-	[`xwiki:14-postgres-tomcat`](#xwiki14-postgres-tomcat)
-	[`xwiki:14.10`](#xwiki1410)
-	[`xwiki:14.10-mariadb-tomcat`](#xwiki1410-mariadb-tomcat)
-	[`xwiki:14.10-mysql-tomcat`](#xwiki1410-mysql-tomcat)
-	[`xwiki:14.10-postgres-tomcat`](#xwiki1410-postgres-tomcat)
-	[`xwiki:14.10.14`](#xwiki141014)
-	[`xwiki:14.10.14-mariadb-tomcat`](#xwiki141014-mariadb-tomcat)
-	[`xwiki:14.10.14-mysql-tomcat`](#xwiki141014-mysql-tomcat)
-	[`xwiki:14.10.14-postgres-tomcat`](#xwiki141014-postgres-tomcat)
-	[`xwiki:15`](#xwiki15)
-	[`xwiki:15-mariadb-tomcat`](#xwiki15-mariadb-tomcat)
-	[`xwiki:15-mysql-tomcat`](#xwiki15-mysql-tomcat)
-	[`xwiki:15-postgres-tomcat`](#xwiki15-postgres-tomcat)
-	[`xwiki:15.5`](#xwiki155)
-	[`xwiki:15.5-mariadb-tomcat`](#xwiki155-mariadb-tomcat)
-	[`xwiki:15.5-mysql-tomcat`](#xwiki155-mysql-tomcat)
-	[`xwiki:15.5-postgres-tomcat`](#xwiki155-postgres-tomcat)
-	[`xwiki:15.5.0`](#xwiki1550)
-	[`xwiki:15.5.0-mariadb-tomcat`](#xwiki1550-mariadb-tomcat)
-	[`xwiki:15.5.0-mysql-tomcat`](#xwiki1550-mysql-tomcat)
-	[`xwiki:15.5.0-postgres-tomcat`](#xwiki1550-postgres-tomcat)
-	[`xwiki:latest`](#xwikilatest)
-	[`xwiki:lts`](#xwikilts)
-	[`xwiki:lts-mariadb`](#xwikilts-mariadb)
-	[`xwiki:lts-mariadb-tomcat`](#xwikilts-mariadb-tomcat)
-	[`xwiki:lts-mysql`](#xwikilts-mysql)
-	[`xwiki:lts-mysql-tomcat`](#xwikilts-mysql-tomcat)
-	[`xwiki:lts-postgres`](#xwikilts-postgres)
-	[`xwiki:lts-postgres-tomcat`](#xwikilts-postgres-tomcat)
-	[`xwiki:mariadb-tomcat`](#xwikimariadb-tomcat)
-	[`xwiki:mysql-tomcat`](#xwikimysql-tomcat)
-	[`xwiki:postgres-tomcat`](#xwikipostgres-tomcat)
-	[`xwiki:stable`](#xwikistable)
-	[`xwiki:stable-mariadb`](#xwikistable-mariadb)
-	[`xwiki:stable-mariadb-tomcat`](#xwikistable-mariadb-tomcat)
-	[`xwiki:stable-mysql`](#xwikistable-mysql)
-	[`xwiki:stable-mysql-tomcat`](#xwikistable-mysql-tomcat)
-	[`xwiki:stable-postgres`](#xwikistable-postgres)
-	[`xwiki:stable-postgres-tomcat`](#xwikistable-postgres-tomcat)

## `xwiki:14`

```console
$ docker pull xwiki@sha256:d684b69a373a2cef6fa2a32d55c3e87eed6a6f36cfac5320606e88204e88186a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:14` - linux; amd64

```console
$ docker pull xwiki@sha256:ede13785f63dcaf8042ae3ad55c0c8fa410a3832504cdcf66916035506feebc9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.3 MB (590275216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0cdff4d327d68685f5dd8da61be21269df316c760ef6487e0aa642ec059b882`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:37:40 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:37:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:37:42 GMT
ADD file:140fb5108b4a2861b5718ad03b4a5174bba03589ea8d4c053e6a0b282f439ff3 in / 
# Wed, 28 Jun 2023 08:37:42 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:34:07 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:35:02 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 20:35:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 20:35:35 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 08:22:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 08:22:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 08:22:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 08:22:21 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 08:22:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:22:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:25:33 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 08:25:34 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 00:16:15 GMT
COPY dir:8ddeace4a16f09a0d97488e225c7b2e4a48c9a93484d24b46a09759f52800501 in /usr/local/tomcat 
# Tue, 11 Jul 2023 00:16:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 00:16:20 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 00:16:20 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 00:16:20 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 04:40:02 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 04:42:15 GMT
ENV XWIKI_VERSION=14.10.13
# Tue, 11 Jul 2023 04:42:15 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.13
# Tue, 11 Jul 2023 04:42:15 GMT
ENV XWIKI_DOWNLOAD_SHA256=5883ffdbc10865043778f3caa48fbca900129cf41c76ee6fdafba74769c928d4
# Tue, 11 Jul 2023 04:42:54 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 04:42:54 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Tue, 11 Jul 2023 04:42:55 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Tue, 11 Jul 2023 04:42:55 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Tue, 11 Jul 2023 04:42:55 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 04:42:55 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 04:42:56 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Tue, 11 Jul 2023 04:42:56 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 04:42:56 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 04:42:56 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 04:42:56 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 04:42:56 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 04:42:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 04:42:57 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:9d19ee268e0d7bcf6716e6658ee1b0384a71d6f2f9aa1ae2085610cf7c7b316f`  
		Last Modified: Wed, 28 Jun 2023 11:50:41 GMT  
		Size: 30.4 MB (30431229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32db0ad82863deaedd2f9a365e52f595085778d28bd1e6f1d351107590cad806`  
		Last Modified: Tue, 04 Jul 2023 20:39:05 GMT  
		Size: 12.5 MB (12495341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01bb55fbcae928d7e6c08d6618580d2b27ce6e46083f861bbed1e01db41c20b`  
		Last Modified: Tue, 04 Jul 2023 20:41:01 GMT  
		Size: 46.7 MB (46666353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297c6e3f57ee032a3cc5f0fd28b52687129e7a1e6485aea12aff08cb6620071e`  
		Last Modified: Tue, 04 Jul 2023 20:40:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15b01f5ab5b71b356d93dff08f5037af8e8a03b4657f1fd303052261161ebd8`  
		Last Modified: Wed, 05 Jul 2023 08:37:14 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c6051a2b9ffe906ea99b555033966c877468da73cd19fd793c86099d0af531`  
		Last Modified: Tue, 11 Jul 2023 00:38:45 GMT  
		Size: 12.3 MB (12274167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34aaed1f6a3460fc256e262b462c1180ccef1b0665ffd50f900d1ef9c19f1d24`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 454.7 KB (454674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b809bf54ada009dfd91afa6ad239f7a791807f2928941b7f969493ec38246be`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877cc60516baaeb7846bba5d5de9e491d0406cd2f43959d7d4e104d89df5e228`  
		Last Modified: Tue, 11 Jul 2023 04:44:49 GMT  
		Size: 178.3 MB (178335971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d83ab8708da1a9ab9fb6a48ac52687e3488789fccbd4a07ced23e73be97d1b`  
		Last Modified: Tue, 11 Jul 2023 04:46:37 GMT  
		Size: 307.3 MB (307261194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:663bd82ddfd62b4cf39556e967220c977dcdbb37a1fd053c779fd0baa6898818`  
		Last Modified: Tue, 11 Jul 2023 04:46:21 GMT  
		Size: 2.3 MB (2343668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed5bec13f08d98c63e3c81fb0a45f8734746d82b5504310835cac9e7a8e18dec`  
		Last Modified: Tue, 11 Jul 2023 04:46:21 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dfccb5d359b6e3ae2ddf7257f81d0e9b794f602ab4e3f3196c372af5543d1ca`  
		Last Modified: Tue, 11 Jul 2023 04:46:21 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac17a1dc4319814e728392d0b0b3ad40083d48efeaec075e52bdaef3545341d0`  
		Last Modified: Tue, 11 Jul 2023 04:46:21 GMT  
		Size: 6.0 KB (6015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57f2437b546ab6322d8db9cf14928c907568c9728574599d16ea306286ab824c`  
		Last Modified: Tue, 11 Jul 2023 04:46:21 GMT  
		Size: 2.5 KB (2498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:14` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:2c70da3ff6aad987960017b1f402de397c9e9a3b3f806a125702c26c14a1bfb8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.6 MB (581585177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a5e15a24190e32ccad68b6a75aa965123ee8a3fd0edd724d8cbaecbcf34acf6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:42:48 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:42:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:42:50 GMT
ADD file:262490f82459c14632f5c9a6d6a5cf6c07b4f307e8fd380fa764662cda46e88f in / 
# Wed, 28 Jun 2023 08:42:50 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:59 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 15:33:41 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 15:34:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 15:34:08 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 02:55:59 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 02:55:59 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 02:55:59 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 02:55:59 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 02:56:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 02:56:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 03:00:51 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 03:00:51 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 01:18:24 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 01:18:25 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 01:18:25 GMT
COPY dir:1743191a9534b9e7d795d3bf9ad18535d99e75967877447e17d7b63574d878d5 in /usr/local/tomcat 
# Tue, 11 Jul 2023 01:18:28 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 01:18:29 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 01:18:29 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 01:18:29 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 05:21:20 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 05:23:40 GMT
ENV XWIKI_VERSION=14.10.13
# Tue, 11 Jul 2023 05:23:40 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.13
# Tue, 11 Jul 2023 05:23:40 GMT
ENV XWIKI_DOWNLOAD_SHA256=5883ffdbc10865043778f3caa48fbca900129cf41c76ee6fdafba74769c928d4
# Tue, 11 Jul 2023 05:24:20 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 05:24:23 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Tue, 11 Jul 2023 05:24:23 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Tue, 11 Jul 2023 05:24:23 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Tue, 11 Jul 2023 05:24:23 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 05:24:23 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 05:24:24 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Tue, 11 Jul 2023 05:24:24 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 05:24:24 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 05:24:25 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 05:24:25 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 05:24:25 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 05:24:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 05:24:25 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:ac34a2e0269ced3acc355be706239ee0f3f1e73a035c40dd2fac74827164ee53`  
		Last Modified: Wed, 28 Jun 2023 23:23:40 GMT  
		Size: 28.4 MB (28391011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d9df805749ad7c4605f0d49a64da6a6173ab190ec361dc2063b6b73af59ab5`  
		Last Modified: Tue, 04 Jul 2023 15:36:55 GMT  
		Size: 12.5 MB (12455497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1e11a5919e5746092b2a288f71090ffdb0d3544b7b54c31ed0137e6d5d4735`  
		Last Modified: Tue, 04 Jul 2023 15:38:37 GMT  
		Size: 45.0 MB (45009079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80987dc89da28aa5ceec7a86ea74e13cee06ecd9304cf4c92d8f382c79eb4f2`  
		Last Modified: Tue, 04 Jul 2023 15:38:32 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de67c7824eef053da628456fe8aba244c4150024af9454dd4091763920d836c`  
		Last Modified: Wed, 05 Jul 2023 03:14:23 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f77f07e56c3d3019cd346deaeacbe572b15b26a924c19b6386877b47123a89e`  
		Last Modified: Tue, 11 Jul 2023 01:39:24 GMT  
		Size: 12.3 MB (12283700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2422cddd65b0ff63d783c999d005c42281720b8615f5872e1e8fdb32dd9981d9`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 455.1 KB (455052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b023f0d964d565a960e567dcaaa605fdff6da02b54971f4d0693506b481b8c`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28177f0763a75e5c940bb6a7919185effccd7cf14c0e350198b3aedbe1db789`  
		Last Modified: Tue, 11 Jul 2023 05:26:01 GMT  
		Size: 173.4 MB (173373450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc5b16765fdc498e3f3e0db1f6f5968716864f931b8490f2092985f2aad66e6`  
		Last Modified: Tue, 11 Jul 2023 05:27:47 GMT  
		Size: 307.3 MB (307261061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e05260decea8ae0b8e52961a6b822e7f61aa0d94e359d9bdfb0a8d1c12ab373`  
		Last Modified: Tue, 11 Jul 2023 05:27:33 GMT  
		Size: 2.3 MB (2343684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80db78e6c67fd96e8da400c8505c850ac34058465e92e7c08c2079a56c581eef`  
		Last Modified: Tue, 11 Jul 2023 05:27:32 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e13d3d8f1788f25950792ca1b21389742cb964f69af7853cd12c938239fa7c94`  
		Last Modified: Tue, 11 Jul 2023 05:27:33 GMT  
		Size: 2.3 KB (2311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ecfdbab47ad32f6ddf82bd2c97ac1e2786af57d2bfc2653639b91c3a1833a3`  
		Last Modified: Tue, 11 Jul 2023 05:27:32 GMT  
		Size: 6.0 KB (6020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0b9874cce7da8c08bc10f43d1a239ff6d3d1b18189a83d61bf566a352cba781`  
		Last Modified: Tue, 11 Jul 2023 05:27:32 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:14-mariadb-tomcat`

```console
$ docker pull xwiki@sha256:4f0cfbbcc4d2a7ab73eac160f70b796dbe864d041ce38174443170e66be4e82c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:14-mariadb-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:2457ece1ecfc0fdb7b33b40d99e1cc0e647b34427eb7d3adf0321d7035832bd7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **588.5 MB (588526114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23dabbcf30b0cba2e6e27db54197aadc63470a751d0cf652f95c6ffc4dc48bc5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:37:40 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:37:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:37:42 GMT
ADD file:140fb5108b4a2861b5718ad03b4a5174bba03589ea8d4c053e6a0b282f439ff3 in / 
# Wed, 28 Jun 2023 08:37:42 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:34:07 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:35:02 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 20:35:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 20:35:35 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 08:22:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 08:22:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 08:22:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 08:22:21 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 08:22:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:22:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:25:33 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 08:25:34 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 00:16:15 GMT
COPY dir:8ddeace4a16f09a0d97488e225c7b2e4a48c9a93484d24b46a09759f52800501 in /usr/local/tomcat 
# Tue, 11 Jul 2023 00:16:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 00:16:20 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 00:16:20 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 00:16:20 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 04:40:02 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 04:42:15 GMT
ENV XWIKI_VERSION=14.10.13
# Tue, 11 Jul 2023 04:42:15 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.13
# Tue, 11 Jul 2023 04:42:15 GMT
ENV XWIKI_DOWNLOAD_SHA256=5883ffdbc10865043778f3caa48fbca900129cf41c76ee6fdafba74769c928d4
# Tue, 11 Jul 2023 04:42:54 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 04:43:53 GMT
ENV MARIADB_JDBC_VERSION=3.1.4
# Tue, 11 Jul 2023 04:43:53 GMT
ENV MARIADB_JDBC_SHA256=eb88b5d727d82e25117e2b6fabcec1daf734633b0a576456c73215884c189ad4
# Tue, 11 Jul 2023 04:43:53 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.1.4
# Tue, 11 Jul 2023 04:43:53 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.1.4.jar
# Tue, 11 Jul 2023 04:43:53 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.1.4.jar
# Tue, 11 Jul 2023 04:43:54 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Tue, 11 Jul 2023 04:43:54 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 04:43:54 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 04:43:55 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 04:43:55 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 04:43:55 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 04:43:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 04:43:55 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:9d19ee268e0d7bcf6716e6658ee1b0384a71d6f2f9aa1ae2085610cf7c7b316f`  
		Last Modified: Wed, 28 Jun 2023 11:50:41 GMT  
		Size: 30.4 MB (30431229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32db0ad82863deaedd2f9a365e52f595085778d28bd1e6f1d351107590cad806`  
		Last Modified: Tue, 04 Jul 2023 20:39:05 GMT  
		Size: 12.5 MB (12495341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01bb55fbcae928d7e6c08d6618580d2b27ce6e46083f861bbed1e01db41c20b`  
		Last Modified: Tue, 04 Jul 2023 20:41:01 GMT  
		Size: 46.7 MB (46666353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297c6e3f57ee032a3cc5f0fd28b52687129e7a1e6485aea12aff08cb6620071e`  
		Last Modified: Tue, 04 Jul 2023 20:40:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15b01f5ab5b71b356d93dff08f5037af8e8a03b4657f1fd303052261161ebd8`  
		Last Modified: Wed, 05 Jul 2023 08:37:14 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c6051a2b9ffe906ea99b555033966c877468da73cd19fd793c86099d0af531`  
		Last Modified: Tue, 11 Jul 2023 00:38:45 GMT  
		Size: 12.3 MB (12274167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34aaed1f6a3460fc256e262b462c1180ccef1b0665ffd50f900d1ef9c19f1d24`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 454.7 KB (454674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b809bf54ada009dfd91afa6ad239f7a791807f2928941b7f969493ec38246be`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877cc60516baaeb7846bba5d5de9e491d0406cd2f43959d7d4e104d89df5e228`  
		Last Modified: Tue, 11 Jul 2023 04:44:49 GMT  
		Size: 178.3 MB (178335971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d83ab8708da1a9ab9fb6a48ac52687e3488789fccbd4a07ced23e73be97d1b`  
		Last Modified: Tue, 11 Jul 2023 04:46:37 GMT  
		Size: 307.3 MB (307261194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e875fea8a2c98d9a649ede02e5cde89adc140d705cd90f987da3c01c0e0e91ba`  
		Last Modified: Tue, 11 Jul 2023 04:47:34 GMT  
		Size: 594.6 KB (594551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03c934df3cbcee083ccb0b050eb79b8a33e576b12a5d653cf3779efd73ae0886`  
		Last Modified: Tue, 11 Jul 2023 04:47:34 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:169d82fe476f2ba0c25f369977bcad3dbefc51aecdd90854d3d5bd162ffca191`  
		Last Modified: Tue, 11 Jul 2023 04:47:34 GMT  
		Size: 2.3 KB (2309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2bc34d1fe1755d4b6c92a1f18f895229ebbd1c4c33b8d9870ad601f460c6e30`  
		Last Modified: Tue, 11 Jul 2023 04:47:34 GMT  
		Size: 6.0 KB (6017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dc85b4209f7c5902eaddc9237e35ff851834dbe9a46b12cda8f7c6bd37e98f0`  
		Last Modified: Tue, 11 Jul 2023 04:47:33 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:14-mariadb-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:f2d58b0e807535f9a89d2aefdb36e0ed212696276c598c6ac7a44ae4a463571e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.8 MB (579836046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4827d8602436ba34af88ff0bccf958bc03dbf862b5011c12c3799c90dba3626a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:42:48 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:42:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:42:50 GMT
ADD file:262490f82459c14632f5c9a6d6a5cf6c07b4f307e8fd380fa764662cda46e88f in / 
# Wed, 28 Jun 2023 08:42:50 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:59 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 15:33:41 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 15:34:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 15:34:08 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 02:55:59 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 02:55:59 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 02:55:59 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 02:55:59 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 02:56:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 02:56:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 03:00:51 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 03:00:51 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 01:18:24 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 01:18:25 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 01:18:25 GMT
COPY dir:1743191a9534b9e7d795d3bf9ad18535d99e75967877447e17d7b63574d878d5 in /usr/local/tomcat 
# Tue, 11 Jul 2023 01:18:28 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 01:18:29 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 01:18:29 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 01:18:29 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 05:21:20 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 05:23:40 GMT
ENV XWIKI_VERSION=14.10.13
# Tue, 11 Jul 2023 05:23:40 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.13
# Tue, 11 Jul 2023 05:23:40 GMT
ENV XWIKI_DOWNLOAD_SHA256=5883ffdbc10865043778f3caa48fbca900129cf41c76ee6fdafba74769c928d4
# Tue, 11 Jul 2023 05:24:20 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 05:25:16 GMT
ENV MARIADB_JDBC_VERSION=3.1.4
# Tue, 11 Jul 2023 05:25:16 GMT
ENV MARIADB_JDBC_SHA256=eb88b5d727d82e25117e2b6fabcec1daf734633b0a576456c73215884c189ad4
# Tue, 11 Jul 2023 05:25:16 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.1.4
# Tue, 11 Jul 2023 05:25:16 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.1.4.jar
# Tue, 11 Jul 2023 05:25:17 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.1.4.jar
# Tue, 11 Jul 2023 05:25:17 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Tue, 11 Jul 2023 05:25:17 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 05:25:17 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 05:25:18 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 05:25:18 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 05:25:18 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 05:25:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 05:25:18 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:ac34a2e0269ced3acc355be706239ee0f3f1e73a035c40dd2fac74827164ee53`  
		Last Modified: Wed, 28 Jun 2023 23:23:40 GMT  
		Size: 28.4 MB (28391011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d9df805749ad7c4605f0d49a64da6a6173ab190ec361dc2063b6b73af59ab5`  
		Last Modified: Tue, 04 Jul 2023 15:36:55 GMT  
		Size: 12.5 MB (12455497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1e11a5919e5746092b2a288f71090ffdb0d3544b7b54c31ed0137e6d5d4735`  
		Last Modified: Tue, 04 Jul 2023 15:38:37 GMT  
		Size: 45.0 MB (45009079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80987dc89da28aa5ceec7a86ea74e13cee06ecd9304cf4c92d8f382c79eb4f2`  
		Last Modified: Tue, 04 Jul 2023 15:38:32 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de67c7824eef053da628456fe8aba244c4150024af9454dd4091763920d836c`  
		Last Modified: Wed, 05 Jul 2023 03:14:23 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f77f07e56c3d3019cd346deaeacbe572b15b26a924c19b6386877b47123a89e`  
		Last Modified: Tue, 11 Jul 2023 01:39:24 GMT  
		Size: 12.3 MB (12283700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2422cddd65b0ff63d783c999d005c42281720b8615f5872e1e8fdb32dd9981d9`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 455.1 KB (455052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b023f0d964d565a960e567dcaaa605fdff6da02b54971f4d0693506b481b8c`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28177f0763a75e5c940bb6a7919185effccd7cf14c0e350198b3aedbe1db789`  
		Last Modified: Tue, 11 Jul 2023 05:26:01 GMT  
		Size: 173.4 MB (173373450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc5b16765fdc498e3f3e0db1f6f5968716864f931b8490f2092985f2aad66e6`  
		Last Modified: Tue, 11 Jul 2023 05:27:47 GMT  
		Size: 307.3 MB (307261061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cde3b2925cca0eaeca051a9d34fc8559173eb81198be6edb87ef675ddbd104c`  
		Last Modified: Tue, 11 Jul 2023 05:28:44 GMT  
		Size: 594.6 KB (594553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a572ecd6de904372e67871760ea39b4c45f94b03c1bd47a6ee27a1151f44f25`  
		Last Modified: Tue, 11 Jul 2023 05:28:43 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48dc7acaf3762507fe63c6d484d73da83682cfc993ce96feccb9b0cb2bea8895`  
		Last Modified: Tue, 11 Jul 2023 05:28:43 GMT  
		Size: 2.3 KB (2314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd91b38c50762886b672122ce7698e839324aa39970db075d8fa1a46ae5d6fe5`  
		Last Modified: Tue, 11 Jul 2023 05:28:43 GMT  
		Size: 6.0 KB (6018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:536a460fc0ee741e1de6915eb0f7533df412ab1b9c51ac2f7686ca966abef1fc`  
		Last Modified: Tue, 11 Jul 2023 05:28:43 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:14-mysql-tomcat`

```console
$ docker pull xwiki@sha256:d684b69a373a2cef6fa2a32d55c3e87eed6a6f36cfac5320606e88204e88186a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:14-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:ede13785f63dcaf8042ae3ad55c0c8fa410a3832504cdcf66916035506feebc9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.3 MB (590275216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0cdff4d327d68685f5dd8da61be21269df316c760ef6487e0aa642ec059b882`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:37:40 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:37:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:37:42 GMT
ADD file:140fb5108b4a2861b5718ad03b4a5174bba03589ea8d4c053e6a0b282f439ff3 in / 
# Wed, 28 Jun 2023 08:37:42 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:34:07 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:35:02 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 20:35:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 20:35:35 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 08:22:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 08:22:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 08:22:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 08:22:21 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 08:22:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:22:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:25:33 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 08:25:34 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 00:16:15 GMT
COPY dir:8ddeace4a16f09a0d97488e225c7b2e4a48c9a93484d24b46a09759f52800501 in /usr/local/tomcat 
# Tue, 11 Jul 2023 00:16:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 00:16:20 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 00:16:20 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 00:16:20 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 04:40:02 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 04:42:15 GMT
ENV XWIKI_VERSION=14.10.13
# Tue, 11 Jul 2023 04:42:15 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.13
# Tue, 11 Jul 2023 04:42:15 GMT
ENV XWIKI_DOWNLOAD_SHA256=5883ffdbc10865043778f3caa48fbca900129cf41c76ee6fdafba74769c928d4
# Tue, 11 Jul 2023 04:42:54 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 04:42:54 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Tue, 11 Jul 2023 04:42:55 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Tue, 11 Jul 2023 04:42:55 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Tue, 11 Jul 2023 04:42:55 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 04:42:55 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 04:42:56 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Tue, 11 Jul 2023 04:42:56 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 04:42:56 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 04:42:56 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 04:42:56 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 04:42:56 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 04:42:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 04:42:57 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:9d19ee268e0d7bcf6716e6658ee1b0384a71d6f2f9aa1ae2085610cf7c7b316f`  
		Last Modified: Wed, 28 Jun 2023 11:50:41 GMT  
		Size: 30.4 MB (30431229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32db0ad82863deaedd2f9a365e52f595085778d28bd1e6f1d351107590cad806`  
		Last Modified: Tue, 04 Jul 2023 20:39:05 GMT  
		Size: 12.5 MB (12495341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01bb55fbcae928d7e6c08d6618580d2b27ce6e46083f861bbed1e01db41c20b`  
		Last Modified: Tue, 04 Jul 2023 20:41:01 GMT  
		Size: 46.7 MB (46666353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297c6e3f57ee032a3cc5f0fd28b52687129e7a1e6485aea12aff08cb6620071e`  
		Last Modified: Tue, 04 Jul 2023 20:40:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15b01f5ab5b71b356d93dff08f5037af8e8a03b4657f1fd303052261161ebd8`  
		Last Modified: Wed, 05 Jul 2023 08:37:14 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c6051a2b9ffe906ea99b555033966c877468da73cd19fd793c86099d0af531`  
		Last Modified: Tue, 11 Jul 2023 00:38:45 GMT  
		Size: 12.3 MB (12274167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34aaed1f6a3460fc256e262b462c1180ccef1b0665ffd50f900d1ef9c19f1d24`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 454.7 KB (454674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b809bf54ada009dfd91afa6ad239f7a791807f2928941b7f969493ec38246be`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877cc60516baaeb7846bba5d5de9e491d0406cd2f43959d7d4e104d89df5e228`  
		Last Modified: Tue, 11 Jul 2023 04:44:49 GMT  
		Size: 178.3 MB (178335971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d83ab8708da1a9ab9fb6a48ac52687e3488789fccbd4a07ced23e73be97d1b`  
		Last Modified: Tue, 11 Jul 2023 04:46:37 GMT  
		Size: 307.3 MB (307261194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:663bd82ddfd62b4cf39556e967220c977dcdbb37a1fd053c779fd0baa6898818`  
		Last Modified: Tue, 11 Jul 2023 04:46:21 GMT  
		Size: 2.3 MB (2343668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed5bec13f08d98c63e3c81fb0a45f8734746d82b5504310835cac9e7a8e18dec`  
		Last Modified: Tue, 11 Jul 2023 04:46:21 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dfccb5d359b6e3ae2ddf7257f81d0e9b794f602ab4e3f3196c372af5543d1ca`  
		Last Modified: Tue, 11 Jul 2023 04:46:21 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac17a1dc4319814e728392d0b0b3ad40083d48efeaec075e52bdaef3545341d0`  
		Last Modified: Tue, 11 Jul 2023 04:46:21 GMT  
		Size: 6.0 KB (6015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57f2437b546ab6322d8db9cf14928c907568c9728574599d16ea306286ab824c`  
		Last Modified: Tue, 11 Jul 2023 04:46:21 GMT  
		Size: 2.5 KB (2498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:14-mysql-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:2c70da3ff6aad987960017b1f402de397c9e9a3b3f806a125702c26c14a1bfb8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.6 MB (581585177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a5e15a24190e32ccad68b6a75aa965123ee8a3fd0edd724d8cbaecbcf34acf6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:42:48 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:42:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:42:50 GMT
ADD file:262490f82459c14632f5c9a6d6a5cf6c07b4f307e8fd380fa764662cda46e88f in / 
# Wed, 28 Jun 2023 08:42:50 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:59 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 15:33:41 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 15:34:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 15:34:08 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 02:55:59 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 02:55:59 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 02:55:59 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 02:55:59 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 02:56:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 02:56:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 03:00:51 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 03:00:51 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 01:18:24 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 01:18:25 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 01:18:25 GMT
COPY dir:1743191a9534b9e7d795d3bf9ad18535d99e75967877447e17d7b63574d878d5 in /usr/local/tomcat 
# Tue, 11 Jul 2023 01:18:28 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 01:18:29 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 01:18:29 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 01:18:29 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 05:21:20 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 05:23:40 GMT
ENV XWIKI_VERSION=14.10.13
# Tue, 11 Jul 2023 05:23:40 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.13
# Tue, 11 Jul 2023 05:23:40 GMT
ENV XWIKI_DOWNLOAD_SHA256=5883ffdbc10865043778f3caa48fbca900129cf41c76ee6fdafba74769c928d4
# Tue, 11 Jul 2023 05:24:20 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 05:24:23 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Tue, 11 Jul 2023 05:24:23 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Tue, 11 Jul 2023 05:24:23 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Tue, 11 Jul 2023 05:24:23 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 05:24:23 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 05:24:24 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Tue, 11 Jul 2023 05:24:24 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 05:24:24 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 05:24:25 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 05:24:25 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 05:24:25 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 05:24:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 05:24:25 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:ac34a2e0269ced3acc355be706239ee0f3f1e73a035c40dd2fac74827164ee53`  
		Last Modified: Wed, 28 Jun 2023 23:23:40 GMT  
		Size: 28.4 MB (28391011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d9df805749ad7c4605f0d49a64da6a6173ab190ec361dc2063b6b73af59ab5`  
		Last Modified: Tue, 04 Jul 2023 15:36:55 GMT  
		Size: 12.5 MB (12455497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1e11a5919e5746092b2a288f71090ffdb0d3544b7b54c31ed0137e6d5d4735`  
		Last Modified: Tue, 04 Jul 2023 15:38:37 GMT  
		Size: 45.0 MB (45009079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80987dc89da28aa5ceec7a86ea74e13cee06ecd9304cf4c92d8f382c79eb4f2`  
		Last Modified: Tue, 04 Jul 2023 15:38:32 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de67c7824eef053da628456fe8aba244c4150024af9454dd4091763920d836c`  
		Last Modified: Wed, 05 Jul 2023 03:14:23 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f77f07e56c3d3019cd346deaeacbe572b15b26a924c19b6386877b47123a89e`  
		Last Modified: Tue, 11 Jul 2023 01:39:24 GMT  
		Size: 12.3 MB (12283700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2422cddd65b0ff63d783c999d005c42281720b8615f5872e1e8fdb32dd9981d9`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 455.1 KB (455052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b023f0d964d565a960e567dcaaa605fdff6da02b54971f4d0693506b481b8c`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28177f0763a75e5c940bb6a7919185effccd7cf14c0e350198b3aedbe1db789`  
		Last Modified: Tue, 11 Jul 2023 05:26:01 GMT  
		Size: 173.4 MB (173373450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc5b16765fdc498e3f3e0db1f6f5968716864f931b8490f2092985f2aad66e6`  
		Last Modified: Tue, 11 Jul 2023 05:27:47 GMT  
		Size: 307.3 MB (307261061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e05260decea8ae0b8e52961a6b822e7f61aa0d94e359d9bdfb0a8d1c12ab373`  
		Last Modified: Tue, 11 Jul 2023 05:27:33 GMT  
		Size: 2.3 MB (2343684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80db78e6c67fd96e8da400c8505c850ac34058465e92e7c08c2079a56c581eef`  
		Last Modified: Tue, 11 Jul 2023 05:27:32 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e13d3d8f1788f25950792ca1b21389742cb964f69af7853cd12c938239fa7c94`  
		Last Modified: Tue, 11 Jul 2023 05:27:33 GMT  
		Size: 2.3 KB (2311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ecfdbab47ad32f6ddf82bd2c97ac1e2786af57d2bfc2653639b91c3a1833a3`  
		Last Modified: Tue, 11 Jul 2023 05:27:32 GMT  
		Size: 6.0 KB (6020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0b9874cce7da8c08bc10f43d1a239ff6d3d1b18189a83d61bf566a352cba781`  
		Last Modified: Tue, 11 Jul 2023 05:27:32 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:14-postgres-tomcat`

```console
$ docker pull xwiki@sha256:32c79a7b00472757f10412ef3b239548c73e98a078012993d0d05d4c8ae24a90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:14-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:d01097f47bf6df2a0da617f68c5ebfd8ff7ea70fdfa268248e85245ecac517e4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.8 MB (589808935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df679394031ff1d5971a374c7d42e0b63e4495b07ba1a6cfc13bb75e004aa28`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:37:40 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:37:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:37:42 GMT
ADD file:140fb5108b4a2861b5718ad03b4a5174bba03589ea8d4c053e6a0b282f439ff3 in / 
# Wed, 28 Jun 2023 08:37:42 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:34:07 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:35:02 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 20:35:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 20:35:35 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 08:22:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 08:22:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 08:22:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 08:22:21 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 08:22:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:22:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:25:33 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 08:25:34 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 00:16:15 GMT
COPY dir:8ddeace4a16f09a0d97488e225c7b2e4a48c9a93484d24b46a09759f52800501 in /usr/local/tomcat 
# Tue, 11 Jul 2023 00:16:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 00:16:20 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 00:16:20 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 00:16:20 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 04:41:24 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 04:43:04 GMT
ENV XWIKI_VERSION=14.10.13
# Tue, 11 Jul 2023 04:43:04 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.13
# Tue, 11 Jul 2023 04:43:04 GMT
ENV XWIKI_DOWNLOAD_SHA256=5883ffdbc10865043778f3caa48fbca900129cf41c76ee6fdafba74769c928d4
# Tue, 11 Jul 2023 04:43:42 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 04:43:44 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Tue, 11 Jul 2023 04:43:44 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 04:43:44 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 04:43:44 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 04:43:44 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 04:43:44 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 04:43:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 04:43:45 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:9d19ee268e0d7bcf6716e6658ee1b0384a71d6f2f9aa1ae2085610cf7c7b316f`  
		Last Modified: Wed, 28 Jun 2023 11:50:41 GMT  
		Size: 30.4 MB (30431229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32db0ad82863deaedd2f9a365e52f595085778d28bd1e6f1d351107590cad806`  
		Last Modified: Tue, 04 Jul 2023 20:39:05 GMT  
		Size: 12.5 MB (12495341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01bb55fbcae928d7e6c08d6618580d2b27ce6e46083f861bbed1e01db41c20b`  
		Last Modified: Tue, 04 Jul 2023 20:41:01 GMT  
		Size: 46.7 MB (46666353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297c6e3f57ee032a3cc5f0fd28b52687129e7a1e6485aea12aff08cb6620071e`  
		Last Modified: Tue, 04 Jul 2023 20:40:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15b01f5ab5b71b356d93dff08f5037af8e8a03b4657f1fd303052261161ebd8`  
		Last Modified: Wed, 05 Jul 2023 08:37:14 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c6051a2b9ffe906ea99b555033966c877468da73cd19fd793c86099d0af531`  
		Last Modified: Tue, 11 Jul 2023 00:38:45 GMT  
		Size: 12.3 MB (12274167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34aaed1f6a3460fc256e262b462c1180ccef1b0665ffd50f900d1ef9c19f1d24`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 454.7 KB (454674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b809bf54ada009dfd91afa6ad239f7a791807f2928941b7f969493ec38246be`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bd305e7867896df13faced03525a0f25bf1ac1b2a2c93e60382cdfd41c08e16`  
		Last Modified: Tue, 11 Jul 2023 04:45:43 GMT  
		Size: 179.3 MB (179276407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:241d47b2e9b47cfbb131cde5eef64788e51d1adc745cd086b858dcce53744f96`  
		Last Modified: Tue, 11 Jul 2023 04:47:17 GMT  
		Size: 307.3 MB (307261147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f4659e18fff023a31986cddf337f7070ad540e3f2f5d788844d96b7afe3e09a`  
		Last Modified: Tue, 11 Jul 2023 04:47:02 GMT  
		Size: 936.9 KB (936850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e59501fb2b56042afce97a149bbda1ccf3a5051fd5a37b1ea5ade709d470fbf`  
		Last Modified: Tue, 11 Jul 2023 04:47:01 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f06d08f1ecba9ed57618eb230d5e981c069e02d8828c2b1613c9b5a2183cdb`  
		Last Modified: Tue, 11 Jul 2023 04:47:01 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27996d6a7bfe148d65a59be70b8a3358db5db63098c6efb311675b3d3e686aef`  
		Last Modified: Tue, 11 Jul 2023 04:47:01 GMT  
		Size: 6.0 KB (6015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5d4d60c04deaa508f3eb56cb4e847396e6df7158d261b34d3898ef54f81f526`  
		Last Modified: Tue, 11 Jul 2023 04:47:02 GMT  
		Size: 2.5 KB (2500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:14-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:966dfa46c0b58952823d9211ae493ea913edb22afe1aea49b60731e88ec9946b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.1 MB (581118361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f50afd98b0124061cd1380a5284513a88143aa86ccd826878235f8e45a5cc684`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:42:48 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:42:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:42:50 GMT
ADD file:262490f82459c14632f5c9a6d6a5cf6c07b4f307e8fd380fa764662cda46e88f in / 
# Wed, 28 Jun 2023 08:42:50 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:59 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 15:33:41 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 15:34:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 15:34:08 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 02:55:59 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 02:55:59 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 02:55:59 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 02:55:59 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 02:56:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 02:56:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 03:00:51 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 03:00:51 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 01:18:24 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 01:18:25 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 01:18:25 GMT
COPY dir:1743191a9534b9e7d795d3bf9ad18535d99e75967877447e17d7b63574d878d5 in /usr/local/tomcat 
# Tue, 11 Jul 2023 01:18:28 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 01:18:29 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 01:18:29 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 01:18:29 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 05:22:36 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 05:24:28 GMT
ENV XWIKI_VERSION=14.10.13
# Tue, 11 Jul 2023 05:24:28 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.13
# Tue, 11 Jul 2023 05:24:28 GMT
ENV XWIKI_DOWNLOAD_SHA256=5883ffdbc10865043778f3caa48fbca900129cf41c76ee6fdafba74769c928d4
# Tue, 11 Jul 2023 05:25:08 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 05:25:11 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Tue, 11 Jul 2023 05:25:11 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 05:25:11 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 05:25:11 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 05:25:11 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 05:25:11 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 05:25:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 05:25:11 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:ac34a2e0269ced3acc355be706239ee0f3f1e73a035c40dd2fac74827164ee53`  
		Last Modified: Wed, 28 Jun 2023 23:23:40 GMT  
		Size: 28.4 MB (28391011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d9df805749ad7c4605f0d49a64da6a6173ab190ec361dc2063b6b73af59ab5`  
		Last Modified: Tue, 04 Jul 2023 15:36:55 GMT  
		Size: 12.5 MB (12455497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1e11a5919e5746092b2a288f71090ffdb0d3544b7b54c31ed0137e6d5d4735`  
		Last Modified: Tue, 04 Jul 2023 15:38:37 GMT  
		Size: 45.0 MB (45009079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80987dc89da28aa5ceec7a86ea74e13cee06ecd9304cf4c92d8f382c79eb4f2`  
		Last Modified: Tue, 04 Jul 2023 15:38:32 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de67c7824eef053da628456fe8aba244c4150024af9454dd4091763920d836c`  
		Last Modified: Wed, 05 Jul 2023 03:14:23 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f77f07e56c3d3019cd346deaeacbe572b15b26a924c19b6386877b47123a89e`  
		Last Modified: Tue, 11 Jul 2023 01:39:24 GMT  
		Size: 12.3 MB (12283700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2422cddd65b0ff63d783c999d005c42281720b8615f5872e1e8fdb32dd9981d9`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 455.1 KB (455052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b023f0d964d565a960e567dcaaa605fdff6da02b54971f4d0693506b481b8c`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:968d46d099e01403854799f31b6235698a474c27fd58b0172b1eb3889cd5067f`  
		Last Modified: Tue, 11 Jul 2023 05:26:50 GMT  
		Size: 174.3 MB (174313369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58c2e2d1a49c77dd7a2b5e47670a35d29aca6a19183b43226d929ab037e2cf4a`  
		Last Modified: Tue, 11 Jul 2023 05:28:26 GMT  
		Size: 307.3 MB (307261017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48ff25a83276ff7bee5e0cc9402d6b809cee66bd4e22515f9e4ebf33a5f98d54`  
		Last Modified: Tue, 11 Jul 2023 05:28:12 GMT  
		Size: 936.9 KB (936850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a430a5f61ae1c957b6abf407c502bbac7994125fec841c264e73b3570ca318b`  
		Last Modified: Tue, 11 Jul 2023 05:28:12 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1a1106197e50baaa0b1e4612ce7252b217213ebdc52808529790aec8db034d`  
		Last Modified: Tue, 11 Jul 2023 05:28:12 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84d0854ce2eb5e1ce140a35ba96b4870e229a0bcc691cac48550a44dafbe83d1`  
		Last Modified: Tue, 11 Jul 2023 05:28:12 GMT  
		Size: 6.0 KB (6019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b30724798e976582c41b18d0c093767d1a9df69f9a34b9d57bbf90c21634feff`  
		Last Modified: Tue, 11 Jul 2023 05:28:12 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:14.10`

```console
$ docker pull xwiki@sha256:d684b69a373a2cef6fa2a32d55c3e87eed6a6f36cfac5320606e88204e88186a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:14.10` - linux; amd64

```console
$ docker pull xwiki@sha256:ede13785f63dcaf8042ae3ad55c0c8fa410a3832504cdcf66916035506feebc9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.3 MB (590275216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0cdff4d327d68685f5dd8da61be21269df316c760ef6487e0aa642ec059b882`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:37:40 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:37:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:37:42 GMT
ADD file:140fb5108b4a2861b5718ad03b4a5174bba03589ea8d4c053e6a0b282f439ff3 in / 
# Wed, 28 Jun 2023 08:37:42 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:34:07 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:35:02 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 20:35:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 20:35:35 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 08:22:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 08:22:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 08:22:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 08:22:21 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 08:22:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:22:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:25:33 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 08:25:34 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 00:16:15 GMT
COPY dir:8ddeace4a16f09a0d97488e225c7b2e4a48c9a93484d24b46a09759f52800501 in /usr/local/tomcat 
# Tue, 11 Jul 2023 00:16:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 00:16:20 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 00:16:20 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 00:16:20 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 04:40:02 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 04:42:15 GMT
ENV XWIKI_VERSION=14.10.13
# Tue, 11 Jul 2023 04:42:15 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.13
# Tue, 11 Jul 2023 04:42:15 GMT
ENV XWIKI_DOWNLOAD_SHA256=5883ffdbc10865043778f3caa48fbca900129cf41c76ee6fdafba74769c928d4
# Tue, 11 Jul 2023 04:42:54 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 04:42:54 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Tue, 11 Jul 2023 04:42:55 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Tue, 11 Jul 2023 04:42:55 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Tue, 11 Jul 2023 04:42:55 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 04:42:55 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 04:42:56 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Tue, 11 Jul 2023 04:42:56 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 04:42:56 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 04:42:56 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 04:42:56 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 04:42:56 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 04:42:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 04:42:57 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:9d19ee268e0d7bcf6716e6658ee1b0384a71d6f2f9aa1ae2085610cf7c7b316f`  
		Last Modified: Wed, 28 Jun 2023 11:50:41 GMT  
		Size: 30.4 MB (30431229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32db0ad82863deaedd2f9a365e52f595085778d28bd1e6f1d351107590cad806`  
		Last Modified: Tue, 04 Jul 2023 20:39:05 GMT  
		Size: 12.5 MB (12495341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01bb55fbcae928d7e6c08d6618580d2b27ce6e46083f861bbed1e01db41c20b`  
		Last Modified: Tue, 04 Jul 2023 20:41:01 GMT  
		Size: 46.7 MB (46666353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297c6e3f57ee032a3cc5f0fd28b52687129e7a1e6485aea12aff08cb6620071e`  
		Last Modified: Tue, 04 Jul 2023 20:40:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15b01f5ab5b71b356d93dff08f5037af8e8a03b4657f1fd303052261161ebd8`  
		Last Modified: Wed, 05 Jul 2023 08:37:14 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c6051a2b9ffe906ea99b555033966c877468da73cd19fd793c86099d0af531`  
		Last Modified: Tue, 11 Jul 2023 00:38:45 GMT  
		Size: 12.3 MB (12274167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34aaed1f6a3460fc256e262b462c1180ccef1b0665ffd50f900d1ef9c19f1d24`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 454.7 KB (454674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b809bf54ada009dfd91afa6ad239f7a791807f2928941b7f969493ec38246be`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877cc60516baaeb7846bba5d5de9e491d0406cd2f43959d7d4e104d89df5e228`  
		Last Modified: Tue, 11 Jul 2023 04:44:49 GMT  
		Size: 178.3 MB (178335971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d83ab8708da1a9ab9fb6a48ac52687e3488789fccbd4a07ced23e73be97d1b`  
		Last Modified: Tue, 11 Jul 2023 04:46:37 GMT  
		Size: 307.3 MB (307261194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:663bd82ddfd62b4cf39556e967220c977dcdbb37a1fd053c779fd0baa6898818`  
		Last Modified: Tue, 11 Jul 2023 04:46:21 GMT  
		Size: 2.3 MB (2343668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed5bec13f08d98c63e3c81fb0a45f8734746d82b5504310835cac9e7a8e18dec`  
		Last Modified: Tue, 11 Jul 2023 04:46:21 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dfccb5d359b6e3ae2ddf7257f81d0e9b794f602ab4e3f3196c372af5543d1ca`  
		Last Modified: Tue, 11 Jul 2023 04:46:21 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac17a1dc4319814e728392d0b0b3ad40083d48efeaec075e52bdaef3545341d0`  
		Last Modified: Tue, 11 Jul 2023 04:46:21 GMT  
		Size: 6.0 KB (6015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57f2437b546ab6322d8db9cf14928c907568c9728574599d16ea306286ab824c`  
		Last Modified: Tue, 11 Jul 2023 04:46:21 GMT  
		Size: 2.5 KB (2498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:14.10` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:2c70da3ff6aad987960017b1f402de397c9e9a3b3f806a125702c26c14a1bfb8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.6 MB (581585177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a5e15a24190e32ccad68b6a75aa965123ee8a3fd0edd724d8cbaecbcf34acf6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:42:48 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:42:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:42:50 GMT
ADD file:262490f82459c14632f5c9a6d6a5cf6c07b4f307e8fd380fa764662cda46e88f in / 
# Wed, 28 Jun 2023 08:42:50 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:59 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 15:33:41 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 15:34:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 15:34:08 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 02:55:59 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 02:55:59 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 02:55:59 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 02:55:59 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 02:56:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 02:56:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 03:00:51 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 03:00:51 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 01:18:24 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 01:18:25 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 01:18:25 GMT
COPY dir:1743191a9534b9e7d795d3bf9ad18535d99e75967877447e17d7b63574d878d5 in /usr/local/tomcat 
# Tue, 11 Jul 2023 01:18:28 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 01:18:29 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 01:18:29 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 01:18:29 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 05:21:20 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 05:23:40 GMT
ENV XWIKI_VERSION=14.10.13
# Tue, 11 Jul 2023 05:23:40 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.13
# Tue, 11 Jul 2023 05:23:40 GMT
ENV XWIKI_DOWNLOAD_SHA256=5883ffdbc10865043778f3caa48fbca900129cf41c76ee6fdafba74769c928d4
# Tue, 11 Jul 2023 05:24:20 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 05:24:23 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Tue, 11 Jul 2023 05:24:23 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Tue, 11 Jul 2023 05:24:23 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Tue, 11 Jul 2023 05:24:23 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 05:24:23 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 05:24:24 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Tue, 11 Jul 2023 05:24:24 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 05:24:24 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 05:24:25 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 05:24:25 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 05:24:25 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 05:24:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 05:24:25 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:ac34a2e0269ced3acc355be706239ee0f3f1e73a035c40dd2fac74827164ee53`  
		Last Modified: Wed, 28 Jun 2023 23:23:40 GMT  
		Size: 28.4 MB (28391011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d9df805749ad7c4605f0d49a64da6a6173ab190ec361dc2063b6b73af59ab5`  
		Last Modified: Tue, 04 Jul 2023 15:36:55 GMT  
		Size: 12.5 MB (12455497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1e11a5919e5746092b2a288f71090ffdb0d3544b7b54c31ed0137e6d5d4735`  
		Last Modified: Tue, 04 Jul 2023 15:38:37 GMT  
		Size: 45.0 MB (45009079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80987dc89da28aa5ceec7a86ea74e13cee06ecd9304cf4c92d8f382c79eb4f2`  
		Last Modified: Tue, 04 Jul 2023 15:38:32 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de67c7824eef053da628456fe8aba244c4150024af9454dd4091763920d836c`  
		Last Modified: Wed, 05 Jul 2023 03:14:23 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f77f07e56c3d3019cd346deaeacbe572b15b26a924c19b6386877b47123a89e`  
		Last Modified: Tue, 11 Jul 2023 01:39:24 GMT  
		Size: 12.3 MB (12283700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2422cddd65b0ff63d783c999d005c42281720b8615f5872e1e8fdb32dd9981d9`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 455.1 KB (455052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b023f0d964d565a960e567dcaaa605fdff6da02b54971f4d0693506b481b8c`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28177f0763a75e5c940bb6a7919185effccd7cf14c0e350198b3aedbe1db789`  
		Last Modified: Tue, 11 Jul 2023 05:26:01 GMT  
		Size: 173.4 MB (173373450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc5b16765fdc498e3f3e0db1f6f5968716864f931b8490f2092985f2aad66e6`  
		Last Modified: Tue, 11 Jul 2023 05:27:47 GMT  
		Size: 307.3 MB (307261061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e05260decea8ae0b8e52961a6b822e7f61aa0d94e359d9bdfb0a8d1c12ab373`  
		Last Modified: Tue, 11 Jul 2023 05:27:33 GMT  
		Size: 2.3 MB (2343684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80db78e6c67fd96e8da400c8505c850ac34058465e92e7c08c2079a56c581eef`  
		Last Modified: Tue, 11 Jul 2023 05:27:32 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e13d3d8f1788f25950792ca1b21389742cb964f69af7853cd12c938239fa7c94`  
		Last Modified: Tue, 11 Jul 2023 05:27:33 GMT  
		Size: 2.3 KB (2311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ecfdbab47ad32f6ddf82bd2c97ac1e2786af57d2bfc2653639b91c3a1833a3`  
		Last Modified: Tue, 11 Jul 2023 05:27:32 GMT  
		Size: 6.0 KB (6020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0b9874cce7da8c08bc10f43d1a239ff6d3d1b18189a83d61bf566a352cba781`  
		Last Modified: Tue, 11 Jul 2023 05:27:32 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:14.10-mariadb-tomcat`

```console
$ docker pull xwiki@sha256:4f0cfbbcc4d2a7ab73eac160f70b796dbe864d041ce38174443170e66be4e82c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:14.10-mariadb-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:2457ece1ecfc0fdb7b33b40d99e1cc0e647b34427eb7d3adf0321d7035832bd7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **588.5 MB (588526114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23dabbcf30b0cba2e6e27db54197aadc63470a751d0cf652f95c6ffc4dc48bc5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:37:40 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:37:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:37:42 GMT
ADD file:140fb5108b4a2861b5718ad03b4a5174bba03589ea8d4c053e6a0b282f439ff3 in / 
# Wed, 28 Jun 2023 08:37:42 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:34:07 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:35:02 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 20:35:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 20:35:35 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 08:22:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 08:22:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 08:22:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 08:22:21 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 08:22:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:22:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:25:33 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 08:25:34 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 00:16:15 GMT
COPY dir:8ddeace4a16f09a0d97488e225c7b2e4a48c9a93484d24b46a09759f52800501 in /usr/local/tomcat 
# Tue, 11 Jul 2023 00:16:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 00:16:20 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 00:16:20 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 00:16:20 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 04:40:02 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 04:42:15 GMT
ENV XWIKI_VERSION=14.10.13
# Tue, 11 Jul 2023 04:42:15 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.13
# Tue, 11 Jul 2023 04:42:15 GMT
ENV XWIKI_DOWNLOAD_SHA256=5883ffdbc10865043778f3caa48fbca900129cf41c76ee6fdafba74769c928d4
# Tue, 11 Jul 2023 04:42:54 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 04:43:53 GMT
ENV MARIADB_JDBC_VERSION=3.1.4
# Tue, 11 Jul 2023 04:43:53 GMT
ENV MARIADB_JDBC_SHA256=eb88b5d727d82e25117e2b6fabcec1daf734633b0a576456c73215884c189ad4
# Tue, 11 Jul 2023 04:43:53 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.1.4
# Tue, 11 Jul 2023 04:43:53 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.1.4.jar
# Tue, 11 Jul 2023 04:43:53 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.1.4.jar
# Tue, 11 Jul 2023 04:43:54 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Tue, 11 Jul 2023 04:43:54 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 04:43:54 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 04:43:55 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 04:43:55 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 04:43:55 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 04:43:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 04:43:55 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:9d19ee268e0d7bcf6716e6658ee1b0384a71d6f2f9aa1ae2085610cf7c7b316f`  
		Last Modified: Wed, 28 Jun 2023 11:50:41 GMT  
		Size: 30.4 MB (30431229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32db0ad82863deaedd2f9a365e52f595085778d28bd1e6f1d351107590cad806`  
		Last Modified: Tue, 04 Jul 2023 20:39:05 GMT  
		Size: 12.5 MB (12495341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01bb55fbcae928d7e6c08d6618580d2b27ce6e46083f861bbed1e01db41c20b`  
		Last Modified: Tue, 04 Jul 2023 20:41:01 GMT  
		Size: 46.7 MB (46666353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297c6e3f57ee032a3cc5f0fd28b52687129e7a1e6485aea12aff08cb6620071e`  
		Last Modified: Tue, 04 Jul 2023 20:40:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15b01f5ab5b71b356d93dff08f5037af8e8a03b4657f1fd303052261161ebd8`  
		Last Modified: Wed, 05 Jul 2023 08:37:14 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c6051a2b9ffe906ea99b555033966c877468da73cd19fd793c86099d0af531`  
		Last Modified: Tue, 11 Jul 2023 00:38:45 GMT  
		Size: 12.3 MB (12274167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34aaed1f6a3460fc256e262b462c1180ccef1b0665ffd50f900d1ef9c19f1d24`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 454.7 KB (454674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b809bf54ada009dfd91afa6ad239f7a791807f2928941b7f969493ec38246be`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877cc60516baaeb7846bba5d5de9e491d0406cd2f43959d7d4e104d89df5e228`  
		Last Modified: Tue, 11 Jul 2023 04:44:49 GMT  
		Size: 178.3 MB (178335971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d83ab8708da1a9ab9fb6a48ac52687e3488789fccbd4a07ced23e73be97d1b`  
		Last Modified: Tue, 11 Jul 2023 04:46:37 GMT  
		Size: 307.3 MB (307261194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e875fea8a2c98d9a649ede02e5cde89adc140d705cd90f987da3c01c0e0e91ba`  
		Last Modified: Tue, 11 Jul 2023 04:47:34 GMT  
		Size: 594.6 KB (594551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03c934df3cbcee083ccb0b050eb79b8a33e576b12a5d653cf3779efd73ae0886`  
		Last Modified: Tue, 11 Jul 2023 04:47:34 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:169d82fe476f2ba0c25f369977bcad3dbefc51aecdd90854d3d5bd162ffca191`  
		Last Modified: Tue, 11 Jul 2023 04:47:34 GMT  
		Size: 2.3 KB (2309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2bc34d1fe1755d4b6c92a1f18f895229ebbd1c4c33b8d9870ad601f460c6e30`  
		Last Modified: Tue, 11 Jul 2023 04:47:34 GMT  
		Size: 6.0 KB (6017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dc85b4209f7c5902eaddc9237e35ff851834dbe9a46b12cda8f7c6bd37e98f0`  
		Last Modified: Tue, 11 Jul 2023 04:47:33 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:14.10-mariadb-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:f2d58b0e807535f9a89d2aefdb36e0ed212696276c598c6ac7a44ae4a463571e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.8 MB (579836046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4827d8602436ba34af88ff0bccf958bc03dbf862b5011c12c3799c90dba3626a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:42:48 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:42:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:42:50 GMT
ADD file:262490f82459c14632f5c9a6d6a5cf6c07b4f307e8fd380fa764662cda46e88f in / 
# Wed, 28 Jun 2023 08:42:50 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:59 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 15:33:41 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 15:34:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 15:34:08 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 02:55:59 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 02:55:59 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 02:55:59 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 02:55:59 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 02:56:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 02:56:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 03:00:51 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 03:00:51 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 01:18:24 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 01:18:25 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 01:18:25 GMT
COPY dir:1743191a9534b9e7d795d3bf9ad18535d99e75967877447e17d7b63574d878d5 in /usr/local/tomcat 
# Tue, 11 Jul 2023 01:18:28 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 01:18:29 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 01:18:29 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 01:18:29 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 05:21:20 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 05:23:40 GMT
ENV XWIKI_VERSION=14.10.13
# Tue, 11 Jul 2023 05:23:40 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.13
# Tue, 11 Jul 2023 05:23:40 GMT
ENV XWIKI_DOWNLOAD_SHA256=5883ffdbc10865043778f3caa48fbca900129cf41c76ee6fdafba74769c928d4
# Tue, 11 Jul 2023 05:24:20 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 05:25:16 GMT
ENV MARIADB_JDBC_VERSION=3.1.4
# Tue, 11 Jul 2023 05:25:16 GMT
ENV MARIADB_JDBC_SHA256=eb88b5d727d82e25117e2b6fabcec1daf734633b0a576456c73215884c189ad4
# Tue, 11 Jul 2023 05:25:16 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.1.4
# Tue, 11 Jul 2023 05:25:16 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.1.4.jar
# Tue, 11 Jul 2023 05:25:17 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.1.4.jar
# Tue, 11 Jul 2023 05:25:17 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Tue, 11 Jul 2023 05:25:17 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 05:25:17 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 05:25:18 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 05:25:18 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 05:25:18 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 05:25:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 05:25:18 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:ac34a2e0269ced3acc355be706239ee0f3f1e73a035c40dd2fac74827164ee53`  
		Last Modified: Wed, 28 Jun 2023 23:23:40 GMT  
		Size: 28.4 MB (28391011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d9df805749ad7c4605f0d49a64da6a6173ab190ec361dc2063b6b73af59ab5`  
		Last Modified: Tue, 04 Jul 2023 15:36:55 GMT  
		Size: 12.5 MB (12455497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1e11a5919e5746092b2a288f71090ffdb0d3544b7b54c31ed0137e6d5d4735`  
		Last Modified: Tue, 04 Jul 2023 15:38:37 GMT  
		Size: 45.0 MB (45009079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80987dc89da28aa5ceec7a86ea74e13cee06ecd9304cf4c92d8f382c79eb4f2`  
		Last Modified: Tue, 04 Jul 2023 15:38:32 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de67c7824eef053da628456fe8aba244c4150024af9454dd4091763920d836c`  
		Last Modified: Wed, 05 Jul 2023 03:14:23 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f77f07e56c3d3019cd346deaeacbe572b15b26a924c19b6386877b47123a89e`  
		Last Modified: Tue, 11 Jul 2023 01:39:24 GMT  
		Size: 12.3 MB (12283700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2422cddd65b0ff63d783c999d005c42281720b8615f5872e1e8fdb32dd9981d9`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 455.1 KB (455052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b023f0d964d565a960e567dcaaa605fdff6da02b54971f4d0693506b481b8c`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28177f0763a75e5c940bb6a7919185effccd7cf14c0e350198b3aedbe1db789`  
		Last Modified: Tue, 11 Jul 2023 05:26:01 GMT  
		Size: 173.4 MB (173373450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc5b16765fdc498e3f3e0db1f6f5968716864f931b8490f2092985f2aad66e6`  
		Last Modified: Tue, 11 Jul 2023 05:27:47 GMT  
		Size: 307.3 MB (307261061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cde3b2925cca0eaeca051a9d34fc8559173eb81198be6edb87ef675ddbd104c`  
		Last Modified: Tue, 11 Jul 2023 05:28:44 GMT  
		Size: 594.6 KB (594553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a572ecd6de904372e67871760ea39b4c45f94b03c1bd47a6ee27a1151f44f25`  
		Last Modified: Tue, 11 Jul 2023 05:28:43 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48dc7acaf3762507fe63c6d484d73da83682cfc993ce96feccb9b0cb2bea8895`  
		Last Modified: Tue, 11 Jul 2023 05:28:43 GMT  
		Size: 2.3 KB (2314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd91b38c50762886b672122ce7698e839324aa39970db075d8fa1a46ae5d6fe5`  
		Last Modified: Tue, 11 Jul 2023 05:28:43 GMT  
		Size: 6.0 KB (6018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:536a460fc0ee741e1de6915eb0f7533df412ab1b9c51ac2f7686ca966abef1fc`  
		Last Modified: Tue, 11 Jul 2023 05:28:43 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:14.10-mysql-tomcat`

```console
$ docker pull xwiki@sha256:d684b69a373a2cef6fa2a32d55c3e87eed6a6f36cfac5320606e88204e88186a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:14.10-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:ede13785f63dcaf8042ae3ad55c0c8fa410a3832504cdcf66916035506feebc9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.3 MB (590275216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0cdff4d327d68685f5dd8da61be21269df316c760ef6487e0aa642ec059b882`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:37:40 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:37:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:37:42 GMT
ADD file:140fb5108b4a2861b5718ad03b4a5174bba03589ea8d4c053e6a0b282f439ff3 in / 
# Wed, 28 Jun 2023 08:37:42 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:34:07 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:35:02 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 20:35:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 20:35:35 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 08:22:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 08:22:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 08:22:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 08:22:21 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 08:22:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:22:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:25:33 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 08:25:34 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 00:16:15 GMT
COPY dir:8ddeace4a16f09a0d97488e225c7b2e4a48c9a93484d24b46a09759f52800501 in /usr/local/tomcat 
# Tue, 11 Jul 2023 00:16:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 00:16:20 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 00:16:20 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 00:16:20 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 04:40:02 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 04:42:15 GMT
ENV XWIKI_VERSION=14.10.13
# Tue, 11 Jul 2023 04:42:15 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.13
# Tue, 11 Jul 2023 04:42:15 GMT
ENV XWIKI_DOWNLOAD_SHA256=5883ffdbc10865043778f3caa48fbca900129cf41c76ee6fdafba74769c928d4
# Tue, 11 Jul 2023 04:42:54 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 04:42:54 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Tue, 11 Jul 2023 04:42:55 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Tue, 11 Jul 2023 04:42:55 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Tue, 11 Jul 2023 04:42:55 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 04:42:55 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 04:42:56 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Tue, 11 Jul 2023 04:42:56 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 04:42:56 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 04:42:56 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 04:42:56 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 04:42:56 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 04:42:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 04:42:57 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:9d19ee268e0d7bcf6716e6658ee1b0384a71d6f2f9aa1ae2085610cf7c7b316f`  
		Last Modified: Wed, 28 Jun 2023 11:50:41 GMT  
		Size: 30.4 MB (30431229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32db0ad82863deaedd2f9a365e52f595085778d28bd1e6f1d351107590cad806`  
		Last Modified: Tue, 04 Jul 2023 20:39:05 GMT  
		Size: 12.5 MB (12495341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01bb55fbcae928d7e6c08d6618580d2b27ce6e46083f861bbed1e01db41c20b`  
		Last Modified: Tue, 04 Jul 2023 20:41:01 GMT  
		Size: 46.7 MB (46666353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297c6e3f57ee032a3cc5f0fd28b52687129e7a1e6485aea12aff08cb6620071e`  
		Last Modified: Tue, 04 Jul 2023 20:40:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15b01f5ab5b71b356d93dff08f5037af8e8a03b4657f1fd303052261161ebd8`  
		Last Modified: Wed, 05 Jul 2023 08:37:14 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c6051a2b9ffe906ea99b555033966c877468da73cd19fd793c86099d0af531`  
		Last Modified: Tue, 11 Jul 2023 00:38:45 GMT  
		Size: 12.3 MB (12274167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34aaed1f6a3460fc256e262b462c1180ccef1b0665ffd50f900d1ef9c19f1d24`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 454.7 KB (454674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b809bf54ada009dfd91afa6ad239f7a791807f2928941b7f969493ec38246be`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877cc60516baaeb7846bba5d5de9e491d0406cd2f43959d7d4e104d89df5e228`  
		Last Modified: Tue, 11 Jul 2023 04:44:49 GMT  
		Size: 178.3 MB (178335971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d83ab8708da1a9ab9fb6a48ac52687e3488789fccbd4a07ced23e73be97d1b`  
		Last Modified: Tue, 11 Jul 2023 04:46:37 GMT  
		Size: 307.3 MB (307261194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:663bd82ddfd62b4cf39556e967220c977dcdbb37a1fd053c779fd0baa6898818`  
		Last Modified: Tue, 11 Jul 2023 04:46:21 GMT  
		Size: 2.3 MB (2343668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed5bec13f08d98c63e3c81fb0a45f8734746d82b5504310835cac9e7a8e18dec`  
		Last Modified: Tue, 11 Jul 2023 04:46:21 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dfccb5d359b6e3ae2ddf7257f81d0e9b794f602ab4e3f3196c372af5543d1ca`  
		Last Modified: Tue, 11 Jul 2023 04:46:21 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac17a1dc4319814e728392d0b0b3ad40083d48efeaec075e52bdaef3545341d0`  
		Last Modified: Tue, 11 Jul 2023 04:46:21 GMT  
		Size: 6.0 KB (6015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57f2437b546ab6322d8db9cf14928c907568c9728574599d16ea306286ab824c`  
		Last Modified: Tue, 11 Jul 2023 04:46:21 GMT  
		Size: 2.5 KB (2498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:14.10-mysql-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:2c70da3ff6aad987960017b1f402de397c9e9a3b3f806a125702c26c14a1bfb8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.6 MB (581585177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a5e15a24190e32ccad68b6a75aa965123ee8a3fd0edd724d8cbaecbcf34acf6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:42:48 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:42:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:42:50 GMT
ADD file:262490f82459c14632f5c9a6d6a5cf6c07b4f307e8fd380fa764662cda46e88f in / 
# Wed, 28 Jun 2023 08:42:50 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:59 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 15:33:41 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 15:34:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 15:34:08 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 02:55:59 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 02:55:59 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 02:55:59 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 02:55:59 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 02:56:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 02:56:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 03:00:51 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 03:00:51 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 01:18:24 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 01:18:25 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 01:18:25 GMT
COPY dir:1743191a9534b9e7d795d3bf9ad18535d99e75967877447e17d7b63574d878d5 in /usr/local/tomcat 
# Tue, 11 Jul 2023 01:18:28 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 01:18:29 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 01:18:29 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 01:18:29 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 05:21:20 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 05:23:40 GMT
ENV XWIKI_VERSION=14.10.13
# Tue, 11 Jul 2023 05:23:40 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.13
# Tue, 11 Jul 2023 05:23:40 GMT
ENV XWIKI_DOWNLOAD_SHA256=5883ffdbc10865043778f3caa48fbca900129cf41c76ee6fdafba74769c928d4
# Tue, 11 Jul 2023 05:24:20 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 05:24:23 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Tue, 11 Jul 2023 05:24:23 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Tue, 11 Jul 2023 05:24:23 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Tue, 11 Jul 2023 05:24:23 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 05:24:23 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 05:24:24 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Tue, 11 Jul 2023 05:24:24 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 05:24:24 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 05:24:25 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 05:24:25 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 05:24:25 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 05:24:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 05:24:25 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:ac34a2e0269ced3acc355be706239ee0f3f1e73a035c40dd2fac74827164ee53`  
		Last Modified: Wed, 28 Jun 2023 23:23:40 GMT  
		Size: 28.4 MB (28391011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d9df805749ad7c4605f0d49a64da6a6173ab190ec361dc2063b6b73af59ab5`  
		Last Modified: Tue, 04 Jul 2023 15:36:55 GMT  
		Size: 12.5 MB (12455497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1e11a5919e5746092b2a288f71090ffdb0d3544b7b54c31ed0137e6d5d4735`  
		Last Modified: Tue, 04 Jul 2023 15:38:37 GMT  
		Size: 45.0 MB (45009079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80987dc89da28aa5ceec7a86ea74e13cee06ecd9304cf4c92d8f382c79eb4f2`  
		Last Modified: Tue, 04 Jul 2023 15:38:32 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de67c7824eef053da628456fe8aba244c4150024af9454dd4091763920d836c`  
		Last Modified: Wed, 05 Jul 2023 03:14:23 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f77f07e56c3d3019cd346deaeacbe572b15b26a924c19b6386877b47123a89e`  
		Last Modified: Tue, 11 Jul 2023 01:39:24 GMT  
		Size: 12.3 MB (12283700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2422cddd65b0ff63d783c999d005c42281720b8615f5872e1e8fdb32dd9981d9`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 455.1 KB (455052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b023f0d964d565a960e567dcaaa605fdff6da02b54971f4d0693506b481b8c`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28177f0763a75e5c940bb6a7919185effccd7cf14c0e350198b3aedbe1db789`  
		Last Modified: Tue, 11 Jul 2023 05:26:01 GMT  
		Size: 173.4 MB (173373450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc5b16765fdc498e3f3e0db1f6f5968716864f931b8490f2092985f2aad66e6`  
		Last Modified: Tue, 11 Jul 2023 05:27:47 GMT  
		Size: 307.3 MB (307261061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e05260decea8ae0b8e52961a6b822e7f61aa0d94e359d9bdfb0a8d1c12ab373`  
		Last Modified: Tue, 11 Jul 2023 05:27:33 GMT  
		Size: 2.3 MB (2343684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80db78e6c67fd96e8da400c8505c850ac34058465e92e7c08c2079a56c581eef`  
		Last Modified: Tue, 11 Jul 2023 05:27:32 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e13d3d8f1788f25950792ca1b21389742cb964f69af7853cd12c938239fa7c94`  
		Last Modified: Tue, 11 Jul 2023 05:27:33 GMT  
		Size: 2.3 KB (2311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ecfdbab47ad32f6ddf82bd2c97ac1e2786af57d2bfc2653639b91c3a1833a3`  
		Last Modified: Tue, 11 Jul 2023 05:27:32 GMT  
		Size: 6.0 KB (6020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0b9874cce7da8c08bc10f43d1a239ff6d3d1b18189a83d61bf566a352cba781`  
		Last Modified: Tue, 11 Jul 2023 05:27:32 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:14.10-postgres-tomcat`

```console
$ docker pull xwiki@sha256:32c79a7b00472757f10412ef3b239548c73e98a078012993d0d05d4c8ae24a90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:14.10-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:d01097f47bf6df2a0da617f68c5ebfd8ff7ea70fdfa268248e85245ecac517e4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.8 MB (589808935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df679394031ff1d5971a374c7d42e0b63e4495b07ba1a6cfc13bb75e004aa28`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:37:40 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:37:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:37:42 GMT
ADD file:140fb5108b4a2861b5718ad03b4a5174bba03589ea8d4c053e6a0b282f439ff3 in / 
# Wed, 28 Jun 2023 08:37:42 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:34:07 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:35:02 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 20:35:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 20:35:35 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 08:22:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 08:22:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 08:22:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 08:22:21 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 08:22:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:22:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:25:33 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 08:25:34 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 00:16:15 GMT
COPY dir:8ddeace4a16f09a0d97488e225c7b2e4a48c9a93484d24b46a09759f52800501 in /usr/local/tomcat 
# Tue, 11 Jul 2023 00:16:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 00:16:20 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 00:16:20 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 00:16:20 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 04:41:24 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 04:43:04 GMT
ENV XWIKI_VERSION=14.10.13
# Tue, 11 Jul 2023 04:43:04 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.13
# Tue, 11 Jul 2023 04:43:04 GMT
ENV XWIKI_DOWNLOAD_SHA256=5883ffdbc10865043778f3caa48fbca900129cf41c76ee6fdafba74769c928d4
# Tue, 11 Jul 2023 04:43:42 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 04:43:44 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Tue, 11 Jul 2023 04:43:44 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 04:43:44 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 04:43:44 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 04:43:44 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 04:43:44 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 04:43:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 04:43:45 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:9d19ee268e0d7bcf6716e6658ee1b0384a71d6f2f9aa1ae2085610cf7c7b316f`  
		Last Modified: Wed, 28 Jun 2023 11:50:41 GMT  
		Size: 30.4 MB (30431229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32db0ad82863deaedd2f9a365e52f595085778d28bd1e6f1d351107590cad806`  
		Last Modified: Tue, 04 Jul 2023 20:39:05 GMT  
		Size: 12.5 MB (12495341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01bb55fbcae928d7e6c08d6618580d2b27ce6e46083f861bbed1e01db41c20b`  
		Last Modified: Tue, 04 Jul 2023 20:41:01 GMT  
		Size: 46.7 MB (46666353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297c6e3f57ee032a3cc5f0fd28b52687129e7a1e6485aea12aff08cb6620071e`  
		Last Modified: Tue, 04 Jul 2023 20:40:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15b01f5ab5b71b356d93dff08f5037af8e8a03b4657f1fd303052261161ebd8`  
		Last Modified: Wed, 05 Jul 2023 08:37:14 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c6051a2b9ffe906ea99b555033966c877468da73cd19fd793c86099d0af531`  
		Last Modified: Tue, 11 Jul 2023 00:38:45 GMT  
		Size: 12.3 MB (12274167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34aaed1f6a3460fc256e262b462c1180ccef1b0665ffd50f900d1ef9c19f1d24`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 454.7 KB (454674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b809bf54ada009dfd91afa6ad239f7a791807f2928941b7f969493ec38246be`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bd305e7867896df13faced03525a0f25bf1ac1b2a2c93e60382cdfd41c08e16`  
		Last Modified: Tue, 11 Jul 2023 04:45:43 GMT  
		Size: 179.3 MB (179276407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:241d47b2e9b47cfbb131cde5eef64788e51d1adc745cd086b858dcce53744f96`  
		Last Modified: Tue, 11 Jul 2023 04:47:17 GMT  
		Size: 307.3 MB (307261147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f4659e18fff023a31986cddf337f7070ad540e3f2f5d788844d96b7afe3e09a`  
		Last Modified: Tue, 11 Jul 2023 04:47:02 GMT  
		Size: 936.9 KB (936850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e59501fb2b56042afce97a149bbda1ccf3a5051fd5a37b1ea5ade709d470fbf`  
		Last Modified: Tue, 11 Jul 2023 04:47:01 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f06d08f1ecba9ed57618eb230d5e981c069e02d8828c2b1613c9b5a2183cdb`  
		Last Modified: Tue, 11 Jul 2023 04:47:01 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27996d6a7bfe148d65a59be70b8a3358db5db63098c6efb311675b3d3e686aef`  
		Last Modified: Tue, 11 Jul 2023 04:47:01 GMT  
		Size: 6.0 KB (6015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5d4d60c04deaa508f3eb56cb4e847396e6df7158d261b34d3898ef54f81f526`  
		Last Modified: Tue, 11 Jul 2023 04:47:02 GMT  
		Size: 2.5 KB (2500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:14.10-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:966dfa46c0b58952823d9211ae493ea913edb22afe1aea49b60731e88ec9946b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.1 MB (581118361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f50afd98b0124061cd1380a5284513a88143aa86ccd826878235f8e45a5cc684`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:42:48 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:42:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:42:50 GMT
ADD file:262490f82459c14632f5c9a6d6a5cf6c07b4f307e8fd380fa764662cda46e88f in / 
# Wed, 28 Jun 2023 08:42:50 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:59 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 15:33:41 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 15:34:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 15:34:08 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 02:55:59 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 02:55:59 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 02:55:59 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 02:55:59 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 02:56:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 02:56:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 03:00:51 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 03:00:51 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 01:18:24 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 01:18:25 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 01:18:25 GMT
COPY dir:1743191a9534b9e7d795d3bf9ad18535d99e75967877447e17d7b63574d878d5 in /usr/local/tomcat 
# Tue, 11 Jul 2023 01:18:28 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 01:18:29 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 01:18:29 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 01:18:29 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 05:22:36 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 05:24:28 GMT
ENV XWIKI_VERSION=14.10.13
# Tue, 11 Jul 2023 05:24:28 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.13
# Tue, 11 Jul 2023 05:24:28 GMT
ENV XWIKI_DOWNLOAD_SHA256=5883ffdbc10865043778f3caa48fbca900129cf41c76ee6fdafba74769c928d4
# Tue, 11 Jul 2023 05:25:08 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 05:25:11 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Tue, 11 Jul 2023 05:25:11 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 05:25:11 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 05:25:11 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 05:25:11 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 05:25:11 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 05:25:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 05:25:11 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:ac34a2e0269ced3acc355be706239ee0f3f1e73a035c40dd2fac74827164ee53`  
		Last Modified: Wed, 28 Jun 2023 23:23:40 GMT  
		Size: 28.4 MB (28391011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d9df805749ad7c4605f0d49a64da6a6173ab190ec361dc2063b6b73af59ab5`  
		Last Modified: Tue, 04 Jul 2023 15:36:55 GMT  
		Size: 12.5 MB (12455497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1e11a5919e5746092b2a288f71090ffdb0d3544b7b54c31ed0137e6d5d4735`  
		Last Modified: Tue, 04 Jul 2023 15:38:37 GMT  
		Size: 45.0 MB (45009079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80987dc89da28aa5ceec7a86ea74e13cee06ecd9304cf4c92d8f382c79eb4f2`  
		Last Modified: Tue, 04 Jul 2023 15:38:32 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de67c7824eef053da628456fe8aba244c4150024af9454dd4091763920d836c`  
		Last Modified: Wed, 05 Jul 2023 03:14:23 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f77f07e56c3d3019cd346deaeacbe572b15b26a924c19b6386877b47123a89e`  
		Last Modified: Tue, 11 Jul 2023 01:39:24 GMT  
		Size: 12.3 MB (12283700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2422cddd65b0ff63d783c999d005c42281720b8615f5872e1e8fdb32dd9981d9`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 455.1 KB (455052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b023f0d964d565a960e567dcaaa605fdff6da02b54971f4d0693506b481b8c`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:968d46d099e01403854799f31b6235698a474c27fd58b0172b1eb3889cd5067f`  
		Last Modified: Tue, 11 Jul 2023 05:26:50 GMT  
		Size: 174.3 MB (174313369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58c2e2d1a49c77dd7a2b5e47670a35d29aca6a19183b43226d929ab037e2cf4a`  
		Last Modified: Tue, 11 Jul 2023 05:28:26 GMT  
		Size: 307.3 MB (307261017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48ff25a83276ff7bee5e0cc9402d6b809cee66bd4e22515f9e4ebf33a5f98d54`  
		Last Modified: Tue, 11 Jul 2023 05:28:12 GMT  
		Size: 936.9 KB (936850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a430a5f61ae1c957b6abf407c502bbac7994125fec841c264e73b3570ca318b`  
		Last Modified: Tue, 11 Jul 2023 05:28:12 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1a1106197e50baaa0b1e4612ce7252b217213ebdc52808529790aec8db034d`  
		Last Modified: Tue, 11 Jul 2023 05:28:12 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84d0854ce2eb5e1ce140a35ba96b4870e229a0bcc691cac48550a44dafbe83d1`  
		Last Modified: Tue, 11 Jul 2023 05:28:12 GMT  
		Size: 6.0 KB (6019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b30724798e976582c41b18d0c093767d1a9df69f9a34b9d57bbf90c21634feff`  
		Last Modified: Tue, 11 Jul 2023 05:28:12 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:14.10.14`

**does not exist** (yet?)

## `xwiki:14.10.14-mariadb-tomcat`

**does not exist** (yet?)

## `xwiki:14.10.14-mysql-tomcat`

**does not exist** (yet?)

## `xwiki:14.10.14-postgres-tomcat`

**does not exist** (yet?)

## `xwiki:15`

```console
$ docker pull xwiki@sha256:66e25eb51a5a079e68e523ac98a46358b70c8c431f4360e1565d23aead7eaa3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:15` - linux; amd64

```console
$ docker pull xwiki@sha256:80718cf2818aac2523383b177893d1f4454722abe547ec303a18e3b4a30362b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **587.3 MB (587250774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97a5a7f1172dd3ea626947d13678241c2e0f4e5391c13ab4c32dd3f009d902c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:37:40 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:37:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:37:42 GMT
ADD file:140fb5108b4a2861b5718ad03b4a5174bba03589ea8d4c053e6a0b282f439ff3 in / 
# Wed, 28 Jun 2023 08:37:42 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:34:07 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:35:02 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 20:35:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 20:35:35 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 08:22:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 08:22:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 08:22:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 08:22:21 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 08:22:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:22:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:25:33 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 08:25:34 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 00:16:15 GMT
COPY dir:8ddeace4a16f09a0d97488e225c7b2e4a48c9a93484d24b46a09759f52800501 in /usr/local/tomcat 
# Tue, 11 Jul 2023 00:16:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 00:16:20 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 00:16:20 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 00:16:20 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 04:40:02 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 04:40:03 GMT
ENV XWIKI_VERSION=15.5
# Tue, 11 Jul 2023 04:40:03 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.5
# Tue, 11 Jul 2023 04:40:03 GMT
ENV XWIKI_DOWNLOAD_SHA256=e552586d371da33b012cfbd974b3ba80d1b147a5c892ad6cf989960212cdaa02
# Tue, 11 Jul 2023 04:40:41 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 04:40:42 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Tue, 11 Jul 2023 04:40:42 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Tue, 11 Jul 2023 04:40:42 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Tue, 11 Jul 2023 04:40:42 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 04:40:42 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 04:40:43 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Tue, 11 Jul 2023 04:40:43 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 04:40:43 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 04:40:44 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 04:40:44 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 04:40:44 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 04:40:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 04:40:44 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:9d19ee268e0d7bcf6716e6658ee1b0384a71d6f2f9aa1ae2085610cf7c7b316f`  
		Last Modified: Wed, 28 Jun 2023 11:50:41 GMT  
		Size: 30.4 MB (30431229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32db0ad82863deaedd2f9a365e52f595085778d28bd1e6f1d351107590cad806`  
		Last Modified: Tue, 04 Jul 2023 20:39:05 GMT  
		Size: 12.5 MB (12495341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01bb55fbcae928d7e6c08d6618580d2b27ce6e46083f861bbed1e01db41c20b`  
		Last Modified: Tue, 04 Jul 2023 20:41:01 GMT  
		Size: 46.7 MB (46666353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297c6e3f57ee032a3cc5f0fd28b52687129e7a1e6485aea12aff08cb6620071e`  
		Last Modified: Tue, 04 Jul 2023 20:40:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15b01f5ab5b71b356d93dff08f5037af8e8a03b4657f1fd303052261161ebd8`  
		Last Modified: Wed, 05 Jul 2023 08:37:14 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c6051a2b9ffe906ea99b555033966c877468da73cd19fd793c86099d0af531`  
		Last Modified: Tue, 11 Jul 2023 00:38:45 GMT  
		Size: 12.3 MB (12274167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34aaed1f6a3460fc256e262b462c1180ccef1b0665ffd50f900d1ef9c19f1d24`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 454.7 KB (454674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b809bf54ada009dfd91afa6ad239f7a791807f2928941b7f969493ec38246be`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877cc60516baaeb7846bba5d5de9e491d0406cd2f43959d7d4e104d89df5e228`  
		Last Modified: Tue, 11 Jul 2023 04:44:49 GMT  
		Size: 178.3 MB (178335971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b863cfbbf93cec3814eec01a334529779a02fcbb3cdff4e2d212bb70287a5720`  
		Last Modified: Tue, 11 Jul 2023 04:44:42 GMT  
		Size: 304.2 MB (304236736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faad5f8d2320ee7d3eb3c3f81aff36754d147687cdb520bc8b24d3170bfcee58`  
		Last Modified: Tue, 11 Jul 2023 04:44:25 GMT  
		Size: 2.3 MB (2343679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ad43407c01ec5371102aaa125c19fb5399f629346a71d4913d742cfed44165`  
		Last Modified: Tue, 11 Jul 2023 04:44:24 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03112af3cb3ddf2e651a23fd879dd50f96a17b20d580105c90d7bb357f02ab0a`  
		Last Modified: Tue, 11 Jul 2023 04:44:24 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7098881bee3a8920bec6f5c352be02657d02e5bb3a4ce69faa81f9354193acbf`  
		Last Modified: Tue, 11 Jul 2023 04:44:24 GMT  
		Size: 6.0 KB (6004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:880ec6a5100b3effc0772c9e06afdfdab1786151d59c78eb30826e0245f2ebe5`  
		Last Modified: Tue, 11 Jul 2023 04:44:24 GMT  
		Size: 2.5 KB (2507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:15` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:80454bf7fba586e95357c0d982c52ab2d1504e85c6d085e14a1091a19a0d7e65
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.6 MB (578560793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e24eddde7707953934d4ceba63f6297ff5115dc6ec8e8e39946e4f8bd2542c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:42:48 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:42:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:42:50 GMT
ADD file:262490f82459c14632f5c9a6d6a5cf6c07b4f307e8fd380fa764662cda46e88f in / 
# Wed, 28 Jun 2023 08:42:50 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:59 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 15:33:41 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 15:34:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 15:34:08 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 02:55:59 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 02:55:59 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 02:55:59 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 02:55:59 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 02:56:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 02:56:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 03:00:51 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 03:00:51 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 01:18:24 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 01:18:25 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 01:18:25 GMT
COPY dir:1743191a9534b9e7d795d3bf9ad18535d99e75967877447e17d7b63574d878d5 in /usr/local/tomcat 
# Tue, 11 Jul 2023 01:18:28 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 01:18:29 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 01:18:29 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 01:18:29 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 05:21:20 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 05:21:23 GMT
ENV XWIKI_VERSION=15.5
# Tue, 11 Jul 2023 05:21:23 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.5
# Tue, 11 Jul 2023 05:21:23 GMT
ENV XWIKI_DOWNLOAD_SHA256=e552586d371da33b012cfbd974b3ba80d1b147a5c892ad6cf989960212cdaa02
# Tue, 11 Jul 2023 05:22:02 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 05:22:04 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Tue, 11 Jul 2023 05:22:04 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Tue, 11 Jul 2023 05:22:04 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Tue, 11 Jul 2023 05:22:04 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 05:22:04 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 05:22:05 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Tue, 11 Jul 2023 05:22:06 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 05:22:06 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 05:22:06 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 05:22:06 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 05:22:06 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 05:22:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 05:22:06 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:ac34a2e0269ced3acc355be706239ee0f3f1e73a035c40dd2fac74827164ee53`  
		Last Modified: Wed, 28 Jun 2023 23:23:40 GMT  
		Size: 28.4 MB (28391011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d9df805749ad7c4605f0d49a64da6a6173ab190ec361dc2063b6b73af59ab5`  
		Last Modified: Tue, 04 Jul 2023 15:36:55 GMT  
		Size: 12.5 MB (12455497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1e11a5919e5746092b2a288f71090ffdb0d3544b7b54c31ed0137e6d5d4735`  
		Last Modified: Tue, 04 Jul 2023 15:38:37 GMT  
		Size: 45.0 MB (45009079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80987dc89da28aa5ceec7a86ea74e13cee06ecd9304cf4c92d8f382c79eb4f2`  
		Last Modified: Tue, 04 Jul 2023 15:38:32 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de67c7824eef053da628456fe8aba244c4150024af9454dd4091763920d836c`  
		Last Modified: Wed, 05 Jul 2023 03:14:23 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f77f07e56c3d3019cd346deaeacbe572b15b26a924c19b6386877b47123a89e`  
		Last Modified: Tue, 11 Jul 2023 01:39:24 GMT  
		Size: 12.3 MB (12283700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2422cddd65b0ff63d783c999d005c42281720b8615f5872e1e8fdb32dd9981d9`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 455.1 KB (455052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b023f0d964d565a960e567dcaaa605fdff6da02b54971f4d0693506b481b8c`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28177f0763a75e5c940bb6a7919185effccd7cf14c0e350198b3aedbe1db789`  
		Last Modified: Tue, 11 Jul 2023 05:26:01 GMT  
		Size: 173.4 MB (173373450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b39c7f4340aa5dd678a6a0a9bc018229eaadb2a94a0af6bc41d17ce77cdefb`  
		Last Modified: Tue, 11 Jul 2023 05:25:57 GMT  
		Size: 304.2 MB (304236707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc58f6eb776423b78c7a88af6ee221317c44f67e3fb4f413ef3823e8895288a2`  
		Last Modified: Tue, 11 Jul 2023 05:25:43 GMT  
		Size: 2.3 MB (2343673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea5e5502a3de7ec04368cbbb5f6c48f21fc7eac2657e2376ab3c7271ad4f85d`  
		Last Modified: Tue, 11 Jul 2023 05:25:43 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f8adcd32841dea1f4e39476b790a663510401829d69a806cad6007452d0367`  
		Last Modified: Tue, 11 Jul 2023 05:25:43 GMT  
		Size: 2.3 KB (2310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa238d29e18bbc7bdc963a1e1b2680c62ba2df6944ca0da2f99bd14855d1534`  
		Last Modified: Tue, 11 Jul 2023 05:25:43 GMT  
		Size: 6.0 KB (6005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ff1ad0797d8b4bc76bf31cb29679b76b9a9af76a225e434abe3b7d81295b942`  
		Last Modified: Tue, 11 Jul 2023 05:25:43 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:15-mariadb-tomcat`

```console
$ docker pull xwiki@sha256:d447b71c1f3084c255c2effee1762e635e6e07f08edcc0bd5b9c46d892350483
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:15-mariadb-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:6ece9caf8c15d2557f7f165d530deb3442aae7b1bb3b968ba2236e987cebbe2d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **585.5 MB (585501648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac976c622edabab4c9f4be5e6b071f4be6640e98d657487308bb3bb030921d13`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:37:40 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:37:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:37:42 GMT
ADD file:140fb5108b4a2861b5718ad03b4a5174bba03589ea8d4c053e6a0b282f439ff3 in / 
# Wed, 28 Jun 2023 08:37:42 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:34:07 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:35:02 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 20:35:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 20:35:35 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 08:22:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 08:22:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 08:22:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 08:22:21 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 08:22:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:22:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:25:33 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 08:25:34 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 00:16:15 GMT
COPY dir:8ddeace4a16f09a0d97488e225c7b2e4a48c9a93484d24b46a09759f52800501 in /usr/local/tomcat 
# Tue, 11 Jul 2023 00:16:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 00:16:20 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 00:16:20 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 00:16:20 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 04:40:02 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 04:40:03 GMT
ENV XWIKI_VERSION=15.5
# Tue, 11 Jul 2023 04:40:03 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.5
# Tue, 11 Jul 2023 04:40:03 GMT
ENV XWIKI_DOWNLOAD_SHA256=e552586d371da33b012cfbd974b3ba80d1b147a5c892ad6cf989960212cdaa02
# Tue, 11 Jul 2023 04:40:41 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 04:42:10 GMT
ENV MARIADB_JDBC_VERSION=3.1.4
# Tue, 11 Jul 2023 04:42:10 GMT
ENV MARIADB_JDBC_SHA256=eb88b5d727d82e25117e2b6fabcec1daf734633b0a576456c73215884c189ad4
# Tue, 11 Jul 2023 04:42:10 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.1.4
# Tue, 11 Jul 2023 04:42:10 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.1.4.jar
# Tue, 11 Jul 2023 04:42:10 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.1.4.jar
# Tue, 11 Jul 2023 04:42:11 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Tue, 11 Jul 2023 04:42:11 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 04:42:11 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 04:42:12 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 04:42:12 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 04:42:12 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 04:42:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 04:42:12 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:9d19ee268e0d7bcf6716e6658ee1b0384a71d6f2f9aa1ae2085610cf7c7b316f`  
		Last Modified: Wed, 28 Jun 2023 11:50:41 GMT  
		Size: 30.4 MB (30431229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32db0ad82863deaedd2f9a365e52f595085778d28bd1e6f1d351107590cad806`  
		Last Modified: Tue, 04 Jul 2023 20:39:05 GMT  
		Size: 12.5 MB (12495341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01bb55fbcae928d7e6c08d6618580d2b27ce6e46083f861bbed1e01db41c20b`  
		Last Modified: Tue, 04 Jul 2023 20:41:01 GMT  
		Size: 46.7 MB (46666353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297c6e3f57ee032a3cc5f0fd28b52687129e7a1e6485aea12aff08cb6620071e`  
		Last Modified: Tue, 04 Jul 2023 20:40:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15b01f5ab5b71b356d93dff08f5037af8e8a03b4657f1fd303052261161ebd8`  
		Last Modified: Wed, 05 Jul 2023 08:37:14 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c6051a2b9ffe906ea99b555033966c877468da73cd19fd793c86099d0af531`  
		Last Modified: Tue, 11 Jul 2023 00:38:45 GMT  
		Size: 12.3 MB (12274167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34aaed1f6a3460fc256e262b462c1180ccef1b0665ffd50f900d1ef9c19f1d24`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 454.7 KB (454674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b809bf54ada009dfd91afa6ad239f7a791807f2928941b7f969493ec38246be`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877cc60516baaeb7846bba5d5de9e491d0406cd2f43959d7d4e104d89df5e228`  
		Last Modified: Tue, 11 Jul 2023 04:44:49 GMT  
		Size: 178.3 MB (178335971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b863cfbbf93cec3814eec01a334529779a02fcbb3cdff4e2d212bb70287a5720`  
		Last Modified: Tue, 11 Jul 2023 04:44:42 GMT  
		Size: 304.2 MB (304236736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d9f121998f3ebb1fe9d8b1e2b7964a6e19afe2500ee4c64b95739f1578f0728`  
		Last Modified: Tue, 11 Jul 2023 04:46:03 GMT  
		Size: 594.6 KB (594553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b2c8c7e34dbea6b864808d65dae2a48aaa73e9595b3dd30f14d4b95b28cbcf`  
		Last Modified: Tue, 11 Jul 2023 04:46:03 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84634ee1814641c052e3b568592a22c625bc82aaf05fdb64d6dcbdb17ff803b7`  
		Last Modified: Tue, 11 Jul 2023 04:46:03 GMT  
		Size: 2.3 KB (2311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f62b3d21969533fa11c23f989db62def095f4c38f4e3ebba9bdb897cb756a783`  
		Last Modified: Tue, 11 Jul 2023 04:46:03 GMT  
		Size: 6.0 KB (6003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d136eed865c53c0489a1100cd4c540d7269e0bbc620b8b44fa3c71d168a0e583`  
		Last Modified: Tue, 11 Jul 2023 04:46:03 GMT  
		Size: 2.5 KB (2503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:15-mariadb-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:2745b46e135b629961fa0abba943bcd28e8793d51275fbf2d1a945545b31961b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **576.8 MB (576811676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa8facaf677aa5a99371bfdf03feab6977a37475e6664e98cdef94878d40484c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:42:48 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:42:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:42:50 GMT
ADD file:262490f82459c14632f5c9a6d6a5cf6c07b4f307e8fd380fa764662cda46e88f in / 
# Wed, 28 Jun 2023 08:42:50 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:59 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 15:33:41 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 15:34:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 15:34:08 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 02:55:59 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 02:55:59 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 02:55:59 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 02:55:59 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 02:56:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 02:56:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 03:00:51 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 03:00:51 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 01:18:24 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 01:18:25 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 01:18:25 GMT
COPY dir:1743191a9534b9e7d795d3bf9ad18535d99e75967877447e17d7b63574d878d5 in /usr/local/tomcat 
# Tue, 11 Jul 2023 01:18:28 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 01:18:29 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 01:18:29 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 01:18:29 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 05:21:20 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 05:21:23 GMT
ENV XWIKI_VERSION=15.5
# Tue, 11 Jul 2023 05:21:23 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.5
# Tue, 11 Jul 2023 05:21:23 GMT
ENV XWIKI_DOWNLOAD_SHA256=e552586d371da33b012cfbd974b3ba80d1b147a5c892ad6cf989960212cdaa02
# Tue, 11 Jul 2023 05:22:02 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 05:23:36 GMT
ENV MARIADB_JDBC_VERSION=3.1.4
# Tue, 11 Jul 2023 05:23:36 GMT
ENV MARIADB_JDBC_SHA256=eb88b5d727d82e25117e2b6fabcec1daf734633b0a576456c73215884c189ad4
# Tue, 11 Jul 2023 05:23:36 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.1.4
# Tue, 11 Jul 2023 05:23:37 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.1.4.jar
# Tue, 11 Jul 2023 05:23:37 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.1.4.jar
# Tue, 11 Jul 2023 05:23:37 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Tue, 11 Jul 2023 05:23:37 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 05:23:37 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 05:23:38 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 05:23:38 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 05:23:38 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 05:23:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 05:23:38 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:ac34a2e0269ced3acc355be706239ee0f3f1e73a035c40dd2fac74827164ee53`  
		Last Modified: Wed, 28 Jun 2023 23:23:40 GMT  
		Size: 28.4 MB (28391011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d9df805749ad7c4605f0d49a64da6a6173ab190ec361dc2063b6b73af59ab5`  
		Last Modified: Tue, 04 Jul 2023 15:36:55 GMT  
		Size: 12.5 MB (12455497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1e11a5919e5746092b2a288f71090ffdb0d3544b7b54c31ed0137e6d5d4735`  
		Last Modified: Tue, 04 Jul 2023 15:38:37 GMT  
		Size: 45.0 MB (45009079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80987dc89da28aa5ceec7a86ea74e13cee06ecd9304cf4c92d8f382c79eb4f2`  
		Last Modified: Tue, 04 Jul 2023 15:38:32 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de67c7824eef053da628456fe8aba244c4150024af9454dd4091763920d836c`  
		Last Modified: Wed, 05 Jul 2023 03:14:23 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f77f07e56c3d3019cd346deaeacbe572b15b26a924c19b6386877b47123a89e`  
		Last Modified: Tue, 11 Jul 2023 01:39:24 GMT  
		Size: 12.3 MB (12283700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2422cddd65b0ff63d783c999d005c42281720b8615f5872e1e8fdb32dd9981d9`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 455.1 KB (455052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b023f0d964d565a960e567dcaaa605fdff6da02b54971f4d0693506b481b8c`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28177f0763a75e5c940bb6a7919185effccd7cf14c0e350198b3aedbe1db789`  
		Last Modified: Tue, 11 Jul 2023 05:26:01 GMT  
		Size: 173.4 MB (173373450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b39c7f4340aa5dd678a6a0a9bc018229eaadb2a94a0af6bc41d17ce77cdefb`  
		Last Modified: Tue, 11 Jul 2023 05:25:57 GMT  
		Size: 304.2 MB (304236707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0be5f78ca514976c969b47013a6e82418af20d755526a18e35388d7482170b8`  
		Last Modified: Tue, 11 Jul 2023 05:27:14 GMT  
		Size: 594.6 KB (594556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01372195bd2be58e8f5f6433314edfd376c3ce7d69fe9fc1b21188af306f2ce1`  
		Last Modified: Tue, 11 Jul 2023 05:27:14 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15366f793a0d945e4ef67931cb193ae8c2b7f218ecba840af9cf4958adb81ce8`  
		Last Modified: Tue, 11 Jul 2023 05:27:14 GMT  
		Size: 2.3 KB (2312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae0ba8487202e29a15c7c1b505e9f148753e98c7e9284bb88ab357269ef43ab`  
		Last Modified: Tue, 11 Jul 2023 05:27:14 GMT  
		Size: 6.0 KB (6004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4d894785e0d9bda2444090848544b861a5280bd4c8a3e5686acc3d6f3f232fe`  
		Last Modified: Tue, 11 Jul 2023 05:27:14 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:15-mysql-tomcat`

```console
$ docker pull xwiki@sha256:66e25eb51a5a079e68e523ac98a46358b70c8c431f4360e1565d23aead7eaa3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:15-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:80718cf2818aac2523383b177893d1f4454722abe547ec303a18e3b4a30362b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **587.3 MB (587250774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97a5a7f1172dd3ea626947d13678241c2e0f4e5391c13ab4c32dd3f009d902c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:37:40 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:37:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:37:42 GMT
ADD file:140fb5108b4a2861b5718ad03b4a5174bba03589ea8d4c053e6a0b282f439ff3 in / 
# Wed, 28 Jun 2023 08:37:42 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:34:07 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:35:02 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 20:35:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 20:35:35 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 08:22:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 08:22:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 08:22:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 08:22:21 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 08:22:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:22:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:25:33 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 08:25:34 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 00:16:15 GMT
COPY dir:8ddeace4a16f09a0d97488e225c7b2e4a48c9a93484d24b46a09759f52800501 in /usr/local/tomcat 
# Tue, 11 Jul 2023 00:16:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 00:16:20 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 00:16:20 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 00:16:20 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 04:40:02 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 04:40:03 GMT
ENV XWIKI_VERSION=15.5
# Tue, 11 Jul 2023 04:40:03 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.5
# Tue, 11 Jul 2023 04:40:03 GMT
ENV XWIKI_DOWNLOAD_SHA256=e552586d371da33b012cfbd974b3ba80d1b147a5c892ad6cf989960212cdaa02
# Tue, 11 Jul 2023 04:40:41 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 04:40:42 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Tue, 11 Jul 2023 04:40:42 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Tue, 11 Jul 2023 04:40:42 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Tue, 11 Jul 2023 04:40:42 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 04:40:42 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 04:40:43 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Tue, 11 Jul 2023 04:40:43 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 04:40:43 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 04:40:44 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 04:40:44 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 04:40:44 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 04:40:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 04:40:44 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:9d19ee268e0d7bcf6716e6658ee1b0384a71d6f2f9aa1ae2085610cf7c7b316f`  
		Last Modified: Wed, 28 Jun 2023 11:50:41 GMT  
		Size: 30.4 MB (30431229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32db0ad82863deaedd2f9a365e52f595085778d28bd1e6f1d351107590cad806`  
		Last Modified: Tue, 04 Jul 2023 20:39:05 GMT  
		Size: 12.5 MB (12495341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01bb55fbcae928d7e6c08d6618580d2b27ce6e46083f861bbed1e01db41c20b`  
		Last Modified: Tue, 04 Jul 2023 20:41:01 GMT  
		Size: 46.7 MB (46666353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297c6e3f57ee032a3cc5f0fd28b52687129e7a1e6485aea12aff08cb6620071e`  
		Last Modified: Tue, 04 Jul 2023 20:40:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15b01f5ab5b71b356d93dff08f5037af8e8a03b4657f1fd303052261161ebd8`  
		Last Modified: Wed, 05 Jul 2023 08:37:14 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c6051a2b9ffe906ea99b555033966c877468da73cd19fd793c86099d0af531`  
		Last Modified: Tue, 11 Jul 2023 00:38:45 GMT  
		Size: 12.3 MB (12274167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34aaed1f6a3460fc256e262b462c1180ccef1b0665ffd50f900d1ef9c19f1d24`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 454.7 KB (454674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b809bf54ada009dfd91afa6ad239f7a791807f2928941b7f969493ec38246be`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877cc60516baaeb7846bba5d5de9e491d0406cd2f43959d7d4e104d89df5e228`  
		Last Modified: Tue, 11 Jul 2023 04:44:49 GMT  
		Size: 178.3 MB (178335971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b863cfbbf93cec3814eec01a334529779a02fcbb3cdff4e2d212bb70287a5720`  
		Last Modified: Tue, 11 Jul 2023 04:44:42 GMT  
		Size: 304.2 MB (304236736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faad5f8d2320ee7d3eb3c3f81aff36754d147687cdb520bc8b24d3170bfcee58`  
		Last Modified: Tue, 11 Jul 2023 04:44:25 GMT  
		Size: 2.3 MB (2343679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ad43407c01ec5371102aaa125c19fb5399f629346a71d4913d742cfed44165`  
		Last Modified: Tue, 11 Jul 2023 04:44:24 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03112af3cb3ddf2e651a23fd879dd50f96a17b20d580105c90d7bb357f02ab0a`  
		Last Modified: Tue, 11 Jul 2023 04:44:24 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7098881bee3a8920bec6f5c352be02657d02e5bb3a4ce69faa81f9354193acbf`  
		Last Modified: Tue, 11 Jul 2023 04:44:24 GMT  
		Size: 6.0 KB (6004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:880ec6a5100b3effc0772c9e06afdfdab1786151d59c78eb30826e0245f2ebe5`  
		Last Modified: Tue, 11 Jul 2023 04:44:24 GMT  
		Size: 2.5 KB (2507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:15-mysql-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:80454bf7fba586e95357c0d982c52ab2d1504e85c6d085e14a1091a19a0d7e65
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.6 MB (578560793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e24eddde7707953934d4ceba63f6297ff5115dc6ec8e8e39946e4f8bd2542c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:42:48 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:42:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:42:50 GMT
ADD file:262490f82459c14632f5c9a6d6a5cf6c07b4f307e8fd380fa764662cda46e88f in / 
# Wed, 28 Jun 2023 08:42:50 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:59 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 15:33:41 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 15:34:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 15:34:08 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 02:55:59 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 02:55:59 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 02:55:59 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 02:55:59 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 02:56:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 02:56:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 03:00:51 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 03:00:51 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 01:18:24 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 01:18:25 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 01:18:25 GMT
COPY dir:1743191a9534b9e7d795d3bf9ad18535d99e75967877447e17d7b63574d878d5 in /usr/local/tomcat 
# Tue, 11 Jul 2023 01:18:28 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 01:18:29 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 01:18:29 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 01:18:29 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 05:21:20 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 05:21:23 GMT
ENV XWIKI_VERSION=15.5
# Tue, 11 Jul 2023 05:21:23 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.5
# Tue, 11 Jul 2023 05:21:23 GMT
ENV XWIKI_DOWNLOAD_SHA256=e552586d371da33b012cfbd974b3ba80d1b147a5c892ad6cf989960212cdaa02
# Tue, 11 Jul 2023 05:22:02 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 05:22:04 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Tue, 11 Jul 2023 05:22:04 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Tue, 11 Jul 2023 05:22:04 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Tue, 11 Jul 2023 05:22:04 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 05:22:04 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 05:22:05 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Tue, 11 Jul 2023 05:22:06 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 05:22:06 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 05:22:06 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 05:22:06 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 05:22:06 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 05:22:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 05:22:06 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:ac34a2e0269ced3acc355be706239ee0f3f1e73a035c40dd2fac74827164ee53`  
		Last Modified: Wed, 28 Jun 2023 23:23:40 GMT  
		Size: 28.4 MB (28391011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d9df805749ad7c4605f0d49a64da6a6173ab190ec361dc2063b6b73af59ab5`  
		Last Modified: Tue, 04 Jul 2023 15:36:55 GMT  
		Size: 12.5 MB (12455497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1e11a5919e5746092b2a288f71090ffdb0d3544b7b54c31ed0137e6d5d4735`  
		Last Modified: Tue, 04 Jul 2023 15:38:37 GMT  
		Size: 45.0 MB (45009079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80987dc89da28aa5ceec7a86ea74e13cee06ecd9304cf4c92d8f382c79eb4f2`  
		Last Modified: Tue, 04 Jul 2023 15:38:32 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de67c7824eef053da628456fe8aba244c4150024af9454dd4091763920d836c`  
		Last Modified: Wed, 05 Jul 2023 03:14:23 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f77f07e56c3d3019cd346deaeacbe572b15b26a924c19b6386877b47123a89e`  
		Last Modified: Tue, 11 Jul 2023 01:39:24 GMT  
		Size: 12.3 MB (12283700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2422cddd65b0ff63d783c999d005c42281720b8615f5872e1e8fdb32dd9981d9`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 455.1 KB (455052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b023f0d964d565a960e567dcaaa605fdff6da02b54971f4d0693506b481b8c`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28177f0763a75e5c940bb6a7919185effccd7cf14c0e350198b3aedbe1db789`  
		Last Modified: Tue, 11 Jul 2023 05:26:01 GMT  
		Size: 173.4 MB (173373450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b39c7f4340aa5dd678a6a0a9bc018229eaadb2a94a0af6bc41d17ce77cdefb`  
		Last Modified: Tue, 11 Jul 2023 05:25:57 GMT  
		Size: 304.2 MB (304236707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc58f6eb776423b78c7a88af6ee221317c44f67e3fb4f413ef3823e8895288a2`  
		Last Modified: Tue, 11 Jul 2023 05:25:43 GMT  
		Size: 2.3 MB (2343673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea5e5502a3de7ec04368cbbb5f6c48f21fc7eac2657e2376ab3c7271ad4f85d`  
		Last Modified: Tue, 11 Jul 2023 05:25:43 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f8adcd32841dea1f4e39476b790a663510401829d69a806cad6007452d0367`  
		Last Modified: Tue, 11 Jul 2023 05:25:43 GMT  
		Size: 2.3 KB (2310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa238d29e18bbc7bdc963a1e1b2680c62ba2df6944ca0da2f99bd14855d1534`  
		Last Modified: Tue, 11 Jul 2023 05:25:43 GMT  
		Size: 6.0 KB (6005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ff1ad0797d8b4bc76bf31cb29679b76b9a9af76a225e434abe3b7d81295b942`  
		Last Modified: Tue, 11 Jul 2023 05:25:43 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:15-postgres-tomcat`

```console
$ docker pull xwiki@sha256:143482a096b13073c1d9d59fde125210cd6009c4fb253a6d30cf5eaf8481fc5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:15-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:4741e9d9b24c00013903dbabf718e61ef5c4b23fd41a283067988225a4ea60ae
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **586.8 MB (586784502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1a1f265f59dcb2e5a6888c86ef11b46a92e4d498dcf98b2ab1f05735021fa2a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:37:40 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:37:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:37:42 GMT
ADD file:140fb5108b4a2861b5718ad03b4a5174bba03589ea8d4c053e6a0b282f439ff3 in / 
# Wed, 28 Jun 2023 08:37:42 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:34:07 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:35:02 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 20:35:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 20:35:35 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 08:22:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 08:22:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 08:22:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 08:22:21 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 08:22:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:22:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:25:33 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 08:25:34 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 00:16:15 GMT
COPY dir:8ddeace4a16f09a0d97488e225c7b2e4a48c9a93484d24b46a09759f52800501 in /usr/local/tomcat 
# Tue, 11 Jul 2023 00:16:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 00:16:20 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 00:16:20 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 00:16:20 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 04:41:24 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 04:41:26 GMT
ENV XWIKI_VERSION=15.5
# Tue, 11 Jul 2023 04:41:26 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.5
# Tue, 11 Jul 2023 04:41:26 GMT
ENV XWIKI_DOWNLOAD_SHA256=e552586d371da33b012cfbd974b3ba80d1b147a5c892ad6cf989960212cdaa02
# Tue, 11 Jul 2023 04:42:04 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 04:42:05 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Tue, 11 Jul 2023 04:42:05 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 04:42:05 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 04:42:06 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 04:42:06 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 04:42:06 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 04:42:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 04:42:06 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:9d19ee268e0d7bcf6716e6658ee1b0384a71d6f2f9aa1ae2085610cf7c7b316f`  
		Last Modified: Wed, 28 Jun 2023 11:50:41 GMT  
		Size: 30.4 MB (30431229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32db0ad82863deaedd2f9a365e52f595085778d28bd1e6f1d351107590cad806`  
		Last Modified: Tue, 04 Jul 2023 20:39:05 GMT  
		Size: 12.5 MB (12495341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01bb55fbcae928d7e6c08d6618580d2b27ce6e46083f861bbed1e01db41c20b`  
		Last Modified: Tue, 04 Jul 2023 20:41:01 GMT  
		Size: 46.7 MB (46666353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297c6e3f57ee032a3cc5f0fd28b52687129e7a1e6485aea12aff08cb6620071e`  
		Last Modified: Tue, 04 Jul 2023 20:40:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15b01f5ab5b71b356d93dff08f5037af8e8a03b4657f1fd303052261161ebd8`  
		Last Modified: Wed, 05 Jul 2023 08:37:14 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c6051a2b9ffe906ea99b555033966c877468da73cd19fd793c86099d0af531`  
		Last Modified: Tue, 11 Jul 2023 00:38:45 GMT  
		Size: 12.3 MB (12274167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34aaed1f6a3460fc256e262b462c1180ccef1b0665ffd50f900d1ef9c19f1d24`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 454.7 KB (454674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b809bf54ada009dfd91afa6ad239f7a791807f2928941b7f969493ec38246be`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bd305e7867896df13faced03525a0f25bf1ac1b2a2c93e60382cdfd41c08e16`  
		Last Modified: Tue, 11 Jul 2023 04:45:43 GMT  
		Size: 179.3 MB (179276407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35bfb758076cf011f5df9081f31dfbcf656cd98cd11b65f53f3684ec1e485c8f`  
		Last Modified: Tue, 11 Jul 2023 04:45:37 GMT  
		Size: 304.2 MB (304236708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2f8ccc8af30dd82bb4657bfdb7193ed23e8dc8823df1eaea8b1c8e4ab85d60`  
		Last Modified: Tue, 11 Jul 2023 04:45:20 GMT  
		Size: 936.8 KB (936849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:822e7d00d75f2a5b9a34edd0741b7e19410deb191f96800278c2921b043c81cb`  
		Last Modified: Tue, 11 Jul 2023 04:45:19 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba3137d80fef0218e2aaa65df38833a3e9d79b0d6e0b8d441376edbc36190ab`  
		Last Modified: Tue, 11 Jul 2023 04:45:19 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d02045e3c19030183c43f79b2c5e3a2f244dda96d11e96014e91d90e85f6e3a9`  
		Last Modified: Tue, 11 Jul 2023 04:45:19 GMT  
		Size: 6.0 KB (6006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91afad54a0c6d44f603953379c22801e4dbc9f2c282eaa00e94946d1d77dc3a4`  
		Last Modified: Tue, 11 Jul 2023 04:45:19 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:15-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:30799eeac6bc3f0efeefaf95f4161eeea6298cf60983391d2b7789735d58fa07
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.1 MB (578094027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc026cfcc219f16306961c1815044f7a63d5f49577815243d20c27d2d823d48`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:42:48 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:42:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:42:50 GMT
ADD file:262490f82459c14632f5c9a6d6a5cf6c07b4f307e8fd380fa764662cda46e88f in / 
# Wed, 28 Jun 2023 08:42:50 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:59 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 15:33:41 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 15:34:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 15:34:08 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 02:55:59 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 02:55:59 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 02:55:59 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 02:55:59 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 02:56:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 02:56:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 03:00:51 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 03:00:51 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 01:18:24 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 01:18:25 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 01:18:25 GMT
COPY dir:1743191a9534b9e7d795d3bf9ad18535d99e75967877447e17d7b63574d878d5 in /usr/local/tomcat 
# Tue, 11 Jul 2023 01:18:28 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 01:18:29 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 01:18:29 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 01:18:29 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 05:22:36 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 05:22:39 GMT
ENV XWIKI_VERSION=15.5
# Tue, 11 Jul 2023 05:22:39 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.5
# Tue, 11 Jul 2023 05:22:39 GMT
ENV XWIKI_DOWNLOAD_SHA256=e552586d371da33b012cfbd974b3ba80d1b147a5c892ad6cf989960212cdaa02
# Tue, 11 Jul 2023 05:23:18 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 05:23:21 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Tue, 11 Jul 2023 05:23:21 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 05:23:21 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 05:23:22 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 05:23:22 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 05:23:22 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 05:23:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 05:23:22 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:ac34a2e0269ced3acc355be706239ee0f3f1e73a035c40dd2fac74827164ee53`  
		Last Modified: Wed, 28 Jun 2023 23:23:40 GMT  
		Size: 28.4 MB (28391011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d9df805749ad7c4605f0d49a64da6a6173ab190ec361dc2063b6b73af59ab5`  
		Last Modified: Tue, 04 Jul 2023 15:36:55 GMT  
		Size: 12.5 MB (12455497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1e11a5919e5746092b2a288f71090ffdb0d3544b7b54c31ed0137e6d5d4735`  
		Last Modified: Tue, 04 Jul 2023 15:38:37 GMT  
		Size: 45.0 MB (45009079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80987dc89da28aa5ceec7a86ea74e13cee06ecd9304cf4c92d8f382c79eb4f2`  
		Last Modified: Tue, 04 Jul 2023 15:38:32 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de67c7824eef053da628456fe8aba244c4150024af9454dd4091763920d836c`  
		Last Modified: Wed, 05 Jul 2023 03:14:23 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f77f07e56c3d3019cd346deaeacbe572b15b26a924c19b6386877b47123a89e`  
		Last Modified: Tue, 11 Jul 2023 01:39:24 GMT  
		Size: 12.3 MB (12283700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2422cddd65b0ff63d783c999d005c42281720b8615f5872e1e8fdb32dd9981d9`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 455.1 KB (455052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b023f0d964d565a960e567dcaaa605fdff6da02b54971f4d0693506b481b8c`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:968d46d099e01403854799f31b6235698a474c27fd58b0172b1eb3889cd5067f`  
		Last Modified: Tue, 11 Jul 2023 05:26:50 GMT  
		Size: 174.3 MB (174313369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2894444c04152ca46b568422ea482a66ed3763028ff87cc82d80132ea0e4cdd`  
		Last Modified: Tue, 11 Jul 2023 05:26:46 GMT  
		Size: 304.2 MB (304236690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77118bb73ac2d6b789413d31beabdbb72e88543cca5b3e6406076fd10d40d8d3`  
		Last Modified: Tue, 11 Jul 2023 05:26:32 GMT  
		Size: 936.9 KB (936852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9eb9df1942e9402403596582620c7fb14dbdd8e12de634c88e080cc5795a812`  
		Last Modified: Tue, 11 Jul 2023 05:26:32 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d23fb311f1a568af6e8b96dcb8cfb10d4d96a88aee4243256a3e73f4727fa318`  
		Last Modified: Tue, 11 Jul 2023 05:26:32 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dd3c555379bf5bd7f8d13501bb806b6b5ffb4c2ecb169ce4485f1cbf0d26b9a`  
		Last Modified: Tue, 11 Jul 2023 05:26:32 GMT  
		Size: 6.0 KB (6006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8254381348a57ea56306a83d8f2a89630202f393f54d6102b5652be9cfa10f8f`  
		Last Modified: Tue, 11 Jul 2023 05:26:33 GMT  
		Size: 2.5 KB (2507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:15.5`

```console
$ docker pull xwiki@sha256:66e25eb51a5a079e68e523ac98a46358b70c8c431f4360e1565d23aead7eaa3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:15.5` - linux; amd64

```console
$ docker pull xwiki@sha256:80718cf2818aac2523383b177893d1f4454722abe547ec303a18e3b4a30362b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **587.3 MB (587250774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97a5a7f1172dd3ea626947d13678241c2e0f4e5391c13ab4c32dd3f009d902c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:37:40 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:37:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:37:42 GMT
ADD file:140fb5108b4a2861b5718ad03b4a5174bba03589ea8d4c053e6a0b282f439ff3 in / 
# Wed, 28 Jun 2023 08:37:42 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:34:07 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:35:02 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 20:35:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 20:35:35 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 08:22:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 08:22:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 08:22:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 08:22:21 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 08:22:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:22:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:25:33 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 08:25:34 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 00:16:15 GMT
COPY dir:8ddeace4a16f09a0d97488e225c7b2e4a48c9a93484d24b46a09759f52800501 in /usr/local/tomcat 
# Tue, 11 Jul 2023 00:16:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 00:16:20 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 00:16:20 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 00:16:20 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 04:40:02 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 04:40:03 GMT
ENV XWIKI_VERSION=15.5
# Tue, 11 Jul 2023 04:40:03 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.5
# Tue, 11 Jul 2023 04:40:03 GMT
ENV XWIKI_DOWNLOAD_SHA256=e552586d371da33b012cfbd974b3ba80d1b147a5c892ad6cf989960212cdaa02
# Tue, 11 Jul 2023 04:40:41 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 04:40:42 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Tue, 11 Jul 2023 04:40:42 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Tue, 11 Jul 2023 04:40:42 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Tue, 11 Jul 2023 04:40:42 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 04:40:42 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 04:40:43 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Tue, 11 Jul 2023 04:40:43 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 04:40:43 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 04:40:44 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 04:40:44 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 04:40:44 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 04:40:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 04:40:44 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:9d19ee268e0d7bcf6716e6658ee1b0384a71d6f2f9aa1ae2085610cf7c7b316f`  
		Last Modified: Wed, 28 Jun 2023 11:50:41 GMT  
		Size: 30.4 MB (30431229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32db0ad82863deaedd2f9a365e52f595085778d28bd1e6f1d351107590cad806`  
		Last Modified: Tue, 04 Jul 2023 20:39:05 GMT  
		Size: 12.5 MB (12495341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01bb55fbcae928d7e6c08d6618580d2b27ce6e46083f861bbed1e01db41c20b`  
		Last Modified: Tue, 04 Jul 2023 20:41:01 GMT  
		Size: 46.7 MB (46666353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297c6e3f57ee032a3cc5f0fd28b52687129e7a1e6485aea12aff08cb6620071e`  
		Last Modified: Tue, 04 Jul 2023 20:40:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15b01f5ab5b71b356d93dff08f5037af8e8a03b4657f1fd303052261161ebd8`  
		Last Modified: Wed, 05 Jul 2023 08:37:14 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c6051a2b9ffe906ea99b555033966c877468da73cd19fd793c86099d0af531`  
		Last Modified: Tue, 11 Jul 2023 00:38:45 GMT  
		Size: 12.3 MB (12274167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34aaed1f6a3460fc256e262b462c1180ccef1b0665ffd50f900d1ef9c19f1d24`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 454.7 KB (454674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b809bf54ada009dfd91afa6ad239f7a791807f2928941b7f969493ec38246be`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877cc60516baaeb7846bba5d5de9e491d0406cd2f43959d7d4e104d89df5e228`  
		Last Modified: Tue, 11 Jul 2023 04:44:49 GMT  
		Size: 178.3 MB (178335971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b863cfbbf93cec3814eec01a334529779a02fcbb3cdff4e2d212bb70287a5720`  
		Last Modified: Tue, 11 Jul 2023 04:44:42 GMT  
		Size: 304.2 MB (304236736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faad5f8d2320ee7d3eb3c3f81aff36754d147687cdb520bc8b24d3170bfcee58`  
		Last Modified: Tue, 11 Jul 2023 04:44:25 GMT  
		Size: 2.3 MB (2343679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ad43407c01ec5371102aaa125c19fb5399f629346a71d4913d742cfed44165`  
		Last Modified: Tue, 11 Jul 2023 04:44:24 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03112af3cb3ddf2e651a23fd879dd50f96a17b20d580105c90d7bb357f02ab0a`  
		Last Modified: Tue, 11 Jul 2023 04:44:24 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7098881bee3a8920bec6f5c352be02657d02e5bb3a4ce69faa81f9354193acbf`  
		Last Modified: Tue, 11 Jul 2023 04:44:24 GMT  
		Size: 6.0 KB (6004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:880ec6a5100b3effc0772c9e06afdfdab1786151d59c78eb30826e0245f2ebe5`  
		Last Modified: Tue, 11 Jul 2023 04:44:24 GMT  
		Size: 2.5 KB (2507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:15.5` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:80454bf7fba586e95357c0d982c52ab2d1504e85c6d085e14a1091a19a0d7e65
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.6 MB (578560793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e24eddde7707953934d4ceba63f6297ff5115dc6ec8e8e39946e4f8bd2542c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:42:48 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:42:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:42:50 GMT
ADD file:262490f82459c14632f5c9a6d6a5cf6c07b4f307e8fd380fa764662cda46e88f in / 
# Wed, 28 Jun 2023 08:42:50 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:59 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 15:33:41 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 15:34:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 15:34:08 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 02:55:59 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 02:55:59 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 02:55:59 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 02:55:59 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 02:56:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 02:56:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 03:00:51 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 03:00:51 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 01:18:24 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 01:18:25 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 01:18:25 GMT
COPY dir:1743191a9534b9e7d795d3bf9ad18535d99e75967877447e17d7b63574d878d5 in /usr/local/tomcat 
# Tue, 11 Jul 2023 01:18:28 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 01:18:29 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 01:18:29 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 01:18:29 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 05:21:20 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 05:21:23 GMT
ENV XWIKI_VERSION=15.5
# Tue, 11 Jul 2023 05:21:23 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.5
# Tue, 11 Jul 2023 05:21:23 GMT
ENV XWIKI_DOWNLOAD_SHA256=e552586d371da33b012cfbd974b3ba80d1b147a5c892ad6cf989960212cdaa02
# Tue, 11 Jul 2023 05:22:02 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 05:22:04 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Tue, 11 Jul 2023 05:22:04 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Tue, 11 Jul 2023 05:22:04 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Tue, 11 Jul 2023 05:22:04 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 05:22:04 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 05:22:05 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Tue, 11 Jul 2023 05:22:06 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 05:22:06 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 05:22:06 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 05:22:06 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 05:22:06 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 05:22:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 05:22:06 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:ac34a2e0269ced3acc355be706239ee0f3f1e73a035c40dd2fac74827164ee53`  
		Last Modified: Wed, 28 Jun 2023 23:23:40 GMT  
		Size: 28.4 MB (28391011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d9df805749ad7c4605f0d49a64da6a6173ab190ec361dc2063b6b73af59ab5`  
		Last Modified: Tue, 04 Jul 2023 15:36:55 GMT  
		Size: 12.5 MB (12455497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1e11a5919e5746092b2a288f71090ffdb0d3544b7b54c31ed0137e6d5d4735`  
		Last Modified: Tue, 04 Jul 2023 15:38:37 GMT  
		Size: 45.0 MB (45009079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80987dc89da28aa5ceec7a86ea74e13cee06ecd9304cf4c92d8f382c79eb4f2`  
		Last Modified: Tue, 04 Jul 2023 15:38:32 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de67c7824eef053da628456fe8aba244c4150024af9454dd4091763920d836c`  
		Last Modified: Wed, 05 Jul 2023 03:14:23 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f77f07e56c3d3019cd346deaeacbe572b15b26a924c19b6386877b47123a89e`  
		Last Modified: Tue, 11 Jul 2023 01:39:24 GMT  
		Size: 12.3 MB (12283700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2422cddd65b0ff63d783c999d005c42281720b8615f5872e1e8fdb32dd9981d9`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 455.1 KB (455052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b023f0d964d565a960e567dcaaa605fdff6da02b54971f4d0693506b481b8c`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28177f0763a75e5c940bb6a7919185effccd7cf14c0e350198b3aedbe1db789`  
		Last Modified: Tue, 11 Jul 2023 05:26:01 GMT  
		Size: 173.4 MB (173373450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b39c7f4340aa5dd678a6a0a9bc018229eaadb2a94a0af6bc41d17ce77cdefb`  
		Last Modified: Tue, 11 Jul 2023 05:25:57 GMT  
		Size: 304.2 MB (304236707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc58f6eb776423b78c7a88af6ee221317c44f67e3fb4f413ef3823e8895288a2`  
		Last Modified: Tue, 11 Jul 2023 05:25:43 GMT  
		Size: 2.3 MB (2343673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea5e5502a3de7ec04368cbbb5f6c48f21fc7eac2657e2376ab3c7271ad4f85d`  
		Last Modified: Tue, 11 Jul 2023 05:25:43 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f8adcd32841dea1f4e39476b790a663510401829d69a806cad6007452d0367`  
		Last Modified: Tue, 11 Jul 2023 05:25:43 GMT  
		Size: 2.3 KB (2310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa238d29e18bbc7bdc963a1e1b2680c62ba2df6944ca0da2f99bd14855d1534`  
		Last Modified: Tue, 11 Jul 2023 05:25:43 GMT  
		Size: 6.0 KB (6005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ff1ad0797d8b4bc76bf31cb29679b76b9a9af76a225e434abe3b7d81295b942`  
		Last Modified: Tue, 11 Jul 2023 05:25:43 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:15.5-mariadb-tomcat`

```console
$ docker pull xwiki@sha256:d447b71c1f3084c255c2effee1762e635e6e07f08edcc0bd5b9c46d892350483
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:15.5-mariadb-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:6ece9caf8c15d2557f7f165d530deb3442aae7b1bb3b968ba2236e987cebbe2d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **585.5 MB (585501648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac976c622edabab4c9f4be5e6b071f4be6640e98d657487308bb3bb030921d13`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:37:40 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:37:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:37:42 GMT
ADD file:140fb5108b4a2861b5718ad03b4a5174bba03589ea8d4c053e6a0b282f439ff3 in / 
# Wed, 28 Jun 2023 08:37:42 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:34:07 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:35:02 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 20:35:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 20:35:35 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 08:22:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 08:22:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 08:22:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 08:22:21 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 08:22:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:22:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:25:33 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 08:25:34 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 00:16:15 GMT
COPY dir:8ddeace4a16f09a0d97488e225c7b2e4a48c9a93484d24b46a09759f52800501 in /usr/local/tomcat 
# Tue, 11 Jul 2023 00:16:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 00:16:20 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 00:16:20 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 00:16:20 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 04:40:02 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 04:40:03 GMT
ENV XWIKI_VERSION=15.5
# Tue, 11 Jul 2023 04:40:03 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.5
# Tue, 11 Jul 2023 04:40:03 GMT
ENV XWIKI_DOWNLOAD_SHA256=e552586d371da33b012cfbd974b3ba80d1b147a5c892ad6cf989960212cdaa02
# Tue, 11 Jul 2023 04:40:41 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 04:42:10 GMT
ENV MARIADB_JDBC_VERSION=3.1.4
# Tue, 11 Jul 2023 04:42:10 GMT
ENV MARIADB_JDBC_SHA256=eb88b5d727d82e25117e2b6fabcec1daf734633b0a576456c73215884c189ad4
# Tue, 11 Jul 2023 04:42:10 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.1.4
# Tue, 11 Jul 2023 04:42:10 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.1.4.jar
# Tue, 11 Jul 2023 04:42:10 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.1.4.jar
# Tue, 11 Jul 2023 04:42:11 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Tue, 11 Jul 2023 04:42:11 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 04:42:11 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 04:42:12 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 04:42:12 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 04:42:12 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 04:42:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 04:42:12 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:9d19ee268e0d7bcf6716e6658ee1b0384a71d6f2f9aa1ae2085610cf7c7b316f`  
		Last Modified: Wed, 28 Jun 2023 11:50:41 GMT  
		Size: 30.4 MB (30431229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32db0ad82863deaedd2f9a365e52f595085778d28bd1e6f1d351107590cad806`  
		Last Modified: Tue, 04 Jul 2023 20:39:05 GMT  
		Size: 12.5 MB (12495341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01bb55fbcae928d7e6c08d6618580d2b27ce6e46083f861bbed1e01db41c20b`  
		Last Modified: Tue, 04 Jul 2023 20:41:01 GMT  
		Size: 46.7 MB (46666353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297c6e3f57ee032a3cc5f0fd28b52687129e7a1e6485aea12aff08cb6620071e`  
		Last Modified: Tue, 04 Jul 2023 20:40:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15b01f5ab5b71b356d93dff08f5037af8e8a03b4657f1fd303052261161ebd8`  
		Last Modified: Wed, 05 Jul 2023 08:37:14 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c6051a2b9ffe906ea99b555033966c877468da73cd19fd793c86099d0af531`  
		Last Modified: Tue, 11 Jul 2023 00:38:45 GMT  
		Size: 12.3 MB (12274167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34aaed1f6a3460fc256e262b462c1180ccef1b0665ffd50f900d1ef9c19f1d24`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 454.7 KB (454674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b809bf54ada009dfd91afa6ad239f7a791807f2928941b7f969493ec38246be`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877cc60516baaeb7846bba5d5de9e491d0406cd2f43959d7d4e104d89df5e228`  
		Last Modified: Tue, 11 Jul 2023 04:44:49 GMT  
		Size: 178.3 MB (178335971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b863cfbbf93cec3814eec01a334529779a02fcbb3cdff4e2d212bb70287a5720`  
		Last Modified: Tue, 11 Jul 2023 04:44:42 GMT  
		Size: 304.2 MB (304236736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d9f121998f3ebb1fe9d8b1e2b7964a6e19afe2500ee4c64b95739f1578f0728`  
		Last Modified: Tue, 11 Jul 2023 04:46:03 GMT  
		Size: 594.6 KB (594553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b2c8c7e34dbea6b864808d65dae2a48aaa73e9595b3dd30f14d4b95b28cbcf`  
		Last Modified: Tue, 11 Jul 2023 04:46:03 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84634ee1814641c052e3b568592a22c625bc82aaf05fdb64d6dcbdb17ff803b7`  
		Last Modified: Tue, 11 Jul 2023 04:46:03 GMT  
		Size: 2.3 KB (2311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f62b3d21969533fa11c23f989db62def095f4c38f4e3ebba9bdb897cb756a783`  
		Last Modified: Tue, 11 Jul 2023 04:46:03 GMT  
		Size: 6.0 KB (6003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d136eed865c53c0489a1100cd4c540d7269e0bbc620b8b44fa3c71d168a0e583`  
		Last Modified: Tue, 11 Jul 2023 04:46:03 GMT  
		Size: 2.5 KB (2503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:15.5-mariadb-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:2745b46e135b629961fa0abba943bcd28e8793d51275fbf2d1a945545b31961b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **576.8 MB (576811676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa8facaf677aa5a99371bfdf03feab6977a37475e6664e98cdef94878d40484c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:42:48 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:42:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:42:50 GMT
ADD file:262490f82459c14632f5c9a6d6a5cf6c07b4f307e8fd380fa764662cda46e88f in / 
# Wed, 28 Jun 2023 08:42:50 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:59 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 15:33:41 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 15:34:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 15:34:08 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 02:55:59 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 02:55:59 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 02:55:59 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 02:55:59 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 02:56:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 02:56:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 03:00:51 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 03:00:51 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 01:18:24 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 01:18:25 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 01:18:25 GMT
COPY dir:1743191a9534b9e7d795d3bf9ad18535d99e75967877447e17d7b63574d878d5 in /usr/local/tomcat 
# Tue, 11 Jul 2023 01:18:28 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 01:18:29 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 01:18:29 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 01:18:29 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 05:21:20 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 05:21:23 GMT
ENV XWIKI_VERSION=15.5
# Tue, 11 Jul 2023 05:21:23 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.5
# Tue, 11 Jul 2023 05:21:23 GMT
ENV XWIKI_DOWNLOAD_SHA256=e552586d371da33b012cfbd974b3ba80d1b147a5c892ad6cf989960212cdaa02
# Tue, 11 Jul 2023 05:22:02 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 05:23:36 GMT
ENV MARIADB_JDBC_VERSION=3.1.4
# Tue, 11 Jul 2023 05:23:36 GMT
ENV MARIADB_JDBC_SHA256=eb88b5d727d82e25117e2b6fabcec1daf734633b0a576456c73215884c189ad4
# Tue, 11 Jul 2023 05:23:36 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.1.4
# Tue, 11 Jul 2023 05:23:37 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.1.4.jar
# Tue, 11 Jul 2023 05:23:37 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.1.4.jar
# Tue, 11 Jul 2023 05:23:37 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Tue, 11 Jul 2023 05:23:37 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 05:23:37 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 05:23:38 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 05:23:38 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 05:23:38 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 05:23:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 05:23:38 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:ac34a2e0269ced3acc355be706239ee0f3f1e73a035c40dd2fac74827164ee53`  
		Last Modified: Wed, 28 Jun 2023 23:23:40 GMT  
		Size: 28.4 MB (28391011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d9df805749ad7c4605f0d49a64da6a6173ab190ec361dc2063b6b73af59ab5`  
		Last Modified: Tue, 04 Jul 2023 15:36:55 GMT  
		Size: 12.5 MB (12455497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1e11a5919e5746092b2a288f71090ffdb0d3544b7b54c31ed0137e6d5d4735`  
		Last Modified: Tue, 04 Jul 2023 15:38:37 GMT  
		Size: 45.0 MB (45009079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80987dc89da28aa5ceec7a86ea74e13cee06ecd9304cf4c92d8f382c79eb4f2`  
		Last Modified: Tue, 04 Jul 2023 15:38:32 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de67c7824eef053da628456fe8aba244c4150024af9454dd4091763920d836c`  
		Last Modified: Wed, 05 Jul 2023 03:14:23 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f77f07e56c3d3019cd346deaeacbe572b15b26a924c19b6386877b47123a89e`  
		Last Modified: Tue, 11 Jul 2023 01:39:24 GMT  
		Size: 12.3 MB (12283700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2422cddd65b0ff63d783c999d005c42281720b8615f5872e1e8fdb32dd9981d9`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 455.1 KB (455052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b023f0d964d565a960e567dcaaa605fdff6da02b54971f4d0693506b481b8c`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28177f0763a75e5c940bb6a7919185effccd7cf14c0e350198b3aedbe1db789`  
		Last Modified: Tue, 11 Jul 2023 05:26:01 GMT  
		Size: 173.4 MB (173373450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b39c7f4340aa5dd678a6a0a9bc018229eaadb2a94a0af6bc41d17ce77cdefb`  
		Last Modified: Tue, 11 Jul 2023 05:25:57 GMT  
		Size: 304.2 MB (304236707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0be5f78ca514976c969b47013a6e82418af20d755526a18e35388d7482170b8`  
		Last Modified: Tue, 11 Jul 2023 05:27:14 GMT  
		Size: 594.6 KB (594556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01372195bd2be58e8f5f6433314edfd376c3ce7d69fe9fc1b21188af306f2ce1`  
		Last Modified: Tue, 11 Jul 2023 05:27:14 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15366f793a0d945e4ef67931cb193ae8c2b7f218ecba840af9cf4958adb81ce8`  
		Last Modified: Tue, 11 Jul 2023 05:27:14 GMT  
		Size: 2.3 KB (2312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae0ba8487202e29a15c7c1b505e9f148753e98c7e9284bb88ab357269ef43ab`  
		Last Modified: Tue, 11 Jul 2023 05:27:14 GMT  
		Size: 6.0 KB (6004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4d894785e0d9bda2444090848544b861a5280bd4c8a3e5686acc3d6f3f232fe`  
		Last Modified: Tue, 11 Jul 2023 05:27:14 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:15.5-mysql-tomcat`

```console
$ docker pull xwiki@sha256:66e25eb51a5a079e68e523ac98a46358b70c8c431f4360e1565d23aead7eaa3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:15.5-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:80718cf2818aac2523383b177893d1f4454722abe547ec303a18e3b4a30362b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **587.3 MB (587250774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97a5a7f1172dd3ea626947d13678241c2e0f4e5391c13ab4c32dd3f009d902c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:37:40 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:37:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:37:42 GMT
ADD file:140fb5108b4a2861b5718ad03b4a5174bba03589ea8d4c053e6a0b282f439ff3 in / 
# Wed, 28 Jun 2023 08:37:42 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:34:07 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:35:02 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 20:35:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 20:35:35 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 08:22:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 08:22:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 08:22:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 08:22:21 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 08:22:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:22:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:25:33 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 08:25:34 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 00:16:15 GMT
COPY dir:8ddeace4a16f09a0d97488e225c7b2e4a48c9a93484d24b46a09759f52800501 in /usr/local/tomcat 
# Tue, 11 Jul 2023 00:16:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 00:16:20 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 00:16:20 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 00:16:20 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 04:40:02 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 04:40:03 GMT
ENV XWIKI_VERSION=15.5
# Tue, 11 Jul 2023 04:40:03 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.5
# Tue, 11 Jul 2023 04:40:03 GMT
ENV XWIKI_DOWNLOAD_SHA256=e552586d371da33b012cfbd974b3ba80d1b147a5c892ad6cf989960212cdaa02
# Tue, 11 Jul 2023 04:40:41 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 04:40:42 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Tue, 11 Jul 2023 04:40:42 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Tue, 11 Jul 2023 04:40:42 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Tue, 11 Jul 2023 04:40:42 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 04:40:42 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 04:40:43 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Tue, 11 Jul 2023 04:40:43 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 04:40:43 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 04:40:44 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 04:40:44 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 04:40:44 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 04:40:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 04:40:44 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:9d19ee268e0d7bcf6716e6658ee1b0384a71d6f2f9aa1ae2085610cf7c7b316f`  
		Last Modified: Wed, 28 Jun 2023 11:50:41 GMT  
		Size: 30.4 MB (30431229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32db0ad82863deaedd2f9a365e52f595085778d28bd1e6f1d351107590cad806`  
		Last Modified: Tue, 04 Jul 2023 20:39:05 GMT  
		Size: 12.5 MB (12495341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01bb55fbcae928d7e6c08d6618580d2b27ce6e46083f861bbed1e01db41c20b`  
		Last Modified: Tue, 04 Jul 2023 20:41:01 GMT  
		Size: 46.7 MB (46666353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297c6e3f57ee032a3cc5f0fd28b52687129e7a1e6485aea12aff08cb6620071e`  
		Last Modified: Tue, 04 Jul 2023 20:40:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15b01f5ab5b71b356d93dff08f5037af8e8a03b4657f1fd303052261161ebd8`  
		Last Modified: Wed, 05 Jul 2023 08:37:14 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c6051a2b9ffe906ea99b555033966c877468da73cd19fd793c86099d0af531`  
		Last Modified: Tue, 11 Jul 2023 00:38:45 GMT  
		Size: 12.3 MB (12274167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34aaed1f6a3460fc256e262b462c1180ccef1b0665ffd50f900d1ef9c19f1d24`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 454.7 KB (454674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b809bf54ada009dfd91afa6ad239f7a791807f2928941b7f969493ec38246be`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877cc60516baaeb7846bba5d5de9e491d0406cd2f43959d7d4e104d89df5e228`  
		Last Modified: Tue, 11 Jul 2023 04:44:49 GMT  
		Size: 178.3 MB (178335971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b863cfbbf93cec3814eec01a334529779a02fcbb3cdff4e2d212bb70287a5720`  
		Last Modified: Tue, 11 Jul 2023 04:44:42 GMT  
		Size: 304.2 MB (304236736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faad5f8d2320ee7d3eb3c3f81aff36754d147687cdb520bc8b24d3170bfcee58`  
		Last Modified: Tue, 11 Jul 2023 04:44:25 GMT  
		Size: 2.3 MB (2343679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ad43407c01ec5371102aaa125c19fb5399f629346a71d4913d742cfed44165`  
		Last Modified: Tue, 11 Jul 2023 04:44:24 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03112af3cb3ddf2e651a23fd879dd50f96a17b20d580105c90d7bb357f02ab0a`  
		Last Modified: Tue, 11 Jul 2023 04:44:24 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7098881bee3a8920bec6f5c352be02657d02e5bb3a4ce69faa81f9354193acbf`  
		Last Modified: Tue, 11 Jul 2023 04:44:24 GMT  
		Size: 6.0 KB (6004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:880ec6a5100b3effc0772c9e06afdfdab1786151d59c78eb30826e0245f2ebe5`  
		Last Modified: Tue, 11 Jul 2023 04:44:24 GMT  
		Size: 2.5 KB (2507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:15.5-mysql-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:80454bf7fba586e95357c0d982c52ab2d1504e85c6d085e14a1091a19a0d7e65
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.6 MB (578560793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e24eddde7707953934d4ceba63f6297ff5115dc6ec8e8e39946e4f8bd2542c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:42:48 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:42:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:42:50 GMT
ADD file:262490f82459c14632f5c9a6d6a5cf6c07b4f307e8fd380fa764662cda46e88f in / 
# Wed, 28 Jun 2023 08:42:50 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:59 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 15:33:41 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 15:34:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 15:34:08 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 02:55:59 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 02:55:59 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 02:55:59 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 02:55:59 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 02:56:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 02:56:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 03:00:51 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 03:00:51 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 01:18:24 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 01:18:25 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 01:18:25 GMT
COPY dir:1743191a9534b9e7d795d3bf9ad18535d99e75967877447e17d7b63574d878d5 in /usr/local/tomcat 
# Tue, 11 Jul 2023 01:18:28 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 01:18:29 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 01:18:29 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 01:18:29 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 05:21:20 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 05:21:23 GMT
ENV XWIKI_VERSION=15.5
# Tue, 11 Jul 2023 05:21:23 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.5
# Tue, 11 Jul 2023 05:21:23 GMT
ENV XWIKI_DOWNLOAD_SHA256=e552586d371da33b012cfbd974b3ba80d1b147a5c892ad6cf989960212cdaa02
# Tue, 11 Jul 2023 05:22:02 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 05:22:04 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Tue, 11 Jul 2023 05:22:04 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Tue, 11 Jul 2023 05:22:04 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Tue, 11 Jul 2023 05:22:04 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 05:22:04 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 05:22:05 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Tue, 11 Jul 2023 05:22:06 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 05:22:06 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 05:22:06 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 05:22:06 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 05:22:06 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 05:22:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 05:22:06 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:ac34a2e0269ced3acc355be706239ee0f3f1e73a035c40dd2fac74827164ee53`  
		Last Modified: Wed, 28 Jun 2023 23:23:40 GMT  
		Size: 28.4 MB (28391011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d9df805749ad7c4605f0d49a64da6a6173ab190ec361dc2063b6b73af59ab5`  
		Last Modified: Tue, 04 Jul 2023 15:36:55 GMT  
		Size: 12.5 MB (12455497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1e11a5919e5746092b2a288f71090ffdb0d3544b7b54c31ed0137e6d5d4735`  
		Last Modified: Tue, 04 Jul 2023 15:38:37 GMT  
		Size: 45.0 MB (45009079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80987dc89da28aa5ceec7a86ea74e13cee06ecd9304cf4c92d8f382c79eb4f2`  
		Last Modified: Tue, 04 Jul 2023 15:38:32 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de67c7824eef053da628456fe8aba244c4150024af9454dd4091763920d836c`  
		Last Modified: Wed, 05 Jul 2023 03:14:23 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f77f07e56c3d3019cd346deaeacbe572b15b26a924c19b6386877b47123a89e`  
		Last Modified: Tue, 11 Jul 2023 01:39:24 GMT  
		Size: 12.3 MB (12283700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2422cddd65b0ff63d783c999d005c42281720b8615f5872e1e8fdb32dd9981d9`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 455.1 KB (455052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b023f0d964d565a960e567dcaaa605fdff6da02b54971f4d0693506b481b8c`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28177f0763a75e5c940bb6a7919185effccd7cf14c0e350198b3aedbe1db789`  
		Last Modified: Tue, 11 Jul 2023 05:26:01 GMT  
		Size: 173.4 MB (173373450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b39c7f4340aa5dd678a6a0a9bc018229eaadb2a94a0af6bc41d17ce77cdefb`  
		Last Modified: Tue, 11 Jul 2023 05:25:57 GMT  
		Size: 304.2 MB (304236707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc58f6eb776423b78c7a88af6ee221317c44f67e3fb4f413ef3823e8895288a2`  
		Last Modified: Tue, 11 Jul 2023 05:25:43 GMT  
		Size: 2.3 MB (2343673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea5e5502a3de7ec04368cbbb5f6c48f21fc7eac2657e2376ab3c7271ad4f85d`  
		Last Modified: Tue, 11 Jul 2023 05:25:43 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f8adcd32841dea1f4e39476b790a663510401829d69a806cad6007452d0367`  
		Last Modified: Tue, 11 Jul 2023 05:25:43 GMT  
		Size: 2.3 KB (2310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa238d29e18bbc7bdc963a1e1b2680c62ba2df6944ca0da2f99bd14855d1534`  
		Last Modified: Tue, 11 Jul 2023 05:25:43 GMT  
		Size: 6.0 KB (6005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ff1ad0797d8b4bc76bf31cb29679b76b9a9af76a225e434abe3b7d81295b942`  
		Last Modified: Tue, 11 Jul 2023 05:25:43 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:15.5-postgres-tomcat`

```console
$ docker pull xwiki@sha256:143482a096b13073c1d9d59fde125210cd6009c4fb253a6d30cf5eaf8481fc5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:15.5-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:4741e9d9b24c00013903dbabf718e61ef5c4b23fd41a283067988225a4ea60ae
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **586.8 MB (586784502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1a1f265f59dcb2e5a6888c86ef11b46a92e4d498dcf98b2ab1f05735021fa2a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:37:40 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:37:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:37:42 GMT
ADD file:140fb5108b4a2861b5718ad03b4a5174bba03589ea8d4c053e6a0b282f439ff3 in / 
# Wed, 28 Jun 2023 08:37:42 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:34:07 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:35:02 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 20:35:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 20:35:35 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 08:22:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 08:22:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 08:22:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 08:22:21 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 08:22:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:22:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:25:33 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 08:25:34 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 00:16:15 GMT
COPY dir:8ddeace4a16f09a0d97488e225c7b2e4a48c9a93484d24b46a09759f52800501 in /usr/local/tomcat 
# Tue, 11 Jul 2023 00:16:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 00:16:20 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 00:16:20 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 00:16:20 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 04:41:24 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 04:41:26 GMT
ENV XWIKI_VERSION=15.5
# Tue, 11 Jul 2023 04:41:26 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.5
# Tue, 11 Jul 2023 04:41:26 GMT
ENV XWIKI_DOWNLOAD_SHA256=e552586d371da33b012cfbd974b3ba80d1b147a5c892ad6cf989960212cdaa02
# Tue, 11 Jul 2023 04:42:04 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 04:42:05 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Tue, 11 Jul 2023 04:42:05 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 04:42:05 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 04:42:06 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 04:42:06 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 04:42:06 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 04:42:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 04:42:06 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:9d19ee268e0d7bcf6716e6658ee1b0384a71d6f2f9aa1ae2085610cf7c7b316f`  
		Last Modified: Wed, 28 Jun 2023 11:50:41 GMT  
		Size: 30.4 MB (30431229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32db0ad82863deaedd2f9a365e52f595085778d28bd1e6f1d351107590cad806`  
		Last Modified: Tue, 04 Jul 2023 20:39:05 GMT  
		Size: 12.5 MB (12495341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01bb55fbcae928d7e6c08d6618580d2b27ce6e46083f861bbed1e01db41c20b`  
		Last Modified: Tue, 04 Jul 2023 20:41:01 GMT  
		Size: 46.7 MB (46666353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297c6e3f57ee032a3cc5f0fd28b52687129e7a1e6485aea12aff08cb6620071e`  
		Last Modified: Tue, 04 Jul 2023 20:40:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15b01f5ab5b71b356d93dff08f5037af8e8a03b4657f1fd303052261161ebd8`  
		Last Modified: Wed, 05 Jul 2023 08:37:14 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c6051a2b9ffe906ea99b555033966c877468da73cd19fd793c86099d0af531`  
		Last Modified: Tue, 11 Jul 2023 00:38:45 GMT  
		Size: 12.3 MB (12274167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34aaed1f6a3460fc256e262b462c1180ccef1b0665ffd50f900d1ef9c19f1d24`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 454.7 KB (454674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b809bf54ada009dfd91afa6ad239f7a791807f2928941b7f969493ec38246be`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bd305e7867896df13faced03525a0f25bf1ac1b2a2c93e60382cdfd41c08e16`  
		Last Modified: Tue, 11 Jul 2023 04:45:43 GMT  
		Size: 179.3 MB (179276407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35bfb758076cf011f5df9081f31dfbcf656cd98cd11b65f53f3684ec1e485c8f`  
		Last Modified: Tue, 11 Jul 2023 04:45:37 GMT  
		Size: 304.2 MB (304236708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2f8ccc8af30dd82bb4657bfdb7193ed23e8dc8823df1eaea8b1c8e4ab85d60`  
		Last Modified: Tue, 11 Jul 2023 04:45:20 GMT  
		Size: 936.8 KB (936849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:822e7d00d75f2a5b9a34edd0741b7e19410deb191f96800278c2921b043c81cb`  
		Last Modified: Tue, 11 Jul 2023 04:45:19 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba3137d80fef0218e2aaa65df38833a3e9d79b0d6e0b8d441376edbc36190ab`  
		Last Modified: Tue, 11 Jul 2023 04:45:19 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d02045e3c19030183c43f79b2c5e3a2f244dda96d11e96014e91d90e85f6e3a9`  
		Last Modified: Tue, 11 Jul 2023 04:45:19 GMT  
		Size: 6.0 KB (6006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91afad54a0c6d44f603953379c22801e4dbc9f2c282eaa00e94946d1d77dc3a4`  
		Last Modified: Tue, 11 Jul 2023 04:45:19 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:15.5-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:30799eeac6bc3f0efeefaf95f4161eeea6298cf60983391d2b7789735d58fa07
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.1 MB (578094027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc026cfcc219f16306961c1815044f7a63d5f49577815243d20c27d2d823d48`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:42:48 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:42:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:42:50 GMT
ADD file:262490f82459c14632f5c9a6d6a5cf6c07b4f307e8fd380fa764662cda46e88f in / 
# Wed, 28 Jun 2023 08:42:50 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:59 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 15:33:41 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 15:34:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 15:34:08 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 02:55:59 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 02:55:59 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 02:55:59 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 02:55:59 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 02:56:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 02:56:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 03:00:51 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 03:00:51 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 01:18:24 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 01:18:25 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 01:18:25 GMT
COPY dir:1743191a9534b9e7d795d3bf9ad18535d99e75967877447e17d7b63574d878d5 in /usr/local/tomcat 
# Tue, 11 Jul 2023 01:18:28 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 01:18:29 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 01:18:29 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 01:18:29 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 05:22:36 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 05:22:39 GMT
ENV XWIKI_VERSION=15.5
# Tue, 11 Jul 2023 05:22:39 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.5
# Tue, 11 Jul 2023 05:22:39 GMT
ENV XWIKI_DOWNLOAD_SHA256=e552586d371da33b012cfbd974b3ba80d1b147a5c892ad6cf989960212cdaa02
# Tue, 11 Jul 2023 05:23:18 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 05:23:21 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Tue, 11 Jul 2023 05:23:21 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 05:23:21 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 05:23:22 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 05:23:22 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 05:23:22 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 05:23:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 05:23:22 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:ac34a2e0269ced3acc355be706239ee0f3f1e73a035c40dd2fac74827164ee53`  
		Last Modified: Wed, 28 Jun 2023 23:23:40 GMT  
		Size: 28.4 MB (28391011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d9df805749ad7c4605f0d49a64da6a6173ab190ec361dc2063b6b73af59ab5`  
		Last Modified: Tue, 04 Jul 2023 15:36:55 GMT  
		Size: 12.5 MB (12455497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1e11a5919e5746092b2a288f71090ffdb0d3544b7b54c31ed0137e6d5d4735`  
		Last Modified: Tue, 04 Jul 2023 15:38:37 GMT  
		Size: 45.0 MB (45009079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80987dc89da28aa5ceec7a86ea74e13cee06ecd9304cf4c92d8f382c79eb4f2`  
		Last Modified: Tue, 04 Jul 2023 15:38:32 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de67c7824eef053da628456fe8aba244c4150024af9454dd4091763920d836c`  
		Last Modified: Wed, 05 Jul 2023 03:14:23 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f77f07e56c3d3019cd346deaeacbe572b15b26a924c19b6386877b47123a89e`  
		Last Modified: Tue, 11 Jul 2023 01:39:24 GMT  
		Size: 12.3 MB (12283700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2422cddd65b0ff63d783c999d005c42281720b8615f5872e1e8fdb32dd9981d9`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 455.1 KB (455052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b023f0d964d565a960e567dcaaa605fdff6da02b54971f4d0693506b481b8c`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:968d46d099e01403854799f31b6235698a474c27fd58b0172b1eb3889cd5067f`  
		Last Modified: Tue, 11 Jul 2023 05:26:50 GMT  
		Size: 174.3 MB (174313369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2894444c04152ca46b568422ea482a66ed3763028ff87cc82d80132ea0e4cdd`  
		Last Modified: Tue, 11 Jul 2023 05:26:46 GMT  
		Size: 304.2 MB (304236690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77118bb73ac2d6b789413d31beabdbb72e88543cca5b3e6406076fd10d40d8d3`  
		Last Modified: Tue, 11 Jul 2023 05:26:32 GMT  
		Size: 936.9 KB (936852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9eb9df1942e9402403596582620c7fb14dbdd8e12de634c88e080cc5795a812`  
		Last Modified: Tue, 11 Jul 2023 05:26:32 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d23fb311f1a568af6e8b96dcb8cfb10d4d96a88aee4243256a3e73f4727fa318`  
		Last Modified: Tue, 11 Jul 2023 05:26:32 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dd3c555379bf5bd7f8d13501bb806b6b5ffb4c2ecb169ce4485f1cbf0d26b9a`  
		Last Modified: Tue, 11 Jul 2023 05:26:32 GMT  
		Size: 6.0 KB (6006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8254381348a57ea56306a83d8f2a89630202f393f54d6102b5652be9cfa10f8f`  
		Last Modified: Tue, 11 Jul 2023 05:26:33 GMT  
		Size: 2.5 KB (2507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:15.5.0`

```console
$ docker pull xwiki@sha256:66e25eb51a5a079e68e523ac98a46358b70c8c431f4360e1565d23aead7eaa3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:15.5.0` - linux; amd64

```console
$ docker pull xwiki@sha256:80718cf2818aac2523383b177893d1f4454722abe547ec303a18e3b4a30362b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **587.3 MB (587250774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97a5a7f1172dd3ea626947d13678241c2e0f4e5391c13ab4c32dd3f009d902c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:37:40 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:37:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:37:42 GMT
ADD file:140fb5108b4a2861b5718ad03b4a5174bba03589ea8d4c053e6a0b282f439ff3 in / 
# Wed, 28 Jun 2023 08:37:42 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:34:07 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:35:02 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 20:35:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 20:35:35 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 08:22:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 08:22:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 08:22:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 08:22:21 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 08:22:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:22:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:25:33 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 08:25:34 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 00:16:15 GMT
COPY dir:8ddeace4a16f09a0d97488e225c7b2e4a48c9a93484d24b46a09759f52800501 in /usr/local/tomcat 
# Tue, 11 Jul 2023 00:16:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 00:16:20 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 00:16:20 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 00:16:20 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 04:40:02 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 04:40:03 GMT
ENV XWIKI_VERSION=15.5
# Tue, 11 Jul 2023 04:40:03 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.5
# Tue, 11 Jul 2023 04:40:03 GMT
ENV XWIKI_DOWNLOAD_SHA256=e552586d371da33b012cfbd974b3ba80d1b147a5c892ad6cf989960212cdaa02
# Tue, 11 Jul 2023 04:40:41 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 04:40:42 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Tue, 11 Jul 2023 04:40:42 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Tue, 11 Jul 2023 04:40:42 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Tue, 11 Jul 2023 04:40:42 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 04:40:42 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 04:40:43 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Tue, 11 Jul 2023 04:40:43 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 04:40:43 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 04:40:44 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 04:40:44 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 04:40:44 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 04:40:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 04:40:44 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:9d19ee268e0d7bcf6716e6658ee1b0384a71d6f2f9aa1ae2085610cf7c7b316f`  
		Last Modified: Wed, 28 Jun 2023 11:50:41 GMT  
		Size: 30.4 MB (30431229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32db0ad82863deaedd2f9a365e52f595085778d28bd1e6f1d351107590cad806`  
		Last Modified: Tue, 04 Jul 2023 20:39:05 GMT  
		Size: 12.5 MB (12495341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01bb55fbcae928d7e6c08d6618580d2b27ce6e46083f861bbed1e01db41c20b`  
		Last Modified: Tue, 04 Jul 2023 20:41:01 GMT  
		Size: 46.7 MB (46666353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297c6e3f57ee032a3cc5f0fd28b52687129e7a1e6485aea12aff08cb6620071e`  
		Last Modified: Tue, 04 Jul 2023 20:40:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15b01f5ab5b71b356d93dff08f5037af8e8a03b4657f1fd303052261161ebd8`  
		Last Modified: Wed, 05 Jul 2023 08:37:14 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c6051a2b9ffe906ea99b555033966c877468da73cd19fd793c86099d0af531`  
		Last Modified: Tue, 11 Jul 2023 00:38:45 GMT  
		Size: 12.3 MB (12274167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34aaed1f6a3460fc256e262b462c1180ccef1b0665ffd50f900d1ef9c19f1d24`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 454.7 KB (454674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b809bf54ada009dfd91afa6ad239f7a791807f2928941b7f969493ec38246be`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877cc60516baaeb7846bba5d5de9e491d0406cd2f43959d7d4e104d89df5e228`  
		Last Modified: Tue, 11 Jul 2023 04:44:49 GMT  
		Size: 178.3 MB (178335971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b863cfbbf93cec3814eec01a334529779a02fcbb3cdff4e2d212bb70287a5720`  
		Last Modified: Tue, 11 Jul 2023 04:44:42 GMT  
		Size: 304.2 MB (304236736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faad5f8d2320ee7d3eb3c3f81aff36754d147687cdb520bc8b24d3170bfcee58`  
		Last Modified: Tue, 11 Jul 2023 04:44:25 GMT  
		Size: 2.3 MB (2343679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ad43407c01ec5371102aaa125c19fb5399f629346a71d4913d742cfed44165`  
		Last Modified: Tue, 11 Jul 2023 04:44:24 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03112af3cb3ddf2e651a23fd879dd50f96a17b20d580105c90d7bb357f02ab0a`  
		Last Modified: Tue, 11 Jul 2023 04:44:24 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7098881bee3a8920bec6f5c352be02657d02e5bb3a4ce69faa81f9354193acbf`  
		Last Modified: Tue, 11 Jul 2023 04:44:24 GMT  
		Size: 6.0 KB (6004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:880ec6a5100b3effc0772c9e06afdfdab1786151d59c78eb30826e0245f2ebe5`  
		Last Modified: Tue, 11 Jul 2023 04:44:24 GMT  
		Size: 2.5 KB (2507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:15.5.0` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:80454bf7fba586e95357c0d982c52ab2d1504e85c6d085e14a1091a19a0d7e65
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.6 MB (578560793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e24eddde7707953934d4ceba63f6297ff5115dc6ec8e8e39946e4f8bd2542c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:42:48 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:42:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:42:50 GMT
ADD file:262490f82459c14632f5c9a6d6a5cf6c07b4f307e8fd380fa764662cda46e88f in / 
# Wed, 28 Jun 2023 08:42:50 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:59 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 15:33:41 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 15:34:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 15:34:08 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 02:55:59 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 02:55:59 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 02:55:59 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 02:55:59 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 02:56:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 02:56:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 03:00:51 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 03:00:51 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 01:18:24 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 01:18:25 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 01:18:25 GMT
COPY dir:1743191a9534b9e7d795d3bf9ad18535d99e75967877447e17d7b63574d878d5 in /usr/local/tomcat 
# Tue, 11 Jul 2023 01:18:28 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 01:18:29 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 01:18:29 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 01:18:29 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 05:21:20 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 05:21:23 GMT
ENV XWIKI_VERSION=15.5
# Tue, 11 Jul 2023 05:21:23 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.5
# Tue, 11 Jul 2023 05:21:23 GMT
ENV XWIKI_DOWNLOAD_SHA256=e552586d371da33b012cfbd974b3ba80d1b147a5c892ad6cf989960212cdaa02
# Tue, 11 Jul 2023 05:22:02 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 05:22:04 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Tue, 11 Jul 2023 05:22:04 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Tue, 11 Jul 2023 05:22:04 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Tue, 11 Jul 2023 05:22:04 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 05:22:04 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 05:22:05 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Tue, 11 Jul 2023 05:22:06 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 05:22:06 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 05:22:06 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 05:22:06 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 05:22:06 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 05:22:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 05:22:06 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:ac34a2e0269ced3acc355be706239ee0f3f1e73a035c40dd2fac74827164ee53`  
		Last Modified: Wed, 28 Jun 2023 23:23:40 GMT  
		Size: 28.4 MB (28391011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d9df805749ad7c4605f0d49a64da6a6173ab190ec361dc2063b6b73af59ab5`  
		Last Modified: Tue, 04 Jul 2023 15:36:55 GMT  
		Size: 12.5 MB (12455497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1e11a5919e5746092b2a288f71090ffdb0d3544b7b54c31ed0137e6d5d4735`  
		Last Modified: Tue, 04 Jul 2023 15:38:37 GMT  
		Size: 45.0 MB (45009079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80987dc89da28aa5ceec7a86ea74e13cee06ecd9304cf4c92d8f382c79eb4f2`  
		Last Modified: Tue, 04 Jul 2023 15:38:32 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de67c7824eef053da628456fe8aba244c4150024af9454dd4091763920d836c`  
		Last Modified: Wed, 05 Jul 2023 03:14:23 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f77f07e56c3d3019cd346deaeacbe572b15b26a924c19b6386877b47123a89e`  
		Last Modified: Tue, 11 Jul 2023 01:39:24 GMT  
		Size: 12.3 MB (12283700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2422cddd65b0ff63d783c999d005c42281720b8615f5872e1e8fdb32dd9981d9`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 455.1 KB (455052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b023f0d964d565a960e567dcaaa605fdff6da02b54971f4d0693506b481b8c`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28177f0763a75e5c940bb6a7919185effccd7cf14c0e350198b3aedbe1db789`  
		Last Modified: Tue, 11 Jul 2023 05:26:01 GMT  
		Size: 173.4 MB (173373450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b39c7f4340aa5dd678a6a0a9bc018229eaadb2a94a0af6bc41d17ce77cdefb`  
		Last Modified: Tue, 11 Jul 2023 05:25:57 GMT  
		Size: 304.2 MB (304236707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc58f6eb776423b78c7a88af6ee221317c44f67e3fb4f413ef3823e8895288a2`  
		Last Modified: Tue, 11 Jul 2023 05:25:43 GMT  
		Size: 2.3 MB (2343673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea5e5502a3de7ec04368cbbb5f6c48f21fc7eac2657e2376ab3c7271ad4f85d`  
		Last Modified: Tue, 11 Jul 2023 05:25:43 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f8adcd32841dea1f4e39476b790a663510401829d69a806cad6007452d0367`  
		Last Modified: Tue, 11 Jul 2023 05:25:43 GMT  
		Size: 2.3 KB (2310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa238d29e18bbc7bdc963a1e1b2680c62ba2df6944ca0da2f99bd14855d1534`  
		Last Modified: Tue, 11 Jul 2023 05:25:43 GMT  
		Size: 6.0 KB (6005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ff1ad0797d8b4bc76bf31cb29679b76b9a9af76a225e434abe3b7d81295b942`  
		Last Modified: Tue, 11 Jul 2023 05:25:43 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:15.5.0-mariadb-tomcat`

```console
$ docker pull xwiki@sha256:d447b71c1f3084c255c2effee1762e635e6e07f08edcc0bd5b9c46d892350483
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:15.5.0-mariadb-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:6ece9caf8c15d2557f7f165d530deb3442aae7b1bb3b968ba2236e987cebbe2d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **585.5 MB (585501648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac976c622edabab4c9f4be5e6b071f4be6640e98d657487308bb3bb030921d13`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:37:40 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:37:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:37:42 GMT
ADD file:140fb5108b4a2861b5718ad03b4a5174bba03589ea8d4c053e6a0b282f439ff3 in / 
# Wed, 28 Jun 2023 08:37:42 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:34:07 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:35:02 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 20:35:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 20:35:35 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 08:22:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 08:22:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 08:22:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 08:22:21 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 08:22:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:22:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:25:33 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 08:25:34 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 00:16:15 GMT
COPY dir:8ddeace4a16f09a0d97488e225c7b2e4a48c9a93484d24b46a09759f52800501 in /usr/local/tomcat 
# Tue, 11 Jul 2023 00:16:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 00:16:20 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 00:16:20 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 00:16:20 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 04:40:02 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 04:40:03 GMT
ENV XWIKI_VERSION=15.5
# Tue, 11 Jul 2023 04:40:03 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.5
# Tue, 11 Jul 2023 04:40:03 GMT
ENV XWIKI_DOWNLOAD_SHA256=e552586d371da33b012cfbd974b3ba80d1b147a5c892ad6cf989960212cdaa02
# Tue, 11 Jul 2023 04:40:41 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 04:42:10 GMT
ENV MARIADB_JDBC_VERSION=3.1.4
# Tue, 11 Jul 2023 04:42:10 GMT
ENV MARIADB_JDBC_SHA256=eb88b5d727d82e25117e2b6fabcec1daf734633b0a576456c73215884c189ad4
# Tue, 11 Jul 2023 04:42:10 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.1.4
# Tue, 11 Jul 2023 04:42:10 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.1.4.jar
# Tue, 11 Jul 2023 04:42:10 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.1.4.jar
# Tue, 11 Jul 2023 04:42:11 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Tue, 11 Jul 2023 04:42:11 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 04:42:11 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 04:42:12 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 04:42:12 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 04:42:12 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 04:42:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 04:42:12 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:9d19ee268e0d7bcf6716e6658ee1b0384a71d6f2f9aa1ae2085610cf7c7b316f`  
		Last Modified: Wed, 28 Jun 2023 11:50:41 GMT  
		Size: 30.4 MB (30431229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32db0ad82863deaedd2f9a365e52f595085778d28bd1e6f1d351107590cad806`  
		Last Modified: Tue, 04 Jul 2023 20:39:05 GMT  
		Size: 12.5 MB (12495341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01bb55fbcae928d7e6c08d6618580d2b27ce6e46083f861bbed1e01db41c20b`  
		Last Modified: Tue, 04 Jul 2023 20:41:01 GMT  
		Size: 46.7 MB (46666353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297c6e3f57ee032a3cc5f0fd28b52687129e7a1e6485aea12aff08cb6620071e`  
		Last Modified: Tue, 04 Jul 2023 20:40:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15b01f5ab5b71b356d93dff08f5037af8e8a03b4657f1fd303052261161ebd8`  
		Last Modified: Wed, 05 Jul 2023 08:37:14 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c6051a2b9ffe906ea99b555033966c877468da73cd19fd793c86099d0af531`  
		Last Modified: Tue, 11 Jul 2023 00:38:45 GMT  
		Size: 12.3 MB (12274167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34aaed1f6a3460fc256e262b462c1180ccef1b0665ffd50f900d1ef9c19f1d24`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 454.7 KB (454674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b809bf54ada009dfd91afa6ad239f7a791807f2928941b7f969493ec38246be`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877cc60516baaeb7846bba5d5de9e491d0406cd2f43959d7d4e104d89df5e228`  
		Last Modified: Tue, 11 Jul 2023 04:44:49 GMT  
		Size: 178.3 MB (178335971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b863cfbbf93cec3814eec01a334529779a02fcbb3cdff4e2d212bb70287a5720`  
		Last Modified: Tue, 11 Jul 2023 04:44:42 GMT  
		Size: 304.2 MB (304236736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d9f121998f3ebb1fe9d8b1e2b7964a6e19afe2500ee4c64b95739f1578f0728`  
		Last Modified: Tue, 11 Jul 2023 04:46:03 GMT  
		Size: 594.6 KB (594553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b2c8c7e34dbea6b864808d65dae2a48aaa73e9595b3dd30f14d4b95b28cbcf`  
		Last Modified: Tue, 11 Jul 2023 04:46:03 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84634ee1814641c052e3b568592a22c625bc82aaf05fdb64d6dcbdb17ff803b7`  
		Last Modified: Tue, 11 Jul 2023 04:46:03 GMT  
		Size: 2.3 KB (2311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f62b3d21969533fa11c23f989db62def095f4c38f4e3ebba9bdb897cb756a783`  
		Last Modified: Tue, 11 Jul 2023 04:46:03 GMT  
		Size: 6.0 KB (6003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d136eed865c53c0489a1100cd4c540d7269e0bbc620b8b44fa3c71d168a0e583`  
		Last Modified: Tue, 11 Jul 2023 04:46:03 GMT  
		Size: 2.5 KB (2503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:15.5.0-mariadb-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:2745b46e135b629961fa0abba943bcd28e8793d51275fbf2d1a945545b31961b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **576.8 MB (576811676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa8facaf677aa5a99371bfdf03feab6977a37475e6664e98cdef94878d40484c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:42:48 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:42:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:42:50 GMT
ADD file:262490f82459c14632f5c9a6d6a5cf6c07b4f307e8fd380fa764662cda46e88f in / 
# Wed, 28 Jun 2023 08:42:50 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:59 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 15:33:41 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 15:34:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 15:34:08 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 02:55:59 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 02:55:59 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 02:55:59 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 02:55:59 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 02:56:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 02:56:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 03:00:51 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 03:00:51 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 01:18:24 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 01:18:25 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 01:18:25 GMT
COPY dir:1743191a9534b9e7d795d3bf9ad18535d99e75967877447e17d7b63574d878d5 in /usr/local/tomcat 
# Tue, 11 Jul 2023 01:18:28 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 01:18:29 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 01:18:29 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 01:18:29 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 05:21:20 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 05:21:23 GMT
ENV XWIKI_VERSION=15.5
# Tue, 11 Jul 2023 05:21:23 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.5
# Tue, 11 Jul 2023 05:21:23 GMT
ENV XWIKI_DOWNLOAD_SHA256=e552586d371da33b012cfbd974b3ba80d1b147a5c892ad6cf989960212cdaa02
# Tue, 11 Jul 2023 05:22:02 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 05:23:36 GMT
ENV MARIADB_JDBC_VERSION=3.1.4
# Tue, 11 Jul 2023 05:23:36 GMT
ENV MARIADB_JDBC_SHA256=eb88b5d727d82e25117e2b6fabcec1daf734633b0a576456c73215884c189ad4
# Tue, 11 Jul 2023 05:23:36 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.1.4
# Tue, 11 Jul 2023 05:23:37 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.1.4.jar
# Tue, 11 Jul 2023 05:23:37 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.1.4.jar
# Tue, 11 Jul 2023 05:23:37 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Tue, 11 Jul 2023 05:23:37 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 05:23:37 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 05:23:38 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 05:23:38 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 05:23:38 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 05:23:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 05:23:38 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:ac34a2e0269ced3acc355be706239ee0f3f1e73a035c40dd2fac74827164ee53`  
		Last Modified: Wed, 28 Jun 2023 23:23:40 GMT  
		Size: 28.4 MB (28391011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d9df805749ad7c4605f0d49a64da6a6173ab190ec361dc2063b6b73af59ab5`  
		Last Modified: Tue, 04 Jul 2023 15:36:55 GMT  
		Size: 12.5 MB (12455497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1e11a5919e5746092b2a288f71090ffdb0d3544b7b54c31ed0137e6d5d4735`  
		Last Modified: Tue, 04 Jul 2023 15:38:37 GMT  
		Size: 45.0 MB (45009079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80987dc89da28aa5ceec7a86ea74e13cee06ecd9304cf4c92d8f382c79eb4f2`  
		Last Modified: Tue, 04 Jul 2023 15:38:32 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de67c7824eef053da628456fe8aba244c4150024af9454dd4091763920d836c`  
		Last Modified: Wed, 05 Jul 2023 03:14:23 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f77f07e56c3d3019cd346deaeacbe572b15b26a924c19b6386877b47123a89e`  
		Last Modified: Tue, 11 Jul 2023 01:39:24 GMT  
		Size: 12.3 MB (12283700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2422cddd65b0ff63d783c999d005c42281720b8615f5872e1e8fdb32dd9981d9`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 455.1 KB (455052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b023f0d964d565a960e567dcaaa605fdff6da02b54971f4d0693506b481b8c`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28177f0763a75e5c940bb6a7919185effccd7cf14c0e350198b3aedbe1db789`  
		Last Modified: Tue, 11 Jul 2023 05:26:01 GMT  
		Size: 173.4 MB (173373450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b39c7f4340aa5dd678a6a0a9bc018229eaadb2a94a0af6bc41d17ce77cdefb`  
		Last Modified: Tue, 11 Jul 2023 05:25:57 GMT  
		Size: 304.2 MB (304236707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0be5f78ca514976c969b47013a6e82418af20d755526a18e35388d7482170b8`  
		Last Modified: Tue, 11 Jul 2023 05:27:14 GMT  
		Size: 594.6 KB (594556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01372195bd2be58e8f5f6433314edfd376c3ce7d69fe9fc1b21188af306f2ce1`  
		Last Modified: Tue, 11 Jul 2023 05:27:14 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15366f793a0d945e4ef67931cb193ae8c2b7f218ecba840af9cf4958adb81ce8`  
		Last Modified: Tue, 11 Jul 2023 05:27:14 GMT  
		Size: 2.3 KB (2312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae0ba8487202e29a15c7c1b505e9f148753e98c7e9284bb88ab357269ef43ab`  
		Last Modified: Tue, 11 Jul 2023 05:27:14 GMT  
		Size: 6.0 KB (6004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4d894785e0d9bda2444090848544b861a5280bd4c8a3e5686acc3d6f3f232fe`  
		Last Modified: Tue, 11 Jul 2023 05:27:14 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:15.5.0-mysql-tomcat`

```console
$ docker pull xwiki@sha256:66e25eb51a5a079e68e523ac98a46358b70c8c431f4360e1565d23aead7eaa3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:15.5.0-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:80718cf2818aac2523383b177893d1f4454722abe547ec303a18e3b4a30362b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **587.3 MB (587250774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97a5a7f1172dd3ea626947d13678241c2e0f4e5391c13ab4c32dd3f009d902c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:37:40 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:37:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:37:42 GMT
ADD file:140fb5108b4a2861b5718ad03b4a5174bba03589ea8d4c053e6a0b282f439ff3 in / 
# Wed, 28 Jun 2023 08:37:42 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:34:07 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:35:02 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 20:35:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 20:35:35 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 08:22:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 08:22:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 08:22:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 08:22:21 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 08:22:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:22:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:25:33 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 08:25:34 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 00:16:15 GMT
COPY dir:8ddeace4a16f09a0d97488e225c7b2e4a48c9a93484d24b46a09759f52800501 in /usr/local/tomcat 
# Tue, 11 Jul 2023 00:16:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 00:16:20 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 00:16:20 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 00:16:20 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 04:40:02 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 04:40:03 GMT
ENV XWIKI_VERSION=15.5
# Tue, 11 Jul 2023 04:40:03 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.5
# Tue, 11 Jul 2023 04:40:03 GMT
ENV XWIKI_DOWNLOAD_SHA256=e552586d371da33b012cfbd974b3ba80d1b147a5c892ad6cf989960212cdaa02
# Tue, 11 Jul 2023 04:40:41 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 04:40:42 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Tue, 11 Jul 2023 04:40:42 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Tue, 11 Jul 2023 04:40:42 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Tue, 11 Jul 2023 04:40:42 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 04:40:42 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 04:40:43 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Tue, 11 Jul 2023 04:40:43 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 04:40:43 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 04:40:44 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 04:40:44 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 04:40:44 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 04:40:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 04:40:44 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:9d19ee268e0d7bcf6716e6658ee1b0384a71d6f2f9aa1ae2085610cf7c7b316f`  
		Last Modified: Wed, 28 Jun 2023 11:50:41 GMT  
		Size: 30.4 MB (30431229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32db0ad82863deaedd2f9a365e52f595085778d28bd1e6f1d351107590cad806`  
		Last Modified: Tue, 04 Jul 2023 20:39:05 GMT  
		Size: 12.5 MB (12495341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01bb55fbcae928d7e6c08d6618580d2b27ce6e46083f861bbed1e01db41c20b`  
		Last Modified: Tue, 04 Jul 2023 20:41:01 GMT  
		Size: 46.7 MB (46666353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297c6e3f57ee032a3cc5f0fd28b52687129e7a1e6485aea12aff08cb6620071e`  
		Last Modified: Tue, 04 Jul 2023 20:40:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15b01f5ab5b71b356d93dff08f5037af8e8a03b4657f1fd303052261161ebd8`  
		Last Modified: Wed, 05 Jul 2023 08:37:14 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c6051a2b9ffe906ea99b555033966c877468da73cd19fd793c86099d0af531`  
		Last Modified: Tue, 11 Jul 2023 00:38:45 GMT  
		Size: 12.3 MB (12274167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34aaed1f6a3460fc256e262b462c1180ccef1b0665ffd50f900d1ef9c19f1d24`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 454.7 KB (454674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b809bf54ada009dfd91afa6ad239f7a791807f2928941b7f969493ec38246be`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877cc60516baaeb7846bba5d5de9e491d0406cd2f43959d7d4e104d89df5e228`  
		Last Modified: Tue, 11 Jul 2023 04:44:49 GMT  
		Size: 178.3 MB (178335971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b863cfbbf93cec3814eec01a334529779a02fcbb3cdff4e2d212bb70287a5720`  
		Last Modified: Tue, 11 Jul 2023 04:44:42 GMT  
		Size: 304.2 MB (304236736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faad5f8d2320ee7d3eb3c3f81aff36754d147687cdb520bc8b24d3170bfcee58`  
		Last Modified: Tue, 11 Jul 2023 04:44:25 GMT  
		Size: 2.3 MB (2343679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ad43407c01ec5371102aaa125c19fb5399f629346a71d4913d742cfed44165`  
		Last Modified: Tue, 11 Jul 2023 04:44:24 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03112af3cb3ddf2e651a23fd879dd50f96a17b20d580105c90d7bb357f02ab0a`  
		Last Modified: Tue, 11 Jul 2023 04:44:24 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7098881bee3a8920bec6f5c352be02657d02e5bb3a4ce69faa81f9354193acbf`  
		Last Modified: Tue, 11 Jul 2023 04:44:24 GMT  
		Size: 6.0 KB (6004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:880ec6a5100b3effc0772c9e06afdfdab1786151d59c78eb30826e0245f2ebe5`  
		Last Modified: Tue, 11 Jul 2023 04:44:24 GMT  
		Size: 2.5 KB (2507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:15.5.0-mysql-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:80454bf7fba586e95357c0d982c52ab2d1504e85c6d085e14a1091a19a0d7e65
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.6 MB (578560793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e24eddde7707953934d4ceba63f6297ff5115dc6ec8e8e39946e4f8bd2542c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:42:48 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:42:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:42:50 GMT
ADD file:262490f82459c14632f5c9a6d6a5cf6c07b4f307e8fd380fa764662cda46e88f in / 
# Wed, 28 Jun 2023 08:42:50 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:59 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 15:33:41 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 15:34:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 15:34:08 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 02:55:59 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 02:55:59 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 02:55:59 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 02:55:59 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 02:56:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 02:56:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 03:00:51 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 03:00:51 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 01:18:24 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 01:18:25 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 01:18:25 GMT
COPY dir:1743191a9534b9e7d795d3bf9ad18535d99e75967877447e17d7b63574d878d5 in /usr/local/tomcat 
# Tue, 11 Jul 2023 01:18:28 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 01:18:29 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 01:18:29 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 01:18:29 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 05:21:20 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 05:21:23 GMT
ENV XWIKI_VERSION=15.5
# Tue, 11 Jul 2023 05:21:23 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.5
# Tue, 11 Jul 2023 05:21:23 GMT
ENV XWIKI_DOWNLOAD_SHA256=e552586d371da33b012cfbd974b3ba80d1b147a5c892ad6cf989960212cdaa02
# Tue, 11 Jul 2023 05:22:02 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 05:22:04 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Tue, 11 Jul 2023 05:22:04 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Tue, 11 Jul 2023 05:22:04 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Tue, 11 Jul 2023 05:22:04 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 05:22:04 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 05:22:05 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Tue, 11 Jul 2023 05:22:06 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 05:22:06 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 05:22:06 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 05:22:06 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 05:22:06 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 05:22:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 05:22:06 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:ac34a2e0269ced3acc355be706239ee0f3f1e73a035c40dd2fac74827164ee53`  
		Last Modified: Wed, 28 Jun 2023 23:23:40 GMT  
		Size: 28.4 MB (28391011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d9df805749ad7c4605f0d49a64da6a6173ab190ec361dc2063b6b73af59ab5`  
		Last Modified: Tue, 04 Jul 2023 15:36:55 GMT  
		Size: 12.5 MB (12455497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1e11a5919e5746092b2a288f71090ffdb0d3544b7b54c31ed0137e6d5d4735`  
		Last Modified: Tue, 04 Jul 2023 15:38:37 GMT  
		Size: 45.0 MB (45009079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80987dc89da28aa5ceec7a86ea74e13cee06ecd9304cf4c92d8f382c79eb4f2`  
		Last Modified: Tue, 04 Jul 2023 15:38:32 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de67c7824eef053da628456fe8aba244c4150024af9454dd4091763920d836c`  
		Last Modified: Wed, 05 Jul 2023 03:14:23 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f77f07e56c3d3019cd346deaeacbe572b15b26a924c19b6386877b47123a89e`  
		Last Modified: Tue, 11 Jul 2023 01:39:24 GMT  
		Size: 12.3 MB (12283700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2422cddd65b0ff63d783c999d005c42281720b8615f5872e1e8fdb32dd9981d9`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 455.1 KB (455052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b023f0d964d565a960e567dcaaa605fdff6da02b54971f4d0693506b481b8c`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28177f0763a75e5c940bb6a7919185effccd7cf14c0e350198b3aedbe1db789`  
		Last Modified: Tue, 11 Jul 2023 05:26:01 GMT  
		Size: 173.4 MB (173373450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b39c7f4340aa5dd678a6a0a9bc018229eaadb2a94a0af6bc41d17ce77cdefb`  
		Last Modified: Tue, 11 Jul 2023 05:25:57 GMT  
		Size: 304.2 MB (304236707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc58f6eb776423b78c7a88af6ee221317c44f67e3fb4f413ef3823e8895288a2`  
		Last Modified: Tue, 11 Jul 2023 05:25:43 GMT  
		Size: 2.3 MB (2343673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea5e5502a3de7ec04368cbbb5f6c48f21fc7eac2657e2376ab3c7271ad4f85d`  
		Last Modified: Tue, 11 Jul 2023 05:25:43 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f8adcd32841dea1f4e39476b790a663510401829d69a806cad6007452d0367`  
		Last Modified: Tue, 11 Jul 2023 05:25:43 GMT  
		Size: 2.3 KB (2310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa238d29e18bbc7bdc963a1e1b2680c62ba2df6944ca0da2f99bd14855d1534`  
		Last Modified: Tue, 11 Jul 2023 05:25:43 GMT  
		Size: 6.0 KB (6005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ff1ad0797d8b4bc76bf31cb29679b76b9a9af76a225e434abe3b7d81295b942`  
		Last Modified: Tue, 11 Jul 2023 05:25:43 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:15.5.0-postgres-tomcat`

```console
$ docker pull xwiki@sha256:143482a096b13073c1d9d59fde125210cd6009c4fb253a6d30cf5eaf8481fc5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:15.5.0-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:4741e9d9b24c00013903dbabf718e61ef5c4b23fd41a283067988225a4ea60ae
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **586.8 MB (586784502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1a1f265f59dcb2e5a6888c86ef11b46a92e4d498dcf98b2ab1f05735021fa2a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:37:40 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:37:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:37:42 GMT
ADD file:140fb5108b4a2861b5718ad03b4a5174bba03589ea8d4c053e6a0b282f439ff3 in / 
# Wed, 28 Jun 2023 08:37:42 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:34:07 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:35:02 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 20:35:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 20:35:35 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 08:22:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 08:22:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 08:22:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 08:22:21 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 08:22:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:22:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:25:33 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 08:25:34 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 00:16:15 GMT
COPY dir:8ddeace4a16f09a0d97488e225c7b2e4a48c9a93484d24b46a09759f52800501 in /usr/local/tomcat 
# Tue, 11 Jul 2023 00:16:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 00:16:20 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 00:16:20 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 00:16:20 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 04:41:24 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 04:41:26 GMT
ENV XWIKI_VERSION=15.5
# Tue, 11 Jul 2023 04:41:26 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.5
# Tue, 11 Jul 2023 04:41:26 GMT
ENV XWIKI_DOWNLOAD_SHA256=e552586d371da33b012cfbd974b3ba80d1b147a5c892ad6cf989960212cdaa02
# Tue, 11 Jul 2023 04:42:04 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 04:42:05 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Tue, 11 Jul 2023 04:42:05 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 04:42:05 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 04:42:06 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 04:42:06 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 04:42:06 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 04:42:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 04:42:06 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:9d19ee268e0d7bcf6716e6658ee1b0384a71d6f2f9aa1ae2085610cf7c7b316f`  
		Last Modified: Wed, 28 Jun 2023 11:50:41 GMT  
		Size: 30.4 MB (30431229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32db0ad82863deaedd2f9a365e52f595085778d28bd1e6f1d351107590cad806`  
		Last Modified: Tue, 04 Jul 2023 20:39:05 GMT  
		Size: 12.5 MB (12495341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01bb55fbcae928d7e6c08d6618580d2b27ce6e46083f861bbed1e01db41c20b`  
		Last Modified: Tue, 04 Jul 2023 20:41:01 GMT  
		Size: 46.7 MB (46666353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297c6e3f57ee032a3cc5f0fd28b52687129e7a1e6485aea12aff08cb6620071e`  
		Last Modified: Tue, 04 Jul 2023 20:40:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15b01f5ab5b71b356d93dff08f5037af8e8a03b4657f1fd303052261161ebd8`  
		Last Modified: Wed, 05 Jul 2023 08:37:14 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c6051a2b9ffe906ea99b555033966c877468da73cd19fd793c86099d0af531`  
		Last Modified: Tue, 11 Jul 2023 00:38:45 GMT  
		Size: 12.3 MB (12274167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34aaed1f6a3460fc256e262b462c1180ccef1b0665ffd50f900d1ef9c19f1d24`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 454.7 KB (454674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b809bf54ada009dfd91afa6ad239f7a791807f2928941b7f969493ec38246be`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bd305e7867896df13faced03525a0f25bf1ac1b2a2c93e60382cdfd41c08e16`  
		Last Modified: Tue, 11 Jul 2023 04:45:43 GMT  
		Size: 179.3 MB (179276407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35bfb758076cf011f5df9081f31dfbcf656cd98cd11b65f53f3684ec1e485c8f`  
		Last Modified: Tue, 11 Jul 2023 04:45:37 GMT  
		Size: 304.2 MB (304236708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2f8ccc8af30dd82bb4657bfdb7193ed23e8dc8823df1eaea8b1c8e4ab85d60`  
		Last Modified: Tue, 11 Jul 2023 04:45:20 GMT  
		Size: 936.8 KB (936849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:822e7d00d75f2a5b9a34edd0741b7e19410deb191f96800278c2921b043c81cb`  
		Last Modified: Tue, 11 Jul 2023 04:45:19 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba3137d80fef0218e2aaa65df38833a3e9d79b0d6e0b8d441376edbc36190ab`  
		Last Modified: Tue, 11 Jul 2023 04:45:19 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d02045e3c19030183c43f79b2c5e3a2f244dda96d11e96014e91d90e85f6e3a9`  
		Last Modified: Tue, 11 Jul 2023 04:45:19 GMT  
		Size: 6.0 KB (6006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91afad54a0c6d44f603953379c22801e4dbc9f2c282eaa00e94946d1d77dc3a4`  
		Last Modified: Tue, 11 Jul 2023 04:45:19 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:15.5.0-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:30799eeac6bc3f0efeefaf95f4161eeea6298cf60983391d2b7789735d58fa07
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.1 MB (578094027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc026cfcc219f16306961c1815044f7a63d5f49577815243d20c27d2d823d48`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:42:48 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:42:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:42:50 GMT
ADD file:262490f82459c14632f5c9a6d6a5cf6c07b4f307e8fd380fa764662cda46e88f in / 
# Wed, 28 Jun 2023 08:42:50 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:59 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 15:33:41 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 15:34:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 15:34:08 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 02:55:59 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 02:55:59 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 02:55:59 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 02:55:59 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 02:56:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 02:56:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 03:00:51 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 03:00:51 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 01:18:24 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 01:18:25 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 01:18:25 GMT
COPY dir:1743191a9534b9e7d795d3bf9ad18535d99e75967877447e17d7b63574d878d5 in /usr/local/tomcat 
# Tue, 11 Jul 2023 01:18:28 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 01:18:29 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 01:18:29 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 01:18:29 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 05:22:36 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 05:22:39 GMT
ENV XWIKI_VERSION=15.5
# Tue, 11 Jul 2023 05:22:39 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.5
# Tue, 11 Jul 2023 05:22:39 GMT
ENV XWIKI_DOWNLOAD_SHA256=e552586d371da33b012cfbd974b3ba80d1b147a5c892ad6cf989960212cdaa02
# Tue, 11 Jul 2023 05:23:18 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 05:23:21 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Tue, 11 Jul 2023 05:23:21 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 05:23:21 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 05:23:22 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 05:23:22 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 05:23:22 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 05:23:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 05:23:22 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:ac34a2e0269ced3acc355be706239ee0f3f1e73a035c40dd2fac74827164ee53`  
		Last Modified: Wed, 28 Jun 2023 23:23:40 GMT  
		Size: 28.4 MB (28391011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d9df805749ad7c4605f0d49a64da6a6173ab190ec361dc2063b6b73af59ab5`  
		Last Modified: Tue, 04 Jul 2023 15:36:55 GMT  
		Size: 12.5 MB (12455497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1e11a5919e5746092b2a288f71090ffdb0d3544b7b54c31ed0137e6d5d4735`  
		Last Modified: Tue, 04 Jul 2023 15:38:37 GMT  
		Size: 45.0 MB (45009079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80987dc89da28aa5ceec7a86ea74e13cee06ecd9304cf4c92d8f382c79eb4f2`  
		Last Modified: Tue, 04 Jul 2023 15:38:32 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de67c7824eef053da628456fe8aba244c4150024af9454dd4091763920d836c`  
		Last Modified: Wed, 05 Jul 2023 03:14:23 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f77f07e56c3d3019cd346deaeacbe572b15b26a924c19b6386877b47123a89e`  
		Last Modified: Tue, 11 Jul 2023 01:39:24 GMT  
		Size: 12.3 MB (12283700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2422cddd65b0ff63d783c999d005c42281720b8615f5872e1e8fdb32dd9981d9`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 455.1 KB (455052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b023f0d964d565a960e567dcaaa605fdff6da02b54971f4d0693506b481b8c`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:968d46d099e01403854799f31b6235698a474c27fd58b0172b1eb3889cd5067f`  
		Last Modified: Tue, 11 Jul 2023 05:26:50 GMT  
		Size: 174.3 MB (174313369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2894444c04152ca46b568422ea482a66ed3763028ff87cc82d80132ea0e4cdd`  
		Last Modified: Tue, 11 Jul 2023 05:26:46 GMT  
		Size: 304.2 MB (304236690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77118bb73ac2d6b789413d31beabdbb72e88543cca5b3e6406076fd10d40d8d3`  
		Last Modified: Tue, 11 Jul 2023 05:26:32 GMT  
		Size: 936.9 KB (936852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9eb9df1942e9402403596582620c7fb14dbdd8e12de634c88e080cc5795a812`  
		Last Modified: Tue, 11 Jul 2023 05:26:32 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d23fb311f1a568af6e8b96dcb8cfb10d4d96a88aee4243256a3e73f4727fa318`  
		Last Modified: Tue, 11 Jul 2023 05:26:32 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dd3c555379bf5bd7f8d13501bb806b6b5ffb4c2ecb169ce4485f1cbf0d26b9a`  
		Last Modified: Tue, 11 Jul 2023 05:26:32 GMT  
		Size: 6.0 KB (6006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8254381348a57ea56306a83d8f2a89630202f393f54d6102b5652be9cfa10f8f`  
		Last Modified: Tue, 11 Jul 2023 05:26:33 GMT  
		Size: 2.5 KB (2507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:latest`

```console
$ docker pull xwiki@sha256:66e25eb51a5a079e68e523ac98a46358b70c8c431f4360e1565d23aead7eaa3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:latest` - linux; amd64

```console
$ docker pull xwiki@sha256:80718cf2818aac2523383b177893d1f4454722abe547ec303a18e3b4a30362b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **587.3 MB (587250774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97a5a7f1172dd3ea626947d13678241c2e0f4e5391c13ab4c32dd3f009d902c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:37:40 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:37:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:37:42 GMT
ADD file:140fb5108b4a2861b5718ad03b4a5174bba03589ea8d4c053e6a0b282f439ff3 in / 
# Wed, 28 Jun 2023 08:37:42 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:34:07 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:35:02 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 20:35:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 20:35:35 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 08:22:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 08:22:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 08:22:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 08:22:21 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 08:22:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:22:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:25:33 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 08:25:34 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 00:16:15 GMT
COPY dir:8ddeace4a16f09a0d97488e225c7b2e4a48c9a93484d24b46a09759f52800501 in /usr/local/tomcat 
# Tue, 11 Jul 2023 00:16:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 00:16:20 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 00:16:20 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 00:16:20 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 04:40:02 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 04:40:03 GMT
ENV XWIKI_VERSION=15.5
# Tue, 11 Jul 2023 04:40:03 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.5
# Tue, 11 Jul 2023 04:40:03 GMT
ENV XWIKI_DOWNLOAD_SHA256=e552586d371da33b012cfbd974b3ba80d1b147a5c892ad6cf989960212cdaa02
# Tue, 11 Jul 2023 04:40:41 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 04:40:42 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Tue, 11 Jul 2023 04:40:42 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Tue, 11 Jul 2023 04:40:42 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Tue, 11 Jul 2023 04:40:42 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 04:40:42 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 04:40:43 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Tue, 11 Jul 2023 04:40:43 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 04:40:43 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 04:40:44 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 04:40:44 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 04:40:44 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 04:40:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 04:40:44 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:9d19ee268e0d7bcf6716e6658ee1b0384a71d6f2f9aa1ae2085610cf7c7b316f`  
		Last Modified: Wed, 28 Jun 2023 11:50:41 GMT  
		Size: 30.4 MB (30431229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32db0ad82863deaedd2f9a365e52f595085778d28bd1e6f1d351107590cad806`  
		Last Modified: Tue, 04 Jul 2023 20:39:05 GMT  
		Size: 12.5 MB (12495341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01bb55fbcae928d7e6c08d6618580d2b27ce6e46083f861bbed1e01db41c20b`  
		Last Modified: Tue, 04 Jul 2023 20:41:01 GMT  
		Size: 46.7 MB (46666353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297c6e3f57ee032a3cc5f0fd28b52687129e7a1e6485aea12aff08cb6620071e`  
		Last Modified: Tue, 04 Jul 2023 20:40:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15b01f5ab5b71b356d93dff08f5037af8e8a03b4657f1fd303052261161ebd8`  
		Last Modified: Wed, 05 Jul 2023 08:37:14 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c6051a2b9ffe906ea99b555033966c877468da73cd19fd793c86099d0af531`  
		Last Modified: Tue, 11 Jul 2023 00:38:45 GMT  
		Size: 12.3 MB (12274167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34aaed1f6a3460fc256e262b462c1180ccef1b0665ffd50f900d1ef9c19f1d24`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 454.7 KB (454674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b809bf54ada009dfd91afa6ad239f7a791807f2928941b7f969493ec38246be`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877cc60516baaeb7846bba5d5de9e491d0406cd2f43959d7d4e104d89df5e228`  
		Last Modified: Tue, 11 Jul 2023 04:44:49 GMT  
		Size: 178.3 MB (178335971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b863cfbbf93cec3814eec01a334529779a02fcbb3cdff4e2d212bb70287a5720`  
		Last Modified: Tue, 11 Jul 2023 04:44:42 GMT  
		Size: 304.2 MB (304236736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faad5f8d2320ee7d3eb3c3f81aff36754d147687cdb520bc8b24d3170bfcee58`  
		Last Modified: Tue, 11 Jul 2023 04:44:25 GMT  
		Size: 2.3 MB (2343679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ad43407c01ec5371102aaa125c19fb5399f629346a71d4913d742cfed44165`  
		Last Modified: Tue, 11 Jul 2023 04:44:24 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03112af3cb3ddf2e651a23fd879dd50f96a17b20d580105c90d7bb357f02ab0a`  
		Last Modified: Tue, 11 Jul 2023 04:44:24 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7098881bee3a8920bec6f5c352be02657d02e5bb3a4ce69faa81f9354193acbf`  
		Last Modified: Tue, 11 Jul 2023 04:44:24 GMT  
		Size: 6.0 KB (6004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:880ec6a5100b3effc0772c9e06afdfdab1786151d59c78eb30826e0245f2ebe5`  
		Last Modified: Tue, 11 Jul 2023 04:44:24 GMT  
		Size: 2.5 KB (2507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:latest` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:80454bf7fba586e95357c0d982c52ab2d1504e85c6d085e14a1091a19a0d7e65
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.6 MB (578560793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e24eddde7707953934d4ceba63f6297ff5115dc6ec8e8e39946e4f8bd2542c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:42:48 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:42:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:42:50 GMT
ADD file:262490f82459c14632f5c9a6d6a5cf6c07b4f307e8fd380fa764662cda46e88f in / 
# Wed, 28 Jun 2023 08:42:50 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:59 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 15:33:41 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 15:34:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 15:34:08 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 02:55:59 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 02:55:59 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 02:55:59 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 02:55:59 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 02:56:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 02:56:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 03:00:51 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 03:00:51 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 01:18:24 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 01:18:25 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 01:18:25 GMT
COPY dir:1743191a9534b9e7d795d3bf9ad18535d99e75967877447e17d7b63574d878d5 in /usr/local/tomcat 
# Tue, 11 Jul 2023 01:18:28 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 01:18:29 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 01:18:29 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 01:18:29 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 05:21:20 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 05:21:23 GMT
ENV XWIKI_VERSION=15.5
# Tue, 11 Jul 2023 05:21:23 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.5
# Tue, 11 Jul 2023 05:21:23 GMT
ENV XWIKI_DOWNLOAD_SHA256=e552586d371da33b012cfbd974b3ba80d1b147a5c892ad6cf989960212cdaa02
# Tue, 11 Jul 2023 05:22:02 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 05:22:04 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Tue, 11 Jul 2023 05:22:04 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Tue, 11 Jul 2023 05:22:04 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Tue, 11 Jul 2023 05:22:04 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 05:22:04 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 05:22:05 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Tue, 11 Jul 2023 05:22:06 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 05:22:06 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 05:22:06 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 05:22:06 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 05:22:06 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 05:22:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 05:22:06 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:ac34a2e0269ced3acc355be706239ee0f3f1e73a035c40dd2fac74827164ee53`  
		Last Modified: Wed, 28 Jun 2023 23:23:40 GMT  
		Size: 28.4 MB (28391011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d9df805749ad7c4605f0d49a64da6a6173ab190ec361dc2063b6b73af59ab5`  
		Last Modified: Tue, 04 Jul 2023 15:36:55 GMT  
		Size: 12.5 MB (12455497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1e11a5919e5746092b2a288f71090ffdb0d3544b7b54c31ed0137e6d5d4735`  
		Last Modified: Tue, 04 Jul 2023 15:38:37 GMT  
		Size: 45.0 MB (45009079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80987dc89da28aa5ceec7a86ea74e13cee06ecd9304cf4c92d8f382c79eb4f2`  
		Last Modified: Tue, 04 Jul 2023 15:38:32 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de67c7824eef053da628456fe8aba244c4150024af9454dd4091763920d836c`  
		Last Modified: Wed, 05 Jul 2023 03:14:23 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f77f07e56c3d3019cd346deaeacbe572b15b26a924c19b6386877b47123a89e`  
		Last Modified: Tue, 11 Jul 2023 01:39:24 GMT  
		Size: 12.3 MB (12283700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2422cddd65b0ff63d783c999d005c42281720b8615f5872e1e8fdb32dd9981d9`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 455.1 KB (455052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b023f0d964d565a960e567dcaaa605fdff6da02b54971f4d0693506b481b8c`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28177f0763a75e5c940bb6a7919185effccd7cf14c0e350198b3aedbe1db789`  
		Last Modified: Tue, 11 Jul 2023 05:26:01 GMT  
		Size: 173.4 MB (173373450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b39c7f4340aa5dd678a6a0a9bc018229eaadb2a94a0af6bc41d17ce77cdefb`  
		Last Modified: Tue, 11 Jul 2023 05:25:57 GMT  
		Size: 304.2 MB (304236707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc58f6eb776423b78c7a88af6ee221317c44f67e3fb4f413ef3823e8895288a2`  
		Last Modified: Tue, 11 Jul 2023 05:25:43 GMT  
		Size: 2.3 MB (2343673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea5e5502a3de7ec04368cbbb5f6c48f21fc7eac2657e2376ab3c7271ad4f85d`  
		Last Modified: Tue, 11 Jul 2023 05:25:43 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f8adcd32841dea1f4e39476b790a663510401829d69a806cad6007452d0367`  
		Last Modified: Tue, 11 Jul 2023 05:25:43 GMT  
		Size: 2.3 KB (2310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa238d29e18bbc7bdc963a1e1b2680c62ba2df6944ca0da2f99bd14855d1534`  
		Last Modified: Tue, 11 Jul 2023 05:25:43 GMT  
		Size: 6.0 KB (6005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ff1ad0797d8b4bc76bf31cb29679b76b9a9af76a225e434abe3b7d81295b942`  
		Last Modified: Tue, 11 Jul 2023 05:25:43 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:lts`

```console
$ docker pull xwiki@sha256:d684b69a373a2cef6fa2a32d55c3e87eed6a6f36cfac5320606e88204e88186a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:lts` - linux; amd64

```console
$ docker pull xwiki@sha256:ede13785f63dcaf8042ae3ad55c0c8fa410a3832504cdcf66916035506feebc9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.3 MB (590275216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0cdff4d327d68685f5dd8da61be21269df316c760ef6487e0aa642ec059b882`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:37:40 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:37:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:37:42 GMT
ADD file:140fb5108b4a2861b5718ad03b4a5174bba03589ea8d4c053e6a0b282f439ff3 in / 
# Wed, 28 Jun 2023 08:37:42 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:34:07 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:35:02 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 20:35:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 20:35:35 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 08:22:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 08:22:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 08:22:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 08:22:21 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 08:22:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:22:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:25:33 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 08:25:34 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 00:16:15 GMT
COPY dir:8ddeace4a16f09a0d97488e225c7b2e4a48c9a93484d24b46a09759f52800501 in /usr/local/tomcat 
# Tue, 11 Jul 2023 00:16:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 00:16:20 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 00:16:20 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 00:16:20 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 04:40:02 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 04:42:15 GMT
ENV XWIKI_VERSION=14.10.13
# Tue, 11 Jul 2023 04:42:15 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.13
# Tue, 11 Jul 2023 04:42:15 GMT
ENV XWIKI_DOWNLOAD_SHA256=5883ffdbc10865043778f3caa48fbca900129cf41c76ee6fdafba74769c928d4
# Tue, 11 Jul 2023 04:42:54 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 04:42:54 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Tue, 11 Jul 2023 04:42:55 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Tue, 11 Jul 2023 04:42:55 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Tue, 11 Jul 2023 04:42:55 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 04:42:55 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 04:42:56 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Tue, 11 Jul 2023 04:42:56 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 04:42:56 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 04:42:56 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 04:42:56 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 04:42:56 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 04:42:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 04:42:57 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:9d19ee268e0d7bcf6716e6658ee1b0384a71d6f2f9aa1ae2085610cf7c7b316f`  
		Last Modified: Wed, 28 Jun 2023 11:50:41 GMT  
		Size: 30.4 MB (30431229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32db0ad82863deaedd2f9a365e52f595085778d28bd1e6f1d351107590cad806`  
		Last Modified: Tue, 04 Jul 2023 20:39:05 GMT  
		Size: 12.5 MB (12495341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01bb55fbcae928d7e6c08d6618580d2b27ce6e46083f861bbed1e01db41c20b`  
		Last Modified: Tue, 04 Jul 2023 20:41:01 GMT  
		Size: 46.7 MB (46666353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297c6e3f57ee032a3cc5f0fd28b52687129e7a1e6485aea12aff08cb6620071e`  
		Last Modified: Tue, 04 Jul 2023 20:40:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15b01f5ab5b71b356d93dff08f5037af8e8a03b4657f1fd303052261161ebd8`  
		Last Modified: Wed, 05 Jul 2023 08:37:14 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c6051a2b9ffe906ea99b555033966c877468da73cd19fd793c86099d0af531`  
		Last Modified: Tue, 11 Jul 2023 00:38:45 GMT  
		Size: 12.3 MB (12274167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34aaed1f6a3460fc256e262b462c1180ccef1b0665ffd50f900d1ef9c19f1d24`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 454.7 KB (454674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b809bf54ada009dfd91afa6ad239f7a791807f2928941b7f969493ec38246be`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877cc60516baaeb7846bba5d5de9e491d0406cd2f43959d7d4e104d89df5e228`  
		Last Modified: Tue, 11 Jul 2023 04:44:49 GMT  
		Size: 178.3 MB (178335971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d83ab8708da1a9ab9fb6a48ac52687e3488789fccbd4a07ced23e73be97d1b`  
		Last Modified: Tue, 11 Jul 2023 04:46:37 GMT  
		Size: 307.3 MB (307261194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:663bd82ddfd62b4cf39556e967220c977dcdbb37a1fd053c779fd0baa6898818`  
		Last Modified: Tue, 11 Jul 2023 04:46:21 GMT  
		Size: 2.3 MB (2343668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed5bec13f08d98c63e3c81fb0a45f8734746d82b5504310835cac9e7a8e18dec`  
		Last Modified: Tue, 11 Jul 2023 04:46:21 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dfccb5d359b6e3ae2ddf7257f81d0e9b794f602ab4e3f3196c372af5543d1ca`  
		Last Modified: Tue, 11 Jul 2023 04:46:21 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac17a1dc4319814e728392d0b0b3ad40083d48efeaec075e52bdaef3545341d0`  
		Last Modified: Tue, 11 Jul 2023 04:46:21 GMT  
		Size: 6.0 KB (6015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57f2437b546ab6322d8db9cf14928c907568c9728574599d16ea306286ab824c`  
		Last Modified: Tue, 11 Jul 2023 04:46:21 GMT  
		Size: 2.5 KB (2498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:lts` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:2c70da3ff6aad987960017b1f402de397c9e9a3b3f806a125702c26c14a1bfb8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.6 MB (581585177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a5e15a24190e32ccad68b6a75aa965123ee8a3fd0edd724d8cbaecbcf34acf6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:42:48 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:42:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:42:50 GMT
ADD file:262490f82459c14632f5c9a6d6a5cf6c07b4f307e8fd380fa764662cda46e88f in / 
# Wed, 28 Jun 2023 08:42:50 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:59 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 15:33:41 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 15:34:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 15:34:08 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 02:55:59 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 02:55:59 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 02:55:59 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 02:55:59 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 02:56:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 02:56:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 03:00:51 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 03:00:51 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 01:18:24 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 01:18:25 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 01:18:25 GMT
COPY dir:1743191a9534b9e7d795d3bf9ad18535d99e75967877447e17d7b63574d878d5 in /usr/local/tomcat 
# Tue, 11 Jul 2023 01:18:28 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 01:18:29 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 01:18:29 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 01:18:29 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 05:21:20 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 05:23:40 GMT
ENV XWIKI_VERSION=14.10.13
# Tue, 11 Jul 2023 05:23:40 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.13
# Tue, 11 Jul 2023 05:23:40 GMT
ENV XWIKI_DOWNLOAD_SHA256=5883ffdbc10865043778f3caa48fbca900129cf41c76ee6fdafba74769c928d4
# Tue, 11 Jul 2023 05:24:20 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 05:24:23 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Tue, 11 Jul 2023 05:24:23 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Tue, 11 Jul 2023 05:24:23 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Tue, 11 Jul 2023 05:24:23 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 05:24:23 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 05:24:24 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Tue, 11 Jul 2023 05:24:24 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 05:24:24 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 05:24:25 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 05:24:25 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 05:24:25 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 05:24:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 05:24:25 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:ac34a2e0269ced3acc355be706239ee0f3f1e73a035c40dd2fac74827164ee53`  
		Last Modified: Wed, 28 Jun 2023 23:23:40 GMT  
		Size: 28.4 MB (28391011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d9df805749ad7c4605f0d49a64da6a6173ab190ec361dc2063b6b73af59ab5`  
		Last Modified: Tue, 04 Jul 2023 15:36:55 GMT  
		Size: 12.5 MB (12455497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1e11a5919e5746092b2a288f71090ffdb0d3544b7b54c31ed0137e6d5d4735`  
		Last Modified: Tue, 04 Jul 2023 15:38:37 GMT  
		Size: 45.0 MB (45009079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80987dc89da28aa5ceec7a86ea74e13cee06ecd9304cf4c92d8f382c79eb4f2`  
		Last Modified: Tue, 04 Jul 2023 15:38:32 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de67c7824eef053da628456fe8aba244c4150024af9454dd4091763920d836c`  
		Last Modified: Wed, 05 Jul 2023 03:14:23 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f77f07e56c3d3019cd346deaeacbe572b15b26a924c19b6386877b47123a89e`  
		Last Modified: Tue, 11 Jul 2023 01:39:24 GMT  
		Size: 12.3 MB (12283700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2422cddd65b0ff63d783c999d005c42281720b8615f5872e1e8fdb32dd9981d9`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 455.1 KB (455052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b023f0d964d565a960e567dcaaa605fdff6da02b54971f4d0693506b481b8c`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28177f0763a75e5c940bb6a7919185effccd7cf14c0e350198b3aedbe1db789`  
		Last Modified: Tue, 11 Jul 2023 05:26:01 GMT  
		Size: 173.4 MB (173373450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc5b16765fdc498e3f3e0db1f6f5968716864f931b8490f2092985f2aad66e6`  
		Last Modified: Tue, 11 Jul 2023 05:27:47 GMT  
		Size: 307.3 MB (307261061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e05260decea8ae0b8e52961a6b822e7f61aa0d94e359d9bdfb0a8d1c12ab373`  
		Last Modified: Tue, 11 Jul 2023 05:27:33 GMT  
		Size: 2.3 MB (2343684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80db78e6c67fd96e8da400c8505c850ac34058465e92e7c08c2079a56c581eef`  
		Last Modified: Tue, 11 Jul 2023 05:27:32 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e13d3d8f1788f25950792ca1b21389742cb964f69af7853cd12c938239fa7c94`  
		Last Modified: Tue, 11 Jul 2023 05:27:33 GMT  
		Size: 2.3 KB (2311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ecfdbab47ad32f6ddf82bd2c97ac1e2786af57d2bfc2653639b91c3a1833a3`  
		Last Modified: Tue, 11 Jul 2023 05:27:32 GMT  
		Size: 6.0 KB (6020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0b9874cce7da8c08bc10f43d1a239ff6d3d1b18189a83d61bf566a352cba781`  
		Last Modified: Tue, 11 Jul 2023 05:27:32 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:lts-mariadb`

```console
$ docker pull xwiki@sha256:4f0cfbbcc4d2a7ab73eac160f70b796dbe864d041ce38174443170e66be4e82c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:lts-mariadb` - linux; amd64

```console
$ docker pull xwiki@sha256:2457ece1ecfc0fdb7b33b40d99e1cc0e647b34427eb7d3adf0321d7035832bd7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **588.5 MB (588526114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23dabbcf30b0cba2e6e27db54197aadc63470a751d0cf652f95c6ffc4dc48bc5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:37:40 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:37:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:37:42 GMT
ADD file:140fb5108b4a2861b5718ad03b4a5174bba03589ea8d4c053e6a0b282f439ff3 in / 
# Wed, 28 Jun 2023 08:37:42 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:34:07 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:35:02 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 20:35:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 20:35:35 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 08:22:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 08:22:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 08:22:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 08:22:21 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 08:22:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:22:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:25:33 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 08:25:34 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 00:16:15 GMT
COPY dir:8ddeace4a16f09a0d97488e225c7b2e4a48c9a93484d24b46a09759f52800501 in /usr/local/tomcat 
# Tue, 11 Jul 2023 00:16:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 00:16:20 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 00:16:20 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 00:16:20 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 04:40:02 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 04:42:15 GMT
ENV XWIKI_VERSION=14.10.13
# Tue, 11 Jul 2023 04:42:15 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.13
# Tue, 11 Jul 2023 04:42:15 GMT
ENV XWIKI_DOWNLOAD_SHA256=5883ffdbc10865043778f3caa48fbca900129cf41c76ee6fdafba74769c928d4
# Tue, 11 Jul 2023 04:42:54 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 04:43:53 GMT
ENV MARIADB_JDBC_VERSION=3.1.4
# Tue, 11 Jul 2023 04:43:53 GMT
ENV MARIADB_JDBC_SHA256=eb88b5d727d82e25117e2b6fabcec1daf734633b0a576456c73215884c189ad4
# Tue, 11 Jul 2023 04:43:53 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.1.4
# Tue, 11 Jul 2023 04:43:53 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.1.4.jar
# Tue, 11 Jul 2023 04:43:53 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.1.4.jar
# Tue, 11 Jul 2023 04:43:54 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Tue, 11 Jul 2023 04:43:54 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 04:43:54 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 04:43:55 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 04:43:55 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 04:43:55 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 04:43:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 04:43:55 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:9d19ee268e0d7bcf6716e6658ee1b0384a71d6f2f9aa1ae2085610cf7c7b316f`  
		Last Modified: Wed, 28 Jun 2023 11:50:41 GMT  
		Size: 30.4 MB (30431229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32db0ad82863deaedd2f9a365e52f595085778d28bd1e6f1d351107590cad806`  
		Last Modified: Tue, 04 Jul 2023 20:39:05 GMT  
		Size: 12.5 MB (12495341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01bb55fbcae928d7e6c08d6618580d2b27ce6e46083f861bbed1e01db41c20b`  
		Last Modified: Tue, 04 Jul 2023 20:41:01 GMT  
		Size: 46.7 MB (46666353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297c6e3f57ee032a3cc5f0fd28b52687129e7a1e6485aea12aff08cb6620071e`  
		Last Modified: Tue, 04 Jul 2023 20:40:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15b01f5ab5b71b356d93dff08f5037af8e8a03b4657f1fd303052261161ebd8`  
		Last Modified: Wed, 05 Jul 2023 08:37:14 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c6051a2b9ffe906ea99b555033966c877468da73cd19fd793c86099d0af531`  
		Last Modified: Tue, 11 Jul 2023 00:38:45 GMT  
		Size: 12.3 MB (12274167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34aaed1f6a3460fc256e262b462c1180ccef1b0665ffd50f900d1ef9c19f1d24`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 454.7 KB (454674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b809bf54ada009dfd91afa6ad239f7a791807f2928941b7f969493ec38246be`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877cc60516baaeb7846bba5d5de9e491d0406cd2f43959d7d4e104d89df5e228`  
		Last Modified: Tue, 11 Jul 2023 04:44:49 GMT  
		Size: 178.3 MB (178335971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d83ab8708da1a9ab9fb6a48ac52687e3488789fccbd4a07ced23e73be97d1b`  
		Last Modified: Tue, 11 Jul 2023 04:46:37 GMT  
		Size: 307.3 MB (307261194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e875fea8a2c98d9a649ede02e5cde89adc140d705cd90f987da3c01c0e0e91ba`  
		Last Modified: Tue, 11 Jul 2023 04:47:34 GMT  
		Size: 594.6 KB (594551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03c934df3cbcee083ccb0b050eb79b8a33e576b12a5d653cf3779efd73ae0886`  
		Last Modified: Tue, 11 Jul 2023 04:47:34 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:169d82fe476f2ba0c25f369977bcad3dbefc51aecdd90854d3d5bd162ffca191`  
		Last Modified: Tue, 11 Jul 2023 04:47:34 GMT  
		Size: 2.3 KB (2309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2bc34d1fe1755d4b6c92a1f18f895229ebbd1c4c33b8d9870ad601f460c6e30`  
		Last Modified: Tue, 11 Jul 2023 04:47:34 GMT  
		Size: 6.0 KB (6017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dc85b4209f7c5902eaddc9237e35ff851834dbe9a46b12cda8f7c6bd37e98f0`  
		Last Modified: Tue, 11 Jul 2023 04:47:33 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:lts-mariadb` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:f2d58b0e807535f9a89d2aefdb36e0ed212696276c598c6ac7a44ae4a463571e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.8 MB (579836046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4827d8602436ba34af88ff0bccf958bc03dbf862b5011c12c3799c90dba3626a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:42:48 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:42:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:42:50 GMT
ADD file:262490f82459c14632f5c9a6d6a5cf6c07b4f307e8fd380fa764662cda46e88f in / 
# Wed, 28 Jun 2023 08:42:50 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:59 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 15:33:41 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 15:34:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 15:34:08 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 02:55:59 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 02:55:59 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 02:55:59 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 02:55:59 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 02:56:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 02:56:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 03:00:51 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 03:00:51 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 01:18:24 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 01:18:25 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 01:18:25 GMT
COPY dir:1743191a9534b9e7d795d3bf9ad18535d99e75967877447e17d7b63574d878d5 in /usr/local/tomcat 
# Tue, 11 Jul 2023 01:18:28 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 01:18:29 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 01:18:29 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 01:18:29 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 05:21:20 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 05:23:40 GMT
ENV XWIKI_VERSION=14.10.13
# Tue, 11 Jul 2023 05:23:40 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.13
# Tue, 11 Jul 2023 05:23:40 GMT
ENV XWIKI_DOWNLOAD_SHA256=5883ffdbc10865043778f3caa48fbca900129cf41c76ee6fdafba74769c928d4
# Tue, 11 Jul 2023 05:24:20 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 05:25:16 GMT
ENV MARIADB_JDBC_VERSION=3.1.4
# Tue, 11 Jul 2023 05:25:16 GMT
ENV MARIADB_JDBC_SHA256=eb88b5d727d82e25117e2b6fabcec1daf734633b0a576456c73215884c189ad4
# Tue, 11 Jul 2023 05:25:16 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.1.4
# Tue, 11 Jul 2023 05:25:16 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.1.4.jar
# Tue, 11 Jul 2023 05:25:17 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.1.4.jar
# Tue, 11 Jul 2023 05:25:17 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Tue, 11 Jul 2023 05:25:17 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 05:25:17 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 05:25:18 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 05:25:18 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 05:25:18 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 05:25:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 05:25:18 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:ac34a2e0269ced3acc355be706239ee0f3f1e73a035c40dd2fac74827164ee53`  
		Last Modified: Wed, 28 Jun 2023 23:23:40 GMT  
		Size: 28.4 MB (28391011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d9df805749ad7c4605f0d49a64da6a6173ab190ec361dc2063b6b73af59ab5`  
		Last Modified: Tue, 04 Jul 2023 15:36:55 GMT  
		Size: 12.5 MB (12455497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1e11a5919e5746092b2a288f71090ffdb0d3544b7b54c31ed0137e6d5d4735`  
		Last Modified: Tue, 04 Jul 2023 15:38:37 GMT  
		Size: 45.0 MB (45009079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80987dc89da28aa5ceec7a86ea74e13cee06ecd9304cf4c92d8f382c79eb4f2`  
		Last Modified: Tue, 04 Jul 2023 15:38:32 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de67c7824eef053da628456fe8aba244c4150024af9454dd4091763920d836c`  
		Last Modified: Wed, 05 Jul 2023 03:14:23 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f77f07e56c3d3019cd346deaeacbe572b15b26a924c19b6386877b47123a89e`  
		Last Modified: Tue, 11 Jul 2023 01:39:24 GMT  
		Size: 12.3 MB (12283700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2422cddd65b0ff63d783c999d005c42281720b8615f5872e1e8fdb32dd9981d9`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 455.1 KB (455052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b023f0d964d565a960e567dcaaa605fdff6da02b54971f4d0693506b481b8c`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28177f0763a75e5c940bb6a7919185effccd7cf14c0e350198b3aedbe1db789`  
		Last Modified: Tue, 11 Jul 2023 05:26:01 GMT  
		Size: 173.4 MB (173373450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc5b16765fdc498e3f3e0db1f6f5968716864f931b8490f2092985f2aad66e6`  
		Last Modified: Tue, 11 Jul 2023 05:27:47 GMT  
		Size: 307.3 MB (307261061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cde3b2925cca0eaeca051a9d34fc8559173eb81198be6edb87ef675ddbd104c`  
		Last Modified: Tue, 11 Jul 2023 05:28:44 GMT  
		Size: 594.6 KB (594553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a572ecd6de904372e67871760ea39b4c45f94b03c1bd47a6ee27a1151f44f25`  
		Last Modified: Tue, 11 Jul 2023 05:28:43 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48dc7acaf3762507fe63c6d484d73da83682cfc993ce96feccb9b0cb2bea8895`  
		Last Modified: Tue, 11 Jul 2023 05:28:43 GMT  
		Size: 2.3 KB (2314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd91b38c50762886b672122ce7698e839324aa39970db075d8fa1a46ae5d6fe5`  
		Last Modified: Tue, 11 Jul 2023 05:28:43 GMT  
		Size: 6.0 KB (6018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:536a460fc0ee741e1de6915eb0f7533df412ab1b9c51ac2f7686ca966abef1fc`  
		Last Modified: Tue, 11 Jul 2023 05:28:43 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:lts-mariadb-tomcat`

```console
$ docker pull xwiki@sha256:4f0cfbbcc4d2a7ab73eac160f70b796dbe864d041ce38174443170e66be4e82c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:lts-mariadb-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:2457ece1ecfc0fdb7b33b40d99e1cc0e647b34427eb7d3adf0321d7035832bd7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **588.5 MB (588526114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23dabbcf30b0cba2e6e27db54197aadc63470a751d0cf652f95c6ffc4dc48bc5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:37:40 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:37:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:37:42 GMT
ADD file:140fb5108b4a2861b5718ad03b4a5174bba03589ea8d4c053e6a0b282f439ff3 in / 
# Wed, 28 Jun 2023 08:37:42 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:34:07 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:35:02 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 20:35:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 20:35:35 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 08:22:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 08:22:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 08:22:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 08:22:21 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 08:22:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:22:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:25:33 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 08:25:34 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 00:16:15 GMT
COPY dir:8ddeace4a16f09a0d97488e225c7b2e4a48c9a93484d24b46a09759f52800501 in /usr/local/tomcat 
# Tue, 11 Jul 2023 00:16:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 00:16:20 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 00:16:20 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 00:16:20 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 04:40:02 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 04:42:15 GMT
ENV XWIKI_VERSION=14.10.13
# Tue, 11 Jul 2023 04:42:15 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.13
# Tue, 11 Jul 2023 04:42:15 GMT
ENV XWIKI_DOWNLOAD_SHA256=5883ffdbc10865043778f3caa48fbca900129cf41c76ee6fdafba74769c928d4
# Tue, 11 Jul 2023 04:42:54 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 04:43:53 GMT
ENV MARIADB_JDBC_VERSION=3.1.4
# Tue, 11 Jul 2023 04:43:53 GMT
ENV MARIADB_JDBC_SHA256=eb88b5d727d82e25117e2b6fabcec1daf734633b0a576456c73215884c189ad4
# Tue, 11 Jul 2023 04:43:53 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.1.4
# Tue, 11 Jul 2023 04:43:53 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.1.4.jar
# Tue, 11 Jul 2023 04:43:53 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.1.4.jar
# Tue, 11 Jul 2023 04:43:54 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Tue, 11 Jul 2023 04:43:54 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 04:43:54 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 04:43:55 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 04:43:55 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 04:43:55 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 04:43:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 04:43:55 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:9d19ee268e0d7bcf6716e6658ee1b0384a71d6f2f9aa1ae2085610cf7c7b316f`  
		Last Modified: Wed, 28 Jun 2023 11:50:41 GMT  
		Size: 30.4 MB (30431229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32db0ad82863deaedd2f9a365e52f595085778d28bd1e6f1d351107590cad806`  
		Last Modified: Tue, 04 Jul 2023 20:39:05 GMT  
		Size: 12.5 MB (12495341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01bb55fbcae928d7e6c08d6618580d2b27ce6e46083f861bbed1e01db41c20b`  
		Last Modified: Tue, 04 Jul 2023 20:41:01 GMT  
		Size: 46.7 MB (46666353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297c6e3f57ee032a3cc5f0fd28b52687129e7a1e6485aea12aff08cb6620071e`  
		Last Modified: Tue, 04 Jul 2023 20:40:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15b01f5ab5b71b356d93dff08f5037af8e8a03b4657f1fd303052261161ebd8`  
		Last Modified: Wed, 05 Jul 2023 08:37:14 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c6051a2b9ffe906ea99b555033966c877468da73cd19fd793c86099d0af531`  
		Last Modified: Tue, 11 Jul 2023 00:38:45 GMT  
		Size: 12.3 MB (12274167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34aaed1f6a3460fc256e262b462c1180ccef1b0665ffd50f900d1ef9c19f1d24`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 454.7 KB (454674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b809bf54ada009dfd91afa6ad239f7a791807f2928941b7f969493ec38246be`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877cc60516baaeb7846bba5d5de9e491d0406cd2f43959d7d4e104d89df5e228`  
		Last Modified: Tue, 11 Jul 2023 04:44:49 GMT  
		Size: 178.3 MB (178335971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d83ab8708da1a9ab9fb6a48ac52687e3488789fccbd4a07ced23e73be97d1b`  
		Last Modified: Tue, 11 Jul 2023 04:46:37 GMT  
		Size: 307.3 MB (307261194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e875fea8a2c98d9a649ede02e5cde89adc140d705cd90f987da3c01c0e0e91ba`  
		Last Modified: Tue, 11 Jul 2023 04:47:34 GMT  
		Size: 594.6 KB (594551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03c934df3cbcee083ccb0b050eb79b8a33e576b12a5d653cf3779efd73ae0886`  
		Last Modified: Tue, 11 Jul 2023 04:47:34 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:169d82fe476f2ba0c25f369977bcad3dbefc51aecdd90854d3d5bd162ffca191`  
		Last Modified: Tue, 11 Jul 2023 04:47:34 GMT  
		Size: 2.3 KB (2309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2bc34d1fe1755d4b6c92a1f18f895229ebbd1c4c33b8d9870ad601f460c6e30`  
		Last Modified: Tue, 11 Jul 2023 04:47:34 GMT  
		Size: 6.0 KB (6017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dc85b4209f7c5902eaddc9237e35ff851834dbe9a46b12cda8f7c6bd37e98f0`  
		Last Modified: Tue, 11 Jul 2023 04:47:33 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:lts-mariadb-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:f2d58b0e807535f9a89d2aefdb36e0ed212696276c598c6ac7a44ae4a463571e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.8 MB (579836046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4827d8602436ba34af88ff0bccf958bc03dbf862b5011c12c3799c90dba3626a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:42:48 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:42:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:42:50 GMT
ADD file:262490f82459c14632f5c9a6d6a5cf6c07b4f307e8fd380fa764662cda46e88f in / 
# Wed, 28 Jun 2023 08:42:50 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:59 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 15:33:41 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 15:34:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 15:34:08 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 02:55:59 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 02:55:59 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 02:55:59 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 02:55:59 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 02:56:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 02:56:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 03:00:51 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 03:00:51 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 01:18:24 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 01:18:25 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 01:18:25 GMT
COPY dir:1743191a9534b9e7d795d3bf9ad18535d99e75967877447e17d7b63574d878d5 in /usr/local/tomcat 
# Tue, 11 Jul 2023 01:18:28 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 01:18:29 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 01:18:29 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 01:18:29 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 05:21:20 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 05:23:40 GMT
ENV XWIKI_VERSION=14.10.13
# Tue, 11 Jul 2023 05:23:40 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.13
# Tue, 11 Jul 2023 05:23:40 GMT
ENV XWIKI_DOWNLOAD_SHA256=5883ffdbc10865043778f3caa48fbca900129cf41c76ee6fdafba74769c928d4
# Tue, 11 Jul 2023 05:24:20 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 05:25:16 GMT
ENV MARIADB_JDBC_VERSION=3.1.4
# Tue, 11 Jul 2023 05:25:16 GMT
ENV MARIADB_JDBC_SHA256=eb88b5d727d82e25117e2b6fabcec1daf734633b0a576456c73215884c189ad4
# Tue, 11 Jul 2023 05:25:16 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.1.4
# Tue, 11 Jul 2023 05:25:16 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.1.4.jar
# Tue, 11 Jul 2023 05:25:17 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.1.4.jar
# Tue, 11 Jul 2023 05:25:17 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Tue, 11 Jul 2023 05:25:17 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 05:25:17 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 05:25:18 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 05:25:18 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 05:25:18 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 05:25:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 05:25:18 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:ac34a2e0269ced3acc355be706239ee0f3f1e73a035c40dd2fac74827164ee53`  
		Last Modified: Wed, 28 Jun 2023 23:23:40 GMT  
		Size: 28.4 MB (28391011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d9df805749ad7c4605f0d49a64da6a6173ab190ec361dc2063b6b73af59ab5`  
		Last Modified: Tue, 04 Jul 2023 15:36:55 GMT  
		Size: 12.5 MB (12455497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1e11a5919e5746092b2a288f71090ffdb0d3544b7b54c31ed0137e6d5d4735`  
		Last Modified: Tue, 04 Jul 2023 15:38:37 GMT  
		Size: 45.0 MB (45009079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80987dc89da28aa5ceec7a86ea74e13cee06ecd9304cf4c92d8f382c79eb4f2`  
		Last Modified: Tue, 04 Jul 2023 15:38:32 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de67c7824eef053da628456fe8aba244c4150024af9454dd4091763920d836c`  
		Last Modified: Wed, 05 Jul 2023 03:14:23 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f77f07e56c3d3019cd346deaeacbe572b15b26a924c19b6386877b47123a89e`  
		Last Modified: Tue, 11 Jul 2023 01:39:24 GMT  
		Size: 12.3 MB (12283700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2422cddd65b0ff63d783c999d005c42281720b8615f5872e1e8fdb32dd9981d9`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 455.1 KB (455052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b023f0d964d565a960e567dcaaa605fdff6da02b54971f4d0693506b481b8c`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28177f0763a75e5c940bb6a7919185effccd7cf14c0e350198b3aedbe1db789`  
		Last Modified: Tue, 11 Jul 2023 05:26:01 GMT  
		Size: 173.4 MB (173373450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc5b16765fdc498e3f3e0db1f6f5968716864f931b8490f2092985f2aad66e6`  
		Last Modified: Tue, 11 Jul 2023 05:27:47 GMT  
		Size: 307.3 MB (307261061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cde3b2925cca0eaeca051a9d34fc8559173eb81198be6edb87ef675ddbd104c`  
		Last Modified: Tue, 11 Jul 2023 05:28:44 GMT  
		Size: 594.6 KB (594553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a572ecd6de904372e67871760ea39b4c45f94b03c1bd47a6ee27a1151f44f25`  
		Last Modified: Tue, 11 Jul 2023 05:28:43 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48dc7acaf3762507fe63c6d484d73da83682cfc993ce96feccb9b0cb2bea8895`  
		Last Modified: Tue, 11 Jul 2023 05:28:43 GMT  
		Size: 2.3 KB (2314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd91b38c50762886b672122ce7698e839324aa39970db075d8fa1a46ae5d6fe5`  
		Last Modified: Tue, 11 Jul 2023 05:28:43 GMT  
		Size: 6.0 KB (6018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:536a460fc0ee741e1de6915eb0f7533df412ab1b9c51ac2f7686ca966abef1fc`  
		Last Modified: Tue, 11 Jul 2023 05:28:43 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:lts-mysql`

```console
$ docker pull xwiki@sha256:d684b69a373a2cef6fa2a32d55c3e87eed6a6f36cfac5320606e88204e88186a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:lts-mysql` - linux; amd64

```console
$ docker pull xwiki@sha256:ede13785f63dcaf8042ae3ad55c0c8fa410a3832504cdcf66916035506feebc9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.3 MB (590275216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0cdff4d327d68685f5dd8da61be21269df316c760ef6487e0aa642ec059b882`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:37:40 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:37:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:37:42 GMT
ADD file:140fb5108b4a2861b5718ad03b4a5174bba03589ea8d4c053e6a0b282f439ff3 in / 
# Wed, 28 Jun 2023 08:37:42 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:34:07 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:35:02 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 20:35:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 20:35:35 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 08:22:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 08:22:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 08:22:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 08:22:21 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 08:22:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:22:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:25:33 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 08:25:34 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 00:16:15 GMT
COPY dir:8ddeace4a16f09a0d97488e225c7b2e4a48c9a93484d24b46a09759f52800501 in /usr/local/tomcat 
# Tue, 11 Jul 2023 00:16:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 00:16:20 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 00:16:20 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 00:16:20 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 04:40:02 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 04:42:15 GMT
ENV XWIKI_VERSION=14.10.13
# Tue, 11 Jul 2023 04:42:15 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.13
# Tue, 11 Jul 2023 04:42:15 GMT
ENV XWIKI_DOWNLOAD_SHA256=5883ffdbc10865043778f3caa48fbca900129cf41c76ee6fdafba74769c928d4
# Tue, 11 Jul 2023 04:42:54 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 04:42:54 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Tue, 11 Jul 2023 04:42:55 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Tue, 11 Jul 2023 04:42:55 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Tue, 11 Jul 2023 04:42:55 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 04:42:55 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 04:42:56 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Tue, 11 Jul 2023 04:42:56 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 04:42:56 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 04:42:56 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 04:42:56 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 04:42:56 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 04:42:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 04:42:57 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:9d19ee268e0d7bcf6716e6658ee1b0384a71d6f2f9aa1ae2085610cf7c7b316f`  
		Last Modified: Wed, 28 Jun 2023 11:50:41 GMT  
		Size: 30.4 MB (30431229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32db0ad82863deaedd2f9a365e52f595085778d28bd1e6f1d351107590cad806`  
		Last Modified: Tue, 04 Jul 2023 20:39:05 GMT  
		Size: 12.5 MB (12495341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01bb55fbcae928d7e6c08d6618580d2b27ce6e46083f861bbed1e01db41c20b`  
		Last Modified: Tue, 04 Jul 2023 20:41:01 GMT  
		Size: 46.7 MB (46666353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297c6e3f57ee032a3cc5f0fd28b52687129e7a1e6485aea12aff08cb6620071e`  
		Last Modified: Tue, 04 Jul 2023 20:40:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15b01f5ab5b71b356d93dff08f5037af8e8a03b4657f1fd303052261161ebd8`  
		Last Modified: Wed, 05 Jul 2023 08:37:14 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c6051a2b9ffe906ea99b555033966c877468da73cd19fd793c86099d0af531`  
		Last Modified: Tue, 11 Jul 2023 00:38:45 GMT  
		Size: 12.3 MB (12274167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34aaed1f6a3460fc256e262b462c1180ccef1b0665ffd50f900d1ef9c19f1d24`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 454.7 KB (454674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b809bf54ada009dfd91afa6ad239f7a791807f2928941b7f969493ec38246be`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877cc60516baaeb7846bba5d5de9e491d0406cd2f43959d7d4e104d89df5e228`  
		Last Modified: Tue, 11 Jul 2023 04:44:49 GMT  
		Size: 178.3 MB (178335971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d83ab8708da1a9ab9fb6a48ac52687e3488789fccbd4a07ced23e73be97d1b`  
		Last Modified: Tue, 11 Jul 2023 04:46:37 GMT  
		Size: 307.3 MB (307261194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:663bd82ddfd62b4cf39556e967220c977dcdbb37a1fd053c779fd0baa6898818`  
		Last Modified: Tue, 11 Jul 2023 04:46:21 GMT  
		Size: 2.3 MB (2343668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed5bec13f08d98c63e3c81fb0a45f8734746d82b5504310835cac9e7a8e18dec`  
		Last Modified: Tue, 11 Jul 2023 04:46:21 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dfccb5d359b6e3ae2ddf7257f81d0e9b794f602ab4e3f3196c372af5543d1ca`  
		Last Modified: Tue, 11 Jul 2023 04:46:21 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac17a1dc4319814e728392d0b0b3ad40083d48efeaec075e52bdaef3545341d0`  
		Last Modified: Tue, 11 Jul 2023 04:46:21 GMT  
		Size: 6.0 KB (6015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57f2437b546ab6322d8db9cf14928c907568c9728574599d16ea306286ab824c`  
		Last Modified: Tue, 11 Jul 2023 04:46:21 GMT  
		Size: 2.5 KB (2498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:lts-mysql` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:2c70da3ff6aad987960017b1f402de397c9e9a3b3f806a125702c26c14a1bfb8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.6 MB (581585177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a5e15a24190e32ccad68b6a75aa965123ee8a3fd0edd724d8cbaecbcf34acf6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:42:48 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:42:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:42:50 GMT
ADD file:262490f82459c14632f5c9a6d6a5cf6c07b4f307e8fd380fa764662cda46e88f in / 
# Wed, 28 Jun 2023 08:42:50 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:59 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 15:33:41 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 15:34:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 15:34:08 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 02:55:59 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 02:55:59 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 02:55:59 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 02:55:59 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 02:56:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 02:56:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 03:00:51 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 03:00:51 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 01:18:24 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 01:18:25 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 01:18:25 GMT
COPY dir:1743191a9534b9e7d795d3bf9ad18535d99e75967877447e17d7b63574d878d5 in /usr/local/tomcat 
# Tue, 11 Jul 2023 01:18:28 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 01:18:29 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 01:18:29 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 01:18:29 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 05:21:20 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 05:23:40 GMT
ENV XWIKI_VERSION=14.10.13
# Tue, 11 Jul 2023 05:23:40 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.13
# Tue, 11 Jul 2023 05:23:40 GMT
ENV XWIKI_DOWNLOAD_SHA256=5883ffdbc10865043778f3caa48fbca900129cf41c76ee6fdafba74769c928d4
# Tue, 11 Jul 2023 05:24:20 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 05:24:23 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Tue, 11 Jul 2023 05:24:23 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Tue, 11 Jul 2023 05:24:23 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Tue, 11 Jul 2023 05:24:23 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 05:24:23 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 05:24:24 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Tue, 11 Jul 2023 05:24:24 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 05:24:24 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 05:24:25 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 05:24:25 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 05:24:25 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 05:24:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 05:24:25 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:ac34a2e0269ced3acc355be706239ee0f3f1e73a035c40dd2fac74827164ee53`  
		Last Modified: Wed, 28 Jun 2023 23:23:40 GMT  
		Size: 28.4 MB (28391011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d9df805749ad7c4605f0d49a64da6a6173ab190ec361dc2063b6b73af59ab5`  
		Last Modified: Tue, 04 Jul 2023 15:36:55 GMT  
		Size: 12.5 MB (12455497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1e11a5919e5746092b2a288f71090ffdb0d3544b7b54c31ed0137e6d5d4735`  
		Last Modified: Tue, 04 Jul 2023 15:38:37 GMT  
		Size: 45.0 MB (45009079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80987dc89da28aa5ceec7a86ea74e13cee06ecd9304cf4c92d8f382c79eb4f2`  
		Last Modified: Tue, 04 Jul 2023 15:38:32 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de67c7824eef053da628456fe8aba244c4150024af9454dd4091763920d836c`  
		Last Modified: Wed, 05 Jul 2023 03:14:23 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f77f07e56c3d3019cd346deaeacbe572b15b26a924c19b6386877b47123a89e`  
		Last Modified: Tue, 11 Jul 2023 01:39:24 GMT  
		Size: 12.3 MB (12283700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2422cddd65b0ff63d783c999d005c42281720b8615f5872e1e8fdb32dd9981d9`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 455.1 KB (455052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b023f0d964d565a960e567dcaaa605fdff6da02b54971f4d0693506b481b8c`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28177f0763a75e5c940bb6a7919185effccd7cf14c0e350198b3aedbe1db789`  
		Last Modified: Tue, 11 Jul 2023 05:26:01 GMT  
		Size: 173.4 MB (173373450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc5b16765fdc498e3f3e0db1f6f5968716864f931b8490f2092985f2aad66e6`  
		Last Modified: Tue, 11 Jul 2023 05:27:47 GMT  
		Size: 307.3 MB (307261061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e05260decea8ae0b8e52961a6b822e7f61aa0d94e359d9bdfb0a8d1c12ab373`  
		Last Modified: Tue, 11 Jul 2023 05:27:33 GMT  
		Size: 2.3 MB (2343684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80db78e6c67fd96e8da400c8505c850ac34058465e92e7c08c2079a56c581eef`  
		Last Modified: Tue, 11 Jul 2023 05:27:32 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e13d3d8f1788f25950792ca1b21389742cb964f69af7853cd12c938239fa7c94`  
		Last Modified: Tue, 11 Jul 2023 05:27:33 GMT  
		Size: 2.3 KB (2311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ecfdbab47ad32f6ddf82bd2c97ac1e2786af57d2bfc2653639b91c3a1833a3`  
		Last Modified: Tue, 11 Jul 2023 05:27:32 GMT  
		Size: 6.0 KB (6020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0b9874cce7da8c08bc10f43d1a239ff6d3d1b18189a83d61bf566a352cba781`  
		Last Modified: Tue, 11 Jul 2023 05:27:32 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:lts-mysql-tomcat`

```console
$ docker pull xwiki@sha256:d684b69a373a2cef6fa2a32d55c3e87eed6a6f36cfac5320606e88204e88186a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:lts-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:ede13785f63dcaf8042ae3ad55c0c8fa410a3832504cdcf66916035506feebc9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.3 MB (590275216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0cdff4d327d68685f5dd8da61be21269df316c760ef6487e0aa642ec059b882`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:37:40 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:37:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:37:42 GMT
ADD file:140fb5108b4a2861b5718ad03b4a5174bba03589ea8d4c053e6a0b282f439ff3 in / 
# Wed, 28 Jun 2023 08:37:42 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:34:07 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:35:02 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 20:35:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 20:35:35 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 08:22:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 08:22:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 08:22:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 08:22:21 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 08:22:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:22:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:25:33 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 08:25:34 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 00:16:15 GMT
COPY dir:8ddeace4a16f09a0d97488e225c7b2e4a48c9a93484d24b46a09759f52800501 in /usr/local/tomcat 
# Tue, 11 Jul 2023 00:16:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 00:16:20 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 00:16:20 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 00:16:20 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 04:40:02 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 04:42:15 GMT
ENV XWIKI_VERSION=14.10.13
# Tue, 11 Jul 2023 04:42:15 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.13
# Tue, 11 Jul 2023 04:42:15 GMT
ENV XWIKI_DOWNLOAD_SHA256=5883ffdbc10865043778f3caa48fbca900129cf41c76ee6fdafba74769c928d4
# Tue, 11 Jul 2023 04:42:54 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 04:42:54 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Tue, 11 Jul 2023 04:42:55 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Tue, 11 Jul 2023 04:42:55 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Tue, 11 Jul 2023 04:42:55 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 04:42:55 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 04:42:56 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Tue, 11 Jul 2023 04:42:56 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 04:42:56 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 04:42:56 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 04:42:56 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 04:42:56 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 04:42:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 04:42:57 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:9d19ee268e0d7bcf6716e6658ee1b0384a71d6f2f9aa1ae2085610cf7c7b316f`  
		Last Modified: Wed, 28 Jun 2023 11:50:41 GMT  
		Size: 30.4 MB (30431229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32db0ad82863deaedd2f9a365e52f595085778d28bd1e6f1d351107590cad806`  
		Last Modified: Tue, 04 Jul 2023 20:39:05 GMT  
		Size: 12.5 MB (12495341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01bb55fbcae928d7e6c08d6618580d2b27ce6e46083f861bbed1e01db41c20b`  
		Last Modified: Tue, 04 Jul 2023 20:41:01 GMT  
		Size: 46.7 MB (46666353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297c6e3f57ee032a3cc5f0fd28b52687129e7a1e6485aea12aff08cb6620071e`  
		Last Modified: Tue, 04 Jul 2023 20:40:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15b01f5ab5b71b356d93dff08f5037af8e8a03b4657f1fd303052261161ebd8`  
		Last Modified: Wed, 05 Jul 2023 08:37:14 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c6051a2b9ffe906ea99b555033966c877468da73cd19fd793c86099d0af531`  
		Last Modified: Tue, 11 Jul 2023 00:38:45 GMT  
		Size: 12.3 MB (12274167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34aaed1f6a3460fc256e262b462c1180ccef1b0665ffd50f900d1ef9c19f1d24`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 454.7 KB (454674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b809bf54ada009dfd91afa6ad239f7a791807f2928941b7f969493ec38246be`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877cc60516baaeb7846bba5d5de9e491d0406cd2f43959d7d4e104d89df5e228`  
		Last Modified: Tue, 11 Jul 2023 04:44:49 GMT  
		Size: 178.3 MB (178335971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d83ab8708da1a9ab9fb6a48ac52687e3488789fccbd4a07ced23e73be97d1b`  
		Last Modified: Tue, 11 Jul 2023 04:46:37 GMT  
		Size: 307.3 MB (307261194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:663bd82ddfd62b4cf39556e967220c977dcdbb37a1fd053c779fd0baa6898818`  
		Last Modified: Tue, 11 Jul 2023 04:46:21 GMT  
		Size: 2.3 MB (2343668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed5bec13f08d98c63e3c81fb0a45f8734746d82b5504310835cac9e7a8e18dec`  
		Last Modified: Tue, 11 Jul 2023 04:46:21 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dfccb5d359b6e3ae2ddf7257f81d0e9b794f602ab4e3f3196c372af5543d1ca`  
		Last Modified: Tue, 11 Jul 2023 04:46:21 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac17a1dc4319814e728392d0b0b3ad40083d48efeaec075e52bdaef3545341d0`  
		Last Modified: Tue, 11 Jul 2023 04:46:21 GMT  
		Size: 6.0 KB (6015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57f2437b546ab6322d8db9cf14928c907568c9728574599d16ea306286ab824c`  
		Last Modified: Tue, 11 Jul 2023 04:46:21 GMT  
		Size: 2.5 KB (2498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:lts-mysql-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:2c70da3ff6aad987960017b1f402de397c9e9a3b3f806a125702c26c14a1bfb8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.6 MB (581585177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a5e15a24190e32ccad68b6a75aa965123ee8a3fd0edd724d8cbaecbcf34acf6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:42:48 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:42:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:42:50 GMT
ADD file:262490f82459c14632f5c9a6d6a5cf6c07b4f307e8fd380fa764662cda46e88f in / 
# Wed, 28 Jun 2023 08:42:50 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:59 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 15:33:41 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 15:34:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 15:34:08 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 02:55:59 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 02:55:59 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 02:55:59 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 02:55:59 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 02:56:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 02:56:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 03:00:51 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 03:00:51 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 01:18:24 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 01:18:25 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 01:18:25 GMT
COPY dir:1743191a9534b9e7d795d3bf9ad18535d99e75967877447e17d7b63574d878d5 in /usr/local/tomcat 
# Tue, 11 Jul 2023 01:18:28 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 01:18:29 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 01:18:29 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 01:18:29 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 05:21:20 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 05:23:40 GMT
ENV XWIKI_VERSION=14.10.13
# Tue, 11 Jul 2023 05:23:40 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.13
# Tue, 11 Jul 2023 05:23:40 GMT
ENV XWIKI_DOWNLOAD_SHA256=5883ffdbc10865043778f3caa48fbca900129cf41c76ee6fdafba74769c928d4
# Tue, 11 Jul 2023 05:24:20 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 05:24:23 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Tue, 11 Jul 2023 05:24:23 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Tue, 11 Jul 2023 05:24:23 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Tue, 11 Jul 2023 05:24:23 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 05:24:23 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 05:24:24 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Tue, 11 Jul 2023 05:24:24 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 05:24:24 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 05:24:25 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 05:24:25 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 05:24:25 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 05:24:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 05:24:25 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:ac34a2e0269ced3acc355be706239ee0f3f1e73a035c40dd2fac74827164ee53`  
		Last Modified: Wed, 28 Jun 2023 23:23:40 GMT  
		Size: 28.4 MB (28391011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d9df805749ad7c4605f0d49a64da6a6173ab190ec361dc2063b6b73af59ab5`  
		Last Modified: Tue, 04 Jul 2023 15:36:55 GMT  
		Size: 12.5 MB (12455497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1e11a5919e5746092b2a288f71090ffdb0d3544b7b54c31ed0137e6d5d4735`  
		Last Modified: Tue, 04 Jul 2023 15:38:37 GMT  
		Size: 45.0 MB (45009079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80987dc89da28aa5ceec7a86ea74e13cee06ecd9304cf4c92d8f382c79eb4f2`  
		Last Modified: Tue, 04 Jul 2023 15:38:32 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de67c7824eef053da628456fe8aba244c4150024af9454dd4091763920d836c`  
		Last Modified: Wed, 05 Jul 2023 03:14:23 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f77f07e56c3d3019cd346deaeacbe572b15b26a924c19b6386877b47123a89e`  
		Last Modified: Tue, 11 Jul 2023 01:39:24 GMT  
		Size: 12.3 MB (12283700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2422cddd65b0ff63d783c999d005c42281720b8615f5872e1e8fdb32dd9981d9`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 455.1 KB (455052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b023f0d964d565a960e567dcaaa605fdff6da02b54971f4d0693506b481b8c`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28177f0763a75e5c940bb6a7919185effccd7cf14c0e350198b3aedbe1db789`  
		Last Modified: Tue, 11 Jul 2023 05:26:01 GMT  
		Size: 173.4 MB (173373450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc5b16765fdc498e3f3e0db1f6f5968716864f931b8490f2092985f2aad66e6`  
		Last Modified: Tue, 11 Jul 2023 05:27:47 GMT  
		Size: 307.3 MB (307261061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e05260decea8ae0b8e52961a6b822e7f61aa0d94e359d9bdfb0a8d1c12ab373`  
		Last Modified: Tue, 11 Jul 2023 05:27:33 GMT  
		Size: 2.3 MB (2343684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80db78e6c67fd96e8da400c8505c850ac34058465e92e7c08c2079a56c581eef`  
		Last Modified: Tue, 11 Jul 2023 05:27:32 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e13d3d8f1788f25950792ca1b21389742cb964f69af7853cd12c938239fa7c94`  
		Last Modified: Tue, 11 Jul 2023 05:27:33 GMT  
		Size: 2.3 KB (2311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ecfdbab47ad32f6ddf82bd2c97ac1e2786af57d2bfc2653639b91c3a1833a3`  
		Last Modified: Tue, 11 Jul 2023 05:27:32 GMT  
		Size: 6.0 KB (6020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0b9874cce7da8c08bc10f43d1a239ff6d3d1b18189a83d61bf566a352cba781`  
		Last Modified: Tue, 11 Jul 2023 05:27:32 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:lts-postgres`

```console
$ docker pull xwiki@sha256:32c79a7b00472757f10412ef3b239548c73e98a078012993d0d05d4c8ae24a90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:lts-postgres` - linux; amd64

```console
$ docker pull xwiki@sha256:d01097f47bf6df2a0da617f68c5ebfd8ff7ea70fdfa268248e85245ecac517e4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.8 MB (589808935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df679394031ff1d5971a374c7d42e0b63e4495b07ba1a6cfc13bb75e004aa28`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:37:40 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:37:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:37:42 GMT
ADD file:140fb5108b4a2861b5718ad03b4a5174bba03589ea8d4c053e6a0b282f439ff3 in / 
# Wed, 28 Jun 2023 08:37:42 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:34:07 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:35:02 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 20:35:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 20:35:35 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 08:22:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 08:22:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 08:22:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 08:22:21 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 08:22:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:22:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:25:33 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 08:25:34 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 00:16:15 GMT
COPY dir:8ddeace4a16f09a0d97488e225c7b2e4a48c9a93484d24b46a09759f52800501 in /usr/local/tomcat 
# Tue, 11 Jul 2023 00:16:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 00:16:20 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 00:16:20 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 00:16:20 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 04:41:24 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 04:43:04 GMT
ENV XWIKI_VERSION=14.10.13
# Tue, 11 Jul 2023 04:43:04 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.13
# Tue, 11 Jul 2023 04:43:04 GMT
ENV XWIKI_DOWNLOAD_SHA256=5883ffdbc10865043778f3caa48fbca900129cf41c76ee6fdafba74769c928d4
# Tue, 11 Jul 2023 04:43:42 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 04:43:44 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Tue, 11 Jul 2023 04:43:44 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 04:43:44 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 04:43:44 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 04:43:44 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 04:43:44 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 04:43:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 04:43:45 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:9d19ee268e0d7bcf6716e6658ee1b0384a71d6f2f9aa1ae2085610cf7c7b316f`  
		Last Modified: Wed, 28 Jun 2023 11:50:41 GMT  
		Size: 30.4 MB (30431229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32db0ad82863deaedd2f9a365e52f595085778d28bd1e6f1d351107590cad806`  
		Last Modified: Tue, 04 Jul 2023 20:39:05 GMT  
		Size: 12.5 MB (12495341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01bb55fbcae928d7e6c08d6618580d2b27ce6e46083f861bbed1e01db41c20b`  
		Last Modified: Tue, 04 Jul 2023 20:41:01 GMT  
		Size: 46.7 MB (46666353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297c6e3f57ee032a3cc5f0fd28b52687129e7a1e6485aea12aff08cb6620071e`  
		Last Modified: Tue, 04 Jul 2023 20:40:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15b01f5ab5b71b356d93dff08f5037af8e8a03b4657f1fd303052261161ebd8`  
		Last Modified: Wed, 05 Jul 2023 08:37:14 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c6051a2b9ffe906ea99b555033966c877468da73cd19fd793c86099d0af531`  
		Last Modified: Tue, 11 Jul 2023 00:38:45 GMT  
		Size: 12.3 MB (12274167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34aaed1f6a3460fc256e262b462c1180ccef1b0665ffd50f900d1ef9c19f1d24`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 454.7 KB (454674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b809bf54ada009dfd91afa6ad239f7a791807f2928941b7f969493ec38246be`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bd305e7867896df13faced03525a0f25bf1ac1b2a2c93e60382cdfd41c08e16`  
		Last Modified: Tue, 11 Jul 2023 04:45:43 GMT  
		Size: 179.3 MB (179276407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:241d47b2e9b47cfbb131cde5eef64788e51d1adc745cd086b858dcce53744f96`  
		Last Modified: Tue, 11 Jul 2023 04:47:17 GMT  
		Size: 307.3 MB (307261147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f4659e18fff023a31986cddf337f7070ad540e3f2f5d788844d96b7afe3e09a`  
		Last Modified: Tue, 11 Jul 2023 04:47:02 GMT  
		Size: 936.9 KB (936850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e59501fb2b56042afce97a149bbda1ccf3a5051fd5a37b1ea5ade709d470fbf`  
		Last Modified: Tue, 11 Jul 2023 04:47:01 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f06d08f1ecba9ed57618eb230d5e981c069e02d8828c2b1613c9b5a2183cdb`  
		Last Modified: Tue, 11 Jul 2023 04:47:01 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27996d6a7bfe148d65a59be70b8a3358db5db63098c6efb311675b3d3e686aef`  
		Last Modified: Tue, 11 Jul 2023 04:47:01 GMT  
		Size: 6.0 KB (6015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5d4d60c04deaa508f3eb56cb4e847396e6df7158d261b34d3898ef54f81f526`  
		Last Modified: Tue, 11 Jul 2023 04:47:02 GMT  
		Size: 2.5 KB (2500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:lts-postgres` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:966dfa46c0b58952823d9211ae493ea913edb22afe1aea49b60731e88ec9946b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.1 MB (581118361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f50afd98b0124061cd1380a5284513a88143aa86ccd826878235f8e45a5cc684`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:42:48 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:42:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:42:50 GMT
ADD file:262490f82459c14632f5c9a6d6a5cf6c07b4f307e8fd380fa764662cda46e88f in / 
# Wed, 28 Jun 2023 08:42:50 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:59 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 15:33:41 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 15:34:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 15:34:08 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 02:55:59 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 02:55:59 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 02:55:59 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 02:55:59 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 02:56:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 02:56:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 03:00:51 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 03:00:51 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 01:18:24 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 01:18:25 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 01:18:25 GMT
COPY dir:1743191a9534b9e7d795d3bf9ad18535d99e75967877447e17d7b63574d878d5 in /usr/local/tomcat 
# Tue, 11 Jul 2023 01:18:28 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 01:18:29 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 01:18:29 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 01:18:29 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 05:22:36 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 05:24:28 GMT
ENV XWIKI_VERSION=14.10.13
# Tue, 11 Jul 2023 05:24:28 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.13
# Tue, 11 Jul 2023 05:24:28 GMT
ENV XWIKI_DOWNLOAD_SHA256=5883ffdbc10865043778f3caa48fbca900129cf41c76ee6fdafba74769c928d4
# Tue, 11 Jul 2023 05:25:08 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 05:25:11 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Tue, 11 Jul 2023 05:25:11 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 05:25:11 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 05:25:11 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 05:25:11 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 05:25:11 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 05:25:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 05:25:11 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:ac34a2e0269ced3acc355be706239ee0f3f1e73a035c40dd2fac74827164ee53`  
		Last Modified: Wed, 28 Jun 2023 23:23:40 GMT  
		Size: 28.4 MB (28391011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d9df805749ad7c4605f0d49a64da6a6173ab190ec361dc2063b6b73af59ab5`  
		Last Modified: Tue, 04 Jul 2023 15:36:55 GMT  
		Size: 12.5 MB (12455497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1e11a5919e5746092b2a288f71090ffdb0d3544b7b54c31ed0137e6d5d4735`  
		Last Modified: Tue, 04 Jul 2023 15:38:37 GMT  
		Size: 45.0 MB (45009079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80987dc89da28aa5ceec7a86ea74e13cee06ecd9304cf4c92d8f382c79eb4f2`  
		Last Modified: Tue, 04 Jul 2023 15:38:32 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de67c7824eef053da628456fe8aba244c4150024af9454dd4091763920d836c`  
		Last Modified: Wed, 05 Jul 2023 03:14:23 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f77f07e56c3d3019cd346deaeacbe572b15b26a924c19b6386877b47123a89e`  
		Last Modified: Tue, 11 Jul 2023 01:39:24 GMT  
		Size: 12.3 MB (12283700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2422cddd65b0ff63d783c999d005c42281720b8615f5872e1e8fdb32dd9981d9`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 455.1 KB (455052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b023f0d964d565a960e567dcaaa605fdff6da02b54971f4d0693506b481b8c`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:968d46d099e01403854799f31b6235698a474c27fd58b0172b1eb3889cd5067f`  
		Last Modified: Tue, 11 Jul 2023 05:26:50 GMT  
		Size: 174.3 MB (174313369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58c2e2d1a49c77dd7a2b5e47670a35d29aca6a19183b43226d929ab037e2cf4a`  
		Last Modified: Tue, 11 Jul 2023 05:28:26 GMT  
		Size: 307.3 MB (307261017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48ff25a83276ff7bee5e0cc9402d6b809cee66bd4e22515f9e4ebf33a5f98d54`  
		Last Modified: Tue, 11 Jul 2023 05:28:12 GMT  
		Size: 936.9 KB (936850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a430a5f61ae1c957b6abf407c502bbac7994125fec841c264e73b3570ca318b`  
		Last Modified: Tue, 11 Jul 2023 05:28:12 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1a1106197e50baaa0b1e4612ce7252b217213ebdc52808529790aec8db034d`  
		Last Modified: Tue, 11 Jul 2023 05:28:12 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84d0854ce2eb5e1ce140a35ba96b4870e229a0bcc691cac48550a44dafbe83d1`  
		Last Modified: Tue, 11 Jul 2023 05:28:12 GMT  
		Size: 6.0 KB (6019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b30724798e976582c41b18d0c093767d1a9df69f9a34b9d57bbf90c21634feff`  
		Last Modified: Tue, 11 Jul 2023 05:28:12 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:lts-postgres-tomcat`

```console
$ docker pull xwiki@sha256:32c79a7b00472757f10412ef3b239548c73e98a078012993d0d05d4c8ae24a90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:lts-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:d01097f47bf6df2a0da617f68c5ebfd8ff7ea70fdfa268248e85245ecac517e4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.8 MB (589808935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df679394031ff1d5971a374c7d42e0b63e4495b07ba1a6cfc13bb75e004aa28`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:37:40 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:37:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:37:42 GMT
ADD file:140fb5108b4a2861b5718ad03b4a5174bba03589ea8d4c053e6a0b282f439ff3 in / 
# Wed, 28 Jun 2023 08:37:42 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:34:07 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:35:02 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 20:35:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 20:35:35 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 08:22:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 08:22:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 08:22:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 08:22:21 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 08:22:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:22:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:25:33 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 08:25:34 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 00:16:15 GMT
COPY dir:8ddeace4a16f09a0d97488e225c7b2e4a48c9a93484d24b46a09759f52800501 in /usr/local/tomcat 
# Tue, 11 Jul 2023 00:16:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 00:16:20 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 00:16:20 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 00:16:20 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 04:41:24 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 04:43:04 GMT
ENV XWIKI_VERSION=14.10.13
# Tue, 11 Jul 2023 04:43:04 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.13
# Tue, 11 Jul 2023 04:43:04 GMT
ENV XWIKI_DOWNLOAD_SHA256=5883ffdbc10865043778f3caa48fbca900129cf41c76ee6fdafba74769c928d4
# Tue, 11 Jul 2023 04:43:42 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 04:43:44 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Tue, 11 Jul 2023 04:43:44 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 04:43:44 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 04:43:44 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 04:43:44 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 04:43:44 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 04:43:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 04:43:45 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:9d19ee268e0d7bcf6716e6658ee1b0384a71d6f2f9aa1ae2085610cf7c7b316f`  
		Last Modified: Wed, 28 Jun 2023 11:50:41 GMT  
		Size: 30.4 MB (30431229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32db0ad82863deaedd2f9a365e52f595085778d28bd1e6f1d351107590cad806`  
		Last Modified: Tue, 04 Jul 2023 20:39:05 GMT  
		Size: 12.5 MB (12495341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01bb55fbcae928d7e6c08d6618580d2b27ce6e46083f861bbed1e01db41c20b`  
		Last Modified: Tue, 04 Jul 2023 20:41:01 GMT  
		Size: 46.7 MB (46666353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297c6e3f57ee032a3cc5f0fd28b52687129e7a1e6485aea12aff08cb6620071e`  
		Last Modified: Tue, 04 Jul 2023 20:40:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15b01f5ab5b71b356d93dff08f5037af8e8a03b4657f1fd303052261161ebd8`  
		Last Modified: Wed, 05 Jul 2023 08:37:14 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c6051a2b9ffe906ea99b555033966c877468da73cd19fd793c86099d0af531`  
		Last Modified: Tue, 11 Jul 2023 00:38:45 GMT  
		Size: 12.3 MB (12274167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34aaed1f6a3460fc256e262b462c1180ccef1b0665ffd50f900d1ef9c19f1d24`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 454.7 KB (454674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b809bf54ada009dfd91afa6ad239f7a791807f2928941b7f969493ec38246be`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bd305e7867896df13faced03525a0f25bf1ac1b2a2c93e60382cdfd41c08e16`  
		Last Modified: Tue, 11 Jul 2023 04:45:43 GMT  
		Size: 179.3 MB (179276407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:241d47b2e9b47cfbb131cde5eef64788e51d1adc745cd086b858dcce53744f96`  
		Last Modified: Tue, 11 Jul 2023 04:47:17 GMT  
		Size: 307.3 MB (307261147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f4659e18fff023a31986cddf337f7070ad540e3f2f5d788844d96b7afe3e09a`  
		Last Modified: Tue, 11 Jul 2023 04:47:02 GMT  
		Size: 936.9 KB (936850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e59501fb2b56042afce97a149bbda1ccf3a5051fd5a37b1ea5ade709d470fbf`  
		Last Modified: Tue, 11 Jul 2023 04:47:01 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f06d08f1ecba9ed57618eb230d5e981c069e02d8828c2b1613c9b5a2183cdb`  
		Last Modified: Tue, 11 Jul 2023 04:47:01 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27996d6a7bfe148d65a59be70b8a3358db5db63098c6efb311675b3d3e686aef`  
		Last Modified: Tue, 11 Jul 2023 04:47:01 GMT  
		Size: 6.0 KB (6015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5d4d60c04deaa508f3eb56cb4e847396e6df7158d261b34d3898ef54f81f526`  
		Last Modified: Tue, 11 Jul 2023 04:47:02 GMT  
		Size: 2.5 KB (2500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:lts-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:966dfa46c0b58952823d9211ae493ea913edb22afe1aea49b60731e88ec9946b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.1 MB (581118361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f50afd98b0124061cd1380a5284513a88143aa86ccd826878235f8e45a5cc684`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:42:48 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:42:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:42:50 GMT
ADD file:262490f82459c14632f5c9a6d6a5cf6c07b4f307e8fd380fa764662cda46e88f in / 
# Wed, 28 Jun 2023 08:42:50 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:59 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 15:33:41 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 15:34:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 15:34:08 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 02:55:59 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 02:55:59 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 02:55:59 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 02:55:59 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 02:56:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 02:56:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 03:00:51 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 03:00:51 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 01:18:24 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 01:18:25 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 01:18:25 GMT
COPY dir:1743191a9534b9e7d795d3bf9ad18535d99e75967877447e17d7b63574d878d5 in /usr/local/tomcat 
# Tue, 11 Jul 2023 01:18:28 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 01:18:29 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 01:18:29 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 01:18:29 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 05:22:36 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 05:24:28 GMT
ENV XWIKI_VERSION=14.10.13
# Tue, 11 Jul 2023 05:24:28 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.13
# Tue, 11 Jul 2023 05:24:28 GMT
ENV XWIKI_DOWNLOAD_SHA256=5883ffdbc10865043778f3caa48fbca900129cf41c76ee6fdafba74769c928d4
# Tue, 11 Jul 2023 05:25:08 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 05:25:11 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Tue, 11 Jul 2023 05:25:11 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 05:25:11 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 05:25:11 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 05:25:11 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 05:25:11 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 05:25:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 05:25:11 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:ac34a2e0269ced3acc355be706239ee0f3f1e73a035c40dd2fac74827164ee53`  
		Last Modified: Wed, 28 Jun 2023 23:23:40 GMT  
		Size: 28.4 MB (28391011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d9df805749ad7c4605f0d49a64da6a6173ab190ec361dc2063b6b73af59ab5`  
		Last Modified: Tue, 04 Jul 2023 15:36:55 GMT  
		Size: 12.5 MB (12455497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1e11a5919e5746092b2a288f71090ffdb0d3544b7b54c31ed0137e6d5d4735`  
		Last Modified: Tue, 04 Jul 2023 15:38:37 GMT  
		Size: 45.0 MB (45009079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80987dc89da28aa5ceec7a86ea74e13cee06ecd9304cf4c92d8f382c79eb4f2`  
		Last Modified: Tue, 04 Jul 2023 15:38:32 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de67c7824eef053da628456fe8aba244c4150024af9454dd4091763920d836c`  
		Last Modified: Wed, 05 Jul 2023 03:14:23 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f77f07e56c3d3019cd346deaeacbe572b15b26a924c19b6386877b47123a89e`  
		Last Modified: Tue, 11 Jul 2023 01:39:24 GMT  
		Size: 12.3 MB (12283700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2422cddd65b0ff63d783c999d005c42281720b8615f5872e1e8fdb32dd9981d9`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 455.1 KB (455052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b023f0d964d565a960e567dcaaa605fdff6da02b54971f4d0693506b481b8c`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:968d46d099e01403854799f31b6235698a474c27fd58b0172b1eb3889cd5067f`  
		Last Modified: Tue, 11 Jul 2023 05:26:50 GMT  
		Size: 174.3 MB (174313369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58c2e2d1a49c77dd7a2b5e47670a35d29aca6a19183b43226d929ab037e2cf4a`  
		Last Modified: Tue, 11 Jul 2023 05:28:26 GMT  
		Size: 307.3 MB (307261017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48ff25a83276ff7bee5e0cc9402d6b809cee66bd4e22515f9e4ebf33a5f98d54`  
		Last Modified: Tue, 11 Jul 2023 05:28:12 GMT  
		Size: 936.9 KB (936850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a430a5f61ae1c957b6abf407c502bbac7994125fec841c264e73b3570ca318b`  
		Last Modified: Tue, 11 Jul 2023 05:28:12 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1a1106197e50baaa0b1e4612ce7252b217213ebdc52808529790aec8db034d`  
		Last Modified: Tue, 11 Jul 2023 05:28:12 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84d0854ce2eb5e1ce140a35ba96b4870e229a0bcc691cac48550a44dafbe83d1`  
		Last Modified: Tue, 11 Jul 2023 05:28:12 GMT  
		Size: 6.0 KB (6019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b30724798e976582c41b18d0c093767d1a9df69f9a34b9d57bbf90c21634feff`  
		Last Modified: Tue, 11 Jul 2023 05:28:12 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:mariadb-tomcat`

```console
$ docker pull xwiki@sha256:d447b71c1f3084c255c2effee1762e635e6e07f08edcc0bd5b9c46d892350483
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:mariadb-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:6ece9caf8c15d2557f7f165d530deb3442aae7b1bb3b968ba2236e987cebbe2d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **585.5 MB (585501648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac976c622edabab4c9f4be5e6b071f4be6640e98d657487308bb3bb030921d13`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:37:40 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:37:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:37:42 GMT
ADD file:140fb5108b4a2861b5718ad03b4a5174bba03589ea8d4c053e6a0b282f439ff3 in / 
# Wed, 28 Jun 2023 08:37:42 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:34:07 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:35:02 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 20:35:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 20:35:35 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 08:22:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 08:22:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 08:22:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 08:22:21 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 08:22:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:22:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:25:33 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 08:25:34 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 00:16:15 GMT
COPY dir:8ddeace4a16f09a0d97488e225c7b2e4a48c9a93484d24b46a09759f52800501 in /usr/local/tomcat 
# Tue, 11 Jul 2023 00:16:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 00:16:20 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 00:16:20 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 00:16:20 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 04:40:02 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 04:40:03 GMT
ENV XWIKI_VERSION=15.5
# Tue, 11 Jul 2023 04:40:03 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.5
# Tue, 11 Jul 2023 04:40:03 GMT
ENV XWIKI_DOWNLOAD_SHA256=e552586d371da33b012cfbd974b3ba80d1b147a5c892ad6cf989960212cdaa02
# Tue, 11 Jul 2023 04:40:41 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 04:42:10 GMT
ENV MARIADB_JDBC_VERSION=3.1.4
# Tue, 11 Jul 2023 04:42:10 GMT
ENV MARIADB_JDBC_SHA256=eb88b5d727d82e25117e2b6fabcec1daf734633b0a576456c73215884c189ad4
# Tue, 11 Jul 2023 04:42:10 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.1.4
# Tue, 11 Jul 2023 04:42:10 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.1.4.jar
# Tue, 11 Jul 2023 04:42:10 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.1.4.jar
# Tue, 11 Jul 2023 04:42:11 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Tue, 11 Jul 2023 04:42:11 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 04:42:11 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 04:42:12 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 04:42:12 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 04:42:12 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 04:42:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 04:42:12 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:9d19ee268e0d7bcf6716e6658ee1b0384a71d6f2f9aa1ae2085610cf7c7b316f`  
		Last Modified: Wed, 28 Jun 2023 11:50:41 GMT  
		Size: 30.4 MB (30431229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32db0ad82863deaedd2f9a365e52f595085778d28bd1e6f1d351107590cad806`  
		Last Modified: Tue, 04 Jul 2023 20:39:05 GMT  
		Size: 12.5 MB (12495341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01bb55fbcae928d7e6c08d6618580d2b27ce6e46083f861bbed1e01db41c20b`  
		Last Modified: Tue, 04 Jul 2023 20:41:01 GMT  
		Size: 46.7 MB (46666353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297c6e3f57ee032a3cc5f0fd28b52687129e7a1e6485aea12aff08cb6620071e`  
		Last Modified: Tue, 04 Jul 2023 20:40:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15b01f5ab5b71b356d93dff08f5037af8e8a03b4657f1fd303052261161ebd8`  
		Last Modified: Wed, 05 Jul 2023 08:37:14 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c6051a2b9ffe906ea99b555033966c877468da73cd19fd793c86099d0af531`  
		Last Modified: Tue, 11 Jul 2023 00:38:45 GMT  
		Size: 12.3 MB (12274167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34aaed1f6a3460fc256e262b462c1180ccef1b0665ffd50f900d1ef9c19f1d24`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 454.7 KB (454674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b809bf54ada009dfd91afa6ad239f7a791807f2928941b7f969493ec38246be`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877cc60516baaeb7846bba5d5de9e491d0406cd2f43959d7d4e104d89df5e228`  
		Last Modified: Tue, 11 Jul 2023 04:44:49 GMT  
		Size: 178.3 MB (178335971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b863cfbbf93cec3814eec01a334529779a02fcbb3cdff4e2d212bb70287a5720`  
		Last Modified: Tue, 11 Jul 2023 04:44:42 GMT  
		Size: 304.2 MB (304236736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d9f121998f3ebb1fe9d8b1e2b7964a6e19afe2500ee4c64b95739f1578f0728`  
		Last Modified: Tue, 11 Jul 2023 04:46:03 GMT  
		Size: 594.6 KB (594553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b2c8c7e34dbea6b864808d65dae2a48aaa73e9595b3dd30f14d4b95b28cbcf`  
		Last Modified: Tue, 11 Jul 2023 04:46:03 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84634ee1814641c052e3b568592a22c625bc82aaf05fdb64d6dcbdb17ff803b7`  
		Last Modified: Tue, 11 Jul 2023 04:46:03 GMT  
		Size: 2.3 KB (2311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f62b3d21969533fa11c23f989db62def095f4c38f4e3ebba9bdb897cb756a783`  
		Last Modified: Tue, 11 Jul 2023 04:46:03 GMT  
		Size: 6.0 KB (6003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d136eed865c53c0489a1100cd4c540d7269e0bbc620b8b44fa3c71d168a0e583`  
		Last Modified: Tue, 11 Jul 2023 04:46:03 GMT  
		Size: 2.5 KB (2503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:mariadb-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:2745b46e135b629961fa0abba943bcd28e8793d51275fbf2d1a945545b31961b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **576.8 MB (576811676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa8facaf677aa5a99371bfdf03feab6977a37475e6664e98cdef94878d40484c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:42:48 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:42:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:42:50 GMT
ADD file:262490f82459c14632f5c9a6d6a5cf6c07b4f307e8fd380fa764662cda46e88f in / 
# Wed, 28 Jun 2023 08:42:50 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:59 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 15:33:41 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 15:34:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 15:34:08 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 02:55:59 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 02:55:59 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 02:55:59 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 02:55:59 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 02:56:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 02:56:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 03:00:51 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 03:00:51 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 01:18:24 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 01:18:25 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 01:18:25 GMT
COPY dir:1743191a9534b9e7d795d3bf9ad18535d99e75967877447e17d7b63574d878d5 in /usr/local/tomcat 
# Tue, 11 Jul 2023 01:18:28 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 01:18:29 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 01:18:29 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 01:18:29 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 05:21:20 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 05:21:23 GMT
ENV XWIKI_VERSION=15.5
# Tue, 11 Jul 2023 05:21:23 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.5
# Tue, 11 Jul 2023 05:21:23 GMT
ENV XWIKI_DOWNLOAD_SHA256=e552586d371da33b012cfbd974b3ba80d1b147a5c892ad6cf989960212cdaa02
# Tue, 11 Jul 2023 05:22:02 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 05:23:36 GMT
ENV MARIADB_JDBC_VERSION=3.1.4
# Tue, 11 Jul 2023 05:23:36 GMT
ENV MARIADB_JDBC_SHA256=eb88b5d727d82e25117e2b6fabcec1daf734633b0a576456c73215884c189ad4
# Tue, 11 Jul 2023 05:23:36 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.1.4
# Tue, 11 Jul 2023 05:23:37 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.1.4.jar
# Tue, 11 Jul 2023 05:23:37 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.1.4.jar
# Tue, 11 Jul 2023 05:23:37 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Tue, 11 Jul 2023 05:23:37 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 05:23:37 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 05:23:38 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 05:23:38 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 05:23:38 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 05:23:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 05:23:38 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:ac34a2e0269ced3acc355be706239ee0f3f1e73a035c40dd2fac74827164ee53`  
		Last Modified: Wed, 28 Jun 2023 23:23:40 GMT  
		Size: 28.4 MB (28391011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d9df805749ad7c4605f0d49a64da6a6173ab190ec361dc2063b6b73af59ab5`  
		Last Modified: Tue, 04 Jul 2023 15:36:55 GMT  
		Size: 12.5 MB (12455497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1e11a5919e5746092b2a288f71090ffdb0d3544b7b54c31ed0137e6d5d4735`  
		Last Modified: Tue, 04 Jul 2023 15:38:37 GMT  
		Size: 45.0 MB (45009079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80987dc89da28aa5ceec7a86ea74e13cee06ecd9304cf4c92d8f382c79eb4f2`  
		Last Modified: Tue, 04 Jul 2023 15:38:32 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de67c7824eef053da628456fe8aba244c4150024af9454dd4091763920d836c`  
		Last Modified: Wed, 05 Jul 2023 03:14:23 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f77f07e56c3d3019cd346deaeacbe572b15b26a924c19b6386877b47123a89e`  
		Last Modified: Tue, 11 Jul 2023 01:39:24 GMT  
		Size: 12.3 MB (12283700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2422cddd65b0ff63d783c999d005c42281720b8615f5872e1e8fdb32dd9981d9`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 455.1 KB (455052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b023f0d964d565a960e567dcaaa605fdff6da02b54971f4d0693506b481b8c`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28177f0763a75e5c940bb6a7919185effccd7cf14c0e350198b3aedbe1db789`  
		Last Modified: Tue, 11 Jul 2023 05:26:01 GMT  
		Size: 173.4 MB (173373450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b39c7f4340aa5dd678a6a0a9bc018229eaadb2a94a0af6bc41d17ce77cdefb`  
		Last Modified: Tue, 11 Jul 2023 05:25:57 GMT  
		Size: 304.2 MB (304236707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0be5f78ca514976c969b47013a6e82418af20d755526a18e35388d7482170b8`  
		Last Modified: Tue, 11 Jul 2023 05:27:14 GMT  
		Size: 594.6 KB (594556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01372195bd2be58e8f5f6433314edfd376c3ce7d69fe9fc1b21188af306f2ce1`  
		Last Modified: Tue, 11 Jul 2023 05:27:14 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15366f793a0d945e4ef67931cb193ae8c2b7f218ecba840af9cf4958adb81ce8`  
		Last Modified: Tue, 11 Jul 2023 05:27:14 GMT  
		Size: 2.3 KB (2312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae0ba8487202e29a15c7c1b505e9f148753e98c7e9284bb88ab357269ef43ab`  
		Last Modified: Tue, 11 Jul 2023 05:27:14 GMT  
		Size: 6.0 KB (6004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4d894785e0d9bda2444090848544b861a5280bd4c8a3e5686acc3d6f3f232fe`  
		Last Modified: Tue, 11 Jul 2023 05:27:14 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:mysql-tomcat`

```console
$ docker pull xwiki@sha256:66e25eb51a5a079e68e523ac98a46358b70c8c431f4360e1565d23aead7eaa3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:80718cf2818aac2523383b177893d1f4454722abe547ec303a18e3b4a30362b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **587.3 MB (587250774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97a5a7f1172dd3ea626947d13678241c2e0f4e5391c13ab4c32dd3f009d902c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:37:40 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:37:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:37:42 GMT
ADD file:140fb5108b4a2861b5718ad03b4a5174bba03589ea8d4c053e6a0b282f439ff3 in / 
# Wed, 28 Jun 2023 08:37:42 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:34:07 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:35:02 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 20:35:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 20:35:35 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 08:22:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 08:22:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 08:22:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 08:22:21 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 08:22:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:22:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:25:33 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 08:25:34 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 00:16:15 GMT
COPY dir:8ddeace4a16f09a0d97488e225c7b2e4a48c9a93484d24b46a09759f52800501 in /usr/local/tomcat 
# Tue, 11 Jul 2023 00:16:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 00:16:20 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 00:16:20 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 00:16:20 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 04:40:02 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 04:40:03 GMT
ENV XWIKI_VERSION=15.5
# Tue, 11 Jul 2023 04:40:03 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.5
# Tue, 11 Jul 2023 04:40:03 GMT
ENV XWIKI_DOWNLOAD_SHA256=e552586d371da33b012cfbd974b3ba80d1b147a5c892ad6cf989960212cdaa02
# Tue, 11 Jul 2023 04:40:41 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 04:40:42 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Tue, 11 Jul 2023 04:40:42 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Tue, 11 Jul 2023 04:40:42 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Tue, 11 Jul 2023 04:40:42 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 04:40:42 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 04:40:43 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Tue, 11 Jul 2023 04:40:43 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 04:40:43 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 04:40:44 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 04:40:44 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 04:40:44 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 04:40:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 04:40:44 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:9d19ee268e0d7bcf6716e6658ee1b0384a71d6f2f9aa1ae2085610cf7c7b316f`  
		Last Modified: Wed, 28 Jun 2023 11:50:41 GMT  
		Size: 30.4 MB (30431229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32db0ad82863deaedd2f9a365e52f595085778d28bd1e6f1d351107590cad806`  
		Last Modified: Tue, 04 Jul 2023 20:39:05 GMT  
		Size: 12.5 MB (12495341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01bb55fbcae928d7e6c08d6618580d2b27ce6e46083f861bbed1e01db41c20b`  
		Last Modified: Tue, 04 Jul 2023 20:41:01 GMT  
		Size: 46.7 MB (46666353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297c6e3f57ee032a3cc5f0fd28b52687129e7a1e6485aea12aff08cb6620071e`  
		Last Modified: Tue, 04 Jul 2023 20:40:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15b01f5ab5b71b356d93dff08f5037af8e8a03b4657f1fd303052261161ebd8`  
		Last Modified: Wed, 05 Jul 2023 08:37:14 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c6051a2b9ffe906ea99b555033966c877468da73cd19fd793c86099d0af531`  
		Last Modified: Tue, 11 Jul 2023 00:38:45 GMT  
		Size: 12.3 MB (12274167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34aaed1f6a3460fc256e262b462c1180ccef1b0665ffd50f900d1ef9c19f1d24`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 454.7 KB (454674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b809bf54ada009dfd91afa6ad239f7a791807f2928941b7f969493ec38246be`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877cc60516baaeb7846bba5d5de9e491d0406cd2f43959d7d4e104d89df5e228`  
		Last Modified: Tue, 11 Jul 2023 04:44:49 GMT  
		Size: 178.3 MB (178335971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b863cfbbf93cec3814eec01a334529779a02fcbb3cdff4e2d212bb70287a5720`  
		Last Modified: Tue, 11 Jul 2023 04:44:42 GMT  
		Size: 304.2 MB (304236736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faad5f8d2320ee7d3eb3c3f81aff36754d147687cdb520bc8b24d3170bfcee58`  
		Last Modified: Tue, 11 Jul 2023 04:44:25 GMT  
		Size: 2.3 MB (2343679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ad43407c01ec5371102aaa125c19fb5399f629346a71d4913d742cfed44165`  
		Last Modified: Tue, 11 Jul 2023 04:44:24 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03112af3cb3ddf2e651a23fd879dd50f96a17b20d580105c90d7bb357f02ab0a`  
		Last Modified: Tue, 11 Jul 2023 04:44:24 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7098881bee3a8920bec6f5c352be02657d02e5bb3a4ce69faa81f9354193acbf`  
		Last Modified: Tue, 11 Jul 2023 04:44:24 GMT  
		Size: 6.0 KB (6004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:880ec6a5100b3effc0772c9e06afdfdab1786151d59c78eb30826e0245f2ebe5`  
		Last Modified: Tue, 11 Jul 2023 04:44:24 GMT  
		Size: 2.5 KB (2507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:mysql-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:80454bf7fba586e95357c0d982c52ab2d1504e85c6d085e14a1091a19a0d7e65
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.6 MB (578560793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e24eddde7707953934d4ceba63f6297ff5115dc6ec8e8e39946e4f8bd2542c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:42:48 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:42:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:42:50 GMT
ADD file:262490f82459c14632f5c9a6d6a5cf6c07b4f307e8fd380fa764662cda46e88f in / 
# Wed, 28 Jun 2023 08:42:50 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:59 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 15:33:41 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 15:34:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 15:34:08 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 02:55:59 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 02:55:59 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 02:55:59 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 02:55:59 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 02:56:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 02:56:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 03:00:51 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 03:00:51 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 01:18:24 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 01:18:25 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 01:18:25 GMT
COPY dir:1743191a9534b9e7d795d3bf9ad18535d99e75967877447e17d7b63574d878d5 in /usr/local/tomcat 
# Tue, 11 Jul 2023 01:18:28 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 01:18:29 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 01:18:29 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 01:18:29 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 05:21:20 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 05:21:23 GMT
ENV XWIKI_VERSION=15.5
# Tue, 11 Jul 2023 05:21:23 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.5
# Tue, 11 Jul 2023 05:21:23 GMT
ENV XWIKI_DOWNLOAD_SHA256=e552586d371da33b012cfbd974b3ba80d1b147a5c892ad6cf989960212cdaa02
# Tue, 11 Jul 2023 05:22:02 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 05:22:04 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Tue, 11 Jul 2023 05:22:04 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Tue, 11 Jul 2023 05:22:04 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Tue, 11 Jul 2023 05:22:04 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 05:22:04 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 05:22:05 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Tue, 11 Jul 2023 05:22:06 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 05:22:06 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 05:22:06 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 05:22:06 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 05:22:06 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 05:22:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 05:22:06 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:ac34a2e0269ced3acc355be706239ee0f3f1e73a035c40dd2fac74827164ee53`  
		Last Modified: Wed, 28 Jun 2023 23:23:40 GMT  
		Size: 28.4 MB (28391011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d9df805749ad7c4605f0d49a64da6a6173ab190ec361dc2063b6b73af59ab5`  
		Last Modified: Tue, 04 Jul 2023 15:36:55 GMT  
		Size: 12.5 MB (12455497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1e11a5919e5746092b2a288f71090ffdb0d3544b7b54c31ed0137e6d5d4735`  
		Last Modified: Tue, 04 Jul 2023 15:38:37 GMT  
		Size: 45.0 MB (45009079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80987dc89da28aa5ceec7a86ea74e13cee06ecd9304cf4c92d8f382c79eb4f2`  
		Last Modified: Tue, 04 Jul 2023 15:38:32 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de67c7824eef053da628456fe8aba244c4150024af9454dd4091763920d836c`  
		Last Modified: Wed, 05 Jul 2023 03:14:23 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f77f07e56c3d3019cd346deaeacbe572b15b26a924c19b6386877b47123a89e`  
		Last Modified: Tue, 11 Jul 2023 01:39:24 GMT  
		Size: 12.3 MB (12283700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2422cddd65b0ff63d783c999d005c42281720b8615f5872e1e8fdb32dd9981d9`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 455.1 KB (455052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b023f0d964d565a960e567dcaaa605fdff6da02b54971f4d0693506b481b8c`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28177f0763a75e5c940bb6a7919185effccd7cf14c0e350198b3aedbe1db789`  
		Last Modified: Tue, 11 Jul 2023 05:26:01 GMT  
		Size: 173.4 MB (173373450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b39c7f4340aa5dd678a6a0a9bc018229eaadb2a94a0af6bc41d17ce77cdefb`  
		Last Modified: Tue, 11 Jul 2023 05:25:57 GMT  
		Size: 304.2 MB (304236707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc58f6eb776423b78c7a88af6ee221317c44f67e3fb4f413ef3823e8895288a2`  
		Last Modified: Tue, 11 Jul 2023 05:25:43 GMT  
		Size: 2.3 MB (2343673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea5e5502a3de7ec04368cbbb5f6c48f21fc7eac2657e2376ab3c7271ad4f85d`  
		Last Modified: Tue, 11 Jul 2023 05:25:43 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f8adcd32841dea1f4e39476b790a663510401829d69a806cad6007452d0367`  
		Last Modified: Tue, 11 Jul 2023 05:25:43 GMT  
		Size: 2.3 KB (2310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa238d29e18bbc7bdc963a1e1b2680c62ba2df6944ca0da2f99bd14855d1534`  
		Last Modified: Tue, 11 Jul 2023 05:25:43 GMT  
		Size: 6.0 KB (6005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ff1ad0797d8b4bc76bf31cb29679b76b9a9af76a225e434abe3b7d81295b942`  
		Last Modified: Tue, 11 Jul 2023 05:25:43 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:postgres-tomcat`

```console
$ docker pull xwiki@sha256:143482a096b13073c1d9d59fde125210cd6009c4fb253a6d30cf5eaf8481fc5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:4741e9d9b24c00013903dbabf718e61ef5c4b23fd41a283067988225a4ea60ae
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **586.8 MB (586784502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1a1f265f59dcb2e5a6888c86ef11b46a92e4d498dcf98b2ab1f05735021fa2a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:37:40 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:37:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:37:42 GMT
ADD file:140fb5108b4a2861b5718ad03b4a5174bba03589ea8d4c053e6a0b282f439ff3 in / 
# Wed, 28 Jun 2023 08:37:42 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:34:07 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:35:02 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 20:35:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 20:35:35 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 08:22:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 08:22:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 08:22:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 08:22:21 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 08:22:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:22:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:25:33 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 08:25:34 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 00:16:15 GMT
COPY dir:8ddeace4a16f09a0d97488e225c7b2e4a48c9a93484d24b46a09759f52800501 in /usr/local/tomcat 
# Tue, 11 Jul 2023 00:16:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 00:16:20 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 00:16:20 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 00:16:20 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 04:41:24 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 04:41:26 GMT
ENV XWIKI_VERSION=15.5
# Tue, 11 Jul 2023 04:41:26 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.5
# Tue, 11 Jul 2023 04:41:26 GMT
ENV XWIKI_DOWNLOAD_SHA256=e552586d371da33b012cfbd974b3ba80d1b147a5c892ad6cf989960212cdaa02
# Tue, 11 Jul 2023 04:42:04 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 04:42:05 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Tue, 11 Jul 2023 04:42:05 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 04:42:05 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 04:42:06 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 04:42:06 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 04:42:06 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 04:42:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 04:42:06 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:9d19ee268e0d7bcf6716e6658ee1b0384a71d6f2f9aa1ae2085610cf7c7b316f`  
		Last Modified: Wed, 28 Jun 2023 11:50:41 GMT  
		Size: 30.4 MB (30431229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32db0ad82863deaedd2f9a365e52f595085778d28bd1e6f1d351107590cad806`  
		Last Modified: Tue, 04 Jul 2023 20:39:05 GMT  
		Size: 12.5 MB (12495341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01bb55fbcae928d7e6c08d6618580d2b27ce6e46083f861bbed1e01db41c20b`  
		Last Modified: Tue, 04 Jul 2023 20:41:01 GMT  
		Size: 46.7 MB (46666353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297c6e3f57ee032a3cc5f0fd28b52687129e7a1e6485aea12aff08cb6620071e`  
		Last Modified: Tue, 04 Jul 2023 20:40:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15b01f5ab5b71b356d93dff08f5037af8e8a03b4657f1fd303052261161ebd8`  
		Last Modified: Wed, 05 Jul 2023 08:37:14 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c6051a2b9ffe906ea99b555033966c877468da73cd19fd793c86099d0af531`  
		Last Modified: Tue, 11 Jul 2023 00:38:45 GMT  
		Size: 12.3 MB (12274167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34aaed1f6a3460fc256e262b462c1180ccef1b0665ffd50f900d1ef9c19f1d24`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 454.7 KB (454674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b809bf54ada009dfd91afa6ad239f7a791807f2928941b7f969493ec38246be`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bd305e7867896df13faced03525a0f25bf1ac1b2a2c93e60382cdfd41c08e16`  
		Last Modified: Tue, 11 Jul 2023 04:45:43 GMT  
		Size: 179.3 MB (179276407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35bfb758076cf011f5df9081f31dfbcf656cd98cd11b65f53f3684ec1e485c8f`  
		Last Modified: Tue, 11 Jul 2023 04:45:37 GMT  
		Size: 304.2 MB (304236708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2f8ccc8af30dd82bb4657bfdb7193ed23e8dc8823df1eaea8b1c8e4ab85d60`  
		Last Modified: Tue, 11 Jul 2023 04:45:20 GMT  
		Size: 936.8 KB (936849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:822e7d00d75f2a5b9a34edd0741b7e19410deb191f96800278c2921b043c81cb`  
		Last Modified: Tue, 11 Jul 2023 04:45:19 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba3137d80fef0218e2aaa65df38833a3e9d79b0d6e0b8d441376edbc36190ab`  
		Last Modified: Tue, 11 Jul 2023 04:45:19 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d02045e3c19030183c43f79b2c5e3a2f244dda96d11e96014e91d90e85f6e3a9`  
		Last Modified: Tue, 11 Jul 2023 04:45:19 GMT  
		Size: 6.0 KB (6006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91afad54a0c6d44f603953379c22801e4dbc9f2c282eaa00e94946d1d77dc3a4`  
		Last Modified: Tue, 11 Jul 2023 04:45:19 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:30799eeac6bc3f0efeefaf95f4161eeea6298cf60983391d2b7789735d58fa07
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.1 MB (578094027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc026cfcc219f16306961c1815044f7a63d5f49577815243d20c27d2d823d48`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:42:48 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:42:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:42:50 GMT
ADD file:262490f82459c14632f5c9a6d6a5cf6c07b4f307e8fd380fa764662cda46e88f in / 
# Wed, 28 Jun 2023 08:42:50 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:59 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 15:33:41 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 15:34:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 15:34:08 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 02:55:59 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 02:55:59 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 02:55:59 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 02:55:59 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 02:56:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 02:56:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 03:00:51 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 03:00:51 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 01:18:24 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 01:18:25 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 01:18:25 GMT
COPY dir:1743191a9534b9e7d795d3bf9ad18535d99e75967877447e17d7b63574d878d5 in /usr/local/tomcat 
# Tue, 11 Jul 2023 01:18:28 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 01:18:29 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 01:18:29 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 01:18:29 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 05:22:36 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 05:22:39 GMT
ENV XWIKI_VERSION=15.5
# Tue, 11 Jul 2023 05:22:39 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.5
# Tue, 11 Jul 2023 05:22:39 GMT
ENV XWIKI_DOWNLOAD_SHA256=e552586d371da33b012cfbd974b3ba80d1b147a5c892ad6cf989960212cdaa02
# Tue, 11 Jul 2023 05:23:18 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 05:23:21 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Tue, 11 Jul 2023 05:23:21 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 05:23:21 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 05:23:22 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 05:23:22 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 05:23:22 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 05:23:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 05:23:22 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:ac34a2e0269ced3acc355be706239ee0f3f1e73a035c40dd2fac74827164ee53`  
		Last Modified: Wed, 28 Jun 2023 23:23:40 GMT  
		Size: 28.4 MB (28391011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d9df805749ad7c4605f0d49a64da6a6173ab190ec361dc2063b6b73af59ab5`  
		Last Modified: Tue, 04 Jul 2023 15:36:55 GMT  
		Size: 12.5 MB (12455497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1e11a5919e5746092b2a288f71090ffdb0d3544b7b54c31ed0137e6d5d4735`  
		Last Modified: Tue, 04 Jul 2023 15:38:37 GMT  
		Size: 45.0 MB (45009079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80987dc89da28aa5ceec7a86ea74e13cee06ecd9304cf4c92d8f382c79eb4f2`  
		Last Modified: Tue, 04 Jul 2023 15:38:32 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de67c7824eef053da628456fe8aba244c4150024af9454dd4091763920d836c`  
		Last Modified: Wed, 05 Jul 2023 03:14:23 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f77f07e56c3d3019cd346deaeacbe572b15b26a924c19b6386877b47123a89e`  
		Last Modified: Tue, 11 Jul 2023 01:39:24 GMT  
		Size: 12.3 MB (12283700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2422cddd65b0ff63d783c999d005c42281720b8615f5872e1e8fdb32dd9981d9`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 455.1 KB (455052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b023f0d964d565a960e567dcaaa605fdff6da02b54971f4d0693506b481b8c`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:968d46d099e01403854799f31b6235698a474c27fd58b0172b1eb3889cd5067f`  
		Last Modified: Tue, 11 Jul 2023 05:26:50 GMT  
		Size: 174.3 MB (174313369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2894444c04152ca46b568422ea482a66ed3763028ff87cc82d80132ea0e4cdd`  
		Last Modified: Tue, 11 Jul 2023 05:26:46 GMT  
		Size: 304.2 MB (304236690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77118bb73ac2d6b789413d31beabdbb72e88543cca5b3e6406076fd10d40d8d3`  
		Last Modified: Tue, 11 Jul 2023 05:26:32 GMT  
		Size: 936.9 KB (936852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9eb9df1942e9402403596582620c7fb14dbdd8e12de634c88e080cc5795a812`  
		Last Modified: Tue, 11 Jul 2023 05:26:32 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d23fb311f1a568af6e8b96dcb8cfb10d4d96a88aee4243256a3e73f4727fa318`  
		Last Modified: Tue, 11 Jul 2023 05:26:32 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dd3c555379bf5bd7f8d13501bb806b6b5ffb4c2ecb169ce4485f1cbf0d26b9a`  
		Last Modified: Tue, 11 Jul 2023 05:26:32 GMT  
		Size: 6.0 KB (6006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8254381348a57ea56306a83d8f2a89630202f393f54d6102b5652be9cfa10f8f`  
		Last Modified: Tue, 11 Jul 2023 05:26:33 GMT  
		Size: 2.5 KB (2507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:stable`

```console
$ docker pull xwiki@sha256:66e25eb51a5a079e68e523ac98a46358b70c8c431f4360e1565d23aead7eaa3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:stable` - linux; amd64

```console
$ docker pull xwiki@sha256:80718cf2818aac2523383b177893d1f4454722abe547ec303a18e3b4a30362b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **587.3 MB (587250774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97a5a7f1172dd3ea626947d13678241c2e0f4e5391c13ab4c32dd3f009d902c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:37:40 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:37:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:37:42 GMT
ADD file:140fb5108b4a2861b5718ad03b4a5174bba03589ea8d4c053e6a0b282f439ff3 in / 
# Wed, 28 Jun 2023 08:37:42 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:34:07 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:35:02 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 20:35:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 20:35:35 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 08:22:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 08:22:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 08:22:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 08:22:21 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 08:22:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:22:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:25:33 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 08:25:34 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 00:16:15 GMT
COPY dir:8ddeace4a16f09a0d97488e225c7b2e4a48c9a93484d24b46a09759f52800501 in /usr/local/tomcat 
# Tue, 11 Jul 2023 00:16:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 00:16:20 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 00:16:20 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 00:16:20 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 04:40:02 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 04:40:03 GMT
ENV XWIKI_VERSION=15.5
# Tue, 11 Jul 2023 04:40:03 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.5
# Tue, 11 Jul 2023 04:40:03 GMT
ENV XWIKI_DOWNLOAD_SHA256=e552586d371da33b012cfbd974b3ba80d1b147a5c892ad6cf989960212cdaa02
# Tue, 11 Jul 2023 04:40:41 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 04:40:42 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Tue, 11 Jul 2023 04:40:42 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Tue, 11 Jul 2023 04:40:42 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Tue, 11 Jul 2023 04:40:42 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 04:40:42 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 04:40:43 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Tue, 11 Jul 2023 04:40:43 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 04:40:43 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 04:40:44 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 04:40:44 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 04:40:44 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 04:40:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 04:40:44 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:9d19ee268e0d7bcf6716e6658ee1b0384a71d6f2f9aa1ae2085610cf7c7b316f`  
		Last Modified: Wed, 28 Jun 2023 11:50:41 GMT  
		Size: 30.4 MB (30431229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32db0ad82863deaedd2f9a365e52f595085778d28bd1e6f1d351107590cad806`  
		Last Modified: Tue, 04 Jul 2023 20:39:05 GMT  
		Size: 12.5 MB (12495341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01bb55fbcae928d7e6c08d6618580d2b27ce6e46083f861bbed1e01db41c20b`  
		Last Modified: Tue, 04 Jul 2023 20:41:01 GMT  
		Size: 46.7 MB (46666353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297c6e3f57ee032a3cc5f0fd28b52687129e7a1e6485aea12aff08cb6620071e`  
		Last Modified: Tue, 04 Jul 2023 20:40:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15b01f5ab5b71b356d93dff08f5037af8e8a03b4657f1fd303052261161ebd8`  
		Last Modified: Wed, 05 Jul 2023 08:37:14 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c6051a2b9ffe906ea99b555033966c877468da73cd19fd793c86099d0af531`  
		Last Modified: Tue, 11 Jul 2023 00:38:45 GMT  
		Size: 12.3 MB (12274167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34aaed1f6a3460fc256e262b462c1180ccef1b0665ffd50f900d1ef9c19f1d24`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 454.7 KB (454674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b809bf54ada009dfd91afa6ad239f7a791807f2928941b7f969493ec38246be`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877cc60516baaeb7846bba5d5de9e491d0406cd2f43959d7d4e104d89df5e228`  
		Last Modified: Tue, 11 Jul 2023 04:44:49 GMT  
		Size: 178.3 MB (178335971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b863cfbbf93cec3814eec01a334529779a02fcbb3cdff4e2d212bb70287a5720`  
		Last Modified: Tue, 11 Jul 2023 04:44:42 GMT  
		Size: 304.2 MB (304236736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faad5f8d2320ee7d3eb3c3f81aff36754d147687cdb520bc8b24d3170bfcee58`  
		Last Modified: Tue, 11 Jul 2023 04:44:25 GMT  
		Size: 2.3 MB (2343679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ad43407c01ec5371102aaa125c19fb5399f629346a71d4913d742cfed44165`  
		Last Modified: Tue, 11 Jul 2023 04:44:24 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03112af3cb3ddf2e651a23fd879dd50f96a17b20d580105c90d7bb357f02ab0a`  
		Last Modified: Tue, 11 Jul 2023 04:44:24 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7098881bee3a8920bec6f5c352be02657d02e5bb3a4ce69faa81f9354193acbf`  
		Last Modified: Tue, 11 Jul 2023 04:44:24 GMT  
		Size: 6.0 KB (6004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:880ec6a5100b3effc0772c9e06afdfdab1786151d59c78eb30826e0245f2ebe5`  
		Last Modified: Tue, 11 Jul 2023 04:44:24 GMT  
		Size: 2.5 KB (2507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:stable` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:80454bf7fba586e95357c0d982c52ab2d1504e85c6d085e14a1091a19a0d7e65
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.6 MB (578560793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e24eddde7707953934d4ceba63f6297ff5115dc6ec8e8e39946e4f8bd2542c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:42:48 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:42:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:42:50 GMT
ADD file:262490f82459c14632f5c9a6d6a5cf6c07b4f307e8fd380fa764662cda46e88f in / 
# Wed, 28 Jun 2023 08:42:50 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:59 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 15:33:41 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 15:34:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 15:34:08 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 02:55:59 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 02:55:59 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 02:55:59 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 02:55:59 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 02:56:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 02:56:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 03:00:51 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 03:00:51 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 01:18:24 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 01:18:25 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 01:18:25 GMT
COPY dir:1743191a9534b9e7d795d3bf9ad18535d99e75967877447e17d7b63574d878d5 in /usr/local/tomcat 
# Tue, 11 Jul 2023 01:18:28 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 01:18:29 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 01:18:29 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 01:18:29 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 05:21:20 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 05:21:23 GMT
ENV XWIKI_VERSION=15.5
# Tue, 11 Jul 2023 05:21:23 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.5
# Tue, 11 Jul 2023 05:21:23 GMT
ENV XWIKI_DOWNLOAD_SHA256=e552586d371da33b012cfbd974b3ba80d1b147a5c892ad6cf989960212cdaa02
# Tue, 11 Jul 2023 05:22:02 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 05:22:04 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Tue, 11 Jul 2023 05:22:04 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Tue, 11 Jul 2023 05:22:04 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Tue, 11 Jul 2023 05:22:04 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 05:22:04 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 05:22:05 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Tue, 11 Jul 2023 05:22:06 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 05:22:06 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 05:22:06 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 05:22:06 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 05:22:06 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 05:22:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 05:22:06 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:ac34a2e0269ced3acc355be706239ee0f3f1e73a035c40dd2fac74827164ee53`  
		Last Modified: Wed, 28 Jun 2023 23:23:40 GMT  
		Size: 28.4 MB (28391011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d9df805749ad7c4605f0d49a64da6a6173ab190ec361dc2063b6b73af59ab5`  
		Last Modified: Tue, 04 Jul 2023 15:36:55 GMT  
		Size: 12.5 MB (12455497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1e11a5919e5746092b2a288f71090ffdb0d3544b7b54c31ed0137e6d5d4735`  
		Last Modified: Tue, 04 Jul 2023 15:38:37 GMT  
		Size: 45.0 MB (45009079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80987dc89da28aa5ceec7a86ea74e13cee06ecd9304cf4c92d8f382c79eb4f2`  
		Last Modified: Tue, 04 Jul 2023 15:38:32 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de67c7824eef053da628456fe8aba244c4150024af9454dd4091763920d836c`  
		Last Modified: Wed, 05 Jul 2023 03:14:23 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f77f07e56c3d3019cd346deaeacbe572b15b26a924c19b6386877b47123a89e`  
		Last Modified: Tue, 11 Jul 2023 01:39:24 GMT  
		Size: 12.3 MB (12283700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2422cddd65b0ff63d783c999d005c42281720b8615f5872e1e8fdb32dd9981d9`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 455.1 KB (455052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b023f0d964d565a960e567dcaaa605fdff6da02b54971f4d0693506b481b8c`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28177f0763a75e5c940bb6a7919185effccd7cf14c0e350198b3aedbe1db789`  
		Last Modified: Tue, 11 Jul 2023 05:26:01 GMT  
		Size: 173.4 MB (173373450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b39c7f4340aa5dd678a6a0a9bc018229eaadb2a94a0af6bc41d17ce77cdefb`  
		Last Modified: Tue, 11 Jul 2023 05:25:57 GMT  
		Size: 304.2 MB (304236707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc58f6eb776423b78c7a88af6ee221317c44f67e3fb4f413ef3823e8895288a2`  
		Last Modified: Tue, 11 Jul 2023 05:25:43 GMT  
		Size: 2.3 MB (2343673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea5e5502a3de7ec04368cbbb5f6c48f21fc7eac2657e2376ab3c7271ad4f85d`  
		Last Modified: Tue, 11 Jul 2023 05:25:43 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f8adcd32841dea1f4e39476b790a663510401829d69a806cad6007452d0367`  
		Last Modified: Tue, 11 Jul 2023 05:25:43 GMT  
		Size: 2.3 KB (2310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa238d29e18bbc7bdc963a1e1b2680c62ba2df6944ca0da2f99bd14855d1534`  
		Last Modified: Tue, 11 Jul 2023 05:25:43 GMT  
		Size: 6.0 KB (6005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ff1ad0797d8b4bc76bf31cb29679b76b9a9af76a225e434abe3b7d81295b942`  
		Last Modified: Tue, 11 Jul 2023 05:25:43 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:stable-mariadb`

```console
$ docker pull xwiki@sha256:d447b71c1f3084c255c2effee1762e635e6e07f08edcc0bd5b9c46d892350483
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:stable-mariadb` - linux; amd64

```console
$ docker pull xwiki@sha256:6ece9caf8c15d2557f7f165d530deb3442aae7b1bb3b968ba2236e987cebbe2d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **585.5 MB (585501648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac976c622edabab4c9f4be5e6b071f4be6640e98d657487308bb3bb030921d13`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:37:40 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:37:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:37:42 GMT
ADD file:140fb5108b4a2861b5718ad03b4a5174bba03589ea8d4c053e6a0b282f439ff3 in / 
# Wed, 28 Jun 2023 08:37:42 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:34:07 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:35:02 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 20:35:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 20:35:35 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 08:22:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 08:22:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 08:22:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 08:22:21 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 08:22:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:22:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:25:33 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 08:25:34 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 00:16:15 GMT
COPY dir:8ddeace4a16f09a0d97488e225c7b2e4a48c9a93484d24b46a09759f52800501 in /usr/local/tomcat 
# Tue, 11 Jul 2023 00:16:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 00:16:20 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 00:16:20 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 00:16:20 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 04:40:02 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 04:40:03 GMT
ENV XWIKI_VERSION=15.5
# Tue, 11 Jul 2023 04:40:03 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.5
# Tue, 11 Jul 2023 04:40:03 GMT
ENV XWIKI_DOWNLOAD_SHA256=e552586d371da33b012cfbd974b3ba80d1b147a5c892ad6cf989960212cdaa02
# Tue, 11 Jul 2023 04:40:41 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 04:42:10 GMT
ENV MARIADB_JDBC_VERSION=3.1.4
# Tue, 11 Jul 2023 04:42:10 GMT
ENV MARIADB_JDBC_SHA256=eb88b5d727d82e25117e2b6fabcec1daf734633b0a576456c73215884c189ad4
# Tue, 11 Jul 2023 04:42:10 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.1.4
# Tue, 11 Jul 2023 04:42:10 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.1.4.jar
# Tue, 11 Jul 2023 04:42:10 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.1.4.jar
# Tue, 11 Jul 2023 04:42:11 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Tue, 11 Jul 2023 04:42:11 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 04:42:11 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 04:42:12 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 04:42:12 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 04:42:12 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 04:42:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 04:42:12 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:9d19ee268e0d7bcf6716e6658ee1b0384a71d6f2f9aa1ae2085610cf7c7b316f`  
		Last Modified: Wed, 28 Jun 2023 11:50:41 GMT  
		Size: 30.4 MB (30431229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32db0ad82863deaedd2f9a365e52f595085778d28bd1e6f1d351107590cad806`  
		Last Modified: Tue, 04 Jul 2023 20:39:05 GMT  
		Size: 12.5 MB (12495341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01bb55fbcae928d7e6c08d6618580d2b27ce6e46083f861bbed1e01db41c20b`  
		Last Modified: Tue, 04 Jul 2023 20:41:01 GMT  
		Size: 46.7 MB (46666353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297c6e3f57ee032a3cc5f0fd28b52687129e7a1e6485aea12aff08cb6620071e`  
		Last Modified: Tue, 04 Jul 2023 20:40:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15b01f5ab5b71b356d93dff08f5037af8e8a03b4657f1fd303052261161ebd8`  
		Last Modified: Wed, 05 Jul 2023 08:37:14 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c6051a2b9ffe906ea99b555033966c877468da73cd19fd793c86099d0af531`  
		Last Modified: Tue, 11 Jul 2023 00:38:45 GMT  
		Size: 12.3 MB (12274167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34aaed1f6a3460fc256e262b462c1180ccef1b0665ffd50f900d1ef9c19f1d24`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 454.7 KB (454674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b809bf54ada009dfd91afa6ad239f7a791807f2928941b7f969493ec38246be`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877cc60516baaeb7846bba5d5de9e491d0406cd2f43959d7d4e104d89df5e228`  
		Last Modified: Tue, 11 Jul 2023 04:44:49 GMT  
		Size: 178.3 MB (178335971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b863cfbbf93cec3814eec01a334529779a02fcbb3cdff4e2d212bb70287a5720`  
		Last Modified: Tue, 11 Jul 2023 04:44:42 GMT  
		Size: 304.2 MB (304236736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d9f121998f3ebb1fe9d8b1e2b7964a6e19afe2500ee4c64b95739f1578f0728`  
		Last Modified: Tue, 11 Jul 2023 04:46:03 GMT  
		Size: 594.6 KB (594553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b2c8c7e34dbea6b864808d65dae2a48aaa73e9595b3dd30f14d4b95b28cbcf`  
		Last Modified: Tue, 11 Jul 2023 04:46:03 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84634ee1814641c052e3b568592a22c625bc82aaf05fdb64d6dcbdb17ff803b7`  
		Last Modified: Tue, 11 Jul 2023 04:46:03 GMT  
		Size: 2.3 KB (2311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f62b3d21969533fa11c23f989db62def095f4c38f4e3ebba9bdb897cb756a783`  
		Last Modified: Tue, 11 Jul 2023 04:46:03 GMT  
		Size: 6.0 KB (6003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d136eed865c53c0489a1100cd4c540d7269e0bbc620b8b44fa3c71d168a0e583`  
		Last Modified: Tue, 11 Jul 2023 04:46:03 GMT  
		Size: 2.5 KB (2503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:stable-mariadb` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:2745b46e135b629961fa0abba943bcd28e8793d51275fbf2d1a945545b31961b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **576.8 MB (576811676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa8facaf677aa5a99371bfdf03feab6977a37475e6664e98cdef94878d40484c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:42:48 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:42:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:42:50 GMT
ADD file:262490f82459c14632f5c9a6d6a5cf6c07b4f307e8fd380fa764662cda46e88f in / 
# Wed, 28 Jun 2023 08:42:50 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:59 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 15:33:41 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 15:34:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 15:34:08 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 02:55:59 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 02:55:59 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 02:55:59 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 02:55:59 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 02:56:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 02:56:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 03:00:51 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 03:00:51 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 01:18:24 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 01:18:25 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 01:18:25 GMT
COPY dir:1743191a9534b9e7d795d3bf9ad18535d99e75967877447e17d7b63574d878d5 in /usr/local/tomcat 
# Tue, 11 Jul 2023 01:18:28 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 01:18:29 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 01:18:29 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 01:18:29 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 05:21:20 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 05:21:23 GMT
ENV XWIKI_VERSION=15.5
# Tue, 11 Jul 2023 05:21:23 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.5
# Tue, 11 Jul 2023 05:21:23 GMT
ENV XWIKI_DOWNLOAD_SHA256=e552586d371da33b012cfbd974b3ba80d1b147a5c892ad6cf989960212cdaa02
# Tue, 11 Jul 2023 05:22:02 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 05:23:36 GMT
ENV MARIADB_JDBC_VERSION=3.1.4
# Tue, 11 Jul 2023 05:23:36 GMT
ENV MARIADB_JDBC_SHA256=eb88b5d727d82e25117e2b6fabcec1daf734633b0a576456c73215884c189ad4
# Tue, 11 Jul 2023 05:23:36 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.1.4
# Tue, 11 Jul 2023 05:23:37 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.1.4.jar
# Tue, 11 Jul 2023 05:23:37 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.1.4.jar
# Tue, 11 Jul 2023 05:23:37 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Tue, 11 Jul 2023 05:23:37 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 05:23:37 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 05:23:38 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 05:23:38 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 05:23:38 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 05:23:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 05:23:38 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:ac34a2e0269ced3acc355be706239ee0f3f1e73a035c40dd2fac74827164ee53`  
		Last Modified: Wed, 28 Jun 2023 23:23:40 GMT  
		Size: 28.4 MB (28391011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d9df805749ad7c4605f0d49a64da6a6173ab190ec361dc2063b6b73af59ab5`  
		Last Modified: Tue, 04 Jul 2023 15:36:55 GMT  
		Size: 12.5 MB (12455497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1e11a5919e5746092b2a288f71090ffdb0d3544b7b54c31ed0137e6d5d4735`  
		Last Modified: Tue, 04 Jul 2023 15:38:37 GMT  
		Size: 45.0 MB (45009079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80987dc89da28aa5ceec7a86ea74e13cee06ecd9304cf4c92d8f382c79eb4f2`  
		Last Modified: Tue, 04 Jul 2023 15:38:32 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de67c7824eef053da628456fe8aba244c4150024af9454dd4091763920d836c`  
		Last Modified: Wed, 05 Jul 2023 03:14:23 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f77f07e56c3d3019cd346deaeacbe572b15b26a924c19b6386877b47123a89e`  
		Last Modified: Tue, 11 Jul 2023 01:39:24 GMT  
		Size: 12.3 MB (12283700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2422cddd65b0ff63d783c999d005c42281720b8615f5872e1e8fdb32dd9981d9`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 455.1 KB (455052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b023f0d964d565a960e567dcaaa605fdff6da02b54971f4d0693506b481b8c`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28177f0763a75e5c940bb6a7919185effccd7cf14c0e350198b3aedbe1db789`  
		Last Modified: Tue, 11 Jul 2023 05:26:01 GMT  
		Size: 173.4 MB (173373450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b39c7f4340aa5dd678a6a0a9bc018229eaadb2a94a0af6bc41d17ce77cdefb`  
		Last Modified: Tue, 11 Jul 2023 05:25:57 GMT  
		Size: 304.2 MB (304236707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0be5f78ca514976c969b47013a6e82418af20d755526a18e35388d7482170b8`  
		Last Modified: Tue, 11 Jul 2023 05:27:14 GMT  
		Size: 594.6 KB (594556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01372195bd2be58e8f5f6433314edfd376c3ce7d69fe9fc1b21188af306f2ce1`  
		Last Modified: Tue, 11 Jul 2023 05:27:14 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15366f793a0d945e4ef67931cb193ae8c2b7f218ecba840af9cf4958adb81ce8`  
		Last Modified: Tue, 11 Jul 2023 05:27:14 GMT  
		Size: 2.3 KB (2312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae0ba8487202e29a15c7c1b505e9f148753e98c7e9284bb88ab357269ef43ab`  
		Last Modified: Tue, 11 Jul 2023 05:27:14 GMT  
		Size: 6.0 KB (6004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4d894785e0d9bda2444090848544b861a5280bd4c8a3e5686acc3d6f3f232fe`  
		Last Modified: Tue, 11 Jul 2023 05:27:14 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:stable-mariadb-tomcat`

```console
$ docker pull xwiki@sha256:d447b71c1f3084c255c2effee1762e635e6e07f08edcc0bd5b9c46d892350483
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:stable-mariadb-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:6ece9caf8c15d2557f7f165d530deb3442aae7b1bb3b968ba2236e987cebbe2d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **585.5 MB (585501648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac976c622edabab4c9f4be5e6b071f4be6640e98d657487308bb3bb030921d13`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:37:40 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:37:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:37:42 GMT
ADD file:140fb5108b4a2861b5718ad03b4a5174bba03589ea8d4c053e6a0b282f439ff3 in / 
# Wed, 28 Jun 2023 08:37:42 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:34:07 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:35:02 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 20:35:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 20:35:35 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 08:22:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 08:22:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 08:22:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 08:22:21 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 08:22:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:22:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:25:33 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 08:25:34 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 00:16:15 GMT
COPY dir:8ddeace4a16f09a0d97488e225c7b2e4a48c9a93484d24b46a09759f52800501 in /usr/local/tomcat 
# Tue, 11 Jul 2023 00:16:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 00:16:20 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 00:16:20 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 00:16:20 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 04:40:02 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 04:40:03 GMT
ENV XWIKI_VERSION=15.5
# Tue, 11 Jul 2023 04:40:03 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.5
# Tue, 11 Jul 2023 04:40:03 GMT
ENV XWIKI_DOWNLOAD_SHA256=e552586d371da33b012cfbd974b3ba80d1b147a5c892ad6cf989960212cdaa02
# Tue, 11 Jul 2023 04:40:41 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 04:42:10 GMT
ENV MARIADB_JDBC_VERSION=3.1.4
# Tue, 11 Jul 2023 04:42:10 GMT
ENV MARIADB_JDBC_SHA256=eb88b5d727d82e25117e2b6fabcec1daf734633b0a576456c73215884c189ad4
# Tue, 11 Jul 2023 04:42:10 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.1.4
# Tue, 11 Jul 2023 04:42:10 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.1.4.jar
# Tue, 11 Jul 2023 04:42:10 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.1.4.jar
# Tue, 11 Jul 2023 04:42:11 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Tue, 11 Jul 2023 04:42:11 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 04:42:11 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 04:42:12 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 04:42:12 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 04:42:12 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 04:42:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 04:42:12 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:9d19ee268e0d7bcf6716e6658ee1b0384a71d6f2f9aa1ae2085610cf7c7b316f`  
		Last Modified: Wed, 28 Jun 2023 11:50:41 GMT  
		Size: 30.4 MB (30431229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32db0ad82863deaedd2f9a365e52f595085778d28bd1e6f1d351107590cad806`  
		Last Modified: Tue, 04 Jul 2023 20:39:05 GMT  
		Size: 12.5 MB (12495341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01bb55fbcae928d7e6c08d6618580d2b27ce6e46083f861bbed1e01db41c20b`  
		Last Modified: Tue, 04 Jul 2023 20:41:01 GMT  
		Size: 46.7 MB (46666353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297c6e3f57ee032a3cc5f0fd28b52687129e7a1e6485aea12aff08cb6620071e`  
		Last Modified: Tue, 04 Jul 2023 20:40:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15b01f5ab5b71b356d93dff08f5037af8e8a03b4657f1fd303052261161ebd8`  
		Last Modified: Wed, 05 Jul 2023 08:37:14 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c6051a2b9ffe906ea99b555033966c877468da73cd19fd793c86099d0af531`  
		Last Modified: Tue, 11 Jul 2023 00:38:45 GMT  
		Size: 12.3 MB (12274167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34aaed1f6a3460fc256e262b462c1180ccef1b0665ffd50f900d1ef9c19f1d24`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 454.7 KB (454674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b809bf54ada009dfd91afa6ad239f7a791807f2928941b7f969493ec38246be`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877cc60516baaeb7846bba5d5de9e491d0406cd2f43959d7d4e104d89df5e228`  
		Last Modified: Tue, 11 Jul 2023 04:44:49 GMT  
		Size: 178.3 MB (178335971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b863cfbbf93cec3814eec01a334529779a02fcbb3cdff4e2d212bb70287a5720`  
		Last Modified: Tue, 11 Jul 2023 04:44:42 GMT  
		Size: 304.2 MB (304236736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d9f121998f3ebb1fe9d8b1e2b7964a6e19afe2500ee4c64b95739f1578f0728`  
		Last Modified: Tue, 11 Jul 2023 04:46:03 GMT  
		Size: 594.6 KB (594553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b2c8c7e34dbea6b864808d65dae2a48aaa73e9595b3dd30f14d4b95b28cbcf`  
		Last Modified: Tue, 11 Jul 2023 04:46:03 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84634ee1814641c052e3b568592a22c625bc82aaf05fdb64d6dcbdb17ff803b7`  
		Last Modified: Tue, 11 Jul 2023 04:46:03 GMT  
		Size: 2.3 KB (2311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f62b3d21969533fa11c23f989db62def095f4c38f4e3ebba9bdb897cb756a783`  
		Last Modified: Tue, 11 Jul 2023 04:46:03 GMT  
		Size: 6.0 KB (6003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d136eed865c53c0489a1100cd4c540d7269e0bbc620b8b44fa3c71d168a0e583`  
		Last Modified: Tue, 11 Jul 2023 04:46:03 GMT  
		Size: 2.5 KB (2503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:stable-mariadb-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:2745b46e135b629961fa0abba943bcd28e8793d51275fbf2d1a945545b31961b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **576.8 MB (576811676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa8facaf677aa5a99371bfdf03feab6977a37475e6664e98cdef94878d40484c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:42:48 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:42:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:42:50 GMT
ADD file:262490f82459c14632f5c9a6d6a5cf6c07b4f307e8fd380fa764662cda46e88f in / 
# Wed, 28 Jun 2023 08:42:50 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:59 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 15:33:41 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 15:34:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 15:34:08 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 02:55:59 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 02:55:59 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 02:55:59 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 02:55:59 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 02:56:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 02:56:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 03:00:51 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 03:00:51 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 01:18:24 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 01:18:25 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 01:18:25 GMT
COPY dir:1743191a9534b9e7d795d3bf9ad18535d99e75967877447e17d7b63574d878d5 in /usr/local/tomcat 
# Tue, 11 Jul 2023 01:18:28 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 01:18:29 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 01:18:29 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 01:18:29 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 05:21:20 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 05:21:23 GMT
ENV XWIKI_VERSION=15.5
# Tue, 11 Jul 2023 05:21:23 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.5
# Tue, 11 Jul 2023 05:21:23 GMT
ENV XWIKI_DOWNLOAD_SHA256=e552586d371da33b012cfbd974b3ba80d1b147a5c892ad6cf989960212cdaa02
# Tue, 11 Jul 2023 05:22:02 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 05:23:36 GMT
ENV MARIADB_JDBC_VERSION=3.1.4
# Tue, 11 Jul 2023 05:23:36 GMT
ENV MARIADB_JDBC_SHA256=eb88b5d727d82e25117e2b6fabcec1daf734633b0a576456c73215884c189ad4
# Tue, 11 Jul 2023 05:23:36 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.1.4
# Tue, 11 Jul 2023 05:23:37 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.1.4.jar
# Tue, 11 Jul 2023 05:23:37 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.1.4.jar
# Tue, 11 Jul 2023 05:23:37 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Tue, 11 Jul 2023 05:23:37 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 05:23:37 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 05:23:38 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 05:23:38 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 05:23:38 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 05:23:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 05:23:38 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:ac34a2e0269ced3acc355be706239ee0f3f1e73a035c40dd2fac74827164ee53`  
		Last Modified: Wed, 28 Jun 2023 23:23:40 GMT  
		Size: 28.4 MB (28391011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d9df805749ad7c4605f0d49a64da6a6173ab190ec361dc2063b6b73af59ab5`  
		Last Modified: Tue, 04 Jul 2023 15:36:55 GMT  
		Size: 12.5 MB (12455497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1e11a5919e5746092b2a288f71090ffdb0d3544b7b54c31ed0137e6d5d4735`  
		Last Modified: Tue, 04 Jul 2023 15:38:37 GMT  
		Size: 45.0 MB (45009079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80987dc89da28aa5ceec7a86ea74e13cee06ecd9304cf4c92d8f382c79eb4f2`  
		Last Modified: Tue, 04 Jul 2023 15:38:32 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de67c7824eef053da628456fe8aba244c4150024af9454dd4091763920d836c`  
		Last Modified: Wed, 05 Jul 2023 03:14:23 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f77f07e56c3d3019cd346deaeacbe572b15b26a924c19b6386877b47123a89e`  
		Last Modified: Tue, 11 Jul 2023 01:39:24 GMT  
		Size: 12.3 MB (12283700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2422cddd65b0ff63d783c999d005c42281720b8615f5872e1e8fdb32dd9981d9`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 455.1 KB (455052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b023f0d964d565a960e567dcaaa605fdff6da02b54971f4d0693506b481b8c`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28177f0763a75e5c940bb6a7919185effccd7cf14c0e350198b3aedbe1db789`  
		Last Modified: Tue, 11 Jul 2023 05:26:01 GMT  
		Size: 173.4 MB (173373450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b39c7f4340aa5dd678a6a0a9bc018229eaadb2a94a0af6bc41d17ce77cdefb`  
		Last Modified: Tue, 11 Jul 2023 05:25:57 GMT  
		Size: 304.2 MB (304236707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0be5f78ca514976c969b47013a6e82418af20d755526a18e35388d7482170b8`  
		Last Modified: Tue, 11 Jul 2023 05:27:14 GMT  
		Size: 594.6 KB (594556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01372195bd2be58e8f5f6433314edfd376c3ce7d69fe9fc1b21188af306f2ce1`  
		Last Modified: Tue, 11 Jul 2023 05:27:14 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15366f793a0d945e4ef67931cb193ae8c2b7f218ecba840af9cf4958adb81ce8`  
		Last Modified: Tue, 11 Jul 2023 05:27:14 GMT  
		Size: 2.3 KB (2312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae0ba8487202e29a15c7c1b505e9f148753e98c7e9284bb88ab357269ef43ab`  
		Last Modified: Tue, 11 Jul 2023 05:27:14 GMT  
		Size: 6.0 KB (6004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4d894785e0d9bda2444090848544b861a5280bd4c8a3e5686acc3d6f3f232fe`  
		Last Modified: Tue, 11 Jul 2023 05:27:14 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:stable-mysql`

```console
$ docker pull xwiki@sha256:66e25eb51a5a079e68e523ac98a46358b70c8c431f4360e1565d23aead7eaa3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:stable-mysql` - linux; amd64

```console
$ docker pull xwiki@sha256:80718cf2818aac2523383b177893d1f4454722abe547ec303a18e3b4a30362b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **587.3 MB (587250774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97a5a7f1172dd3ea626947d13678241c2e0f4e5391c13ab4c32dd3f009d902c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:37:40 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:37:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:37:42 GMT
ADD file:140fb5108b4a2861b5718ad03b4a5174bba03589ea8d4c053e6a0b282f439ff3 in / 
# Wed, 28 Jun 2023 08:37:42 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:34:07 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:35:02 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 20:35:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 20:35:35 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 08:22:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 08:22:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 08:22:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 08:22:21 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 08:22:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:22:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:25:33 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 08:25:34 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 00:16:15 GMT
COPY dir:8ddeace4a16f09a0d97488e225c7b2e4a48c9a93484d24b46a09759f52800501 in /usr/local/tomcat 
# Tue, 11 Jul 2023 00:16:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 00:16:20 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 00:16:20 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 00:16:20 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 04:40:02 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 04:40:03 GMT
ENV XWIKI_VERSION=15.5
# Tue, 11 Jul 2023 04:40:03 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.5
# Tue, 11 Jul 2023 04:40:03 GMT
ENV XWIKI_DOWNLOAD_SHA256=e552586d371da33b012cfbd974b3ba80d1b147a5c892ad6cf989960212cdaa02
# Tue, 11 Jul 2023 04:40:41 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 04:40:42 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Tue, 11 Jul 2023 04:40:42 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Tue, 11 Jul 2023 04:40:42 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Tue, 11 Jul 2023 04:40:42 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 04:40:42 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 04:40:43 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Tue, 11 Jul 2023 04:40:43 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 04:40:43 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 04:40:44 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 04:40:44 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 04:40:44 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 04:40:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 04:40:44 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:9d19ee268e0d7bcf6716e6658ee1b0384a71d6f2f9aa1ae2085610cf7c7b316f`  
		Last Modified: Wed, 28 Jun 2023 11:50:41 GMT  
		Size: 30.4 MB (30431229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32db0ad82863deaedd2f9a365e52f595085778d28bd1e6f1d351107590cad806`  
		Last Modified: Tue, 04 Jul 2023 20:39:05 GMT  
		Size: 12.5 MB (12495341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01bb55fbcae928d7e6c08d6618580d2b27ce6e46083f861bbed1e01db41c20b`  
		Last Modified: Tue, 04 Jul 2023 20:41:01 GMT  
		Size: 46.7 MB (46666353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297c6e3f57ee032a3cc5f0fd28b52687129e7a1e6485aea12aff08cb6620071e`  
		Last Modified: Tue, 04 Jul 2023 20:40:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15b01f5ab5b71b356d93dff08f5037af8e8a03b4657f1fd303052261161ebd8`  
		Last Modified: Wed, 05 Jul 2023 08:37:14 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c6051a2b9ffe906ea99b555033966c877468da73cd19fd793c86099d0af531`  
		Last Modified: Tue, 11 Jul 2023 00:38:45 GMT  
		Size: 12.3 MB (12274167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34aaed1f6a3460fc256e262b462c1180ccef1b0665ffd50f900d1ef9c19f1d24`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 454.7 KB (454674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b809bf54ada009dfd91afa6ad239f7a791807f2928941b7f969493ec38246be`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877cc60516baaeb7846bba5d5de9e491d0406cd2f43959d7d4e104d89df5e228`  
		Last Modified: Tue, 11 Jul 2023 04:44:49 GMT  
		Size: 178.3 MB (178335971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b863cfbbf93cec3814eec01a334529779a02fcbb3cdff4e2d212bb70287a5720`  
		Last Modified: Tue, 11 Jul 2023 04:44:42 GMT  
		Size: 304.2 MB (304236736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faad5f8d2320ee7d3eb3c3f81aff36754d147687cdb520bc8b24d3170bfcee58`  
		Last Modified: Tue, 11 Jul 2023 04:44:25 GMT  
		Size: 2.3 MB (2343679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ad43407c01ec5371102aaa125c19fb5399f629346a71d4913d742cfed44165`  
		Last Modified: Tue, 11 Jul 2023 04:44:24 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03112af3cb3ddf2e651a23fd879dd50f96a17b20d580105c90d7bb357f02ab0a`  
		Last Modified: Tue, 11 Jul 2023 04:44:24 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7098881bee3a8920bec6f5c352be02657d02e5bb3a4ce69faa81f9354193acbf`  
		Last Modified: Tue, 11 Jul 2023 04:44:24 GMT  
		Size: 6.0 KB (6004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:880ec6a5100b3effc0772c9e06afdfdab1786151d59c78eb30826e0245f2ebe5`  
		Last Modified: Tue, 11 Jul 2023 04:44:24 GMT  
		Size: 2.5 KB (2507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:stable-mysql` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:80454bf7fba586e95357c0d982c52ab2d1504e85c6d085e14a1091a19a0d7e65
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.6 MB (578560793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e24eddde7707953934d4ceba63f6297ff5115dc6ec8e8e39946e4f8bd2542c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:42:48 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:42:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:42:50 GMT
ADD file:262490f82459c14632f5c9a6d6a5cf6c07b4f307e8fd380fa764662cda46e88f in / 
# Wed, 28 Jun 2023 08:42:50 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:59 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 15:33:41 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 15:34:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 15:34:08 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 02:55:59 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 02:55:59 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 02:55:59 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 02:55:59 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 02:56:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 02:56:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 03:00:51 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 03:00:51 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 01:18:24 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 01:18:25 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 01:18:25 GMT
COPY dir:1743191a9534b9e7d795d3bf9ad18535d99e75967877447e17d7b63574d878d5 in /usr/local/tomcat 
# Tue, 11 Jul 2023 01:18:28 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 01:18:29 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 01:18:29 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 01:18:29 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 05:21:20 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 05:21:23 GMT
ENV XWIKI_VERSION=15.5
# Tue, 11 Jul 2023 05:21:23 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.5
# Tue, 11 Jul 2023 05:21:23 GMT
ENV XWIKI_DOWNLOAD_SHA256=e552586d371da33b012cfbd974b3ba80d1b147a5c892ad6cf989960212cdaa02
# Tue, 11 Jul 2023 05:22:02 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 05:22:04 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Tue, 11 Jul 2023 05:22:04 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Tue, 11 Jul 2023 05:22:04 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Tue, 11 Jul 2023 05:22:04 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 05:22:04 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 05:22:05 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Tue, 11 Jul 2023 05:22:06 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 05:22:06 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 05:22:06 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 05:22:06 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 05:22:06 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 05:22:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 05:22:06 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:ac34a2e0269ced3acc355be706239ee0f3f1e73a035c40dd2fac74827164ee53`  
		Last Modified: Wed, 28 Jun 2023 23:23:40 GMT  
		Size: 28.4 MB (28391011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d9df805749ad7c4605f0d49a64da6a6173ab190ec361dc2063b6b73af59ab5`  
		Last Modified: Tue, 04 Jul 2023 15:36:55 GMT  
		Size: 12.5 MB (12455497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1e11a5919e5746092b2a288f71090ffdb0d3544b7b54c31ed0137e6d5d4735`  
		Last Modified: Tue, 04 Jul 2023 15:38:37 GMT  
		Size: 45.0 MB (45009079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80987dc89da28aa5ceec7a86ea74e13cee06ecd9304cf4c92d8f382c79eb4f2`  
		Last Modified: Tue, 04 Jul 2023 15:38:32 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de67c7824eef053da628456fe8aba244c4150024af9454dd4091763920d836c`  
		Last Modified: Wed, 05 Jul 2023 03:14:23 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f77f07e56c3d3019cd346deaeacbe572b15b26a924c19b6386877b47123a89e`  
		Last Modified: Tue, 11 Jul 2023 01:39:24 GMT  
		Size: 12.3 MB (12283700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2422cddd65b0ff63d783c999d005c42281720b8615f5872e1e8fdb32dd9981d9`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 455.1 KB (455052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b023f0d964d565a960e567dcaaa605fdff6da02b54971f4d0693506b481b8c`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28177f0763a75e5c940bb6a7919185effccd7cf14c0e350198b3aedbe1db789`  
		Last Modified: Tue, 11 Jul 2023 05:26:01 GMT  
		Size: 173.4 MB (173373450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b39c7f4340aa5dd678a6a0a9bc018229eaadb2a94a0af6bc41d17ce77cdefb`  
		Last Modified: Tue, 11 Jul 2023 05:25:57 GMT  
		Size: 304.2 MB (304236707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc58f6eb776423b78c7a88af6ee221317c44f67e3fb4f413ef3823e8895288a2`  
		Last Modified: Tue, 11 Jul 2023 05:25:43 GMT  
		Size: 2.3 MB (2343673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea5e5502a3de7ec04368cbbb5f6c48f21fc7eac2657e2376ab3c7271ad4f85d`  
		Last Modified: Tue, 11 Jul 2023 05:25:43 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f8adcd32841dea1f4e39476b790a663510401829d69a806cad6007452d0367`  
		Last Modified: Tue, 11 Jul 2023 05:25:43 GMT  
		Size: 2.3 KB (2310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa238d29e18bbc7bdc963a1e1b2680c62ba2df6944ca0da2f99bd14855d1534`  
		Last Modified: Tue, 11 Jul 2023 05:25:43 GMT  
		Size: 6.0 KB (6005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ff1ad0797d8b4bc76bf31cb29679b76b9a9af76a225e434abe3b7d81295b942`  
		Last Modified: Tue, 11 Jul 2023 05:25:43 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:stable-mysql-tomcat`

```console
$ docker pull xwiki@sha256:66e25eb51a5a079e68e523ac98a46358b70c8c431f4360e1565d23aead7eaa3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:stable-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:80718cf2818aac2523383b177893d1f4454722abe547ec303a18e3b4a30362b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **587.3 MB (587250774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97a5a7f1172dd3ea626947d13678241c2e0f4e5391c13ab4c32dd3f009d902c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:37:40 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:37:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:37:42 GMT
ADD file:140fb5108b4a2861b5718ad03b4a5174bba03589ea8d4c053e6a0b282f439ff3 in / 
# Wed, 28 Jun 2023 08:37:42 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:34:07 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:35:02 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 20:35:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 20:35:35 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 08:22:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 08:22:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 08:22:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 08:22:21 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 08:22:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:22:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:25:33 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 08:25:34 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 00:16:15 GMT
COPY dir:8ddeace4a16f09a0d97488e225c7b2e4a48c9a93484d24b46a09759f52800501 in /usr/local/tomcat 
# Tue, 11 Jul 2023 00:16:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 00:16:20 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 00:16:20 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 00:16:20 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 04:40:02 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 04:40:03 GMT
ENV XWIKI_VERSION=15.5
# Tue, 11 Jul 2023 04:40:03 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.5
# Tue, 11 Jul 2023 04:40:03 GMT
ENV XWIKI_DOWNLOAD_SHA256=e552586d371da33b012cfbd974b3ba80d1b147a5c892ad6cf989960212cdaa02
# Tue, 11 Jul 2023 04:40:41 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 04:40:42 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Tue, 11 Jul 2023 04:40:42 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Tue, 11 Jul 2023 04:40:42 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Tue, 11 Jul 2023 04:40:42 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 04:40:42 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 04:40:43 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Tue, 11 Jul 2023 04:40:43 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 04:40:43 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 04:40:44 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 04:40:44 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 04:40:44 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 04:40:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 04:40:44 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:9d19ee268e0d7bcf6716e6658ee1b0384a71d6f2f9aa1ae2085610cf7c7b316f`  
		Last Modified: Wed, 28 Jun 2023 11:50:41 GMT  
		Size: 30.4 MB (30431229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32db0ad82863deaedd2f9a365e52f595085778d28bd1e6f1d351107590cad806`  
		Last Modified: Tue, 04 Jul 2023 20:39:05 GMT  
		Size: 12.5 MB (12495341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01bb55fbcae928d7e6c08d6618580d2b27ce6e46083f861bbed1e01db41c20b`  
		Last Modified: Tue, 04 Jul 2023 20:41:01 GMT  
		Size: 46.7 MB (46666353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297c6e3f57ee032a3cc5f0fd28b52687129e7a1e6485aea12aff08cb6620071e`  
		Last Modified: Tue, 04 Jul 2023 20:40:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15b01f5ab5b71b356d93dff08f5037af8e8a03b4657f1fd303052261161ebd8`  
		Last Modified: Wed, 05 Jul 2023 08:37:14 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c6051a2b9ffe906ea99b555033966c877468da73cd19fd793c86099d0af531`  
		Last Modified: Tue, 11 Jul 2023 00:38:45 GMT  
		Size: 12.3 MB (12274167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34aaed1f6a3460fc256e262b462c1180ccef1b0665ffd50f900d1ef9c19f1d24`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 454.7 KB (454674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b809bf54ada009dfd91afa6ad239f7a791807f2928941b7f969493ec38246be`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877cc60516baaeb7846bba5d5de9e491d0406cd2f43959d7d4e104d89df5e228`  
		Last Modified: Tue, 11 Jul 2023 04:44:49 GMT  
		Size: 178.3 MB (178335971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b863cfbbf93cec3814eec01a334529779a02fcbb3cdff4e2d212bb70287a5720`  
		Last Modified: Tue, 11 Jul 2023 04:44:42 GMT  
		Size: 304.2 MB (304236736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faad5f8d2320ee7d3eb3c3f81aff36754d147687cdb520bc8b24d3170bfcee58`  
		Last Modified: Tue, 11 Jul 2023 04:44:25 GMT  
		Size: 2.3 MB (2343679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ad43407c01ec5371102aaa125c19fb5399f629346a71d4913d742cfed44165`  
		Last Modified: Tue, 11 Jul 2023 04:44:24 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03112af3cb3ddf2e651a23fd879dd50f96a17b20d580105c90d7bb357f02ab0a`  
		Last Modified: Tue, 11 Jul 2023 04:44:24 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7098881bee3a8920bec6f5c352be02657d02e5bb3a4ce69faa81f9354193acbf`  
		Last Modified: Tue, 11 Jul 2023 04:44:24 GMT  
		Size: 6.0 KB (6004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:880ec6a5100b3effc0772c9e06afdfdab1786151d59c78eb30826e0245f2ebe5`  
		Last Modified: Tue, 11 Jul 2023 04:44:24 GMT  
		Size: 2.5 KB (2507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:stable-mysql-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:80454bf7fba586e95357c0d982c52ab2d1504e85c6d085e14a1091a19a0d7e65
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.6 MB (578560793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e24eddde7707953934d4ceba63f6297ff5115dc6ec8e8e39946e4f8bd2542c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:42:48 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:42:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:42:50 GMT
ADD file:262490f82459c14632f5c9a6d6a5cf6c07b4f307e8fd380fa764662cda46e88f in / 
# Wed, 28 Jun 2023 08:42:50 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:59 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 15:33:41 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 15:34:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 15:34:08 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 02:55:59 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 02:55:59 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 02:55:59 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 02:55:59 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 02:56:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 02:56:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 03:00:51 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 03:00:51 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 01:18:24 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 01:18:25 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 01:18:25 GMT
COPY dir:1743191a9534b9e7d795d3bf9ad18535d99e75967877447e17d7b63574d878d5 in /usr/local/tomcat 
# Tue, 11 Jul 2023 01:18:28 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 01:18:29 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 01:18:29 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 01:18:29 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 05:21:20 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 05:21:23 GMT
ENV XWIKI_VERSION=15.5
# Tue, 11 Jul 2023 05:21:23 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.5
# Tue, 11 Jul 2023 05:21:23 GMT
ENV XWIKI_DOWNLOAD_SHA256=e552586d371da33b012cfbd974b3ba80d1b147a5c892ad6cf989960212cdaa02
# Tue, 11 Jul 2023 05:22:02 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 05:22:04 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Tue, 11 Jul 2023 05:22:04 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Tue, 11 Jul 2023 05:22:04 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Tue, 11 Jul 2023 05:22:04 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 05:22:04 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Tue, 11 Jul 2023 05:22:05 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Tue, 11 Jul 2023 05:22:06 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 05:22:06 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 05:22:06 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 05:22:06 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 05:22:06 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 05:22:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 05:22:06 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:ac34a2e0269ced3acc355be706239ee0f3f1e73a035c40dd2fac74827164ee53`  
		Last Modified: Wed, 28 Jun 2023 23:23:40 GMT  
		Size: 28.4 MB (28391011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d9df805749ad7c4605f0d49a64da6a6173ab190ec361dc2063b6b73af59ab5`  
		Last Modified: Tue, 04 Jul 2023 15:36:55 GMT  
		Size: 12.5 MB (12455497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1e11a5919e5746092b2a288f71090ffdb0d3544b7b54c31ed0137e6d5d4735`  
		Last Modified: Tue, 04 Jul 2023 15:38:37 GMT  
		Size: 45.0 MB (45009079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80987dc89da28aa5ceec7a86ea74e13cee06ecd9304cf4c92d8f382c79eb4f2`  
		Last Modified: Tue, 04 Jul 2023 15:38:32 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de67c7824eef053da628456fe8aba244c4150024af9454dd4091763920d836c`  
		Last Modified: Wed, 05 Jul 2023 03:14:23 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f77f07e56c3d3019cd346deaeacbe572b15b26a924c19b6386877b47123a89e`  
		Last Modified: Tue, 11 Jul 2023 01:39:24 GMT  
		Size: 12.3 MB (12283700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2422cddd65b0ff63d783c999d005c42281720b8615f5872e1e8fdb32dd9981d9`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 455.1 KB (455052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b023f0d964d565a960e567dcaaa605fdff6da02b54971f4d0693506b481b8c`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28177f0763a75e5c940bb6a7919185effccd7cf14c0e350198b3aedbe1db789`  
		Last Modified: Tue, 11 Jul 2023 05:26:01 GMT  
		Size: 173.4 MB (173373450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b39c7f4340aa5dd678a6a0a9bc018229eaadb2a94a0af6bc41d17ce77cdefb`  
		Last Modified: Tue, 11 Jul 2023 05:25:57 GMT  
		Size: 304.2 MB (304236707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc58f6eb776423b78c7a88af6ee221317c44f67e3fb4f413ef3823e8895288a2`  
		Last Modified: Tue, 11 Jul 2023 05:25:43 GMT  
		Size: 2.3 MB (2343673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea5e5502a3de7ec04368cbbb5f6c48f21fc7eac2657e2376ab3c7271ad4f85d`  
		Last Modified: Tue, 11 Jul 2023 05:25:43 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f8adcd32841dea1f4e39476b790a663510401829d69a806cad6007452d0367`  
		Last Modified: Tue, 11 Jul 2023 05:25:43 GMT  
		Size: 2.3 KB (2310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa238d29e18bbc7bdc963a1e1b2680c62ba2df6944ca0da2f99bd14855d1534`  
		Last Modified: Tue, 11 Jul 2023 05:25:43 GMT  
		Size: 6.0 KB (6005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ff1ad0797d8b4bc76bf31cb29679b76b9a9af76a225e434abe3b7d81295b942`  
		Last Modified: Tue, 11 Jul 2023 05:25:43 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:stable-postgres`

```console
$ docker pull xwiki@sha256:143482a096b13073c1d9d59fde125210cd6009c4fb253a6d30cf5eaf8481fc5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:stable-postgres` - linux; amd64

```console
$ docker pull xwiki@sha256:4741e9d9b24c00013903dbabf718e61ef5c4b23fd41a283067988225a4ea60ae
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **586.8 MB (586784502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1a1f265f59dcb2e5a6888c86ef11b46a92e4d498dcf98b2ab1f05735021fa2a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:37:40 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:37:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:37:42 GMT
ADD file:140fb5108b4a2861b5718ad03b4a5174bba03589ea8d4c053e6a0b282f439ff3 in / 
# Wed, 28 Jun 2023 08:37:42 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:34:07 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:35:02 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 20:35:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 20:35:35 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 08:22:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 08:22:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 08:22:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 08:22:21 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 08:22:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:22:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:25:33 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 08:25:34 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 00:16:15 GMT
COPY dir:8ddeace4a16f09a0d97488e225c7b2e4a48c9a93484d24b46a09759f52800501 in /usr/local/tomcat 
# Tue, 11 Jul 2023 00:16:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 00:16:20 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 00:16:20 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 00:16:20 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 04:41:24 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 04:41:26 GMT
ENV XWIKI_VERSION=15.5
# Tue, 11 Jul 2023 04:41:26 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.5
# Tue, 11 Jul 2023 04:41:26 GMT
ENV XWIKI_DOWNLOAD_SHA256=e552586d371da33b012cfbd974b3ba80d1b147a5c892ad6cf989960212cdaa02
# Tue, 11 Jul 2023 04:42:04 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 04:42:05 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Tue, 11 Jul 2023 04:42:05 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 04:42:05 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 04:42:06 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 04:42:06 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 04:42:06 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 04:42:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 04:42:06 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:9d19ee268e0d7bcf6716e6658ee1b0384a71d6f2f9aa1ae2085610cf7c7b316f`  
		Last Modified: Wed, 28 Jun 2023 11:50:41 GMT  
		Size: 30.4 MB (30431229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32db0ad82863deaedd2f9a365e52f595085778d28bd1e6f1d351107590cad806`  
		Last Modified: Tue, 04 Jul 2023 20:39:05 GMT  
		Size: 12.5 MB (12495341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01bb55fbcae928d7e6c08d6618580d2b27ce6e46083f861bbed1e01db41c20b`  
		Last Modified: Tue, 04 Jul 2023 20:41:01 GMT  
		Size: 46.7 MB (46666353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297c6e3f57ee032a3cc5f0fd28b52687129e7a1e6485aea12aff08cb6620071e`  
		Last Modified: Tue, 04 Jul 2023 20:40:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15b01f5ab5b71b356d93dff08f5037af8e8a03b4657f1fd303052261161ebd8`  
		Last Modified: Wed, 05 Jul 2023 08:37:14 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c6051a2b9ffe906ea99b555033966c877468da73cd19fd793c86099d0af531`  
		Last Modified: Tue, 11 Jul 2023 00:38:45 GMT  
		Size: 12.3 MB (12274167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34aaed1f6a3460fc256e262b462c1180ccef1b0665ffd50f900d1ef9c19f1d24`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 454.7 KB (454674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b809bf54ada009dfd91afa6ad239f7a791807f2928941b7f969493ec38246be`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bd305e7867896df13faced03525a0f25bf1ac1b2a2c93e60382cdfd41c08e16`  
		Last Modified: Tue, 11 Jul 2023 04:45:43 GMT  
		Size: 179.3 MB (179276407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35bfb758076cf011f5df9081f31dfbcf656cd98cd11b65f53f3684ec1e485c8f`  
		Last Modified: Tue, 11 Jul 2023 04:45:37 GMT  
		Size: 304.2 MB (304236708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2f8ccc8af30dd82bb4657bfdb7193ed23e8dc8823df1eaea8b1c8e4ab85d60`  
		Last Modified: Tue, 11 Jul 2023 04:45:20 GMT  
		Size: 936.8 KB (936849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:822e7d00d75f2a5b9a34edd0741b7e19410deb191f96800278c2921b043c81cb`  
		Last Modified: Tue, 11 Jul 2023 04:45:19 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba3137d80fef0218e2aaa65df38833a3e9d79b0d6e0b8d441376edbc36190ab`  
		Last Modified: Tue, 11 Jul 2023 04:45:19 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d02045e3c19030183c43f79b2c5e3a2f244dda96d11e96014e91d90e85f6e3a9`  
		Last Modified: Tue, 11 Jul 2023 04:45:19 GMT  
		Size: 6.0 KB (6006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91afad54a0c6d44f603953379c22801e4dbc9f2c282eaa00e94946d1d77dc3a4`  
		Last Modified: Tue, 11 Jul 2023 04:45:19 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:stable-postgres` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:30799eeac6bc3f0efeefaf95f4161eeea6298cf60983391d2b7789735d58fa07
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.1 MB (578094027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc026cfcc219f16306961c1815044f7a63d5f49577815243d20c27d2d823d48`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:42:48 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:42:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:42:50 GMT
ADD file:262490f82459c14632f5c9a6d6a5cf6c07b4f307e8fd380fa764662cda46e88f in / 
# Wed, 28 Jun 2023 08:42:50 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:59 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 15:33:41 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 15:34:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 15:34:08 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 02:55:59 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 02:55:59 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 02:55:59 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 02:55:59 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 02:56:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 02:56:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 03:00:51 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 03:00:51 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 01:18:24 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 01:18:25 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 01:18:25 GMT
COPY dir:1743191a9534b9e7d795d3bf9ad18535d99e75967877447e17d7b63574d878d5 in /usr/local/tomcat 
# Tue, 11 Jul 2023 01:18:28 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 01:18:29 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 01:18:29 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 01:18:29 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 05:22:36 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 05:22:39 GMT
ENV XWIKI_VERSION=15.5
# Tue, 11 Jul 2023 05:22:39 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.5
# Tue, 11 Jul 2023 05:22:39 GMT
ENV XWIKI_DOWNLOAD_SHA256=e552586d371da33b012cfbd974b3ba80d1b147a5c892ad6cf989960212cdaa02
# Tue, 11 Jul 2023 05:23:18 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 05:23:21 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Tue, 11 Jul 2023 05:23:21 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 05:23:21 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 05:23:22 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 05:23:22 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 05:23:22 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 05:23:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 05:23:22 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:ac34a2e0269ced3acc355be706239ee0f3f1e73a035c40dd2fac74827164ee53`  
		Last Modified: Wed, 28 Jun 2023 23:23:40 GMT  
		Size: 28.4 MB (28391011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d9df805749ad7c4605f0d49a64da6a6173ab190ec361dc2063b6b73af59ab5`  
		Last Modified: Tue, 04 Jul 2023 15:36:55 GMT  
		Size: 12.5 MB (12455497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1e11a5919e5746092b2a288f71090ffdb0d3544b7b54c31ed0137e6d5d4735`  
		Last Modified: Tue, 04 Jul 2023 15:38:37 GMT  
		Size: 45.0 MB (45009079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80987dc89da28aa5ceec7a86ea74e13cee06ecd9304cf4c92d8f382c79eb4f2`  
		Last Modified: Tue, 04 Jul 2023 15:38:32 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de67c7824eef053da628456fe8aba244c4150024af9454dd4091763920d836c`  
		Last Modified: Wed, 05 Jul 2023 03:14:23 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f77f07e56c3d3019cd346deaeacbe572b15b26a924c19b6386877b47123a89e`  
		Last Modified: Tue, 11 Jul 2023 01:39:24 GMT  
		Size: 12.3 MB (12283700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2422cddd65b0ff63d783c999d005c42281720b8615f5872e1e8fdb32dd9981d9`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 455.1 KB (455052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b023f0d964d565a960e567dcaaa605fdff6da02b54971f4d0693506b481b8c`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:968d46d099e01403854799f31b6235698a474c27fd58b0172b1eb3889cd5067f`  
		Last Modified: Tue, 11 Jul 2023 05:26:50 GMT  
		Size: 174.3 MB (174313369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2894444c04152ca46b568422ea482a66ed3763028ff87cc82d80132ea0e4cdd`  
		Last Modified: Tue, 11 Jul 2023 05:26:46 GMT  
		Size: 304.2 MB (304236690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77118bb73ac2d6b789413d31beabdbb72e88543cca5b3e6406076fd10d40d8d3`  
		Last Modified: Tue, 11 Jul 2023 05:26:32 GMT  
		Size: 936.9 KB (936852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9eb9df1942e9402403596582620c7fb14dbdd8e12de634c88e080cc5795a812`  
		Last Modified: Tue, 11 Jul 2023 05:26:32 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d23fb311f1a568af6e8b96dcb8cfb10d4d96a88aee4243256a3e73f4727fa318`  
		Last Modified: Tue, 11 Jul 2023 05:26:32 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dd3c555379bf5bd7f8d13501bb806b6b5ffb4c2ecb169ce4485f1cbf0d26b9a`  
		Last Modified: Tue, 11 Jul 2023 05:26:32 GMT  
		Size: 6.0 KB (6006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8254381348a57ea56306a83d8f2a89630202f393f54d6102b5652be9cfa10f8f`  
		Last Modified: Tue, 11 Jul 2023 05:26:33 GMT  
		Size: 2.5 KB (2507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:stable-postgres-tomcat`

```console
$ docker pull xwiki@sha256:143482a096b13073c1d9d59fde125210cd6009c4fb253a6d30cf5eaf8481fc5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:stable-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:4741e9d9b24c00013903dbabf718e61ef5c4b23fd41a283067988225a4ea60ae
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **586.8 MB (586784502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1a1f265f59dcb2e5a6888c86ef11b46a92e4d498dcf98b2ab1f05735021fa2a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:37:40 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:37:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:37:42 GMT
ADD file:140fb5108b4a2861b5718ad03b4a5174bba03589ea8d4c053e6a0b282f439ff3 in / 
# Wed, 28 Jun 2023 08:37:42 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:34:07 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:35:02 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 20:35:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 20:35:35 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 08:22:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 08:22:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 08:22:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 08:22:21 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 08:22:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:22:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:25:33 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 08:25:34 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 00:16:15 GMT
COPY dir:8ddeace4a16f09a0d97488e225c7b2e4a48c9a93484d24b46a09759f52800501 in /usr/local/tomcat 
# Tue, 11 Jul 2023 00:16:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 00:16:20 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 00:16:20 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 00:16:20 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 04:41:24 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 04:41:26 GMT
ENV XWIKI_VERSION=15.5
# Tue, 11 Jul 2023 04:41:26 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.5
# Tue, 11 Jul 2023 04:41:26 GMT
ENV XWIKI_DOWNLOAD_SHA256=e552586d371da33b012cfbd974b3ba80d1b147a5c892ad6cf989960212cdaa02
# Tue, 11 Jul 2023 04:42:04 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 04:42:05 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Tue, 11 Jul 2023 04:42:05 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 04:42:05 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 04:42:06 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 04:42:06 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 04:42:06 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 04:42:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 04:42:06 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:9d19ee268e0d7bcf6716e6658ee1b0384a71d6f2f9aa1ae2085610cf7c7b316f`  
		Last Modified: Wed, 28 Jun 2023 11:50:41 GMT  
		Size: 30.4 MB (30431229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32db0ad82863deaedd2f9a365e52f595085778d28bd1e6f1d351107590cad806`  
		Last Modified: Tue, 04 Jul 2023 20:39:05 GMT  
		Size: 12.5 MB (12495341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01bb55fbcae928d7e6c08d6618580d2b27ce6e46083f861bbed1e01db41c20b`  
		Last Modified: Tue, 04 Jul 2023 20:41:01 GMT  
		Size: 46.7 MB (46666353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297c6e3f57ee032a3cc5f0fd28b52687129e7a1e6485aea12aff08cb6620071e`  
		Last Modified: Tue, 04 Jul 2023 20:40:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15b01f5ab5b71b356d93dff08f5037af8e8a03b4657f1fd303052261161ebd8`  
		Last Modified: Wed, 05 Jul 2023 08:37:14 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c6051a2b9ffe906ea99b555033966c877468da73cd19fd793c86099d0af531`  
		Last Modified: Tue, 11 Jul 2023 00:38:45 GMT  
		Size: 12.3 MB (12274167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34aaed1f6a3460fc256e262b462c1180ccef1b0665ffd50f900d1ef9c19f1d24`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 454.7 KB (454674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b809bf54ada009dfd91afa6ad239f7a791807f2928941b7f969493ec38246be`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bd305e7867896df13faced03525a0f25bf1ac1b2a2c93e60382cdfd41c08e16`  
		Last Modified: Tue, 11 Jul 2023 04:45:43 GMT  
		Size: 179.3 MB (179276407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35bfb758076cf011f5df9081f31dfbcf656cd98cd11b65f53f3684ec1e485c8f`  
		Last Modified: Tue, 11 Jul 2023 04:45:37 GMT  
		Size: 304.2 MB (304236708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2f8ccc8af30dd82bb4657bfdb7193ed23e8dc8823df1eaea8b1c8e4ab85d60`  
		Last Modified: Tue, 11 Jul 2023 04:45:20 GMT  
		Size: 936.8 KB (936849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:822e7d00d75f2a5b9a34edd0741b7e19410deb191f96800278c2921b043c81cb`  
		Last Modified: Tue, 11 Jul 2023 04:45:19 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba3137d80fef0218e2aaa65df38833a3e9d79b0d6e0b8d441376edbc36190ab`  
		Last Modified: Tue, 11 Jul 2023 04:45:19 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d02045e3c19030183c43f79b2c5e3a2f244dda96d11e96014e91d90e85f6e3a9`  
		Last Modified: Tue, 11 Jul 2023 04:45:19 GMT  
		Size: 6.0 KB (6006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91afad54a0c6d44f603953379c22801e4dbc9f2c282eaa00e94946d1d77dc3a4`  
		Last Modified: Tue, 11 Jul 2023 04:45:19 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:stable-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:30799eeac6bc3f0efeefaf95f4161eeea6298cf60983391d2b7789735d58fa07
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.1 MB (578094027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc026cfcc219f16306961c1815044f7a63d5f49577815243d20c27d2d823d48`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:42:48 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:42:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:42:50 GMT
ADD file:262490f82459c14632f5c9a6d6a5cf6c07b4f307e8fd380fa764662cda46e88f in / 
# Wed, 28 Jun 2023 08:42:50 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:59 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 15:33:41 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 15:34:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 15:34:08 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 02:55:59 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 02:55:59 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 02:55:59 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 02:55:59 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 02:56:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 02:56:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 03:00:51 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 03:00:51 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 01:18:24 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 01:18:25 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 01:18:25 GMT
COPY dir:1743191a9534b9e7d795d3bf9ad18535d99e75967877447e17d7b63574d878d5 in /usr/local/tomcat 
# Tue, 11 Jul 2023 01:18:28 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 01:18:29 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 01:18:29 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 01:18:29 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 05:22:36 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 05:22:39 GMT
ENV XWIKI_VERSION=15.5
# Tue, 11 Jul 2023 05:22:39 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.5
# Tue, 11 Jul 2023 05:22:39 GMT
ENV XWIKI_DOWNLOAD_SHA256=e552586d371da33b012cfbd974b3ba80d1b147a5c892ad6cf989960212cdaa02
# Tue, 11 Jul 2023 05:23:18 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 05:23:21 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Tue, 11 Jul 2023 05:23:21 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 05:23:21 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 05:23:22 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 05:23:22 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 05:23:22 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 05:23:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 05:23:22 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:ac34a2e0269ced3acc355be706239ee0f3f1e73a035c40dd2fac74827164ee53`  
		Last Modified: Wed, 28 Jun 2023 23:23:40 GMT  
		Size: 28.4 MB (28391011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d9df805749ad7c4605f0d49a64da6a6173ab190ec361dc2063b6b73af59ab5`  
		Last Modified: Tue, 04 Jul 2023 15:36:55 GMT  
		Size: 12.5 MB (12455497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1e11a5919e5746092b2a288f71090ffdb0d3544b7b54c31ed0137e6d5d4735`  
		Last Modified: Tue, 04 Jul 2023 15:38:37 GMT  
		Size: 45.0 MB (45009079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80987dc89da28aa5ceec7a86ea74e13cee06ecd9304cf4c92d8f382c79eb4f2`  
		Last Modified: Tue, 04 Jul 2023 15:38:32 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de67c7824eef053da628456fe8aba244c4150024af9454dd4091763920d836c`  
		Last Modified: Wed, 05 Jul 2023 03:14:23 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f77f07e56c3d3019cd346deaeacbe572b15b26a924c19b6386877b47123a89e`  
		Last Modified: Tue, 11 Jul 2023 01:39:24 GMT  
		Size: 12.3 MB (12283700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2422cddd65b0ff63d783c999d005c42281720b8615f5872e1e8fdb32dd9981d9`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 455.1 KB (455052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b023f0d964d565a960e567dcaaa605fdff6da02b54971f4d0693506b481b8c`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:968d46d099e01403854799f31b6235698a474c27fd58b0172b1eb3889cd5067f`  
		Last Modified: Tue, 11 Jul 2023 05:26:50 GMT  
		Size: 174.3 MB (174313369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2894444c04152ca46b568422ea482a66ed3763028ff87cc82d80132ea0e4cdd`  
		Last Modified: Tue, 11 Jul 2023 05:26:46 GMT  
		Size: 304.2 MB (304236690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77118bb73ac2d6b789413d31beabdbb72e88543cca5b3e6406076fd10d40d8d3`  
		Last Modified: Tue, 11 Jul 2023 05:26:32 GMT  
		Size: 936.9 KB (936852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9eb9df1942e9402403596582620c7fb14dbdd8e12de634c88e080cc5795a812`  
		Last Modified: Tue, 11 Jul 2023 05:26:32 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d23fb311f1a568af6e8b96dcb8cfb10d4d96a88aee4243256a3e73f4727fa318`  
		Last Modified: Tue, 11 Jul 2023 05:26:32 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dd3c555379bf5bd7f8d13501bb806b6b5ffb4c2ecb169ce4485f1cbf0d26b9a`  
		Last Modified: Tue, 11 Jul 2023 05:26:32 GMT  
		Size: 6.0 KB (6006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8254381348a57ea56306a83d8f2a89630202f393f54d6102b5652be9cfa10f8f`  
		Last Modified: Tue, 11 Jul 2023 05:26:33 GMT  
		Size: 2.5 KB (2507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
