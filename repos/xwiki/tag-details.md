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
-	[`xwiki:14.10.11`](#xwiki141011)
-	[`xwiki:14.10.11-mariadb-tomcat`](#xwiki141011-mariadb-tomcat)
-	[`xwiki:14.10.11-mysql-tomcat`](#xwiki141011-mysql-tomcat)
-	[`xwiki:14.10.11-postgres-tomcat`](#xwiki141011-postgres-tomcat)
-	[`xwiki:15`](#xwiki15)
-	[`xwiki:15-mariadb-tomcat`](#xwiki15-mariadb-tomcat)
-	[`xwiki:15-mysql-tomcat`](#xwiki15-mysql-tomcat)
-	[`xwiki:15-postgres-tomcat`](#xwiki15-postgres-tomcat)
-	[`xwiki:15.4`](#xwiki154)
-	[`xwiki:15.4-mariadb-tomcat`](#xwiki154-mariadb-tomcat)
-	[`xwiki:15.4-mysql-tomcat`](#xwiki154-mysql-tomcat)
-	[`xwiki:15.4-postgres-tomcat`](#xwiki154-postgres-tomcat)
-	[`xwiki:15.4.0`](#xwiki1540)
-	[`xwiki:15.4.0-mariadb-tomcat`](#xwiki1540-mariadb-tomcat)
-	[`xwiki:15.4.0-mysql-tomcat`](#xwiki1540-mysql-tomcat)
-	[`xwiki:15.4.0-postgres-tomcat`](#xwiki1540-postgres-tomcat)
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
$ docker pull xwiki@sha256:3cb3e791882b8ad6819d53ac0e7fb6c678ba6435b06061929dca6ce1a98fbef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:14` - linux; amd64

```console
$ docker pull xwiki@sha256:8d0ae8c6e385bf7493b07cbab2a2afa371e97538db4f1c040a18c393b5d1e090
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.2 MB (590232292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eff782e5d932a0d40c015b5812ebe948e85c30648a4875e24e6320a36ebb037b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 07:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 07:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 07:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 07:26:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:27:16 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 04 May 2023 07:27:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 07:27:40 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 16:13:14 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 04 May 2023 16:13:14 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 16:13:14 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 04 May 2023 16:13:14 GMT
WORKDIR /usr/local/tomcat
# Thu, 04 May 2023 16:13:14 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 16:13:15 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 16:14:45 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 04 May 2023 16:14:45 GMT
ENV TOMCAT_MAJOR=9
# Wed, 10 May 2023 18:01:17 GMT
ENV TOMCAT_VERSION=9.0.75
# Wed, 10 May 2023 18:01:17 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Wed, 10 May 2023 18:01:17 GMT
COPY dir:606cc669e6833afa7967597ca36d4a4497efbb54719c008108649021142d7549 in /usr/local/tomcat 
# Wed, 10 May 2023 18:01:21 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 18:01:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 10 May 2023 18:01:23 GMT
EXPOSE 8080
# Wed, 10 May 2023 18:01:23 GMT
CMD ["catalina.sh" "run"]
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 10 May 2023 18:28:05 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 24 May 2023 22:47:42 GMT
ENV XWIKI_VERSION=14.10.11
# Wed, 24 May 2023 22:47:42 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.11
# Wed, 24 May 2023 22:47:42 GMT
ENV XWIKI_DOWNLOAD_SHA256=0804bdbc2a4eb370a25cfcd9a2185e80e007180007d15fdaa4d371dbd02b5d43
# Wed, 24 May 2023 22:48:21 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 24 May 2023 22:48:22 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Wed, 24 May 2023 22:48:22 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Wed, 24 May 2023 22:48:22 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Wed, 24 May 2023 22:48:22 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Wed, 24 May 2023 22:48:22 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Wed, 24 May 2023 22:48:23 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Wed, 24 May 2023 22:48:23 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 24 May 2023 22:48:23 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 24 May 2023 22:48:23 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 24 May 2023 22:48:24 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 24 May 2023 22:48:24 GMT
VOLUME [/usr/local/xwiki]
# Wed, 24 May 2023 22:48:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 May 2023 22:48:24 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458b02b5411a07f3b354cde2b461caffc1bb184a3413b5736a9e67ee87cb28b2`  
		Last Modified: Thu, 04 May 2023 07:30:02 GMT  
		Size: 12.5 MB (12504170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04a165ead1d5eabe89dc88e53286af89caab22a5d20c53007b9e6e508affb4b`  
		Last Modified: Thu, 04 May 2023 07:31:19 GMT  
		Size: 46.7 MB (46666270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1187c73b18505bd4495bc03ccbdb723388dfe4d633fd12be845dfe8e253e48e2`  
		Last Modified: Thu, 04 May 2023 07:31:12 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c833cbb14374cde014505e77f6a6122773984a691844e4138fc15cae99ba625`  
		Last Modified: Thu, 04 May 2023 16:24:19 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439ac04571c77c4330db518bc8f35b70f8723246ed34c98787f7ac8d7dc30b42`  
		Last Modified: Wed, 10 May 2023 18:09:06 GMT  
		Size: 12.2 MB (12236613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8e775ba0b76c6692c0b9211e4b94653ba2aa16fdc7a5e3347aba962b684508`  
		Last Modified: Wed, 10 May 2023 18:09:06 GMT  
		Size: 454.2 KB (454222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee5c1ba4848e97d4e3c43d9d4bca0eeeccf2d5d7f6d805d748da4a7d24ad14e`  
		Last Modified: Wed, 10 May 2023 18:09:05 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffadd10be916fc5729676141f5d0ba6aa30968b75555790e449d4988dc81332a`  
		Last Modified: Wed, 10 May 2023 18:32:42 GMT  
		Size: 178.3 MB (178334017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3968819bf3a63424c2b6a4e9591f0c9e6ffbb99a92e0c8d8bb65c67dee37c591`  
		Last Modified: Wed, 24 May 2023 22:50:04 GMT  
		Size: 307.3 MB (307250466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab4c543f2a230baf4ee559f04be553bc00d7b77cc356fee1f21587123cb6977`  
		Last Modified: Wed, 24 May 2023 22:49:49 GMT  
		Size: 2.3 MB (2343680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22684cbd7ece18edde12615b426a6542f278c82ffebfd4d0e88ef0ff8fbde0b`  
		Last Modified: Wed, 24 May 2023 22:49:48 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5270a8761eb66f6e2d094c0879e26935456fa9e19b282bbed9418b58631140c1`  
		Last Modified: Wed, 24 May 2023 22:49:48 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efce4adb2bae1b274febb0d3785c785befb8c4de6c50df158a2aa23673c5b60d`  
		Last Modified: Wed, 24 May 2023 22:49:48 GMT  
		Size: 6.0 KB (6017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9715a623bab854429c5628dcca4718382ada25dbc334b3d61b24a46031cd5d44`  
		Last Modified: Wed, 24 May 2023 22:49:48 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:14` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:15957635ec1e31779c981c0817bf66a72c04e6218e1acc75ef471fc7f46dd01c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.5 MB (581515826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aa7648bbd0225e907a6fd992596c1aedb9a12baa3eb30a4a458df9d4af79c91`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 25 Apr 2023 17:31:58 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:31:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:31:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:31:59 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:32:02 GMT
ADD file:aee0d7770ef2f24dc9697e86d391529d001a4013b6e30a3ac90a57932814a57e in / 
# Tue, 25 Apr 2023 17:32:02 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 03:25:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 03:25:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 03:25:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 03:25:23 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 03:25:47 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 04 May 2023 03:26:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 03:26:10 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 11:14:20 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 04 May 2023 11:14:20 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 11:14:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 04 May 2023 11:14:21 GMT
WORKDIR /usr/local/tomcat
# Thu, 04 May 2023 11:14:21 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 11:14:21 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 11:15:34 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 04 May 2023 11:15:34 GMT
ENV TOMCAT_MAJOR=9
# Wed, 10 May 2023 17:56:49 GMT
ENV TOMCAT_VERSION=9.0.75
# Wed, 10 May 2023 17:56:49 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Wed, 10 May 2023 17:56:49 GMT
COPY dir:2a613f9e425d5febc8be5b6c17f49b39f1b8ad84b1601f07f76abed41b25b24b in /usr/local/tomcat 
# Wed, 10 May 2023 17:56:52 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 17:56:54 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 10 May 2023 17:56:54 GMT
EXPOSE 8080
# Wed, 10 May 2023 17:56:54 GMT
CMD ["catalina.sh" "run"]
# Wed, 10 May 2023 18:22:09 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 10 May 2023 18:23:10 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 24 May 2023 23:08:47 GMT
ENV XWIKI_VERSION=14.10.11
# Wed, 24 May 2023 23:08:47 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.11
# Wed, 24 May 2023 23:08:48 GMT
ENV XWIKI_DOWNLOAD_SHA256=0804bdbc2a4eb370a25cfcd9a2185e80e007180007d15fdaa4d371dbd02b5d43
# Wed, 24 May 2023 23:09:27 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 24 May 2023 23:09:29 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Wed, 24 May 2023 23:09:29 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Wed, 24 May 2023 23:09:30 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Wed, 24 May 2023 23:09:30 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Wed, 24 May 2023 23:09:30 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Wed, 24 May 2023 23:09:31 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Wed, 24 May 2023 23:09:31 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 24 May 2023 23:09:31 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 24 May 2023 23:09:31 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 24 May 2023 23:09:31 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 24 May 2023 23:09:32 GMT
VOLUME [/usr/local/xwiki]
# Wed, 24 May 2023 23:09:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 May 2023 23:09:32 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f3f60f415e9a03eed88bd5dd5268c841cde08dacf16911a3ef1e4e0fcdd76568`  
		Last Modified: Wed, 26 Apr 2023 02:08:37 GMT  
		Size: 28.4 MB (28389440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fb3595122d1cb6fffe722e2624c3c89b00776b393256a5444af56ceda691cf`  
		Last Modified: Thu, 04 May 2023 03:28:13 GMT  
		Size: 12.5 MB (12463858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5542665e33e692b672a405517e6e267c4c6e210bc410b97a6a1ce732618caa87`  
		Last Modified: Thu, 04 May 2023 03:29:19 GMT  
		Size: 45.0 MB (45009401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e52b8550f0ced98adb0880bd041e361ffb69810e6071e6d71eb2ec0c8ecfad5`  
		Last Modified: Thu, 04 May 2023 03:29:14 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea5566732e0a920d0a63e4fbebf073d2c49e3f80716df462e73f895cc0c5dfa`  
		Last Modified: Thu, 04 May 2023 11:24:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c6d16bf5ef403ef11a1cc9e40650f402cd1f8269d16982f7daebc2a76ab0d9`  
		Last Modified: Wed, 10 May 2023 18:03:56 GMT  
		Size: 12.2 MB (12242222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eaf464f1c82b5f85e3173b2c732f0928a28e669fcc4af9eb6da48199e92ae50`  
		Last Modified: Wed, 10 May 2023 18:03:55 GMT  
		Size: 453.7 KB (453682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ef5f2b94b25f2b0f609c429cc1626d9dd857d8294d2d872d6595bdeff3a5ca`  
		Last Modified: Wed, 10 May 2023 18:03:55 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7cc67d2dc8f70f6e05051c0e95eb0de93a45de55ba65c355eedaff2bf118e42`  
		Last Modified: Wed, 10 May 2023 18:27:43 GMT  
		Size: 173.4 MB (173350375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0f918d67c923bb6ad20257659a178cf82a52dbd68eda4c094eb3fb372831c2c`  
		Last Modified: Wed, 24 May 2023 23:11:04 GMT  
		Size: 307.3 MB (307250539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced4cf6fb2a03eefd5f5bf442bda27c93928535469b7e8d6fc9c5d7b5ae30b2f`  
		Last Modified: Wed, 24 May 2023 23:10:51 GMT  
		Size: 2.3 MB (2343677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98623f72442cf00c262363a201209a0aa274f36c3ea6fc9f6982e636f879fa70`  
		Last Modified: Wed, 24 May 2023 23:10:50 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7788f555a977b55dd4bb3cc03f0877839200ef650618e788503063bad30080ce`  
		Last Modified: Wed, 24 May 2023 23:10:50 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874c98264dbb8128fd9c27e97654851dfbde45dfb396778744d7616b44591eae`  
		Last Modified: Wed, 24 May 2023 23:10:50 GMT  
		Size: 6.0 KB (6014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee9de251f061dd4ab29b65e5807e482de72b8f045af577bdc2ade102cedf52d`  
		Last Modified: Wed, 24 May 2023 23:10:50 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:14-mariadb-tomcat`

```console
$ docker pull xwiki@sha256:c1da5ed330d5ca59735d572da388f3a2ce1fbbaf48e03de0b7d0799d1626c0ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:14-mariadb-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:1a75db7f8992a7c4ee2c526aa1a525456625e7a8d132487a30b4db9e5a4d63eb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **588.5 MB (588483181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c4b7b90fa36f2254d9a63b8f50fc26caa9e6bf856d9a1b53f83db9206d899d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 07:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 07:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 07:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 07:26:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:27:16 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 04 May 2023 07:27:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 07:27:40 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 16:13:14 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 04 May 2023 16:13:14 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 16:13:14 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 04 May 2023 16:13:14 GMT
WORKDIR /usr/local/tomcat
# Thu, 04 May 2023 16:13:14 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 16:13:15 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 16:14:45 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 04 May 2023 16:14:45 GMT
ENV TOMCAT_MAJOR=9
# Wed, 10 May 2023 18:01:17 GMT
ENV TOMCAT_VERSION=9.0.75
# Wed, 10 May 2023 18:01:17 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Wed, 10 May 2023 18:01:17 GMT
COPY dir:606cc669e6833afa7967597ca36d4a4497efbb54719c008108649021142d7549 in /usr/local/tomcat 
# Wed, 10 May 2023 18:01:21 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 18:01:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 10 May 2023 18:01:23 GMT
EXPOSE 8080
# Wed, 10 May 2023 18:01:23 GMT
CMD ["catalina.sh" "run"]
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 10 May 2023 18:28:05 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 24 May 2023 22:47:42 GMT
ENV XWIKI_VERSION=14.10.11
# Wed, 24 May 2023 22:47:42 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.11
# Wed, 24 May 2023 22:47:42 GMT
ENV XWIKI_DOWNLOAD_SHA256=0804bdbc2a4eb370a25cfcd9a2185e80e007180007d15fdaa4d371dbd02b5d43
# Wed, 24 May 2023 22:48:21 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 24 May 2023 22:49:20 GMT
ENV MARIADB_JDBC_VERSION=3.1.4
# Wed, 24 May 2023 22:49:20 GMT
ENV MARIADB_JDBC_SHA256=eb88b5d727d82e25117e2b6fabcec1daf734633b0a576456c73215884c189ad4
# Wed, 24 May 2023 22:49:20 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.1.4
# Wed, 24 May 2023 22:49:20 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.1.4.jar
# Wed, 24 May 2023 22:49:20 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.1.4.jar
# Wed, 24 May 2023 22:49:21 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Wed, 24 May 2023 22:49:21 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 24 May 2023 22:49:21 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 24 May 2023 22:49:22 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 24 May 2023 22:49:22 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 24 May 2023 22:49:22 GMT
VOLUME [/usr/local/xwiki]
# Wed, 24 May 2023 22:49:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 May 2023 22:49:22 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458b02b5411a07f3b354cde2b461caffc1bb184a3413b5736a9e67ee87cb28b2`  
		Last Modified: Thu, 04 May 2023 07:30:02 GMT  
		Size: 12.5 MB (12504170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04a165ead1d5eabe89dc88e53286af89caab22a5d20c53007b9e6e508affb4b`  
		Last Modified: Thu, 04 May 2023 07:31:19 GMT  
		Size: 46.7 MB (46666270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1187c73b18505bd4495bc03ccbdb723388dfe4d633fd12be845dfe8e253e48e2`  
		Last Modified: Thu, 04 May 2023 07:31:12 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c833cbb14374cde014505e77f6a6122773984a691844e4138fc15cae99ba625`  
		Last Modified: Thu, 04 May 2023 16:24:19 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439ac04571c77c4330db518bc8f35b70f8723246ed34c98787f7ac8d7dc30b42`  
		Last Modified: Wed, 10 May 2023 18:09:06 GMT  
		Size: 12.2 MB (12236613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8e775ba0b76c6692c0b9211e4b94653ba2aa16fdc7a5e3347aba962b684508`  
		Last Modified: Wed, 10 May 2023 18:09:06 GMT  
		Size: 454.2 KB (454222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee5c1ba4848e97d4e3c43d9d4bca0eeeccf2d5d7f6d805d748da4a7d24ad14e`  
		Last Modified: Wed, 10 May 2023 18:09:05 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffadd10be916fc5729676141f5d0ba6aa30968b75555790e449d4988dc81332a`  
		Last Modified: Wed, 10 May 2023 18:32:42 GMT  
		Size: 178.3 MB (178334017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3968819bf3a63424c2b6a4e9591f0c9e6ffbb99a92e0c8d8bb65c67dee37c591`  
		Last Modified: Wed, 24 May 2023 22:50:04 GMT  
		Size: 307.3 MB (307250466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe65a2b1c269931f9affdbf4926be3a7e6789a0eb5ef5c8469c0ab01708aa54e`  
		Last Modified: Wed, 24 May 2023 22:51:02 GMT  
		Size: 594.6 KB (594559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b1b0dad9556a98d3e225960bc3fdd9550ee0d50cc15b4667535a69cc8cc4f5`  
		Last Modified: Wed, 24 May 2023 22:51:02 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b44a0baefcddcca335cf3e635a10b22f472dcb576dfa3b75755f9db5fc9ec853`  
		Last Modified: Wed, 24 May 2023 22:51:02 GMT  
		Size: 2.3 KB (2313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ebfb8ffc93a8da62fdc799b946b53ae557f1061d920db81d002a7fea3bacbde`  
		Last Modified: Wed, 24 May 2023 22:51:02 GMT  
		Size: 6.0 KB (6019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f48b704e13efa0bd740446998f3193c87fcb7dadc14138af9f9103fdbdcdc87`  
		Last Modified: Wed, 24 May 2023 22:51:02 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:14-mariadb-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:00f5266daef25dc10485eca8533381e175b534a692a79b5e108b3563b604c1a5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.8 MB (579766697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e448e5a8cc6e1fb57ca6ebb008b4fa70de9683b31e4f558bd222f5a5fd0b441f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 25 Apr 2023 17:31:58 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:31:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:31:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:31:59 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:32:02 GMT
ADD file:aee0d7770ef2f24dc9697e86d391529d001a4013b6e30a3ac90a57932814a57e in / 
# Tue, 25 Apr 2023 17:32:02 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 03:25:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 03:25:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 03:25:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 03:25:23 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 03:25:47 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 04 May 2023 03:26:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 03:26:10 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 11:14:20 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 04 May 2023 11:14:20 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 11:14:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 04 May 2023 11:14:21 GMT
WORKDIR /usr/local/tomcat
# Thu, 04 May 2023 11:14:21 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 11:14:21 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 11:15:34 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 04 May 2023 11:15:34 GMT
ENV TOMCAT_MAJOR=9
# Wed, 10 May 2023 17:56:49 GMT
ENV TOMCAT_VERSION=9.0.75
# Wed, 10 May 2023 17:56:49 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Wed, 10 May 2023 17:56:49 GMT
COPY dir:2a613f9e425d5febc8be5b6c17f49b39f1b8ad84b1601f07f76abed41b25b24b in /usr/local/tomcat 
# Wed, 10 May 2023 17:56:52 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 17:56:54 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 10 May 2023 17:56:54 GMT
EXPOSE 8080
# Wed, 10 May 2023 17:56:54 GMT
CMD ["catalina.sh" "run"]
# Wed, 10 May 2023 18:22:09 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 10 May 2023 18:23:10 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 24 May 2023 23:08:47 GMT
ENV XWIKI_VERSION=14.10.11
# Wed, 24 May 2023 23:08:47 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.11
# Wed, 24 May 2023 23:08:48 GMT
ENV XWIKI_DOWNLOAD_SHA256=0804bdbc2a4eb370a25cfcd9a2185e80e007180007d15fdaa4d371dbd02b5d43
# Wed, 24 May 2023 23:09:27 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 24 May 2023 23:10:23 GMT
ENV MARIADB_JDBC_VERSION=3.1.4
# Wed, 24 May 2023 23:10:23 GMT
ENV MARIADB_JDBC_SHA256=eb88b5d727d82e25117e2b6fabcec1daf734633b0a576456c73215884c189ad4
# Wed, 24 May 2023 23:10:23 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.1.4
# Wed, 24 May 2023 23:10:23 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.1.4.jar
# Wed, 24 May 2023 23:10:23 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.1.4.jar
# Wed, 24 May 2023 23:10:24 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Wed, 24 May 2023 23:10:24 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 24 May 2023 23:10:24 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 24 May 2023 23:10:25 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 24 May 2023 23:10:25 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 24 May 2023 23:10:25 GMT
VOLUME [/usr/local/xwiki]
# Wed, 24 May 2023 23:10:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 May 2023 23:10:25 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f3f60f415e9a03eed88bd5dd5268c841cde08dacf16911a3ef1e4e0fcdd76568`  
		Last Modified: Wed, 26 Apr 2023 02:08:37 GMT  
		Size: 28.4 MB (28389440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fb3595122d1cb6fffe722e2624c3c89b00776b393256a5444af56ceda691cf`  
		Last Modified: Thu, 04 May 2023 03:28:13 GMT  
		Size: 12.5 MB (12463858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5542665e33e692b672a405517e6e267c4c6e210bc410b97a6a1ce732618caa87`  
		Last Modified: Thu, 04 May 2023 03:29:19 GMT  
		Size: 45.0 MB (45009401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e52b8550f0ced98adb0880bd041e361ffb69810e6071e6d71eb2ec0c8ecfad5`  
		Last Modified: Thu, 04 May 2023 03:29:14 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea5566732e0a920d0a63e4fbebf073d2c49e3f80716df462e73f895cc0c5dfa`  
		Last Modified: Thu, 04 May 2023 11:24:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c6d16bf5ef403ef11a1cc9e40650f402cd1f8269d16982f7daebc2a76ab0d9`  
		Last Modified: Wed, 10 May 2023 18:03:56 GMT  
		Size: 12.2 MB (12242222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eaf464f1c82b5f85e3173b2c732f0928a28e669fcc4af9eb6da48199e92ae50`  
		Last Modified: Wed, 10 May 2023 18:03:55 GMT  
		Size: 453.7 KB (453682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ef5f2b94b25f2b0f609c429cc1626d9dd857d8294d2d872d6595bdeff3a5ca`  
		Last Modified: Wed, 10 May 2023 18:03:55 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7cc67d2dc8f70f6e05051c0e95eb0de93a45de55ba65c355eedaff2bf118e42`  
		Last Modified: Wed, 10 May 2023 18:27:43 GMT  
		Size: 173.4 MB (173350375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0f918d67c923bb6ad20257659a178cf82a52dbd68eda4c094eb3fb372831c2c`  
		Last Modified: Wed, 24 May 2023 23:11:04 GMT  
		Size: 307.3 MB (307250539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d912a3a12e11af60d952ffa7ac5359c7aa515a7300f75c5ba871ea94e62bd43`  
		Last Modified: Wed, 24 May 2023 23:12:02 GMT  
		Size: 594.5 KB (594549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f871b4dce32a1e7dcce9033dac703bc174253e8b26f41ea7a7d4c4ae1d98372f`  
		Last Modified: Wed, 24 May 2023 23:12:02 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f1d5bccd3396b98e1cf536def6525a295c0a35c6c70a438fc6a917b322efd5f`  
		Last Modified: Wed, 24 May 2023 23:12:02 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b11946e15dcff3a5243af68d7416f684d866731eedb590452d184678df469e`  
		Last Modified: Wed, 24 May 2023 23:12:02 GMT  
		Size: 6.0 KB (6013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33aa2a2a6531b6d4ff0f2638634bbb0a42a3796e25d026234551deb2add3b637`  
		Last Modified: Wed, 24 May 2023 23:12:02 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:14-mysql-tomcat`

```console
$ docker pull xwiki@sha256:3cb3e791882b8ad6819d53ac0e7fb6c678ba6435b06061929dca6ce1a98fbef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:14-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:8d0ae8c6e385bf7493b07cbab2a2afa371e97538db4f1c040a18c393b5d1e090
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.2 MB (590232292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eff782e5d932a0d40c015b5812ebe948e85c30648a4875e24e6320a36ebb037b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 07:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 07:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 07:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 07:26:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:27:16 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 04 May 2023 07:27:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 07:27:40 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 16:13:14 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 04 May 2023 16:13:14 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 16:13:14 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 04 May 2023 16:13:14 GMT
WORKDIR /usr/local/tomcat
# Thu, 04 May 2023 16:13:14 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 16:13:15 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 16:14:45 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 04 May 2023 16:14:45 GMT
ENV TOMCAT_MAJOR=9
# Wed, 10 May 2023 18:01:17 GMT
ENV TOMCAT_VERSION=9.0.75
# Wed, 10 May 2023 18:01:17 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Wed, 10 May 2023 18:01:17 GMT
COPY dir:606cc669e6833afa7967597ca36d4a4497efbb54719c008108649021142d7549 in /usr/local/tomcat 
# Wed, 10 May 2023 18:01:21 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 18:01:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 10 May 2023 18:01:23 GMT
EXPOSE 8080
# Wed, 10 May 2023 18:01:23 GMT
CMD ["catalina.sh" "run"]
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 10 May 2023 18:28:05 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 24 May 2023 22:47:42 GMT
ENV XWIKI_VERSION=14.10.11
# Wed, 24 May 2023 22:47:42 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.11
# Wed, 24 May 2023 22:47:42 GMT
ENV XWIKI_DOWNLOAD_SHA256=0804bdbc2a4eb370a25cfcd9a2185e80e007180007d15fdaa4d371dbd02b5d43
# Wed, 24 May 2023 22:48:21 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 24 May 2023 22:48:22 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Wed, 24 May 2023 22:48:22 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Wed, 24 May 2023 22:48:22 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Wed, 24 May 2023 22:48:22 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Wed, 24 May 2023 22:48:22 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Wed, 24 May 2023 22:48:23 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Wed, 24 May 2023 22:48:23 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 24 May 2023 22:48:23 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 24 May 2023 22:48:23 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 24 May 2023 22:48:24 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 24 May 2023 22:48:24 GMT
VOLUME [/usr/local/xwiki]
# Wed, 24 May 2023 22:48:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 May 2023 22:48:24 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458b02b5411a07f3b354cde2b461caffc1bb184a3413b5736a9e67ee87cb28b2`  
		Last Modified: Thu, 04 May 2023 07:30:02 GMT  
		Size: 12.5 MB (12504170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04a165ead1d5eabe89dc88e53286af89caab22a5d20c53007b9e6e508affb4b`  
		Last Modified: Thu, 04 May 2023 07:31:19 GMT  
		Size: 46.7 MB (46666270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1187c73b18505bd4495bc03ccbdb723388dfe4d633fd12be845dfe8e253e48e2`  
		Last Modified: Thu, 04 May 2023 07:31:12 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c833cbb14374cde014505e77f6a6122773984a691844e4138fc15cae99ba625`  
		Last Modified: Thu, 04 May 2023 16:24:19 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439ac04571c77c4330db518bc8f35b70f8723246ed34c98787f7ac8d7dc30b42`  
		Last Modified: Wed, 10 May 2023 18:09:06 GMT  
		Size: 12.2 MB (12236613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8e775ba0b76c6692c0b9211e4b94653ba2aa16fdc7a5e3347aba962b684508`  
		Last Modified: Wed, 10 May 2023 18:09:06 GMT  
		Size: 454.2 KB (454222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee5c1ba4848e97d4e3c43d9d4bca0eeeccf2d5d7f6d805d748da4a7d24ad14e`  
		Last Modified: Wed, 10 May 2023 18:09:05 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffadd10be916fc5729676141f5d0ba6aa30968b75555790e449d4988dc81332a`  
		Last Modified: Wed, 10 May 2023 18:32:42 GMT  
		Size: 178.3 MB (178334017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3968819bf3a63424c2b6a4e9591f0c9e6ffbb99a92e0c8d8bb65c67dee37c591`  
		Last Modified: Wed, 24 May 2023 22:50:04 GMT  
		Size: 307.3 MB (307250466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab4c543f2a230baf4ee559f04be553bc00d7b77cc356fee1f21587123cb6977`  
		Last Modified: Wed, 24 May 2023 22:49:49 GMT  
		Size: 2.3 MB (2343680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22684cbd7ece18edde12615b426a6542f278c82ffebfd4d0e88ef0ff8fbde0b`  
		Last Modified: Wed, 24 May 2023 22:49:48 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5270a8761eb66f6e2d094c0879e26935456fa9e19b282bbed9418b58631140c1`  
		Last Modified: Wed, 24 May 2023 22:49:48 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efce4adb2bae1b274febb0d3785c785befb8c4de6c50df158a2aa23673c5b60d`  
		Last Modified: Wed, 24 May 2023 22:49:48 GMT  
		Size: 6.0 KB (6017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9715a623bab854429c5628dcca4718382ada25dbc334b3d61b24a46031cd5d44`  
		Last Modified: Wed, 24 May 2023 22:49:48 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:14-mysql-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:15957635ec1e31779c981c0817bf66a72c04e6218e1acc75ef471fc7f46dd01c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.5 MB (581515826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aa7648bbd0225e907a6fd992596c1aedb9a12baa3eb30a4a458df9d4af79c91`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 25 Apr 2023 17:31:58 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:31:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:31:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:31:59 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:32:02 GMT
ADD file:aee0d7770ef2f24dc9697e86d391529d001a4013b6e30a3ac90a57932814a57e in / 
# Tue, 25 Apr 2023 17:32:02 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 03:25:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 03:25:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 03:25:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 03:25:23 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 03:25:47 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 04 May 2023 03:26:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 03:26:10 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 11:14:20 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 04 May 2023 11:14:20 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 11:14:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 04 May 2023 11:14:21 GMT
WORKDIR /usr/local/tomcat
# Thu, 04 May 2023 11:14:21 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 11:14:21 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 11:15:34 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 04 May 2023 11:15:34 GMT
ENV TOMCAT_MAJOR=9
# Wed, 10 May 2023 17:56:49 GMT
ENV TOMCAT_VERSION=9.0.75
# Wed, 10 May 2023 17:56:49 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Wed, 10 May 2023 17:56:49 GMT
COPY dir:2a613f9e425d5febc8be5b6c17f49b39f1b8ad84b1601f07f76abed41b25b24b in /usr/local/tomcat 
# Wed, 10 May 2023 17:56:52 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 17:56:54 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 10 May 2023 17:56:54 GMT
EXPOSE 8080
# Wed, 10 May 2023 17:56:54 GMT
CMD ["catalina.sh" "run"]
# Wed, 10 May 2023 18:22:09 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 10 May 2023 18:23:10 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 24 May 2023 23:08:47 GMT
ENV XWIKI_VERSION=14.10.11
# Wed, 24 May 2023 23:08:47 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.11
# Wed, 24 May 2023 23:08:48 GMT
ENV XWIKI_DOWNLOAD_SHA256=0804bdbc2a4eb370a25cfcd9a2185e80e007180007d15fdaa4d371dbd02b5d43
# Wed, 24 May 2023 23:09:27 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 24 May 2023 23:09:29 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Wed, 24 May 2023 23:09:29 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Wed, 24 May 2023 23:09:30 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Wed, 24 May 2023 23:09:30 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Wed, 24 May 2023 23:09:30 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Wed, 24 May 2023 23:09:31 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Wed, 24 May 2023 23:09:31 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 24 May 2023 23:09:31 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 24 May 2023 23:09:31 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 24 May 2023 23:09:31 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 24 May 2023 23:09:32 GMT
VOLUME [/usr/local/xwiki]
# Wed, 24 May 2023 23:09:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 May 2023 23:09:32 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f3f60f415e9a03eed88bd5dd5268c841cde08dacf16911a3ef1e4e0fcdd76568`  
		Last Modified: Wed, 26 Apr 2023 02:08:37 GMT  
		Size: 28.4 MB (28389440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fb3595122d1cb6fffe722e2624c3c89b00776b393256a5444af56ceda691cf`  
		Last Modified: Thu, 04 May 2023 03:28:13 GMT  
		Size: 12.5 MB (12463858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5542665e33e692b672a405517e6e267c4c6e210bc410b97a6a1ce732618caa87`  
		Last Modified: Thu, 04 May 2023 03:29:19 GMT  
		Size: 45.0 MB (45009401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e52b8550f0ced98adb0880bd041e361ffb69810e6071e6d71eb2ec0c8ecfad5`  
		Last Modified: Thu, 04 May 2023 03:29:14 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea5566732e0a920d0a63e4fbebf073d2c49e3f80716df462e73f895cc0c5dfa`  
		Last Modified: Thu, 04 May 2023 11:24:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c6d16bf5ef403ef11a1cc9e40650f402cd1f8269d16982f7daebc2a76ab0d9`  
		Last Modified: Wed, 10 May 2023 18:03:56 GMT  
		Size: 12.2 MB (12242222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eaf464f1c82b5f85e3173b2c732f0928a28e669fcc4af9eb6da48199e92ae50`  
		Last Modified: Wed, 10 May 2023 18:03:55 GMT  
		Size: 453.7 KB (453682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ef5f2b94b25f2b0f609c429cc1626d9dd857d8294d2d872d6595bdeff3a5ca`  
		Last Modified: Wed, 10 May 2023 18:03:55 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7cc67d2dc8f70f6e05051c0e95eb0de93a45de55ba65c355eedaff2bf118e42`  
		Last Modified: Wed, 10 May 2023 18:27:43 GMT  
		Size: 173.4 MB (173350375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0f918d67c923bb6ad20257659a178cf82a52dbd68eda4c094eb3fb372831c2c`  
		Last Modified: Wed, 24 May 2023 23:11:04 GMT  
		Size: 307.3 MB (307250539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced4cf6fb2a03eefd5f5bf442bda27c93928535469b7e8d6fc9c5d7b5ae30b2f`  
		Last Modified: Wed, 24 May 2023 23:10:51 GMT  
		Size: 2.3 MB (2343677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98623f72442cf00c262363a201209a0aa274f36c3ea6fc9f6982e636f879fa70`  
		Last Modified: Wed, 24 May 2023 23:10:50 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7788f555a977b55dd4bb3cc03f0877839200ef650618e788503063bad30080ce`  
		Last Modified: Wed, 24 May 2023 23:10:50 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874c98264dbb8128fd9c27e97654851dfbde45dfb396778744d7616b44591eae`  
		Last Modified: Wed, 24 May 2023 23:10:50 GMT  
		Size: 6.0 KB (6014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee9de251f061dd4ab29b65e5807e482de72b8f045af577bdc2ade102cedf52d`  
		Last Modified: Wed, 24 May 2023 23:10:50 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:14-postgres-tomcat`

```console
$ docker pull xwiki@sha256:dabd869e53131a2d15143bd5393863a574bacd8268d667ab5f9be188c80b39d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:14-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:ccb7ea5c1410db8b59df0ea0243933bbb5050cf5ed8bc35d3b4702d5928d1482
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.8 MB (589768452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71815ff74c00cebccb5539716f3c3f0391b90709502c0f2f23eae95fd4d9b7f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 07:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 07:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 07:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 07:26:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:27:16 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 04 May 2023 07:27:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 07:27:40 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 16:13:14 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 04 May 2023 16:13:14 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 16:13:14 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 04 May 2023 16:13:14 GMT
WORKDIR /usr/local/tomcat
# Thu, 04 May 2023 16:13:14 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 16:13:15 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 16:14:45 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 04 May 2023 16:14:45 GMT
ENV TOMCAT_MAJOR=9
# Wed, 10 May 2023 18:01:17 GMT
ENV TOMCAT_VERSION=9.0.75
# Wed, 10 May 2023 18:01:17 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Wed, 10 May 2023 18:01:17 GMT
COPY dir:606cc669e6833afa7967597ca36d4a4497efbb54719c008108649021142d7549 in /usr/local/tomcat 
# Wed, 10 May 2023 18:01:21 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 18:01:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 10 May 2023 18:01:23 GMT
EXPOSE 8080
# Wed, 10 May 2023 18:01:23 GMT
CMD ["catalina.sh" "run"]
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 10 May 2023 18:29:15 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Wed, 24 May 2023 22:48:31 GMT
ENV XWIKI_VERSION=14.10.11
# Wed, 24 May 2023 22:48:31 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.11
# Wed, 24 May 2023 22:48:31 GMT
ENV XWIKI_DOWNLOAD_SHA256=0804bdbc2a4eb370a25cfcd9a2185e80e007180007d15fdaa4d371dbd02b5d43
# Wed, 24 May 2023 22:49:09 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 24 May 2023 22:49:11 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Wed, 24 May 2023 22:49:11 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 24 May 2023 22:49:11 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 24 May 2023 22:49:11 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 24 May 2023 22:49:11 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 24 May 2023 22:49:11 GMT
VOLUME [/usr/local/xwiki]
# Wed, 24 May 2023 22:49:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 May 2023 22:49:12 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458b02b5411a07f3b354cde2b461caffc1bb184a3413b5736a9e67ee87cb28b2`  
		Last Modified: Thu, 04 May 2023 07:30:02 GMT  
		Size: 12.5 MB (12504170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04a165ead1d5eabe89dc88e53286af89caab22a5d20c53007b9e6e508affb4b`  
		Last Modified: Thu, 04 May 2023 07:31:19 GMT  
		Size: 46.7 MB (46666270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1187c73b18505bd4495bc03ccbdb723388dfe4d633fd12be845dfe8e253e48e2`  
		Last Modified: Thu, 04 May 2023 07:31:12 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c833cbb14374cde014505e77f6a6122773984a691844e4138fc15cae99ba625`  
		Last Modified: Thu, 04 May 2023 16:24:19 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439ac04571c77c4330db518bc8f35b70f8723246ed34c98787f7ac8d7dc30b42`  
		Last Modified: Wed, 10 May 2023 18:09:06 GMT  
		Size: 12.2 MB (12236613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8e775ba0b76c6692c0b9211e4b94653ba2aa16fdc7a5e3347aba962b684508`  
		Last Modified: Wed, 10 May 2023 18:09:06 GMT  
		Size: 454.2 KB (454222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee5c1ba4848e97d4e3c43d9d4bca0eeeccf2d5d7f6d805d748da4a7d24ad14e`  
		Last Modified: Wed, 10 May 2023 18:09:05 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29abf03d18e0bc34be536fce36ea27d0012a4d330eed44003684563b4d891b2d`  
		Last Modified: Wed, 10 May 2023 18:33:36 GMT  
		Size: 179.3 MB (179276853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:498ed996b7f85205493a73418ae815f35210fc8d8b7b70baa9a06de3e5c233db`  
		Last Modified: Wed, 24 May 2023 22:50:46 GMT  
		Size: 307.3 MB (307250477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:726404a64f919d8c5876da440316ad8fe4a45edd3630ad29f6901546744c11b4`  
		Last Modified: Wed, 24 May 2023 22:50:30 GMT  
		Size: 936.8 KB (936849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84cee4a8e3ec67483536219c5828a467fbc92b808b723cc7fe131aa9d4a6c0ca`  
		Last Modified: Wed, 24 May 2023 22:50:30 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f650315d22dd71a78884aa2fd92ca686e5ce16f9206197580eecb4ecdff2de`  
		Last Modified: Wed, 24 May 2023 22:50:30 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae0aba32059faa0517242b3ddd90818c736c00398d30b55ec885149ac65c2f29`  
		Last Modified: Wed, 24 May 2023 22:50:30 GMT  
		Size: 6.0 KB (6016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9f18e6a2d23412d06f75bdd16e45b58b9e670d8d683b0e55422033d911fc9f1`  
		Last Modified: Wed, 24 May 2023 22:50:30 GMT  
		Size: 2.5 KB (2502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:14-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:80beeb7d3308b8ad1ce8a2ce4e70eb53da61c4632fb10da1448ad9fa7a78d3be
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.0 MB (581049648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ec4529f91042538f49ba29100185d25c41eef43d8163bbb16ad47093be7adbd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 25 Apr 2023 17:31:58 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:31:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:31:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:31:59 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:32:02 GMT
ADD file:aee0d7770ef2f24dc9697e86d391529d001a4013b6e30a3ac90a57932814a57e in / 
# Tue, 25 Apr 2023 17:32:02 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 03:25:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 03:25:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 03:25:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 03:25:23 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 03:25:47 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 04 May 2023 03:26:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 03:26:10 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 11:14:20 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 04 May 2023 11:14:20 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 11:14:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 04 May 2023 11:14:21 GMT
WORKDIR /usr/local/tomcat
# Thu, 04 May 2023 11:14:21 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 11:14:21 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 11:15:34 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 04 May 2023 11:15:34 GMT
ENV TOMCAT_MAJOR=9
# Wed, 10 May 2023 17:56:49 GMT
ENV TOMCAT_VERSION=9.0.75
# Wed, 10 May 2023 17:56:49 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Wed, 10 May 2023 17:56:49 GMT
COPY dir:2a613f9e425d5febc8be5b6c17f49b39f1b8ad84b1601f07f76abed41b25b24b in /usr/local/tomcat 
# Wed, 10 May 2023 17:56:52 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 17:56:54 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 10 May 2023 17:56:54 GMT
EXPOSE 8080
# Wed, 10 May 2023 17:56:54 GMT
CMD ["catalina.sh" "run"]
# Wed, 10 May 2023 18:22:09 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 10 May 2023 18:24:24 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Wed, 24 May 2023 23:09:35 GMT
ENV XWIKI_VERSION=14.10.11
# Wed, 24 May 2023 23:09:35 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.11
# Wed, 24 May 2023 23:09:35 GMT
ENV XWIKI_DOWNLOAD_SHA256=0804bdbc2a4eb370a25cfcd9a2185e80e007180007d15fdaa4d371dbd02b5d43
# Wed, 24 May 2023 23:10:15 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 24 May 2023 23:10:17 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Wed, 24 May 2023 23:10:17 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 24 May 2023 23:10:17 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 24 May 2023 23:10:18 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 24 May 2023 23:10:18 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 24 May 2023 23:10:18 GMT
VOLUME [/usr/local/xwiki]
# Wed, 24 May 2023 23:10:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 May 2023 23:10:18 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f3f60f415e9a03eed88bd5dd5268c841cde08dacf16911a3ef1e4e0fcdd76568`  
		Last Modified: Wed, 26 Apr 2023 02:08:37 GMT  
		Size: 28.4 MB (28389440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fb3595122d1cb6fffe722e2624c3c89b00776b393256a5444af56ceda691cf`  
		Last Modified: Thu, 04 May 2023 03:28:13 GMT  
		Size: 12.5 MB (12463858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5542665e33e692b672a405517e6e267c4c6e210bc410b97a6a1ce732618caa87`  
		Last Modified: Thu, 04 May 2023 03:29:19 GMT  
		Size: 45.0 MB (45009401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e52b8550f0ced98adb0880bd041e361ffb69810e6071e6d71eb2ec0c8ecfad5`  
		Last Modified: Thu, 04 May 2023 03:29:14 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea5566732e0a920d0a63e4fbebf073d2c49e3f80716df462e73f895cc0c5dfa`  
		Last Modified: Thu, 04 May 2023 11:24:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c6d16bf5ef403ef11a1cc9e40650f402cd1f8269d16982f7daebc2a76ab0d9`  
		Last Modified: Wed, 10 May 2023 18:03:56 GMT  
		Size: 12.2 MB (12242222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eaf464f1c82b5f85e3173b2c732f0928a28e669fcc4af9eb6da48199e92ae50`  
		Last Modified: Wed, 10 May 2023 18:03:55 GMT  
		Size: 453.7 KB (453682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ef5f2b94b25f2b0f609c429cc1626d9dd857d8294d2d872d6595bdeff3a5ca`  
		Last Modified: Wed, 10 May 2023 18:03:55 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e76b785cabb7a84968f4d713d3072c255796ddcef576690d954e3fc5b1a09604`  
		Last Modified: Wed, 10 May 2023 18:28:29 GMT  
		Size: 174.3 MB (174290936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ca8b2542757030e2106531ddc6ec3e6dfa6acc493a72d909bb0643df73cf80`  
		Last Modified: Wed, 24 May 2023 23:11:45 GMT  
		Size: 307.3 MB (307250465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97cd250ffbef4fb2fdd174dfb45463c24ac51dfafe9a8660d7a4c5779c36753`  
		Last Modified: Wed, 24 May 2023 23:11:32 GMT  
		Size: 936.9 KB (936854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b1f6e5a8be59e46859d1c9303c24792c97fbcadc1855549404052ed0ed691f`  
		Last Modified: Wed, 24 May 2023 23:11:31 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87f9348f23dfc87a0a5dae7c72f497455e4b3205ef78f38f7e26116fbd5468a7`  
		Last Modified: Wed, 24 May 2023 23:11:31 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ef195c009e7dec60741122ecf4e68a4a11ffefeabf35203eb140ed91090c5c`  
		Last Modified: Wed, 24 May 2023 23:11:31 GMT  
		Size: 6.0 KB (6015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:902e7c9edf86f6fe373bd24ddcdff8ca21d7f599de277b9bcffe4106c4bb5f56`  
		Last Modified: Wed, 24 May 2023 23:11:31 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:14.10`

```console
$ docker pull xwiki@sha256:3cb3e791882b8ad6819d53ac0e7fb6c678ba6435b06061929dca6ce1a98fbef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:14.10` - linux; amd64

```console
$ docker pull xwiki@sha256:8d0ae8c6e385bf7493b07cbab2a2afa371e97538db4f1c040a18c393b5d1e090
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.2 MB (590232292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eff782e5d932a0d40c015b5812ebe948e85c30648a4875e24e6320a36ebb037b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 07:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 07:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 07:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 07:26:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:27:16 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 04 May 2023 07:27:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 07:27:40 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 16:13:14 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 04 May 2023 16:13:14 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 16:13:14 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 04 May 2023 16:13:14 GMT
WORKDIR /usr/local/tomcat
# Thu, 04 May 2023 16:13:14 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 16:13:15 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 16:14:45 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 04 May 2023 16:14:45 GMT
ENV TOMCAT_MAJOR=9
# Wed, 10 May 2023 18:01:17 GMT
ENV TOMCAT_VERSION=9.0.75
# Wed, 10 May 2023 18:01:17 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Wed, 10 May 2023 18:01:17 GMT
COPY dir:606cc669e6833afa7967597ca36d4a4497efbb54719c008108649021142d7549 in /usr/local/tomcat 
# Wed, 10 May 2023 18:01:21 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 18:01:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 10 May 2023 18:01:23 GMT
EXPOSE 8080
# Wed, 10 May 2023 18:01:23 GMT
CMD ["catalina.sh" "run"]
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 10 May 2023 18:28:05 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 24 May 2023 22:47:42 GMT
ENV XWIKI_VERSION=14.10.11
# Wed, 24 May 2023 22:47:42 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.11
# Wed, 24 May 2023 22:47:42 GMT
ENV XWIKI_DOWNLOAD_SHA256=0804bdbc2a4eb370a25cfcd9a2185e80e007180007d15fdaa4d371dbd02b5d43
# Wed, 24 May 2023 22:48:21 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 24 May 2023 22:48:22 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Wed, 24 May 2023 22:48:22 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Wed, 24 May 2023 22:48:22 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Wed, 24 May 2023 22:48:22 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Wed, 24 May 2023 22:48:22 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Wed, 24 May 2023 22:48:23 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Wed, 24 May 2023 22:48:23 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 24 May 2023 22:48:23 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 24 May 2023 22:48:23 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 24 May 2023 22:48:24 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 24 May 2023 22:48:24 GMT
VOLUME [/usr/local/xwiki]
# Wed, 24 May 2023 22:48:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 May 2023 22:48:24 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458b02b5411a07f3b354cde2b461caffc1bb184a3413b5736a9e67ee87cb28b2`  
		Last Modified: Thu, 04 May 2023 07:30:02 GMT  
		Size: 12.5 MB (12504170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04a165ead1d5eabe89dc88e53286af89caab22a5d20c53007b9e6e508affb4b`  
		Last Modified: Thu, 04 May 2023 07:31:19 GMT  
		Size: 46.7 MB (46666270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1187c73b18505bd4495bc03ccbdb723388dfe4d633fd12be845dfe8e253e48e2`  
		Last Modified: Thu, 04 May 2023 07:31:12 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c833cbb14374cde014505e77f6a6122773984a691844e4138fc15cae99ba625`  
		Last Modified: Thu, 04 May 2023 16:24:19 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439ac04571c77c4330db518bc8f35b70f8723246ed34c98787f7ac8d7dc30b42`  
		Last Modified: Wed, 10 May 2023 18:09:06 GMT  
		Size: 12.2 MB (12236613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8e775ba0b76c6692c0b9211e4b94653ba2aa16fdc7a5e3347aba962b684508`  
		Last Modified: Wed, 10 May 2023 18:09:06 GMT  
		Size: 454.2 KB (454222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee5c1ba4848e97d4e3c43d9d4bca0eeeccf2d5d7f6d805d748da4a7d24ad14e`  
		Last Modified: Wed, 10 May 2023 18:09:05 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffadd10be916fc5729676141f5d0ba6aa30968b75555790e449d4988dc81332a`  
		Last Modified: Wed, 10 May 2023 18:32:42 GMT  
		Size: 178.3 MB (178334017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3968819bf3a63424c2b6a4e9591f0c9e6ffbb99a92e0c8d8bb65c67dee37c591`  
		Last Modified: Wed, 24 May 2023 22:50:04 GMT  
		Size: 307.3 MB (307250466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab4c543f2a230baf4ee559f04be553bc00d7b77cc356fee1f21587123cb6977`  
		Last Modified: Wed, 24 May 2023 22:49:49 GMT  
		Size: 2.3 MB (2343680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22684cbd7ece18edde12615b426a6542f278c82ffebfd4d0e88ef0ff8fbde0b`  
		Last Modified: Wed, 24 May 2023 22:49:48 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5270a8761eb66f6e2d094c0879e26935456fa9e19b282bbed9418b58631140c1`  
		Last Modified: Wed, 24 May 2023 22:49:48 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efce4adb2bae1b274febb0d3785c785befb8c4de6c50df158a2aa23673c5b60d`  
		Last Modified: Wed, 24 May 2023 22:49:48 GMT  
		Size: 6.0 KB (6017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9715a623bab854429c5628dcca4718382ada25dbc334b3d61b24a46031cd5d44`  
		Last Modified: Wed, 24 May 2023 22:49:48 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:14.10` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:15957635ec1e31779c981c0817bf66a72c04e6218e1acc75ef471fc7f46dd01c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.5 MB (581515826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aa7648bbd0225e907a6fd992596c1aedb9a12baa3eb30a4a458df9d4af79c91`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 25 Apr 2023 17:31:58 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:31:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:31:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:31:59 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:32:02 GMT
ADD file:aee0d7770ef2f24dc9697e86d391529d001a4013b6e30a3ac90a57932814a57e in / 
# Tue, 25 Apr 2023 17:32:02 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 03:25:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 03:25:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 03:25:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 03:25:23 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 03:25:47 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 04 May 2023 03:26:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 03:26:10 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 11:14:20 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 04 May 2023 11:14:20 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 11:14:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 04 May 2023 11:14:21 GMT
WORKDIR /usr/local/tomcat
# Thu, 04 May 2023 11:14:21 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 11:14:21 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 11:15:34 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 04 May 2023 11:15:34 GMT
ENV TOMCAT_MAJOR=9
# Wed, 10 May 2023 17:56:49 GMT
ENV TOMCAT_VERSION=9.0.75
# Wed, 10 May 2023 17:56:49 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Wed, 10 May 2023 17:56:49 GMT
COPY dir:2a613f9e425d5febc8be5b6c17f49b39f1b8ad84b1601f07f76abed41b25b24b in /usr/local/tomcat 
# Wed, 10 May 2023 17:56:52 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 17:56:54 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 10 May 2023 17:56:54 GMT
EXPOSE 8080
# Wed, 10 May 2023 17:56:54 GMT
CMD ["catalina.sh" "run"]
# Wed, 10 May 2023 18:22:09 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 10 May 2023 18:23:10 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 24 May 2023 23:08:47 GMT
ENV XWIKI_VERSION=14.10.11
# Wed, 24 May 2023 23:08:47 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.11
# Wed, 24 May 2023 23:08:48 GMT
ENV XWIKI_DOWNLOAD_SHA256=0804bdbc2a4eb370a25cfcd9a2185e80e007180007d15fdaa4d371dbd02b5d43
# Wed, 24 May 2023 23:09:27 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 24 May 2023 23:09:29 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Wed, 24 May 2023 23:09:29 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Wed, 24 May 2023 23:09:30 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Wed, 24 May 2023 23:09:30 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Wed, 24 May 2023 23:09:30 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Wed, 24 May 2023 23:09:31 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Wed, 24 May 2023 23:09:31 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 24 May 2023 23:09:31 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 24 May 2023 23:09:31 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 24 May 2023 23:09:31 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 24 May 2023 23:09:32 GMT
VOLUME [/usr/local/xwiki]
# Wed, 24 May 2023 23:09:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 May 2023 23:09:32 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f3f60f415e9a03eed88bd5dd5268c841cde08dacf16911a3ef1e4e0fcdd76568`  
		Last Modified: Wed, 26 Apr 2023 02:08:37 GMT  
		Size: 28.4 MB (28389440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fb3595122d1cb6fffe722e2624c3c89b00776b393256a5444af56ceda691cf`  
		Last Modified: Thu, 04 May 2023 03:28:13 GMT  
		Size: 12.5 MB (12463858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5542665e33e692b672a405517e6e267c4c6e210bc410b97a6a1ce732618caa87`  
		Last Modified: Thu, 04 May 2023 03:29:19 GMT  
		Size: 45.0 MB (45009401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e52b8550f0ced98adb0880bd041e361ffb69810e6071e6d71eb2ec0c8ecfad5`  
		Last Modified: Thu, 04 May 2023 03:29:14 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea5566732e0a920d0a63e4fbebf073d2c49e3f80716df462e73f895cc0c5dfa`  
		Last Modified: Thu, 04 May 2023 11:24:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c6d16bf5ef403ef11a1cc9e40650f402cd1f8269d16982f7daebc2a76ab0d9`  
		Last Modified: Wed, 10 May 2023 18:03:56 GMT  
		Size: 12.2 MB (12242222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eaf464f1c82b5f85e3173b2c732f0928a28e669fcc4af9eb6da48199e92ae50`  
		Last Modified: Wed, 10 May 2023 18:03:55 GMT  
		Size: 453.7 KB (453682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ef5f2b94b25f2b0f609c429cc1626d9dd857d8294d2d872d6595bdeff3a5ca`  
		Last Modified: Wed, 10 May 2023 18:03:55 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7cc67d2dc8f70f6e05051c0e95eb0de93a45de55ba65c355eedaff2bf118e42`  
		Last Modified: Wed, 10 May 2023 18:27:43 GMT  
		Size: 173.4 MB (173350375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0f918d67c923bb6ad20257659a178cf82a52dbd68eda4c094eb3fb372831c2c`  
		Last Modified: Wed, 24 May 2023 23:11:04 GMT  
		Size: 307.3 MB (307250539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced4cf6fb2a03eefd5f5bf442bda27c93928535469b7e8d6fc9c5d7b5ae30b2f`  
		Last Modified: Wed, 24 May 2023 23:10:51 GMT  
		Size: 2.3 MB (2343677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98623f72442cf00c262363a201209a0aa274f36c3ea6fc9f6982e636f879fa70`  
		Last Modified: Wed, 24 May 2023 23:10:50 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7788f555a977b55dd4bb3cc03f0877839200ef650618e788503063bad30080ce`  
		Last Modified: Wed, 24 May 2023 23:10:50 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874c98264dbb8128fd9c27e97654851dfbde45dfb396778744d7616b44591eae`  
		Last Modified: Wed, 24 May 2023 23:10:50 GMT  
		Size: 6.0 KB (6014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee9de251f061dd4ab29b65e5807e482de72b8f045af577bdc2ade102cedf52d`  
		Last Modified: Wed, 24 May 2023 23:10:50 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:14.10-mariadb-tomcat`

```console
$ docker pull xwiki@sha256:c1da5ed330d5ca59735d572da388f3a2ce1fbbaf48e03de0b7d0799d1626c0ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:14.10-mariadb-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:1a75db7f8992a7c4ee2c526aa1a525456625e7a8d132487a30b4db9e5a4d63eb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **588.5 MB (588483181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c4b7b90fa36f2254d9a63b8f50fc26caa9e6bf856d9a1b53f83db9206d899d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 07:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 07:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 07:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 07:26:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:27:16 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 04 May 2023 07:27:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 07:27:40 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 16:13:14 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 04 May 2023 16:13:14 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 16:13:14 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 04 May 2023 16:13:14 GMT
WORKDIR /usr/local/tomcat
# Thu, 04 May 2023 16:13:14 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 16:13:15 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 16:14:45 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 04 May 2023 16:14:45 GMT
ENV TOMCAT_MAJOR=9
# Wed, 10 May 2023 18:01:17 GMT
ENV TOMCAT_VERSION=9.0.75
# Wed, 10 May 2023 18:01:17 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Wed, 10 May 2023 18:01:17 GMT
COPY dir:606cc669e6833afa7967597ca36d4a4497efbb54719c008108649021142d7549 in /usr/local/tomcat 
# Wed, 10 May 2023 18:01:21 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 18:01:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 10 May 2023 18:01:23 GMT
EXPOSE 8080
# Wed, 10 May 2023 18:01:23 GMT
CMD ["catalina.sh" "run"]
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 10 May 2023 18:28:05 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 24 May 2023 22:47:42 GMT
ENV XWIKI_VERSION=14.10.11
# Wed, 24 May 2023 22:47:42 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.11
# Wed, 24 May 2023 22:47:42 GMT
ENV XWIKI_DOWNLOAD_SHA256=0804bdbc2a4eb370a25cfcd9a2185e80e007180007d15fdaa4d371dbd02b5d43
# Wed, 24 May 2023 22:48:21 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 24 May 2023 22:49:20 GMT
ENV MARIADB_JDBC_VERSION=3.1.4
# Wed, 24 May 2023 22:49:20 GMT
ENV MARIADB_JDBC_SHA256=eb88b5d727d82e25117e2b6fabcec1daf734633b0a576456c73215884c189ad4
# Wed, 24 May 2023 22:49:20 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.1.4
# Wed, 24 May 2023 22:49:20 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.1.4.jar
# Wed, 24 May 2023 22:49:20 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.1.4.jar
# Wed, 24 May 2023 22:49:21 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Wed, 24 May 2023 22:49:21 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 24 May 2023 22:49:21 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 24 May 2023 22:49:22 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 24 May 2023 22:49:22 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 24 May 2023 22:49:22 GMT
VOLUME [/usr/local/xwiki]
# Wed, 24 May 2023 22:49:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 May 2023 22:49:22 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458b02b5411a07f3b354cde2b461caffc1bb184a3413b5736a9e67ee87cb28b2`  
		Last Modified: Thu, 04 May 2023 07:30:02 GMT  
		Size: 12.5 MB (12504170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04a165ead1d5eabe89dc88e53286af89caab22a5d20c53007b9e6e508affb4b`  
		Last Modified: Thu, 04 May 2023 07:31:19 GMT  
		Size: 46.7 MB (46666270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1187c73b18505bd4495bc03ccbdb723388dfe4d633fd12be845dfe8e253e48e2`  
		Last Modified: Thu, 04 May 2023 07:31:12 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c833cbb14374cde014505e77f6a6122773984a691844e4138fc15cae99ba625`  
		Last Modified: Thu, 04 May 2023 16:24:19 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439ac04571c77c4330db518bc8f35b70f8723246ed34c98787f7ac8d7dc30b42`  
		Last Modified: Wed, 10 May 2023 18:09:06 GMT  
		Size: 12.2 MB (12236613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8e775ba0b76c6692c0b9211e4b94653ba2aa16fdc7a5e3347aba962b684508`  
		Last Modified: Wed, 10 May 2023 18:09:06 GMT  
		Size: 454.2 KB (454222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee5c1ba4848e97d4e3c43d9d4bca0eeeccf2d5d7f6d805d748da4a7d24ad14e`  
		Last Modified: Wed, 10 May 2023 18:09:05 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffadd10be916fc5729676141f5d0ba6aa30968b75555790e449d4988dc81332a`  
		Last Modified: Wed, 10 May 2023 18:32:42 GMT  
		Size: 178.3 MB (178334017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3968819bf3a63424c2b6a4e9591f0c9e6ffbb99a92e0c8d8bb65c67dee37c591`  
		Last Modified: Wed, 24 May 2023 22:50:04 GMT  
		Size: 307.3 MB (307250466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe65a2b1c269931f9affdbf4926be3a7e6789a0eb5ef5c8469c0ab01708aa54e`  
		Last Modified: Wed, 24 May 2023 22:51:02 GMT  
		Size: 594.6 KB (594559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b1b0dad9556a98d3e225960bc3fdd9550ee0d50cc15b4667535a69cc8cc4f5`  
		Last Modified: Wed, 24 May 2023 22:51:02 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b44a0baefcddcca335cf3e635a10b22f472dcb576dfa3b75755f9db5fc9ec853`  
		Last Modified: Wed, 24 May 2023 22:51:02 GMT  
		Size: 2.3 KB (2313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ebfb8ffc93a8da62fdc799b946b53ae557f1061d920db81d002a7fea3bacbde`  
		Last Modified: Wed, 24 May 2023 22:51:02 GMT  
		Size: 6.0 KB (6019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f48b704e13efa0bd740446998f3193c87fcb7dadc14138af9f9103fdbdcdc87`  
		Last Modified: Wed, 24 May 2023 22:51:02 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:14.10-mariadb-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:00f5266daef25dc10485eca8533381e175b534a692a79b5e108b3563b604c1a5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.8 MB (579766697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e448e5a8cc6e1fb57ca6ebb008b4fa70de9683b31e4f558bd222f5a5fd0b441f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 25 Apr 2023 17:31:58 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:31:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:31:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:31:59 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:32:02 GMT
ADD file:aee0d7770ef2f24dc9697e86d391529d001a4013b6e30a3ac90a57932814a57e in / 
# Tue, 25 Apr 2023 17:32:02 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 03:25:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 03:25:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 03:25:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 03:25:23 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 03:25:47 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 04 May 2023 03:26:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 03:26:10 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 11:14:20 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 04 May 2023 11:14:20 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 11:14:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 04 May 2023 11:14:21 GMT
WORKDIR /usr/local/tomcat
# Thu, 04 May 2023 11:14:21 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 11:14:21 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 11:15:34 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 04 May 2023 11:15:34 GMT
ENV TOMCAT_MAJOR=9
# Wed, 10 May 2023 17:56:49 GMT
ENV TOMCAT_VERSION=9.0.75
# Wed, 10 May 2023 17:56:49 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Wed, 10 May 2023 17:56:49 GMT
COPY dir:2a613f9e425d5febc8be5b6c17f49b39f1b8ad84b1601f07f76abed41b25b24b in /usr/local/tomcat 
# Wed, 10 May 2023 17:56:52 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 17:56:54 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 10 May 2023 17:56:54 GMT
EXPOSE 8080
# Wed, 10 May 2023 17:56:54 GMT
CMD ["catalina.sh" "run"]
# Wed, 10 May 2023 18:22:09 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 10 May 2023 18:23:10 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 24 May 2023 23:08:47 GMT
ENV XWIKI_VERSION=14.10.11
# Wed, 24 May 2023 23:08:47 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.11
# Wed, 24 May 2023 23:08:48 GMT
ENV XWIKI_DOWNLOAD_SHA256=0804bdbc2a4eb370a25cfcd9a2185e80e007180007d15fdaa4d371dbd02b5d43
# Wed, 24 May 2023 23:09:27 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 24 May 2023 23:10:23 GMT
ENV MARIADB_JDBC_VERSION=3.1.4
# Wed, 24 May 2023 23:10:23 GMT
ENV MARIADB_JDBC_SHA256=eb88b5d727d82e25117e2b6fabcec1daf734633b0a576456c73215884c189ad4
# Wed, 24 May 2023 23:10:23 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.1.4
# Wed, 24 May 2023 23:10:23 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.1.4.jar
# Wed, 24 May 2023 23:10:23 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.1.4.jar
# Wed, 24 May 2023 23:10:24 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Wed, 24 May 2023 23:10:24 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 24 May 2023 23:10:24 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 24 May 2023 23:10:25 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 24 May 2023 23:10:25 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 24 May 2023 23:10:25 GMT
VOLUME [/usr/local/xwiki]
# Wed, 24 May 2023 23:10:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 May 2023 23:10:25 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f3f60f415e9a03eed88bd5dd5268c841cde08dacf16911a3ef1e4e0fcdd76568`  
		Last Modified: Wed, 26 Apr 2023 02:08:37 GMT  
		Size: 28.4 MB (28389440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fb3595122d1cb6fffe722e2624c3c89b00776b393256a5444af56ceda691cf`  
		Last Modified: Thu, 04 May 2023 03:28:13 GMT  
		Size: 12.5 MB (12463858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5542665e33e692b672a405517e6e267c4c6e210bc410b97a6a1ce732618caa87`  
		Last Modified: Thu, 04 May 2023 03:29:19 GMT  
		Size: 45.0 MB (45009401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e52b8550f0ced98adb0880bd041e361ffb69810e6071e6d71eb2ec0c8ecfad5`  
		Last Modified: Thu, 04 May 2023 03:29:14 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea5566732e0a920d0a63e4fbebf073d2c49e3f80716df462e73f895cc0c5dfa`  
		Last Modified: Thu, 04 May 2023 11:24:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c6d16bf5ef403ef11a1cc9e40650f402cd1f8269d16982f7daebc2a76ab0d9`  
		Last Modified: Wed, 10 May 2023 18:03:56 GMT  
		Size: 12.2 MB (12242222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eaf464f1c82b5f85e3173b2c732f0928a28e669fcc4af9eb6da48199e92ae50`  
		Last Modified: Wed, 10 May 2023 18:03:55 GMT  
		Size: 453.7 KB (453682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ef5f2b94b25f2b0f609c429cc1626d9dd857d8294d2d872d6595bdeff3a5ca`  
		Last Modified: Wed, 10 May 2023 18:03:55 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7cc67d2dc8f70f6e05051c0e95eb0de93a45de55ba65c355eedaff2bf118e42`  
		Last Modified: Wed, 10 May 2023 18:27:43 GMT  
		Size: 173.4 MB (173350375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0f918d67c923bb6ad20257659a178cf82a52dbd68eda4c094eb3fb372831c2c`  
		Last Modified: Wed, 24 May 2023 23:11:04 GMT  
		Size: 307.3 MB (307250539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d912a3a12e11af60d952ffa7ac5359c7aa515a7300f75c5ba871ea94e62bd43`  
		Last Modified: Wed, 24 May 2023 23:12:02 GMT  
		Size: 594.5 KB (594549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f871b4dce32a1e7dcce9033dac703bc174253e8b26f41ea7a7d4c4ae1d98372f`  
		Last Modified: Wed, 24 May 2023 23:12:02 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f1d5bccd3396b98e1cf536def6525a295c0a35c6c70a438fc6a917b322efd5f`  
		Last Modified: Wed, 24 May 2023 23:12:02 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b11946e15dcff3a5243af68d7416f684d866731eedb590452d184678df469e`  
		Last Modified: Wed, 24 May 2023 23:12:02 GMT  
		Size: 6.0 KB (6013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33aa2a2a6531b6d4ff0f2638634bbb0a42a3796e25d026234551deb2add3b637`  
		Last Modified: Wed, 24 May 2023 23:12:02 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:14.10-mysql-tomcat`

```console
$ docker pull xwiki@sha256:3cb3e791882b8ad6819d53ac0e7fb6c678ba6435b06061929dca6ce1a98fbef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:14.10-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:8d0ae8c6e385bf7493b07cbab2a2afa371e97538db4f1c040a18c393b5d1e090
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.2 MB (590232292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eff782e5d932a0d40c015b5812ebe948e85c30648a4875e24e6320a36ebb037b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 07:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 07:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 07:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 07:26:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:27:16 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 04 May 2023 07:27:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 07:27:40 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 16:13:14 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 04 May 2023 16:13:14 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 16:13:14 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 04 May 2023 16:13:14 GMT
WORKDIR /usr/local/tomcat
# Thu, 04 May 2023 16:13:14 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 16:13:15 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 16:14:45 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 04 May 2023 16:14:45 GMT
ENV TOMCAT_MAJOR=9
# Wed, 10 May 2023 18:01:17 GMT
ENV TOMCAT_VERSION=9.0.75
# Wed, 10 May 2023 18:01:17 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Wed, 10 May 2023 18:01:17 GMT
COPY dir:606cc669e6833afa7967597ca36d4a4497efbb54719c008108649021142d7549 in /usr/local/tomcat 
# Wed, 10 May 2023 18:01:21 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 18:01:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 10 May 2023 18:01:23 GMT
EXPOSE 8080
# Wed, 10 May 2023 18:01:23 GMT
CMD ["catalina.sh" "run"]
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 10 May 2023 18:28:05 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 24 May 2023 22:47:42 GMT
ENV XWIKI_VERSION=14.10.11
# Wed, 24 May 2023 22:47:42 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.11
# Wed, 24 May 2023 22:47:42 GMT
ENV XWIKI_DOWNLOAD_SHA256=0804bdbc2a4eb370a25cfcd9a2185e80e007180007d15fdaa4d371dbd02b5d43
# Wed, 24 May 2023 22:48:21 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 24 May 2023 22:48:22 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Wed, 24 May 2023 22:48:22 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Wed, 24 May 2023 22:48:22 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Wed, 24 May 2023 22:48:22 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Wed, 24 May 2023 22:48:22 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Wed, 24 May 2023 22:48:23 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Wed, 24 May 2023 22:48:23 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 24 May 2023 22:48:23 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 24 May 2023 22:48:23 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 24 May 2023 22:48:24 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 24 May 2023 22:48:24 GMT
VOLUME [/usr/local/xwiki]
# Wed, 24 May 2023 22:48:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 May 2023 22:48:24 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458b02b5411a07f3b354cde2b461caffc1bb184a3413b5736a9e67ee87cb28b2`  
		Last Modified: Thu, 04 May 2023 07:30:02 GMT  
		Size: 12.5 MB (12504170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04a165ead1d5eabe89dc88e53286af89caab22a5d20c53007b9e6e508affb4b`  
		Last Modified: Thu, 04 May 2023 07:31:19 GMT  
		Size: 46.7 MB (46666270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1187c73b18505bd4495bc03ccbdb723388dfe4d633fd12be845dfe8e253e48e2`  
		Last Modified: Thu, 04 May 2023 07:31:12 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c833cbb14374cde014505e77f6a6122773984a691844e4138fc15cae99ba625`  
		Last Modified: Thu, 04 May 2023 16:24:19 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439ac04571c77c4330db518bc8f35b70f8723246ed34c98787f7ac8d7dc30b42`  
		Last Modified: Wed, 10 May 2023 18:09:06 GMT  
		Size: 12.2 MB (12236613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8e775ba0b76c6692c0b9211e4b94653ba2aa16fdc7a5e3347aba962b684508`  
		Last Modified: Wed, 10 May 2023 18:09:06 GMT  
		Size: 454.2 KB (454222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee5c1ba4848e97d4e3c43d9d4bca0eeeccf2d5d7f6d805d748da4a7d24ad14e`  
		Last Modified: Wed, 10 May 2023 18:09:05 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffadd10be916fc5729676141f5d0ba6aa30968b75555790e449d4988dc81332a`  
		Last Modified: Wed, 10 May 2023 18:32:42 GMT  
		Size: 178.3 MB (178334017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3968819bf3a63424c2b6a4e9591f0c9e6ffbb99a92e0c8d8bb65c67dee37c591`  
		Last Modified: Wed, 24 May 2023 22:50:04 GMT  
		Size: 307.3 MB (307250466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab4c543f2a230baf4ee559f04be553bc00d7b77cc356fee1f21587123cb6977`  
		Last Modified: Wed, 24 May 2023 22:49:49 GMT  
		Size: 2.3 MB (2343680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22684cbd7ece18edde12615b426a6542f278c82ffebfd4d0e88ef0ff8fbde0b`  
		Last Modified: Wed, 24 May 2023 22:49:48 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5270a8761eb66f6e2d094c0879e26935456fa9e19b282bbed9418b58631140c1`  
		Last Modified: Wed, 24 May 2023 22:49:48 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efce4adb2bae1b274febb0d3785c785befb8c4de6c50df158a2aa23673c5b60d`  
		Last Modified: Wed, 24 May 2023 22:49:48 GMT  
		Size: 6.0 KB (6017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9715a623bab854429c5628dcca4718382ada25dbc334b3d61b24a46031cd5d44`  
		Last Modified: Wed, 24 May 2023 22:49:48 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:14.10-mysql-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:15957635ec1e31779c981c0817bf66a72c04e6218e1acc75ef471fc7f46dd01c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.5 MB (581515826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aa7648bbd0225e907a6fd992596c1aedb9a12baa3eb30a4a458df9d4af79c91`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 25 Apr 2023 17:31:58 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:31:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:31:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:31:59 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:32:02 GMT
ADD file:aee0d7770ef2f24dc9697e86d391529d001a4013b6e30a3ac90a57932814a57e in / 
# Tue, 25 Apr 2023 17:32:02 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 03:25:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 03:25:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 03:25:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 03:25:23 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 03:25:47 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 04 May 2023 03:26:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 03:26:10 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 11:14:20 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 04 May 2023 11:14:20 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 11:14:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 04 May 2023 11:14:21 GMT
WORKDIR /usr/local/tomcat
# Thu, 04 May 2023 11:14:21 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 11:14:21 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 11:15:34 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 04 May 2023 11:15:34 GMT
ENV TOMCAT_MAJOR=9
# Wed, 10 May 2023 17:56:49 GMT
ENV TOMCAT_VERSION=9.0.75
# Wed, 10 May 2023 17:56:49 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Wed, 10 May 2023 17:56:49 GMT
COPY dir:2a613f9e425d5febc8be5b6c17f49b39f1b8ad84b1601f07f76abed41b25b24b in /usr/local/tomcat 
# Wed, 10 May 2023 17:56:52 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 17:56:54 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 10 May 2023 17:56:54 GMT
EXPOSE 8080
# Wed, 10 May 2023 17:56:54 GMT
CMD ["catalina.sh" "run"]
# Wed, 10 May 2023 18:22:09 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 10 May 2023 18:23:10 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 24 May 2023 23:08:47 GMT
ENV XWIKI_VERSION=14.10.11
# Wed, 24 May 2023 23:08:47 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.11
# Wed, 24 May 2023 23:08:48 GMT
ENV XWIKI_DOWNLOAD_SHA256=0804bdbc2a4eb370a25cfcd9a2185e80e007180007d15fdaa4d371dbd02b5d43
# Wed, 24 May 2023 23:09:27 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 24 May 2023 23:09:29 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Wed, 24 May 2023 23:09:29 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Wed, 24 May 2023 23:09:30 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Wed, 24 May 2023 23:09:30 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Wed, 24 May 2023 23:09:30 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Wed, 24 May 2023 23:09:31 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Wed, 24 May 2023 23:09:31 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 24 May 2023 23:09:31 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 24 May 2023 23:09:31 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 24 May 2023 23:09:31 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 24 May 2023 23:09:32 GMT
VOLUME [/usr/local/xwiki]
# Wed, 24 May 2023 23:09:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 May 2023 23:09:32 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f3f60f415e9a03eed88bd5dd5268c841cde08dacf16911a3ef1e4e0fcdd76568`  
		Last Modified: Wed, 26 Apr 2023 02:08:37 GMT  
		Size: 28.4 MB (28389440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fb3595122d1cb6fffe722e2624c3c89b00776b393256a5444af56ceda691cf`  
		Last Modified: Thu, 04 May 2023 03:28:13 GMT  
		Size: 12.5 MB (12463858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5542665e33e692b672a405517e6e267c4c6e210bc410b97a6a1ce732618caa87`  
		Last Modified: Thu, 04 May 2023 03:29:19 GMT  
		Size: 45.0 MB (45009401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e52b8550f0ced98adb0880bd041e361ffb69810e6071e6d71eb2ec0c8ecfad5`  
		Last Modified: Thu, 04 May 2023 03:29:14 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea5566732e0a920d0a63e4fbebf073d2c49e3f80716df462e73f895cc0c5dfa`  
		Last Modified: Thu, 04 May 2023 11:24:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c6d16bf5ef403ef11a1cc9e40650f402cd1f8269d16982f7daebc2a76ab0d9`  
		Last Modified: Wed, 10 May 2023 18:03:56 GMT  
		Size: 12.2 MB (12242222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eaf464f1c82b5f85e3173b2c732f0928a28e669fcc4af9eb6da48199e92ae50`  
		Last Modified: Wed, 10 May 2023 18:03:55 GMT  
		Size: 453.7 KB (453682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ef5f2b94b25f2b0f609c429cc1626d9dd857d8294d2d872d6595bdeff3a5ca`  
		Last Modified: Wed, 10 May 2023 18:03:55 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7cc67d2dc8f70f6e05051c0e95eb0de93a45de55ba65c355eedaff2bf118e42`  
		Last Modified: Wed, 10 May 2023 18:27:43 GMT  
		Size: 173.4 MB (173350375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0f918d67c923bb6ad20257659a178cf82a52dbd68eda4c094eb3fb372831c2c`  
		Last Modified: Wed, 24 May 2023 23:11:04 GMT  
		Size: 307.3 MB (307250539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced4cf6fb2a03eefd5f5bf442bda27c93928535469b7e8d6fc9c5d7b5ae30b2f`  
		Last Modified: Wed, 24 May 2023 23:10:51 GMT  
		Size: 2.3 MB (2343677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98623f72442cf00c262363a201209a0aa274f36c3ea6fc9f6982e636f879fa70`  
		Last Modified: Wed, 24 May 2023 23:10:50 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7788f555a977b55dd4bb3cc03f0877839200ef650618e788503063bad30080ce`  
		Last Modified: Wed, 24 May 2023 23:10:50 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874c98264dbb8128fd9c27e97654851dfbde45dfb396778744d7616b44591eae`  
		Last Modified: Wed, 24 May 2023 23:10:50 GMT  
		Size: 6.0 KB (6014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee9de251f061dd4ab29b65e5807e482de72b8f045af577bdc2ade102cedf52d`  
		Last Modified: Wed, 24 May 2023 23:10:50 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:14.10-postgres-tomcat`

```console
$ docker pull xwiki@sha256:dabd869e53131a2d15143bd5393863a574bacd8268d667ab5f9be188c80b39d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:14.10-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:ccb7ea5c1410db8b59df0ea0243933bbb5050cf5ed8bc35d3b4702d5928d1482
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.8 MB (589768452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71815ff74c00cebccb5539716f3c3f0391b90709502c0f2f23eae95fd4d9b7f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 07:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 07:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 07:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 07:26:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:27:16 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 04 May 2023 07:27:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 07:27:40 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 16:13:14 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 04 May 2023 16:13:14 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 16:13:14 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 04 May 2023 16:13:14 GMT
WORKDIR /usr/local/tomcat
# Thu, 04 May 2023 16:13:14 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 16:13:15 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 16:14:45 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 04 May 2023 16:14:45 GMT
ENV TOMCAT_MAJOR=9
# Wed, 10 May 2023 18:01:17 GMT
ENV TOMCAT_VERSION=9.0.75
# Wed, 10 May 2023 18:01:17 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Wed, 10 May 2023 18:01:17 GMT
COPY dir:606cc669e6833afa7967597ca36d4a4497efbb54719c008108649021142d7549 in /usr/local/tomcat 
# Wed, 10 May 2023 18:01:21 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 18:01:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 10 May 2023 18:01:23 GMT
EXPOSE 8080
# Wed, 10 May 2023 18:01:23 GMT
CMD ["catalina.sh" "run"]
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 10 May 2023 18:29:15 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Wed, 24 May 2023 22:48:31 GMT
ENV XWIKI_VERSION=14.10.11
# Wed, 24 May 2023 22:48:31 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.11
# Wed, 24 May 2023 22:48:31 GMT
ENV XWIKI_DOWNLOAD_SHA256=0804bdbc2a4eb370a25cfcd9a2185e80e007180007d15fdaa4d371dbd02b5d43
# Wed, 24 May 2023 22:49:09 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 24 May 2023 22:49:11 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Wed, 24 May 2023 22:49:11 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 24 May 2023 22:49:11 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 24 May 2023 22:49:11 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 24 May 2023 22:49:11 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 24 May 2023 22:49:11 GMT
VOLUME [/usr/local/xwiki]
# Wed, 24 May 2023 22:49:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 May 2023 22:49:12 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458b02b5411a07f3b354cde2b461caffc1bb184a3413b5736a9e67ee87cb28b2`  
		Last Modified: Thu, 04 May 2023 07:30:02 GMT  
		Size: 12.5 MB (12504170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04a165ead1d5eabe89dc88e53286af89caab22a5d20c53007b9e6e508affb4b`  
		Last Modified: Thu, 04 May 2023 07:31:19 GMT  
		Size: 46.7 MB (46666270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1187c73b18505bd4495bc03ccbdb723388dfe4d633fd12be845dfe8e253e48e2`  
		Last Modified: Thu, 04 May 2023 07:31:12 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c833cbb14374cde014505e77f6a6122773984a691844e4138fc15cae99ba625`  
		Last Modified: Thu, 04 May 2023 16:24:19 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439ac04571c77c4330db518bc8f35b70f8723246ed34c98787f7ac8d7dc30b42`  
		Last Modified: Wed, 10 May 2023 18:09:06 GMT  
		Size: 12.2 MB (12236613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8e775ba0b76c6692c0b9211e4b94653ba2aa16fdc7a5e3347aba962b684508`  
		Last Modified: Wed, 10 May 2023 18:09:06 GMT  
		Size: 454.2 KB (454222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee5c1ba4848e97d4e3c43d9d4bca0eeeccf2d5d7f6d805d748da4a7d24ad14e`  
		Last Modified: Wed, 10 May 2023 18:09:05 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29abf03d18e0bc34be536fce36ea27d0012a4d330eed44003684563b4d891b2d`  
		Last Modified: Wed, 10 May 2023 18:33:36 GMT  
		Size: 179.3 MB (179276853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:498ed996b7f85205493a73418ae815f35210fc8d8b7b70baa9a06de3e5c233db`  
		Last Modified: Wed, 24 May 2023 22:50:46 GMT  
		Size: 307.3 MB (307250477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:726404a64f919d8c5876da440316ad8fe4a45edd3630ad29f6901546744c11b4`  
		Last Modified: Wed, 24 May 2023 22:50:30 GMT  
		Size: 936.8 KB (936849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84cee4a8e3ec67483536219c5828a467fbc92b808b723cc7fe131aa9d4a6c0ca`  
		Last Modified: Wed, 24 May 2023 22:50:30 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f650315d22dd71a78884aa2fd92ca686e5ce16f9206197580eecb4ecdff2de`  
		Last Modified: Wed, 24 May 2023 22:50:30 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae0aba32059faa0517242b3ddd90818c736c00398d30b55ec885149ac65c2f29`  
		Last Modified: Wed, 24 May 2023 22:50:30 GMT  
		Size: 6.0 KB (6016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9f18e6a2d23412d06f75bdd16e45b58b9e670d8d683b0e55422033d911fc9f1`  
		Last Modified: Wed, 24 May 2023 22:50:30 GMT  
		Size: 2.5 KB (2502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:14.10-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:80beeb7d3308b8ad1ce8a2ce4e70eb53da61c4632fb10da1448ad9fa7a78d3be
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.0 MB (581049648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ec4529f91042538f49ba29100185d25c41eef43d8163bbb16ad47093be7adbd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 25 Apr 2023 17:31:58 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:31:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:31:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:31:59 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:32:02 GMT
ADD file:aee0d7770ef2f24dc9697e86d391529d001a4013b6e30a3ac90a57932814a57e in / 
# Tue, 25 Apr 2023 17:32:02 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 03:25:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 03:25:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 03:25:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 03:25:23 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 03:25:47 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 04 May 2023 03:26:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 03:26:10 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 11:14:20 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 04 May 2023 11:14:20 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 11:14:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 04 May 2023 11:14:21 GMT
WORKDIR /usr/local/tomcat
# Thu, 04 May 2023 11:14:21 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 11:14:21 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 11:15:34 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 04 May 2023 11:15:34 GMT
ENV TOMCAT_MAJOR=9
# Wed, 10 May 2023 17:56:49 GMT
ENV TOMCAT_VERSION=9.0.75
# Wed, 10 May 2023 17:56:49 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Wed, 10 May 2023 17:56:49 GMT
COPY dir:2a613f9e425d5febc8be5b6c17f49b39f1b8ad84b1601f07f76abed41b25b24b in /usr/local/tomcat 
# Wed, 10 May 2023 17:56:52 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 17:56:54 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 10 May 2023 17:56:54 GMT
EXPOSE 8080
# Wed, 10 May 2023 17:56:54 GMT
CMD ["catalina.sh" "run"]
# Wed, 10 May 2023 18:22:09 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 10 May 2023 18:24:24 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Wed, 24 May 2023 23:09:35 GMT
ENV XWIKI_VERSION=14.10.11
# Wed, 24 May 2023 23:09:35 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.11
# Wed, 24 May 2023 23:09:35 GMT
ENV XWIKI_DOWNLOAD_SHA256=0804bdbc2a4eb370a25cfcd9a2185e80e007180007d15fdaa4d371dbd02b5d43
# Wed, 24 May 2023 23:10:15 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 24 May 2023 23:10:17 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Wed, 24 May 2023 23:10:17 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 24 May 2023 23:10:17 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 24 May 2023 23:10:18 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 24 May 2023 23:10:18 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 24 May 2023 23:10:18 GMT
VOLUME [/usr/local/xwiki]
# Wed, 24 May 2023 23:10:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 May 2023 23:10:18 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f3f60f415e9a03eed88bd5dd5268c841cde08dacf16911a3ef1e4e0fcdd76568`  
		Last Modified: Wed, 26 Apr 2023 02:08:37 GMT  
		Size: 28.4 MB (28389440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fb3595122d1cb6fffe722e2624c3c89b00776b393256a5444af56ceda691cf`  
		Last Modified: Thu, 04 May 2023 03:28:13 GMT  
		Size: 12.5 MB (12463858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5542665e33e692b672a405517e6e267c4c6e210bc410b97a6a1ce732618caa87`  
		Last Modified: Thu, 04 May 2023 03:29:19 GMT  
		Size: 45.0 MB (45009401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e52b8550f0ced98adb0880bd041e361ffb69810e6071e6d71eb2ec0c8ecfad5`  
		Last Modified: Thu, 04 May 2023 03:29:14 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea5566732e0a920d0a63e4fbebf073d2c49e3f80716df462e73f895cc0c5dfa`  
		Last Modified: Thu, 04 May 2023 11:24:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c6d16bf5ef403ef11a1cc9e40650f402cd1f8269d16982f7daebc2a76ab0d9`  
		Last Modified: Wed, 10 May 2023 18:03:56 GMT  
		Size: 12.2 MB (12242222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eaf464f1c82b5f85e3173b2c732f0928a28e669fcc4af9eb6da48199e92ae50`  
		Last Modified: Wed, 10 May 2023 18:03:55 GMT  
		Size: 453.7 KB (453682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ef5f2b94b25f2b0f609c429cc1626d9dd857d8294d2d872d6595bdeff3a5ca`  
		Last Modified: Wed, 10 May 2023 18:03:55 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e76b785cabb7a84968f4d713d3072c255796ddcef576690d954e3fc5b1a09604`  
		Last Modified: Wed, 10 May 2023 18:28:29 GMT  
		Size: 174.3 MB (174290936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ca8b2542757030e2106531ddc6ec3e6dfa6acc493a72d909bb0643df73cf80`  
		Last Modified: Wed, 24 May 2023 23:11:45 GMT  
		Size: 307.3 MB (307250465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97cd250ffbef4fb2fdd174dfb45463c24ac51dfafe9a8660d7a4c5779c36753`  
		Last Modified: Wed, 24 May 2023 23:11:32 GMT  
		Size: 936.9 KB (936854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b1f6e5a8be59e46859d1c9303c24792c97fbcadc1855549404052ed0ed691f`  
		Last Modified: Wed, 24 May 2023 23:11:31 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87f9348f23dfc87a0a5dae7c72f497455e4b3205ef78f38f7e26116fbd5468a7`  
		Last Modified: Wed, 24 May 2023 23:11:31 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ef195c009e7dec60741122ecf4e68a4a11ffefeabf35203eb140ed91090c5c`  
		Last Modified: Wed, 24 May 2023 23:11:31 GMT  
		Size: 6.0 KB (6015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:902e7c9edf86f6fe373bd24ddcdff8ca21d7f599de277b9bcffe4106c4bb5f56`  
		Last Modified: Wed, 24 May 2023 23:11:31 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:14.10.11`

```console
$ docker pull xwiki@sha256:3cb3e791882b8ad6819d53ac0e7fb6c678ba6435b06061929dca6ce1a98fbef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:14.10.11` - linux; amd64

```console
$ docker pull xwiki@sha256:8d0ae8c6e385bf7493b07cbab2a2afa371e97538db4f1c040a18c393b5d1e090
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.2 MB (590232292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eff782e5d932a0d40c015b5812ebe948e85c30648a4875e24e6320a36ebb037b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 07:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 07:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 07:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 07:26:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:27:16 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 04 May 2023 07:27:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 07:27:40 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 16:13:14 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 04 May 2023 16:13:14 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 16:13:14 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 04 May 2023 16:13:14 GMT
WORKDIR /usr/local/tomcat
# Thu, 04 May 2023 16:13:14 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 16:13:15 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 16:14:45 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 04 May 2023 16:14:45 GMT
ENV TOMCAT_MAJOR=9
# Wed, 10 May 2023 18:01:17 GMT
ENV TOMCAT_VERSION=9.0.75
# Wed, 10 May 2023 18:01:17 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Wed, 10 May 2023 18:01:17 GMT
COPY dir:606cc669e6833afa7967597ca36d4a4497efbb54719c008108649021142d7549 in /usr/local/tomcat 
# Wed, 10 May 2023 18:01:21 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 18:01:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 10 May 2023 18:01:23 GMT
EXPOSE 8080
# Wed, 10 May 2023 18:01:23 GMT
CMD ["catalina.sh" "run"]
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 10 May 2023 18:28:05 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 24 May 2023 22:47:42 GMT
ENV XWIKI_VERSION=14.10.11
# Wed, 24 May 2023 22:47:42 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.11
# Wed, 24 May 2023 22:47:42 GMT
ENV XWIKI_DOWNLOAD_SHA256=0804bdbc2a4eb370a25cfcd9a2185e80e007180007d15fdaa4d371dbd02b5d43
# Wed, 24 May 2023 22:48:21 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 24 May 2023 22:48:22 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Wed, 24 May 2023 22:48:22 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Wed, 24 May 2023 22:48:22 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Wed, 24 May 2023 22:48:22 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Wed, 24 May 2023 22:48:22 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Wed, 24 May 2023 22:48:23 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Wed, 24 May 2023 22:48:23 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 24 May 2023 22:48:23 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 24 May 2023 22:48:23 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 24 May 2023 22:48:24 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 24 May 2023 22:48:24 GMT
VOLUME [/usr/local/xwiki]
# Wed, 24 May 2023 22:48:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 May 2023 22:48:24 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458b02b5411a07f3b354cde2b461caffc1bb184a3413b5736a9e67ee87cb28b2`  
		Last Modified: Thu, 04 May 2023 07:30:02 GMT  
		Size: 12.5 MB (12504170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04a165ead1d5eabe89dc88e53286af89caab22a5d20c53007b9e6e508affb4b`  
		Last Modified: Thu, 04 May 2023 07:31:19 GMT  
		Size: 46.7 MB (46666270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1187c73b18505bd4495bc03ccbdb723388dfe4d633fd12be845dfe8e253e48e2`  
		Last Modified: Thu, 04 May 2023 07:31:12 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c833cbb14374cde014505e77f6a6122773984a691844e4138fc15cae99ba625`  
		Last Modified: Thu, 04 May 2023 16:24:19 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439ac04571c77c4330db518bc8f35b70f8723246ed34c98787f7ac8d7dc30b42`  
		Last Modified: Wed, 10 May 2023 18:09:06 GMT  
		Size: 12.2 MB (12236613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8e775ba0b76c6692c0b9211e4b94653ba2aa16fdc7a5e3347aba962b684508`  
		Last Modified: Wed, 10 May 2023 18:09:06 GMT  
		Size: 454.2 KB (454222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee5c1ba4848e97d4e3c43d9d4bca0eeeccf2d5d7f6d805d748da4a7d24ad14e`  
		Last Modified: Wed, 10 May 2023 18:09:05 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffadd10be916fc5729676141f5d0ba6aa30968b75555790e449d4988dc81332a`  
		Last Modified: Wed, 10 May 2023 18:32:42 GMT  
		Size: 178.3 MB (178334017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3968819bf3a63424c2b6a4e9591f0c9e6ffbb99a92e0c8d8bb65c67dee37c591`  
		Last Modified: Wed, 24 May 2023 22:50:04 GMT  
		Size: 307.3 MB (307250466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab4c543f2a230baf4ee559f04be553bc00d7b77cc356fee1f21587123cb6977`  
		Last Modified: Wed, 24 May 2023 22:49:49 GMT  
		Size: 2.3 MB (2343680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22684cbd7ece18edde12615b426a6542f278c82ffebfd4d0e88ef0ff8fbde0b`  
		Last Modified: Wed, 24 May 2023 22:49:48 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5270a8761eb66f6e2d094c0879e26935456fa9e19b282bbed9418b58631140c1`  
		Last Modified: Wed, 24 May 2023 22:49:48 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efce4adb2bae1b274febb0d3785c785befb8c4de6c50df158a2aa23673c5b60d`  
		Last Modified: Wed, 24 May 2023 22:49:48 GMT  
		Size: 6.0 KB (6017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9715a623bab854429c5628dcca4718382ada25dbc334b3d61b24a46031cd5d44`  
		Last Modified: Wed, 24 May 2023 22:49:48 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:14.10.11` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:15957635ec1e31779c981c0817bf66a72c04e6218e1acc75ef471fc7f46dd01c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.5 MB (581515826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aa7648bbd0225e907a6fd992596c1aedb9a12baa3eb30a4a458df9d4af79c91`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 25 Apr 2023 17:31:58 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:31:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:31:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:31:59 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:32:02 GMT
ADD file:aee0d7770ef2f24dc9697e86d391529d001a4013b6e30a3ac90a57932814a57e in / 
# Tue, 25 Apr 2023 17:32:02 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 03:25:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 03:25:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 03:25:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 03:25:23 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 03:25:47 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 04 May 2023 03:26:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 03:26:10 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 11:14:20 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 04 May 2023 11:14:20 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 11:14:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 04 May 2023 11:14:21 GMT
WORKDIR /usr/local/tomcat
# Thu, 04 May 2023 11:14:21 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 11:14:21 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 11:15:34 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 04 May 2023 11:15:34 GMT
ENV TOMCAT_MAJOR=9
# Wed, 10 May 2023 17:56:49 GMT
ENV TOMCAT_VERSION=9.0.75
# Wed, 10 May 2023 17:56:49 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Wed, 10 May 2023 17:56:49 GMT
COPY dir:2a613f9e425d5febc8be5b6c17f49b39f1b8ad84b1601f07f76abed41b25b24b in /usr/local/tomcat 
# Wed, 10 May 2023 17:56:52 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 17:56:54 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 10 May 2023 17:56:54 GMT
EXPOSE 8080
# Wed, 10 May 2023 17:56:54 GMT
CMD ["catalina.sh" "run"]
# Wed, 10 May 2023 18:22:09 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 10 May 2023 18:23:10 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 24 May 2023 23:08:47 GMT
ENV XWIKI_VERSION=14.10.11
# Wed, 24 May 2023 23:08:47 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.11
# Wed, 24 May 2023 23:08:48 GMT
ENV XWIKI_DOWNLOAD_SHA256=0804bdbc2a4eb370a25cfcd9a2185e80e007180007d15fdaa4d371dbd02b5d43
# Wed, 24 May 2023 23:09:27 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 24 May 2023 23:09:29 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Wed, 24 May 2023 23:09:29 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Wed, 24 May 2023 23:09:30 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Wed, 24 May 2023 23:09:30 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Wed, 24 May 2023 23:09:30 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Wed, 24 May 2023 23:09:31 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Wed, 24 May 2023 23:09:31 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 24 May 2023 23:09:31 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 24 May 2023 23:09:31 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 24 May 2023 23:09:31 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 24 May 2023 23:09:32 GMT
VOLUME [/usr/local/xwiki]
# Wed, 24 May 2023 23:09:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 May 2023 23:09:32 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f3f60f415e9a03eed88bd5dd5268c841cde08dacf16911a3ef1e4e0fcdd76568`  
		Last Modified: Wed, 26 Apr 2023 02:08:37 GMT  
		Size: 28.4 MB (28389440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fb3595122d1cb6fffe722e2624c3c89b00776b393256a5444af56ceda691cf`  
		Last Modified: Thu, 04 May 2023 03:28:13 GMT  
		Size: 12.5 MB (12463858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5542665e33e692b672a405517e6e267c4c6e210bc410b97a6a1ce732618caa87`  
		Last Modified: Thu, 04 May 2023 03:29:19 GMT  
		Size: 45.0 MB (45009401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e52b8550f0ced98adb0880bd041e361ffb69810e6071e6d71eb2ec0c8ecfad5`  
		Last Modified: Thu, 04 May 2023 03:29:14 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea5566732e0a920d0a63e4fbebf073d2c49e3f80716df462e73f895cc0c5dfa`  
		Last Modified: Thu, 04 May 2023 11:24:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c6d16bf5ef403ef11a1cc9e40650f402cd1f8269d16982f7daebc2a76ab0d9`  
		Last Modified: Wed, 10 May 2023 18:03:56 GMT  
		Size: 12.2 MB (12242222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eaf464f1c82b5f85e3173b2c732f0928a28e669fcc4af9eb6da48199e92ae50`  
		Last Modified: Wed, 10 May 2023 18:03:55 GMT  
		Size: 453.7 KB (453682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ef5f2b94b25f2b0f609c429cc1626d9dd857d8294d2d872d6595bdeff3a5ca`  
		Last Modified: Wed, 10 May 2023 18:03:55 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7cc67d2dc8f70f6e05051c0e95eb0de93a45de55ba65c355eedaff2bf118e42`  
		Last Modified: Wed, 10 May 2023 18:27:43 GMT  
		Size: 173.4 MB (173350375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0f918d67c923bb6ad20257659a178cf82a52dbd68eda4c094eb3fb372831c2c`  
		Last Modified: Wed, 24 May 2023 23:11:04 GMT  
		Size: 307.3 MB (307250539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced4cf6fb2a03eefd5f5bf442bda27c93928535469b7e8d6fc9c5d7b5ae30b2f`  
		Last Modified: Wed, 24 May 2023 23:10:51 GMT  
		Size: 2.3 MB (2343677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98623f72442cf00c262363a201209a0aa274f36c3ea6fc9f6982e636f879fa70`  
		Last Modified: Wed, 24 May 2023 23:10:50 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7788f555a977b55dd4bb3cc03f0877839200ef650618e788503063bad30080ce`  
		Last Modified: Wed, 24 May 2023 23:10:50 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874c98264dbb8128fd9c27e97654851dfbde45dfb396778744d7616b44591eae`  
		Last Modified: Wed, 24 May 2023 23:10:50 GMT  
		Size: 6.0 KB (6014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee9de251f061dd4ab29b65e5807e482de72b8f045af577bdc2ade102cedf52d`  
		Last Modified: Wed, 24 May 2023 23:10:50 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:14.10.11-mariadb-tomcat`

```console
$ docker pull xwiki@sha256:c1da5ed330d5ca59735d572da388f3a2ce1fbbaf48e03de0b7d0799d1626c0ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:14.10.11-mariadb-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:1a75db7f8992a7c4ee2c526aa1a525456625e7a8d132487a30b4db9e5a4d63eb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **588.5 MB (588483181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c4b7b90fa36f2254d9a63b8f50fc26caa9e6bf856d9a1b53f83db9206d899d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 07:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 07:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 07:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 07:26:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:27:16 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 04 May 2023 07:27:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 07:27:40 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 16:13:14 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 04 May 2023 16:13:14 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 16:13:14 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 04 May 2023 16:13:14 GMT
WORKDIR /usr/local/tomcat
# Thu, 04 May 2023 16:13:14 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 16:13:15 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 16:14:45 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 04 May 2023 16:14:45 GMT
ENV TOMCAT_MAJOR=9
# Wed, 10 May 2023 18:01:17 GMT
ENV TOMCAT_VERSION=9.0.75
# Wed, 10 May 2023 18:01:17 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Wed, 10 May 2023 18:01:17 GMT
COPY dir:606cc669e6833afa7967597ca36d4a4497efbb54719c008108649021142d7549 in /usr/local/tomcat 
# Wed, 10 May 2023 18:01:21 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 18:01:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 10 May 2023 18:01:23 GMT
EXPOSE 8080
# Wed, 10 May 2023 18:01:23 GMT
CMD ["catalina.sh" "run"]
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 10 May 2023 18:28:05 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 24 May 2023 22:47:42 GMT
ENV XWIKI_VERSION=14.10.11
# Wed, 24 May 2023 22:47:42 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.11
# Wed, 24 May 2023 22:47:42 GMT
ENV XWIKI_DOWNLOAD_SHA256=0804bdbc2a4eb370a25cfcd9a2185e80e007180007d15fdaa4d371dbd02b5d43
# Wed, 24 May 2023 22:48:21 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 24 May 2023 22:49:20 GMT
ENV MARIADB_JDBC_VERSION=3.1.4
# Wed, 24 May 2023 22:49:20 GMT
ENV MARIADB_JDBC_SHA256=eb88b5d727d82e25117e2b6fabcec1daf734633b0a576456c73215884c189ad4
# Wed, 24 May 2023 22:49:20 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.1.4
# Wed, 24 May 2023 22:49:20 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.1.4.jar
# Wed, 24 May 2023 22:49:20 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.1.4.jar
# Wed, 24 May 2023 22:49:21 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Wed, 24 May 2023 22:49:21 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 24 May 2023 22:49:21 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 24 May 2023 22:49:22 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 24 May 2023 22:49:22 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 24 May 2023 22:49:22 GMT
VOLUME [/usr/local/xwiki]
# Wed, 24 May 2023 22:49:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 May 2023 22:49:22 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458b02b5411a07f3b354cde2b461caffc1bb184a3413b5736a9e67ee87cb28b2`  
		Last Modified: Thu, 04 May 2023 07:30:02 GMT  
		Size: 12.5 MB (12504170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04a165ead1d5eabe89dc88e53286af89caab22a5d20c53007b9e6e508affb4b`  
		Last Modified: Thu, 04 May 2023 07:31:19 GMT  
		Size: 46.7 MB (46666270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1187c73b18505bd4495bc03ccbdb723388dfe4d633fd12be845dfe8e253e48e2`  
		Last Modified: Thu, 04 May 2023 07:31:12 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c833cbb14374cde014505e77f6a6122773984a691844e4138fc15cae99ba625`  
		Last Modified: Thu, 04 May 2023 16:24:19 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439ac04571c77c4330db518bc8f35b70f8723246ed34c98787f7ac8d7dc30b42`  
		Last Modified: Wed, 10 May 2023 18:09:06 GMT  
		Size: 12.2 MB (12236613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8e775ba0b76c6692c0b9211e4b94653ba2aa16fdc7a5e3347aba962b684508`  
		Last Modified: Wed, 10 May 2023 18:09:06 GMT  
		Size: 454.2 KB (454222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee5c1ba4848e97d4e3c43d9d4bca0eeeccf2d5d7f6d805d748da4a7d24ad14e`  
		Last Modified: Wed, 10 May 2023 18:09:05 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffadd10be916fc5729676141f5d0ba6aa30968b75555790e449d4988dc81332a`  
		Last Modified: Wed, 10 May 2023 18:32:42 GMT  
		Size: 178.3 MB (178334017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3968819bf3a63424c2b6a4e9591f0c9e6ffbb99a92e0c8d8bb65c67dee37c591`  
		Last Modified: Wed, 24 May 2023 22:50:04 GMT  
		Size: 307.3 MB (307250466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe65a2b1c269931f9affdbf4926be3a7e6789a0eb5ef5c8469c0ab01708aa54e`  
		Last Modified: Wed, 24 May 2023 22:51:02 GMT  
		Size: 594.6 KB (594559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b1b0dad9556a98d3e225960bc3fdd9550ee0d50cc15b4667535a69cc8cc4f5`  
		Last Modified: Wed, 24 May 2023 22:51:02 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b44a0baefcddcca335cf3e635a10b22f472dcb576dfa3b75755f9db5fc9ec853`  
		Last Modified: Wed, 24 May 2023 22:51:02 GMT  
		Size: 2.3 KB (2313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ebfb8ffc93a8da62fdc799b946b53ae557f1061d920db81d002a7fea3bacbde`  
		Last Modified: Wed, 24 May 2023 22:51:02 GMT  
		Size: 6.0 KB (6019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f48b704e13efa0bd740446998f3193c87fcb7dadc14138af9f9103fdbdcdc87`  
		Last Modified: Wed, 24 May 2023 22:51:02 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:14.10.11-mariadb-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:00f5266daef25dc10485eca8533381e175b534a692a79b5e108b3563b604c1a5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.8 MB (579766697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e448e5a8cc6e1fb57ca6ebb008b4fa70de9683b31e4f558bd222f5a5fd0b441f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 25 Apr 2023 17:31:58 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:31:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:31:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:31:59 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:32:02 GMT
ADD file:aee0d7770ef2f24dc9697e86d391529d001a4013b6e30a3ac90a57932814a57e in / 
# Tue, 25 Apr 2023 17:32:02 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 03:25:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 03:25:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 03:25:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 03:25:23 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 03:25:47 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 04 May 2023 03:26:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 03:26:10 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 11:14:20 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 04 May 2023 11:14:20 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 11:14:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 04 May 2023 11:14:21 GMT
WORKDIR /usr/local/tomcat
# Thu, 04 May 2023 11:14:21 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 11:14:21 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 11:15:34 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 04 May 2023 11:15:34 GMT
ENV TOMCAT_MAJOR=9
# Wed, 10 May 2023 17:56:49 GMT
ENV TOMCAT_VERSION=9.0.75
# Wed, 10 May 2023 17:56:49 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Wed, 10 May 2023 17:56:49 GMT
COPY dir:2a613f9e425d5febc8be5b6c17f49b39f1b8ad84b1601f07f76abed41b25b24b in /usr/local/tomcat 
# Wed, 10 May 2023 17:56:52 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 17:56:54 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 10 May 2023 17:56:54 GMT
EXPOSE 8080
# Wed, 10 May 2023 17:56:54 GMT
CMD ["catalina.sh" "run"]
# Wed, 10 May 2023 18:22:09 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 10 May 2023 18:23:10 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 24 May 2023 23:08:47 GMT
ENV XWIKI_VERSION=14.10.11
# Wed, 24 May 2023 23:08:47 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.11
# Wed, 24 May 2023 23:08:48 GMT
ENV XWIKI_DOWNLOAD_SHA256=0804bdbc2a4eb370a25cfcd9a2185e80e007180007d15fdaa4d371dbd02b5d43
# Wed, 24 May 2023 23:09:27 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 24 May 2023 23:10:23 GMT
ENV MARIADB_JDBC_VERSION=3.1.4
# Wed, 24 May 2023 23:10:23 GMT
ENV MARIADB_JDBC_SHA256=eb88b5d727d82e25117e2b6fabcec1daf734633b0a576456c73215884c189ad4
# Wed, 24 May 2023 23:10:23 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.1.4
# Wed, 24 May 2023 23:10:23 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.1.4.jar
# Wed, 24 May 2023 23:10:23 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.1.4.jar
# Wed, 24 May 2023 23:10:24 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Wed, 24 May 2023 23:10:24 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 24 May 2023 23:10:24 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 24 May 2023 23:10:25 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 24 May 2023 23:10:25 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 24 May 2023 23:10:25 GMT
VOLUME [/usr/local/xwiki]
# Wed, 24 May 2023 23:10:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 May 2023 23:10:25 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f3f60f415e9a03eed88bd5dd5268c841cde08dacf16911a3ef1e4e0fcdd76568`  
		Last Modified: Wed, 26 Apr 2023 02:08:37 GMT  
		Size: 28.4 MB (28389440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fb3595122d1cb6fffe722e2624c3c89b00776b393256a5444af56ceda691cf`  
		Last Modified: Thu, 04 May 2023 03:28:13 GMT  
		Size: 12.5 MB (12463858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5542665e33e692b672a405517e6e267c4c6e210bc410b97a6a1ce732618caa87`  
		Last Modified: Thu, 04 May 2023 03:29:19 GMT  
		Size: 45.0 MB (45009401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e52b8550f0ced98adb0880bd041e361ffb69810e6071e6d71eb2ec0c8ecfad5`  
		Last Modified: Thu, 04 May 2023 03:29:14 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea5566732e0a920d0a63e4fbebf073d2c49e3f80716df462e73f895cc0c5dfa`  
		Last Modified: Thu, 04 May 2023 11:24:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c6d16bf5ef403ef11a1cc9e40650f402cd1f8269d16982f7daebc2a76ab0d9`  
		Last Modified: Wed, 10 May 2023 18:03:56 GMT  
		Size: 12.2 MB (12242222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eaf464f1c82b5f85e3173b2c732f0928a28e669fcc4af9eb6da48199e92ae50`  
		Last Modified: Wed, 10 May 2023 18:03:55 GMT  
		Size: 453.7 KB (453682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ef5f2b94b25f2b0f609c429cc1626d9dd857d8294d2d872d6595bdeff3a5ca`  
		Last Modified: Wed, 10 May 2023 18:03:55 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7cc67d2dc8f70f6e05051c0e95eb0de93a45de55ba65c355eedaff2bf118e42`  
		Last Modified: Wed, 10 May 2023 18:27:43 GMT  
		Size: 173.4 MB (173350375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0f918d67c923bb6ad20257659a178cf82a52dbd68eda4c094eb3fb372831c2c`  
		Last Modified: Wed, 24 May 2023 23:11:04 GMT  
		Size: 307.3 MB (307250539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d912a3a12e11af60d952ffa7ac5359c7aa515a7300f75c5ba871ea94e62bd43`  
		Last Modified: Wed, 24 May 2023 23:12:02 GMT  
		Size: 594.5 KB (594549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f871b4dce32a1e7dcce9033dac703bc174253e8b26f41ea7a7d4c4ae1d98372f`  
		Last Modified: Wed, 24 May 2023 23:12:02 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f1d5bccd3396b98e1cf536def6525a295c0a35c6c70a438fc6a917b322efd5f`  
		Last Modified: Wed, 24 May 2023 23:12:02 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b11946e15dcff3a5243af68d7416f684d866731eedb590452d184678df469e`  
		Last Modified: Wed, 24 May 2023 23:12:02 GMT  
		Size: 6.0 KB (6013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33aa2a2a6531b6d4ff0f2638634bbb0a42a3796e25d026234551deb2add3b637`  
		Last Modified: Wed, 24 May 2023 23:12:02 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:14.10.11-mysql-tomcat`

```console
$ docker pull xwiki@sha256:3cb3e791882b8ad6819d53ac0e7fb6c678ba6435b06061929dca6ce1a98fbef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:14.10.11-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:8d0ae8c6e385bf7493b07cbab2a2afa371e97538db4f1c040a18c393b5d1e090
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.2 MB (590232292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eff782e5d932a0d40c015b5812ebe948e85c30648a4875e24e6320a36ebb037b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 07:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 07:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 07:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 07:26:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:27:16 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 04 May 2023 07:27:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 07:27:40 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 16:13:14 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 04 May 2023 16:13:14 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 16:13:14 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 04 May 2023 16:13:14 GMT
WORKDIR /usr/local/tomcat
# Thu, 04 May 2023 16:13:14 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 16:13:15 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 16:14:45 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 04 May 2023 16:14:45 GMT
ENV TOMCAT_MAJOR=9
# Wed, 10 May 2023 18:01:17 GMT
ENV TOMCAT_VERSION=9.0.75
# Wed, 10 May 2023 18:01:17 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Wed, 10 May 2023 18:01:17 GMT
COPY dir:606cc669e6833afa7967597ca36d4a4497efbb54719c008108649021142d7549 in /usr/local/tomcat 
# Wed, 10 May 2023 18:01:21 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 18:01:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 10 May 2023 18:01:23 GMT
EXPOSE 8080
# Wed, 10 May 2023 18:01:23 GMT
CMD ["catalina.sh" "run"]
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 10 May 2023 18:28:05 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 24 May 2023 22:47:42 GMT
ENV XWIKI_VERSION=14.10.11
# Wed, 24 May 2023 22:47:42 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.11
# Wed, 24 May 2023 22:47:42 GMT
ENV XWIKI_DOWNLOAD_SHA256=0804bdbc2a4eb370a25cfcd9a2185e80e007180007d15fdaa4d371dbd02b5d43
# Wed, 24 May 2023 22:48:21 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 24 May 2023 22:48:22 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Wed, 24 May 2023 22:48:22 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Wed, 24 May 2023 22:48:22 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Wed, 24 May 2023 22:48:22 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Wed, 24 May 2023 22:48:22 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Wed, 24 May 2023 22:48:23 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Wed, 24 May 2023 22:48:23 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 24 May 2023 22:48:23 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 24 May 2023 22:48:23 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 24 May 2023 22:48:24 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 24 May 2023 22:48:24 GMT
VOLUME [/usr/local/xwiki]
# Wed, 24 May 2023 22:48:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 May 2023 22:48:24 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458b02b5411a07f3b354cde2b461caffc1bb184a3413b5736a9e67ee87cb28b2`  
		Last Modified: Thu, 04 May 2023 07:30:02 GMT  
		Size: 12.5 MB (12504170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04a165ead1d5eabe89dc88e53286af89caab22a5d20c53007b9e6e508affb4b`  
		Last Modified: Thu, 04 May 2023 07:31:19 GMT  
		Size: 46.7 MB (46666270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1187c73b18505bd4495bc03ccbdb723388dfe4d633fd12be845dfe8e253e48e2`  
		Last Modified: Thu, 04 May 2023 07:31:12 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c833cbb14374cde014505e77f6a6122773984a691844e4138fc15cae99ba625`  
		Last Modified: Thu, 04 May 2023 16:24:19 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439ac04571c77c4330db518bc8f35b70f8723246ed34c98787f7ac8d7dc30b42`  
		Last Modified: Wed, 10 May 2023 18:09:06 GMT  
		Size: 12.2 MB (12236613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8e775ba0b76c6692c0b9211e4b94653ba2aa16fdc7a5e3347aba962b684508`  
		Last Modified: Wed, 10 May 2023 18:09:06 GMT  
		Size: 454.2 KB (454222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee5c1ba4848e97d4e3c43d9d4bca0eeeccf2d5d7f6d805d748da4a7d24ad14e`  
		Last Modified: Wed, 10 May 2023 18:09:05 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffadd10be916fc5729676141f5d0ba6aa30968b75555790e449d4988dc81332a`  
		Last Modified: Wed, 10 May 2023 18:32:42 GMT  
		Size: 178.3 MB (178334017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3968819bf3a63424c2b6a4e9591f0c9e6ffbb99a92e0c8d8bb65c67dee37c591`  
		Last Modified: Wed, 24 May 2023 22:50:04 GMT  
		Size: 307.3 MB (307250466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab4c543f2a230baf4ee559f04be553bc00d7b77cc356fee1f21587123cb6977`  
		Last Modified: Wed, 24 May 2023 22:49:49 GMT  
		Size: 2.3 MB (2343680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22684cbd7ece18edde12615b426a6542f278c82ffebfd4d0e88ef0ff8fbde0b`  
		Last Modified: Wed, 24 May 2023 22:49:48 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5270a8761eb66f6e2d094c0879e26935456fa9e19b282bbed9418b58631140c1`  
		Last Modified: Wed, 24 May 2023 22:49:48 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efce4adb2bae1b274febb0d3785c785befb8c4de6c50df158a2aa23673c5b60d`  
		Last Modified: Wed, 24 May 2023 22:49:48 GMT  
		Size: 6.0 KB (6017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9715a623bab854429c5628dcca4718382ada25dbc334b3d61b24a46031cd5d44`  
		Last Modified: Wed, 24 May 2023 22:49:48 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:14.10.11-mysql-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:15957635ec1e31779c981c0817bf66a72c04e6218e1acc75ef471fc7f46dd01c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.5 MB (581515826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aa7648bbd0225e907a6fd992596c1aedb9a12baa3eb30a4a458df9d4af79c91`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 25 Apr 2023 17:31:58 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:31:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:31:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:31:59 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:32:02 GMT
ADD file:aee0d7770ef2f24dc9697e86d391529d001a4013b6e30a3ac90a57932814a57e in / 
# Tue, 25 Apr 2023 17:32:02 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 03:25:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 03:25:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 03:25:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 03:25:23 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 03:25:47 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 04 May 2023 03:26:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 03:26:10 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 11:14:20 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 04 May 2023 11:14:20 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 11:14:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 04 May 2023 11:14:21 GMT
WORKDIR /usr/local/tomcat
# Thu, 04 May 2023 11:14:21 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 11:14:21 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 11:15:34 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 04 May 2023 11:15:34 GMT
ENV TOMCAT_MAJOR=9
# Wed, 10 May 2023 17:56:49 GMT
ENV TOMCAT_VERSION=9.0.75
# Wed, 10 May 2023 17:56:49 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Wed, 10 May 2023 17:56:49 GMT
COPY dir:2a613f9e425d5febc8be5b6c17f49b39f1b8ad84b1601f07f76abed41b25b24b in /usr/local/tomcat 
# Wed, 10 May 2023 17:56:52 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 17:56:54 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 10 May 2023 17:56:54 GMT
EXPOSE 8080
# Wed, 10 May 2023 17:56:54 GMT
CMD ["catalina.sh" "run"]
# Wed, 10 May 2023 18:22:09 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 10 May 2023 18:23:10 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 24 May 2023 23:08:47 GMT
ENV XWIKI_VERSION=14.10.11
# Wed, 24 May 2023 23:08:47 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.11
# Wed, 24 May 2023 23:08:48 GMT
ENV XWIKI_DOWNLOAD_SHA256=0804bdbc2a4eb370a25cfcd9a2185e80e007180007d15fdaa4d371dbd02b5d43
# Wed, 24 May 2023 23:09:27 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 24 May 2023 23:09:29 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Wed, 24 May 2023 23:09:29 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Wed, 24 May 2023 23:09:30 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Wed, 24 May 2023 23:09:30 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Wed, 24 May 2023 23:09:30 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Wed, 24 May 2023 23:09:31 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Wed, 24 May 2023 23:09:31 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 24 May 2023 23:09:31 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 24 May 2023 23:09:31 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 24 May 2023 23:09:31 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 24 May 2023 23:09:32 GMT
VOLUME [/usr/local/xwiki]
# Wed, 24 May 2023 23:09:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 May 2023 23:09:32 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f3f60f415e9a03eed88bd5dd5268c841cde08dacf16911a3ef1e4e0fcdd76568`  
		Last Modified: Wed, 26 Apr 2023 02:08:37 GMT  
		Size: 28.4 MB (28389440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fb3595122d1cb6fffe722e2624c3c89b00776b393256a5444af56ceda691cf`  
		Last Modified: Thu, 04 May 2023 03:28:13 GMT  
		Size: 12.5 MB (12463858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5542665e33e692b672a405517e6e267c4c6e210bc410b97a6a1ce732618caa87`  
		Last Modified: Thu, 04 May 2023 03:29:19 GMT  
		Size: 45.0 MB (45009401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e52b8550f0ced98adb0880bd041e361ffb69810e6071e6d71eb2ec0c8ecfad5`  
		Last Modified: Thu, 04 May 2023 03:29:14 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea5566732e0a920d0a63e4fbebf073d2c49e3f80716df462e73f895cc0c5dfa`  
		Last Modified: Thu, 04 May 2023 11:24:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c6d16bf5ef403ef11a1cc9e40650f402cd1f8269d16982f7daebc2a76ab0d9`  
		Last Modified: Wed, 10 May 2023 18:03:56 GMT  
		Size: 12.2 MB (12242222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eaf464f1c82b5f85e3173b2c732f0928a28e669fcc4af9eb6da48199e92ae50`  
		Last Modified: Wed, 10 May 2023 18:03:55 GMT  
		Size: 453.7 KB (453682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ef5f2b94b25f2b0f609c429cc1626d9dd857d8294d2d872d6595bdeff3a5ca`  
		Last Modified: Wed, 10 May 2023 18:03:55 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7cc67d2dc8f70f6e05051c0e95eb0de93a45de55ba65c355eedaff2bf118e42`  
		Last Modified: Wed, 10 May 2023 18:27:43 GMT  
		Size: 173.4 MB (173350375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0f918d67c923bb6ad20257659a178cf82a52dbd68eda4c094eb3fb372831c2c`  
		Last Modified: Wed, 24 May 2023 23:11:04 GMT  
		Size: 307.3 MB (307250539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced4cf6fb2a03eefd5f5bf442bda27c93928535469b7e8d6fc9c5d7b5ae30b2f`  
		Last Modified: Wed, 24 May 2023 23:10:51 GMT  
		Size: 2.3 MB (2343677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98623f72442cf00c262363a201209a0aa274f36c3ea6fc9f6982e636f879fa70`  
		Last Modified: Wed, 24 May 2023 23:10:50 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7788f555a977b55dd4bb3cc03f0877839200ef650618e788503063bad30080ce`  
		Last Modified: Wed, 24 May 2023 23:10:50 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874c98264dbb8128fd9c27e97654851dfbde45dfb396778744d7616b44591eae`  
		Last Modified: Wed, 24 May 2023 23:10:50 GMT  
		Size: 6.0 KB (6014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee9de251f061dd4ab29b65e5807e482de72b8f045af577bdc2ade102cedf52d`  
		Last Modified: Wed, 24 May 2023 23:10:50 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:14.10.11-postgres-tomcat`

```console
$ docker pull xwiki@sha256:dabd869e53131a2d15143bd5393863a574bacd8268d667ab5f9be188c80b39d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:14.10.11-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:ccb7ea5c1410db8b59df0ea0243933bbb5050cf5ed8bc35d3b4702d5928d1482
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.8 MB (589768452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71815ff74c00cebccb5539716f3c3f0391b90709502c0f2f23eae95fd4d9b7f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 07:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 07:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 07:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 07:26:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:27:16 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 04 May 2023 07:27:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 07:27:40 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 16:13:14 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 04 May 2023 16:13:14 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 16:13:14 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 04 May 2023 16:13:14 GMT
WORKDIR /usr/local/tomcat
# Thu, 04 May 2023 16:13:14 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 16:13:15 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 16:14:45 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 04 May 2023 16:14:45 GMT
ENV TOMCAT_MAJOR=9
# Wed, 10 May 2023 18:01:17 GMT
ENV TOMCAT_VERSION=9.0.75
# Wed, 10 May 2023 18:01:17 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Wed, 10 May 2023 18:01:17 GMT
COPY dir:606cc669e6833afa7967597ca36d4a4497efbb54719c008108649021142d7549 in /usr/local/tomcat 
# Wed, 10 May 2023 18:01:21 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 18:01:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 10 May 2023 18:01:23 GMT
EXPOSE 8080
# Wed, 10 May 2023 18:01:23 GMT
CMD ["catalina.sh" "run"]
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 10 May 2023 18:29:15 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Wed, 24 May 2023 22:48:31 GMT
ENV XWIKI_VERSION=14.10.11
# Wed, 24 May 2023 22:48:31 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.11
# Wed, 24 May 2023 22:48:31 GMT
ENV XWIKI_DOWNLOAD_SHA256=0804bdbc2a4eb370a25cfcd9a2185e80e007180007d15fdaa4d371dbd02b5d43
# Wed, 24 May 2023 22:49:09 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 24 May 2023 22:49:11 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Wed, 24 May 2023 22:49:11 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 24 May 2023 22:49:11 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 24 May 2023 22:49:11 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 24 May 2023 22:49:11 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 24 May 2023 22:49:11 GMT
VOLUME [/usr/local/xwiki]
# Wed, 24 May 2023 22:49:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 May 2023 22:49:12 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458b02b5411a07f3b354cde2b461caffc1bb184a3413b5736a9e67ee87cb28b2`  
		Last Modified: Thu, 04 May 2023 07:30:02 GMT  
		Size: 12.5 MB (12504170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04a165ead1d5eabe89dc88e53286af89caab22a5d20c53007b9e6e508affb4b`  
		Last Modified: Thu, 04 May 2023 07:31:19 GMT  
		Size: 46.7 MB (46666270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1187c73b18505bd4495bc03ccbdb723388dfe4d633fd12be845dfe8e253e48e2`  
		Last Modified: Thu, 04 May 2023 07:31:12 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c833cbb14374cde014505e77f6a6122773984a691844e4138fc15cae99ba625`  
		Last Modified: Thu, 04 May 2023 16:24:19 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439ac04571c77c4330db518bc8f35b70f8723246ed34c98787f7ac8d7dc30b42`  
		Last Modified: Wed, 10 May 2023 18:09:06 GMT  
		Size: 12.2 MB (12236613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8e775ba0b76c6692c0b9211e4b94653ba2aa16fdc7a5e3347aba962b684508`  
		Last Modified: Wed, 10 May 2023 18:09:06 GMT  
		Size: 454.2 KB (454222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee5c1ba4848e97d4e3c43d9d4bca0eeeccf2d5d7f6d805d748da4a7d24ad14e`  
		Last Modified: Wed, 10 May 2023 18:09:05 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29abf03d18e0bc34be536fce36ea27d0012a4d330eed44003684563b4d891b2d`  
		Last Modified: Wed, 10 May 2023 18:33:36 GMT  
		Size: 179.3 MB (179276853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:498ed996b7f85205493a73418ae815f35210fc8d8b7b70baa9a06de3e5c233db`  
		Last Modified: Wed, 24 May 2023 22:50:46 GMT  
		Size: 307.3 MB (307250477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:726404a64f919d8c5876da440316ad8fe4a45edd3630ad29f6901546744c11b4`  
		Last Modified: Wed, 24 May 2023 22:50:30 GMT  
		Size: 936.8 KB (936849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84cee4a8e3ec67483536219c5828a467fbc92b808b723cc7fe131aa9d4a6c0ca`  
		Last Modified: Wed, 24 May 2023 22:50:30 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f650315d22dd71a78884aa2fd92ca686e5ce16f9206197580eecb4ecdff2de`  
		Last Modified: Wed, 24 May 2023 22:50:30 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae0aba32059faa0517242b3ddd90818c736c00398d30b55ec885149ac65c2f29`  
		Last Modified: Wed, 24 May 2023 22:50:30 GMT  
		Size: 6.0 KB (6016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9f18e6a2d23412d06f75bdd16e45b58b9e670d8d683b0e55422033d911fc9f1`  
		Last Modified: Wed, 24 May 2023 22:50:30 GMT  
		Size: 2.5 KB (2502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:14.10.11-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:80beeb7d3308b8ad1ce8a2ce4e70eb53da61c4632fb10da1448ad9fa7a78d3be
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.0 MB (581049648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ec4529f91042538f49ba29100185d25c41eef43d8163bbb16ad47093be7adbd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 25 Apr 2023 17:31:58 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:31:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:31:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:31:59 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:32:02 GMT
ADD file:aee0d7770ef2f24dc9697e86d391529d001a4013b6e30a3ac90a57932814a57e in / 
# Tue, 25 Apr 2023 17:32:02 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 03:25:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 03:25:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 03:25:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 03:25:23 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 03:25:47 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 04 May 2023 03:26:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 03:26:10 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 11:14:20 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 04 May 2023 11:14:20 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 11:14:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 04 May 2023 11:14:21 GMT
WORKDIR /usr/local/tomcat
# Thu, 04 May 2023 11:14:21 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 11:14:21 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 11:15:34 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 04 May 2023 11:15:34 GMT
ENV TOMCAT_MAJOR=9
# Wed, 10 May 2023 17:56:49 GMT
ENV TOMCAT_VERSION=9.0.75
# Wed, 10 May 2023 17:56:49 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Wed, 10 May 2023 17:56:49 GMT
COPY dir:2a613f9e425d5febc8be5b6c17f49b39f1b8ad84b1601f07f76abed41b25b24b in /usr/local/tomcat 
# Wed, 10 May 2023 17:56:52 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 17:56:54 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 10 May 2023 17:56:54 GMT
EXPOSE 8080
# Wed, 10 May 2023 17:56:54 GMT
CMD ["catalina.sh" "run"]
# Wed, 10 May 2023 18:22:09 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 10 May 2023 18:24:24 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Wed, 24 May 2023 23:09:35 GMT
ENV XWIKI_VERSION=14.10.11
# Wed, 24 May 2023 23:09:35 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.11
# Wed, 24 May 2023 23:09:35 GMT
ENV XWIKI_DOWNLOAD_SHA256=0804bdbc2a4eb370a25cfcd9a2185e80e007180007d15fdaa4d371dbd02b5d43
# Wed, 24 May 2023 23:10:15 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 24 May 2023 23:10:17 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Wed, 24 May 2023 23:10:17 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 24 May 2023 23:10:17 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 24 May 2023 23:10:18 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 24 May 2023 23:10:18 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 24 May 2023 23:10:18 GMT
VOLUME [/usr/local/xwiki]
# Wed, 24 May 2023 23:10:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 May 2023 23:10:18 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f3f60f415e9a03eed88bd5dd5268c841cde08dacf16911a3ef1e4e0fcdd76568`  
		Last Modified: Wed, 26 Apr 2023 02:08:37 GMT  
		Size: 28.4 MB (28389440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fb3595122d1cb6fffe722e2624c3c89b00776b393256a5444af56ceda691cf`  
		Last Modified: Thu, 04 May 2023 03:28:13 GMT  
		Size: 12.5 MB (12463858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5542665e33e692b672a405517e6e267c4c6e210bc410b97a6a1ce732618caa87`  
		Last Modified: Thu, 04 May 2023 03:29:19 GMT  
		Size: 45.0 MB (45009401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e52b8550f0ced98adb0880bd041e361ffb69810e6071e6d71eb2ec0c8ecfad5`  
		Last Modified: Thu, 04 May 2023 03:29:14 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea5566732e0a920d0a63e4fbebf073d2c49e3f80716df462e73f895cc0c5dfa`  
		Last Modified: Thu, 04 May 2023 11:24:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c6d16bf5ef403ef11a1cc9e40650f402cd1f8269d16982f7daebc2a76ab0d9`  
		Last Modified: Wed, 10 May 2023 18:03:56 GMT  
		Size: 12.2 MB (12242222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eaf464f1c82b5f85e3173b2c732f0928a28e669fcc4af9eb6da48199e92ae50`  
		Last Modified: Wed, 10 May 2023 18:03:55 GMT  
		Size: 453.7 KB (453682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ef5f2b94b25f2b0f609c429cc1626d9dd857d8294d2d872d6595bdeff3a5ca`  
		Last Modified: Wed, 10 May 2023 18:03:55 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e76b785cabb7a84968f4d713d3072c255796ddcef576690d954e3fc5b1a09604`  
		Last Modified: Wed, 10 May 2023 18:28:29 GMT  
		Size: 174.3 MB (174290936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ca8b2542757030e2106531ddc6ec3e6dfa6acc493a72d909bb0643df73cf80`  
		Last Modified: Wed, 24 May 2023 23:11:45 GMT  
		Size: 307.3 MB (307250465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97cd250ffbef4fb2fdd174dfb45463c24ac51dfafe9a8660d7a4c5779c36753`  
		Last Modified: Wed, 24 May 2023 23:11:32 GMT  
		Size: 936.9 KB (936854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b1f6e5a8be59e46859d1c9303c24792c97fbcadc1855549404052ed0ed691f`  
		Last Modified: Wed, 24 May 2023 23:11:31 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87f9348f23dfc87a0a5dae7c72f497455e4b3205ef78f38f7e26116fbd5468a7`  
		Last Modified: Wed, 24 May 2023 23:11:31 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ef195c009e7dec60741122ecf4e68a4a11ffefeabf35203eb140ed91090c5c`  
		Last Modified: Wed, 24 May 2023 23:11:31 GMT  
		Size: 6.0 KB (6015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:902e7c9edf86f6fe373bd24ddcdff8ca21d7f599de277b9bcffe4106c4bb5f56`  
		Last Modified: Wed, 24 May 2023 23:11:31 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:15`

```console
$ docker pull xwiki@sha256:64eecc071ed4a6789fa3a37bc7fefe78ae08fad1bd9a7fcb6680991bfe7e0923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:15` - linux; amd64

```console
$ docker pull xwiki@sha256:3252b1cffdf08d016b5e82eae75fed4b890197fa6c7afedd85183b898c8a9777
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.2 MB (589196097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a12be474865cce04cbc87bf8db36fdcded4887dc178f49604d68b710d16be056`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 07:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 07:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 07:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 07:26:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:27:16 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 04 May 2023 07:27:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 07:27:40 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 16:13:14 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 04 May 2023 16:13:14 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 16:13:14 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 04 May 2023 16:13:14 GMT
WORKDIR /usr/local/tomcat
# Thu, 04 May 2023 16:13:14 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 16:13:15 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 16:14:45 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 04 May 2023 16:14:45 GMT
ENV TOMCAT_MAJOR=9
# Wed, 10 May 2023 18:01:17 GMT
ENV TOMCAT_VERSION=9.0.75
# Wed, 10 May 2023 18:01:17 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Wed, 10 May 2023 18:01:17 GMT
COPY dir:606cc669e6833afa7967597ca36d4a4497efbb54719c008108649021142d7549 in /usr/local/tomcat 
# Wed, 10 May 2023 18:01:21 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 18:01:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 10 May 2023 18:01:23 GMT
EXPOSE 8080
# Wed, 10 May 2023 18:01:23 GMT
CMD ["catalina.sh" "run"]
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 10 May 2023 18:28:05 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 18:28:06 GMT
ENV XWIKI_VERSION=15.3
# Wed, 10 May 2023 18:28:06 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.3
# Wed, 10 May 2023 18:28:06 GMT
ENV XWIKI_DOWNLOAD_SHA256=fbe35bcc5c6cc5764f2a1da4aca7878531f93bae069d94f399fea7d9656da3b8
# Wed, 10 May 2023 18:28:44 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 10 May 2023 18:28:45 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Wed, 10 May 2023 18:28:45 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Wed, 10 May 2023 18:28:45 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Wed, 10 May 2023 18:28:45 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Wed, 10 May 2023 18:28:45 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Wed, 10 May 2023 18:28:46 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Wed, 10 May 2023 18:28:46 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 10 May 2023 18:28:46 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 10 May 2023 18:28:47 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 10 May 2023 18:28:47 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 10 May 2023 18:28:47 GMT
VOLUME [/usr/local/xwiki]
# Wed, 10 May 2023 18:28:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 May 2023 18:28:47 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458b02b5411a07f3b354cde2b461caffc1bb184a3413b5736a9e67ee87cb28b2`  
		Last Modified: Thu, 04 May 2023 07:30:02 GMT  
		Size: 12.5 MB (12504170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04a165ead1d5eabe89dc88e53286af89caab22a5d20c53007b9e6e508affb4b`  
		Last Modified: Thu, 04 May 2023 07:31:19 GMT  
		Size: 46.7 MB (46666270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1187c73b18505bd4495bc03ccbdb723388dfe4d633fd12be845dfe8e253e48e2`  
		Last Modified: Thu, 04 May 2023 07:31:12 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c833cbb14374cde014505e77f6a6122773984a691844e4138fc15cae99ba625`  
		Last Modified: Thu, 04 May 2023 16:24:19 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439ac04571c77c4330db518bc8f35b70f8723246ed34c98787f7ac8d7dc30b42`  
		Last Modified: Wed, 10 May 2023 18:09:06 GMT  
		Size: 12.2 MB (12236613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8e775ba0b76c6692c0b9211e4b94653ba2aa16fdc7a5e3347aba962b684508`  
		Last Modified: Wed, 10 May 2023 18:09:06 GMT  
		Size: 454.2 KB (454222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee5c1ba4848e97d4e3c43d9d4bca0eeeccf2d5d7f6d805d748da4a7d24ad14e`  
		Last Modified: Wed, 10 May 2023 18:09:05 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffadd10be916fc5729676141f5d0ba6aa30968b75555790e449d4988dc81332a`  
		Last Modified: Wed, 10 May 2023 18:32:42 GMT  
		Size: 178.3 MB (178334017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a29002da219be23e789ef538aeaae1d2296399cdfa64c6c2ed7438210947d7`  
		Last Modified: Wed, 10 May 2023 18:32:34 GMT  
		Size: 306.2 MB (306214302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628263d6dd0a28e03148683703ead7b3c5ef0abd589af1c7352f58aadb9c01a8`  
		Last Modified: Wed, 10 May 2023 18:32:17 GMT  
		Size: 2.3 MB (2343663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81942c3829003d54f85f9d0e3d4fb84d03f7db66060cdd1d2a6a812ce516ccd6`  
		Last Modified: Wed, 10 May 2023 18:32:17 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e635acc63235269abedf51ee8315a58bbb09ff0cbd90f9c6f68c6ea5269d909`  
		Last Modified: Wed, 10 May 2023 18:32:17 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e905c9c0de831ffb2222e8e0420b569e8658457adc3ae299482d6ad73bdb3abb`  
		Last Modified: Wed, 10 May 2023 18:32:17 GMT  
		Size: 6.0 KB (6003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3459a44ee12986d9a54da5b087233e6dfe71171061ce1a63376de231c25ea842`  
		Last Modified: Wed, 10 May 2023 18:32:17 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:15` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:156f67756ea75d27982bd550fe642c9e9bea5cf04a008f6d3e5af5d2343ca83b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.5 MB (580479573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab46181cab4d5b59fc90bad1883f22f0f812a647a62e801240dfa51c485ed1b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 25 Apr 2023 17:31:58 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:31:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:31:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:31:59 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:32:02 GMT
ADD file:aee0d7770ef2f24dc9697e86d391529d001a4013b6e30a3ac90a57932814a57e in / 
# Tue, 25 Apr 2023 17:32:02 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 03:25:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 03:25:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 03:25:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 03:25:23 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 03:25:47 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 04 May 2023 03:26:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 03:26:10 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 11:14:20 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 04 May 2023 11:14:20 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 11:14:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 04 May 2023 11:14:21 GMT
WORKDIR /usr/local/tomcat
# Thu, 04 May 2023 11:14:21 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 11:14:21 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 11:15:34 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 04 May 2023 11:15:34 GMT
ENV TOMCAT_MAJOR=9
# Wed, 10 May 2023 17:56:49 GMT
ENV TOMCAT_VERSION=9.0.75
# Wed, 10 May 2023 17:56:49 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Wed, 10 May 2023 17:56:49 GMT
COPY dir:2a613f9e425d5febc8be5b6c17f49b39f1b8ad84b1601f07f76abed41b25b24b in /usr/local/tomcat 
# Wed, 10 May 2023 17:56:52 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 17:56:54 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 10 May 2023 17:56:54 GMT
EXPOSE 8080
# Wed, 10 May 2023 17:56:54 GMT
CMD ["catalina.sh" "run"]
# Wed, 10 May 2023 18:22:09 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 10 May 2023 18:23:10 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 18:23:13 GMT
ENV XWIKI_VERSION=15.3
# Wed, 10 May 2023 18:23:13 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.3
# Wed, 10 May 2023 18:23:13 GMT
ENV XWIKI_DOWNLOAD_SHA256=fbe35bcc5c6cc5764f2a1da4aca7878531f93bae069d94f399fea7d9656da3b8
# Wed, 10 May 2023 18:23:53 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 10 May 2023 18:23:55 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Wed, 10 May 2023 18:23:55 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Wed, 10 May 2023 18:23:55 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Wed, 10 May 2023 18:23:56 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Wed, 10 May 2023 18:23:56 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Wed, 10 May 2023 18:23:56 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Wed, 10 May 2023 18:23:56 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 10 May 2023 18:23:57 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 10 May 2023 18:23:57 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 10 May 2023 18:23:57 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 10 May 2023 18:23:57 GMT
VOLUME [/usr/local/xwiki]
# Wed, 10 May 2023 18:23:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 May 2023 18:23:57 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f3f60f415e9a03eed88bd5dd5268c841cde08dacf16911a3ef1e4e0fcdd76568`  
		Last Modified: Wed, 26 Apr 2023 02:08:37 GMT  
		Size: 28.4 MB (28389440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fb3595122d1cb6fffe722e2624c3c89b00776b393256a5444af56ceda691cf`  
		Last Modified: Thu, 04 May 2023 03:28:13 GMT  
		Size: 12.5 MB (12463858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5542665e33e692b672a405517e6e267c4c6e210bc410b97a6a1ce732618caa87`  
		Last Modified: Thu, 04 May 2023 03:29:19 GMT  
		Size: 45.0 MB (45009401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e52b8550f0ced98adb0880bd041e361ffb69810e6071e6d71eb2ec0c8ecfad5`  
		Last Modified: Thu, 04 May 2023 03:29:14 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea5566732e0a920d0a63e4fbebf073d2c49e3f80716df462e73f895cc0c5dfa`  
		Last Modified: Thu, 04 May 2023 11:24:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c6d16bf5ef403ef11a1cc9e40650f402cd1f8269d16982f7daebc2a76ab0d9`  
		Last Modified: Wed, 10 May 2023 18:03:56 GMT  
		Size: 12.2 MB (12242222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eaf464f1c82b5f85e3173b2c732f0928a28e669fcc4af9eb6da48199e92ae50`  
		Last Modified: Wed, 10 May 2023 18:03:55 GMT  
		Size: 453.7 KB (453682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ef5f2b94b25f2b0f609c429cc1626d9dd857d8294d2d872d6595bdeff3a5ca`  
		Last Modified: Wed, 10 May 2023 18:03:55 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7cc67d2dc8f70f6e05051c0e95eb0de93a45de55ba65c355eedaff2bf118e42`  
		Last Modified: Wed, 10 May 2023 18:27:43 GMT  
		Size: 173.4 MB (173350375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321a150ce2c4526d3d3f5be05b00d833ba0d530e3b594708aeda7ef22c1855a3`  
		Last Modified: Wed, 10 May 2023 18:27:39 GMT  
		Size: 306.2 MB (306214312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de8537cceb0f08c97a9244c93c7142180f99d25a07a008c897b3e7f2e01749f5`  
		Last Modified: Wed, 10 May 2023 18:27:25 GMT  
		Size: 2.3 MB (2343667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:174ceadf9884a59c863a2f45bc8a9d2c877073089ab2293ec28b4a890edbd549`  
		Last Modified: Wed, 10 May 2023 18:27:25 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4340d0afded864299aaa098ecb92231c246d875fd05e7babc4eb574c24aba63`  
		Last Modified: Wed, 10 May 2023 18:27:25 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ff6fb98971adf0b973b7c902a39cadccb245e656dc8470ec75d8e115e335c0`  
		Last Modified: Wed, 10 May 2023 18:27:25 GMT  
		Size: 6.0 KB (6000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e40c1aaebc8527a9ad709da10958451577ca896b6c968e0e49daf1cc4f790ddd`  
		Last Modified: Wed, 10 May 2023 18:27:25 GMT  
		Size: 2.5 KB (2503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:15-mariadb-tomcat`

```console
$ docker pull xwiki@sha256:ba65c6db6cbf680842f048e25f348c8981c5b4295810467e68a3df22f2c0ef77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:15-mariadb-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:9dc755ce1b9a1d005e8b42c492573371e37310a9960b9b7becc88e7744b5a1b7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **587.4 MB (587443810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9bff1a50bba5fc8078ed4a8574445fb147d50e1d8bd49b788f4954dd1da4132`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 07:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 07:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 07:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 07:26:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:27:16 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 04 May 2023 07:27:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 07:27:40 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 16:13:14 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 04 May 2023 16:13:14 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 16:13:14 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 04 May 2023 16:13:14 GMT
WORKDIR /usr/local/tomcat
# Thu, 04 May 2023 16:13:14 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 16:13:15 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 16:14:45 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 04 May 2023 16:14:45 GMT
ENV TOMCAT_MAJOR=9
# Wed, 10 May 2023 18:01:17 GMT
ENV TOMCAT_VERSION=9.0.75
# Wed, 10 May 2023 18:01:17 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Wed, 10 May 2023 18:01:17 GMT
COPY dir:606cc669e6833afa7967597ca36d4a4497efbb54719c008108649021142d7549 in /usr/local/tomcat 
# Wed, 10 May 2023 18:01:21 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 18:01:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 10 May 2023 18:01:23 GMT
EXPOSE 8080
# Wed, 10 May 2023 18:01:23 GMT
CMD ["catalina.sh" "run"]
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 10 May 2023 18:28:05 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 18:28:06 GMT
ENV XWIKI_VERSION=15.3
# Wed, 10 May 2023 18:28:06 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.3
# Wed, 10 May 2023 18:28:06 GMT
ENV XWIKI_DOWNLOAD_SHA256=fbe35bcc5c6cc5764f2a1da4aca7878531f93bae069d94f399fea7d9656da3b8
# Wed, 10 May 2023 18:28:44 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 10 May 2023 18:30:14 GMT
ENV MARIADB_JDBC_VERSION=3.1.3
# Wed, 10 May 2023 18:30:14 GMT
ENV MARIADB_JDBC_SHA256=11297ee6562426c49c81387c860153cbc131c4c3d042492d4f6d2d97ab3a1ca5
# Wed, 10 May 2023 18:30:14 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.1.3
# Wed, 10 May 2023 18:30:14 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.1.3.jar
# Wed, 10 May 2023 18:30:15 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.1.3.jar
# Wed, 10 May 2023 18:30:15 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Wed, 10 May 2023 18:30:15 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 10 May 2023 18:30:16 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 10 May 2023 18:30:16 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 10 May 2023 18:30:16 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 10 May 2023 18:30:16 GMT
VOLUME [/usr/local/xwiki]
# Wed, 10 May 2023 18:30:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 May 2023 18:30:16 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458b02b5411a07f3b354cde2b461caffc1bb184a3413b5736a9e67ee87cb28b2`  
		Last Modified: Thu, 04 May 2023 07:30:02 GMT  
		Size: 12.5 MB (12504170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04a165ead1d5eabe89dc88e53286af89caab22a5d20c53007b9e6e508affb4b`  
		Last Modified: Thu, 04 May 2023 07:31:19 GMT  
		Size: 46.7 MB (46666270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1187c73b18505bd4495bc03ccbdb723388dfe4d633fd12be845dfe8e253e48e2`  
		Last Modified: Thu, 04 May 2023 07:31:12 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c833cbb14374cde014505e77f6a6122773984a691844e4138fc15cae99ba625`  
		Last Modified: Thu, 04 May 2023 16:24:19 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439ac04571c77c4330db518bc8f35b70f8723246ed34c98787f7ac8d7dc30b42`  
		Last Modified: Wed, 10 May 2023 18:09:06 GMT  
		Size: 12.2 MB (12236613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8e775ba0b76c6692c0b9211e4b94653ba2aa16fdc7a5e3347aba962b684508`  
		Last Modified: Wed, 10 May 2023 18:09:06 GMT  
		Size: 454.2 KB (454222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee5c1ba4848e97d4e3c43d9d4bca0eeeccf2d5d7f6d805d748da4a7d24ad14e`  
		Last Modified: Wed, 10 May 2023 18:09:05 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffadd10be916fc5729676141f5d0ba6aa30968b75555790e449d4988dc81332a`  
		Last Modified: Wed, 10 May 2023 18:32:42 GMT  
		Size: 178.3 MB (178334017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a29002da219be23e789ef538aeaae1d2296399cdfa64c6c2ed7438210947d7`  
		Last Modified: Wed, 10 May 2023 18:32:34 GMT  
		Size: 306.2 MB (306214302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:552f4dcf26ef5ef3b3a7315cc47f3dc07974cb0684775dc9f2d390f7b19be181`  
		Last Modified: Wed, 10 May 2023 18:33:53 GMT  
		Size: 591.4 KB (591369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:647b04728750fccef49babf80ba8257ced3661baa001e9e8a73067bea60c3784`  
		Last Modified: Wed, 10 May 2023 18:33:53 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bcdcc6da901312c0e56c818dfec97184f4cf9e78308964322dba08f16215da0`  
		Last Modified: Wed, 10 May 2023 18:33:53 GMT  
		Size: 2.3 KB (2312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e34abf77fe47a0d97eb01a41d2e6a9b8c0db4e9dfa284dfc767e1d9287b1effe`  
		Last Modified: Wed, 10 May 2023 18:33:53 GMT  
		Size: 6.0 KB (6005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e5b8636c37250081b1a1fd47f2ab5926692c75a635a5b3f805ed897fddb43b`  
		Last Modified: Wed, 10 May 2023 18:33:53 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:15-mariadb-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:8ba7073b3049679fb036a6d00a78b2b70da792b9cde40df0cc088094dc3a3d59
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.7 MB (578727276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c23d916ce05444c655cb6c876c29ee4fe78165b88d66fad2613ac17dcb7b9924`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 25 Apr 2023 17:31:58 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:31:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:31:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:31:59 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:32:02 GMT
ADD file:aee0d7770ef2f24dc9697e86d391529d001a4013b6e30a3ac90a57932814a57e in / 
# Tue, 25 Apr 2023 17:32:02 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 03:25:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 03:25:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 03:25:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 03:25:23 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 03:25:47 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 04 May 2023 03:26:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 03:26:10 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 11:14:20 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 04 May 2023 11:14:20 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 11:14:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 04 May 2023 11:14:21 GMT
WORKDIR /usr/local/tomcat
# Thu, 04 May 2023 11:14:21 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 11:14:21 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 11:15:34 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 04 May 2023 11:15:34 GMT
ENV TOMCAT_MAJOR=9
# Wed, 10 May 2023 17:56:49 GMT
ENV TOMCAT_VERSION=9.0.75
# Wed, 10 May 2023 17:56:49 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Wed, 10 May 2023 17:56:49 GMT
COPY dir:2a613f9e425d5febc8be5b6c17f49b39f1b8ad84b1601f07f76abed41b25b24b in /usr/local/tomcat 
# Wed, 10 May 2023 17:56:52 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 17:56:54 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 10 May 2023 17:56:54 GMT
EXPOSE 8080
# Wed, 10 May 2023 17:56:54 GMT
CMD ["catalina.sh" "run"]
# Wed, 10 May 2023 18:22:09 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 10 May 2023 18:23:10 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 18:23:13 GMT
ENV XWIKI_VERSION=15.3
# Wed, 10 May 2023 18:23:13 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.3
# Wed, 10 May 2023 18:23:13 GMT
ENV XWIKI_DOWNLOAD_SHA256=fbe35bcc5c6cc5764f2a1da4aca7878531f93bae069d94f399fea7d9656da3b8
# Wed, 10 May 2023 18:23:53 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 10 May 2023 18:25:25 GMT
ENV MARIADB_JDBC_VERSION=3.1.3
# Wed, 10 May 2023 18:25:25 GMT
ENV MARIADB_JDBC_SHA256=11297ee6562426c49c81387c860153cbc131c4c3d042492d4f6d2d97ab3a1ca5
# Wed, 10 May 2023 18:25:25 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.1.3
# Wed, 10 May 2023 18:25:25 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.1.3.jar
# Wed, 10 May 2023 18:25:25 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.1.3.jar
# Wed, 10 May 2023 18:25:26 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Wed, 10 May 2023 18:25:26 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 10 May 2023 18:25:26 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 10 May 2023 18:25:26 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 10 May 2023 18:25:26 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 10 May 2023 18:25:26 GMT
VOLUME [/usr/local/xwiki]
# Wed, 10 May 2023 18:25:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 May 2023 18:25:26 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f3f60f415e9a03eed88bd5dd5268c841cde08dacf16911a3ef1e4e0fcdd76568`  
		Last Modified: Wed, 26 Apr 2023 02:08:37 GMT  
		Size: 28.4 MB (28389440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fb3595122d1cb6fffe722e2624c3c89b00776b393256a5444af56ceda691cf`  
		Last Modified: Thu, 04 May 2023 03:28:13 GMT  
		Size: 12.5 MB (12463858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5542665e33e692b672a405517e6e267c4c6e210bc410b97a6a1ce732618caa87`  
		Last Modified: Thu, 04 May 2023 03:29:19 GMT  
		Size: 45.0 MB (45009401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e52b8550f0ced98adb0880bd041e361ffb69810e6071e6d71eb2ec0c8ecfad5`  
		Last Modified: Thu, 04 May 2023 03:29:14 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea5566732e0a920d0a63e4fbebf073d2c49e3f80716df462e73f895cc0c5dfa`  
		Last Modified: Thu, 04 May 2023 11:24:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c6d16bf5ef403ef11a1cc9e40650f402cd1f8269d16982f7daebc2a76ab0d9`  
		Last Modified: Wed, 10 May 2023 18:03:56 GMT  
		Size: 12.2 MB (12242222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eaf464f1c82b5f85e3173b2c732f0928a28e669fcc4af9eb6da48199e92ae50`  
		Last Modified: Wed, 10 May 2023 18:03:55 GMT  
		Size: 453.7 KB (453682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ef5f2b94b25f2b0f609c429cc1626d9dd857d8294d2d872d6595bdeff3a5ca`  
		Last Modified: Wed, 10 May 2023 18:03:55 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7cc67d2dc8f70f6e05051c0e95eb0de93a45de55ba65c355eedaff2bf118e42`  
		Last Modified: Wed, 10 May 2023 18:27:43 GMT  
		Size: 173.4 MB (173350375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321a150ce2c4526d3d3f5be05b00d833ba0d530e3b594708aeda7ef22c1855a3`  
		Last Modified: Wed, 10 May 2023 18:27:39 GMT  
		Size: 306.2 MB (306214312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b88233cbf990b6d3911be4ac1c98102dab898e81d932d7a8a5af05dc01d2815f`  
		Last Modified: Wed, 10 May 2023 18:28:48 GMT  
		Size: 591.4 KB (591368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d80dd60b9d5f967b2e17e47f926486cc55c29ad8afc7d311694a70ac16cee628`  
		Last Modified: Wed, 10 May 2023 18:28:48 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54f901e61dc9940e28d9d144bc1defd8b0b7cc2618db70202a9192e68bbf9fc`  
		Last Modified: Wed, 10 May 2023 18:28:48 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a61b65e0ea72006075aa51df69871be6a2a03de0f4ae1602592693e7ad4634`  
		Last Modified: Wed, 10 May 2023 18:28:48 GMT  
		Size: 6.0 KB (6000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abdd5570c03cb152fa5a309ffb407bb26a45dd2e6a102316c9cbcb102abbb8e9`  
		Last Modified: Wed, 10 May 2023 18:28:48 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:15-mysql-tomcat`

```console
$ docker pull xwiki@sha256:64eecc071ed4a6789fa3a37bc7fefe78ae08fad1bd9a7fcb6680991bfe7e0923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:15-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:3252b1cffdf08d016b5e82eae75fed4b890197fa6c7afedd85183b898c8a9777
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.2 MB (589196097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a12be474865cce04cbc87bf8db36fdcded4887dc178f49604d68b710d16be056`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 07:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 07:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 07:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 07:26:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:27:16 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 04 May 2023 07:27:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 07:27:40 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 16:13:14 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 04 May 2023 16:13:14 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 16:13:14 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 04 May 2023 16:13:14 GMT
WORKDIR /usr/local/tomcat
# Thu, 04 May 2023 16:13:14 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 16:13:15 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 16:14:45 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 04 May 2023 16:14:45 GMT
ENV TOMCAT_MAJOR=9
# Wed, 10 May 2023 18:01:17 GMT
ENV TOMCAT_VERSION=9.0.75
# Wed, 10 May 2023 18:01:17 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Wed, 10 May 2023 18:01:17 GMT
COPY dir:606cc669e6833afa7967597ca36d4a4497efbb54719c008108649021142d7549 in /usr/local/tomcat 
# Wed, 10 May 2023 18:01:21 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 18:01:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 10 May 2023 18:01:23 GMT
EXPOSE 8080
# Wed, 10 May 2023 18:01:23 GMT
CMD ["catalina.sh" "run"]
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 10 May 2023 18:28:05 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 18:28:06 GMT
ENV XWIKI_VERSION=15.3
# Wed, 10 May 2023 18:28:06 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.3
# Wed, 10 May 2023 18:28:06 GMT
ENV XWIKI_DOWNLOAD_SHA256=fbe35bcc5c6cc5764f2a1da4aca7878531f93bae069d94f399fea7d9656da3b8
# Wed, 10 May 2023 18:28:44 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 10 May 2023 18:28:45 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Wed, 10 May 2023 18:28:45 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Wed, 10 May 2023 18:28:45 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Wed, 10 May 2023 18:28:45 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Wed, 10 May 2023 18:28:45 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Wed, 10 May 2023 18:28:46 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Wed, 10 May 2023 18:28:46 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 10 May 2023 18:28:46 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 10 May 2023 18:28:47 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 10 May 2023 18:28:47 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 10 May 2023 18:28:47 GMT
VOLUME [/usr/local/xwiki]
# Wed, 10 May 2023 18:28:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 May 2023 18:28:47 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458b02b5411a07f3b354cde2b461caffc1bb184a3413b5736a9e67ee87cb28b2`  
		Last Modified: Thu, 04 May 2023 07:30:02 GMT  
		Size: 12.5 MB (12504170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04a165ead1d5eabe89dc88e53286af89caab22a5d20c53007b9e6e508affb4b`  
		Last Modified: Thu, 04 May 2023 07:31:19 GMT  
		Size: 46.7 MB (46666270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1187c73b18505bd4495bc03ccbdb723388dfe4d633fd12be845dfe8e253e48e2`  
		Last Modified: Thu, 04 May 2023 07:31:12 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c833cbb14374cde014505e77f6a6122773984a691844e4138fc15cae99ba625`  
		Last Modified: Thu, 04 May 2023 16:24:19 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439ac04571c77c4330db518bc8f35b70f8723246ed34c98787f7ac8d7dc30b42`  
		Last Modified: Wed, 10 May 2023 18:09:06 GMT  
		Size: 12.2 MB (12236613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8e775ba0b76c6692c0b9211e4b94653ba2aa16fdc7a5e3347aba962b684508`  
		Last Modified: Wed, 10 May 2023 18:09:06 GMT  
		Size: 454.2 KB (454222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee5c1ba4848e97d4e3c43d9d4bca0eeeccf2d5d7f6d805d748da4a7d24ad14e`  
		Last Modified: Wed, 10 May 2023 18:09:05 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffadd10be916fc5729676141f5d0ba6aa30968b75555790e449d4988dc81332a`  
		Last Modified: Wed, 10 May 2023 18:32:42 GMT  
		Size: 178.3 MB (178334017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a29002da219be23e789ef538aeaae1d2296399cdfa64c6c2ed7438210947d7`  
		Last Modified: Wed, 10 May 2023 18:32:34 GMT  
		Size: 306.2 MB (306214302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628263d6dd0a28e03148683703ead7b3c5ef0abd589af1c7352f58aadb9c01a8`  
		Last Modified: Wed, 10 May 2023 18:32:17 GMT  
		Size: 2.3 MB (2343663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81942c3829003d54f85f9d0e3d4fb84d03f7db66060cdd1d2a6a812ce516ccd6`  
		Last Modified: Wed, 10 May 2023 18:32:17 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e635acc63235269abedf51ee8315a58bbb09ff0cbd90f9c6f68c6ea5269d909`  
		Last Modified: Wed, 10 May 2023 18:32:17 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e905c9c0de831ffb2222e8e0420b569e8658457adc3ae299482d6ad73bdb3abb`  
		Last Modified: Wed, 10 May 2023 18:32:17 GMT  
		Size: 6.0 KB (6003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3459a44ee12986d9a54da5b087233e6dfe71171061ce1a63376de231c25ea842`  
		Last Modified: Wed, 10 May 2023 18:32:17 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:15-mysql-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:156f67756ea75d27982bd550fe642c9e9bea5cf04a008f6d3e5af5d2343ca83b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.5 MB (580479573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab46181cab4d5b59fc90bad1883f22f0f812a647a62e801240dfa51c485ed1b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 25 Apr 2023 17:31:58 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:31:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:31:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:31:59 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:32:02 GMT
ADD file:aee0d7770ef2f24dc9697e86d391529d001a4013b6e30a3ac90a57932814a57e in / 
# Tue, 25 Apr 2023 17:32:02 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 03:25:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 03:25:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 03:25:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 03:25:23 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 03:25:47 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 04 May 2023 03:26:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 03:26:10 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 11:14:20 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 04 May 2023 11:14:20 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 11:14:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 04 May 2023 11:14:21 GMT
WORKDIR /usr/local/tomcat
# Thu, 04 May 2023 11:14:21 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 11:14:21 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 11:15:34 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 04 May 2023 11:15:34 GMT
ENV TOMCAT_MAJOR=9
# Wed, 10 May 2023 17:56:49 GMT
ENV TOMCAT_VERSION=9.0.75
# Wed, 10 May 2023 17:56:49 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Wed, 10 May 2023 17:56:49 GMT
COPY dir:2a613f9e425d5febc8be5b6c17f49b39f1b8ad84b1601f07f76abed41b25b24b in /usr/local/tomcat 
# Wed, 10 May 2023 17:56:52 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 17:56:54 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 10 May 2023 17:56:54 GMT
EXPOSE 8080
# Wed, 10 May 2023 17:56:54 GMT
CMD ["catalina.sh" "run"]
# Wed, 10 May 2023 18:22:09 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 10 May 2023 18:23:10 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 18:23:13 GMT
ENV XWIKI_VERSION=15.3
# Wed, 10 May 2023 18:23:13 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.3
# Wed, 10 May 2023 18:23:13 GMT
ENV XWIKI_DOWNLOAD_SHA256=fbe35bcc5c6cc5764f2a1da4aca7878531f93bae069d94f399fea7d9656da3b8
# Wed, 10 May 2023 18:23:53 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 10 May 2023 18:23:55 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Wed, 10 May 2023 18:23:55 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Wed, 10 May 2023 18:23:55 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Wed, 10 May 2023 18:23:56 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Wed, 10 May 2023 18:23:56 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Wed, 10 May 2023 18:23:56 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Wed, 10 May 2023 18:23:56 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 10 May 2023 18:23:57 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 10 May 2023 18:23:57 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 10 May 2023 18:23:57 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 10 May 2023 18:23:57 GMT
VOLUME [/usr/local/xwiki]
# Wed, 10 May 2023 18:23:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 May 2023 18:23:57 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f3f60f415e9a03eed88bd5dd5268c841cde08dacf16911a3ef1e4e0fcdd76568`  
		Last Modified: Wed, 26 Apr 2023 02:08:37 GMT  
		Size: 28.4 MB (28389440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fb3595122d1cb6fffe722e2624c3c89b00776b393256a5444af56ceda691cf`  
		Last Modified: Thu, 04 May 2023 03:28:13 GMT  
		Size: 12.5 MB (12463858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5542665e33e692b672a405517e6e267c4c6e210bc410b97a6a1ce732618caa87`  
		Last Modified: Thu, 04 May 2023 03:29:19 GMT  
		Size: 45.0 MB (45009401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e52b8550f0ced98adb0880bd041e361ffb69810e6071e6d71eb2ec0c8ecfad5`  
		Last Modified: Thu, 04 May 2023 03:29:14 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea5566732e0a920d0a63e4fbebf073d2c49e3f80716df462e73f895cc0c5dfa`  
		Last Modified: Thu, 04 May 2023 11:24:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c6d16bf5ef403ef11a1cc9e40650f402cd1f8269d16982f7daebc2a76ab0d9`  
		Last Modified: Wed, 10 May 2023 18:03:56 GMT  
		Size: 12.2 MB (12242222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eaf464f1c82b5f85e3173b2c732f0928a28e669fcc4af9eb6da48199e92ae50`  
		Last Modified: Wed, 10 May 2023 18:03:55 GMT  
		Size: 453.7 KB (453682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ef5f2b94b25f2b0f609c429cc1626d9dd857d8294d2d872d6595bdeff3a5ca`  
		Last Modified: Wed, 10 May 2023 18:03:55 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7cc67d2dc8f70f6e05051c0e95eb0de93a45de55ba65c355eedaff2bf118e42`  
		Last Modified: Wed, 10 May 2023 18:27:43 GMT  
		Size: 173.4 MB (173350375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321a150ce2c4526d3d3f5be05b00d833ba0d530e3b594708aeda7ef22c1855a3`  
		Last Modified: Wed, 10 May 2023 18:27:39 GMT  
		Size: 306.2 MB (306214312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de8537cceb0f08c97a9244c93c7142180f99d25a07a008c897b3e7f2e01749f5`  
		Last Modified: Wed, 10 May 2023 18:27:25 GMT  
		Size: 2.3 MB (2343667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:174ceadf9884a59c863a2f45bc8a9d2c877073089ab2293ec28b4a890edbd549`  
		Last Modified: Wed, 10 May 2023 18:27:25 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4340d0afded864299aaa098ecb92231c246d875fd05e7babc4eb574c24aba63`  
		Last Modified: Wed, 10 May 2023 18:27:25 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ff6fb98971adf0b973b7c902a39cadccb245e656dc8470ec75d8e115e335c0`  
		Last Modified: Wed, 10 May 2023 18:27:25 GMT  
		Size: 6.0 KB (6000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e40c1aaebc8527a9ad709da10958451577ca896b6c968e0e49daf1cc4f790ddd`  
		Last Modified: Wed, 10 May 2023 18:27:25 GMT  
		Size: 2.5 KB (2503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:15-postgres-tomcat`

```console
$ docker pull xwiki@sha256:735933782d363352e7012650659093d08fb0ad9b2fdf0bf6f481f6a6007e57e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:15-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:2900c897a5a066bba2d94f8c0328bda225a94fe5d86155f565d8a024e15967ac
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **588.7 MB (588732305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ea08c636ebabfa7d8491ee29125599e2839801fa05ae791780a490474746bef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 07:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 07:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 07:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 07:26:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:27:16 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 04 May 2023 07:27:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 07:27:40 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 16:13:14 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 04 May 2023 16:13:14 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 16:13:14 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 04 May 2023 16:13:14 GMT
WORKDIR /usr/local/tomcat
# Thu, 04 May 2023 16:13:14 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 16:13:15 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 16:14:45 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 04 May 2023 16:14:45 GMT
ENV TOMCAT_MAJOR=9
# Wed, 10 May 2023 18:01:17 GMT
ENV TOMCAT_VERSION=9.0.75
# Wed, 10 May 2023 18:01:17 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Wed, 10 May 2023 18:01:17 GMT
COPY dir:606cc669e6833afa7967597ca36d4a4497efbb54719c008108649021142d7549 in /usr/local/tomcat 
# Wed, 10 May 2023 18:01:21 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 18:01:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 10 May 2023 18:01:23 GMT
EXPOSE 8080
# Wed, 10 May 2023 18:01:23 GMT
CMD ["catalina.sh" "run"]
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 10 May 2023 18:29:15 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 18:29:16 GMT
ENV XWIKI_VERSION=15.3
# Wed, 10 May 2023 18:29:16 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.3
# Wed, 10 May 2023 18:29:16 GMT
ENV XWIKI_DOWNLOAD_SHA256=fbe35bcc5c6cc5764f2a1da4aca7878531f93bae069d94f399fea7d9656da3b8
# Wed, 10 May 2023 18:29:56 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 10 May 2023 18:29:58 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Wed, 10 May 2023 18:29:58 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 10 May 2023 18:29:58 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 10 May 2023 18:29:58 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 10 May 2023 18:29:58 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 10 May 2023 18:29:59 GMT
VOLUME [/usr/local/xwiki]
# Wed, 10 May 2023 18:29:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 May 2023 18:29:59 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458b02b5411a07f3b354cde2b461caffc1bb184a3413b5736a9e67ee87cb28b2`  
		Last Modified: Thu, 04 May 2023 07:30:02 GMT  
		Size: 12.5 MB (12504170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04a165ead1d5eabe89dc88e53286af89caab22a5d20c53007b9e6e508affb4b`  
		Last Modified: Thu, 04 May 2023 07:31:19 GMT  
		Size: 46.7 MB (46666270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1187c73b18505bd4495bc03ccbdb723388dfe4d633fd12be845dfe8e253e48e2`  
		Last Modified: Thu, 04 May 2023 07:31:12 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c833cbb14374cde014505e77f6a6122773984a691844e4138fc15cae99ba625`  
		Last Modified: Thu, 04 May 2023 16:24:19 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439ac04571c77c4330db518bc8f35b70f8723246ed34c98787f7ac8d7dc30b42`  
		Last Modified: Wed, 10 May 2023 18:09:06 GMT  
		Size: 12.2 MB (12236613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8e775ba0b76c6692c0b9211e4b94653ba2aa16fdc7a5e3347aba962b684508`  
		Last Modified: Wed, 10 May 2023 18:09:06 GMT  
		Size: 454.2 KB (454222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee5c1ba4848e97d4e3c43d9d4bca0eeeccf2d5d7f6d805d748da4a7d24ad14e`  
		Last Modified: Wed, 10 May 2023 18:09:05 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29abf03d18e0bc34be536fce36ea27d0012a4d330eed44003684563b4d891b2d`  
		Last Modified: Wed, 10 May 2023 18:33:36 GMT  
		Size: 179.3 MB (179276853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04893bb957c480bd2610cdfdf9d8ce54f10892dc666a3f546d0a47e08a8b6bf3`  
		Last Modified: Wed, 10 May 2023 18:33:28 GMT  
		Size: 306.2 MB (306214334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c733bdd07cccb12e268038f38cc2208c02cab00afde7af1103ad9ab1d34ddc49`  
		Last Modified: Wed, 10 May 2023 18:33:11 GMT  
		Size: 936.9 KB (936851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:308d5fe9ecebf8518e4a3354dfd14989f5a913a5a8d7a6abec2afaca25ea32ac`  
		Last Modified: Wed, 10 May 2023 18:33:11 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3080392f0ef7aac169f05c443bbff282a8f4c46dbf39c2f91bd942f63c4296e4`  
		Last Modified: Wed, 10 May 2023 18:33:11 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cde226d897c8670f291d599b6ddecdece884739dc8e4f66874764aa1a46fd4a`  
		Last Modified: Wed, 10 May 2023 18:33:11 GMT  
		Size: 6.0 KB (6002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:552d5c735b1472b69f77b166b9824e3f6cee95760872d8f8c00958e81a510428`  
		Last Modified: Wed, 10 May 2023 18:33:11 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:15-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:10bfb120c331e4fd20b20348ab4270888db1418737568c832e5dbb489577d754
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.0 MB (580013492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e62cc10c58ce901b71a525883c5fac34e70c79f319bbce13405788bcaa52e78a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 25 Apr 2023 17:31:58 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:31:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:31:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:31:59 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:32:02 GMT
ADD file:aee0d7770ef2f24dc9697e86d391529d001a4013b6e30a3ac90a57932814a57e in / 
# Tue, 25 Apr 2023 17:32:02 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 03:25:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 03:25:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 03:25:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 03:25:23 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 03:25:47 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 04 May 2023 03:26:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 03:26:10 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 11:14:20 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 04 May 2023 11:14:20 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 11:14:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 04 May 2023 11:14:21 GMT
WORKDIR /usr/local/tomcat
# Thu, 04 May 2023 11:14:21 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 11:14:21 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 11:15:34 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 04 May 2023 11:15:34 GMT
ENV TOMCAT_MAJOR=9
# Wed, 10 May 2023 17:56:49 GMT
ENV TOMCAT_VERSION=9.0.75
# Wed, 10 May 2023 17:56:49 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Wed, 10 May 2023 17:56:49 GMT
COPY dir:2a613f9e425d5febc8be5b6c17f49b39f1b8ad84b1601f07f76abed41b25b24b in /usr/local/tomcat 
# Wed, 10 May 2023 17:56:52 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 17:56:54 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 10 May 2023 17:56:54 GMT
EXPOSE 8080
# Wed, 10 May 2023 17:56:54 GMT
CMD ["catalina.sh" "run"]
# Wed, 10 May 2023 18:22:09 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 10 May 2023 18:24:24 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 18:24:27 GMT
ENV XWIKI_VERSION=15.3
# Wed, 10 May 2023 18:24:28 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.3
# Wed, 10 May 2023 18:24:28 GMT
ENV XWIKI_DOWNLOAD_SHA256=fbe35bcc5c6cc5764f2a1da4aca7878531f93bae069d94f399fea7d9656da3b8
# Wed, 10 May 2023 18:25:07 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 10 May 2023 18:25:10 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Wed, 10 May 2023 18:25:10 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 10 May 2023 18:25:10 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 10 May 2023 18:25:11 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 10 May 2023 18:25:11 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 10 May 2023 18:25:11 GMT
VOLUME [/usr/local/xwiki]
# Wed, 10 May 2023 18:25:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 May 2023 18:25:11 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f3f60f415e9a03eed88bd5dd5268c841cde08dacf16911a3ef1e4e0fcdd76568`  
		Last Modified: Wed, 26 Apr 2023 02:08:37 GMT  
		Size: 28.4 MB (28389440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fb3595122d1cb6fffe722e2624c3c89b00776b393256a5444af56ceda691cf`  
		Last Modified: Thu, 04 May 2023 03:28:13 GMT  
		Size: 12.5 MB (12463858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5542665e33e692b672a405517e6e267c4c6e210bc410b97a6a1ce732618caa87`  
		Last Modified: Thu, 04 May 2023 03:29:19 GMT  
		Size: 45.0 MB (45009401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e52b8550f0ced98adb0880bd041e361ffb69810e6071e6d71eb2ec0c8ecfad5`  
		Last Modified: Thu, 04 May 2023 03:29:14 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea5566732e0a920d0a63e4fbebf073d2c49e3f80716df462e73f895cc0c5dfa`  
		Last Modified: Thu, 04 May 2023 11:24:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c6d16bf5ef403ef11a1cc9e40650f402cd1f8269d16982f7daebc2a76ab0d9`  
		Last Modified: Wed, 10 May 2023 18:03:56 GMT  
		Size: 12.2 MB (12242222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eaf464f1c82b5f85e3173b2c732f0928a28e669fcc4af9eb6da48199e92ae50`  
		Last Modified: Wed, 10 May 2023 18:03:55 GMT  
		Size: 453.7 KB (453682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ef5f2b94b25f2b0f609c429cc1626d9dd857d8294d2d872d6595bdeff3a5ca`  
		Last Modified: Wed, 10 May 2023 18:03:55 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e76b785cabb7a84968f4d713d3072c255796ddcef576690d954e3fc5b1a09604`  
		Last Modified: Wed, 10 May 2023 18:28:29 GMT  
		Size: 174.3 MB (174290936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bbb1bea6fd7e5ad54d9a435449598eab16234ad43ac144f2e8bfd3d6ba08f53`  
		Last Modified: Wed, 10 May 2023 18:28:26 GMT  
		Size: 306.2 MB (306214328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ec4bf084be2f31ea6d132041630e63267918cd9d3fda2c1c5729796be49ca3`  
		Last Modified: Wed, 10 May 2023 18:28:12 GMT  
		Size: 936.9 KB (936850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35482f801e8bffd20763dc900fe57a71e0b8b6e9704fc5960d1ae5c49c36568f`  
		Last Modified: Wed, 10 May 2023 18:28:12 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73fefab11cdaf813c0992abeb9546ca3853626b0c153d8792dda45700405f9d7`  
		Last Modified: Wed, 10 May 2023 18:28:12 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510da944c55d824606569a712e2defc95041c832ea8b07bd45aca2bf455095c2`  
		Last Modified: Wed, 10 May 2023 18:28:12 GMT  
		Size: 6.0 KB (6005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60c6d213e30aaeb6555c54770342ec9de274eb11eff3007dc29f2d552d0dd36c`  
		Last Modified: Wed, 10 May 2023 18:28:12 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:15.4`

**does not exist** (yet?)

## `xwiki:15.4-mariadb-tomcat`

**does not exist** (yet?)

## `xwiki:15.4-mysql-tomcat`

**does not exist** (yet?)

## `xwiki:15.4-postgres-tomcat`

**does not exist** (yet?)

## `xwiki:15.4.0`

**does not exist** (yet?)

## `xwiki:15.4.0-mariadb-tomcat`

**does not exist** (yet?)

## `xwiki:15.4.0-mysql-tomcat`

**does not exist** (yet?)

## `xwiki:15.4.0-postgres-tomcat`

**does not exist** (yet?)

## `xwiki:latest`

```console
$ docker pull xwiki@sha256:64eecc071ed4a6789fa3a37bc7fefe78ae08fad1bd9a7fcb6680991bfe7e0923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:latest` - linux; amd64

```console
$ docker pull xwiki@sha256:3252b1cffdf08d016b5e82eae75fed4b890197fa6c7afedd85183b898c8a9777
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.2 MB (589196097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a12be474865cce04cbc87bf8db36fdcded4887dc178f49604d68b710d16be056`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 07:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 07:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 07:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 07:26:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:27:16 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 04 May 2023 07:27:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 07:27:40 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 16:13:14 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 04 May 2023 16:13:14 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 16:13:14 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 04 May 2023 16:13:14 GMT
WORKDIR /usr/local/tomcat
# Thu, 04 May 2023 16:13:14 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 16:13:15 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 16:14:45 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 04 May 2023 16:14:45 GMT
ENV TOMCAT_MAJOR=9
# Wed, 10 May 2023 18:01:17 GMT
ENV TOMCAT_VERSION=9.0.75
# Wed, 10 May 2023 18:01:17 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Wed, 10 May 2023 18:01:17 GMT
COPY dir:606cc669e6833afa7967597ca36d4a4497efbb54719c008108649021142d7549 in /usr/local/tomcat 
# Wed, 10 May 2023 18:01:21 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 18:01:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 10 May 2023 18:01:23 GMT
EXPOSE 8080
# Wed, 10 May 2023 18:01:23 GMT
CMD ["catalina.sh" "run"]
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 10 May 2023 18:28:05 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 18:28:06 GMT
ENV XWIKI_VERSION=15.3
# Wed, 10 May 2023 18:28:06 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.3
# Wed, 10 May 2023 18:28:06 GMT
ENV XWIKI_DOWNLOAD_SHA256=fbe35bcc5c6cc5764f2a1da4aca7878531f93bae069d94f399fea7d9656da3b8
# Wed, 10 May 2023 18:28:44 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 10 May 2023 18:28:45 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Wed, 10 May 2023 18:28:45 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Wed, 10 May 2023 18:28:45 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Wed, 10 May 2023 18:28:45 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Wed, 10 May 2023 18:28:45 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Wed, 10 May 2023 18:28:46 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Wed, 10 May 2023 18:28:46 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 10 May 2023 18:28:46 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 10 May 2023 18:28:47 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 10 May 2023 18:28:47 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 10 May 2023 18:28:47 GMT
VOLUME [/usr/local/xwiki]
# Wed, 10 May 2023 18:28:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 May 2023 18:28:47 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458b02b5411a07f3b354cde2b461caffc1bb184a3413b5736a9e67ee87cb28b2`  
		Last Modified: Thu, 04 May 2023 07:30:02 GMT  
		Size: 12.5 MB (12504170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04a165ead1d5eabe89dc88e53286af89caab22a5d20c53007b9e6e508affb4b`  
		Last Modified: Thu, 04 May 2023 07:31:19 GMT  
		Size: 46.7 MB (46666270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1187c73b18505bd4495bc03ccbdb723388dfe4d633fd12be845dfe8e253e48e2`  
		Last Modified: Thu, 04 May 2023 07:31:12 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c833cbb14374cde014505e77f6a6122773984a691844e4138fc15cae99ba625`  
		Last Modified: Thu, 04 May 2023 16:24:19 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439ac04571c77c4330db518bc8f35b70f8723246ed34c98787f7ac8d7dc30b42`  
		Last Modified: Wed, 10 May 2023 18:09:06 GMT  
		Size: 12.2 MB (12236613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8e775ba0b76c6692c0b9211e4b94653ba2aa16fdc7a5e3347aba962b684508`  
		Last Modified: Wed, 10 May 2023 18:09:06 GMT  
		Size: 454.2 KB (454222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee5c1ba4848e97d4e3c43d9d4bca0eeeccf2d5d7f6d805d748da4a7d24ad14e`  
		Last Modified: Wed, 10 May 2023 18:09:05 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffadd10be916fc5729676141f5d0ba6aa30968b75555790e449d4988dc81332a`  
		Last Modified: Wed, 10 May 2023 18:32:42 GMT  
		Size: 178.3 MB (178334017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a29002da219be23e789ef538aeaae1d2296399cdfa64c6c2ed7438210947d7`  
		Last Modified: Wed, 10 May 2023 18:32:34 GMT  
		Size: 306.2 MB (306214302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628263d6dd0a28e03148683703ead7b3c5ef0abd589af1c7352f58aadb9c01a8`  
		Last Modified: Wed, 10 May 2023 18:32:17 GMT  
		Size: 2.3 MB (2343663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81942c3829003d54f85f9d0e3d4fb84d03f7db66060cdd1d2a6a812ce516ccd6`  
		Last Modified: Wed, 10 May 2023 18:32:17 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e635acc63235269abedf51ee8315a58bbb09ff0cbd90f9c6f68c6ea5269d909`  
		Last Modified: Wed, 10 May 2023 18:32:17 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e905c9c0de831ffb2222e8e0420b569e8658457adc3ae299482d6ad73bdb3abb`  
		Last Modified: Wed, 10 May 2023 18:32:17 GMT  
		Size: 6.0 KB (6003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3459a44ee12986d9a54da5b087233e6dfe71171061ce1a63376de231c25ea842`  
		Last Modified: Wed, 10 May 2023 18:32:17 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:latest` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:156f67756ea75d27982bd550fe642c9e9bea5cf04a008f6d3e5af5d2343ca83b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.5 MB (580479573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab46181cab4d5b59fc90bad1883f22f0f812a647a62e801240dfa51c485ed1b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 25 Apr 2023 17:31:58 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:31:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:31:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:31:59 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:32:02 GMT
ADD file:aee0d7770ef2f24dc9697e86d391529d001a4013b6e30a3ac90a57932814a57e in / 
# Tue, 25 Apr 2023 17:32:02 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 03:25:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 03:25:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 03:25:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 03:25:23 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 03:25:47 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 04 May 2023 03:26:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 03:26:10 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 11:14:20 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 04 May 2023 11:14:20 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 11:14:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 04 May 2023 11:14:21 GMT
WORKDIR /usr/local/tomcat
# Thu, 04 May 2023 11:14:21 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 11:14:21 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 11:15:34 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 04 May 2023 11:15:34 GMT
ENV TOMCAT_MAJOR=9
# Wed, 10 May 2023 17:56:49 GMT
ENV TOMCAT_VERSION=9.0.75
# Wed, 10 May 2023 17:56:49 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Wed, 10 May 2023 17:56:49 GMT
COPY dir:2a613f9e425d5febc8be5b6c17f49b39f1b8ad84b1601f07f76abed41b25b24b in /usr/local/tomcat 
# Wed, 10 May 2023 17:56:52 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 17:56:54 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 10 May 2023 17:56:54 GMT
EXPOSE 8080
# Wed, 10 May 2023 17:56:54 GMT
CMD ["catalina.sh" "run"]
# Wed, 10 May 2023 18:22:09 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 10 May 2023 18:23:10 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 18:23:13 GMT
ENV XWIKI_VERSION=15.3
# Wed, 10 May 2023 18:23:13 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.3
# Wed, 10 May 2023 18:23:13 GMT
ENV XWIKI_DOWNLOAD_SHA256=fbe35bcc5c6cc5764f2a1da4aca7878531f93bae069d94f399fea7d9656da3b8
# Wed, 10 May 2023 18:23:53 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 10 May 2023 18:23:55 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Wed, 10 May 2023 18:23:55 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Wed, 10 May 2023 18:23:55 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Wed, 10 May 2023 18:23:56 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Wed, 10 May 2023 18:23:56 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Wed, 10 May 2023 18:23:56 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Wed, 10 May 2023 18:23:56 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 10 May 2023 18:23:57 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 10 May 2023 18:23:57 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 10 May 2023 18:23:57 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 10 May 2023 18:23:57 GMT
VOLUME [/usr/local/xwiki]
# Wed, 10 May 2023 18:23:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 May 2023 18:23:57 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f3f60f415e9a03eed88bd5dd5268c841cde08dacf16911a3ef1e4e0fcdd76568`  
		Last Modified: Wed, 26 Apr 2023 02:08:37 GMT  
		Size: 28.4 MB (28389440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fb3595122d1cb6fffe722e2624c3c89b00776b393256a5444af56ceda691cf`  
		Last Modified: Thu, 04 May 2023 03:28:13 GMT  
		Size: 12.5 MB (12463858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5542665e33e692b672a405517e6e267c4c6e210bc410b97a6a1ce732618caa87`  
		Last Modified: Thu, 04 May 2023 03:29:19 GMT  
		Size: 45.0 MB (45009401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e52b8550f0ced98adb0880bd041e361ffb69810e6071e6d71eb2ec0c8ecfad5`  
		Last Modified: Thu, 04 May 2023 03:29:14 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea5566732e0a920d0a63e4fbebf073d2c49e3f80716df462e73f895cc0c5dfa`  
		Last Modified: Thu, 04 May 2023 11:24:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c6d16bf5ef403ef11a1cc9e40650f402cd1f8269d16982f7daebc2a76ab0d9`  
		Last Modified: Wed, 10 May 2023 18:03:56 GMT  
		Size: 12.2 MB (12242222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eaf464f1c82b5f85e3173b2c732f0928a28e669fcc4af9eb6da48199e92ae50`  
		Last Modified: Wed, 10 May 2023 18:03:55 GMT  
		Size: 453.7 KB (453682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ef5f2b94b25f2b0f609c429cc1626d9dd857d8294d2d872d6595bdeff3a5ca`  
		Last Modified: Wed, 10 May 2023 18:03:55 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7cc67d2dc8f70f6e05051c0e95eb0de93a45de55ba65c355eedaff2bf118e42`  
		Last Modified: Wed, 10 May 2023 18:27:43 GMT  
		Size: 173.4 MB (173350375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321a150ce2c4526d3d3f5be05b00d833ba0d530e3b594708aeda7ef22c1855a3`  
		Last Modified: Wed, 10 May 2023 18:27:39 GMT  
		Size: 306.2 MB (306214312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de8537cceb0f08c97a9244c93c7142180f99d25a07a008c897b3e7f2e01749f5`  
		Last Modified: Wed, 10 May 2023 18:27:25 GMT  
		Size: 2.3 MB (2343667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:174ceadf9884a59c863a2f45bc8a9d2c877073089ab2293ec28b4a890edbd549`  
		Last Modified: Wed, 10 May 2023 18:27:25 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4340d0afded864299aaa098ecb92231c246d875fd05e7babc4eb574c24aba63`  
		Last Modified: Wed, 10 May 2023 18:27:25 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ff6fb98971adf0b973b7c902a39cadccb245e656dc8470ec75d8e115e335c0`  
		Last Modified: Wed, 10 May 2023 18:27:25 GMT  
		Size: 6.0 KB (6000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e40c1aaebc8527a9ad709da10958451577ca896b6c968e0e49daf1cc4f790ddd`  
		Last Modified: Wed, 10 May 2023 18:27:25 GMT  
		Size: 2.5 KB (2503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:lts`

```console
$ docker pull xwiki@sha256:3cb3e791882b8ad6819d53ac0e7fb6c678ba6435b06061929dca6ce1a98fbef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:lts` - linux; amd64

```console
$ docker pull xwiki@sha256:8d0ae8c6e385bf7493b07cbab2a2afa371e97538db4f1c040a18c393b5d1e090
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.2 MB (590232292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eff782e5d932a0d40c015b5812ebe948e85c30648a4875e24e6320a36ebb037b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 07:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 07:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 07:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 07:26:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:27:16 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 04 May 2023 07:27:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 07:27:40 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 16:13:14 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 04 May 2023 16:13:14 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 16:13:14 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 04 May 2023 16:13:14 GMT
WORKDIR /usr/local/tomcat
# Thu, 04 May 2023 16:13:14 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 16:13:15 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 16:14:45 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 04 May 2023 16:14:45 GMT
ENV TOMCAT_MAJOR=9
# Wed, 10 May 2023 18:01:17 GMT
ENV TOMCAT_VERSION=9.0.75
# Wed, 10 May 2023 18:01:17 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Wed, 10 May 2023 18:01:17 GMT
COPY dir:606cc669e6833afa7967597ca36d4a4497efbb54719c008108649021142d7549 in /usr/local/tomcat 
# Wed, 10 May 2023 18:01:21 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 18:01:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 10 May 2023 18:01:23 GMT
EXPOSE 8080
# Wed, 10 May 2023 18:01:23 GMT
CMD ["catalina.sh" "run"]
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 10 May 2023 18:28:05 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 24 May 2023 22:47:42 GMT
ENV XWIKI_VERSION=14.10.11
# Wed, 24 May 2023 22:47:42 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.11
# Wed, 24 May 2023 22:47:42 GMT
ENV XWIKI_DOWNLOAD_SHA256=0804bdbc2a4eb370a25cfcd9a2185e80e007180007d15fdaa4d371dbd02b5d43
# Wed, 24 May 2023 22:48:21 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 24 May 2023 22:48:22 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Wed, 24 May 2023 22:48:22 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Wed, 24 May 2023 22:48:22 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Wed, 24 May 2023 22:48:22 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Wed, 24 May 2023 22:48:22 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Wed, 24 May 2023 22:48:23 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Wed, 24 May 2023 22:48:23 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 24 May 2023 22:48:23 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 24 May 2023 22:48:23 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 24 May 2023 22:48:24 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 24 May 2023 22:48:24 GMT
VOLUME [/usr/local/xwiki]
# Wed, 24 May 2023 22:48:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 May 2023 22:48:24 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458b02b5411a07f3b354cde2b461caffc1bb184a3413b5736a9e67ee87cb28b2`  
		Last Modified: Thu, 04 May 2023 07:30:02 GMT  
		Size: 12.5 MB (12504170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04a165ead1d5eabe89dc88e53286af89caab22a5d20c53007b9e6e508affb4b`  
		Last Modified: Thu, 04 May 2023 07:31:19 GMT  
		Size: 46.7 MB (46666270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1187c73b18505bd4495bc03ccbdb723388dfe4d633fd12be845dfe8e253e48e2`  
		Last Modified: Thu, 04 May 2023 07:31:12 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c833cbb14374cde014505e77f6a6122773984a691844e4138fc15cae99ba625`  
		Last Modified: Thu, 04 May 2023 16:24:19 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439ac04571c77c4330db518bc8f35b70f8723246ed34c98787f7ac8d7dc30b42`  
		Last Modified: Wed, 10 May 2023 18:09:06 GMT  
		Size: 12.2 MB (12236613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8e775ba0b76c6692c0b9211e4b94653ba2aa16fdc7a5e3347aba962b684508`  
		Last Modified: Wed, 10 May 2023 18:09:06 GMT  
		Size: 454.2 KB (454222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee5c1ba4848e97d4e3c43d9d4bca0eeeccf2d5d7f6d805d748da4a7d24ad14e`  
		Last Modified: Wed, 10 May 2023 18:09:05 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffadd10be916fc5729676141f5d0ba6aa30968b75555790e449d4988dc81332a`  
		Last Modified: Wed, 10 May 2023 18:32:42 GMT  
		Size: 178.3 MB (178334017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3968819bf3a63424c2b6a4e9591f0c9e6ffbb99a92e0c8d8bb65c67dee37c591`  
		Last Modified: Wed, 24 May 2023 22:50:04 GMT  
		Size: 307.3 MB (307250466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab4c543f2a230baf4ee559f04be553bc00d7b77cc356fee1f21587123cb6977`  
		Last Modified: Wed, 24 May 2023 22:49:49 GMT  
		Size: 2.3 MB (2343680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22684cbd7ece18edde12615b426a6542f278c82ffebfd4d0e88ef0ff8fbde0b`  
		Last Modified: Wed, 24 May 2023 22:49:48 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5270a8761eb66f6e2d094c0879e26935456fa9e19b282bbed9418b58631140c1`  
		Last Modified: Wed, 24 May 2023 22:49:48 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efce4adb2bae1b274febb0d3785c785befb8c4de6c50df158a2aa23673c5b60d`  
		Last Modified: Wed, 24 May 2023 22:49:48 GMT  
		Size: 6.0 KB (6017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9715a623bab854429c5628dcca4718382ada25dbc334b3d61b24a46031cd5d44`  
		Last Modified: Wed, 24 May 2023 22:49:48 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:lts` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:15957635ec1e31779c981c0817bf66a72c04e6218e1acc75ef471fc7f46dd01c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.5 MB (581515826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aa7648bbd0225e907a6fd992596c1aedb9a12baa3eb30a4a458df9d4af79c91`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 25 Apr 2023 17:31:58 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:31:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:31:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:31:59 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:32:02 GMT
ADD file:aee0d7770ef2f24dc9697e86d391529d001a4013b6e30a3ac90a57932814a57e in / 
# Tue, 25 Apr 2023 17:32:02 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 03:25:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 03:25:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 03:25:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 03:25:23 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 03:25:47 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 04 May 2023 03:26:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 03:26:10 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 11:14:20 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 04 May 2023 11:14:20 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 11:14:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 04 May 2023 11:14:21 GMT
WORKDIR /usr/local/tomcat
# Thu, 04 May 2023 11:14:21 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 11:14:21 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 11:15:34 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 04 May 2023 11:15:34 GMT
ENV TOMCAT_MAJOR=9
# Wed, 10 May 2023 17:56:49 GMT
ENV TOMCAT_VERSION=9.0.75
# Wed, 10 May 2023 17:56:49 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Wed, 10 May 2023 17:56:49 GMT
COPY dir:2a613f9e425d5febc8be5b6c17f49b39f1b8ad84b1601f07f76abed41b25b24b in /usr/local/tomcat 
# Wed, 10 May 2023 17:56:52 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 17:56:54 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 10 May 2023 17:56:54 GMT
EXPOSE 8080
# Wed, 10 May 2023 17:56:54 GMT
CMD ["catalina.sh" "run"]
# Wed, 10 May 2023 18:22:09 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 10 May 2023 18:23:10 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 24 May 2023 23:08:47 GMT
ENV XWIKI_VERSION=14.10.11
# Wed, 24 May 2023 23:08:47 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.11
# Wed, 24 May 2023 23:08:48 GMT
ENV XWIKI_DOWNLOAD_SHA256=0804bdbc2a4eb370a25cfcd9a2185e80e007180007d15fdaa4d371dbd02b5d43
# Wed, 24 May 2023 23:09:27 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 24 May 2023 23:09:29 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Wed, 24 May 2023 23:09:29 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Wed, 24 May 2023 23:09:30 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Wed, 24 May 2023 23:09:30 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Wed, 24 May 2023 23:09:30 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Wed, 24 May 2023 23:09:31 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Wed, 24 May 2023 23:09:31 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 24 May 2023 23:09:31 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 24 May 2023 23:09:31 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 24 May 2023 23:09:31 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 24 May 2023 23:09:32 GMT
VOLUME [/usr/local/xwiki]
# Wed, 24 May 2023 23:09:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 May 2023 23:09:32 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f3f60f415e9a03eed88bd5dd5268c841cde08dacf16911a3ef1e4e0fcdd76568`  
		Last Modified: Wed, 26 Apr 2023 02:08:37 GMT  
		Size: 28.4 MB (28389440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fb3595122d1cb6fffe722e2624c3c89b00776b393256a5444af56ceda691cf`  
		Last Modified: Thu, 04 May 2023 03:28:13 GMT  
		Size: 12.5 MB (12463858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5542665e33e692b672a405517e6e267c4c6e210bc410b97a6a1ce732618caa87`  
		Last Modified: Thu, 04 May 2023 03:29:19 GMT  
		Size: 45.0 MB (45009401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e52b8550f0ced98adb0880bd041e361ffb69810e6071e6d71eb2ec0c8ecfad5`  
		Last Modified: Thu, 04 May 2023 03:29:14 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea5566732e0a920d0a63e4fbebf073d2c49e3f80716df462e73f895cc0c5dfa`  
		Last Modified: Thu, 04 May 2023 11:24:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c6d16bf5ef403ef11a1cc9e40650f402cd1f8269d16982f7daebc2a76ab0d9`  
		Last Modified: Wed, 10 May 2023 18:03:56 GMT  
		Size: 12.2 MB (12242222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eaf464f1c82b5f85e3173b2c732f0928a28e669fcc4af9eb6da48199e92ae50`  
		Last Modified: Wed, 10 May 2023 18:03:55 GMT  
		Size: 453.7 KB (453682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ef5f2b94b25f2b0f609c429cc1626d9dd857d8294d2d872d6595bdeff3a5ca`  
		Last Modified: Wed, 10 May 2023 18:03:55 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7cc67d2dc8f70f6e05051c0e95eb0de93a45de55ba65c355eedaff2bf118e42`  
		Last Modified: Wed, 10 May 2023 18:27:43 GMT  
		Size: 173.4 MB (173350375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0f918d67c923bb6ad20257659a178cf82a52dbd68eda4c094eb3fb372831c2c`  
		Last Modified: Wed, 24 May 2023 23:11:04 GMT  
		Size: 307.3 MB (307250539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced4cf6fb2a03eefd5f5bf442bda27c93928535469b7e8d6fc9c5d7b5ae30b2f`  
		Last Modified: Wed, 24 May 2023 23:10:51 GMT  
		Size: 2.3 MB (2343677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98623f72442cf00c262363a201209a0aa274f36c3ea6fc9f6982e636f879fa70`  
		Last Modified: Wed, 24 May 2023 23:10:50 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7788f555a977b55dd4bb3cc03f0877839200ef650618e788503063bad30080ce`  
		Last Modified: Wed, 24 May 2023 23:10:50 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874c98264dbb8128fd9c27e97654851dfbde45dfb396778744d7616b44591eae`  
		Last Modified: Wed, 24 May 2023 23:10:50 GMT  
		Size: 6.0 KB (6014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee9de251f061dd4ab29b65e5807e482de72b8f045af577bdc2ade102cedf52d`  
		Last Modified: Wed, 24 May 2023 23:10:50 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:lts-mariadb`

```console
$ docker pull xwiki@sha256:c1da5ed330d5ca59735d572da388f3a2ce1fbbaf48e03de0b7d0799d1626c0ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:lts-mariadb` - linux; amd64

```console
$ docker pull xwiki@sha256:1a75db7f8992a7c4ee2c526aa1a525456625e7a8d132487a30b4db9e5a4d63eb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **588.5 MB (588483181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c4b7b90fa36f2254d9a63b8f50fc26caa9e6bf856d9a1b53f83db9206d899d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 07:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 07:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 07:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 07:26:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:27:16 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 04 May 2023 07:27:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 07:27:40 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 16:13:14 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 04 May 2023 16:13:14 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 16:13:14 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 04 May 2023 16:13:14 GMT
WORKDIR /usr/local/tomcat
# Thu, 04 May 2023 16:13:14 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 16:13:15 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 16:14:45 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 04 May 2023 16:14:45 GMT
ENV TOMCAT_MAJOR=9
# Wed, 10 May 2023 18:01:17 GMT
ENV TOMCAT_VERSION=9.0.75
# Wed, 10 May 2023 18:01:17 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Wed, 10 May 2023 18:01:17 GMT
COPY dir:606cc669e6833afa7967597ca36d4a4497efbb54719c008108649021142d7549 in /usr/local/tomcat 
# Wed, 10 May 2023 18:01:21 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 18:01:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 10 May 2023 18:01:23 GMT
EXPOSE 8080
# Wed, 10 May 2023 18:01:23 GMT
CMD ["catalina.sh" "run"]
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 10 May 2023 18:28:05 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 24 May 2023 22:47:42 GMT
ENV XWIKI_VERSION=14.10.11
# Wed, 24 May 2023 22:47:42 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.11
# Wed, 24 May 2023 22:47:42 GMT
ENV XWIKI_DOWNLOAD_SHA256=0804bdbc2a4eb370a25cfcd9a2185e80e007180007d15fdaa4d371dbd02b5d43
# Wed, 24 May 2023 22:48:21 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 24 May 2023 22:49:20 GMT
ENV MARIADB_JDBC_VERSION=3.1.4
# Wed, 24 May 2023 22:49:20 GMT
ENV MARIADB_JDBC_SHA256=eb88b5d727d82e25117e2b6fabcec1daf734633b0a576456c73215884c189ad4
# Wed, 24 May 2023 22:49:20 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.1.4
# Wed, 24 May 2023 22:49:20 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.1.4.jar
# Wed, 24 May 2023 22:49:20 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.1.4.jar
# Wed, 24 May 2023 22:49:21 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Wed, 24 May 2023 22:49:21 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 24 May 2023 22:49:21 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 24 May 2023 22:49:22 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 24 May 2023 22:49:22 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 24 May 2023 22:49:22 GMT
VOLUME [/usr/local/xwiki]
# Wed, 24 May 2023 22:49:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 May 2023 22:49:22 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458b02b5411a07f3b354cde2b461caffc1bb184a3413b5736a9e67ee87cb28b2`  
		Last Modified: Thu, 04 May 2023 07:30:02 GMT  
		Size: 12.5 MB (12504170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04a165ead1d5eabe89dc88e53286af89caab22a5d20c53007b9e6e508affb4b`  
		Last Modified: Thu, 04 May 2023 07:31:19 GMT  
		Size: 46.7 MB (46666270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1187c73b18505bd4495bc03ccbdb723388dfe4d633fd12be845dfe8e253e48e2`  
		Last Modified: Thu, 04 May 2023 07:31:12 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c833cbb14374cde014505e77f6a6122773984a691844e4138fc15cae99ba625`  
		Last Modified: Thu, 04 May 2023 16:24:19 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439ac04571c77c4330db518bc8f35b70f8723246ed34c98787f7ac8d7dc30b42`  
		Last Modified: Wed, 10 May 2023 18:09:06 GMT  
		Size: 12.2 MB (12236613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8e775ba0b76c6692c0b9211e4b94653ba2aa16fdc7a5e3347aba962b684508`  
		Last Modified: Wed, 10 May 2023 18:09:06 GMT  
		Size: 454.2 KB (454222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee5c1ba4848e97d4e3c43d9d4bca0eeeccf2d5d7f6d805d748da4a7d24ad14e`  
		Last Modified: Wed, 10 May 2023 18:09:05 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffadd10be916fc5729676141f5d0ba6aa30968b75555790e449d4988dc81332a`  
		Last Modified: Wed, 10 May 2023 18:32:42 GMT  
		Size: 178.3 MB (178334017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3968819bf3a63424c2b6a4e9591f0c9e6ffbb99a92e0c8d8bb65c67dee37c591`  
		Last Modified: Wed, 24 May 2023 22:50:04 GMT  
		Size: 307.3 MB (307250466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe65a2b1c269931f9affdbf4926be3a7e6789a0eb5ef5c8469c0ab01708aa54e`  
		Last Modified: Wed, 24 May 2023 22:51:02 GMT  
		Size: 594.6 KB (594559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b1b0dad9556a98d3e225960bc3fdd9550ee0d50cc15b4667535a69cc8cc4f5`  
		Last Modified: Wed, 24 May 2023 22:51:02 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b44a0baefcddcca335cf3e635a10b22f472dcb576dfa3b75755f9db5fc9ec853`  
		Last Modified: Wed, 24 May 2023 22:51:02 GMT  
		Size: 2.3 KB (2313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ebfb8ffc93a8da62fdc799b946b53ae557f1061d920db81d002a7fea3bacbde`  
		Last Modified: Wed, 24 May 2023 22:51:02 GMT  
		Size: 6.0 KB (6019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f48b704e13efa0bd740446998f3193c87fcb7dadc14138af9f9103fdbdcdc87`  
		Last Modified: Wed, 24 May 2023 22:51:02 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:lts-mariadb` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:00f5266daef25dc10485eca8533381e175b534a692a79b5e108b3563b604c1a5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.8 MB (579766697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e448e5a8cc6e1fb57ca6ebb008b4fa70de9683b31e4f558bd222f5a5fd0b441f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 25 Apr 2023 17:31:58 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:31:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:31:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:31:59 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:32:02 GMT
ADD file:aee0d7770ef2f24dc9697e86d391529d001a4013b6e30a3ac90a57932814a57e in / 
# Tue, 25 Apr 2023 17:32:02 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 03:25:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 03:25:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 03:25:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 03:25:23 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 03:25:47 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 04 May 2023 03:26:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 03:26:10 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 11:14:20 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 04 May 2023 11:14:20 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 11:14:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 04 May 2023 11:14:21 GMT
WORKDIR /usr/local/tomcat
# Thu, 04 May 2023 11:14:21 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 11:14:21 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 11:15:34 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 04 May 2023 11:15:34 GMT
ENV TOMCAT_MAJOR=9
# Wed, 10 May 2023 17:56:49 GMT
ENV TOMCAT_VERSION=9.0.75
# Wed, 10 May 2023 17:56:49 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Wed, 10 May 2023 17:56:49 GMT
COPY dir:2a613f9e425d5febc8be5b6c17f49b39f1b8ad84b1601f07f76abed41b25b24b in /usr/local/tomcat 
# Wed, 10 May 2023 17:56:52 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 17:56:54 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 10 May 2023 17:56:54 GMT
EXPOSE 8080
# Wed, 10 May 2023 17:56:54 GMT
CMD ["catalina.sh" "run"]
# Wed, 10 May 2023 18:22:09 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 10 May 2023 18:23:10 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 24 May 2023 23:08:47 GMT
ENV XWIKI_VERSION=14.10.11
# Wed, 24 May 2023 23:08:47 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.11
# Wed, 24 May 2023 23:08:48 GMT
ENV XWIKI_DOWNLOAD_SHA256=0804bdbc2a4eb370a25cfcd9a2185e80e007180007d15fdaa4d371dbd02b5d43
# Wed, 24 May 2023 23:09:27 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 24 May 2023 23:10:23 GMT
ENV MARIADB_JDBC_VERSION=3.1.4
# Wed, 24 May 2023 23:10:23 GMT
ENV MARIADB_JDBC_SHA256=eb88b5d727d82e25117e2b6fabcec1daf734633b0a576456c73215884c189ad4
# Wed, 24 May 2023 23:10:23 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.1.4
# Wed, 24 May 2023 23:10:23 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.1.4.jar
# Wed, 24 May 2023 23:10:23 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.1.4.jar
# Wed, 24 May 2023 23:10:24 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Wed, 24 May 2023 23:10:24 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 24 May 2023 23:10:24 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 24 May 2023 23:10:25 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 24 May 2023 23:10:25 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 24 May 2023 23:10:25 GMT
VOLUME [/usr/local/xwiki]
# Wed, 24 May 2023 23:10:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 May 2023 23:10:25 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f3f60f415e9a03eed88bd5dd5268c841cde08dacf16911a3ef1e4e0fcdd76568`  
		Last Modified: Wed, 26 Apr 2023 02:08:37 GMT  
		Size: 28.4 MB (28389440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fb3595122d1cb6fffe722e2624c3c89b00776b393256a5444af56ceda691cf`  
		Last Modified: Thu, 04 May 2023 03:28:13 GMT  
		Size: 12.5 MB (12463858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5542665e33e692b672a405517e6e267c4c6e210bc410b97a6a1ce732618caa87`  
		Last Modified: Thu, 04 May 2023 03:29:19 GMT  
		Size: 45.0 MB (45009401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e52b8550f0ced98adb0880bd041e361ffb69810e6071e6d71eb2ec0c8ecfad5`  
		Last Modified: Thu, 04 May 2023 03:29:14 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea5566732e0a920d0a63e4fbebf073d2c49e3f80716df462e73f895cc0c5dfa`  
		Last Modified: Thu, 04 May 2023 11:24:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c6d16bf5ef403ef11a1cc9e40650f402cd1f8269d16982f7daebc2a76ab0d9`  
		Last Modified: Wed, 10 May 2023 18:03:56 GMT  
		Size: 12.2 MB (12242222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eaf464f1c82b5f85e3173b2c732f0928a28e669fcc4af9eb6da48199e92ae50`  
		Last Modified: Wed, 10 May 2023 18:03:55 GMT  
		Size: 453.7 KB (453682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ef5f2b94b25f2b0f609c429cc1626d9dd857d8294d2d872d6595bdeff3a5ca`  
		Last Modified: Wed, 10 May 2023 18:03:55 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7cc67d2dc8f70f6e05051c0e95eb0de93a45de55ba65c355eedaff2bf118e42`  
		Last Modified: Wed, 10 May 2023 18:27:43 GMT  
		Size: 173.4 MB (173350375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0f918d67c923bb6ad20257659a178cf82a52dbd68eda4c094eb3fb372831c2c`  
		Last Modified: Wed, 24 May 2023 23:11:04 GMT  
		Size: 307.3 MB (307250539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d912a3a12e11af60d952ffa7ac5359c7aa515a7300f75c5ba871ea94e62bd43`  
		Last Modified: Wed, 24 May 2023 23:12:02 GMT  
		Size: 594.5 KB (594549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f871b4dce32a1e7dcce9033dac703bc174253e8b26f41ea7a7d4c4ae1d98372f`  
		Last Modified: Wed, 24 May 2023 23:12:02 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f1d5bccd3396b98e1cf536def6525a295c0a35c6c70a438fc6a917b322efd5f`  
		Last Modified: Wed, 24 May 2023 23:12:02 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b11946e15dcff3a5243af68d7416f684d866731eedb590452d184678df469e`  
		Last Modified: Wed, 24 May 2023 23:12:02 GMT  
		Size: 6.0 KB (6013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33aa2a2a6531b6d4ff0f2638634bbb0a42a3796e25d026234551deb2add3b637`  
		Last Modified: Wed, 24 May 2023 23:12:02 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:lts-mariadb-tomcat`

```console
$ docker pull xwiki@sha256:c1da5ed330d5ca59735d572da388f3a2ce1fbbaf48e03de0b7d0799d1626c0ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:lts-mariadb-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:1a75db7f8992a7c4ee2c526aa1a525456625e7a8d132487a30b4db9e5a4d63eb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **588.5 MB (588483181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c4b7b90fa36f2254d9a63b8f50fc26caa9e6bf856d9a1b53f83db9206d899d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 07:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 07:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 07:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 07:26:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:27:16 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 04 May 2023 07:27:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 07:27:40 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 16:13:14 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 04 May 2023 16:13:14 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 16:13:14 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 04 May 2023 16:13:14 GMT
WORKDIR /usr/local/tomcat
# Thu, 04 May 2023 16:13:14 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 16:13:15 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 16:14:45 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 04 May 2023 16:14:45 GMT
ENV TOMCAT_MAJOR=9
# Wed, 10 May 2023 18:01:17 GMT
ENV TOMCAT_VERSION=9.0.75
# Wed, 10 May 2023 18:01:17 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Wed, 10 May 2023 18:01:17 GMT
COPY dir:606cc669e6833afa7967597ca36d4a4497efbb54719c008108649021142d7549 in /usr/local/tomcat 
# Wed, 10 May 2023 18:01:21 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 18:01:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 10 May 2023 18:01:23 GMT
EXPOSE 8080
# Wed, 10 May 2023 18:01:23 GMT
CMD ["catalina.sh" "run"]
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 10 May 2023 18:28:05 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 24 May 2023 22:47:42 GMT
ENV XWIKI_VERSION=14.10.11
# Wed, 24 May 2023 22:47:42 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.11
# Wed, 24 May 2023 22:47:42 GMT
ENV XWIKI_DOWNLOAD_SHA256=0804bdbc2a4eb370a25cfcd9a2185e80e007180007d15fdaa4d371dbd02b5d43
# Wed, 24 May 2023 22:48:21 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 24 May 2023 22:49:20 GMT
ENV MARIADB_JDBC_VERSION=3.1.4
# Wed, 24 May 2023 22:49:20 GMT
ENV MARIADB_JDBC_SHA256=eb88b5d727d82e25117e2b6fabcec1daf734633b0a576456c73215884c189ad4
# Wed, 24 May 2023 22:49:20 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.1.4
# Wed, 24 May 2023 22:49:20 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.1.4.jar
# Wed, 24 May 2023 22:49:20 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.1.4.jar
# Wed, 24 May 2023 22:49:21 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Wed, 24 May 2023 22:49:21 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 24 May 2023 22:49:21 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 24 May 2023 22:49:22 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 24 May 2023 22:49:22 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 24 May 2023 22:49:22 GMT
VOLUME [/usr/local/xwiki]
# Wed, 24 May 2023 22:49:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 May 2023 22:49:22 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458b02b5411a07f3b354cde2b461caffc1bb184a3413b5736a9e67ee87cb28b2`  
		Last Modified: Thu, 04 May 2023 07:30:02 GMT  
		Size: 12.5 MB (12504170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04a165ead1d5eabe89dc88e53286af89caab22a5d20c53007b9e6e508affb4b`  
		Last Modified: Thu, 04 May 2023 07:31:19 GMT  
		Size: 46.7 MB (46666270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1187c73b18505bd4495bc03ccbdb723388dfe4d633fd12be845dfe8e253e48e2`  
		Last Modified: Thu, 04 May 2023 07:31:12 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c833cbb14374cde014505e77f6a6122773984a691844e4138fc15cae99ba625`  
		Last Modified: Thu, 04 May 2023 16:24:19 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439ac04571c77c4330db518bc8f35b70f8723246ed34c98787f7ac8d7dc30b42`  
		Last Modified: Wed, 10 May 2023 18:09:06 GMT  
		Size: 12.2 MB (12236613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8e775ba0b76c6692c0b9211e4b94653ba2aa16fdc7a5e3347aba962b684508`  
		Last Modified: Wed, 10 May 2023 18:09:06 GMT  
		Size: 454.2 KB (454222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee5c1ba4848e97d4e3c43d9d4bca0eeeccf2d5d7f6d805d748da4a7d24ad14e`  
		Last Modified: Wed, 10 May 2023 18:09:05 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffadd10be916fc5729676141f5d0ba6aa30968b75555790e449d4988dc81332a`  
		Last Modified: Wed, 10 May 2023 18:32:42 GMT  
		Size: 178.3 MB (178334017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3968819bf3a63424c2b6a4e9591f0c9e6ffbb99a92e0c8d8bb65c67dee37c591`  
		Last Modified: Wed, 24 May 2023 22:50:04 GMT  
		Size: 307.3 MB (307250466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe65a2b1c269931f9affdbf4926be3a7e6789a0eb5ef5c8469c0ab01708aa54e`  
		Last Modified: Wed, 24 May 2023 22:51:02 GMT  
		Size: 594.6 KB (594559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b1b0dad9556a98d3e225960bc3fdd9550ee0d50cc15b4667535a69cc8cc4f5`  
		Last Modified: Wed, 24 May 2023 22:51:02 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b44a0baefcddcca335cf3e635a10b22f472dcb576dfa3b75755f9db5fc9ec853`  
		Last Modified: Wed, 24 May 2023 22:51:02 GMT  
		Size: 2.3 KB (2313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ebfb8ffc93a8da62fdc799b946b53ae557f1061d920db81d002a7fea3bacbde`  
		Last Modified: Wed, 24 May 2023 22:51:02 GMT  
		Size: 6.0 KB (6019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f48b704e13efa0bd740446998f3193c87fcb7dadc14138af9f9103fdbdcdc87`  
		Last Modified: Wed, 24 May 2023 22:51:02 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:lts-mariadb-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:00f5266daef25dc10485eca8533381e175b534a692a79b5e108b3563b604c1a5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.8 MB (579766697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e448e5a8cc6e1fb57ca6ebb008b4fa70de9683b31e4f558bd222f5a5fd0b441f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 25 Apr 2023 17:31:58 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:31:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:31:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:31:59 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:32:02 GMT
ADD file:aee0d7770ef2f24dc9697e86d391529d001a4013b6e30a3ac90a57932814a57e in / 
# Tue, 25 Apr 2023 17:32:02 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 03:25:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 03:25:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 03:25:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 03:25:23 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 03:25:47 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 04 May 2023 03:26:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 03:26:10 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 11:14:20 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 04 May 2023 11:14:20 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 11:14:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 04 May 2023 11:14:21 GMT
WORKDIR /usr/local/tomcat
# Thu, 04 May 2023 11:14:21 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 11:14:21 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 11:15:34 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 04 May 2023 11:15:34 GMT
ENV TOMCAT_MAJOR=9
# Wed, 10 May 2023 17:56:49 GMT
ENV TOMCAT_VERSION=9.0.75
# Wed, 10 May 2023 17:56:49 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Wed, 10 May 2023 17:56:49 GMT
COPY dir:2a613f9e425d5febc8be5b6c17f49b39f1b8ad84b1601f07f76abed41b25b24b in /usr/local/tomcat 
# Wed, 10 May 2023 17:56:52 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 17:56:54 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 10 May 2023 17:56:54 GMT
EXPOSE 8080
# Wed, 10 May 2023 17:56:54 GMT
CMD ["catalina.sh" "run"]
# Wed, 10 May 2023 18:22:09 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 10 May 2023 18:23:10 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 24 May 2023 23:08:47 GMT
ENV XWIKI_VERSION=14.10.11
# Wed, 24 May 2023 23:08:47 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.11
# Wed, 24 May 2023 23:08:48 GMT
ENV XWIKI_DOWNLOAD_SHA256=0804bdbc2a4eb370a25cfcd9a2185e80e007180007d15fdaa4d371dbd02b5d43
# Wed, 24 May 2023 23:09:27 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 24 May 2023 23:10:23 GMT
ENV MARIADB_JDBC_VERSION=3.1.4
# Wed, 24 May 2023 23:10:23 GMT
ENV MARIADB_JDBC_SHA256=eb88b5d727d82e25117e2b6fabcec1daf734633b0a576456c73215884c189ad4
# Wed, 24 May 2023 23:10:23 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.1.4
# Wed, 24 May 2023 23:10:23 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.1.4.jar
# Wed, 24 May 2023 23:10:23 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.1.4.jar
# Wed, 24 May 2023 23:10:24 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Wed, 24 May 2023 23:10:24 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 24 May 2023 23:10:24 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 24 May 2023 23:10:25 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 24 May 2023 23:10:25 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 24 May 2023 23:10:25 GMT
VOLUME [/usr/local/xwiki]
# Wed, 24 May 2023 23:10:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 May 2023 23:10:25 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f3f60f415e9a03eed88bd5dd5268c841cde08dacf16911a3ef1e4e0fcdd76568`  
		Last Modified: Wed, 26 Apr 2023 02:08:37 GMT  
		Size: 28.4 MB (28389440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fb3595122d1cb6fffe722e2624c3c89b00776b393256a5444af56ceda691cf`  
		Last Modified: Thu, 04 May 2023 03:28:13 GMT  
		Size: 12.5 MB (12463858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5542665e33e692b672a405517e6e267c4c6e210bc410b97a6a1ce732618caa87`  
		Last Modified: Thu, 04 May 2023 03:29:19 GMT  
		Size: 45.0 MB (45009401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e52b8550f0ced98adb0880bd041e361ffb69810e6071e6d71eb2ec0c8ecfad5`  
		Last Modified: Thu, 04 May 2023 03:29:14 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea5566732e0a920d0a63e4fbebf073d2c49e3f80716df462e73f895cc0c5dfa`  
		Last Modified: Thu, 04 May 2023 11:24:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c6d16bf5ef403ef11a1cc9e40650f402cd1f8269d16982f7daebc2a76ab0d9`  
		Last Modified: Wed, 10 May 2023 18:03:56 GMT  
		Size: 12.2 MB (12242222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eaf464f1c82b5f85e3173b2c732f0928a28e669fcc4af9eb6da48199e92ae50`  
		Last Modified: Wed, 10 May 2023 18:03:55 GMT  
		Size: 453.7 KB (453682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ef5f2b94b25f2b0f609c429cc1626d9dd857d8294d2d872d6595bdeff3a5ca`  
		Last Modified: Wed, 10 May 2023 18:03:55 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7cc67d2dc8f70f6e05051c0e95eb0de93a45de55ba65c355eedaff2bf118e42`  
		Last Modified: Wed, 10 May 2023 18:27:43 GMT  
		Size: 173.4 MB (173350375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0f918d67c923bb6ad20257659a178cf82a52dbd68eda4c094eb3fb372831c2c`  
		Last Modified: Wed, 24 May 2023 23:11:04 GMT  
		Size: 307.3 MB (307250539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d912a3a12e11af60d952ffa7ac5359c7aa515a7300f75c5ba871ea94e62bd43`  
		Last Modified: Wed, 24 May 2023 23:12:02 GMT  
		Size: 594.5 KB (594549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f871b4dce32a1e7dcce9033dac703bc174253e8b26f41ea7a7d4c4ae1d98372f`  
		Last Modified: Wed, 24 May 2023 23:12:02 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f1d5bccd3396b98e1cf536def6525a295c0a35c6c70a438fc6a917b322efd5f`  
		Last Modified: Wed, 24 May 2023 23:12:02 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b11946e15dcff3a5243af68d7416f684d866731eedb590452d184678df469e`  
		Last Modified: Wed, 24 May 2023 23:12:02 GMT  
		Size: 6.0 KB (6013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33aa2a2a6531b6d4ff0f2638634bbb0a42a3796e25d026234551deb2add3b637`  
		Last Modified: Wed, 24 May 2023 23:12:02 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:lts-mysql`

```console
$ docker pull xwiki@sha256:3cb3e791882b8ad6819d53ac0e7fb6c678ba6435b06061929dca6ce1a98fbef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:lts-mysql` - linux; amd64

```console
$ docker pull xwiki@sha256:8d0ae8c6e385bf7493b07cbab2a2afa371e97538db4f1c040a18c393b5d1e090
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.2 MB (590232292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eff782e5d932a0d40c015b5812ebe948e85c30648a4875e24e6320a36ebb037b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 07:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 07:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 07:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 07:26:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:27:16 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 04 May 2023 07:27:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 07:27:40 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 16:13:14 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 04 May 2023 16:13:14 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 16:13:14 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 04 May 2023 16:13:14 GMT
WORKDIR /usr/local/tomcat
# Thu, 04 May 2023 16:13:14 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 16:13:15 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 16:14:45 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 04 May 2023 16:14:45 GMT
ENV TOMCAT_MAJOR=9
# Wed, 10 May 2023 18:01:17 GMT
ENV TOMCAT_VERSION=9.0.75
# Wed, 10 May 2023 18:01:17 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Wed, 10 May 2023 18:01:17 GMT
COPY dir:606cc669e6833afa7967597ca36d4a4497efbb54719c008108649021142d7549 in /usr/local/tomcat 
# Wed, 10 May 2023 18:01:21 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 18:01:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 10 May 2023 18:01:23 GMT
EXPOSE 8080
# Wed, 10 May 2023 18:01:23 GMT
CMD ["catalina.sh" "run"]
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 10 May 2023 18:28:05 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 24 May 2023 22:47:42 GMT
ENV XWIKI_VERSION=14.10.11
# Wed, 24 May 2023 22:47:42 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.11
# Wed, 24 May 2023 22:47:42 GMT
ENV XWIKI_DOWNLOAD_SHA256=0804bdbc2a4eb370a25cfcd9a2185e80e007180007d15fdaa4d371dbd02b5d43
# Wed, 24 May 2023 22:48:21 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 24 May 2023 22:48:22 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Wed, 24 May 2023 22:48:22 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Wed, 24 May 2023 22:48:22 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Wed, 24 May 2023 22:48:22 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Wed, 24 May 2023 22:48:22 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Wed, 24 May 2023 22:48:23 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Wed, 24 May 2023 22:48:23 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 24 May 2023 22:48:23 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 24 May 2023 22:48:23 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 24 May 2023 22:48:24 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 24 May 2023 22:48:24 GMT
VOLUME [/usr/local/xwiki]
# Wed, 24 May 2023 22:48:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 May 2023 22:48:24 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458b02b5411a07f3b354cde2b461caffc1bb184a3413b5736a9e67ee87cb28b2`  
		Last Modified: Thu, 04 May 2023 07:30:02 GMT  
		Size: 12.5 MB (12504170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04a165ead1d5eabe89dc88e53286af89caab22a5d20c53007b9e6e508affb4b`  
		Last Modified: Thu, 04 May 2023 07:31:19 GMT  
		Size: 46.7 MB (46666270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1187c73b18505bd4495bc03ccbdb723388dfe4d633fd12be845dfe8e253e48e2`  
		Last Modified: Thu, 04 May 2023 07:31:12 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c833cbb14374cde014505e77f6a6122773984a691844e4138fc15cae99ba625`  
		Last Modified: Thu, 04 May 2023 16:24:19 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439ac04571c77c4330db518bc8f35b70f8723246ed34c98787f7ac8d7dc30b42`  
		Last Modified: Wed, 10 May 2023 18:09:06 GMT  
		Size: 12.2 MB (12236613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8e775ba0b76c6692c0b9211e4b94653ba2aa16fdc7a5e3347aba962b684508`  
		Last Modified: Wed, 10 May 2023 18:09:06 GMT  
		Size: 454.2 KB (454222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee5c1ba4848e97d4e3c43d9d4bca0eeeccf2d5d7f6d805d748da4a7d24ad14e`  
		Last Modified: Wed, 10 May 2023 18:09:05 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffadd10be916fc5729676141f5d0ba6aa30968b75555790e449d4988dc81332a`  
		Last Modified: Wed, 10 May 2023 18:32:42 GMT  
		Size: 178.3 MB (178334017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3968819bf3a63424c2b6a4e9591f0c9e6ffbb99a92e0c8d8bb65c67dee37c591`  
		Last Modified: Wed, 24 May 2023 22:50:04 GMT  
		Size: 307.3 MB (307250466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab4c543f2a230baf4ee559f04be553bc00d7b77cc356fee1f21587123cb6977`  
		Last Modified: Wed, 24 May 2023 22:49:49 GMT  
		Size: 2.3 MB (2343680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22684cbd7ece18edde12615b426a6542f278c82ffebfd4d0e88ef0ff8fbde0b`  
		Last Modified: Wed, 24 May 2023 22:49:48 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5270a8761eb66f6e2d094c0879e26935456fa9e19b282bbed9418b58631140c1`  
		Last Modified: Wed, 24 May 2023 22:49:48 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efce4adb2bae1b274febb0d3785c785befb8c4de6c50df158a2aa23673c5b60d`  
		Last Modified: Wed, 24 May 2023 22:49:48 GMT  
		Size: 6.0 KB (6017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9715a623bab854429c5628dcca4718382ada25dbc334b3d61b24a46031cd5d44`  
		Last Modified: Wed, 24 May 2023 22:49:48 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:lts-mysql` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:15957635ec1e31779c981c0817bf66a72c04e6218e1acc75ef471fc7f46dd01c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.5 MB (581515826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aa7648bbd0225e907a6fd992596c1aedb9a12baa3eb30a4a458df9d4af79c91`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 25 Apr 2023 17:31:58 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:31:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:31:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:31:59 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:32:02 GMT
ADD file:aee0d7770ef2f24dc9697e86d391529d001a4013b6e30a3ac90a57932814a57e in / 
# Tue, 25 Apr 2023 17:32:02 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 03:25:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 03:25:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 03:25:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 03:25:23 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 03:25:47 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 04 May 2023 03:26:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 03:26:10 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 11:14:20 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 04 May 2023 11:14:20 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 11:14:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 04 May 2023 11:14:21 GMT
WORKDIR /usr/local/tomcat
# Thu, 04 May 2023 11:14:21 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 11:14:21 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 11:15:34 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 04 May 2023 11:15:34 GMT
ENV TOMCAT_MAJOR=9
# Wed, 10 May 2023 17:56:49 GMT
ENV TOMCAT_VERSION=9.0.75
# Wed, 10 May 2023 17:56:49 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Wed, 10 May 2023 17:56:49 GMT
COPY dir:2a613f9e425d5febc8be5b6c17f49b39f1b8ad84b1601f07f76abed41b25b24b in /usr/local/tomcat 
# Wed, 10 May 2023 17:56:52 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 17:56:54 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 10 May 2023 17:56:54 GMT
EXPOSE 8080
# Wed, 10 May 2023 17:56:54 GMT
CMD ["catalina.sh" "run"]
# Wed, 10 May 2023 18:22:09 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 10 May 2023 18:23:10 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 24 May 2023 23:08:47 GMT
ENV XWIKI_VERSION=14.10.11
# Wed, 24 May 2023 23:08:47 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.11
# Wed, 24 May 2023 23:08:48 GMT
ENV XWIKI_DOWNLOAD_SHA256=0804bdbc2a4eb370a25cfcd9a2185e80e007180007d15fdaa4d371dbd02b5d43
# Wed, 24 May 2023 23:09:27 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 24 May 2023 23:09:29 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Wed, 24 May 2023 23:09:29 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Wed, 24 May 2023 23:09:30 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Wed, 24 May 2023 23:09:30 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Wed, 24 May 2023 23:09:30 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Wed, 24 May 2023 23:09:31 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Wed, 24 May 2023 23:09:31 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 24 May 2023 23:09:31 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 24 May 2023 23:09:31 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 24 May 2023 23:09:31 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 24 May 2023 23:09:32 GMT
VOLUME [/usr/local/xwiki]
# Wed, 24 May 2023 23:09:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 May 2023 23:09:32 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f3f60f415e9a03eed88bd5dd5268c841cde08dacf16911a3ef1e4e0fcdd76568`  
		Last Modified: Wed, 26 Apr 2023 02:08:37 GMT  
		Size: 28.4 MB (28389440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fb3595122d1cb6fffe722e2624c3c89b00776b393256a5444af56ceda691cf`  
		Last Modified: Thu, 04 May 2023 03:28:13 GMT  
		Size: 12.5 MB (12463858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5542665e33e692b672a405517e6e267c4c6e210bc410b97a6a1ce732618caa87`  
		Last Modified: Thu, 04 May 2023 03:29:19 GMT  
		Size: 45.0 MB (45009401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e52b8550f0ced98adb0880bd041e361ffb69810e6071e6d71eb2ec0c8ecfad5`  
		Last Modified: Thu, 04 May 2023 03:29:14 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea5566732e0a920d0a63e4fbebf073d2c49e3f80716df462e73f895cc0c5dfa`  
		Last Modified: Thu, 04 May 2023 11:24:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c6d16bf5ef403ef11a1cc9e40650f402cd1f8269d16982f7daebc2a76ab0d9`  
		Last Modified: Wed, 10 May 2023 18:03:56 GMT  
		Size: 12.2 MB (12242222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eaf464f1c82b5f85e3173b2c732f0928a28e669fcc4af9eb6da48199e92ae50`  
		Last Modified: Wed, 10 May 2023 18:03:55 GMT  
		Size: 453.7 KB (453682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ef5f2b94b25f2b0f609c429cc1626d9dd857d8294d2d872d6595bdeff3a5ca`  
		Last Modified: Wed, 10 May 2023 18:03:55 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7cc67d2dc8f70f6e05051c0e95eb0de93a45de55ba65c355eedaff2bf118e42`  
		Last Modified: Wed, 10 May 2023 18:27:43 GMT  
		Size: 173.4 MB (173350375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0f918d67c923bb6ad20257659a178cf82a52dbd68eda4c094eb3fb372831c2c`  
		Last Modified: Wed, 24 May 2023 23:11:04 GMT  
		Size: 307.3 MB (307250539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced4cf6fb2a03eefd5f5bf442bda27c93928535469b7e8d6fc9c5d7b5ae30b2f`  
		Last Modified: Wed, 24 May 2023 23:10:51 GMT  
		Size: 2.3 MB (2343677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98623f72442cf00c262363a201209a0aa274f36c3ea6fc9f6982e636f879fa70`  
		Last Modified: Wed, 24 May 2023 23:10:50 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7788f555a977b55dd4bb3cc03f0877839200ef650618e788503063bad30080ce`  
		Last Modified: Wed, 24 May 2023 23:10:50 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874c98264dbb8128fd9c27e97654851dfbde45dfb396778744d7616b44591eae`  
		Last Modified: Wed, 24 May 2023 23:10:50 GMT  
		Size: 6.0 KB (6014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee9de251f061dd4ab29b65e5807e482de72b8f045af577bdc2ade102cedf52d`  
		Last Modified: Wed, 24 May 2023 23:10:50 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:lts-mysql-tomcat`

```console
$ docker pull xwiki@sha256:3cb3e791882b8ad6819d53ac0e7fb6c678ba6435b06061929dca6ce1a98fbef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:lts-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:8d0ae8c6e385bf7493b07cbab2a2afa371e97538db4f1c040a18c393b5d1e090
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.2 MB (590232292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eff782e5d932a0d40c015b5812ebe948e85c30648a4875e24e6320a36ebb037b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 07:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 07:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 07:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 07:26:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:27:16 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 04 May 2023 07:27:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 07:27:40 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 16:13:14 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 04 May 2023 16:13:14 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 16:13:14 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 04 May 2023 16:13:14 GMT
WORKDIR /usr/local/tomcat
# Thu, 04 May 2023 16:13:14 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 16:13:15 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 16:14:45 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 04 May 2023 16:14:45 GMT
ENV TOMCAT_MAJOR=9
# Wed, 10 May 2023 18:01:17 GMT
ENV TOMCAT_VERSION=9.0.75
# Wed, 10 May 2023 18:01:17 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Wed, 10 May 2023 18:01:17 GMT
COPY dir:606cc669e6833afa7967597ca36d4a4497efbb54719c008108649021142d7549 in /usr/local/tomcat 
# Wed, 10 May 2023 18:01:21 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 18:01:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 10 May 2023 18:01:23 GMT
EXPOSE 8080
# Wed, 10 May 2023 18:01:23 GMT
CMD ["catalina.sh" "run"]
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 10 May 2023 18:28:05 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 24 May 2023 22:47:42 GMT
ENV XWIKI_VERSION=14.10.11
# Wed, 24 May 2023 22:47:42 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.11
# Wed, 24 May 2023 22:47:42 GMT
ENV XWIKI_DOWNLOAD_SHA256=0804bdbc2a4eb370a25cfcd9a2185e80e007180007d15fdaa4d371dbd02b5d43
# Wed, 24 May 2023 22:48:21 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 24 May 2023 22:48:22 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Wed, 24 May 2023 22:48:22 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Wed, 24 May 2023 22:48:22 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Wed, 24 May 2023 22:48:22 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Wed, 24 May 2023 22:48:22 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Wed, 24 May 2023 22:48:23 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Wed, 24 May 2023 22:48:23 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 24 May 2023 22:48:23 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 24 May 2023 22:48:23 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 24 May 2023 22:48:24 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 24 May 2023 22:48:24 GMT
VOLUME [/usr/local/xwiki]
# Wed, 24 May 2023 22:48:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 May 2023 22:48:24 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458b02b5411a07f3b354cde2b461caffc1bb184a3413b5736a9e67ee87cb28b2`  
		Last Modified: Thu, 04 May 2023 07:30:02 GMT  
		Size: 12.5 MB (12504170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04a165ead1d5eabe89dc88e53286af89caab22a5d20c53007b9e6e508affb4b`  
		Last Modified: Thu, 04 May 2023 07:31:19 GMT  
		Size: 46.7 MB (46666270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1187c73b18505bd4495bc03ccbdb723388dfe4d633fd12be845dfe8e253e48e2`  
		Last Modified: Thu, 04 May 2023 07:31:12 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c833cbb14374cde014505e77f6a6122773984a691844e4138fc15cae99ba625`  
		Last Modified: Thu, 04 May 2023 16:24:19 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439ac04571c77c4330db518bc8f35b70f8723246ed34c98787f7ac8d7dc30b42`  
		Last Modified: Wed, 10 May 2023 18:09:06 GMT  
		Size: 12.2 MB (12236613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8e775ba0b76c6692c0b9211e4b94653ba2aa16fdc7a5e3347aba962b684508`  
		Last Modified: Wed, 10 May 2023 18:09:06 GMT  
		Size: 454.2 KB (454222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee5c1ba4848e97d4e3c43d9d4bca0eeeccf2d5d7f6d805d748da4a7d24ad14e`  
		Last Modified: Wed, 10 May 2023 18:09:05 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffadd10be916fc5729676141f5d0ba6aa30968b75555790e449d4988dc81332a`  
		Last Modified: Wed, 10 May 2023 18:32:42 GMT  
		Size: 178.3 MB (178334017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3968819bf3a63424c2b6a4e9591f0c9e6ffbb99a92e0c8d8bb65c67dee37c591`  
		Last Modified: Wed, 24 May 2023 22:50:04 GMT  
		Size: 307.3 MB (307250466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab4c543f2a230baf4ee559f04be553bc00d7b77cc356fee1f21587123cb6977`  
		Last Modified: Wed, 24 May 2023 22:49:49 GMT  
		Size: 2.3 MB (2343680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22684cbd7ece18edde12615b426a6542f278c82ffebfd4d0e88ef0ff8fbde0b`  
		Last Modified: Wed, 24 May 2023 22:49:48 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5270a8761eb66f6e2d094c0879e26935456fa9e19b282bbed9418b58631140c1`  
		Last Modified: Wed, 24 May 2023 22:49:48 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efce4adb2bae1b274febb0d3785c785befb8c4de6c50df158a2aa23673c5b60d`  
		Last Modified: Wed, 24 May 2023 22:49:48 GMT  
		Size: 6.0 KB (6017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9715a623bab854429c5628dcca4718382ada25dbc334b3d61b24a46031cd5d44`  
		Last Modified: Wed, 24 May 2023 22:49:48 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:lts-mysql-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:15957635ec1e31779c981c0817bf66a72c04e6218e1acc75ef471fc7f46dd01c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.5 MB (581515826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aa7648bbd0225e907a6fd992596c1aedb9a12baa3eb30a4a458df9d4af79c91`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 25 Apr 2023 17:31:58 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:31:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:31:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:31:59 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:32:02 GMT
ADD file:aee0d7770ef2f24dc9697e86d391529d001a4013b6e30a3ac90a57932814a57e in / 
# Tue, 25 Apr 2023 17:32:02 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 03:25:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 03:25:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 03:25:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 03:25:23 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 03:25:47 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 04 May 2023 03:26:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 03:26:10 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 11:14:20 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 04 May 2023 11:14:20 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 11:14:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 04 May 2023 11:14:21 GMT
WORKDIR /usr/local/tomcat
# Thu, 04 May 2023 11:14:21 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 11:14:21 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 11:15:34 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 04 May 2023 11:15:34 GMT
ENV TOMCAT_MAJOR=9
# Wed, 10 May 2023 17:56:49 GMT
ENV TOMCAT_VERSION=9.0.75
# Wed, 10 May 2023 17:56:49 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Wed, 10 May 2023 17:56:49 GMT
COPY dir:2a613f9e425d5febc8be5b6c17f49b39f1b8ad84b1601f07f76abed41b25b24b in /usr/local/tomcat 
# Wed, 10 May 2023 17:56:52 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 17:56:54 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 10 May 2023 17:56:54 GMT
EXPOSE 8080
# Wed, 10 May 2023 17:56:54 GMT
CMD ["catalina.sh" "run"]
# Wed, 10 May 2023 18:22:09 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 10 May 2023 18:23:10 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 24 May 2023 23:08:47 GMT
ENV XWIKI_VERSION=14.10.11
# Wed, 24 May 2023 23:08:47 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.11
# Wed, 24 May 2023 23:08:48 GMT
ENV XWIKI_DOWNLOAD_SHA256=0804bdbc2a4eb370a25cfcd9a2185e80e007180007d15fdaa4d371dbd02b5d43
# Wed, 24 May 2023 23:09:27 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 24 May 2023 23:09:29 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Wed, 24 May 2023 23:09:29 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Wed, 24 May 2023 23:09:30 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Wed, 24 May 2023 23:09:30 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Wed, 24 May 2023 23:09:30 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Wed, 24 May 2023 23:09:31 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Wed, 24 May 2023 23:09:31 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 24 May 2023 23:09:31 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 24 May 2023 23:09:31 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 24 May 2023 23:09:31 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 24 May 2023 23:09:32 GMT
VOLUME [/usr/local/xwiki]
# Wed, 24 May 2023 23:09:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 May 2023 23:09:32 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f3f60f415e9a03eed88bd5dd5268c841cde08dacf16911a3ef1e4e0fcdd76568`  
		Last Modified: Wed, 26 Apr 2023 02:08:37 GMT  
		Size: 28.4 MB (28389440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fb3595122d1cb6fffe722e2624c3c89b00776b393256a5444af56ceda691cf`  
		Last Modified: Thu, 04 May 2023 03:28:13 GMT  
		Size: 12.5 MB (12463858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5542665e33e692b672a405517e6e267c4c6e210bc410b97a6a1ce732618caa87`  
		Last Modified: Thu, 04 May 2023 03:29:19 GMT  
		Size: 45.0 MB (45009401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e52b8550f0ced98adb0880bd041e361ffb69810e6071e6d71eb2ec0c8ecfad5`  
		Last Modified: Thu, 04 May 2023 03:29:14 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea5566732e0a920d0a63e4fbebf073d2c49e3f80716df462e73f895cc0c5dfa`  
		Last Modified: Thu, 04 May 2023 11:24:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c6d16bf5ef403ef11a1cc9e40650f402cd1f8269d16982f7daebc2a76ab0d9`  
		Last Modified: Wed, 10 May 2023 18:03:56 GMT  
		Size: 12.2 MB (12242222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eaf464f1c82b5f85e3173b2c732f0928a28e669fcc4af9eb6da48199e92ae50`  
		Last Modified: Wed, 10 May 2023 18:03:55 GMT  
		Size: 453.7 KB (453682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ef5f2b94b25f2b0f609c429cc1626d9dd857d8294d2d872d6595bdeff3a5ca`  
		Last Modified: Wed, 10 May 2023 18:03:55 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7cc67d2dc8f70f6e05051c0e95eb0de93a45de55ba65c355eedaff2bf118e42`  
		Last Modified: Wed, 10 May 2023 18:27:43 GMT  
		Size: 173.4 MB (173350375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0f918d67c923bb6ad20257659a178cf82a52dbd68eda4c094eb3fb372831c2c`  
		Last Modified: Wed, 24 May 2023 23:11:04 GMT  
		Size: 307.3 MB (307250539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced4cf6fb2a03eefd5f5bf442bda27c93928535469b7e8d6fc9c5d7b5ae30b2f`  
		Last Modified: Wed, 24 May 2023 23:10:51 GMT  
		Size: 2.3 MB (2343677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98623f72442cf00c262363a201209a0aa274f36c3ea6fc9f6982e636f879fa70`  
		Last Modified: Wed, 24 May 2023 23:10:50 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7788f555a977b55dd4bb3cc03f0877839200ef650618e788503063bad30080ce`  
		Last Modified: Wed, 24 May 2023 23:10:50 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874c98264dbb8128fd9c27e97654851dfbde45dfb396778744d7616b44591eae`  
		Last Modified: Wed, 24 May 2023 23:10:50 GMT  
		Size: 6.0 KB (6014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee9de251f061dd4ab29b65e5807e482de72b8f045af577bdc2ade102cedf52d`  
		Last Modified: Wed, 24 May 2023 23:10:50 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:lts-postgres`

```console
$ docker pull xwiki@sha256:dabd869e53131a2d15143bd5393863a574bacd8268d667ab5f9be188c80b39d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:lts-postgres` - linux; amd64

```console
$ docker pull xwiki@sha256:ccb7ea5c1410db8b59df0ea0243933bbb5050cf5ed8bc35d3b4702d5928d1482
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.8 MB (589768452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71815ff74c00cebccb5539716f3c3f0391b90709502c0f2f23eae95fd4d9b7f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 07:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 07:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 07:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 07:26:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:27:16 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 04 May 2023 07:27:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 07:27:40 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 16:13:14 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 04 May 2023 16:13:14 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 16:13:14 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 04 May 2023 16:13:14 GMT
WORKDIR /usr/local/tomcat
# Thu, 04 May 2023 16:13:14 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 16:13:15 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 16:14:45 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 04 May 2023 16:14:45 GMT
ENV TOMCAT_MAJOR=9
# Wed, 10 May 2023 18:01:17 GMT
ENV TOMCAT_VERSION=9.0.75
# Wed, 10 May 2023 18:01:17 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Wed, 10 May 2023 18:01:17 GMT
COPY dir:606cc669e6833afa7967597ca36d4a4497efbb54719c008108649021142d7549 in /usr/local/tomcat 
# Wed, 10 May 2023 18:01:21 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 18:01:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 10 May 2023 18:01:23 GMT
EXPOSE 8080
# Wed, 10 May 2023 18:01:23 GMT
CMD ["catalina.sh" "run"]
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 10 May 2023 18:29:15 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Wed, 24 May 2023 22:48:31 GMT
ENV XWIKI_VERSION=14.10.11
# Wed, 24 May 2023 22:48:31 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.11
# Wed, 24 May 2023 22:48:31 GMT
ENV XWIKI_DOWNLOAD_SHA256=0804bdbc2a4eb370a25cfcd9a2185e80e007180007d15fdaa4d371dbd02b5d43
# Wed, 24 May 2023 22:49:09 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 24 May 2023 22:49:11 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Wed, 24 May 2023 22:49:11 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 24 May 2023 22:49:11 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 24 May 2023 22:49:11 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 24 May 2023 22:49:11 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 24 May 2023 22:49:11 GMT
VOLUME [/usr/local/xwiki]
# Wed, 24 May 2023 22:49:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 May 2023 22:49:12 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458b02b5411a07f3b354cde2b461caffc1bb184a3413b5736a9e67ee87cb28b2`  
		Last Modified: Thu, 04 May 2023 07:30:02 GMT  
		Size: 12.5 MB (12504170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04a165ead1d5eabe89dc88e53286af89caab22a5d20c53007b9e6e508affb4b`  
		Last Modified: Thu, 04 May 2023 07:31:19 GMT  
		Size: 46.7 MB (46666270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1187c73b18505bd4495bc03ccbdb723388dfe4d633fd12be845dfe8e253e48e2`  
		Last Modified: Thu, 04 May 2023 07:31:12 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c833cbb14374cde014505e77f6a6122773984a691844e4138fc15cae99ba625`  
		Last Modified: Thu, 04 May 2023 16:24:19 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439ac04571c77c4330db518bc8f35b70f8723246ed34c98787f7ac8d7dc30b42`  
		Last Modified: Wed, 10 May 2023 18:09:06 GMT  
		Size: 12.2 MB (12236613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8e775ba0b76c6692c0b9211e4b94653ba2aa16fdc7a5e3347aba962b684508`  
		Last Modified: Wed, 10 May 2023 18:09:06 GMT  
		Size: 454.2 KB (454222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee5c1ba4848e97d4e3c43d9d4bca0eeeccf2d5d7f6d805d748da4a7d24ad14e`  
		Last Modified: Wed, 10 May 2023 18:09:05 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29abf03d18e0bc34be536fce36ea27d0012a4d330eed44003684563b4d891b2d`  
		Last Modified: Wed, 10 May 2023 18:33:36 GMT  
		Size: 179.3 MB (179276853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:498ed996b7f85205493a73418ae815f35210fc8d8b7b70baa9a06de3e5c233db`  
		Last Modified: Wed, 24 May 2023 22:50:46 GMT  
		Size: 307.3 MB (307250477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:726404a64f919d8c5876da440316ad8fe4a45edd3630ad29f6901546744c11b4`  
		Last Modified: Wed, 24 May 2023 22:50:30 GMT  
		Size: 936.8 KB (936849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84cee4a8e3ec67483536219c5828a467fbc92b808b723cc7fe131aa9d4a6c0ca`  
		Last Modified: Wed, 24 May 2023 22:50:30 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f650315d22dd71a78884aa2fd92ca686e5ce16f9206197580eecb4ecdff2de`  
		Last Modified: Wed, 24 May 2023 22:50:30 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae0aba32059faa0517242b3ddd90818c736c00398d30b55ec885149ac65c2f29`  
		Last Modified: Wed, 24 May 2023 22:50:30 GMT  
		Size: 6.0 KB (6016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9f18e6a2d23412d06f75bdd16e45b58b9e670d8d683b0e55422033d911fc9f1`  
		Last Modified: Wed, 24 May 2023 22:50:30 GMT  
		Size: 2.5 KB (2502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:lts-postgres` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:80beeb7d3308b8ad1ce8a2ce4e70eb53da61c4632fb10da1448ad9fa7a78d3be
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.0 MB (581049648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ec4529f91042538f49ba29100185d25c41eef43d8163bbb16ad47093be7adbd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 25 Apr 2023 17:31:58 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:31:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:31:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:31:59 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:32:02 GMT
ADD file:aee0d7770ef2f24dc9697e86d391529d001a4013b6e30a3ac90a57932814a57e in / 
# Tue, 25 Apr 2023 17:32:02 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 03:25:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 03:25:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 03:25:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 03:25:23 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 03:25:47 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 04 May 2023 03:26:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 03:26:10 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 11:14:20 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 04 May 2023 11:14:20 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 11:14:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 04 May 2023 11:14:21 GMT
WORKDIR /usr/local/tomcat
# Thu, 04 May 2023 11:14:21 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 11:14:21 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 11:15:34 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 04 May 2023 11:15:34 GMT
ENV TOMCAT_MAJOR=9
# Wed, 10 May 2023 17:56:49 GMT
ENV TOMCAT_VERSION=9.0.75
# Wed, 10 May 2023 17:56:49 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Wed, 10 May 2023 17:56:49 GMT
COPY dir:2a613f9e425d5febc8be5b6c17f49b39f1b8ad84b1601f07f76abed41b25b24b in /usr/local/tomcat 
# Wed, 10 May 2023 17:56:52 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 17:56:54 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 10 May 2023 17:56:54 GMT
EXPOSE 8080
# Wed, 10 May 2023 17:56:54 GMT
CMD ["catalina.sh" "run"]
# Wed, 10 May 2023 18:22:09 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 10 May 2023 18:24:24 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Wed, 24 May 2023 23:09:35 GMT
ENV XWIKI_VERSION=14.10.11
# Wed, 24 May 2023 23:09:35 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.11
# Wed, 24 May 2023 23:09:35 GMT
ENV XWIKI_DOWNLOAD_SHA256=0804bdbc2a4eb370a25cfcd9a2185e80e007180007d15fdaa4d371dbd02b5d43
# Wed, 24 May 2023 23:10:15 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 24 May 2023 23:10:17 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Wed, 24 May 2023 23:10:17 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 24 May 2023 23:10:17 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 24 May 2023 23:10:18 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 24 May 2023 23:10:18 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 24 May 2023 23:10:18 GMT
VOLUME [/usr/local/xwiki]
# Wed, 24 May 2023 23:10:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 May 2023 23:10:18 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f3f60f415e9a03eed88bd5dd5268c841cde08dacf16911a3ef1e4e0fcdd76568`  
		Last Modified: Wed, 26 Apr 2023 02:08:37 GMT  
		Size: 28.4 MB (28389440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fb3595122d1cb6fffe722e2624c3c89b00776b393256a5444af56ceda691cf`  
		Last Modified: Thu, 04 May 2023 03:28:13 GMT  
		Size: 12.5 MB (12463858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5542665e33e692b672a405517e6e267c4c6e210bc410b97a6a1ce732618caa87`  
		Last Modified: Thu, 04 May 2023 03:29:19 GMT  
		Size: 45.0 MB (45009401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e52b8550f0ced98adb0880bd041e361ffb69810e6071e6d71eb2ec0c8ecfad5`  
		Last Modified: Thu, 04 May 2023 03:29:14 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea5566732e0a920d0a63e4fbebf073d2c49e3f80716df462e73f895cc0c5dfa`  
		Last Modified: Thu, 04 May 2023 11:24:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c6d16bf5ef403ef11a1cc9e40650f402cd1f8269d16982f7daebc2a76ab0d9`  
		Last Modified: Wed, 10 May 2023 18:03:56 GMT  
		Size: 12.2 MB (12242222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eaf464f1c82b5f85e3173b2c732f0928a28e669fcc4af9eb6da48199e92ae50`  
		Last Modified: Wed, 10 May 2023 18:03:55 GMT  
		Size: 453.7 KB (453682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ef5f2b94b25f2b0f609c429cc1626d9dd857d8294d2d872d6595bdeff3a5ca`  
		Last Modified: Wed, 10 May 2023 18:03:55 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e76b785cabb7a84968f4d713d3072c255796ddcef576690d954e3fc5b1a09604`  
		Last Modified: Wed, 10 May 2023 18:28:29 GMT  
		Size: 174.3 MB (174290936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ca8b2542757030e2106531ddc6ec3e6dfa6acc493a72d909bb0643df73cf80`  
		Last Modified: Wed, 24 May 2023 23:11:45 GMT  
		Size: 307.3 MB (307250465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97cd250ffbef4fb2fdd174dfb45463c24ac51dfafe9a8660d7a4c5779c36753`  
		Last Modified: Wed, 24 May 2023 23:11:32 GMT  
		Size: 936.9 KB (936854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b1f6e5a8be59e46859d1c9303c24792c97fbcadc1855549404052ed0ed691f`  
		Last Modified: Wed, 24 May 2023 23:11:31 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87f9348f23dfc87a0a5dae7c72f497455e4b3205ef78f38f7e26116fbd5468a7`  
		Last Modified: Wed, 24 May 2023 23:11:31 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ef195c009e7dec60741122ecf4e68a4a11ffefeabf35203eb140ed91090c5c`  
		Last Modified: Wed, 24 May 2023 23:11:31 GMT  
		Size: 6.0 KB (6015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:902e7c9edf86f6fe373bd24ddcdff8ca21d7f599de277b9bcffe4106c4bb5f56`  
		Last Modified: Wed, 24 May 2023 23:11:31 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:lts-postgres-tomcat`

```console
$ docker pull xwiki@sha256:dabd869e53131a2d15143bd5393863a574bacd8268d667ab5f9be188c80b39d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:lts-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:ccb7ea5c1410db8b59df0ea0243933bbb5050cf5ed8bc35d3b4702d5928d1482
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.8 MB (589768452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71815ff74c00cebccb5539716f3c3f0391b90709502c0f2f23eae95fd4d9b7f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 07:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 07:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 07:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 07:26:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:27:16 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 04 May 2023 07:27:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 07:27:40 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 16:13:14 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 04 May 2023 16:13:14 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 16:13:14 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 04 May 2023 16:13:14 GMT
WORKDIR /usr/local/tomcat
# Thu, 04 May 2023 16:13:14 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 16:13:15 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 16:14:45 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 04 May 2023 16:14:45 GMT
ENV TOMCAT_MAJOR=9
# Wed, 10 May 2023 18:01:17 GMT
ENV TOMCAT_VERSION=9.0.75
# Wed, 10 May 2023 18:01:17 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Wed, 10 May 2023 18:01:17 GMT
COPY dir:606cc669e6833afa7967597ca36d4a4497efbb54719c008108649021142d7549 in /usr/local/tomcat 
# Wed, 10 May 2023 18:01:21 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 18:01:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 10 May 2023 18:01:23 GMT
EXPOSE 8080
# Wed, 10 May 2023 18:01:23 GMT
CMD ["catalina.sh" "run"]
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 10 May 2023 18:29:15 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Wed, 24 May 2023 22:48:31 GMT
ENV XWIKI_VERSION=14.10.11
# Wed, 24 May 2023 22:48:31 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.11
# Wed, 24 May 2023 22:48:31 GMT
ENV XWIKI_DOWNLOAD_SHA256=0804bdbc2a4eb370a25cfcd9a2185e80e007180007d15fdaa4d371dbd02b5d43
# Wed, 24 May 2023 22:49:09 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 24 May 2023 22:49:11 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Wed, 24 May 2023 22:49:11 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 24 May 2023 22:49:11 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 24 May 2023 22:49:11 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 24 May 2023 22:49:11 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 24 May 2023 22:49:11 GMT
VOLUME [/usr/local/xwiki]
# Wed, 24 May 2023 22:49:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 May 2023 22:49:12 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458b02b5411a07f3b354cde2b461caffc1bb184a3413b5736a9e67ee87cb28b2`  
		Last Modified: Thu, 04 May 2023 07:30:02 GMT  
		Size: 12.5 MB (12504170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04a165ead1d5eabe89dc88e53286af89caab22a5d20c53007b9e6e508affb4b`  
		Last Modified: Thu, 04 May 2023 07:31:19 GMT  
		Size: 46.7 MB (46666270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1187c73b18505bd4495bc03ccbdb723388dfe4d633fd12be845dfe8e253e48e2`  
		Last Modified: Thu, 04 May 2023 07:31:12 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c833cbb14374cde014505e77f6a6122773984a691844e4138fc15cae99ba625`  
		Last Modified: Thu, 04 May 2023 16:24:19 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439ac04571c77c4330db518bc8f35b70f8723246ed34c98787f7ac8d7dc30b42`  
		Last Modified: Wed, 10 May 2023 18:09:06 GMT  
		Size: 12.2 MB (12236613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8e775ba0b76c6692c0b9211e4b94653ba2aa16fdc7a5e3347aba962b684508`  
		Last Modified: Wed, 10 May 2023 18:09:06 GMT  
		Size: 454.2 KB (454222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee5c1ba4848e97d4e3c43d9d4bca0eeeccf2d5d7f6d805d748da4a7d24ad14e`  
		Last Modified: Wed, 10 May 2023 18:09:05 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29abf03d18e0bc34be536fce36ea27d0012a4d330eed44003684563b4d891b2d`  
		Last Modified: Wed, 10 May 2023 18:33:36 GMT  
		Size: 179.3 MB (179276853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:498ed996b7f85205493a73418ae815f35210fc8d8b7b70baa9a06de3e5c233db`  
		Last Modified: Wed, 24 May 2023 22:50:46 GMT  
		Size: 307.3 MB (307250477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:726404a64f919d8c5876da440316ad8fe4a45edd3630ad29f6901546744c11b4`  
		Last Modified: Wed, 24 May 2023 22:50:30 GMT  
		Size: 936.8 KB (936849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84cee4a8e3ec67483536219c5828a467fbc92b808b723cc7fe131aa9d4a6c0ca`  
		Last Modified: Wed, 24 May 2023 22:50:30 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f650315d22dd71a78884aa2fd92ca686e5ce16f9206197580eecb4ecdff2de`  
		Last Modified: Wed, 24 May 2023 22:50:30 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae0aba32059faa0517242b3ddd90818c736c00398d30b55ec885149ac65c2f29`  
		Last Modified: Wed, 24 May 2023 22:50:30 GMT  
		Size: 6.0 KB (6016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9f18e6a2d23412d06f75bdd16e45b58b9e670d8d683b0e55422033d911fc9f1`  
		Last Modified: Wed, 24 May 2023 22:50:30 GMT  
		Size: 2.5 KB (2502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:lts-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:80beeb7d3308b8ad1ce8a2ce4e70eb53da61c4632fb10da1448ad9fa7a78d3be
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.0 MB (581049648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ec4529f91042538f49ba29100185d25c41eef43d8163bbb16ad47093be7adbd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 25 Apr 2023 17:31:58 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:31:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:31:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:31:59 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:32:02 GMT
ADD file:aee0d7770ef2f24dc9697e86d391529d001a4013b6e30a3ac90a57932814a57e in / 
# Tue, 25 Apr 2023 17:32:02 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 03:25:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 03:25:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 03:25:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 03:25:23 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 03:25:47 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 04 May 2023 03:26:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 03:26:10 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 11:14:20 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 04 May 2023 11:14:20 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 11:14:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 04 May 2023 11:14:21 GMT
WORKDIR /usr/local/tomcat
# Thu, 04 May 2023 11:14:21 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 11:14:21 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 11:15:34 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 04 May 2023 11:15:34 GMT
ENV TOMCAT_MAJOR=9
# Wed, 10 May 2023 17:56:49 GMT
ENV TOMCAT_VERSION=9.0.75
# Wed, 10 May 2023 17:56:49 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Wed, 10 May 2023 17:56:49 GMT
COPY dir:2a613f9e425d5febc8be5b6c17f49b39f1b8ad84b1601f07f76abed41b25b24b in /usr/local/tomcat 
# Wed, 10 May 2023 17:56:52 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 17:56:54 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 10 May 2023 17:56:54 GMT
EXPOSE 8080
# Wed, 10 May 2023 17:56:54 GMT
CMD ["catalina.sh" "run"]
# Wed, 10 May 2023 18:22:09 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 10 May 2023 18:24:24 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Wed, 24 May 2023 23:09:35 GMT
ENV XWIKI_VERSION=14.10.11
# Wed, 24 May 2023 23:09:35 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.11
# Wed, 24 May 2023 23:09:35 GMT
ENV XWIKI_DOWNLOAD_SHA256=0804bdbc2a4eb370a25cfcd9a2185e80e007180007d15fdaa4d371dbd02b5d43
# Wed, 24 May 2023 23:10:15 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 24 May 2023 23:10:17 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Wed, 24 May 2023 23:10:17 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 24 May 2023 23:10:17 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 24 May 2023 23:10:18 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 24 May 2023 23:10:18 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 24 May 2023 23:10:18 GMT
VOLUME [/usr/local/xwiki]
# Wed, 24 May 2023 23:10:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 May 2023 23:10:18 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f3f60f415e9a03eed88bd5dd5268c841cde08dacf16911a3ef1e4e0fcdd76568`  
		Last Modified: Wed, 26 Apr 2023 02:08:37 GMT  
		Size: 28.4 MB (28389440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fb3595122d1cb6fffe722e2624c3c89b00776b393256a5444af56ceda691cf`  
		Last Modified: Thu, 04 May 2023 03:28:13 GMT  
		Size: 12.5 MB (12463858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5542665e33e692b672a405517e6e267c4c6e210bc410b97a6a1ce732618caa87`  
		Last Modified: Thu, 04 May 2023 03:29:19 GMT  
		Size: 45.0 MB (45009401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e52b8550f0ced98adb0880bd041e361ffb69810e6071e6d71eb2ec0c8ecfad5`  
		Last Modified: Thu, 04 May 2023 03:29:14 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea5566732e0a920d0a63e4fbebf073d2c49e3f80716df462e73f895cc0c5dfa`  
		Last Modified: Thu, 04 May 2023 11:24:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c6d16bf5ef403ef11a1cc9e40650f402cd1f8269d16982f7daebc2a76ab0d9`  
		Last Modified: Wed, 10 May 2023 18:03:56 GMT  
		Size: 12.2 MB (12242222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eaf464f1c82b5f85e3173b2c732f0928a28e669fcc4af9eb6da48199e92ae50`  
		Last Modified: Wed, 10 May 2023 18:03:55 GMT  
		Size: 453.7 KB (453682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ef5f2b94b25f2b0f609c429cc1626d9dd857d8294d2d872d6595bdeff3a5ca`  
		Last Modified: Wed, 10 May 2023 18:03:55 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e76b785cabb7a84968f4d713d3072c255796ddcef576690d954e3fc5b1a09604`  
		Last Modified: Wed, 10 May 2023 18:28:29 GMT  
		Size: 174.3 MB (174290936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ca8b2542757030e2106531ddc6ec3e6dfa6acc493a72d909bb0643df73cf80`  
		Last Modified: Wed, 24 May 2023 23:11:45 GMT  
		Size: 307.3 MB (307250465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97cd250ffbef4fb2fdd174dfb45463c24ac51dfafe9a8660d7a4c5779c36753`  
		Last Modified: Wed, 24 May 2023 23:11:32 GMT  
		Size: 936.9 KB (936854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b1f6e5a8be59e46859d1c9303c24792c97fbcadc1855549404052ed0ed691f`  
		Last Modified: Wed, 24 May 2023 23:11:31 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87f9348f23dfc87a0a5dae7c72f497455e4b3205ef78f38f7e26116fbd5468a7`  
		Last Modified: Wed, 24 May 2023 23:11:31 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ef195c009e7dec60741122ecf4e68a4a11ffefeabf35203eb140ed91090c5c`  
		Last Modified: Wed, 24 May 2023 23:11:31 GMT  
		Size: 6.0 KB (6015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:902e7c9edf86f6fe373bd24ddcdff8ca21d7f599de277b9bcffe4106c4bb5f56`  
		Last Modified: Wed, 24 May 2023 23:11:31 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:mariadb-tomcat`

```console
$ docker pull xwiki@sha256:ba65c6db6cbf680842f048e25f348c8981c5b4295810467e68a3df22f2c0ef77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:mariadb-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:9dc755ce1b9a1d005e8b42c492573371e37310a9960b9b7becc88e7744b5a1b7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **587.4 MB (587443810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9bff1a50bba5fc8078ed4a8574445fb147d50e1d8bd49b788f4954dd1da4132`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 07:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 07:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 07:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 07:26:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:27:16 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 04 May 2023 07:27:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 07:27:40 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 16:13:14 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 04 May 2023 16:13:14 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 16:13:14 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 04 May 2023 16:13:14 GMT
WORKDIR /usr/local/tomcat
# Thu, 04 May 2023 16:13:14 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 16:13:15 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 16:14:45 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 04 May 2023 16:14:45 GMT
ENV TOMCAT_MAJOR=9
# Wed, 10 May 2023 18:01:17 GMT
ENV TOMCAT_VERSION=9.0.75
# Wed, 10 May 2023 18:01:17 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Wed, 10 May 2023 18:01:17 GMT
COPY dir:606cc669e6833afa7967597ca36d4a4497efbb54719c008108649021142d7549 in /usr/local/tomcat 
# Wed, 10 May 2023 18:01:21 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 18:01:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 10 May 2023 18:01:23 GMT
EXPOSE 8080
# Wed, 10 May 2023 18:01:23 GMT
CMD ["catalina.sh" "run"]
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 10 May 2023 18:28:05 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 18:28:06 GMT
ENV XWIKI_VERSION=15.3
# Wed, 10 May 2023 18:28:06 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.3
# Wed, 10 May 2023 18:28:06 GMT
ENV XWIKI_DOWNLOAD_SHA256=fbe35bcc5c6cc5764f2a1da4aca7878531f93bae069d94f399fea7d9656da3b8
# Wed, 10 May 2023 18:28:44 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 10 May 2023 18:30:14 GMT
ENV MARIADB_JDBC_VERSION=3.1.3
# Wed, 10 May 2023 18:30:14 GMT
ENV MARIADB_JDBC_SHA256=11297ee6562426c49c81387c860153cbc131c4c3d042492d4f6d2d97ab3a1ca5
# Wed, 10 May 2023 18:30:14 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.1.3
# Wed, 10 May 2023 18:30:14 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.1.3.jar
# Wed, 10 May 2023 18:30:15 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.1.3.jar
# Wed, 10 May 2023 18:30:15 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Wed, 10 May 2023 18:30:15 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 10 May 2023 18:30:16 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 10 May 2023 18:30:16 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 10 May 2023 18:30:16 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 10 May 2023 18:30:16 GMT
VOLUME [/usr/local/xwiki]
# Wed, 10 May 2023 18:30:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 May 2023 18:30:16 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458b02b5411a07f3b354cde2b461caffc1bb184a3413b5736a9e67ee87cb28b2`  
		Last Modified: Thu, 04 May 2023 07:30:02 GMT  
		Size: 12.5 MB (12504170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04a165ead1d5eabe89dc88e53286af89caab22a5d20c53007b9e6e508affb4b`  
		Last Modified: Thu, 04 May 2023 07:31:19 GMT  
		Size: 46.7 MB (46666270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1187c73b18505bd4495bc03ccbdb723388dfe4d633fd12be845dfe8e253e48e2`  
		Last Modified: Thu, 04 May 2023 07:31:12 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c833cbb14374cde014505e77f6a6122773984a691844e4138fc15cae99ba625`  
		Last Modified: Thu, 04 May 2023 16:24:19 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439ac04571c77c4330db518bc8f35b70f8723246ed34c98787f7ac8d7dc30b42`  
		Last Modified: Wed, 10 May 2023 18:09:06 GMT  
		Size: 12.2 MB (12236613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8e775ba0b76c6692c0b9211e4b94653ba2aa16fdc7a5e3347aba962b684508`  
		Last Modified: Wed, 10 May 2023 18:09:06 GMT  
		Size: 454.2 KB (454222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee5c1ba4848e97d4e3c43d9d4bca0eeeccf2d5d7f6d805d748da4a7d24ad14e`  
		Last Modified: Wed, 10 May 2023 18:09:05 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffadd10be916fc5729676141f5d0ba6aa30968b75555790e449d4988dc81332a`  
		Last Modified: Wed, 10 May 2023 18:32:42 GMT  
		Size: 178.3 MB (178334017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a29002da219be23e789ef538aeaae1d2296399cdfa64c6c2ed7438210947d7`  
		Last Modified: Wed, 10 May 2023 18:32:34 GMT  
		Size: 306.2 MB (306214302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:552f4dcf26ef5ef3b3a7315cc47f3dc07974cb0684775dc9f2d390f7b19be181`  
		Last Modified: Wed, 10 May 2023 18:33:53 GMT  
		Size: 591.4 KB (591369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:647b04728750fccef49babf80ba8257ced3661baa001e9e8a73067bea60c3784`  
		Last Modified: Wed, 10 May 2023 18:33:53 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bcdcc6da901312c0e56c818dfec97184f4cf9e78308964322dba08f16215da0`  
		Last Modified: Wed, 10 May 2023 18:33:53 GMT  
		Size: 2.3 KB (2312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e34abf77fe47a0d97eb01a41d2e6a9b8c0db4e9dfa284dfc767e1d9287b1effe`  
		Last Modified: Wed, 10 May 2023 18:33:53 GMT  
		Size: 6.0 KB (6005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e5b8636c37250081b1a1fd47f2ab5926692c75a635a5b3f805ed897fddb43b`  
		Last Modified: Wed, 10 May 2023 18:33:53 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:mariadb-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:8ba7073b3049679fb036a6d00a78b2b70da792b9cde40df0cc088094dc3a3d59
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.7 MB (578727276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c23d916ce05444c655cb6c876c29ee4fe78165b88d66fad2613ac17dcb7b9924`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 25 Apr 2023 17:31:58 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:31:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:31:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:31:59 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:32:02 GMT
ADD file:aee0d7770ef2f24dc9697e86d391529d001a4013b6e30a3ac90a57932814a57e in / 
# Tue, 25 Apr 2023 17:32:02 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 03:25:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 03:25:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 03:25:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 03:25:23 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 03:25:47 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 04 May 2023 03:26:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 03:26:10 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 11:14:20 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 04 May 2023 11:14:20 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 11:14:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 04 May 2023 11:14:21 GMT
WORKDIR /usr/local/tomcat
# Thu, 04 May 2023 11:14:21 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 11:14:21 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 11:15:34 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 04 May 2023 11:15:34 GMT
ENV TOMCAT_MAJOR=9
# Wed, 10 May 2023 17:56:49 GMT
ENV TOMCAT_VERSION=9.0.75
# Wed, 10 May 2023 17:56:49 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Wed, 10 May 2023 17:56:49 GMT
COPY dir:2a613f9e425d5febc8be5b6c17f49b39f1b8ad84b1601f07f76abed41b25b24b in /usr/local/tomcat 
# Wed, 10 May 2023 17:56:52 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 17:56:54 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 10 May 2023 17:56:54 GMT
EXPOSE 8080
# Wed, 10 May 2023 17:56:54 GMT
CMD ["catalina.sh" "run"]
# Wed, 10 May 2023 18:22:09 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 10 May 2023 18:23:10 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 18:23:13 GMT
ENV XWIKI_VERSION=15.3
# Wed, 10 May 2023 18:23:13 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.3
# Wed, 10 May 2023 18:23:13 GMT
ENV XWIKI_DOWNLOAD_SHA256=fbe35bcc5c6cc5764f2a1da4aca7878531f93bae069d94f399fea7d9656da3b8
# Wed, 10 May 2023 18:23:53 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 10 May 2023 18:25:25 GMT
ENV MARIADB_JDBC_VERSION=3.1.3
# Wed, 10 May 2023 18:25:25 GMT
ENV MARIADB_JDBC_SHA256=11297ee6562426c49c81387c860153cbc131c4c3d042492d4f6d2d97ab3a1ca5
# Wed, 10 May 2023 18:25:25 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.1.3
# Wed, 10 May 2023 18:25:25 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.1.3.jar
# Wed, 10 May 2023 18:25:25 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.1.3.jar
# Wed, 10 May 2023 18:25:26 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Wed, 10 May 2023 18:25:26 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 10 May 2023 18:25:26 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 10 May 2023 18:25:26 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 10 May 2023 18:25:26 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 10 May 2023 18:25:26 GMT
VOLUME [/usr/local/xwiki]
# Wed, 10 May 2023 18:25:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 May 2023 18:25:26 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f3f60f415e9a03eed88bd5dd5268c841cde08dacf16911a3ef1e4e0fcdd76568`  
		Last Modified: Wed, 26 Apr 2023 02:08:37 GMT  
		Size: 28.4 MB (28389440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fb3595122d1cb6fffe722e2624c3c89b00776b393256a5444af56ceda691cf`  
		Last Modified: Thu, 04 May 2023 03:28:13 GMT  
		Size: 12.5 MB (12463858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5542665e33e692b672a405517e6e267c4c6e210bc410b97a6a1ce732618caa87`  
		Last Modified: Thu, 04 May 2023 03:29:19 GMT  
		Size: 45.0 MB (45009401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e52b8550f0ced98adb0880bd041e361ffb69810e6071e6d71eb2ec0c8ecfad5`  
		Last Modified: Thu, 04 May 2023 03:29:14 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea5566732e0a920d0a63e4fbebf073d2c49e3f80716df462e73f895cc0c5dfa`  
		Last Modified: Thu, 04 May 2023 11:24:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c6d16bf5ef403ef11a1cc9e40650f402cd1f8269d16982f7daebc2a76ab0d9`  
		Last Modified: Wed, 10 May 2023 18:03:56 GMT  
		Size: 12.2 MB (12242222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eaf464f1c82b5f85e3173b2c732f0928a28e669fcc4af9eb6da48199e92ae50`  
		Last Modified: Wed, 10 May 2023 18:03:55 GMT  
		Size: 453.7 KB (453682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ef5f2b94b25f2b0f609c429cc1626d9dd857d8294d2d872d6595bdeff3a5ca`  
		Last Modified: Wed, 10 May 2023 18:03:55 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7cc67d2dc8f70f6e05051c0e95eb0de93a45de55ba65c355eedaff2bf118e42`  
		Last Modified: Wed, 10 May 2023 18:27:43 GMT  
		Size: 173.4 MB (173350375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321a150ce2c4526d3d3f5be05b00d833ba0d530e3b594708aeda7ef22c1855a3`  
		Last Modified: Wed, 10 May 2023 18:27:39 GMT  
		Size: 306.2 MB (306214312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b88233cbf990b6d3911be4ac1c98102dab898e81d932d7a8a5af05dc01d2815f`  
		Last Modified: Wed, 10 May 2023 18:28:48 GMT  
		Size: 591.4 KB (591368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d80dd60b9d5f967b2e17e47f926486cc55c29ad8afc7d311694a70ac16cee628`  
		Last Modified: Wed, 10 May 2023 18:28:48 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54f901e61dc9940e28d9d144bc1defd8b0b7cc2618db70202a9192e68bbf9fc`  
		Last Modified: Wed, 10 May 2023 18:28:48 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a61b65e0ea72006075aa51df69871be6a2a03de0f4ae1602592693e7ad4634`  
		Last Modified: Wed, 10 May 2023 18:28:48 GMT  
		Size: 6.0 KB (6000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abdd5570c03cb152fa5a309ffb407bb26a45dd2e6a102316c9cbcb102abbb8e9`  
		Last Modified: Wed, 10 May 2023 18:28:48 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:mysql-tomcat`

```console
$ docker pull xwiki@sha256:64eecc071ed4a6789fa3a37bc7fefe78ae08fad1bd9a7fcb6680991bfe7e0923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:3252b1cffdf08d016b5e82eae75fed4b890197fa6c7afedd85183b898c8a9777
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.2 MB (589196097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a12be474865cce04cbc87bf8db36fdcded4887dc178f49604d68b710d16be056`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 07:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 07:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 07:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 07:26:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:27:16 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 04 May 2023 07:27:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 07:27:40 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 16:13:14 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 04 May 2023 16:13:14 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 16:13:14 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 04 May 2023 16:13:14 GMT
WORKDIR /usr/local/tomcat
# Thu, 04 May 2023 16:13:14 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 16:13:15 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 16:14:45 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 04 May 2023 16:14:45 GMT
ENV TOMCAT_MAJOR=9
# Wed, 10 May 2023 18:01:17 GMT
ENV TOMCAT_VERSION=9.0.75
# Wed, 10 May 2023 18:01:17 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Wed, 10 May 2023 18:01:17 GMT
COPY dir:606cc669e6833afa7967597ca36d4a4497efbb54719c008108649021142d7549 in /usr/local/tomcat 
# Wed, 10 May 2023 18:01:21 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 18:01:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 10 May 2023 18:01:23 GMT
EXPOSE 8080
# Wed, 10 May 2023 18:01:23 GMT
CMD ["catalina.sh" "run"]
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 10 May 2023 18:28:05 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 18:28:06 GMT
ENV XWIKI_VERSION=15.3
# Wed, 10 May 2023 18:28:06 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.3
# Wed, 10 May 2023 18:28:06 GMT
ENV XWIKI_DOWNLOAD_SHA256=fbe35bcc5c6cc5764f2a1da4aca7878531f93bae069d94f399fea7d9656da3b8
# Wed, 10 May 2023 18:28:44 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 10 May 2023 18:28:45 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Wed, 10 May 2023 18:28:45 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Wed, 10 May 2023 18:28:45 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Wed, 10 May 2023 18:28:45 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Wed, 10 May 2023 18:28:45 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Wed, 10 May 2023 18:28:46 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Wed, 10 May 2023 18:28:46 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 10 May 2023 18:28:46 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 10 May 2023 18:28:47 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 10 May 2023 18:28:47 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 10 May 2023 18:28:47 GMT
VOLUME [/usr/local/xwiki]
# Wed, 10 May 2023 18:28:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 May 2023 18:28:47 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458b02b5411a07f3b354cde2b461caffc1bb184a3413b5736a9e67ee87cb28b2`  
		Last Modified: Thu, 04 May 2023 07:30:02 GMT  
		Size: 12.5 MB (12504170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04a165ead1d5eabe89dc88e53286af89caab22a5d20c53007b9e6e508affb4b`  
		Last Modified: Thu, 04 May 2023 07:31:19 GMT  
		Size: 46.7 MB (46666270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1187c73b18505bd4495bc03ccbdb723388dfe4d633fd12be845dfe8e253e48e2`  
		Last Modified: Thu, 04 May 2023 07:31:12 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c833cbb14374cde014505e77f6a6122773984a691844e4138fc15cae99ba625`  
		Last Modified: Thu, 04 May 2023 16:24:19 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439ac04571c77c4330db518bc8f35b70f8723246ed34c98787f7ac8d7dc30b42`  
		Last Modified: Wed, 10 May 2023 18:09:06 GMT  
		Size: 12.2 MB (12236613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8e775ba0b76c6692c0b9211e4b94653ba2aa16fdc7a5e3347aba962b684508`  
		Last Modified: Wed, 10 May 2023 18:09:06 GMT  
		Size: 454.2 KB (454222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee5c1ba4848e97d4e3c43d9d4bca0eeeccf2d5d7f6d805d748da4a7d24ad14e`  
		Last Modified: Wed, 10 May 2023 18:09:05 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffadd10be916fc5729676141f5d0ba6aa30968b75555790e449d4988dc81332a`  
		Last Modified: Wed, 10 May 2023 18:32:42 GMT  
		Size: 178.3 MB (178334017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a29002da219be23e789ef538aeaae1d2296399cdfa64c6c2ed7438210947d7`  
		Last Modified: Wed, 10 May 2023 18:32:34 GMT  
		Size: 306.2 MB (306214302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628263d6dd0a28e03148683703ead7b3c5ef0abd589af1c7352f58aadb9c01a8`  
		Last Modified: Wed, 10 May 2023 18:32:17 GMT  
		Size: 2.3 MB (2343663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81942c3829003d54f85f9d0e3d4fb84d03f7db66060cdd1d2a6a812ce516ccd6`  
		Last Modified: Wed, 10 May 2023 18:32:17 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e635acc63235269abedf51ee8315a58bbb09ff0cbd90f9c6f68c6ea5269d909`  
		Last Modified: Wed, 10 May 2023 18:32:17 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e905c9c0de831ffb2222e8e0420b569e8658457adc3ae299482d6ad73bdb3abb`  
		Last Modified: Wed, 10 May 2023 18:32:17 GMT  
		Size: 6.0 KB (6003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3459a44ee12986d9a54da5b087233e6dfe71171061ce1a63376de231c25ea842`  
		Last Modified: Wed, 10 May 2023 18:32:17 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:mysql-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:156f67756ea75d27982bd550fe642c9e9bea5cf04a008f6d3e5af5d2343ca83b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.5 MB (580479573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab46181cab4d5b59fc90bad1883f22f0f812a647a62e801240dfa51c485ed1b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 25 Apr 2023 17:31:58 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:31:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:31:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:31:59 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:32:02 GMT
ADD file:aee0d7770ef2f24dc9697e86d391529d001a4013b6e30a3ac90a57932814a57e in / 
# Tue, 25 Apr 2023 17:32:02 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 03:25:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 03:25:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 03:25:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 03:25:23 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 03:25:47 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 04 May 2023 03:26:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 03:26:10 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 11:14:20 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 04 May 2023 11:14:20 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 11:14:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 04 May 2023 11:14:21 GMT
WORKDIR /usr/local/tomcat
# Thu, 04 May 2023 11:14:21 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 11:14:21 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 11:15:34 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 04 May 2023 11:15:34 GMT
ENV TOMCAT_MAJOR=9
# Wed, 10 May 2023 17:56:49 GMT
ENV TOMCAT_VERSION=9.0.75
# Wed, 10 May 2023 17:56:49 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Wed, 10 May 2023 17:56:49 GMT
COPY dir:2a613f9e425d5febc8be5b6c17f49b39f1b8ad84b1601f07f76abed41b25b24b in /usr/local/tomcat 
# Wed, 10 May 2023 17:56:52 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 17:56:54 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 10 May 2023 17:56:54 GMT
EXPOSE 8080
# Wed, 10 May 2023 17:56:54 GMT
CMD ["catalina.sh" "run"]
# Wed, 10 May 2023 18:22:09 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 10 May 2023 18:23:10 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 18:23:13 GMT
ENV XWIKI_VERSION=15.3
# Wed, 10 May 2023 18:23:13 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.3
# Wed, 10 May 2023 18:23:13 GMT
ENV XWIKI_DOWNLOAD_SHA256=fbe35bcc5c6cc5764f2a1da4aca7878531f93bae069d94f399fea7d9656da3b8
# Wed, 10 May 2023 18:23:53 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 10 May 2023 18:23:55 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Wed, 10 May 2023 18:23:55 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Wed, 10 May 2023 18:23:55 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Wed, 10 May 2023 18:23:56 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Wed, 10 May 2023 18:23:56 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Wed, 10 May 2023 18:23:56 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Wed, 10 May 2023 18:23:56 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 10 May 2023 18:23:57 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 10 May 2023 18:23:57 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 10 May 2023 18:23:57 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 10 May 2023 18:23:57 GMT
VOLUME [/usr/local/xwiki]
# Wed, 10 May 2023 18:23:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 May 2023 18:23:57 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f3f60f415e9a03eed88bd5dd5268c841cde08dacf16911a3ef1e4e0fcdd76568`  
		Last Modified: Wed, 26 Apr 2023 02:08:37 GMT  
		Size: 28.4 MB (28389440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fb3595122d1cb6fffe722e2624c3c89b00776b393256a5444af56ceda691cf`  
		Last Modified: Thu, 04 May 2023 03:28:13 GMT  
		Size: 12.5 MB (12463858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5542665e33e692b672a405517e6e267c4c6e210bc410b97a6a1ce732618caa87`  
		Last Modified: Thu, 04 May 2023 03:29:19 GMT  
		Size: 45.0 MB (45009401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e52b8550f0ced98adb0880bd041e361ffb69810e6071e6d71eb2ec0c8ecfad5`  
		Last Modified: Thu, 04 May 2023 03:29:14 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea5566732e0a920d0a63e4fbebf073d2c49e3f80716df462e73f895cc0c5dfa`  
		Last Modified: Thu, 04 May 2023 11:24:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c6d16bf5ef403ef11a1cc9e40650f402cd1f8269d16982f7daebc2a76ab0d9`  
		Last Modified: Wed, 10 May 2023 18:03:56 GMT  
		Size: 12.2 MB (12242222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eaf464f1c82b5f85e3173b2c732f0928a28e669fcc4af9eb6da48199e92ae50`  
		Last Modified: Wed, 10 May 2023 18:03:55 GMT  
		Size: 453.7 KB (453682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ef5f2b94b25f2b0f609c429cc1626d9dd857d8294d2d872d6595bdeff3a5ca`  
		Last Modified: Wed, 10 May 2023 18:03:55 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7cc67d2dc8f70f6e05051c0e95eb0de93a45de55ba65c355eedaff2bf118e42`  
		Last Modified: Wed, 10 May 2023 18:27:43 GMT  
		Size: 173.4 MB (173350375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321a150ce2c4526d3d3f5be05b00d833ba0d530e3b594708aeda7ef22c1855a3`  
		Last Modified: Wed, 10 May 2023 18:27:39 GMT  
		Size: 306.2 MB (306214312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de8537cceb0f08c97a9244c93c7142180f99d25a07a008c897b3e7f2e01749f5`  
		Last Modified: Wed, 10 May 2023 18:27:25 GMT  
		Size: 2.3 MB (2343667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:174ceadf9884a59c863a2f45bc8a9d2c877073089ab2293ec28b4a890edbd549`  
		Last Modified: Wed, 10 May 2023 18:27:25 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4340d0afded864299aaa098ecb92231c246d875fd05e7babc4eb574c24aba63`  
		Last Modified: Wed, 10 May 2023 18:27:25 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ff6fb98971adf0b973b7c902a39cadccb245e656dc8470ec75d8e115e335c0`  
		Last Modified: Wed, 10 May 2023 18:27:25 GMT  
		Size: 6.0 KB (6000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e40c1aaebc8527a9ad709da10958451577ca896b6c968e0e49daf1cc4f790ddd`  
		Last Modified: Wed, 10 May 2023 18:27:25 GMT  
		Size: 2.5 KB (2503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:postgres-tomcat`

```console
$ docker pull xwiki@sha256:735933782d363352e7012650659093d08fb0ad9b2fdf0bf6f481f6a6007e57e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:2900c897a5a066bba2d94f8c0328bda225a94fe5d86155f565d8a024e15967ac
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **588.7 MB (588732305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ea08c636ebabfa7d8491ee29125599e2839801fa05ae791780a490474746bef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 07:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 07:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 07:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 07:26:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:27:16 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 04 May 2023 07:27:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 07:27:40 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 16:13:14 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 04 May 2023 16:13:14 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 16:13:14 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 04 May 2023 16:13:14 GMT
WORKDIR /usr/local/tomcat
# Thu, 04 May 2023 16:13:14 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 16:13:15 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 16:14:45 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 04 May 2023 16:14:45 GMT
ENV TOMCAT_MAJOR=9
# Wed, 10 May 2023 18:01:17 GMT
ENV TOMCAT_VERSION=9.0.75
# Wed, 10 May 2023 18:01:17 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Wed, 10 May 2023 18:01:17 GMT
COPY dir:606cc669e6833afa7967597ca36d4a4497efbb54719c008108649021142d7549 in /usr/local/tomcat 
# Wed, 10 May 2023 18:01:21 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 18:01:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 10 May 2023 18:01:23 GMT
EXPOSE 8080
# Wed, 10 May 2023 18:01:23 GMT
CMD ["catalina.sh" "run"]
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 10 May 2023 18:29:15 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 18:29:16 GMT
ENV XWIKI_VERSION=15.3
# Wed, 10 May 2023 18:29:16 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.3
# Wed, 10 May 2023 18:29:16 GMT
ENV XWIKI_DOWNLOAD_SHA256=fbe35bcc5c6cc5764f2a1da4aca7878531f93bae069d94f399fea7d9656da3b8
# Wed, 10 May 2023 18:29:56 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 10 May 2023 18:29:58 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Wed, 10 May 2023 18:29:58 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 10 May 2023 18:29:58 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 10 May 2023 18:29:58 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 10 May 2023 18:29:58 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 10 May 2023 18:29:59 GMT
VOLUME [/usr/local/xwiki]
# Wed, 10 May 2023 18:29:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 May 2023 18:29:59 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458b02b5411a07f3b354cde2b461caffc1bb184a3413b5736a9e67ee87cb28b2`  
		Last Modified: Thu, 04 May 2023 07:30:02 GMT  
		Size: 12.5 MB (12504170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04a165ead1d5eabe89dc88e53286af89caab22a5d20c53007b9e6e508affb4b`  
		Last Modified: Thu, 04 May 2023 07:31:19 GMT  
		Size: 46.7 MB (46666270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1187c73b18505bd4495bc03ccbdb723388dfe4d633fd12be845dfe8e253e48e2`  
		Last Modified: Thu, 04 May 2023 07:31:12 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c833cbb14374cde014505e77f6a6122773984a691844e4138fc15cae99ba625`  
		Last Modified: Thu, 04 May 2023 16:24:19 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439ac04571c77c4330db518bc8f35b70f8723246ed34c98787f7ac8d7dc30b42`  
		Last Modified: Wed, 10 May 2023 18:09:06 GMT  
		Size: 12.2 MB (12236613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8e775ba0b76c6692c0b9211e4b94653ba2aa16fdc7a5e3347aba962b684508`  
		Last Modified: Wed, 10 May 2023 18:09:06 GMT  
		Size: 454.2 KB (454222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee5c1ba4848e97d4e3c43d9d4bca0eeeccf2d5d7f6d805d748da4a7d24ad14e`  
		Last Modified: Wed, 10 May 2023 18:09:05 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29abf03d18e0bc34be536fce36ea27d0012a4d330eed44003684563b4d891b2d`  
		Last Modified: Wed, 10 May 2023 18:33:36 GMT  
		Size: 179.3 MB (179276853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04893bb957c480bd2610cdfdf9d8ce54f10892dc666a3f546d0a47e08a8b6bf3`  
		Last Modified: Wed, 10 May 2023 18:33:28 GMT  
		Size: 306.2 MB (306214334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c733bdd07cccb12e268038f38cc2208c02cab00afde7af1103ad9ab1d34ddc49`  
		Last Modified: Wed, 10 May 2023 18:33:11 GMT  
		Size: 936.9 KB (936851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:308d5fe9ecebf8518e4a3354dfd14989f5a913a5a8d7a6abec2afaca25ea32ac`  
		Last Modified: Wed, 10 May 2023 18:33:11 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3080392f0ef7aac169f05c443bbff282a8f4c46dbf39c2f91bd942f63c4296e4`  
		Last Modified: Wed, 10 May 2023 18:33:11 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cde226d897c8670f291d599b6ddecdece884739dc8e4f66874764aa1a46fd4a`  
		Last Modified: Wed, 10 May 2023 18:33:11 GMT  
		Size: 6.0 KB (6002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:552d5c735b1472b69f77b166b9824e3f6cee95760872d8f8c00958e81a510428`  
		Last Modified: Wed, 10 May 2023 18:33:11 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:10bfb120c331e4fd20b20348ab4270888db1418737568c832e5dbb489577d754
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.0 MB (580013492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e62cc10c58ce901b71a525883c5fac34e70c79f319bbce13405788bcaa52e78a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 25 Apr 2023 17:31:58 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:31:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:31:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:31:59 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:32:02 GMT
ADD file:aee0d7770ef2f24dc9697e86d391529d001a4013b6e30a3ac90a57932814a57e in / 
# Tue, 25 Apr 2023 17:32:02 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 03:25:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 03:25:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 03:25:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 03:25:23 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 03:25:47 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 04 May 2023 03:26:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 03:26:10 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 11:14:20 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 04 May 2023 11:14:20 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 11:14:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 04 May 2023 11:14:21 GMT
WORKDIR /usr/local/tomcat
# Thu, 04 May 2023 11:14:21 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 11:14:21 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 11:15:34 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 04 May 2023 11:15:34 GMT
ENV TOMCAT_MAJOR=9
# Wed, 10 May 2023 17:56:49 GMT
ENV TOMCAT_VERSION=9.0.75
# Wed, 10 May 2023 17:56:49 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Wed, 10 May 2023 17:56:49 GMT
COPY dir:2a613f9e425d5febc8be5b6c17f49b39f1b8ad84b1601f07f76abed41b25b24b in /usr/local/tomcat 
# Wed, 10 May 2023 17:56:52 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 17:56:54 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 10 May 2023 17:56:54 GMT
EXPOSE 8080
# Wed, 10 May 2023 17:56:54 GMT
CMD ["catalina.sh" "run"]
# Wed, 10 May 2023 18:22:09 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 10 May 2023 18:24:24 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 18:24:27 GMT
ENV XWIKI_VERSION=15.3
# Wed, 10 May 2023 18:24:28 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.3
# Wed, 10 May 2023 18:24:28 GMT
ENV XWIKI_DOWNLOAD_SHA256=fbe35bcc5c6cc5764f2a1da4aca7878531f93bae069d94f399fea7d9656da3b8
# Wed, 10 May 2023 18:25:07 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 10 May 2023 18:25:10 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Wed, 10 May 2023 18:25:10 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 10 May 2023 18:25:10 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 10 May 2023 18:25:11 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 10 May 2023 18:25:11 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 10 May 2023 18:25:11 GMT
VOLUME [/usr/local/xwiki]
# Wed, 10 May 2023 18:25:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 May 2023 18:25:11 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f3f60f415e9a03eed88bd5dd5268c841cde08dacf16911a3ef1e4e0fcdd76568`  
		Last Modified: Wed, 26 Apr 2023 02:08:37 GMT  
		Size: 28.4 MB (28389440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fb3595122d1cb6fffe722e2624c3c89b00776b393256a5444af56ceda691cf`  
		Last Modified: Thu, 04 May 2023 03:28:13 GMT  
		Size: 12.5 MB (12463858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5542665e33e692b672a405517e6e267c4c6e210bc410b97a6a1ce732618caa87`  
		Last Modified: Thu, 04 May 2023 03:29:19 GMT  
		Size: 45.0 MB (45009401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e52b8550f0ced98adb0880bd041e361ffb69810e6071e6d71eb2ec0c8ecfad5`  
		Last Modified: Thu, 04 May 2023 03:29:14 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea5566732e0a920d0a63e4fbebf073d2c49e3f80716df462e73f895cc0c5dfa`  
		Last Modified: Thu, 04 May 2023 11:24:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c6d16bf5ef403ef11a1cc9e40650f402cd1f8269d16982f7daebc2a76ab0d9`  
		Last Modified: Wed, 10 May 2023 18:03:56 GMT  
		Size: 12.2 MB (12242222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eaf464f1c82b5f85e3173b2c732f0928a28e669fcc4af9eb6da48199e92ae50`  
		Last Modified: Wed, 10 May 2023 18:03:55 GMT  
		Size: 453.7 KB (453682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ef5f2b94b25f2b0f609c429cc1626d9dd857d8294d2d872d6595bdeff3a5ca`  
		Last Modified: Wed, 10 May 2023 18:03:55 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e76b785cabb7a84968f4d713d3072c255796ddcef576690d954e3fc5b1a09604`  
		Last Modified: Wed, 10 May 2023 18:28:29 GMT  
		Size: 174.3 MB (174290936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bbb1bea6fd7e5ad54d9a435449598eab16234ad43ac144f2e8bfd3d6ba08f53`  
		Last Modified: Wed, 10 May 2023 18:28:26 GMT  
		Size: 306.2 MB (306214328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ec4bf084be2f31ea6d132041630e63267918cd9d3fda2c1c5729796be49ca3`  
		Last Modified: Wed, 10 May 2023 18:28:12 GMT  
		Size: 936.9 KB (936850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35482f801e8bffd20763dc900fe57a71e0b8b6e9704fc5960d1ae5c49c36568f`  
		Last Modified: Wed, 10 May 2023 18:28:12 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73fefab11cdaf813c0992abeb9546ca3853626b0c153d8792dda45700405f9d7`  
		Last Modified: Wed, 10 May 2023 18:28:12 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510da944c55d824606569a712e2defc95041c832ea8b07bd45aca2bf455095c2`  
		Last Modified: Wed, 10 May 2023 18:28:12 GMT  
		Size: 6.0 KB (6005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60c6d213e30aaeb6555c54770342ec9de274eb11eff3007dc29f2d552d0dd36c`  
		Last Modified: Wed, 10 May 2023 18:28:12 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:stable`

```console
$ docker pull xwiki@sha256:64eecc071ed4a6789fa3a37bc7fefe78ae08fad1bd9a7fcb6680991bfe7e0923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:stable` - linux; amd64

```console
$ docker pull xwiki@sha256:3252b1cffdf08d016b5e82eae75fed4b890197fa6c7afedd85183b898c8a9777
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.2 MB (589196097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a12be474865cce04cbc87bf8db36fdcded4887dc178f49604d68b710d16be056`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 07:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 07:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 07:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 07:26:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:27:16 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 04 May 2023 07:27:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 07:27:40 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 16:13:14 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 04 May 2023 16:13:14 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 16:13:14 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 04 May 2023 16:13:14 GMT
WORKDIR /usr/local/tomcat
# Thu, 04 May 2023 16:13:14 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 16:13:15 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 16:14:45 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 04 May 2023 16:14:45 GMT
ENV TOMCAT_MAJOR=9
# Wed, 10 May 2023 18:01:17 GMT
ENV TOMCAT_VERSION=9.0.75
# Wed, 10 May 2023 18:01:17 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Wed, 10 May 2023 18:01:17 GMT
COPY dir:606cc669e6833afa7967597ca36d4a4497efbb54719c008108649021142d7549 in /usr/local/tomcat 
# Wed, 10 May 2023 18:01:21 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 18:01:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 10 May 2023 18:01:23 GMT
EXPOSE 8080
# Wed, 10 May 2023 18:01:23 GMT
CMD ["catalina.sh" "run"]
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 10 May 2023 18:28:05 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 18:28:06 GMT
ENV XWIKI_VERSION=15.3
# Wed, 10 May 2023 18:28:06 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.3
# Wed, 10 May 2023 18:28:06 GMT
ENV XWIKI_DOWNLOAD_SHA256=fbe35bcc5c6cc5764f2a1da4aca7878531f93bae069d94f399fea7d9656da3b8
# Wed, 10 May 2023 18:28:44 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 10 May 2023 18:28:45 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Wed, 10 May 2023 18:28:45 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Wed, 10 May 2023 18:28:45 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Wed, 10 May 2023 18:28:45 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Wed, 10 May 2023 18:28:45 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Wed, 10 May 2023 18:28:46 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Wed, 10 May 2023 18:28:46 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 10 May 2023 18:28:46 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 10 May 2023 18:28:47 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 10 May 2023 18:28:47 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 10 May 2023 18:28:47 GMT
VOLUME [/usr/local/xwiki]
# Wed, 10 May 2023 18:28:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 May 2023 18:28:47 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458b02b5411a07f3b354cde2b461caffc1bb184a3413b5736a9e67ee87cb28b2`  
		Last Modified: Thu, 04 May 2023 07:30:02 GMT  
		Size: 12.5 MB (12504170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04a165ead1d5eabe89dc88e53286af89caab22a5d20c53007b9e6e508affb4b`  
		Last Modified: Thu, 04 May 2023 07:31:19 GMT  
		Size: 46.7 MB (46666270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1187c73b18505bd4495bc03ccbdb723388dfe4d633fd12be845dfe8e253e48e2`  
		Last Modified: Thu, 04 May 2023 07:31:12 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c833cbb14374cde014505e77f6a6122773984a691844e4138fc15cae99ba625`  
		Last Modified: Thu, 04 May 2023 16:24:19 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439ac04571c77c4330db518bc8f35b70f8723246ed34c98787f7ac8d7dc30b42`  
		Last Modified: Wed, 10 May 2023 18:09:06 GMT  
		Size: 12.2 MB (12236613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8e775ba0b76c6692c0b9211e4b94653ba2aa16fdc7a5e3347aba962b684508`  
		Last Modified: Wed, 10 May 2023 18:09:06 GMT  
		Size: 454.2 KB (454222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee5c1ba4848e97d4e3c43d9d4bca0eeeccf2d5d7f6d805d748da4a7d24ad14e`  
		Last Modified: Wed, 10 May 2023 18:09:05 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffadd10be916fc5729676141f5d0ba6aa30968b75555790e449d4988dc81332a`  
		Last Modified: Wed, 10 May 2023 18:32:42 GMT  
		Size: 178.3 MB (178334017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a29002da219be23e789ef538aeaae1d2296399cdfa64c6c2ed7438210947d7`  
		Last Modified: Wed, 10 May 2023 18:32:34 GMT  
		Size: 306.2 MB (306214302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628263d6dd0a28e03148683703ead7b3c5ef0abd589af1c7352f58aadb9c01a8`  
		Last Modified: Wed, 10 May 2023 18:32:17 GMT  
		Size: 2.3 MB (2343663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81942c3829003d54f85f9d0e3d4fb84d03f7db66060cdd1d2a6a812ce516ccd6`  
		Last Modified: Wed, 10 May 2023 18:32:17 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e635acc63235269abedf51ee8315a58bbb09ff0cbd90f9c6f68c6ea5269d909`  
		Last Modified: Wed, 10 May 2023 18:32:17 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e905c9c0de831ffb2222e8e0420b569e8658457adc3ae299482d6ad73bdb3abb`  
		Last Modified: Wed, 10 May 2023 18:32:17 GMT  
		Size: 6.0 KB (6003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3459a44ee12986d9a54da5b087233e6dfe71171061ce1a63376de231c25ea842`  
		Last Modified: Wed, 10 May 2023 18:32:17 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:stable` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:156f67756ea75d27982bd550fe642c9e9bea5cf04a008f6d3e5af5d2343ca83b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.5 MB (580479573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab46181cab4d5b59fc90bad1883f22f0f812a647a62e801240dfa51c485ed1b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 25 Apr 2023 17:31:58 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:31:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:31:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:31:59 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:32:02 GMT
ADD file:aee0d7770ef2f24dc9697e86d391529d001a4013b6e30a3ac90a57932814a57e in / 
# Tue, 25 Apr 2023 17:32:02 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 03:25:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 03:25:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 03:25:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 03:25:23 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 03:25:47 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 04 May 2023 03:26:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 03:26:10 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 11:14:20 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 04 May 2023 11:14:20 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 11:14:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 04 May 2023 11:14:21 GMT
WORKDIR /usr/local/tomcat
# Thu, 04 May 2023 11:14:21 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 11:14:21 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 11:15:34 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 04 May 2023 11:15:34 GMT
ENV TOMCAT_MAJOR=9
# Wed, 10 May 2023 17:56:49 GMT
ENV TOMCAT_VERSION=9.0.75
# Wed, 10 May 2023 17:56:49 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Wed, 10 May 2023 17:56:49 GMT
COPY dir:2a613f9e425d5febc8be5b6c17f49b39f1b8ad84b1601f07f76abed41b25b24b in /usr/local/tomcat 
# Wed, 10 May 2023 17:56:52 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 17:56:54 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 10 May 2023 17:56:54 GMT
EXPOSE 8080
# Wed, 10 May 2023 17:56:54 GMT
CMD ["catalina.sh" "run"]
# Wed, 10 May 2023 18:22:09 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 10 May 2023 18:23:10 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 18:23:13 GMT
ENV XWIKI_VERSION=15.3
# Wed, 10 May 2023 18:23:13 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.3
# Wed, 10 May 2023 18:23:13 GMT
ENV XWIKI_DOWNLOAD_SHA256=fbe35bcc5c6cc5764f2a1da4aca7878531f93bae069d94f399fea7d9656da3b8
# Wed, 10 May 2023 18:23:53 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 10 May 2023 18:23:55 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Wed, 10 May 2023 18:23:55 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Wed, 10 May 2023 18:23:55 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Wed, 10 May 2023 18:23:56 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Wed, 10 May 2023 18:23:56 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Wed, 10 May 2023 18:23:56 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Wed, 10 May 2023 18:23:56 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 10 May 2023 18:23:57 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 10 May 2023 18:23:57 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 10 May 2023 18:23:57 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 10 May 2023 18:23:57 GMT
VOLUME [/usr/local/xwiki]
# Wed, 10 May 2023 18:23:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 May 2023 18:23:57 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f3f60f415e9a03eed88bd5dd5268c841cde08dacf16911a3ef1e4e0fcdd76568`  
		Last Modified: Wed, 26 Apr 2023 02:08:37 GMT  
		Size: 28.4 MB (28389440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fb3595122d1cb6fffe722e2624c3c89b00776b393256a5444af56ceda691cf`  
		Last Modified: Thu, 04 May 2023 03:28:13 GMT  
		Size: 12.5 MB (12463858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5542665e33e692b672a405517e6e267c4c6e210bc410b97a6a1ce732618caa87`  
		Last Modified: Thu, 04 May 2023 03:29:19 GMT  
		Size: 45.0 MB (45009401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e52b8550f0ced98adb0880bd041e361ffb69810e6071e6d71eb2ec0c8ecfad5`  
		Last Modified: Thu, 04 May 2023 03:29:14 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea5566732e0a920d0a63e4fbebf073d2c49e3f80716df462e73f895cc0c5dfa`  
		Last Modified: Thu, 04 May 2023 11:24:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c6d16bf5ef403ef11a1cc9e40650f402cd1f8269d16982f7daebc2a76ab0d9`  
		Last Modified: Wed, 10 May 2023 18:03:56 GMT  
		Size: 12.2 MB (12242222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eaf464f1c82b5f85e3173b2c732f0928a28e669fcc4af9eb6da48199e92ae50`  
		Last Modified: Wed, 10 May 2023 18:03:55 GMT  
		Size: 453.7 KB (453682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ef5f2b94b25f2b0f609c429cc1626d9dd857d8294d2d872d6595bdeff3a5ca`  
		Last Modified: Wed, 10 May 2023 18:03:55 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7cc67d2dc8f70f6e05051c0e95eb0de93a45de55ba65c355eedaff2bf118e42`  
		Last Modified: Wed, 10 May 2023 18:27:43 GMT  
		Size: 173.4 MB (173350375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321a150ce2c4526d3d3f5be05b00d833ba0d530e3b594708aeda7ef22c1855a3`  
		Last Modified: Wed, 10 May 2023 18:27:39 GMT  
		Size: 306.2 MB (306214312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de8537cceb0f08c97a9244c93c7142180f99d25a07a008c897b3e7f2e01749f5`  
		Last Modified: Wed, 10 May 2023 18:27:25 GMT  
		Size: 2.3 MB (2343667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:174ceadf9884a59c863a2f45bc8a9d2c877073089ab2293ec28b4a890edbd549`  
		Last Modified: Wed, 10 May 2023 18:27:25 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4340d0afded864299aaa098ecb92231c246d875fd05e7babc4eb574c24aba63`  
		Last Modified: Wed, 10 May 2023 18:27:25 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ff6fb98971adf0b973b7c902a39cadccb245e656dc8470ec75d8e115e335c0`  
		Last Modified: Wed, 10 May 2023 18:27:25 GMT  
		Size: 6.0 KB (6000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e40c1aaebc8527a9ad709da10958451577ca896b6c968e0e49daf1cc4f790ddd`  
		Last Modified: Wed, 10 May 2023 18:27:25 GMT  
		Size: 2.5 KB (2503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:stable-mariadb`

```console
$ docker pull xwiki@sha256:ba65c6db6cbf680842f048e25f348c8981c5b4295810467e68a3df22f2c0ef77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:stable-mariadb` - linux; amd64

```console
$ docker pull xwiki@sha256:9dc755ce1b9a1d005e8b42c492573371e37310a9960b9b7becc88e7744b5a1b7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **587.4 MB (587443810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9bff1a50bba5fc8078ed4a8574445fb147d50e1d8bd49b788f4954dd1da4132`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 07:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 07:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 07:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 07:26:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:27:16 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 04 May 2023 07:27:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 07:27:40 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 16:13:14 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 04 May 2023 16:13:14 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 16:13:14 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 04 May 2023 16:13:14 GMT
WORKDIR /usr/local/tomcat
# Thu, 04 May 2023 16:13:14 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 16:13:15 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 16:14:45 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 04 May 2023 16:14:45 GMT
ENV TOMCAT_MAJOR=9
# Wed, 10 May 2023 18:01:17 GMT
ENV TOMCAT_VERSION=9.0.75
# Wed, 10 May 2023 18:01:17 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Wed, 10 May 2023 18:01:17 GMT
COPY dir:606cc669e6833afa7967597ca36d4a4497efbb54719c008108649021142d7549 in /usr/local/tomcat 
# Wed, 10 May 2023 18:01:21 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 18:01:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 10 May 2023 18:01:23 GMT
EXPOSE 8080
# Wed, 10 May 2023 18:01:23 GMT
CMD ["catalina.sh" "run"]
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 10 May 2023 18:28:05 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 18:28:06 GMT
ENV XWIKI_VERSION=15.3
# Wed, 10 May 2023 18:28:06 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.3
# Wed, 10 May 2023 18:28:06 GMT
ENV XWIKI_DOWNLOAD_SHA256=fbe35bcc5c6cc5764f2a1da4aca7878531f93bae069d94f399fea7d9656da3b8
# Wed, 10 May 2023 18:28:44 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 10 May 2023 18:30:14 GMT
ENV MARIADB_JDBC_VERSION=3.1.3
# Wed, 10 May 2023 18:30:14 GMT
ENV MARIADB_JDBC_SHA256=11297ee6562426c49c81387c860153cbc131c4c3d042492d4f6d2d97ab3a1ca5
# Wed, 10 May 2023 18:30:14 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.1.3
# Wed, 10 May 2023 18:30:14 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.1.3.jar
# Wed, 10 May 2023 18:30:15 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.1.3.jar
# Wed, 10 May 2023 18:30:15 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Wed, 10 May 2023 18:30:15 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 10 May 2023 18:30:16 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 10 May 2023 18:30:16 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 10 May 2023 18:30:16 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 10 May 2023 18:30:16 GMT
VOLUME [/usr/local/xwiki]
# Wed, 10 May 2023 18:30:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 May 2023 18:30:16 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458b02b5411a07f3b354cde2b461caffc1bb184a3413b5736a9e67ee87cb28b2`  
		Last Modified: Thu, 04 May 2023 07:30:02 GMT  
		Size: 12.5 MB (12504170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04a165ead1d5eabe89dc88e53286af89caab22a5d20c53007b9e6e508affb4b`  
		Last Modified: Thu, 04 May 2023 07:31:19 GMT  
		Size: 46.7 MB (46666270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1187c73b18505bd4495bc03ccbdb723388dfe4d633fd12be845dfe8e253e48e2`  
		Last Modified: Thu, 04 May 2023 07:31:12 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c833cbb14374cde014505e77f6a6122773984a691844e4138fc15cae99ba625`  
		Last Modified: Thu, 04 May 2023 16:24:19 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439ac04571c77c4330db518bc8f35b70f8723246ed34c98787f7ac8d7dc30b42`  
		Last Modified: Wed, 10 May 2023 18:09:06 GMT  
		Size: 12.2 MB (12236613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8e775ba0b76c6692c0b9211e4b94653ba2aa16fdc7a5e3347aba962b684508`  
		Last Modified: Wed, 10 May 2023 18:09:06 GMT  
		Size: 454.2 KB (454222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee5c1ba4848e97d4e3c43d9d4bca0eeeccf2d5d7f6d805d748da4a7d24ad14e`  
		Last Modified: Wed, 10 May 2023 18:09:05 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffadd10be916fc5729676141f5d0ba6aa30968b75555790e449d4988dc81332a`  
		Last Modified: Wed, 10 May 2023 18:32:42 GMT  
		Size: 178.3 MB (178334017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a29002da219be23e789ef538aeaae1d2296399cdfa64c6c2ed7438210947d7`  
		Last Modified: Wed, 10 May 2023 18:32:34 GMT  
		Size: 306.2 MB (306214302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:552f4dcf26ef5ef3b3a7315cc47f3dc07974cb0684775dc9f2d390f7b19be181`  
		Last Modified: Wed, 10 May 2023 18:33:53 GMT  
		Size: 591.4 KB (591369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:647b04728750fccef49babf80ba8257ced3661baa001e9e8a73067bea60c3784`  
		Last Modified: Wed, 10 May 2023 18:33:53 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bcdcc6da901312c0e56c818dfec97184f4cf9e78308964322dba08f16215da0`  
		Last Modified: Wed, 10 May 2023 18:33:53 GMT  
		Size: 2.3 KB (2312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e34abf77fe47a0d97eb01a41d2e6a9b8c0db4e9dfa284dfc767e1d9287b1effe`  
		Last Modified: Wed, 10 May 2023 18:33:53 GMT  
		Size: 6.0 KB (6005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e5b8636c37250081b1a1fd47f2ab5926692c75a635a5b3f805ed897fddb43b`  
		Last Modified: Wed, 10 May 2023 18:33:53 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:stable-mariadb` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:8ba7073b3049679fb036a6d00a78b2b70da792b9cde40df0cc088094dc3a3d59
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.7 MB (578727276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c23d916ce05444c655cb6c876c29ee4fe78165b88d66fad2613ac17dcb7b9924`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 25 Apr 2023 17:31:58 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:31:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:31:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:31:59 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:32:02 GMT
ADD file:aee0d7770ef2f24dc9697e86d391529d001a4013b6e30a3ac90a57932814a57e in / 
# Tue, 25 Apr 2023 17:32:02 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 03:25:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 03:25:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 03:25:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 03:25:23 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 03:25:47 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 04 May 2023 03:26:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 03:26:10 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 11:14:20 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 04 May 2023 11:14:20 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 11:14:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 04 May 2023 11:14:21 GMT
WORKDIR /usr/local/tomcat
# Thu, 04 May 2023 11:14:21 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 11:14:21 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 11:15:34 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 04 May 2023 11:15:34 GMT
ENV TOMCAT_MAJOR=9
# Wed, 10 May 2023 17:56:49 GMT
ENV TOMCAT_VERSION=9.0.75
# Wed, 10 May 2023 17:56:49 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Wed, 10 May 2023 17:56:49 GMT
COPY dir:2a613f9e425d5febc8be5b6c17f49b39f1b8ad84b1601f07f76abed41b25b24b in /usr/local/tomcat 
# Wed, 10 May 2023 17:56:52 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 17:56:54 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 10 May 2023 17:56:54 GMT
EXPOSE 8080
# Wed, 10 May 2023 17:56:54 GMT
CMD ["catalina.sh" "run"]
# Wed, 10 May 2023 18:22:09 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 10 May 2023 18:23:10 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 18:23:13 GMT
ENV XWIKI_VERSION=15.3
# Wed, 10 May 2023 18:23:13 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.3
# Wed, 10 May 2023 18:23:13 GMT
ENV XWIKI_DOWNLOAD_SHA256=fbe35bcc5c6cc5764f2a1da4aca7878531f93bae069d94f399fea7d9656da3b8
# Wed, 10 May 2023 18:23:53 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 10 May 2023 18:25:25 GMT
ENV MARIADB_JDBC_VERSION=3.1.3
# Wed, 10 May 2023 18:25:25 GMT
ENV MARIADB_JDBC_SHA256=11297ee6562426c49c81387c860153cbc131c4c3d042492d4f6d2d97ab3a1ca5
# Wed, 10 May 2023 18:25:25 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.1.3
# Wed, 10 May 2023 18:25:25 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.1.3.jar
# Wed, 10 May 2023 18:25:25 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.1.3.jar
# Wed, 10 May 2023 18:25:26 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Wed, 10 May 2023 18:25:26 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 10 May 2023 18:25:26 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 10 May 2023 18:25:26 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 10 May 2023 18:25:26 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 10 May 2023 18:25:26 GMT
VOLUME [/usr/local/xwiki]
# Wed, 10 May 2023 18:25:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 May 2023 18:25:26 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f3f60f415e9a03eed88bd5dd5268c841cde08dacf16911a3ef1e4e0fcdd76568`  
		Last Modified: Wed, 26 Apr 2023 02:08:37 GMT  
		Size: 28.4 MB (28389440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fb3595122d1cb6fffe722e2624c3c89b00776b393256a5444af56ceda691cf`  
		Last Modified: Thu, 04 May 2023 03:28:13 GMT  
		Size: 12.5 MB (12463858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5542665e33e692b672a405517e6e267c4c6e210bc410b97a6a1ce732618caa87`  
		Last Modified: Thu, 04 May 2023 03:29:19 GMT  
		Size: 45.0 MB (45009401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e52b8550f0ced98adb0880bd041e361ffb69810e6071e6d71eb2ec0c8ecfad5`  
		Last Modified: Thu, 04 May 2023 03:29:14 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea5566732e0a920d0a63e4fbebf073d2c49e3f80716df462e73f895cc0c5dfa`  
		Last Modified: Thu, 04 May 2023 11:24:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c6d16bf5ef403ef11a1cc9e40650f402cd1f8269d16982f7daebc2a76ab0d9`  
		Last Modified: Wed, 10 May 2023 18:03:56 GMT  
		Size: 12.2 MB (12242222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eaf464f1c82b5f85e3173b2c732f0928a28e669fcc4af9eb6da48199e92ae50`  
		Last Modified: Wed, 10 May 2023 18:03:55 GMT  
		Size: 453.7 KB (453682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ef5f2b94b25f2b0f609c429cc1626d9dd857d8294d2d872d6595bdeff3a5ca`  
		Last Modified: Wed, 10 May 2023 18:03:55 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7cc67d2dc8f70f6e05051c0e95eb0de93a45de55ba65c355eedaff2bf118e42`  
		Last Modified: Wed, 10 May 2023 18:27:43 GMT  
		Size: 173.4 MB (173350375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321a150ce2c4526d3d3f5be05b00d833ba0d530e3b594708aeda7ef22c1855a3`  
		Last Modified: Wed, 10 May 2023 18:27:39 GMT  
		Size: 306.2 MB (306214312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b88233cbf990b6d3911be4ac1c98102dab898e81d932d7a8a5af05dc01d2815f`  
		Last Modified: Wed, 10 May 2023 18:28:48 GMT  
		Size: 591.4 KB (591368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d80dd60b9d5f967b2e17e47f926486cc55c29ad8afc7d311694a70ac16cee628`  
		Last Modified: Wed, 10 May 2023 18:28:48 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54f901e61dc9940e28d9d144bc1defd8b0b7cc2618db70202a9192e68bbf9fc`  
		Last Modified: Wed, 10 May 2023 18:28:48 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a61b65e0ea72006075aa51df69871be6a2a03de0f4ae1602592693e7ad4634`  
		Last Modified: Wed, 10 May 2023 18:28:48 GMT  
		Size: 6.0 KB (6000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abdd5570c03cb152fa5a309ffb407bb26a45dd2e6a102316c9cbcb102abbb8e9`  
		Last Modified: Wed, 10 May 2023 18:28:48 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:stable-mariadb-tomcat`

```console
$ docker pull xwiki@sha256:ba65c6db6cbf680842f048e25f348c8981c5b4295810467e68a3df22f2c0ef77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:stable-mariadb-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:9dc755ce1b9a1d005e8b42c492573371e37310a9960b9b7becc88e7744b5a1b7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **587.4 MB (587443810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9bff1a50bba5fc8078ed4a8574445fb147d50e1d8bd49b788f4954dd1da4132`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 07:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 07:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 07:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 07:26:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:27:16 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 04 May 2023 07:27:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 07:27:40 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 16:13:14 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 04 May 2023 16:13:14 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 16:13:14 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 04 May 2023 16:13:14 GMT
WORKDIR /usr/local/tomcat
# Thu, 04 May 2023 16:13:14 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 16:13:15 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 16:14:45 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 04 May 2023 16:14:45 GMT
ENV TOMCAT_MAJOR=9
# Wed, 10 May 2023 18:01:17 GMT
ENV TOMCAT_VERSION=9.0.75
# Wed, 10 May 2023 18:01:17 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Wed, 10 May 2023 18:01:17 GMT
COPY dir:606cc669e6833afa7967597ca36d4a4497efbb54719c008108649021142d7549 in /usr/local/tomcat 
# Wed, 10 May 2023 18:01:21 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 18:01:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 10 May 2023 18:01:23 GMT
EXPOSE 8080
# Wed, 10 May 2023 18:01:23 GMT
CMD ["catalina.sh" "run"]
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 10 May 2023 18:28:05 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 18:28:06 GMT
ENV XWIKI_VERSION=15.3
# Wed, 10 May 2023 18:28:06 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.3
# Wed, 10 May 2023 18:28:06 GMT
ENV XWIKI_DOWNLOAD_SHA256=fbe35bcc5c6cc5764f2a1da4aca7878531f93bae069d94f399fea7d9656da3b8
# Wed, 10 May 2023 18:28:44 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 10 May 2023 18:30:14 GMT
ENV MARIADB_JDBC_VERSION=3.1.3
# Wed, 10 May 2023 18:30:14 GMT
ENV MARIADB_JDBC_SHA256=11297ee6562426c49c81387c860153cbc131c4c3d042492d4f6d2d97ab3a1ca5
# Wed, 10 May 2023 18:30:14 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.1.3
# Wed, 10 May 2023 18:30:14 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.1.3.jar
# Wed, 10 May 2023 18:30:15 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.1.3.jar
# Wed, 10 May 2023 18:30:15 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Wed, 10 May 2023 18:30:15 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 10 May 2023 18:30:16 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 10 May 2023 18:30:16 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 10 May 2023 18:30:16 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 10 May 2023 18:30:16 GMT
VOLUME [/usr/local/xwiki]
# Wed, 10 May 2023 18:30:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 May 2023 18:30:16 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458b02b5411a07f3b354cde2b461caffc1bb184a3413b5736a9e67ee87cb28b2`  
		Last Modified: Thu, 04 May 2023 07:30:02 GMT  
		Size: 12.5 MB (12504170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04a165ead1d5eabe89dc88e53286af89caab22a5d20c53007b9e6e508affb4b`  
		Last Modified: Thu, 04 May 2023 07:31:19 GMT  
		Size: 46.7 MB (46666270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1187c73b18505bd4495bc03ccbdb723388dfe4d633fd12be845dfe8e253e48e2`  
		Last Modified: Thu, 04 May 2023 07:31:12 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c833cbb14374cde014505e77f6a6122773984a691844e4138fc15cae99ba625`  
		Last Modified: Thu, 04 May 2023 16:24:19 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439ac04571c77c4330db518bc8f35b70f8723246ed34c98787f7ac8d7dc30b42`  
		Last Modified: Wed, 10 May 2023 18:09:06 GMT  
		Size: 12.2 MB (12236613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8e775ba0b76c6692c0b9211e4b94653ba2aa16fdc7a5e3347aba962b684508`  
		Last Modified: Wed, 10 May 2023 18:09:06 GMT  
		Size: 454.2 KB (454222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee5c1ba4848e97d4e3c43d9d4bca0eeeccf2d5d7f6d805d748da4a7d24ad14e`  
		Last Modified: Wed, 10 May 2023 18:09:05 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffadd10be916fc5729676141f5d0ba6aa30968b75555790e449d4988dc81332a`  
		Last Modified: Wed, 10 May 2023 18:32:42 GMT  
		Size: 178.3 MB (178334017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a29002da219be23e789ef538aeaae1d2296399cdfa64c6c2ed7438210947d7`  
		Last Modified: Wed, 10 May 2023 18:32:34 GMT  
		Size: 306.2 MB (306214302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:552f4dcf26ef5ef3b3a7315cc47f3dc07974cb0684775dc9f2d390f7b19be181`  
		Last Modified: Wed, 10 May 2023 18:33:53 GMT  
		Size: 591.4 KB (591369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:647b04728750fccef49babf80ba8257ced3661baa001e9e8a73067bea60c3784`  
		Last Modified: Wed, 10 May 2023 18:33:53 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bcdcc6da901312c0e56c818dfec97184f4cf9e78308964322dba08f16215da0`  
		Last Modified: Wed, 10 May 2023 18:33:53 GMT  
		Size: 2.3 KB (2312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e34abf77fe47a0d97eb01a41d2e6a9b8c0db4e9dfa284dfc767e1d9287b1effe`  
		Last Modified: Wed, 10 May 2023 18:33:53 GMT  
		Size: 6.0 KB (6005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e5b8636c37250081b1a1fd47f2ab5926692c75a635a5b3f805ed897fddb43b`  
		Last Modified: Wed, 10 May 2023 18:33:53 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:stable-mariadb-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:8ba7073b3049679fb036a6d00a78b2b70da792b9cde40df0cc088094dc3a3d59
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.7 MB (578727276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c23d916ce05444c655cb6c876c29ee4fe78165b88d66fad2613ac17dcb7b9924`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 25 Apr 2023 17:31:58 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:31:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:31:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:31:59 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:32:02 GMT
ADD file:aee0d7770ef2f24dc9697e86d391529d001a4013b6e30a3ac90a57932814a57e in / 
# Tue, 25 Apr 2023 17:32:02 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 03:25:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 03:25:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 03:25:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 03:25:23 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 03:25:47 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 04 May 2023 03:26:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 03:26:10 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 11:14:20 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 04 May 2023 11:14:20 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 11:14:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 04 May 2023 11:14:21 GMT
WORKDIR /usr/local/tomcat
# Thu, 04 May 2023 11:14:21 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 11:14:21 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 11:15:34 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 04 May 2023 11:15:34 GMT
ENV TOMCAT_MAJOR=9
# Wed, 10 May 2023 17:56:49 GMT
ENV TOMCAT_VERSION=9.0.75
# Wed, 10 May 2023 17:56:49 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Wed, 10 May 2023 17:56:49 GMT
COPY dir:2a613f9e425d5febc8be5b6c17f49b39f1b8ad84b1601f07f76abed41b25b24b in /usr/local/tomcat 
# Wed, 10 May 2023 17:56:52 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 17:56:54 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 10 May 2023 17:56:54 GMT
EXPOSE 8080
# Wed, 10 May 2023 17:56:54 GMT
CMD ["catalina.sh" "run"]
# Wed, 10 May 2023 18:22:09 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 10 May 2023 18:23:10 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 18:23:13 GMT
ENV XWIKI_VERSION=15.3
# Wed, 10 May 2023 18:23:13 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.3
# Wed, 10 May 2023 18:23:13 GMT
ENV XWIKI_DOWNLOAD_SHA256=fbe35bcc5c6cc5764f2a1da4aca7878531f93bae069d94f399fea7d9656da3b8
# Wed, 10 May 2023 18:23:53 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 10 May 2023 18:25:25 GMT
ENV MARIADB_JDBC_VERSION=3.1.3
# Wed, 10 May 2023 18:25:25 GMT
ENV MARIADB_JDBC_SHA256=11297ee6562426c49c81387c860153cbc131c4c3d042492d4f6d2d97ab3a1ca5
# Wed, 10 May 2023 18:25:25 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.1.3
# Wed, 10 May 2023 18:25:25 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.1.3.jar
# Wed, 10 May 2023 18:25:25 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.1.3.jar
# Wed, 10 May 2023 18:25:26 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Wed, 10 May 2023 18:25:26 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 10 May 2023 18:25:26 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 10 May 2023 18:25:26 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 10 May 2023 18:25:26 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 10 May 2023 18:25:26 GMT
VOLUME [/usr/local/xwiki]
# Wed, 10 May 2023 18:25:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 May 2023 18:25:26 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f3f60f415e9a03eed88bd5dd5268c841cde08dacf16911a3ef1e4e0fcdd76568`  
		Last Modified: Wed, 26 Apr 2023 02:08:37 GMT  
		Size: 28.4 MB (28389440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fb3595122d1cb6fffe722e2624c3c89b00776b393256a5444af56ceda691cf`  
		Last Modified: Thu, 04 May 2023 03:28:13 GMT  
		Size: 12.5 MB (12463858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5542665e33e692b672a405517e6e267c4c6e210bc410b97a6a1ce732618caa87`  
		Last Modified: Thu, 04 May 2023 03:29:19 GMT  
		Size: 45.0 MB (45009401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e52b8550f0ced98adb0880bd041e361ffb69810e6071e6d71eb2ec0c8ecfad5`  
		Last Modified: Thu, 04 May 2023 03:29:14 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea5566732e0a920d0a63e4fbebf073d2c49e3f80716df462e73f895cc0c5dfa`  
		Last Modified: Thu, 04 May 2023 11:24:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c6d16bf5ef403ef11a1cc9e40650f402cd1f8269d16982f7daebc2a76ab0d9`  
		Last Modified: Wed, 10 May 2023 18:03:56 GMT  
		Size: 12.2 MB (12242222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eaf464f1c82b5f85e3173b2c732f0928a28e669fcc4af9eb6da48199e92ae50`  
		Last Modified: Wed, 10 May 2023 18:03:55 GMT  
		Size: 453.7 KB (453682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ef5f2b94b25f2b0f609c429cc1626d9dd857d8294d2d872d6595bdeff3a5ca`  
		Last Modified: Wed, 10 May 2023 18:03:55 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7cc67d2dc8f70f6e05051c0e95eb0de93a45de55ba65c355eedaff2bf118e42`  
		Last Modified: Wed, 10 May 2023 18:27:43 GMT  
		Size: 173.4 MB (173350375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321a150ce2c4526d3d3f5be05b00d833ba0d530e3b594708aeda7ef22c1855a3`  
		Last Modified: Wed, 10 May 2023 18:27:39 GMT  
		Size: 306.2 MB (306214312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b88233cbf990b6d3911be4ac1c98102dab898e81d932d7a8a5af05dc01d2815f`  
		Last Modified: Wed, 10 May 2023 18:28:48 GMT  
		Size: 591.4 KB (591368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d80dd60b9d5f967b2e17e47f926486cc55c29ad8afc7d311694a70ac16cee628`  
		Last Modified: Wed, 10 May 2023 18:28:48 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54f901e61dc9940e28d9d144bc1defd8b0b7cc2618db70202a9192e68bbf9fc`  
		Last Modified: Wed, 10 May 2023 18:28:48 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a61b65e0ea72006075aa51df69871be6a2a03de0f4ae1602592693e7ad4634`  
		Last Modified: Wed, 10 May 2023 18:28:48 GMT  
		Size: 6.0 KB (6000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abdd5570c03cb152fa5a309ffb407bb26a45dd2e6a102316c9cbcb102abbb8e9`  
		Last Modified: Wed, 10 May 2023 18:28:48 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:stable-mysql`

```console
$ docker pull xwiki@sha256:64eecc071ed4a6789fa3a37bc7fefe78ae08fad1bd9a7fcb6680991bfe7e0923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:stable-mysql` - linux; amd64

```console
$ docker pull xwiki@sha256:3252b1cffdf08d016b5e82eae75fed4b890197fa6c7afedd85183b898c8a9777
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.2 MB (589196097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a12be474865cce04cbc87bf8db36fdcded4887dc178f49604d68b710d16be056`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 07:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 07:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 07:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 07:26:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:27:16 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 04 May 2023 07:27:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 07:27:40 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 16:13:14 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 04 May 2023 16:13:14 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 16:13:14 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 04 May 2023 16:13:14 GMT
WORKDIR /usr/local/tomcat
# Thu, 04 May 2023 16:13:14 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 16:13:15 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 16:14:45 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 04 May 2023 16:14:45 GMT
ENV TOMCAT_MAJOR=9
# Wed, 10 May 2023 18:01:17 GMT
ENV TOMCAT_VERSION=9.0.75
# Wed, 10 May 2023 18:01:17 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Wed, 10 May 2023 18:01:17 GMT
COPY dir:606cc669e6833afa7967597ca36d4a4497efbb54719c008108649021142d7549 in /usr/local/tomcat 
# Wed, 10 May 2023 18:01:21 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 18:01:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 10 May 2023 18:01:23 GMT
EXPOSE 8080
# Wed, 10 May 2023 18:01:23 GMT
CMD ["catalina.sh" "run"]
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 10 May 2023 18:28:05 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 18:28:06 GMT
ENV XWIKI_VERSION=15.3
# Wed, 10 May 2023 18:28:06 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.3
# Wed, 10 May 2023 18:28:06 GMT
ENV XWIKI_DOWNLOAD_SHA256=fbe35bcc5c6cc5764f2a1da4aca7878531f93bae069d94f399fea7d9656da3b8
# Wed, 10 May 2023 18:28:44 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 10 May 2023 18:28:45 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Wed, 10 May 2023 18:28:45 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Wed, 10 May 2023 18:28:45 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Wed, 10 May 2023 18:28:45 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Wed, 10 May 2023 18:28:45 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Wed, 10 May 2023 18:28:46 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Wed, 10 May 2023 18:28:46 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 10 May 2023 18:28:46 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 10 May 2023 18:28:47 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 10 May 2023 18:28:47 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 10 May 2023 18:28:47 GMT
VOLUME [/usr/local/xwiki]
# Wed, 10 May 2023 18:28:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 May 2023 18:28:47 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458b02b5411a07f3b354cde2b461caffc1bb184a3413b5736a9e67ee87cb28b2`  
		Last Modified: Thu, 04 May 2023 07:30:02 GMT  
		Size: 12.5 MB (12504170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04a165ead1d5eabe89dc88e53286af89caab22a5d20c53007b9e6e508affb4b`  
		Last Modified: Thu, 04 May 2023 07:31:19 GMT  
		Size: 46.7 MB (46666270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1187c73b18505bd4495bc03ccbdb723388dfe4d633fd12be845dfe8e253e48e2`  
		Last Modified: Thu, 04 May 2023 07:31:12 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c833cbb14374cde014505e77f6a6122773984a691844e4138fc15cae99ba625`  
		Last Modified: Thu, 04 May 2023 16:24:19 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439ac04571c77c4330db518bc8f35b70f8723246ed34c98787f7ac8d7dc30b42`  
		Last Modified: Wed, 10 May 2023 18:09:06 GMT  
		Size: 12.2 MB (12236613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8e775ba0b76c6692c0b9211e4b94653ba2aa16fdc7a5e3347aba962b684508`  
		Last Modified: Wed, 10 May 2023 18:09:06 GMT  
		Size: 454.2 KB (454222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee5c1ba4848e97d4e3c43d9d4bca0eeeccf2d5d7f6d805d748da4a7d24ad14e`  
		Last Modified: Wed, 10 May 2023 18:09:05 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffadd10be916fc5729676141f5d0ba6aa30968b75555790e449d4988dc81332a`  
		Last Modified: Wed, 10 May 2023 18:32:42 GMT  
		Size: 178.3 MB (178334017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a29002da219be23e789ef538aeaae1d2296399cdfa64c6c2ed7438210947d7`  
		Last Modified: Wed, 10 May 2023 18:32:34 GMT  
		Size: 306.2 MB (306214302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628263d6dd0a28e03148683703ead7b3c5ef0abd589af1c7352f58aadb9c01a8`  
		Last Modified: Wed, 10 May 2023 18:32:17 GMT  
		Size: 2.3 MB (2343663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81942c3829003d54f85f9d0e3d4fb84d03f7db66060cdd1d2a6a812ce516ccd6`  
		Last Modified: Wed, 10 May 2023 18:32:17 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e635acc63235269abedf51ee8315a58bbb09ff0cbd90f9c6f68c6ea5269d909`  
		Last Modified: Wed, 10 May 2023 18:32:17 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e905c9c0de831ffb2222e8e0420b569e8658457adc3ae299482d6ad73bdb3abb`  
		Last Modified: Wed, 10 May 2023 18:32:17 GMT  
		Size: 6.0 KB (6003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3459a44ee12986d9a54da5b087233e6dfe71171061ce1a63376de231c25ea842`  
		Last Modified: Wed, 10 May 2023 18:32:17 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:stable-mysql` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:156f67756ea75d27982bd550fe642c9e9bea5cf04a008f6d3e5af5d2343ca83b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.5 MB (580479573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab46181cab4d5b59fc90bad1883f22f0f812a647a62e801240dfa51c485ed1b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 25 Apr 2023 17:31:58 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:31:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:31:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:31:59 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:32:02 GMT
ADD file:aee0d7770ef2f24dc9697e86d391529d001a4013b6e30a3ac90a57932814a57e in / 
# Tue, 25 Apr 2023 17:32:02 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 03:25:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 03:25:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 03:25:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 03:25:23 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 03:25:47 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 04 May 2023 03:26:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 03:26:10 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 11:14:20 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 04 May 2023 11:14:20 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 11:14:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 04 May 2023 11:14:21 GMT
WORKDIR /usr/local/tomcat
# Thu, 04 May 2023 11:14:21 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 11:14:21 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 11:15:34 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 04 May 2023 11:15:34 GMT
ENV TOMCAT_MAJOR=9
# Wed, 10 May 2023 17:56:49 GMT
ENV TOMCAT_VERSION=9.0.75
# Wed, 10 May 2023 17:56:49 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Wed, 10 May 2023 17:56:49 GMT
COPY dir:2a613f9e425d5febc8be5b6c17f49b39f1b8ad84b1601f07f76abed41b25b24b in /usr/local/tomcat 
# Wed, 10 May 2023 17:56:52 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 17:56:54 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 10 May 2023 17:56:54 GMT
EXPOSE 8080
# Wed, 10 May 2023 17:56:54 GMT
CMD ["catalina.sh" "run"]
# Wed, 10 May 2023 18:22:09 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 10 May 2023 18:23:10 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 18:23:13 GMT
ENV XWIKI_VERSION=15.3
# Wed, 10 May 2023 18:23:13 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.3
# Wed, 10 May 2023 18:23:13 GMT
ENV XWIKI_DOWNLOAD_SHA256=fbe35bcc5c6cc5764f2a1da4aca7878531f93bae069d94f399fea7d9656da3b8
# Wed, 10 May 2023 18:23:53 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 10 May 2023 18:23:55 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Wed, 10 May 2023 18:23:55 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Wed, 10 May 2023 18:23:55 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Wed, 10 May 2023 18:23:56 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Wed, 10 May 2023 18:23:56 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Wed, 10 May 2023 18:23:56 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Wed, 10 May 2023 18:23:56 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 10 May 2023 18:23:57 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 10 May 2023 18:23:57 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 10 May 2023 18:23:57 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 10 May 2023 18:23:57 GMT
VOLUME [/usr/local/xwiki]
# Wed, 10 May 2023 18:23:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 May 2023 18:23:57 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f3f60f415e9a03eed88bd5dd5268c841cde08dacf16911a3ef1e4e0fcdd76568`  
		Last Modified: Wed, 26 Apr 2023 02:08:37 GMT  
		Size: 28.4 MB (28389440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fb3595122d1cb6fffe722e2624c3c89b00776b393256a5444af56ceda691cf`  
		Last Modified: Thu, 04 May 2023 03:28:13 GMT  
		Size: 12.5 MB (12463858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5542665e33e692b672a405517e6e267c4c6e210bc410b97a6a1ce732618caa87`  
		Last Modified: Thu, 04 May 2023 03:29:19 GMT  
		Size: 45.0 MB (45009401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e52b8550f0ced98adb0880bd041e361ffb69810e6071e6d71eb2ec0c8ecfad5`  
		Last Modified: Thu, 04 May 2023 03:29:14 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea5566732e0a920d0a63e4fbebf073d2c49e3f80716df462e73f895cc0c5dfa`  
		Last Modified: Thu, 04 May 2023 11:24:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c6d16bf5ef403ef11a1cc9e40650f402cd1f8269d16982f7daebc2a76ab0d9`  
		Last Modified: Wed, 10 May 2023 18:03:56 GMT  
		Size: 12.2 MB (12242222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eaf464f1c82b5f85e3173b2c732f0928a28e669fcc4af9eb6da48199e92ae50`  
		Last Modified: Wed, 10 May 2023 18:03:55 GMT  
		Size: 453.7 KB (453682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ef5f2b94b25f2b0f609c429cc1626d9dd857d8294d2d872d6595bdeff3a5ca`  
		Last Modified: Wed, 10 May 2023 18:03:55 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7cc67d2dc8f70f6e05051c0e95eb0de93a45de55ba65c355eedaff2bf118e42`  
		Last Modified: Wed, 10 May 2023 18:27:43 GMT  
		Size: 173.4 MB (173350375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321a150ce2c4526d3d3f5be05b00d833ba0d530e3b594708aeda7ef22c1855a3`  
		Last Modified: Wed, 10 May 2023 18:27:39 GMT  
		Size: 306.2 MB (306214312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de8537cceb0f08c97a9244c93c7142180f99d25a07a008c897b3e7f2e01749f5`  
		Last Modified: Wed, 10 May 2023 18:27:25 GMT  
		Size: 2.3 MB (2343667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:174ceadf9884a59c863a2f45bc8a9d2c877073089ab2293ec28b4a890edbd549`  
		Last Modified: Wed, 10 May 2023 18:27:25 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4340d0afded864299aaa098ecb92231c246d875fd05e7babc4eb574c24aba63`  
		Last Modified: Wed, 10 May 2023 18:27:25 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ff6fb98971adf0b973b7c902a39cadccb245e656dc8470ec75d8e115e335c0`  
		Last Modified: Wed, 10 May 2023 18:27:25 GMT  
		Size: 6.0 KB (6000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e40c1aaebc8527a9ad709da10958451577ca896b6c968e0e49daf1cc4f790ddd`  
		Last Modified: Wed, 10 May 2023 18:27:25 GMT  
		Size: 2.5 KB (2503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:stable-mysql-tomcat`

```console
$ docker pull xwiki@sha256:64eecc071ed4a6789fa3a37bc7fefe78ae08fad1bd9a7fcb6680991bfe7e0923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:stable-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:3252b1cffdf08d016b5e82eae75fed4b890197fa6c7afedd85183b898c8a9777
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.2 MB (589196097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a12be474865cce04cbc87bf8db36fdcded4887dc178f49604d68b710d16be056`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 07:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 07:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 07:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 07:26:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:27:16 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 04 May 2023 07:27:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 07:27:40 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 16:13:14 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 04 May 2023 16:13:14 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 16:13:14 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 04 May 2023 16:13:14 GMT
WORKDIR /usr/local/tomcat
# Thu, 04 May 2023 16:13:14 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 16:13:15 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 16:14:45 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 04 May 2023 16:14:45 GMT
ENV TOMCAT_MAJOR=9
# Wed, 10 May 2023 18:01:17 GMT
ENV TOMCAT_VERSION=9.0.75
# Wed, 10 May 2023 18:01:17 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Wed, 10 May 2023 18:01:17 GMT
COPY dir:606cc669e6833afa7967597ca36d4a4497efbb54719c008108649021142d7549 in /usr/local/tomcat 
# Wed, 10 May 2023 18:01:21 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 18:01:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 10 May 2023 18:01:23 GMT
EXPOSE 8080
# Wed, 10 May 2023 18:01:23 GMT
CMD ["catalina.sh" "run"]
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 10 May 2023 18:28:05 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 18:28:06 GMT
ENV XWIKI_VERSION=15.3
# Wed, 10 May 2023 18:28:06 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.3
# Wed, 10 May 2023 18:28:06 GMT
ENV XWIKI_DOWNLOAD_SHA256=fbe35bcc5c6cc5764f2a1da4aca7878531f93bae069d94f399fea7d9656da3b8
# Wed, 10 May 2023 18:28:44 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 10 May 2023 18:28:45 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Wed, 10 May 2023 18:28:45 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Wed, 10 May 2023 18:28:45 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Wed, 10 May 2023 18:28:45 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Wed, 10 May 2023 18:28:45 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Wed, 10 May 2023 18:28:46 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Wed, 10 May 2023 18:28:46 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 10 May 2023 18:28:46 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 10 May 2023 18:28:47 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 10 May 2023 18:28:47 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 10 May 2023 18:28:47 GMT
VOLUME [/usr/local/xwiki]
# Wed, 10 May 2023 18:28:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 May 2023 18:28:47 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458b02b5411a07f3b354cde2b461caffc1bb184a3413b5736a9e67ee87cb28b2`  
		Last Modified: Thu, 04 May 2023 07:30:02 GMT  
		Size: 12.5 MB (12504170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04a165ead1d5eabe89dc88e53286af89caab22a5d20c53007b9e6e508affb4b`  
		Last Modified: Thu, 04 May 2023 07:31:19 GMT  
		Size: 46.7 MB (46666270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1187c73b18505bd4495bc03ccbdb723388dfe4d633fd12be845dfe8e253e48e2`  
		Last Modified: Thu, 04 May 2023 07:31:12 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c833cbb14374cde014505e77f6a6122773984a691844e4138fc15cae99ba625`  
		Last Modified: Thu, 04 May 2023 16:24:19 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439ac04571c77c4330db518bc8f35b70f8723246ed34c98787f7ac8d7dc30b42`  
		Last Modified: Wed, 10 May 2023 18:09:06 GMT  
		Size: 12.2 MB (12236613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8e775ba0b76c6692c0b9211e4b94653ba2aa16fdc7a5e3347aba962b684508`  
		Last Modified: Wed, 10 May 2023 18:09:06 GMT  
		Size: 454.2 KB (454222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee5c1ba4848e97d4e3c43d9d4bca0eeeccf2d5d7f6d805d748da4a7d24ad14e`  
		Last Modified: Wed, 10 May 2023 18:09:05 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffadd10be916fc5729676141f5d0ba6aa30968b75555790e449d4988dc81332a`  
		Last Modified: Wed, 10 May 2023 18:32:42 GMT  
		Size: 178.3 MB (178334017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a29002da219be23e789ef538aeaae1d2296399cdfa64c6c2ed7438210947d7`  
		Last Modified: Wed, 10 May 2023 18:32:34 GMT  
		Size: 306.2 MB (306214302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628263d6dd0a28e03148683703ead7b3c5ef0abd589af1c7352f58aadb9c01a8`  
		Last Modified: Wed, 10 May 2023 18:32:17 GMT  
		Size: 2.3 MB (2343663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81942c3829003d54f85f9d0e3d4fb84d03f7db66060cdd1d2a6a812ce516ccd6`  
		Last Modified: Wed, 10 May 2023 18:32:17 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e635acc63235269abedf51ee8315a58bbb09ff0cbd90f9c6f68c6ea5269d909`  
		Last Modified: Wed, 10 May 2023 18:32:17 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e905c9c0de831ffb2222e8e0420b569e8658457adc3ae299482d6ad73bdb3abb`  
		Last Modified: Wed, 10 May 2023 18:32:17 GMT  
		Size: 6.0 KB (6003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3459a44ee12986d9a54da5b087233e6dfe71171061ce1a63376de231c25ea842`  
		Last Modified: Wed, 10 May 2023 18:32:17 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:stable-mysql-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:156f67756ea75d27982bd550fe642c9e9bea5cf04a008f6d3e5af5d2343ca83b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.5 MB (580479573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab46181cab4d5b59fc90bad1883f22f0f812a647a62e801240dfa51c485ed1b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 25 Apr 2023 17:31:58 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:31:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:31:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:31:59 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:32:02 GMT
ADD file:aee0d7770ef2f24dc9697e86d391529d001a4013b6e30a3ac90a57932814a57e in / 
# Tue, 25 Apr 2023 17:32:02 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 03:25:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 03:25:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 03:25:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 03:25:23 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 03:25:47 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 04 May 2023 03:26:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 03:26:10 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 11:14:20 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 04 May 2023 11:14:20 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 11:14:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 04 May 2023 11:14:21 GMT
WORKDIR /usr/local/tomcat
# Thu, 04 May 2023 11:14:21 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 11:14:21 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 11:15:34 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 04 May 2023 11:15:34 GMT
ENV TOMCAT_MAJOR=9
# Wed, 10 May 2023 17:56:49 GMT
ENV TOMCAT_VERSION=9.0.75
# Wed, 10 May 2023 17:56:49 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Wed, 10 May 2023 17:56:49 GMT
COPY dir:2a613f9e425d5febc8be5b6c17f49b39f1b8ad84b1601f07f76abed41b25b24b in /usr/local/tomcat 
# Wed, 10 May 2023 17:56:52 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 17:56:54 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 10 May 2023 17:56:54 GMT
EXPOSE 8080
# Wed, 10 May 2023 17:56:54 GMT
CMD ["catalina.sh" "run"]
# Wed, 10 May 2023 18:22:09 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 10 May 2023 18:23:10 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 18:23:13 GMT
ENV XWIKI_VERSION=15.3
# Wed, 10 May 2023 18:23:13 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.3
# Wed, 10 May 2023 18:23:13 GMT
ENV XWIKI_DOWNLOAD_SHA256=fbe35bcc5c6cc5764f2a1da4aca7878531f93bae069d94f399fea7d9656da3b8
# Wed, 10 May 2023 18:23:53 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 10 May 2023 18:23:55 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Wed, 10 May 2023 18:23:55 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Wed, 10 May 2023 18:23:55 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Wed, 10 May 2023 18:23:56 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Wed, 10 May 2023 18:23:56 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Wed, 10 May 2023 18:23:56 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Wed, 10 May 2023 18:23:56 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 10 May 2023 18:23:57 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 10 May 2023 18:23:57 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 10 May 2023 18:23:57 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 10 May 2023 18:23:57 GMT
VOLUME [/usr/local/xwiki]
# Wed, 10 May 2023 18:23:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 May 2023 18:23:57 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f3f60f415e9a03eed88bd5dd5268c841cde08dacf16911a3ef1e4e0fcdd76568`  
		Last Modified: Wed, 26 Apr 2023 02:08:37 GMT  
		Size: 28.4 MB (28389440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fb3595122d1cb6fffe722e2624c3c89b00776b393256a5444af56ceda691cf`  
		Last Modified: Thu, 04 May 2023 03:28:13 GMT  
		Size: 12.5 MB (12463858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5542665e33e692b672a405517e6e267c4c6e210bc410b97a6a1ce732618caa87`  
		Last Modified: Thu, 04 May 2023 03:29:19 GMT  
		Size: 45.0 MB (45009401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e52b8550f0ced98adb0880bd041e361ffb69810e6071e6d71eb2ec0c8ecfad5`  
		Last Modified: Thu, 04 May 2023 03:29:14 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea5566732e0a920d0a63e4fbebf073d2c49e3f80716df462e73f895cc0c5dfa`  
		Last Modified: Thu, 04 May 2023 11:24:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c6d16bf5ef403ef11a1cc9e40650f402cd1f8269d16982f7daebc2a76ab0d9`  
		Last Modified: Wed, 10 May 2023 18:03:56 GMT  
		Size: 12.2 MB (12242222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eaf464f1c82b5f85e3173b2c732f0928a28e669fcc4af9eb6da48199e92ae50`  
		Last Modified: Wed, 10 May 2023 18:03:55 GMT  
		Size: 453.7 KB (453682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ef5f2b94b25f2b0f609c429cc1626d9dd857d8294d2d872d6595bdeff3a5ca`  
		Last Modified: Wed, 10 May 2023 18:03:55 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7cc67d2dc8f70f6e05051c0e95eb0de93a45de55ba65c355eedaff2bf118e42`  
		Last Modified: Wed, 10 May 2023 18:27:43 GMT  
		Size: 173.4 MB (173350375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321a150ce2c4526d3d3f5be05b00d833ba0d530e3b594708aeda7ef22c1855a3`  
		Last Modified: Wed, 10 May 2023 18:27:39 GMT  
		Size: 306.2 MB (306214312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de8537cceb0f08c97a9244c93c7142180f99d25a07a008c897b3e7f2e01749f5`  
		Last Modified: Wed, 10 May 2023 18:27:25 GMT  
		Size: 2.3 MB (2343667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:174ceadf9884a59c863a2f45bc8a9d2c877073089ab2293ec28b4a890edbd549`  
		Last Modified: Wed, 10 May 2023 18:27:25 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4340d0afded864299aaa098ecb92231c246d875fd05e7babc4eb574c24aba63`  
		Last Modified: Wed, 10 May 2023 18:27:25 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ff6fb98971adf0b973b7c902a39cadccb245e656dc8470ec75d8e115e335c0`  
		Last Modified: Wed, 10 May 2023 18:27:25 GMT  
		Size: 6.0 KB (6000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e40c1aaebc8527a9ad709da10958451577ca896b6c968e0e49daf1cc4f790ddd`  
		Last Modified: Wed, 10 May 2023 18:27:25 GMT  
		Size: 2.5 KB (2503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:stable-postgres`

```console
$ docker pull xwiki@sha256:735933782d363352e7012650659093d08fb0ad9b2fdf0bf6f481f6a6007e57e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:stable-postgres` - linux; amd64

```console
$ docker pull xwiki@sha256:2900c897a5a066bba2d94f8c0328bda225a94fe5d86155f565d8a024e15967ac
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **588.7 MB (588732305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ea08c636ebabfa7d8491ee29125599e2839801fa05ae791780a490474746bef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 07:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 07:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 07:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 07:26:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:27:16 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 04 May 2023 07:27:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 07:27:40 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 16:13:14 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 04 May 2023 16:13:14 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 16:13:14 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 04 May 2023 16:13:14 GMT
WORKDIR /usr/local/tomcat
# Thu, 04 May 2023 16:13:14 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 16:13:15 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 16:14:45 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 04 May 2023 16:14:45 GMT
ENV TOMCAT_MAJOR=9
# Wed, 10 May 2023 18:01:17 GMT
ENV TOMCAT_VERSION=9.0.75
# Wed, 10 May 2023 18:01:17 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Wed, 10 May 2023 18:01:17 GMT
COPY dir:606cc669e6833afa7967597ca36d4a4497efbb54719c008108649021142d7549 in /usr/local/tomcat 
# Wed, 10 May 2023 18:01:21 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 18:01:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 10 May 2023 18:01:23 GMT
EXPOSE 8080
# Wed, 10 May 2023 18:01:23 GMT
CMD ["catalina.sh" "run"]
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 10 May 2023 18:29:15 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 18:29:16 GMT
ENV XWIKI_VERSION=15.3
# Wed, 10 May 2023 18:29:16 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.3
# Wed, 10 May 2023 18:29:16 GMT
ENV XWIKI_DOWNLOAD_SHA256=fbe35bcc5c6cc5764f2a1da4aca7878531f93bae069d94f399fea7d9656da3b8
# Wed, 10 May 2023 18:29:56 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 10 May 2023 18:29:58 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Wed, 10 May 2023 18:29:58 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 10 May 2023 18:29:58 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 10 May 2023 18:29:58 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 10 May 2023 18:29:58 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 10 May 2023 18:29:59 GMT
VOLUME [/usr/local/xwiki]
# Wed, 10 May 2023 18:29:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 May 2023 18:29:59 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458b02b5411a07f3b354cde2b461caffc1bb184a3413b5736a9e67ee87cb28b2`  
		Last Modified: Thu, 04 May 2023 07:30:02 GMT  
		Size: 12.5 MB (12504170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04a165ead1d5eabe89dc88e53286af89caab22a5d20c53007b9e6e508affb4b`  
		Last Modified: Thu, 04 May 2023 07:31:19 GMT  
		Size: 46.7 MB (46666270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1187c73b18505bd4495bc03ccbdb723388dfe4d633fd12be845dfe8e253e48e2`  
		Last Modified: Thu, 04 May 2023 07:31:12 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c833cbb14374cde014505e77f6a6122773984a691844e4138fc15cae99ba625`  
		Last Modified: Thu, 04 May 2023 16:24:19 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439ac04571c77c4330db518bc8f35b70f8723246ed34c98787f7ac8d7dc30b42`  
		Last Modified: Wed, 10 May 2023 18:09:06 GMT  
		Size: 12.2 MB (12236613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8e775ba0b76c6692c0b9211e4b94653ba2aa16fdc7a5e3347aba962b684508`  
		Last Modified: Wed, 10 May 2023 18:09:06 GMT  
		Size: 454.2 KB (454222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee5c1ba4848e97d4e3c43d9d4bca0eeeccf2d5d7f6d805d748da4a7d24ad14e`  
		Last Modified: Wed, 10 May 2023 18:09:05 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29abf03d18e0bc34be536fce36ea27d0012a4d330eed44003684563b4d891b2d`  
		Last Modified: Wed, 10 May 2023 18:33:36 GMT  
		Size: 179.3 MB (179276853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04893bb957c480bd2610cdfdf9d8ce54f10892dc666a3f546d0a47e08a8b6bf3`  
		Last Modified: Wed, 10 May 2023 18:33:28 GMT  
		Size: 306.2 MB (306214334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c733bdd07cccb12e268038f38cc2208c02cab00afde7af1103ad9ab1d34ddc49`  
		Last Modified: Wed, 10 May 2023 18:33:11 GMT  
		Size: 936.9 KB (936851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:308d5fe9ecebf8518e4a3354dfd14989f5a913a5a8d7a6abec2afaca25ea32ac`  
		Last Modified: Wed, 10 May 2023 18:33:11 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3080392f0ef7aac169f05c443bbff282a8f4c46dbf39c2f91bd942f63c4296e4`  
		Last Modified: Wed, 10 May 2023 18:33:11 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cde226d897c8670f291d599b6ddecdece884739dc8e4f66874764aa1a46fd4a`  
		Last Modified: Wed, 10 May 2023 18:33:11 GMT  
		Size: 6.0 KB (6002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:552d5c735b1472b69f77b166b9824e3f6cee95760872d8f8c00958e81a510428`  
		Last Modified: Wed, 10 May 2023 18:33:11 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:stable-postgres` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:10bfb120c331e4fd20b20348ab4270888db1418737568c832e5dbb489577d754
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.0 MB (580013492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e62cc10c58ce901b71a525883c5fac34e70c79f319bbce13405788bcaa52e78a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 25 Apr 2023 17:31:58 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:31:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:31:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:31:59 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:32:02 GMT
ADD file:aee0d7770ef2f24dc9697e86d391529d001a4013b6e30a3ac90a57932814a57e in / 
# Tue, 25 Apr 2023 17:32:02 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 03:25:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 03:25:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 03:25:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 03:25:23 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 03:25:47 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 04 May 2023 03:26:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 03:26:10 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 11:14:20 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 04 May 2023 11:14:20 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 11:14:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 04 May 2023 11:14:21 GMT
WORKDIR /usr/local/tomcat
# Thu, 04 May 2023 11:14:21 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 11:14:21 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 11:15:34 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 04 May 2023 11:15:34 GMT
ENV TOMCAT_MAJOR=9
# Wed, 10 May 2023 17:56:49 GMT
ENV TOMCAT_VERSION=9.0.75
# Wed, 10 May 2023 17:56:49 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Wed, 10 May 2023 17:56:49 GMT
COPY dir:2a613f9e425d5febc8be5b6c17f49b39f1b8ad84b1601f07f76abed41b25b24b in /usr/local/tomcat 
# Wed, 10 May 2023 17:56:52 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 17:56:54 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 10 May 2023 17:56:54 GMT
EXPOSE 8080
# Wed, 10 May 2023 17:56:54 GMT
CMD ["catalina.sh" "run"]
# Wed, 10 May 2023 18:22:09 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 10 May 2023 18:24:24 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 18:24:27 GMT
ENV XWIKI_VERSION=15.3
# Wed, 10 May 2023 18:24:28 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.3
# Wed, 10 May 2023 18:24:28 GMT
ENV XWIKI_DOWNLOAD_SHA256=fbe35bcc5c6cc5764f2a1da4aca7878531f93bae069d94f399fea7d9656da3b8
# Wed, 10 May 2023 18:25:07 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 10 May 2023 18:25:10 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Wed, 10 May 2023 18:25:10 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 10 May 2023 18:25:10 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 10 May 2023 18:25:11 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 10 May 2023 18:25:11 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 10 May 2023 18:25:11 GMT
VOLUME [/usr/local/xwiki]
# Wed, 10 May 2023 18:25:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 May 2023 18:25:11 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f3f60f415e9a03eed88bd5dd5268c841cde08dacf16911a3ef1e4e0fcdd76568`  
		Last Modified: Wed, 26 Apr 2023 02:08:37 GMT  
		Size: 28.4 MB (28389440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fb3595122d1cb6fffe722e2624c3c89b00776b393256a5444af56ceda691cf`  
		Last Modified: Thu, 04 May 2023 03:28:13 GMT  
		Size: 12.5 MB (12463858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5542665e33e692b672a405517e6e267c4c6e210bc410b97a6a1ce732618caa87`  
		Last Modified: Thu, 04 May 2023 03:29:19 GMT  
		Size: 45.0 MB (45009401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e52b8550f0ced98adb0880bd041e361ffb69810e6071e6d71eb2ec0c8ecfad5`  
		Last Modified: Thu, 04 May 2023 03:29:14 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea5566732e0a920d0a63e4fbebf073d2c49e3f80716df462e73f895cc0c5dfa`  
		Last Modified: Thu, 04 May 2023 11:24:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c6d16bf5ef403ef11a1cc9e40650f402cd1f8269d16982f7daebc2a76ab0d9`  
		Last Modified: Wed, 10 May 2023 18:03:56 GMT  
		Size: 12.2 MB (12242222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eaf464f1c82b5f85e3173b2c732f0928a28e669fcc4af9eb6da48199e92ae50`  
		Last Modified: Wed, 10 May 2023 18:03:55 GMT  
		Size: 453.7 KB (453682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ef5f2b94b25f2b0f609c429cc1626d9dd857d8294d2d872d6595bdeff3a5ca`  
		Last Modified: Wed, 10 May 2023 18:03:55 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e76b785cabb7a84968f4d713d3072c255796ddcef576690d954e3fc5b1a09604`  
		Last Modified: Wed, 10 May 2023 18:28:29 GMT  
		Size: 174.3 MB (174290936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bbb1bea6fd7e5ad54d9a435449598eab16234ad43ac144f2e8bfd3d6ba08f53`  
		Last Modified: Wed, 10 May 2023 18:28:26 GMT  
		Size: 306.2 MB (306214328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ec4bf084be2f31ea6d132041630e63267918cd9d3fda2c1c5729796be49ca3`  
		Last Modified: Wed, 10 May 2023 18:28:12 GMT  
		Size: 936.9 KB (936850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35482f801e8bffd20763dc900fe57a71e0b8b6e9704fc5960d1ae5c49c36568f`  
		Last Modified: Wed, 10 May 2023 18:28:12 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73fefab11cdaf813c0992abeb9546ca3853626b0c153d8792dda45700405f9d7`  
		Last Modified: Wed, 10 May 2023 18:28:12 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510da944c55d824606569a712e2defc95041c832ea8b07bd45aca2bf455095c2`  
		Last Modified: Wed, 10 May 2023 18:28:12 GMT  
		Size: 6.0 KB (6005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60c6d213e30aaeb6555c54770342ec9de274eb11eff3007dc29f2d552d0dd36c`  
		Last Modified: Wed, 10 May 2023 18:28:12 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:stable-postgres-tomcat`

```console
$ docker pull xwiki@sha256:735933782d363352e7012650659093d08fb0ad9b2fdf0bf6f481f6a6007e57e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:stable-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:2900c897a5a066bba2d94f8c0328bda225a94fe5d86155f565d8a024e15967ac
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **588.7 MB (588732305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ea08c636ebabfa7d8491ee29125599e2839801fa05ae791780a490474746bef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 07:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 07:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 07:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 07:26:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:27:16 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 04 May 2023 07:27:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 07:27:40 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 16:13:14 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 04 May 2023 16:13:14 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 16:13:14 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 04 May 2023 16:13:14 GMT
WORKDIR /usr/local/tomcat
# Thu, 04 May 2023 16:13:14 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 16:13:15 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 16:14:45 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 04 May 2023 16:14:45 GMT
ENV TOMCAT_MAJOR=9
# Wed, 10 May 2023 18:01:17 GMT
ENV TOMCAT_VERSION=9.0.75
# Wed, 10 May 2023 18:01:17 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Wed, 10 May 2023 18:01:17 GMT
COPY dir:606cc669e6833afa7967597ca36d4a4497efbb54719c008108649021142d7549 in /usr/local/tomcat 
# Wed, 10 May 2023 18:01:21 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 18:01:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 10 May 2023 18:01:23 GMT
EXPOSE 8080
# Wed, 10 May 2023 18:01:23 GMT
CMD ["catalina.sh" "run"]
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 10 May 2023 18:27:13 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 10 May 2023 18:29:15 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 18:29:16 GMT
ENV XWIKI_VERSION=15.3
# Wed, 10 May 2023 18:29:16 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.3
# Wed, 10 May 2023 18:29:16 GMT
ENV XWIKI_DOWNLOAD_SHA256=fbe35bcc5c6cc5764f2a1da4aca7878531f93bae069d94f399fea7d9656da3b8
# Wed, 10 May 2023 18:29:56 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 10 May 2023 18:29:58 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Wed, 10 May 2023 18:29:58 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 10 May 2023 18:29:58 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 10 May 2023 18:29:58 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 10 May 2023 18:29:58 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 10 May 2023 18:29:59 GMT
VOLUME [/usr/local/xwiki]
# Wed, 10 May 2023 18:29:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 May 2023 18:29:59 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458b02b5411a07f3b354cde2b461caffc1bb184a3413b5736a9e67ee87cb28b2`  
		Last Modified: Thu, 04 May 2023 07:30:02 GMT  
		Size: 12.5 MB (12504170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04a165ead1d5eabe89dc88e53286af89caab22a5d20c53007b9e6e508affb4b`  
		Last Modified: Thu, 04 May 2023 07:31:19 GMT  
		Size: 46.7 MB (46666270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1187c73b18505bd4495bc03ccbdb723388dfe4d633fd12be845dfe8e253e48e2`  
		Last Modified: Thu, 04 May 2023 07:31:12 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c833cbb14374cde014505e77f6a6122773984a691844e4138fc15cae99ba625`  
		Last Modified: Thu, 04 May 2023 16:24:19 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439ac04571c77c4330db518bc8f35b70f8723246ed34c98787f7ac8d7dc30b42`  
		Last Modified: Wed, 10 May 2023 18:09:06 GMT  
		Size: 12.2 MB (12236613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8e775ba0b76c6692c0b9211e4b94653ba2aa16fdc7a5e3347aba962b684508`  
		Last Modified: Wed, 10 May 2023 18:09:06 GMT  
		Size: 454.2 KB (454222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee5c1ba4848e97d4e3c43d9d4bca0eeeccf2d5d7f6d805d748da4a7d24ad14e`  
		Last Modified: Wed, 10 May 2023 18:09:05 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29abf03d18e0bc34be536fce36ea27d0012a4d330eed44003684563b4d891b2d`  
		Last Modified: Wed, 10 May 2023 18:33:36 GMT  
		Size: 179.3 MB (179276853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04893bb957c480bd2610cdfdf9d8ce54f10892dc666a3f546d0a47e08a8b6bf3`  
		Last Modified: Wed, 10 May 2023 18:33:28 GMT  
		Size: 306.2 MB (306214334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c733bdd07cccb12e268038f38cc2208c02cab00afde7af1103ad9ab1d34ddc49`  
		Last Modified: Wed, 10 May 2023 18:33:11 GMT  
		Size: 936.9 KB (936851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:308d5fe9ecebf8518e4a3354dfd14989f5a913a5a8d7a6abec2afaca25ea32ac`  
		Last Modified: Wed, 10 May 2023 18:33:11 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3080392f0ef7aac169f05c443bbff282a8f4c46dbf39c2f91bd942f63c4296e4`  
		Last Modified: Wed, 10 May 2023 18:33:11 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cde226d897c8670f291d599b6ddecdece884739dc8e4f66874764aa1a46fd4a`  
		Last Modified: Wed, 10 May 2023 18:33:11 GMT  
		Size: 6.0 KB (6002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:552d5c735b1472b69f77b166b9824e3f6cee95760872d8f8c00958e81a510428`  
		Last Modified: Wed, 10 May 2023 18:33:11 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:stable-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:10bfb120c331e4fd20b20348ab4270888db1418737568c832e5dbb489577d754
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.0 MB (580013492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e62cc10c58ce901b71a525883c5fac34e70c79f319bbce13405788bcaa52e78a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 25 Apr 2023 17:31:58 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:31:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:31:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:31:59 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:32:02 GMT
ADD file:aee0d7770ef2f24dc9697e86d391529d001a4013b6e30a3ac90a57932814a57e in / 
# Tue, 25 Apr 2023 17:32:02 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 03:25:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 03:25:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 03:25:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 03:25:23 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 03:25:47 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 04 May 2023 03:26:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 03:26:10 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 11:14:20 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 04 May 2023 11:14:20 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 11:14:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 04 May 2023 11:14:21 GMT
WORKDIR /usr/local/tomcat
# Thu, 04 May 2023 11:14:21 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 11:14:21 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 04 May 2023 11:15:34 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 04 May 2023 11:15:34 GMT
ENV TOMCAT_MAJOR=9
# Wed, 10 May 2023 17:56:49 GMT
ENV TOMCAT_VERSION=9.0.75
# Wed, 10 May 2023 17:56:49 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Wed, 10 May 2023 17:56:49 GMT
COPY dir:2a613f9e425d5febc8be5b6c17f49b39f1b8ad84b1601f07f76abed41b25b24b in /usr/local/tomcat 
# Wed, 10 May 2023 17:56:52 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 17:56:54 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 10 May 2023 17:56:54 GMT
EXPOSE 8080
# Wed, 10 May 2023 17:56:54 GMT
CMD ["catalina.sh" "run"]
# Wed, 10 May 2023 18:22:09 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 10 May 2023 18:22:10 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 10 May 2023 18:24:24 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2023 18:24:27 GMT
ENV XWIKI_VERSION=15.3
# Wed, 10 May 2023 18:24:28 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.3
# Wed, 10 May 2023 18:24:28 GMT
ENV XWIKI_DOWNLOAD_SHA256=fbe35bcc5c6cc5764f2a1da4aca7878531f93bae069d94f399fea7d9656da3b8
# Wed, 10 May 2023 18:25:07 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 10 May 2023 18:25:10 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Wed, 10 May 2023 18:25:10 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 10 May 2023 18:25:10 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 10 May 2023 18:25:11 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 10 May 2023 18:25:11 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 10 May 2023 18:25:11 GMT
VOLUME [/usr/local/xwiki]
# Wed, 10 May 2023 18:25:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 May 2023 18:25:11 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f3f60f415e9a03eed88bd5dd5268c841cde08dacf16911a3ef1e4e0fcdd76568`  
		Last Modified: Wed, 26 Apr 2023 02:08:37 GMT  
		Size: 28.4 MB (28389440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fb3595122d1cb6fffe722e2624c3c89b00776b393256a5444af56ceda691cf`  
		Last Modified: Thu, 04 May 2023 03:28:13 GMT  
		Size: 12.5 MB (12463858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5542665e33e692b672a405517e6e267c4c6e210bc410b97a6a1ce732618caa87`  
		Last Modified: Thu, 04 May 2023 03:29:19 GMT  
		Size: 45.0 MB (45009401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e52b8550f0ced98adb0880bd041e361ffb69810e6071e6d71eb2ec0c8ecfad5`  
		Last Modified: Thu, 04 May 2023 03:29:14 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea5566732e0a920d0a63e4fbebf073d2c49e3f80716df462e73f895cc0c5dfa`  
		Last Modified: Thu, 04 May 2023 11:24:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c6d16bf5ef403ef11a1cc9e40650f402cd1f8269d16982f7daebc2a76ab0d9`  
		Last Modified: Wed, 10 May 2023 18:03:56 GMT  
		Size: 12.2 MB (12242222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eaf464f1c82b5f85e3173b2c732f0928a28e669fcc4af9eb6da48199e92ae50`  
		Last Modified: Wed, 10 May 2023 18:03:55 GMT  
		Size: 453.7 KB (453682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ef5f2b94b25f2b0f609c429cc1626d9dd857d8294d2d872d6595bdeff3a5ca`  
		Last Modified: Wed, 10 May 2023 18:03:55 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e76b785cabb7a84968f4d713d3072c255796ddcef576690d954e3fc5b1a09604`  
		Last Modified: Wed, 10 May 2023 18:28:29 GMT  
		Size: 174.3 MB (174290936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bbb1bea6fd7e5ad54d9a435449598eab16234ad43ac144f2e8bfd3d6ba08f53`  
		Last Modified: Wed, 10 May 2023 18:28:26 GMT  
		Size: 306.2 MB (306214328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ec4bf084be2f31ea6d132041630e63267918cd9d3fda2c1c5729796be49ca3`  
		Last Modified: Wed, 10 May 2023 18:28:12 GMT  
		Size: 936.9 KB (936850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35482f801e8bffd20763dc900fe57a71e0b8b6e9704fc5960d1ae5c49c36568f`  
		Last Modified: Wed, 10 May 2023 18:28:12 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73fefab11cdaf813c0992abeb9546ca3853626b0c153d8792dda45700405f9d7`  
		Last Modified: Wed, 10 May 2023 18:28:12 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510da944c55d824606569a712e2defc95041c832ea8b07bd45aca2bf455095c2`  
		Last Modified: Wed, 10 May 2023 18:28:12 GMT  
		Size: 6.0 KB (6005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60c6d213e30aaeb6555c54770342ec9de274eb11eff3007dc29f2d552d0dd36c`  
		Last Modified: Wed, 10 May 2023 18:28:12 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
