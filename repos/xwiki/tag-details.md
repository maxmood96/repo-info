<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `xwiki`

-	[`xwiki:13`](#xwiki13)
-	[`xwiki:13-mariadb-tomcat`](#xwiki13-mariadb-tomcat)
-	[`xwiki:13-mysql-tomcat`](#xwiki13-mysql-tomcat)
-	[`xwiki:13-postgres-tomcat`](#xwiki13-postgres-tomcat)
-	[`xwiki:13.10`](#xwiki1310)
-	[`xwiki:13.10-mariadb-tomcat`](#xwiki1310-mariadb-tomcat)
-	[`xwiki:13.10-mysql-tomcat`](#xwiki1310-mysql-tomcat)
-	[`xwiki:13.10-postgres-tomcat`](#xwiki1310-postgres-tomcat)
-	[`xwiki:13.10.7`](#xwiki13107)
-	[`xwiki:13.10.7-mariadb-tomcat`](#xwiki13107-mariadb-tomcat)
-	[`xwiki:13.10.7-mysql-tomcat`](#xwiki13107-mysql-tomcat)
-	[`xwiki:13.10.7-postgres-tomcat`](#xwiki13107-postgres-tomcat)
-	[`xwiki:14`](#xwiki14)
-	[`xwiki:14-mariadb-tomcat`](#xwiki14-mariadb-tomcat)
-	[`xwiki:14-mysql-tomcat`](#xwiki14-mysql-tomcat)
-	[`xwiki:14-postgres-tomcat`](#xwiki14-postgres-tomcat)
-	[`xwiki:14.4`](#xwiki144)
-	[`xwiki:14.4-mariadb-tomcat`](#xwiki144-mariadb-tomcat)
-	[`xwiki:14.4-mysql-tomcat`](#xwiki144-mysql-tomcat)
-	[`xwiki:14.4-postgres-tomcat`](#xwiki144-postgres-tomcat)
-	[`xwiki:14.4.1`](#xwiki1441)
-	[`xwiki:14.4.1-mariadb-tomcat`](#xwiki1441-mariadb-tomcat)
-	[`xwiki:14.4.1-mysql-tomcat`](#xwiki1441-mysql-tomcat)
-	[`xwiki:14.4.1-postgres-tomcat`](#xwiki1441-postgres-tomcat)
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

## `xwiki:13`

```console
$ docker pull xwiki@sha256:538c472ff45f7c146d4cfbf1e7b31fb39f111a3d49287f502a6d2f71777ff333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:13` - linux; amd64

```console
$ docker pull xwiki@sha256:d6bbb60b487ca00096f55242a245f5d8021e42013dc9a65227548a78a0e39f38
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.1 MB (563089744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce3a4cc5ca40c56b140b6c3abe277f24fb0842adc6ec43651543be6f4ba1e449`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:14:23 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 00:14:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:58 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:59 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 06:30:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:30:41 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 06:30:41 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:30:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:35:57 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 06:35:58 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 00:18:07 GMT
COPY dir:360b17da945f7a5c4dcdc8b0602904442d98c06d17157280c607532ec8b6edaa in /usr/local/tomcat 
# Fri, 10 Jun 2022 00:18:12 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 00:18:13 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 00:18:13 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 00:18:13 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:25:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 24 Jun 2022 03:08:16 GMT
ENV XWIKI_VERSION=13.10.7
# Fri, 24 Jun 2022 03:08:16 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10.7
# Fri, 24 Jun 2022 03:08:16 GMT
ENV XWIKI_DOWNLOAD_SHA256=b886e886ed34e8d7bea8feb2e74e94edb3fb88030f90ab68c7bbc87dcf453d00
# Fri, 24 Jun 2022 03:08:54 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 24 Jun 2022 03:08:54 GMT
ENV MYSQL_JDBC_VERSION=8.0.29
# Fri, 24 Jun 2022 03:08:55 GMT
ENV MYSQL_JDBC_SHA256=d4e32d2a6026b5acc00300b73a86c28fb92681ae9629b21048ee67014c911db6
# Fri, 24 Jun 2022 03:08:55 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.29
# Fri, 24 Jun 2022 03:08:55 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.29.jar
# Fri, 24 Jun 2022 03:08:55 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.29.jar
# Fri, 24 Jun 2022 03:08:56 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 24 Jun 2022 03:08:56 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 24 Jun 2022 03:08:56 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 24 Jun 2022 03:08:56 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 24 Jun 2022 03:08:57 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 24 Jun 2022 03:08:57 GMT
VOLUME [/usr/local/xwiki]
# Fri, 24 Jun 2022 03:08:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jun 2022 03:08:57 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b669251e19038a24bd6cab0baab92077f23163880fac4701fb3efa564350732b`  
		Last Modified: Tue, 07 Jun 2022 00:21:34 GMT  
		Size: 43.3 MB (43267270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf45eff8a02bcdf7a96904e0dc534c78c89a5c860e224fa57780ef2fc2eab99e`  
		Last Modified: Tue, 07 Jun 2022 00:21:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246089a07769500a0adb027d1dc0efbb1254ee07d75dcdc6f8a3ceb8bae3e95f`  
		Last Modified: Tue, 07 Jun 2022 06:48:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3636fe8b4383f769da39b4c598b1e98b53b6d528e34e9d20fac5c17cfefcd866`  
		Last Modified: Fri, 10 Jun 2022 00:40:50 GMT  
		Size: 12.2 MB (12247499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0a0fd2a02961d2a1725c94d0c0f5670c51d5f5f9bad820a96e45791a5d7a32`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 445.5 KB (445476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beba28f927b0599e17785c8f69b8373e61c14da42247f7683f924f80ecae1439`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c54774971cb7c57e8fe14a42f90f7e4cceb67150ff2f3112f9ad46fea390190d`  
		Last Modified: Wed, 22 Jun 2022 04:30:07 GMT  
		Size: 167.5 MB (167492656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f8955940c07caf93c5b3787f4d50541ad84d1a6b710568178150ed29fa8c1fa`  
		Last Modified: Fri, 24 Jun 2022 03:11:53 GMT  
		Size: 292.6 MB (292641283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7511706ae08b48d6c19d83e802574606ae85b91839fd444ed4e26a21afa13cd`  
		Last Modified: Fri, 24 Jun 2022 03:11:35 GMT  
		Size: 2.4 MB (2381172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13635cdd2c775430a870517defaca7b40e34781684ba15c1c4bf4a47a22d7a9f`  
		Last Modified: Fri, 24 Jun 2022 03:11:35 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a6406d38ab58e4a678b831cfa2cf3dc65217dfc73299c135a3c2947cbf288b`  
		Last Modified: Fri, 24 Jun 2022 03:11:35 GMT  
		Size: 2.3 KB (2312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:112f72e7060631567b461a6b28b02795ad282cad23c101738ae01981635a0371`  
		Last Modified: Fri, 24 Jun 2022 03:11:35 GMT  
		Size: 5.3 KB (5338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c054adc9f3f529d9b827670e5c7c0878dd4b56f3f90e919891c04cd198e7bbb`  
		Last Modified: Fri, 24 Jun 2022 03:11:35 GMT  
		Size: 2.5 KB (2501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:13` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:8239f349f41eb1485f92190c846e889c7c6a069deef3e4810d62b3dca3b5cde9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **555.6 MB (555571284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d7ea8edd21d6b5820cbde3f17f19999ebce9e4ad1f0005dd187c3c77c3f8335`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:00:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:35:32 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 06:36:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:36:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:36:20 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 10:50:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 10:50:03 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 10:50:04 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 10:50:05 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 10:50:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:50:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:59:13 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 10:59:14 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 01:28:16 GMT
COPY dir:1fb0204bb532a7d63a0dd2d2677d66a70be0285454d27afba6780853636ba1ef in /usr/local/tomcat 
# Fri, 10 Jun 2022 01:28:22 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 01:28:24 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 01:28:25 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 01:28:26 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:24 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:25 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:09:26 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:09:27 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:10:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 24 Jun 2022 08:10:35 GMT
ENV XWIKI_VERSION=13.10.7
# Fri, 24 Jun 2022 08:10:35 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10.7
# Fri, 24 Jun 2022 08:10:36 GMT
ENV XWIKI_DOWNLOAD_SHA256=b886e886ed34e8d7bea8feb2e74e94edb3fb88030f90ab68c7bbc87dcf453d00
# Fri, 24 Jun 2022 08:11:07 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 24 Jun 2022 08:11:08 GMT
ENV MYSQL_JDBC_VERSION=8.0.29
# Fri, 24 Jun 2022 08:11:08 GMT
ENV MYSQL_JDBC_SHA256=d4e32d2a6026b5acc00300b73a86c28fb92681ae9629b21048ee67014c911db6
# Fri, 24 Jun 2022 08:11:09 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.29
# Fri, 24 Jun 2022 08:11:10 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.29.jar
# Fri, 24 Jun 2022 08:11:11 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.29.jar
# Fri, 24 Jun 2022 08:11:13 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 24 Jun 2022 08:11:14 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 24 Jun 2022 08:11:15 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 24 Jun 2022 08:11:16 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 24 Jun 2022 08:11:17 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 24 Jun 2022 08:11:17 GMT
VOLUME [/usr/local/xwiki]
# Fri, 24 Jun 2022 08:11:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jun 2022 08:11:19 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15da1b4c110f7cc460fbf968fb55b77c541f0e3ab87b92d5e6a822cc2c593e1`  
		Last Modified: Tue, 07 Jun 2022 05:10:23 GMT  
		Size: 15.9 MB (15898299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8e9d6a15d13e6f2d5d43f40b76051350cb7090cfcae5300dc1647e3196577a`  
		Last Modified: Tue, 07 Jun 2022 06:44:15 GMT  
		Size: 41.6 MB (41608356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51219ca7d003431d2f9c6ddda7db0a1902cf2b7e4e879625811b086f268b39c`  
		Last Modified: Tue, 07 Jun 2022 06:44:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5aa4900f44b9e3e20168d54fda3a0b78e62d572de1796db20345b70b1d8b3ca`  
		Last Modified: Tue, 07 Jun 2022 11:23:12 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6796806c88914990f15047665e74a4ea1fb933bdf7b8ebf39b1f2a82b723e044`  
		Last Modified: Fri, 10 Jun 2022 02:03:21 GMT  
		Size: 12.3 MB (12264791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca37469fc5a6ebbc5f1a764aabd4ba48b92a85d1396b644e1139994fad2fa34e`  
		Last Modified: Fri, 10 Jun 2022 02:03:20 GMT  
		Size: 208.8 KB (208841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c24501792b443d8ecb222b1c49c98ee84d4d76016bdbf8ba61b488fa873f7f`  
		Last Modified: Wed, 22 Jun 2022 04:17:01 GMT  
		Size: 163.4 MB (163365370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d4c4674e614cb6318120b7f3b95cc0f15a199054f449c2735cf25af9e2fd68`  
		Last Modified: Fri, 24 Jun 2022 08:14:37 GMT  
		Size: 292.6 MB (292641477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f45433cd06ad26dbb57afb98818c085a9ba114157cc72fa70214f8949e3ccfc`  
		Last Modified: Fri, 24 Jun 2022 08:14:15 GMT  
		Size: 2.4 MB (2381180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f75bf932706df5ca8d04fa02d8711685191f1f1dd7deb53937ba6f1371cb7fc5`  
		Last Modified: Fri, 24 Jun 2022 08:14:14 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04bce02a10640eb0a28ea0cd65126f65a6425540f18bd2acd881ed919828c057`  
		Last Modified: Fri, 24 Jun 2022 08:14:14 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:258f35d21774001fddc3b61192c74e053da90db66513a55c26d096b10ee59564`  
		Last Modified: Fri, 24 Jun 2022 08:14:14 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b877bc26e0f91fafb0bcbe8b609880d5c9cfba95b167970bae7650e06a31d706`  
		Last Modified: Fri, 24 Jun 2022 08:14:14 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13-mariadb-tomcat`

```console
$ docker pull xwiki@sha256:7e992a39803f1553703a95e1c243d3e530a70c492c48ce9f4721f3c0cac22740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:13-mariadb-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:fe68d60e91e8d3eb0e5d23a11eb5b888b7350043a1edc71fd12266ce62957ac7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **561.2 MB (561248650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c580180cdf614c4e58b233442d12859c0c06fb61a5c351ff96835ef123570549`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:14:23 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 00:14:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:58 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:59 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 06:30:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:30:41 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 06:30:41 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:30:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:35:57 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 06:35:58 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 00:18:07 GMT
COPY dir:360b17da945f7a5c4dcdc8b0602904442d98c06d17157280c607532ec8b6edaa in /usr/local/tomcat 
# Fri, 10 Jun 2022 00:18:12 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 00:18:13 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 00:18:13 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 00:18:13 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:25:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 24 Jun 2022 03:08:16 GMT
ENV XWIKI_VERSION=13.10.7
# Fri, 24 Jun 2022 03:08:16 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10.7
# Fri, 24 Jun 2022 03:08:16 GMT
ENV XWIKI_DOWNLOAD_SHA256=b886e886ed34e8d7bea8feb2e74e94edb3fb88030f90ab68c7bbc87dcf453d00
# Fri, 24 Jun 2022 03:08:54 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 24 Jun 2022 03:10:42 GMT
ENV MARIADB_JDBC_VERSION=3.0.5
# Fri, 24 Jun 2022 03:10:42 GMT
ENV MARIADB_JDBC_SHA256=e9532d9bca07c1263c32b00b495bd3ec7f2b79320513cabd762bf39ea09e68d9
# Fri, 24 Jun 2022 03:10:43 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.0.5
# Fri, 24 Jun 2022 03:10:43 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.0.5.jar
# Fri, 24 Jun 2022 03:10:43 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.0.5.jar
# Fri, 24 Jun 2022 03:10:43 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Fri, 24 Jun 2022 03:10:44 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 24 Jun 2022 03:10:44 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 24 Jun 2022 03:10:44 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 24 Jun 2022 03:10:44 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 24 Jun 2022 03:10:44 GMT
VOLUME [/usr/local/xwiki]
# Fri, 24 Jun 2022 03:10:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jun 2022 03:10:45 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b669251e19038a24bd6cab0baab92077f23163880fac4701fb3efa564350732b`  
		Last Modified: Tue, 07 Jun 2022 00:21:34 GMT  
		Size: 43.3 MB (43267270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf45eff8a02bcdf7a96904e0dc534c78c89a5c860e224fa57780ef2fc2eab99e`  
		Last Modified: Tue, 07 Jun 2022 00:21:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246089a07769500a0adb027d1dc0efbb1254ee07d75dcdc6f8a3ceb8bae3e95f`  
		Last Modified: Tue, 07 Jun 2022 06:48:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3636fe8b4383f769da39b4c598b1e98b53b6d528e34e9d20fac5c17cfefcd866`  
		Last Modified: Fri, 10 Jun 2022 00:40:50 GMT  
		Size: 12.2 MB (12247499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0a0fd2a02961d2a1725c94d0c0f5670c51d5f5f9bad820a96e45791a5d7a32`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 445.5 KB (445476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beba28f927b0599e17785c8f69b8373e61c14da42247f7683f924f80ecae1439`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c54774971cb7c57e8fe14a42f90f7e4cceb67150ff2f3112f9ad46fea390190d`  
		Last Modified: Wed, 22 Jun 2022 04:30:07 GMT  
		Size: 167.5 MB (167492656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f8955940c07caf93c5b3787f4d50541ad84d1a6b710568178150ed29fa8c1fa`  
		Last Modified: Fri, 24 Jun 2022 03:11:53 GMT  
		Size: 292.6 MB (292641283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39e75aa0ee70148e023225e5c15afe6370fae11ad20051cbdc9ad36c048410cb`  
		Last Modified: Fri, 24 Jun 2022 03:13:09 GMT  
		Size: 540.1 KB (540074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a78e618b05c2bd943951d754b0495482861f717b916017efa2d775bd91113d07`  
		Last Modified: Fri, 24 Jun 2022 03:13:08 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77f7e7cac8551052ca6034a6b13460c7245751fa15ed047622af1e3a4bdf80e0`  
		Last Modified: Fri, 24 Jun 2022 03:13:08 GMT  
		Size: 2.3 KB (2313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ac5252f40483fbc8e8acc62ff8428fe4b47a3a203ef6412edda8b83a0bfea19`  
		Last Modified: Fri, 24 Jun 2022 03:13:08 GMT  
		Size: 5.3 KB (5339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea840c472b11a8abe56d67979ba671ee677a5046199e8f29afff0c3f9b6871a`  
		Last Modified: Fri, 24 Jun 2022 03:13:08 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:13-mariadb-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:f69b33053370bb439577df2ccf0307fb2b1e92e7ad2e3000e27165d0508ce769
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **553.7 MB (553730176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77e99996ea02f728cd4df08569f2a56128eb95625ce333da516f87ca24dfb42d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:00:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:35:32 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 06:36:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:36:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:36:20 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 10:50:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 10:50:03 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 10:50:04 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 10:50:05 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 10:50:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:50:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:59:13 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 10:59:14 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 01:28:16 GMT
COPY dir:1fb0204bb532a7d63a0dd2d2677d66a70be0285454d27afba6780853636ba1ef in /usr/local/tomcat 
# Fri, 10 Jun 2022 01:28:22 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 01:28:24 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 01:28:25 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 01:28:26 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:24 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:25 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:09:26 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:09:27 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:10:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 24 Jun 2022 08:10:35 GMT
ENV XWIKI_VERSION=13.10.7
# Fri, 24 Jun 2022 08:10:35 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10.7
# Fri, 24 Jun 2022 08:10:36 GMT
ENV XWIKI_DOWNLOAD_SHA256=b886e886ed34e8d7bea8feb2e74e94edb3fb88030f90ab68c7bbc87dcf453d00
# Fri, 24 Jun 2022 08:11:07 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 24 Jun 2022 08:12:29 GMT
ENV MARIADB_JDBC_VERSION=3.0.5
# Fri, 24 Jun 2022 08:12:30 GMT
ENV MARIADB_JDBC_SHA256=e9532d9bca07c1263c32b00b495bd3ec7f2b79320513cabd762bf39ea09e68d9
# Fri, 24 Jun 2022 08:12:31 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.0.5
# Fri, 24 Jun 2022 08:12:32 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.0.5.jar
# Fri, 24 Jun 2022 08:12:33 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.0.5.jar
# Fri, 24 Jun 2022 08:12:35 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Fri, 24 Jun 2022 08:12:36 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 24 Jun 2022 08:12:37 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 24 Jun 2022 08:12:38 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 24 Jun 2022 08:12:39 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 24 Jun 2022 08:12:39 GMT
VOLUME [/usr/local/xwiki]
# Fri, 24 Jun 2022 08:12:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jun 2022 08:12:41 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15da1b4c110f7cc460fbf968fb55b77c541f0e3ab87b92d5e6a822cc2c593e1`  
		Last Modified: Tue, 07 Jun 2022 05:10:23 GMT  
		Size: 15.9 MB (15898299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8e9d6a15d13e6f2d5d43f40b76051350cb7090cfcae5300dc1647e3196577a`  
		Last Modified: Tue, 07 Jun 2022 06:44:15 GMT  
		Size: 41.6 MB (41608356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51219ca7d003431d2f9c6ddda7db0a1902cf2b7e4e879625811b086f268b39c`  
		Last Modified: Tue, 07 Jun 2022 06:44:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5aa4900f44b9e3e20168d54fda3a0b78e62d572de1796db20345b70b1d8b3ca`  
		Last Modified: Tue, 07 Jun 2022 11:23:12 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6796806c88914990f15047665e74a4ea1fb933bdf7b8ebf39b1f2a82b723e044`  
		Last Modified: Fri, 10 Jun 2022 02:03:21 GMT  
		Size: 12.3 MB (12264791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca37469fc5a6ebbc5f1a764aabd4ba48b92a85d1396b644e1139994fad2fa34e`  
		Last Modified: Fri, 10 Jun 2022 02:03:20 GMT  
		Size: 208.8 KB (208841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c24501792b443d8ecb222b1c49c98ee84d4d76016bdbf8ba61b488fa873f7f`  
		Last Modified: Wed, 22 Jun 2022 04:17:01 GMT  
		Size: 163.4 MB (163365370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d4c4674e614cb6318120b7f3b95cc0f15a199054f449c2735cf25af9e2fd68`  
		Last Modified: Fri, 24 Jun 2022 08:14:37 GMT  
		Size: 292.6 MB (292641477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55eb49c20075c8f6f6c3474817337eac98d5ecd1d220ca225ede5b5d516ea478`  
		Last Modified: Fri, 24 Jun 2022 08:15:59 GMT  
		Size: 540.1 KB (540068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52ab0fc86a347634df62c569c68f1d90c68af8888bfd6761815c0dc42be1d9e3`  
		Last Modified: Fri, 24 Jun 2022 08:15:58 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:905cc4a353cba057e2dd9dd80f2a18dab3caf4cd39fc0fe50c6e5963c5ea3e55`  
		Last Modified: Fri, 24 Jun 2022 08:15:58 GMT  
		Size: 2.3 KB (2310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7cc5bcac189f250a4bf9f37357b4a4cadc7fc132044e958bcd14c24d26736ec`  
		Last Modified: Fri, 24 Jun 2022 08:15:58 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743fadc0e05f56a8caa0b29a7c3b8fddddca135a6fce4bd23eab3167966f8e5d`  
		Last Modified: Fri, 24 Jun 2022 08:15:58 GMT  
		Size: 2.5 KB (2507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13-mysql-tomcat`

```console
$ docker pull xwiki@sha256:538c472ff45f7c146d4cfbf1e7b31fb39f111a3d49287f502a6d2f71777ff333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:13-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:d6bbb60b487ca00096f55242a245f5d8021e42013dc9a65227548a78a0e39f38
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.1 MB (563089744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce3a4cc5ca40c56b140b6c3abe277f24fb0842adc6ec43651543be6f4ba1e449`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:14:23 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 00:14:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:58 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:59 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 06:30:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:30:41 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 06:30:41 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:30:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:35:57 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 06:35:58 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 00:18:07 GMT
COPY dir:360b17da945f7a5c4dcdc8b0602904442d98c06d17157280c607532ec8b6edaa in /usr/local/tomcat 
# Fri, 10 Jun 2022 00:18:12 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 00:18:13 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 00:18:13 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 00:18:13 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:25:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 24 Jun 2022 03:08:16 GMT
ENV XWIKI_VERSION=13.10.7
# Fri, 24 Jun 2022 03:08:16 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10.7
# Fri, 24 Jun 2022 03:08:16 GMT
ENV XWIKI_DOWNLOAD_SHA256=b886e886ed34e8d7bea8feb2e74e94edb3fb88030f90ab68c7bbc87dcf453d00
# Fri, 24 Jun 2022 03:08:54 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 24 Jun 2022 03:08:54 GMT
ENV MYSQL_JDBC_VERSION=8.0.29
# Fri, 24 Jun 2022 03:08:55 GMT
ENV MYSQL_JDBC_SHA256=d4e32d2a6026b5acc00300b73a86c28fb92681ae9629b21048ee67014c911db6
# Fri, 24 Jun 2022 03:08:55 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.29
# Fri, 24 Jun 2022 03:08:55 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.29.jar
# Fri, 24 Jun 2022 03:08:55 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.29.jar
# Fri, 24 Jun 2022 03:08:56 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 24 Jun 2022 03:08:56 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 24 Jun 2022 03:08:56 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 24 Jun 2022 03:08:56 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 24 Jun 2022 03:08:57 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 24 Jun 2022 03:08:57 GMT
VOLUME [/usr/local/xwiki]
# Fri, 24 Jun 2022 03:08:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jun 2022 03:08:57 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b669251e19038a24bd6cab0baab92077f23163880fac4701fb3efa564350732b`  
		Last Modified: Tue, 07 Jun 2022 00:21:34 GMT  
		Size: 43.3 MB (43267270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf45eff8a02bcdf7a96904e0dc534c78c89a5c860e224fa57780ef2fc2eab99e`  
		Last Modified: Tue, 07 Jun 2022 00:21:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246089a07769500a0adb027d1dc0efbb1254ee07d75dcdc6f8a3ceb8bae3e95f`  
		Last Modified: Tue, 07 Jun 2022 06:48:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3636fe8b4383f769da39b4c598b1e98b53b6d528e34e9d20fac5c17cfefcd866`  
		Last Modified: Fri, 10 Jun 2022 00:40:50 GMT  
		Size: 12.2 MB (12247499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0a0fd2a02961d2a1725c94d0c0f5670c51d5f5f9bad820a96e45791a5d7a32`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 445.5 KB (445476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beba28f927b0599e17785c8f69b8373e61c14da42247f7683f924f80ecae1439`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c54774971cb7c57e8fe14a42f90f7e4cceb67150ff2f3112f9ad46fea390190d`  
		Last Modified: Wed, 22 Jun 2022 04:30:07 GMT  
		Size: 167.5 MB (167492656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f8955940c07caf93c5b3787f4d50541ad84d1a6b710568178150ed29fa8c1fa`  
		Last Modified: Fri, 24 Jun 2022 03:11:53 GMT  
		Size: 292.6 MB (292641283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7511706ae08b48d6c19d83e802574606ae85b91839fd444ed4e26a21afa13cd`  
		Last Modified: Fri, 24 Jun 2022 03:11:35 GMT  
		Size: 2.4 MB (2381172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13635cdd2c775430a870517defaca7b40e34781684ba15c1c4bf4a47a22d7a9f`  
		Last Modified: Fri, 24 Jun 2022 03:11:35 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a6406d38ab58e4a678b831cfa2cf3dc65217dfc73299c135a3c2947cbf288b`  
		Last Modified: Fri, 24 Jun 2022 03:11:35 GMT  
		Size: 2.3 KB (2312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:112f72e7060631567b461a6b28b02795ad282cad23c101738ae01981635a0371`  
		Last Modified: Fri, 24 Jun 2022 03:11:35 GMT  
		Size: 5.3 KB (5338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c054adc9f3f529d9b827670e5c7c0878dd4b56f3f90e919891c04cd198e7bbb`  
		Last Modified: Fri, 24 Jun 2022 03:11:35 GMT  
		Size: 2.5 KB (2501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:13-mysql-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:8239f349f41eb1485f92190c846e889c7c6a069deef3e4810d62b3dca3b5cde9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **555.6 MB (555571284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d7ea8edd21d6b5820cbde3f17f19999ebce9e4ad1f0005dd187c3c77c3f8335`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:00:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:35:32 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 06:36:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:36:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:36:20 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 10:50:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 10:50:03 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 10:50:04 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 10:50:05 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 10:50:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:50:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:59:13 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 10:59:14 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 01:28:16 GMT
COPY dir:1fb0204bb532a7d63a0dd2d2677d66a70be0285454d27afba6780853636ba1ef in /usr/local/tomcat 
# Fri, 10 Jun 2022 01:28:22 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 01:28:24 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 01:28:25 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 01:28:26 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:24 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:25 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:09:26 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:09:27 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:10:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 24 Jun 2022 08:10:35 GMT
ENV XWIKI_VERSION=13.10.7
# Fri, 24 Jun 2022 08:10:35 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10.7
# Fri, 24 Jun 2022 08:10:36 GMT
ENV XWIKI_DOWNLOAD_SHA256=b886e886ed34e8d7bea8feb2e74e94edb3fb88030f90ab68c7bbc87dcf453d00
# Fri, 24 Jun 2022 08:11:07 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 24 Jun 2022 08:11:08 GMT
ENV MYSQL_JDBC_VERSION=8.0.29
# Fri, 24 Jun 2022 08:11:08 GMT
ENV MYSQL_JDBC_SHA256=d4e32d2a6026b5acc00300b73a86c28fb92681ae9629b21048ee67014c911db6
# Fri, 24 Jun 2022 08:11:09 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.29
# Fri, 24 Jun 2022 08:11:10 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.29.jar
# Fri, 24 Jun 2022 08:11:11 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.29.jar
# Fri, 24 Jun 2022 08:11:13 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 24 Jun 2022 08:11:14 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 24 Jun 2022 08:11:15 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 24 Jun 2022 08:11:16 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 24 Jun 2022 08:11:17 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 24 Jun 2022 08:11:17 GMT
VOLUME [/usr/local/xwiki]
# Fri, 24 Jun 2022 08:11:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jun 2022 08:11:19 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15da1b4c110f7cc460fbf968fb55b77c541f0e3ab87b92d5e6a822cc2c593e1`  
		Last Modified: Tue, 07 Jun 2022 05:10:23 GMT  
		Size: 15.9 MB (15898299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8e9d6a15d13e6f2d5d43f40b76051350cb7090cfcae5300dc1647e3196577a`  
		Last Modified: Tue, 07 Jun 2022 06:44:15 GMT  
		Size: 41.6 MB (41608356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51219ca7d003431d2f9c6ddda7db0a1902cf2b7e4e879625811b086f268b39c`  
		Last Modified: Tue, 07 Jun 2022 06:44:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5aa4900f44b9e3e20168d54fda3a0b78e62d572de1796db20345b70b1d8b3ca`  
		Last Modified: Tue, 07 Jun 2022 11:23:12 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6796806c88914990f15047665e74a4ea1fb933bdf7b8ebf39b1f2a82b723e044`  
		Last Modified: Fri, 10 Jun 2022 02:03:21 GMT  
		Size: 12.3 MB (12264791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca37469fc5a6ebbc5f1a764aabd4ba48b92a85d1396b644e1139994fad2fa34e`  
		Last Modified: Fri, 10 Jun 2022 02:03:20 GMT  
		Size: 208.8 KB (208841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c24501792b443d8ecb222b1c49c98ee84d4d76016bdbf8ba61b488fa873f7f`  
		Last Modified: Wed, 22 Jun 2022 04:17:01 GMT  
		Size: 163.4 MB (163365370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d4c4674e614cb6318120b7f3b95cc0f15a199054f449c2735cf25af9e2fd68`  
		Last Modified: Fri, 24 Jun 2022 08:14:37 GMT  
		Size: 292.6 MB (292641477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f45433cd06ad26dbb57afb98818c085a9ba114157cc72fa70214f8949e3ccfc`  
		Last Modified: Fri, 24 Jun 2022 08:14:15 GMT  
		Size: 2.4 MB (2381180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f75bf932706df5ca8d04fa02d8711685191f1f1dd7deb53937ba6f1371cb7fc5`  
		Last Modified: Fri, 24 Jun 2022 08:14:14 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04bce02a10640eb0a28ea0cd65126f65a6425540f18bd2acd881ed919828c057`  
		Last Modified: Fri, 24 Jun 2022 08:14:14 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:258f35d21774001fddc3b61192c74e053da90db66513a55c26d096b10ee59564`  
		Last Modified: Fri, 24 Jun 2022 08:14:14 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b877bc26e0f91fafb0bcbe8b609880d5c9cfba95b167970bae7650e06a31d706`  
		Last Modified: Fri, 24 Jun 2022 08:14:14 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13-postgres-tomcat`

```console
$ docker pull xwiki@sha256:b250edc19f4cc72d051ff836bc6a66dad2884231ad972b66018917572d37c35d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:13-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:638d7630646963b18a849058a847b7caab4ded28712b60b0d6d1900f56b0c537
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.3 MB (562304923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79cad287c34ddcfc1a8b8fa8c65cb34197ee741da2b4c8d387d6e0ad78009ec9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:14:23 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 00:14:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:58 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:59 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 06:30:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:30:41 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 06:30:41 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:30:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:35:57 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 06:35:58 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 00:18:07 GMT
COPY dir:360b17da945f7a5c4dcdc8b0602904442d98c06d17157280c607532ec8b6edaa in /usr/local/tomcat 
# Fri, 10 Jun 2022 00:18:12 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 00:18:13 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 00:18:13 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 00:18:13 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:26:27 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 24 Jun 2022 03:09:04 GMT
ENV XWIKI_VERSION=13.10.7
# Fri, 24 Jun 2022 03:09:04 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10.7
# Fri, 24 Jun 2022 03:09:05 GMT
ENV XWIKI_DOWNLOAD_SHA256=b886e886ed34e8d7bea8feb2e74e94edb3fb88030f90ab68c7bbc87dcf453d00
# Fri, 24 Jun 2022 03:10:26 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 24 Jun 2022 03:10:28 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 24 Jun 2022 03:10:28 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 24 Jun 2022 03:10:28 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 24 Jun 2022 03:10:29 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 24 Jun 2022 03:10:29 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 24 Jun 2022 03:10:29 GMT
VOLUME [/usr/local/xwiki]
# Fri, 24 Jun 2022 03:10:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jun 2022 03:10:29 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b669251e19038a24bd6cab0baab92077f23163880fac4701fb3efa564350732b`  
		Last Modified: Tue, 07 Jun 2022 00:21:34 GMT  
		Size: 43.3 MB (43267270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf45eff8a02bcdf7a96904e0dc534c78c89a5c860e224fa57780ef2fc2eab99e`  
		Last Modified: Tue, 07 Jun 2022 00:21:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246089a07769500a0adb027d1dc0efbb1254ee07d75dcdc6f8a3ceb8bae3e95f`  
		Last Modified: Tue, 07 Jun 2022 06:48:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3636fe8b4383f769da39b4c598b1e98b53b6d528e34e9d20fac5c17cfefcd866`  
		Last Modified: Fri, 10 Jun 2022 00:40:50 GMT  
		Size: 12.2 MB (12247499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0a0fd2a02961d2a1725c94d0c0f5670c51d5f5f9bad820a96e45791a5d7a32`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 445.5 KB (445476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beba28f927b0599e17785c8f69b8373e61c14da42247f7683f924f80ecae1439`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:657eec0a2bb289006e136ad46dbd1d85e8ff10712e1477c0fcacb617a19bb242`  
		Last Modified: Wed, 22 Jun 2022 04:31:12 GMT  
		Size: 168.3 MB (168293438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:136be306a609540683e370b2425b4d3703542a79224441c6337af82ee1698ca2`  
		Last Modified: Fri, 24 Jun 2022 03:12:46 GMT  
		Size: 292.6 MB (292641286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3769fbd23a38bb2c2737d30cd4a790f8ad775a99a63e6591de2df21d750f52`  
		Last Modified: Fri, 24 Jun 2022 03:12:29 GMT  
		Size: 795.4 KB (795424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:155517bc4fff02081a754dd1ac5674da90d74db9792a871f64983196cbd2b573`  
		Last Modified: Fri, 24 Jun 2022 03:12:28 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e9d584cf5548a2a612999b7b8fb340c4a38d8e9b31fd9ab73ca09cb173eb0f`  
		Last Modified: Fri, 24 Jun 2022 03:12:28 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2330650c98390edb3e1e7bd4d667c7b4e344da794f180c208aa1c92872db10cc`  
		Last Modified: Fri, 24 Jun 2022 03:12:29 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9458af98469686b7341e974f7343a72938ca0fa6984c887bb8d0a160375881ee`  
		Last Modified: Fri, 24 Jun 2022 03:12:29 GMT  
		Size: 2.5 KB (2503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:13-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:bb8443f4c39a1e5e1eaa389c87f32b928bccad2f727705a2e02afcc1b98ac2bf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.8 MB (554784337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99d205394842fb0b6709b682ff9d39e01d0ade2e25f08c11c4c8c766f9ccd182`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:00:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:35:32 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 06:36:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:36:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:36:20 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 10:50:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 10:50:03 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 10:50:04 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 10:50:05 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 10:50:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:50:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:59:13 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 10:59:14 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 01:28:16 GMT
COPY dir:1fb0204bb532a7d63a0dd2d2677d66a70be0285454d27afba6780853636ba1ef in /usr/local/tomcat 
# Fri, 10 Jun 2022 01:28:22 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 01:28:24 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 01:28:25 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 01:28:26 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:24 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:25 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:09:26 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:09:27 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:11:42 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 24 Jun 2022 08:11:28 GMT
ENV XWIKI_VERSION=13.10.7
# Fri, 24 Jun 2022 08:11:29 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10.7
# Fri, 24 Jun 2022 08:11:30 GMT
ENV XWIKI_DOWNLOAD_SHA256=b886e886ed34e8d7bea8feb2e74e94edb3fb88030f90ab68c7bbc87dcf453d00
# Fri, 24 Jun 2022 08:12:12 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 24 Jun 2022 08:12:13 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 24 Jun 2022 08:12:14 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 24 Jun 2022 08:12:15 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 24 Jun 2022 08:12:16 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 24 Jun 2022 08:12:17 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 24 Jun 2022 08:12:17 GMT
VOLUME [/usr/local/xwiki]
# Fri, 24 Jun 2022 08:12:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jun 2022 08:12:19 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15da1b4c110f7cc460fbf968fb55b77c541f0e3ab87b92d5e6a822cc2c593e1`  
		Last Modified: Tue, 07 Jun 2022 05:10:23 GMT  
		Size: 15.9 MB (15898299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8e9d6a15d13e6f2d5d43f40b76051350cb7090cfcae5300dc1647e3196577a`  
		Last Modified: Tue, 07 Jun 2022 06:44:15 GMT  
		Size: 41.6 MB (41608356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51219ca7d003431d2f9c6ddda7db0a1902cf2b7e4e879625811b086f268b39c`  
		Last Modified: Tue, 07 Jun 2022 06:44:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5aa4900f44b9e3e20168d54fda3a0b78e62d572de1796db20345b70b1d8b3ca`  
		Last Modified: Tue, 07 Jun 2022 11:23:12 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6796806c88914990f15047665e74a4ea1fb933bdf7b8ebf39b1f2a82b723e044`  
		Last Modified: Fri, 10 Jun 2022 02:03:21 GMT  
		Size: 12.3 MB (12264791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca37469fc5a6ebbc5f1a764aabd4ba48b92a85d1396b644e1139994fad2fa34e`  
		Last Modified: Fri, 10 Jun 2022 02:03:20 GMT  
		Size: 208.8 KB (208841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbf4753a12af2d02fd26a953119f6843f7e381cfec0d679d92b04b4e4f5a3d6a`  
		Last Modified: Wed, 22 Jun 2022 04:18:08 GMT  
		Size: 164.2 MB (164164156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acdad91995b0da375c92d6651576276e78123cfbb080e5444a094fc5033c930c`  
		Last Modified: Fri, 24 Jun 2022 08:15:36 GMT  
		Size: 292.6 MB (292641359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:350ecfd793c7e54308d1c7a22f36e2e098e8fdae31cecb75339bfa7f0a8b7af6`  
		Last Modified: Fri, 24 Jun 2022 08:15:14 GMT  
		Size: 795.4 KB (795417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c27ddaa528e0298945c5eca4aa5235bd761f13f40e2b35de068a7977434e571d`  
		Last Modified: Fri, 24 Jun 2022 08:15:14 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9edb1eb483f19a886fd0fcf80dc5c21e5ef36163eb1e8df94a3b80f508fbeff8`  
		Last Modified: Fri, 24 Jun 2022 08:15:14 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d9ff4c9416279f5b0a9e42bf517e29f15992d0a7a0c5d3361f7fbc8472c12d`  
		Last Modified: Fri, 24 Jun 2022 08:15:14 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be06063b865aaeadaa012c84711685856110099c19fa07ac1af19e12fa08cce`  
		Last Modified: Fri, 24 Jun 2022 08:15:14 GMT  
		Size: 2.5 KB (2507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13.10`

```console
$ docker pull xwiki@sha256:538c472ff45f7c146d4cfbf1e7b31fb39f111a3d49287f502a6d2f71777ff333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:13.10` - linux; amd64

```console
$ docker pull xwiki@sha256:d6bbb60b487ca00096f55242a245f5d8021e42013dc9a65227548a78a0e39f38
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.1 MB (563089744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce3a4cc5ca40c56b140b6c3abe277f24fb0842adc6ec43651543be6f4ba1e449`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:14:23 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 00:14:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:58 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:59 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 06:30:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:30:41 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 06:30:41 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:30:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:35:57 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 06:35:58 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 00:18:07 GMT
COPY dir:360b17da945f7a5c4dcdc8b0602904442d98c06d17157280c607532ec8b6edaa in /usr/local/tomcat 
# Fri, 10 Jun 2022 00:18:12 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 00:18:13 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 00:18:13 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 00:18:13 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:25:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 24 Jun 2022 03:08:16 GMT
ENV XWIKI_VERSION=13.10.7
# Fri, 24 Jun 2022 03:08:16 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10.7
# Fri, 24 Jun 2022 03:08:16 GMT
ENV XWIKI_DOWNLOAD_SHA256=b886e886ed34e8d7bea8feb2e74e94edb3fb88030f90ab68c7bbc87dcf453d00
# Fri, 24 Jun 2022 03:08:54 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 24 Jun 2022 03:08:54 GMT
ENV MYSQL_JDBC_VERSION=8.0.29
# Fri, 24 Jun 2022 03:08:55 GMT
ENV MYSQL_JDBC_SHA256=d4e32d2a6026b5acc00300b73a86c28fb92681ae9629b21048ee67014c911db6
# Fri, 24 Jun 2022 03:08:55 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.29
# Fri, 24 Jun 2022 03:08:55 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.29.jar
# Fri, 24 Jun 2022 03:08:55 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.29.jar
# Fri, 24 Jun 2022 03:08:56 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 24 Jun 2022 03:08:56 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 24 Jun 2022 03:08:56 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 24 Jun 2022 03:08:56 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 24 Jun 2022 03:08:57 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 24 Jun 2022 03:08:57 GMT
VOLUME [/usr/local/xwiki]
# Fri, 24 Jun 2022 03:08:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jun 2022 03:08:57 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b669251e19038a24bd6cab0baab92077f23163880fac4701fb3efa564350732b`  
		Last Modified: Tue, 07 Jun 2022 00:21:34 GMT  
		Size: 43.3 MB (43267270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf45eff8a02bcdf7a96904e0dc534c78c89a5c860e224fa57780ef2fc2eab99e`  
		Last Modified: Tue, 07 Jun 2022 00:21:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246089a07769500a0adb027d1dc0efbb1254ee07d75dcdc6f8a3ceb8bae3e95f`  
		Last Modified: Tue, 07 Jun 2022 06:48:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3636fe8b4383f769da39b4c598b1e98b53b6d528e34e9d20fac5c17cfefcd866`  
		Last Modified: Fri, 10 Jun 2022 00:40:50 GMT  
		Size: 12.2 MB (12247499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0a0fd2a02961d2a1725c94d0c0f5670c51d5f5f9bad820a96e45791a5d7a32`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 445.5 KB (445476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beba28f927b0599e17785c8f69b8373e61c14da42247f7683f924f80ecae1439`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c54774971cb7c57e8fe14a42f90f7e4cceb67150ff2f3112f9ad46fea390190d`  
		Last Modified: Wed, 22 Jun 2022 04:30:07 GMT  
		Size: 167.5 MB (167492656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f8955940c07caf93c5b3787f4d50541ad84d1a6b710568178150ed29fa8c1fa`  
		Last Modified: Fri, 24 Jun 2022 03:11:53 GMT  
		Size: 292.6 MB (292641283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7511706ae08b48d6c19d83e802574606ae85b91839fd444ed4e26a21afa13cd`  
		Last Modified: Fri, 24 Jun 2022 03:11:35 GMT  
		Size: 2.4 MB (2381172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13635cdd2c775430a870517defaca7b40e34781684ba15c1c4bf4a47a22d7a9f`  
		Last Modified: Fri, 24 Jun 2022 03:11:35 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a6406d38ab58e4a678b831cfa2cf3dc65217dfc73299c135a3c2947cbf288b`  
		Last Modified: Fri, 24 Jun 2022 03:11:35 GMT  
		Size: 2.3 KB (2312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:112f72e7060631567b461a6b28b02795ad282cad23c101738ae01981635a0371`  
		Last Modified: Fri, 24 Jun 2022 03:11:35 GMT  
		Size: 5.3 KB (5338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c054adc9f3f529d9b827670e5c7c0878dd4b56f3f90e919891c04cd198e7bbb`  
		Last Modified: Fri, 24 Jun 2022 03:11:35 GMT  
		Size: 2.5 KB (2501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:13.10` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:8239f349f41eb1485f92190c846e889c7c6a069deef3e4810d62b3dca3b5cde9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **555.6 MB (555571284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d7ea8edd21d6b5820cbde3f17f19999ebce9e4ad1f0005dd187c3c77c3f8335`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:00:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:35:32 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 06:36:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:36:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:36:20 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 10:50:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 10:50:03 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 10:50:04 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 10:50:05 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 10:50:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:50:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:59:13 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 10:59:14 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 01:28:16 GMT
COPY dir:1fb0204bb532a7d63a0dd2d2677d66a70be0285454d27afba6780853636ba1ef in /usr/local/tomcat 
# Fri, 10 Jun 2022 01:28:22 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 01:28:24 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 01:28:25 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 01:28:26 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:24 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:25 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:09:26 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:09:27 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:10:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 24 Jun 2022 08:10:35 GMT
ENV XWIKI_VERSION=13.10.7
# Fri, 24 Jun 2022 08:10:35 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10.7
# Fri, 24 Jun 2022 08:10:36 GMT
ENV XWIKI_DOWNLOAD_SHA256=b886e886ed34e8d7bea8feb2e74e94edb3fb88030f90ab68c7bbc87dcf453d00
# Fri, 24 Jun 2022 08:11:07 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 24 Jun 2022 08:11:08 GMT
ENV MYSQL_JDBC_VERSION=8.0.29
# Fri, 24 Jun 2022 08:11:08 GMT
ENV MYSQL_JDBC_SHA256=d4e32d2a6026b5acc00300b73a86c28fb92681ae9629b21048ee67014c911db6
# Fri, 24 Jun 2022 08:11:09 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.29
# Fri, 24 Jun 2022 08:11:10 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.29.jar
# Fri, 24 Jun 2022 08:11:11 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.29.jar
# Fri, 24 Jun 2022 08:11:13 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 24 Jun 2022 08:11:14 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 24 Jun 2022 08:11:15 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 24 Jun 2022 08:11:16 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 24 Jun 2022 08:11:17 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 24 Jun 2022 08:11:17 GMT
VOLUME [/usr/local/xwiki]
# Fri, 24 Jun 2022 08:11:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jun 2022 08:11:19 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15da1b4c110f7cc460fbf968fb55b77c541f0e3ab87b92d5e6a822cc2c593e1`  
		Last Modified: Tue, 07 Jun 2022 05:10:23 GMT  
		Size: 15.9 MB (15898299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8e9d6a15d13e6f2d5d43f40b76051350cb7090cfcae5300dc1647e3196577a`  
		Last Modified: Tue, 07 Jun 2022 06:44:15 GMT  
		Size: 41.6 MB (41608356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51219ca7d003431d2f9c6ddda7db0a1902cf2b7e4e879625811b086f268b39c`  
		Last Modified: Tue, 07 Jun 2022 06:44:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5aa4900f44b9e3e20168d54fda3a0b78e62d572de1796db20345b70b1d8b3ca`  
		Last Modified: Tue, 07 Jun 2022 11:23:12 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6796806c88914990f15047665e74a4ea1fb933bdf7b8ebf39b1f2a82b723e044`  
		Last Modified: Fri, 10 Jun 2022 02:03:21 GMT  
		Size: 12.3 MB (12264791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca37469fc5a6ebbc5f1a764aabd4ba48b92a85d1396b644e1139994fad2fa34e`  
		Last Modified: Fri, 10 Jun 2022 02:03:20 GMT  
		Size: 208.8 KB (208841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c24501792b443d8ecb222b1c49c98ee84d4d76016bdbf8ba61b488fa873f7f`  
		Last Modified: Wed, 22 Jun 2022 04:17:01 GMT  
		Size: 163.4 MB (163365370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d4c4674e614cb6318120b7f3b95cc0f15a199054f449c2735cf25af9e2fd68`  
		Last Modified: Fri, 24 Jun 2022 08:14:37 GMT  
		Size: 292.6 MB (292641477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f45433cd06ad26dbb57afb98818c085a9ba114157cc72fa70214f8949e3ccfc`  
		Last Modified: Fri, 24 Jun 2022 08:14:15 GMT  
		Size: 2.4 MB (2381180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f75bf932706df5ca8d04fa02d8711685191f1f1dd7deb53937ba6f1371cb7fc5`  
		Last Modified: Fri, 24 Jun 2022 08:14:14 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04bce02a10640eb0a28ea0cd65126f65a6425540f18bd2acd881ed919828c057`  
		Last Modified: Fri, 24 Jun 2022 08:14:14 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:258f35d21774001fddc3b61192c74e053da90db66513a55c26d096b10ee59564`  
		Last Modified: Fri, 24 Jun 2022 08:14:14 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b877bc26e0f91fafb0bcbe8b609880d5c9cfba95b167970bae7650e06a31d706`  
		Last Modified: Fri, 24 Jun 2022 08:14:14 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13.10-mariadb-tomcat`

```console
$ docker pull xwiki@sha256:7e992a39803f1553703a95e1c243d3e530a70c492c48ce9f4721f3c0cac22740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:13.10-mariadb-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:fe68d60e91e8d3eb0e5d23a11eb5b888b7350043a1edc71fd12266ce62957ac7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **561.2 MB (561248650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c580180cdf614c4e58b233442d12859c0c06fb61a5c351ff96835ef123570549`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:14:23 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 00:14:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:58 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:59 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 06:30:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:30:41 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 06:30:41 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:30:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:35:57 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 06:35:58 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 00:18:07 GMT
COPY dir:360b17da945f7a5c4dcdc8b0602904442d98c06d17157280c607532ec8b6edaa in /usr/local/tomcat 
# Fri, 10 Jun 2022 00:18:12 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 00:18:13 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 00:18:13 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 00:18:13 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:25:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 24 Jun 2022 03:08:16 GMT
ENV XWIKI_VERSION=13.10.7
# Fri, 24 Jun 2022 03:08:16 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10.7
# Fri, 24 Jun 2022 03:08:16 GMT
ENV XWIKI_DOWNLOAD_SHA256=b886e886ed34e8d7bea8feb2e74e94edb3fb88030f90ab68c7bbc87dcf453d00
# Fri, 24 Jun 2022 03:08:54 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 24 Jun 2022 03:10:42 GMT
ENV MARIADB_JDBC_VERSION=3.0.5
# Fri, 24 Jun 2022 03:10:42 GMT
ENV MARIADB_JDBC_SHA256=e9532d9bca07c1263c32b00b495bd3ec7f2b79320513cabd762bf39ea09e68d9
# Fri, 24 Jun 2022 03:10:43 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.0.5
# Fri, 24 Jun 2022 03:10:43 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.0.5.jar
# Fri, 24 Jun 2022 03:10:43 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.0.5.jar
# Fri, 24 Jun 2022 03:10:43 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Fri, 24 Jun 2022 03:10:44 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 24 Jun 2022 03:10:44 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 24 Jun 2022 03:10:44 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 24 Jun 2022 03:10:44 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 24 Jun 2022 03:10:44 GMT
VOLUME [/usr/local/xwiki]
# Fri, 24 Jun 2022 03:10:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jun 2022 03:10:45 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b669251e19038a24bd6cab0baab92077f23163880fac4701fb3efa564350732b`  
		Last Modified: Tue, 07 Jun 2022 00:21:34 GMT  
		Size: 43.3 MB (43267270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf45eff8a02bcdf7a96904e0dc534c78c89a5c860e224fa57780ef2fc2eab99e`  
		Last Modified: Tue, 07 Jun 2022 00:21:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246089a07769500a0adb027d1dc0efbb1254ee07d75dcdc6f8a3ceb8bae3e95f`  
		Last Modified: Tue, 07 Jun 2022 06:48:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3636fe8b4383f769da39b4c598b1e98b53b6d528e34e9d20fac5c17cfefcd866`  
		Last Modified: Fri, 10 Jun 2022 00:40:50 GMT  
		Size: 12.2 MB (12247499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0a0fd2a02961d2a1725c94d0c0f5670c51d5f5f9bad820a96e45791a5d7a32`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 445.5 KB (445476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beba28f927b0599e17785c8f69b8373e61c14da42247f7683f924f80ecae1439`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c54774971cb7c57e8fe14a42f90f7e4cceb67150ff2f3112f9ad46fea390190d`  
		Last Modified: Wed, 22 Jun 2022 04:30:07 GMT  
		Size: 167.5 MB (167492656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f8955940c07caf93c5b3787f4d50541ad84d1a6b710568178150ed29fa8c1fa`  
		Last Modified: Fri, 24 Jun 2022 03:11:53 GMT  
		Size: 292.6 MB (292641283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39e75aa0ee70148e023225e5c15afe6370fae11ad20051cbdc9ad36c048410cb`  
		Last Modified: Fri, 24 Jun 2022 03:13:09 GMT  
		Size: 540.1 KB (540074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a78e618b05c2bd943951d754b0495482861f717b916017efa2d775bd91113d07`  
		Last Modified: Fri, 24 Jun 2022 03:13:08 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77f7e7cac8551052ca6034a6b13460c7245751fa15ed047622af1e3a4bdf80e0`  
		Last Modified: Fri, 24 Jun 2022 03:13:08 GMT  
		Size: 2.3 KB (2313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ac5252f40483fbc8e8acc62ff8428fe4b47a3a203ef6412edda8b83a0bfea19`  
		Last Modified: Fri, 24 Jun 2022 03:13:08 GMT  
		Size: 5.3 KB (5339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea840c472b11a8abe56d67979ba671ee677a5046199e8f29afff0c3f9b6871a`  
		Last Modified: Fri, 24 Jun 2022 03:13:08 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:13.10-mariadb-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:f69b33053370bb439577df2ccf0307fb2b1e92e7ad2e3000e27165d0508ce769
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **553.7 MB (553730176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77e99996ea02f728cd4df08569f2a56128eb95625ce333da516f87ca24dfb42d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:00:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:35:32 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 06:36:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:36:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:36:20 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 10:50:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 10:50:03 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 10:50:04 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 10:50:05 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 10:50:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:50:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:59:13 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 10:59:14 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 01:28:16 GMT
COPY dir:1fb0204bb532a7d63a0dd2d2677d66a70be0285454d27afba6780853636ba1ef in /usr/local/tomcat 
# Fri, 10 Jun 2022 01:28:22 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 01:28:24 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 01:28:25 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 01:28:26 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:24 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:25 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:09:26 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:09:27 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:10:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 24 Jun 2022 08:10:35 GMT
ENV XWIKI_VERSION=13.10.7
# Fri, 24 Jun 2022 08:10:35 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10.7
# Fri, 24 Jun 2022 08:10:36 GMT
ENV XWIKI_DOWNLOAD_SHA256=b886e886ed34e8d7bea8feb2e74e94edb3fb88030f90ab68c7bbc87dcf453d00
# Fri, 24 Jun 2022 08:11:07 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 24 Jun 2022 08:12:29 GMT
ENV MARIADB_JDBC_VERSION=3.0.5
# Fri, 24 Jun 2022 08:12:30 GMT
ENV MARIADB_JDBC_SHA256=e9532d9bca07c1263c32b00b495bd3ec7f2b79320513cabd762bf39ea09e68d9
# Fri, 24 Jun 2022 08:12:31 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.0.5
# Fri, 24 Jun 2022 08:12:32 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.0.5.jar
# Fri, 24 Jun 2022 08:12:33 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.0.5.jar
# Fri, 24 Jun 2022 08:12:35 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Fri, 24 Jun 2022 08:12:36 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 24 Jun 2022 08:12:37 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 24 Jun 2022 08:12:38 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 24 Jun 2022 08:12:39 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 24 Jun 2022 08:12:39 GMT
VOLUME [/usr/local/xwiki]
# Fri, 24 Jun 2022 08:12:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jun 2022 08:12:41 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15da1b4c110f7cc460fbf968fb55b77c541f0e3ab87b92d5e6a822cc2c593e1`  
		Last Modified: Tue, 07 Jun 2022 05:10:23 GMT  
		Size: 15.9 MB (15898299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8e9d6a15d13e6f2d5d43f40b76051350cb7090cfcae5300dc1647e3196577a`  
		Last Modified: Tue, 07 Jun 2022 06:44:15 GMT  
		Size: 41.6 MB (41608356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51219ca7d003431d2f9c6ddda7db0a1902cf2b7e4e879625811b086f268b39c`  
		Last Modified: Tue, 07 Jun 2022 06:44:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5aa4900f44b9e3e20168d54fda3a0b78e62d572de1796db20345b70b1d8b3ca`  
		Last Modified: Tue, 07 Jun 2022 11:23:12 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6796806c88914990f15047665e74a4ea1fb933bdf7b8ebf39b1f2a82b723e044`  
		Last Modified: Fri, 10 Jun 2022 02:03:21 GMT  
		Size: 12.3 MB (12264791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca37469fc5a6ebbc5f1a764aabd4ba48b92a85d1396b644e1139994fad2fa34e`  
		Last Modified: Fri, 10 Jun 2022 02:03:20 GMT  
		Size: 208.8 KB (208841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c24501792b443d8ecb222b1c49c98ee84d4d76016bdbf8ba61b488fa873f7f`  
		Last Modified: Wed, 22 Jun 2022 04:17:01 GMT  
		Size: 163.4 MB (163365370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d4c4674e614cb6318120b7f3b95cc0f15a199054f449c2735cf25af9e2fd68`  
		Last Modified: Fri, 24 Jun 2022 08:14:37 GMT  
		Size: 292.6 MB (292641477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55eb49c20075c8f6f6c3474817337eac98d5ecd1d220ca225ede5b5d516ea478`  
		Last Modified: Fri, 24 Jun 2022 08:15:59 GMT  
		Size: 540.1 KB (540068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52ab0fc86a347634df62c569c68f1d90c68af8888bfd6761815c0dc42be1d9e3`  
		Last Modified: Fri, 24 Jun 2022 08:15:58 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:905cc4a353cba057e2dd9dd80f2a18dab3caf4cd39fc0fe50c6e5963c5ea3e55`  
		Last Modified: Fri, 24 Jun 2022 08:15:58 GMT  
		Size: 2.3 KB (2310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7cc5bcac189f250a4bf9f37357b4a4cadc7fc132044e958bcd14c24d26736ec`  
		Last Modified: Fri, 24 Jun 2022 08:15:58 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743fadc0e05f56a8caa0b29a7c3b8fddddca135a6fce4bd23eab3167966f8e5d`  
		Last Modified: Fri, 24 Jun 2022 08:15:58 GMT  
		Size: 2.5 KB (2507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13.10-mysql-tomcat`

```console
$ docker pull xwiki@sha256:538c472ff45f7c146d4cfbf1e7b31fb39f111a3d49287f502a6d2f71777ff333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:13.10-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:d6bbb60b487ca00096f55242a245f5d8021e42013dc9a65227548a78a0e39f38
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.1 MB (563089744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce3a4cc5ca40c56b140b6c3abe277f24fb0842adc6ec43651543be6f4ba1e449`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:14:23 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 00:14:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:58 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:59 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 06:30:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:30:41 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 06:30:41 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:30:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:35:57 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 06:35:58 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 00:18:07 GMT
COPY dir:360b17da945f7a5c4dcdc8b0602904442d98c06d17157280c607532ec8b6edaa in /usr/local/tomcat 
# Fri, 10 Jun 2022 00:18:12 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 00:18:13 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 00:18:13 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 00:18:13 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:25:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 24 Jun 2022 03:08:16 GMT
ENV XWIKI_VERSION=13.10.7
# Fri, 24 Jun 2022 03:08:16 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10.7
# Fri, 24 Jun 2022 03:08:16 GMT
ENV XWIKI_DOWNLOAD_SHA256=b886e886ed34e8d7bea8feb2e74e94edb3fb88030f90ab68c7bbc87dcf453d00
# Fri, 24 Jun 2022 03:08:54 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 24 Jun 2022 03:08:54 GMT
ENV MYSQL_JDBC_VERSION=8.0.29
# Fri, 24 Jun 2022 03:08:55 GMT
ENV MYSQL_JDBC_SHA256=d4e32d2a6026b5acc00300b73a86c28fb92681ae9629b21048ee67014c911db6
# Fri, 24 Jun 2022 03:08:55 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.29
# Fri, 24 Jun 2022 03:08:55 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.29.jar
# Fri, 24 Jun 2022 03:08:55 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.29.jar
# Fri, 24 Jun 2022 03:08:56 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 24 Jun 2022 03:08:56 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 24 Jun 2022 03:08:56 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 24 Jun 2022 03:08:56 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 24 Jun 2022 03:08:57 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 24 Jun 2022 03:08:57 GMT
VOLUME [/usr/local/xwiki]
# Fri, 24 Jun 2022 03:08:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jun 2022 03:08:57 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b669251e19038a24bd6cab0baab92077f23163880fac4701fb3efa564350732b`  
		Last Modified: Tue, 07 Jun 2022 00:21:34 GMT  
		Size: 43.3 MB (43267270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf45eff8a02bcdf7a96904e0dc534c78c89a5c860e224fa57780ef2fc2eab99e`  
		Last Modified: Tue, 07 Jun 2022 00:21:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246089a07769500a0adb027d1dc0efbb1254ee07d75dcdc6f8a3ceb8bae3e95f`  
		Last Modified: Tue, 07 Jun 2022 06:48:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3636fe8b4383f769da39b4c598b1e98b53b6d528e34e9d20fac5c17cfefcd866`  
		Last Modified: Fri, 10 Jun 2022 00:40:50 GMT  
		Size: 12.2 MB (12247499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0a0fd2a02961d2a1725c94d0c0f5670c51d5f5f9bad820a96e45791a5d7a32`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 445.5 KB (445476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beba28f927b0599e17785c8f69b8373e61c14da42247f7683f924f80ecae1439`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c54774971cb7c57e8fe14a42f90f7e4cceb67150ff2f3112f9ad46fea390190d`  
		Last Modified: Wed, 22 Jun 2022 04:30:07 GMT  
		Size: 167.5 MB (167492656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f8955940c07caf93c5b3787f4d50541ad84d1a6b710568178150ed29fa8c1fa`  
		Last Modified: Fri, 24 Jun 2022 03:11:53 GMT  
		Size: 292.6 MB (292641283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7511706ae08b48d6c19d83e802574606ae85b91839fd444ed4e26a21afa13cd`  
		Last Modified: Fri, 24 Jun 2022 03:11:35 GMT  
		Size: 2.4 MB (2381172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13635cdd2c775430a870517defaca7b40e34781684ba15c1c4bf4a47a22d7a9f`  
		Last Modified: Fri, 24 Jun 2022 03:11:35 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a6406d38ab58e4a678b831cfa2cf3dc65217dfc73299c135a3c2947cbf288b`  
		Last Modified: Fri, 24 Jun 2022 03:11:35 GMT  
		Size: 2.3 KB (2312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:112f72e7060631567b461a6b28b02795ad282cad23c101738ae01981635a0371`  
		Last Modified: Fri, 24 Jun 2022 03:11:35 GMT  
		Size: 5.3 KB (5338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c054adc9f3f529d9b827670e5c7c0878dd4b56f3f90e919891c04cd198e7bbb`  
		Last Modified: Fri, 24 Jun 2022 03:11:35 GMT  
		Size: 2.5 KB (2501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:13.10-mysql-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:8239f349f41eb1485f92190c846e889c7c6a069deef3e4810d62b3dca3b5cde9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **555.6 MB (555571284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d7ea8edd21d6b5820cbde3f17f19999ebce9e4ad1f0005dd187c3c77c3f8335`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:00:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:35:32 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 06:36:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:36:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:36:20 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 10:50:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 10:50:03 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 10:50:04 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 10:50:05 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 10:50:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:50:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:59:13 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 10:59:14 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 01:28:16 GMT
COPY dir:1fb0204bb532a7d63a0dd2d2677d66a70be0285454d27afba6780853636ba1ef in /usr/local/tomcat 
# Fri, 10 Jun 2022 01:28:22 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 01:28:24 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 01:28:25 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 01:28:26 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:24 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:25 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:09:26 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:09:27 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:10:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 24 Jun 2022 08:10:35 GMT
ENV XWIKI_VERSION=13.10.7
# Fri, 24 Jun 2022 08:10:35 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10.7
# Fri, 24 Jun 2022 08:10:36 GMT
ENV XWIKI_DOWNLOAD_SHA256=b886e886ed34e8d7bea8feb2e74e94edb3fb88030f90ab68c7bbc87dcf453d00
# Fri, 24 Jun 2022 08:11:07 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 24 Jun 2022 08:11:08 GMT
ENV MYSQL_JDBC_VERSION=8.0.29
# Fri, 24 Jun 2022 08:11:08 GMT
ENV MYSQL_JDBC_SHA256=d4e32d2a6026b5acc00300b73a86c28fb92681ae9629b21048ee67014c911db6
# Fri, 24 Jun 2022 08:11:09 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.29
# Fri, 24 Jun 2022 08:11:10 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.29.jar
# Fri, 24 Jun 2022 08:11:11 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.29.jar
# Fri, 24 Jun 2022 08:11:13 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 24 Jun 2022 08:11:14 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 24 Jun 2022 08:11:15 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 24 Jun 2022 08:11:16 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 24 Jun 2022 08:11:17 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 24 Jun 2022 08:11:17 GMT
VOLUME [/usr/local/xwiki]
# Fri, 24 Jun 2022 08:11:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jun 2022 08:11:19 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15da1b4c110f7cc460fbf968fb55b77c541f0e3ab87b92d5e6a822cc2c593e1`  
		Last Modified: Tue, 07 Jun 2022 05:10:23 GMT  
		Size: 15.9 MB (15898299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8e9d6a15d13e6f2d5d43f40b76051350cb7090cfcae5300dc1647e3196577a`  
		Last Modified: Tue, 07 Jun 2022 06:44:15 GMT  
		Size: 41.6 MB (41608356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51219ca7d003431d2f9c6ddda7db0a1902cf2b7e4e879625811b086f268b39c`  
		Last Modified: Tue, 07 Jun 2022 06:44:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5aa4900f44b9e3e20168d54fda3a0b78e62d572de1796db20345b70b1d8b3ca`  
		Last Modified: Tue, 07 Jun 2022 11:23:12 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6796806c88914990f15047665e74a4ea1fb933bdf7b8ebf39b1f2a82b723e044`  
		Last Modified: Fri, 10 Jun 2022 02:03:21 GMT  
		Size: 12.3 MB (12264791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca37469fc5a6ebbc5f1a764aabd4ba48b92a85d1396b644e1139994fad2fa34e`  
		Last Modified: Fri, 10 Jun 2022 02:03:20 GMT  
		Size: 208.8 KB (208841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c24501792b443d8ecb222b1c49c98ee84d4d76016bdbf8ba61b488fa873f7f`  
		Last Modified: Wed, 22 Jun 2022 04:17:01 GMT  
		Size: 163.4 MB (163365370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d4c4674e614cb6318120b7f3b95cc0f15a199054f449c2735cf25af9e2fd68`  
		Last Modified: Fri, 24 Jun 2022 08:14:37 GMT  
		Size: 292.6 MB (292641477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f45433cd06ad26dbb57afb98818c085a9ba114157cc72fa70214f8949e3ccfc`  
		Last Modified: Fri, 24 Jun 2022 08:14:15 GMT  
		Size: 2.4 MB (2381180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f75bf932706df5ca8d04fa02d8711685191f1f1dd7deb53937ba6f1371cb7fc5`  
		Last Modified: Fri, 24 Jun 2022 08:14:14 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04bce02a10640eb0a28ea0cd65126f65a6425540f18bd2acd881ed919828c057`  
		Last Modified: Fri, 24 Jun 2022 08:14:14 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:258f35d21774001fddc3b61192c74e053da90db66513a55c26d096b10ee59564`  
		Last Modified: Fri, 24 Jun 2022 08:14:14 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b877bc26e0f91fafb0bcbe8b609880d5c9cfba95b167970bae7650e06a31d706`  
		Last Modified: Fri, 24 Jun 2022 08:14:14 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13.10-postgres-tomcat`

```console
$ docker pull xwiki@sha256:b250edc19f4cc72d051ff836bc6a66dad2884231ad972b66018917572d37c35d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:13.10-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:638d7630646963b18a849058a847b7caab4ded28712b60b0d6d1900f56b0c537
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.3 MB (562304923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79cad287c34ddcfc1a8b8fa8c65cb34197ee741da2b4c8d387d6e0ad78009ec9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:14:23 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 00:14:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:58 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:59 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 06:30:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:30:41 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 06:30:41 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:30:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:35:57 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 06:35:58 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 00:18:07 GMT
COPY dir:360b17da945f7a5c4dcdc8b0602904442d98c06d17157280c607532ec8b6edaa in /usr/local/tomcat 
# Fri, 10 Jun 2022 00:18:12 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 00:18:13 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 00:18:13 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 00:18:13 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:26:27 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 24 Jun 2022 03:09:04 GMT
ENV XWIKI_VERSION=13.10.7
# Fri, 24 Jun 2022 03:09:04 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10.7
# Fri, 24 Jun 2022 03:09:05 GMT
ENV XWIKI_DOWNLOAD_SHA256=b886e886ed34e8d7bea8feb2e74e94edb3fb88030f90ab68c7bbc87dcf453d00
# Fri, 24 Jun 2022 03:10:26 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 24 Jun 2022 03:10:28 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 24 Jun 2022 03:10:28 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 24 Jun 2022 03:10:28 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 24 Jun 2022 03:10:29 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 24 Jun 2022 03:10:29 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 24 Jun 2022 03:10:29 GMT
VOLUME [/usr/local/xwiki]
# Fri, 24 Jun 2022 03:10:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jun 2022 03:10:29 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b669251e19038a24bd6cab0baab92077f23163880fac4701fb3efa564350732b`  
		Last Modified: Tue, 07 Jun 2022 00:21:34 GMT  
		Size: 43.3 MB (43267270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf45eff8a02bcdf7a96904e0dc534c78c89a5c860e224fa57780ef2fc2eab99e`  
		Last Modified: Tue, 07 Jun 2022 00:21:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246089a07769500a0adb027d1dc0efbb1254ee07d75dcdc6f8a3ceb8bae3e95f`  
		Last Modified: Tue, 07 Jun 2022 06:48:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3636fe8b4383f769da39b4c598b1e98b53b6d528e34e9d20fac5c17cfefcd866`  
		Last Modified: Fri, 10 Jun 2022 00:40:50 GMT  
		Size: 12.2 MB (12247499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0a0fd2a02961d2a1725c94d0c0f5670c51d5f5f9bad820a96e45791a5d7a32`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 445.5 KB (445476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beba28f927b0599e17785c8f69b8373e61c14da42247f7683f924f80ecae1439`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:657eec0a2bb289006e136ad46dbd1d85e8ff10712e1477c0fcacb617a19bb242`  
		Last Modified: Wed, 22 Jun 2022 04:31:12 GMT  
		Size: 168.3 MB (168293438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:136be306a609540683e370b2425b4d3703542a79224441c6337af82ee1698ca2`  
		Last Modified: Fri, 24 Jun 2022 03:12:46 GMT  
		Size: 292.6 MB (292641286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3769fbd23a38bb2c2737d30cd4a790f8ad775a99a63e6591de2df21d750f52`  
		Last Modified: Fri, 24 Jun 2022 03:12:29 GMT  
		Size: 795.4 KB (795424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:155517bc4fff02081a754dd1ac5674da90d74db9792a871f64983196cbd2b573`  
		Last Modified: Fri, 24 Jun 2022 03:12:28 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e9d584cf5548a2a612999b7b8fb340c4a38d8e9b31fd9ab73ca09cb173eb0f`  
		Last Modified: Fri, 24 Jun 2022 03:12:28 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2330650c98390edb3e1e7bd4d667c7b4e344da794f180c208aa1c92872db10cc`  
		Last Modified: Fri, 24 Jun 2022 03:12:29 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9458af98469686b7341e974f7343a72938ca0fa6984c887bb8d0a160375881ee`  
		Last Modified: Fri, 24 Jun 2022 03:12:29 GMT  
		Size: 2.5 KB (2503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:13.10-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:bb8443f4c39a1e5e1eaa389c87f32b928bccad2f727705a2e02afcc1b98ac2bf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.8 MB (554784337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99d205394842fb0b6709b682ff9d39e01d0ade2e25f08c11c4c8c766f9ccd182`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:00:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:35:32 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 06:36:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:36:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:36:20 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 10:50:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 10:50:03 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 10:50:04 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 10:50:05 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 10:50:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:50:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:59:13 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 10:59:14 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 01:28:16 GMT
COPY dir:1fb0204bb532a7d63a0dd2d2677d66a70be0285454d27afba6780853636ba1ef in /usr/local/tomcat 
# Fri, 10 Jun 2022 01:28:22 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 01:28:24 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 01:28:25 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 01:28:26 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:24 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:25 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:09:26 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:09:27 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:11:42 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 24 Jun 2022 08:11:28 GMT
ENV XWIKI_VERSION=13.10.7
# Fri, 24 Jun 2022 08:11:29 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10.7
# Fri, 24 Jun 2022 08:11:30 GMT
ENV XWIKI_DOWNLOAD_SHA256=b886e886ed34e8d7bea8feb2e74e94edb3fb88030f90ab68c7bbc87dcf453d00
# Fri, 24 Jun 2022 08:12:12 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 24 Jun 2022 08:12:13 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 24 Jun 2022 08:12:14 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 24 Jun 2022 08:12:15 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 24 Jun 2022 08:12:16 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 24 Jun 2022 08:12:17 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 24 Jun 2022 08:12:17 GMT
VOLUME [/usr/local/xwiki]
# Fri, 24 Jun 2022 08:12:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jun 2022 08:12:19 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15da1b4c110f7cc460fbf968fb55b77c541f0e3ab87b92d5e6a822cc2c593e1`  
		Last Modified: Tue, 07 Jun 2022 05:10:23 GMT  
		Size: 15.9 MB (15898299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8e9d6a15d13e6f2d5d43f40b76051350cb7090cfcae5300dc1647e3196577a`  
		Last Modified: Tue, 07 Jun 2022 06:44:15 GMT  
		Size: 41.6 MB (41608356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51219ca7d003431d2f9c6ddda7db0a1902cf2b7e4e879625811b086f268b39c`  
		Last Modified: Tue, 07 Jun 2022 06:44:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5aa4900f44b9e3e20168d54fda3a0b78e62d572de1796db20345b70b1d8b3ca`  
		Last Modified: Tue, 07 Jun 2022 11:23:12 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6796806c88914990f15047665e74a4ea1fb933bdf7b8ebf39b1f2a82b723e044`  
		Last Modified: Fri, 10 Jun 2022 02:03:21 GMT  
		Size: 12.3 MB (12264791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca37469fc5a6ebbc5f1a764aabd4ba48b92a85d1396b644e1139994fad2fa34e`  
		Last Modified: Fri, 10 Jun 2022 02:03:20 GMT  
		Size: 208.8 KB (208841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbf4753a12af2d02fd26a953119f6843f7e381cfec0d679d92b04b4e4f5a3d6a`  
		Last Modified: Wed, 22 Jun 2022 04:18:08 GMT  
		Size: 164.2 MB (164164156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acdad91995b0da375c92d6651576276e78123cfbb080e5444a094fc5033c930c`  
		Last Modified: Fri, 24 Jun 2022 08:15:36 GMT  
		Size: 292.6 MB (292641359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:350ecfd793c7e54308d1c7a22f36e2e098e8fdae31cecb75339bfa7f0a8b7af6`  
		Last Modified: Fri, 24 Jun 2022 08:15:14 GMT  
		Size: 795.4 KB (795417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c27ddaa528e0298945c5eca4aa5235bd761f13f40e2b35de068a7977434e571d`  
		Last Modified: Fri, 24 Jun 2022 08:15:14 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9edb1eb483f19a886fd0fcf80dc5c21e5ef36163eb1e8df94a3b80f508fbeff8`  
		Last Modified: Fri, 24 Jun 2022 08:15:14 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d9ff4c9416279f5b0a9e42bf517e29f15992d0a7a0c5d3361f7fbc8472c12d`  
		Last Modified: Fri, 24 Jun 2022 08:15:14 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be06063b865aaeadaa012c84711685856110099c19fa07ac1af19e12fa08cce`  
		Last Modified: Fri, 24 Jun 2022 08:15:14 GMT  
		Size: 2.5 KB (2507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13.10.7`

```console
$ docker pull xwiki@sha256:538c472ff45f7c146d4cfbf1e7b31fb39f111a3d49287f502a6d2f71777ff333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:13.10.7` - linux; amd64

```console
$ docker pull xwiki@sha256:d6bbb60b487ca00096f55242a245f5d8021e42013dc9a65227548a78a0e39f38
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.1 MB (563089744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce3a4cc5ca40c56b140b6c3abe277f24fb0842adc6ec43651543be6f4ba1e449`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:14:23 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 00:14:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:58 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:59 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 06:30:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:30:41 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 06:30:41 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:30:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:35:57 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 06:35:58 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 00:18:07 GMT
COPY dir:360b17da945f7a5c4dcdc8b0602904442d98c06d17157280c607532ec8b6edaa in /usr/local/tomcat 
# Fri, 10 Jun 2022 00:18:12 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 00:18:13 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 00:18:13 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 00:18:13 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:25:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 24 Jun 2022 03:08:16 GMT
ENV XWIKI_VERSION=13.10.7
# Fri, 24 Jun 2022 03:08:16 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10.7
# Fri, 24 Jun 2022 03:08:16 GMT
ENV XWIKI_DOWNLOAD_SHA256=b886e886ed34e8d7bea8feb2e74e94edb3fb88030f90ab68c7bbc87dcf453d00
# Fri, 24 Jun 2022 03:08:54 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 24 Jun 2022 03:08:54 GMT
ENV MYSQL_JDBC_VERSION=8.0.29
# Fri, 24 Jun 2022 03:08:55 GMT
ENV MYSQL_JDBC_SHA256=d4e32d2a6026b5acc00300b73a86c28fb92681ae9629b21048ee67014c911db6
# Fri, 24 Jun 2022 03:08:55 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.29
# Fri, 24 Jun 2022 03:08:55 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.29.jar
# Fri, 24 Jun 2022 03:08:55 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.29.jar
# Fri, 24 Jun 2022 03:08:56 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 24 Jun 2022 03:08:56 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 24 Jun 2022 03:08:56 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 24 Jun 2022 03:08:56 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 24 Jun 2022 03:08:57 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 24 Jun 2022 03:08:57 GMT
VOLUME [/usr/local/xwiki]
# Fri, 24 Jun 2022 03:08:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jun 2022 03:08:57 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b669251e19038a24bd6cab0baab92077f23163880fac4701fb3efa564350732b`  
		Last Modified: Tue, 07 Jun 2022 00:21:34 GMT  
		Size: 43.3 MB (43267270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf45eff8a02bcdf7a96904e0dc534c78c89a5c860e224fa57780ef2fc2eab99e`  
		Last Modified: Tue, 07 Jun 2022 00:21:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246089a07769500a0adb027d1dc0efbb1254ee07d75dcdc6f8a3ceb8bae3e95f`  
		Last Modified: Tue, 07 Jun 2022 06:48:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3636fe8b4383f769da39b4c598b1e98b53b6d528e34e9d20fac5c17cfefcd866`  
		Last Modified: Fri, 10 Jun 2022 00:40:50 GMT  
		Size: 12.2 MB (12247499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0a0fd2a02961d2a1725c94d0c0f5670c51d5f5f9bad820a96e45791a5d7a32`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 445.5 KB (445476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beba28f927b0599e17785c8f69b8373e61c14da42247f7683f924f80ecae1439`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c54774971cb7c57e8fe14a42f90f7e4cceb67150ff2f3112f9ad46fea390190d`  
		Last Modified: Wed, 22 Jun 2022 04:30:07 GMT  
		Size: 167.5 MB (167492656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f8955940c07caf93c5b3787f4d50541ad84d1a6b710568178150ed29fa8c1fa`  
		Last Modified: Fri, 24 Jun 2022 03:11:53 GMT  
		Size: 292.6 MB (292641283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7511706ae08b48d6c19d83e802574606ae85b91839fd444ed4e26a21afa13cd`  
		Last Modified: Fri, 24 Jun 2022 03:11:35 GMT  
		Size: 2.4 MB (2381172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13635cdd2c775430a870517defaca7b40e34781684ba15c1c4bf4a47a22d7a9f`  
		Last Modified: Fri, 24 Jun 2022 03:11:35 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a6406d38ab58e4a678b831cfa2cf3dc65217dfc73299c135a3c2947cbf288b`  
		Last Modified: Fri, 24 Jun 2022 03:11:35 GMT  
		Size: 2.3 KB (2312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:112f72e7060631567b461a6b28b02795ad282cad23c101738ae01981635a0371`  
		Last Modified: Fri, 24 Jun 2022 03:11:35 GMT  
		Size: 5.3 KB (5338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c054adc9f3f529d9b827670e5c7c0878dd4b56f3f90e919891c04cd198e7bbb`  
		Last Modified: Fri, 24 Jun 2022 03:11:35 GMT  
		Size: 2.5 KB (2501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:13.10.7` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:8239f349f41eb1485f92190c846e889c7c6a069deef3e4810d62b3dca3b5cde9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **555.6 MB (555571284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d7ea8edd21d6b5820cbde3f17f19999ebce9e4ad1f0005dd187c3c77c3f8335`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:00:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:35:32 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 06:36:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:36:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:36:20 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 10:50:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 10:50:03 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 10:50:04 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 10:50:05 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 10:50:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:50:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:59:13 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 10:59:14 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 01:28:16 GMT
COPY dir:1fb0204bb532a7d63a0dd2d2677d66a70be0285454d27afba6780853636ba1ef in /usr/local/tomcat 
# Fri, 10 Jun 2022 01:28:22 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 01:28:24 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 01:28:25 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 01:28:26 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:24 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:25 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:09:26 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:09:27 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:10:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 24 Jun 2022 08:10:35 GMT
ENV XWIKI_VERSION=13.10.7
# Fri, 24 Jun 2022 08:10:35 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10.7
# Fri, 24 Jun 2022 08:10:36 GMT
ENV XWIKI_DOWNLOAD_SHA256=b886e886ed34e8d7bea8feb2e74e94edb3fb88030f90ab68c7bbc87dcf453d00
# Fri, 24 Jun 2022 08:11:07 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 24 Jun 2022 08:11:08 GMT
ENV MYSQL_JDBC_VERSION=8.0.29
# Fri, 24 Jun 2022 08:11:08 GMT
ENV MYSQL_JDBC_SHA256=d4e32d2a6026b5acc00300b73a86c28fb92681ae9629b21048ee67014c911db6
# Fri, 24 Jun 2022 08:11:09 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.29
# Fri, 24 Jun 2022 08:11:10 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.29.jar
# Fri, 24 Jun 2022 08:11:11 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.29.jar
# Fri, 24 Jun 2022 08:11:13 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 24 Jun 2022 08:11:14 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 24 Jun 2022 08:11:15 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 24 Jun 2022 08:11:16 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 24 Jun 2022 08:11:17 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 24 Jun 2022 08:11:17 GMT
VOLUME [/usr/local/xwiki]
# Fri, 24 Jun 2022 08:11:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jun 2022 08:11:19 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15da1b4c110f7cc460fbf968fb55b77c541f0e3ab87b92d5e6a822cc2c593e1`  
		Last Modified: Tue, 07 Jun 2022 05:10:23 GMT  
		Size: 15.9 MB (15898299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8e9d6a15d13e6f2d5d43f40b76051350cb7090cfcae5300dc1647e3196577a`  
		Last Modified: Tue, 07 Jun 2022 06:44:15 GMT  
		Size: 41.6 MB (41608356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51219ca7d003431d2f9c6ddda7db0a1902cf2b7e4e879625811b086f268b39c`  
		Last Modified: Tue, 07 Jun 2022 06:44:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5aa4900f44b9e3e20168d54fda3a0b78e62d572de1796db20345b70b1d8b3ca`  
		Last Modified: Tue, 07 Jun 2022 11:23:12 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6796806c88914990f15047665e74a4ea1fb933bdf7b8ebf39b1f2a82b723e044`  
		Last Modified: Fri, 10 Jun 2022 02:03:21 GMT  
		Size: 12.3 MB (12264791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca37469fc5a6ebbc5f1a764aabd4ba48b92a85d1396b644e1139994fad2fa34e`  
		Last Modified: Fri, 10 Jun 2022 02:03:20 GMT  
		Size: 208.8 KB (208841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c24501792b443d8ecb222b1c49c98ee84d4d76016bdbf8ba61b488fa873f7f`  
		Last Modified: Wed, 22 Jun 2022 04:17:01 GMT  
		Size: 163.4 MB (163365370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d4c4674e614cb6318120b7f3b95cc0f15a199054f449c2735cf25af9e2fd68`  
		Last Modified: Fri, 24 Jun 2022 08:14:37 GMT  
		Size: 292.6 MB (292641477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f45433cd06ad26dbb57afb98818c085a9ba114157cc72fa70214f8949e3ccfc`  
		Last Modified: Fri, 24 Jun 2022 08:14:15 GMT  
		Size: 2.4 MB (2381180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f75bf932706df5ca8d04fa02d8711685191f1f1dd7deb53937ba6f1371cb7fc5`  
		Last Modified: Fri, 24 Jun 2022 08:14:14 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04bce02a10640eb0a28ea0cd65126f65a6425540f18bd2acd881ed919828c057`  
		Last Modified: Fri, 24 Jun 2022 08:14:14 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:258f35d21774001fddc3b61192c74e053da90db66513a55c26d096b10ee59564`  
		Last Modified: Fri, 24 Jun 2022 08:14:14 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b877bc26e0f91fafb0bcbe8b609880d5c9cfba95b167970bae7650e06a31d706`  
		Last Modified: Fri, 24 Jun 2022 08:14:14 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13.10.7-mariadb-tomcat`

```console
$ docker pull xwiki@sha256:7e992a39803f1553703a95e1c243d3e530a70c492c48ce9f4721f3c0cac22740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:13.10.7-mariadb-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:fe68d60e91e8d3eb0e5d23a11eb5b888b7350043a1edc71fd12266ce62957ac7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **561.2 MB (561248650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c580180cdf614c4e58b233442d12859c0c06fb61a5c351ff96835ef123570549`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:14:23 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 00:14:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:58 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:59 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 06:30:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:30:41 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 06:30:41 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:30:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:35:57 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 06:35:58 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 00:18:07 GMT
COPY dir:360b17da945f7a5c4dcdc8b0602904442d98c06d17157280c607532ec8b6edaa in /usr/local/tomcat 
# Fri, 10 Jun 2022 00:18:12 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 00:18:13 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 00:18:13 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 00:18:13 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:25:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 24 Jun 2022 03:08:16 GMT
ENV XWIKI_VERSION=13.10.7
# Fri, 24 Jun 2022 03:08:16 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10.7
# Fri, 24 Jun 2022 03:08:16 GMT
ENV XWIKI_DOWNLOAD_SHA256=b886e886ed34e8d7bea8feb2e74e94edb3fb88030f90ab68c7bbc87dcf453d00
# Fri, 24 Jun 2022 03:08:54 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 24 Jun 2022 03:10:42 GMT
ENV MARIADB_JDBC_VERSION=3.0.5
# Fri, 24 Jun 2022 03:10:42 GMT
ENV MARIADB_JDBC_SHA256=e9532d9bca07c1263c32b00b495bd3ec7f2b79320513cabd762bf39ea09e68d9
# Fri, 24 Jun 2022 03:10:43 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.0.5
# Fri, 24 Jun 2022 03:10:43 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.0.5.jar
# Fri, 24 Jun 2022 03:10:43 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.0.5.jar
# Fri, 24 Jun 2022 03:10:43 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Fri, 24 Jun 2022 03:10:44 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 24 Jun 2022 03:10:44 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 24 Jun 2022 03:10:44 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 24 Jun 2022 03:10:44 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 24 Jun 2022 03:10:44 GMT
VOLUME [/usr/local/xwiki]
# Fri, 24 Jun 2022 03:10:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jun 2022 03:10:45 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b669251e19038a24bd6cab0baab92077f23163880fac4701fb3efa564350732b`  
		Last Modified: Tue, 07 Jun 2022 00:21:34 GMT  
		Size: 43.3 MB (43267270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf45eff8a02bcdf7a96904e0dc534c78c89a5c860e224fa57780ef2fc2eab99e`  
		Last Modified: Tue, 07 Jun 2022 00:21:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246089a07769500a0adb027d1dc0efbb1254ee07d75dcdc6f8a3ceb8bae3e95f`  
		Last Modified: Tue, 07 Jun 2022 06:48:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3636fe8b4383f769da39b4c598b1e98b53b6d528e34e9d20fac5c17cfefcd866`  
		Last Modified: Fri, 10 Jun 2022 00:40:50 GMT  
		Size: 12.2 MB (12247499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0a0fd2a02961d2a1725c94d0c0f5670c51d5f5f9bad820a96e45791a5d7a32`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 445.5 KB (445476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beba28f927b0599e17785c8f69b8373e61c14da42247f7683f924f80ecae1439`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c54774971cb7c57e8fe14a42f90f7e4cceb67150ff2f3112f9ad46fea390190d`  
		Last Modified: Wed, 22 Jun 2022 04:30:07 GMT  
		Size: 167.5 MB (167492656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f8955940c07caf93c5b3787f4d50541ad84d1a6b710568178150ed29fa8c1fa`  
		Last Modified: Fri, 24 Jun 2022 03:11:53 GMT  
		Size: 292.6 MB (292641283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39e75aa0ee70148e023225e5c15afe6370fae11ad20051cbdc9ad36c048410cb`  
		Last Modified: Fri, 24 Jun 2022 03:13:09 GMT  
		Size: 540.1 KB (540074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a78e618b05c2bd943951d754b0495482861f717b916017efa2d775bd91113d07`  
		Last Modified: Fri, 24 Jun 2022 03:13:08 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77f7e7cac8551052ca6034a6b13460c7245751fa15ed047622af1e3a4bdf80e0`  
		Last Modified: Fri, 24 Jun 2022 03:13:08 GMT  
		Size: 2.3 KB (2313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ac5252f40483fbc8e8acc62ff8428fe4b47a3a203ef6412edda8b83a0bfea19`  
		Last Modified: Fri, 24 Jun 2022 03:13:08 GMT  
		Size: 5.3 KB (5339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea840c472b11a8abe56d67979ba671ee677a5046199e8f29afff0c3f9b6871a`  
		Last Modified: Fri, 24 Jun 2022 03:13:08 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:13.10.7-mariadb-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:f69b33053370bb439577df2ccf0307fb2b1e92e7ad2e3000e27165d0508ce769
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **553.7 MB (553730176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77e99996ea02f728cd4df08569f2a56128eb95625ce333da516f87ca24dfb42d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:00:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:35:32 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 06:36:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:36:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:36:20 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 10:50:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 10:50:03 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 10:50:04 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 10:50:05 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 10:50:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:50:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:59:13 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 10:59:14 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 01:28:16 GMT
COPY dir:1fb0204bb532a7d63a0dd2d2677d66a70be0285454d27afba6780853636ba1ef in /usr/local/tomcat 
# Fri, 10 Jun 2022 01:28:22 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 01:28:24 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 01:28:25 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 01:28:26 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:24 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:25 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:09:26 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:09:27 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:10:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 24 Jun 2022 08:10:35 GMT
ENV XWIKI_VERSION=13.10.7
# Fri, 24 Jun 2022 08:10:35 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10.7
# Fri, 24 Jun 2022 08:10:36 GMT
ENV XWIKI_DOWNLOAD_SHA256=b886e886ed34e8d7bea8feb2e74e94edb3fb88030f90ab68c7bbc87dcf453d00
# Fri, 24 Jun 2022 08:11:07 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 24 Jun 2022 08:12:29 GMT
ENV MARIADB_JDBC_VERSION=3.0.5
# Fri, 24 Jun 2022 08:12:30 GMT
ENV MARIADB_JDBC_SHA256=e9532d9bca07c1263c32b00b495bd3ec7f2b79320513cabd762bf39ea09e68d9
# Fri, 24 Jun 2022 08:12:31 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.0.5
# Fri, 24 Jun 2022 08:12:32 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.0.5.jar
# Fri, 24 Jun 2022 08:12:33 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.0.5.jar
# Fri, 24 Jun 2022 08:12:35 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Fri, 24 Jun 2022 08:12:36 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 24 Jun 2022 08:12:37 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 24 Jun 2022 08:12:38 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 24 Jun 2022 08:12:39 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 24 Jun 2022 08:12:39 GMT
VOLUME [/usr/local/xwiki]
# Fri, 24 Jun 2022 08:12:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jun 2022 08:12:41 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15da1b4c110f7cc460fbf968fb55b77c541f0e3ab87b92d5e6a822cc2c593e1`  
		Last Modified: Tue, 07 Jun 2022 05:10:23 GMT  
		Size: 15.9 MB (15898299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8e9d6a15d13e6f2d5d43f40b76051350cb7090cfcae5300dc1647e3196577a`  
		Last Modified: Tue, 07 Jun 2022 06:44:15 GMT  
		Size: 41.6 MB (41608356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51219ca7d003431d2f9c6ddda7db0a1902cf2b7e4e879625811b086f268b39c`  
		Last Modified: Tue, 07 Jun 2022 06:44:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5aa4900f44b9e3e20168d54fda3a0b78e62d572de1796db20345b70b1d8b3ca`  
		Last Modified: Tue, 07 Jun 2022 11:23:12 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6796806c88914990f15047665e74a4ea1fb933bdf7b8ebf39b1f2a82b723e044`  
		Last Modified: Fri, 10 Jun 2022 02:03:21 GMT  
		Size: 12.3 MB (12264791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca37469fc5a6ebbc5f1a764aabd4ba48b92a85d1396b644e1139994fad2fa34e`  
		Last Modified: Fri, 10 Jun 2022 02:03:20 GMT  
		Size: 208.8 KB (208841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c24501792b443d8ecb222b1c49c98ee84d4d76016bdbf8ba61b488fa873f7f`  
		Last Modified: Wed, 22 Jun 2022 04:17:01 GMT  
		Size: 163.4 MB (163365370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d4c4674e614cb6318120b7f3b95cc0f15a199054f449c2735cf25af9e2fd68`  
		Last Modified: Fri, 24 Jun 2022 08:14:37 GMT  
		Size: 292.6 MB (292641477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55eb49c20075c8f6f6c3474817337eac98d5ecd1d220ca225ede5b5d516ea478`  
		Last Modified: Fri, 24 Jun 2022 08:15:59 GMT  
		Size: 540.1 KB (540068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52ab0fc86a347634df62c569c68f1d90c68af8888bfd6761815c0dc42be1d9e3`  
		Last Modified: Fri, 24 Jun 2022 08:15:58 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:905cc4a353cba057e2dd9dd80f2a18dab3caf4cd39fc0fe50c6e5963c5ea3e55`  
		Last Modified: Fri, 24 Jun 2022 08:15:58 GMT  
		Size: 2.3 KB (2310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7cc5bcac189f250a4bf9f37357b4a4cadc7fc132044e958bcd14c24d26736ec`  
		Last Modified: Fri, 24 Jun 2022 08:15:58 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743fadc0e05f56a8caa0b29a7c3b8fddddca135a6fce4bd23eab3167966f8e5d`  
		Last Modified: Fri, 24 Jun 2022 08:15:58 GMT  
		Size: 2.5 KB (2507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13.10.7-mysql-tomcat`

```console
$ docker pull xwiki@sha256:538c472ff45f7c146d4cfbf1e7b31fb39f111a3d49287f502a6d2f71777ff333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:13.10.7-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:d6bbb60b487ca00096f55242a245f5d8021e42013dc9a65227548a78a0e39f38
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.1 MB (563089744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce3a4cc5ca40c56b140b6c3abe277f24fb0842adc6ec43651543be6f4ba1e449`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:14:23 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 00:14:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:58 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:59 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 06:30:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:30:41 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 06:30:41 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:30:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:35:57 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 06:35:58 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 00:18:07 GMT
COPY dir:360b17da945f7a5c4dcdc8b0602904442d98c06d17157280c607532ec8b6edaa in /usr/local/tomcat 
# Fri, 10 Jun 2022 00:18:12 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 00:18:13 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 00:18:13 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 00:18:13 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:25:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 24 Jun 2022 03:08:16 GMT
ENV XWIKI_VERSION=13.10.7
# Fri, 24 Jun 2022 03:08:16 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10.7
# Fri, 24 Jun 2022 03:08:16 GMT
ENV XWIKI_DOWNLOAD_SHA256=b886e886ed34e8d7bea8feb2e74e94edb3fb88030f90ab68c7bbc87dcf453d00
# Fri, 24 Jun 2022 03:08:54 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 24 Jun 2022 03:08:54 GMT
ENV MYSQL_JDBC_VERSION=8.0.29
# Fri, 24 Jun 2022 03:08:55 GMT
ENV MYSQL_JDBC_SHA256=d4e32d2a6026b5acc00300b73a86c28fb92681ae9629b21048ee67014c911db6
# Fri, 24 Jun 2022 03:08:55 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.29
# Fri, 24 Jun 2022 03:08:55 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.29.jar
# Fri, 24 Jun 2022 03:08:55 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.29.jar
# Fri, 24 Jun 2022 03:08:56 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 24 Jun 2022 03:08:56 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 24 Jun 2022 03:08:56 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 24 Jun 2022 03:08:56 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 24 Jun 2022 03:08:57 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 24 Jun 2022 03:08:57 GMT
VOLUME [/usr/local/xwiki]
# Fri, 24 Jun 2022 03:08:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jun 2022 03:08:57 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b669251e19038a24bd6cab0baab92077f23163880fac4701fb3efa564350732b`  
		Last Modified: Tue, 07 Jun 2022 00:21:34 GMT  
		Size: 43.3 MB (43267270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf45eff8a02bcdf7a96904e0dc534c78c89a5c860e224fa57780ef2fc2eab99e`  
		Last Modified: Tue, 07 Jun 2022 00:21:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246089a07769500a0adb027d1dc0efbb1254ee07d75dcdc6f8a3ceb8bae3e95f`  
		Last Modified: Tue, 07 Jun 2022 06:48:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3636fe8b4383f769da39b4c598b1e98b53b6d528e34e9d20fac5c17cfefcd866`  
		Last Modified: Fri, 10 Jun 2022 00:40:50 GMT  
		Size: 12.2 MB (12247499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0a0fd2a02961d2a1725c94d0c0f5670c51d5f5f9bad820a96e45791a5d7a32`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 445.5 KB (445476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beba28f927b0599e17785c8f69b8373e61c14da42247f7683f924f80ecae1439`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c54774971cb7c57e8fe14a42f90f7e4cceb67150ff2f3112f9ad46fea390190d`  
		Last Modified: Wed, 22 Jun 2022 04:30:07 GMT  
		Size: 167.5 MB (167492656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f8955940c07caf93c5b3787f4d50541ad84d1a6b710568178150ed29fa8c1fa`  
		Last Modified: Fri, 24 Jun 2022 03:11:53 GMT  
		Size: 292.6 MB (292641283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7511706ae08b48d6c19d83e802574606ae85b91839fd444ed4e26a21afa13cd`  
		Last Modified: Fri, 24 Jun 2022 03:11:35 GMT  
		Size: 2.4 MB (2381172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13635cdd2c775430a870517defaca7b40e34781684ba15c1c4bf4a47a22d7a9f`  
		Last Modified: Fri, 24 Jun 2022 03:11:35 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a6406d38ab58e4a678b831cfa2cf3dc65217dfc73299c135a3c2947cbf288b`  
		Last Modified: Fri, 24 Jun 2022 03:11:35 GMT  
		Size: 2.3 KB (2312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:112f72e7060631567b461a6b28b02795ad282cad23c101738ae01981635a0371`  
		Last Modified: Fri, 24 Jun 2022 03:11:35 GMT  
		Size: 5.3 KB (5338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c054adc9f3f529d9b827670e5c7c0878dd4b56f3f90e919891c04cd198e7bbb`  
		Last Modified: Fri, 24 Jun 2022 03:11:35 GMT  
		Size: 2.5 KB (2501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:13.10.7-mysql-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:8239f349f41eb1485f92190c846e889c7c6a069deef3e4810d62b3dca3b5cde9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **555.6 MB (555571284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d7ea8edd21d6b5820cbde3f17f19999ebce9e4ad1f0005dd187c3c77c3f8335`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:00:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:35:32 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 06:36:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:36:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:36:20 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 10:50:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 10:50:03 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 10:50:04 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 10:50:05 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 10:50:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:50:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:59:13 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 10:59:14 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 01:28:16 GMT
COPY dir:1fb0204bb532a7d63a0dd2d2677d66a70be0285454d27afba6780853636ba1ef in /usr/local/tomcat 
# Fri, 10 Jun 2022 01:28:22 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 01:28:24 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 01:28:25 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 01:28:26 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:24 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:25 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:09:26 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:09:27 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:10:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 24 Jun 2022 08:10:35 GMT
ENV XWIKI_VERSION=13.10.7
# Fri, 24 Jun 2022 08:10:35 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10.7
# Fri, 24 Jun 2022 08:10:36 GMT
ENV XWIKI_DOWNLOAD_SHA256=b886e886ed34e8d7bea8feb2e74e94edb3fb88030f90ab68c7bbc87dcf453d00
# Fri, 24 Jun 2022 08:11:07 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 24 Jun 2022 08:11:08 GMT
ENV MYSQL_JDBC_VERSION=8.0.29
# Fri, 24 Jun 2022 08:11:08 GMT
ENV MYSQL_JDBC_SHA256=d4e32d2a6026b5acc00300b73a86c28fb92681ae9629b21048ee67014c911db6
# Fri, 24 Jun 2022 08:11:09 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.29
# Fri, 24 Jun 2022 08:11:10 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.29.jar
# Fri, 24 Jun 2022 08:11:11 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.29.jar
# Fri, 24 Jun 2022 08:11:13 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 24 Jun 2022 08:11:14 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 24 Jun 2022 08:11:15 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 24 Jun 2022 08:11:16 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 24 Jun 2022 08:11:17 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 24 Jun 2022 08:11:17 GMT
VOLUME [/usr/local/xwiki]
# Fri, 24 Jun 2022 08:11:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jun 2022 08:11:19 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15da1b4c110f7cc460fbf968fb55b77c541f0e3ab87b92d5e6a822cc2c593e1`  
		Last Modified: Tue, 07 Jun 2022 05:10:23 GMT  
		Size: 15.9 MB (15898299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8e9d6a15d13e6f2d5d43f40b76051350cb7090cfcae5300dc1647e3196577a`  
		Last Modified: Tue, 07 Jun 2022 06:44:15 GMT  
		Size: 41.6 MB (41608356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51219ca7d003431d2f9c6ddda7db0a1902cf2b7e4e879625811b086f268b39c`  
		Last Modified: Tue, 07 Jun 2022 06:44:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5aa4900f44b9e3e20168d54fda3a0b78e62d572de1796db20345b70b1d8b3ca`  
		Last Modified: Tue, 07 Jun 2022 11:23:12 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6796806c88914990f15047665e74a4ea1fb933bdf7b8ebf39b1f2a82b723e044`  
		Last Modified: Fri, 10 Jun 2022 02:03:21 GMT  
		Size: 12.3 MB (12264791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca37469fc5a6ebbc5f1a764aabd4ba48b92a85d1396b644e1139994fad2fa34e`  
		Last Modified: Fri, 10 Jun 2022 02:03:20 GMT  
		Size: 208.8 KB (208841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c24501792b443d8ecb222b1c49c98ee84d4d76016bdbf8ba61b488fa873f7f`  
		Last Modified: Wed, 22 Jun 2022 04:17:01 GMT  
		Size: 163.4 MB (163365370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d4c4674e614cb6318120b7f3b95cc0f15a199054f449c2735cf25af9e2fd68`  
		Last Modified: Fri, 24 Jun 2022 08:14:37 GMT  
		Size: 292.6 MB (292641477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f45433cd06ad26dbb57afb98818c085a9ba114157cc72fa70214f8949e3ccfc`  
		Last Modified: Fri, 24 Jun 2022 08:14:15 GMT  
		Size: 2.4 MB (2381180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f75bf932706df5ca8d04fa02d8711685191f1f1dd7deb53937ba6f1371cb7fc5`  
		Last Modified: Fri, 24 Jun 2022 08:14:14 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04bce02a10640eb0a28ea0cd65126f65a6425540f18bd2acd881ed919828c057`  
		Last Modified: Fri, 24 Jun 2022 08:14:14 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:258f35d21774001fddc3b61192c74e053da90db66513a55c26d096b10ee59564`  
		Last Modified: Fri, 24 Jun 2022 08:14:14 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b877bc26e0f91fafb0bcbe8b609880d5c9cfba95b167970bae7650e06a31d706`  
		Last Modified: Fri, 24 Jun 2022 08:14:14 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13.10.7-postgres-tomcat`

```console
$ docker pull xwiki@sha256:b250edc19f4cc72d051ff836bc6a66dad2884231ad972b66018917572d37c35d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:13.10.7-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:638d7630646963b18a849058a847b7caab4ded28712b60b0d6d1900f56b0c537
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.3 MB (562304923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79cad287c34ddcfc1a8b8fa8c65cb34197ee741da2b4c8d387d6e0ad78009ec9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:14:23 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 00:14:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:58 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:59 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 06:30:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:30:41 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 06:30:41 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:30:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:35:57 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 06:35:58 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 00:18:07 GMT
COPY dir:360b17da945f7a5c4dcdc8b0602904442d98c06d17157280c607532ec8b6edaa in /usr/local/tomcat 
# Fri, 10 Jun 2022 00:18:12 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 00:18:13 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 00:18:13 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 00:18:13 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:26:27 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 24 Jun 2022 03:09:04 GMT
ENV XWIKI_VERSION=13.10.7
# Fri, 24 Jun 2022 03:09:04 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10.7
# Fri, 24 Jun 2022 03:09:05 GMT
ENV XWIKI_DOWNLOAD_SHA256=b886e886ed34e8d7bea8feb2e74e94edb3fb88030f90ab68c7bbc87dcf453d00
# Fri, 24 Jun 2022 03:10:26 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 24 Jun 2022 03:10:28 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 24 Jun 2022 03:10:28 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 24 Jun 2022 03:10:28 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 24 Jun 2022 03:10:29 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 24 Jun 2022 03:10:29 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 24 Jun 2022 03:10:29 GMT
VOLUME [/usr/local/xwiki]
# Fri, 24 Jun 2022 03:10:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jun 2022 03:10:29 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b669251e19038a24bd6cab0baab92077f23163880fac4701fb3efa564350732b`  
		Last Modified: Tue, 07 Jun 2022 00:21:34 GMT  
		Size: 43.3 MB (43267270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf45eff8a02bcdf7a96904e0dc534c78c89a5c860e224fa57780ef2fc2eab99e`  
		Last Modified: Tue, 07 Jun 2022 00:21:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246089a07769500a0adb027d1dc0efbb1254ee07d75dcdc6f8a3ceb8bae3e95f`  
		Last Modified: Tue, 07 Jun 2022 06:48:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3636fe8b4383f769da39b4c598b1e98b53b6d528e34e9d20fac5c17cfefcd866`  
		Last Modified: Fri, 10 Jun 2022 00:40:50 GMT  
		Size: 12.2 MB (12247499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0a0fd2a02961d2a1725c94d0c0f5670c51d5f5f9bad820a96e45791a5d7a32`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 445.5 KB (445476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beba28f927b0599e17785c8f69b8373e61c14da42247f7683f924f80ecae1439`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:657eec0a2bb289006e136ad46dbd1d85e8ff10712e1477c0fcacb617a19bb242`  
		Last Modified: Wed, 22 Jun 2022 04:31:12 GMT  
		Size: 168.3 MB (168293438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:136be306a609540683e370b2425b4d3703542a79224441c6337af82ee1698ca2`  
		Last Modified: Fri, 24 Jun 2022 03:12:46 GMT  
		Size: 292.6 MB (292641286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3769fbd23a38bb2c2737d30cd4a790f8ad775a99a63e6591de2df21d750f52`  
		Last Modified: Fri, 24 Jun 2022 03:12:29 GMT  
		Size: 795.4 KB (795424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:155517bc4fff02081a754dd1ac5674da90d74db9792a871f64983196cbd2b573`  
		Last Modified: Fri, 24 Jun 2022 03:12:28 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e9d584cf5548a2a612999b7b8fb340c4a38d8e9b31fd9ab73ca09cb173eb0f`  
		Last Modified: Fri, 24 Jun 2022 03:12:28 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2330650c98390edb3e1e7bd4d667c7b4e344da794f180c208aa1c92872db10cc`  
		Last Modified: Fri, 24 Jun 2022 03:12:29 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9458af98469686b7341e974f7343a72938ca0fa6984c887bb8d0a160375881ee`  
		Last Modified: Fri, 24 Jun 2022 03:12:29 GMT  
		Size: 2.5 KB (2503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:13.10.7-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:bb8443f4c39a1e5e1eaa389c87f32b928bccad2f727705a2e02afcc1b98ac2bf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.8 MB (554784337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99d205394842fb0b6709b682ff9d39e01d0ade2e25f08c11c4c8c766f9ccd182`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:00:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:35:32 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 06:36:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:36:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:36:20 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 10:50:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 10:50:03 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 10:50:04 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 10:50:05 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 10:50:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:50:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:59:13 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 10:59:14 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 01:28:16 GMT
COPY dir:1fb0204bb532a7d63a0dd2d2677d66a70be0285454d27afba6780853636ba1ef in /usr/local/tomcat 
# Fri, 10 Jun 2022 01:28:22 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 01:28:24 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 01:28:25 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 01:28:26 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:24 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:25 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:09:26 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:09:27 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:11:42 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 24 Jun 2022 08:11:28 GMT
ENV XWIKI_VERSION=13.10.7
# Fri, 24 Jun 2022 08:11:29 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10.7
# Fri, 24 Jun 2022 08:11:30 GMT
ENV XWIKI_DOWNLOAD_SHA256=b886e886ed34e8d7bea8feb2e74e94edb3fb88030f90ab68c7bbc87dcf453d00
# Fri, 24 Jun 2022 08:12:12 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 24 Jun 2022 08:12:13 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 24 Jun 2022 08:12:14 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 24 Jun 2022 08:12:15 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 24 Jun 2022 08:12:16 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 24 Jun 2022 08:12:17 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 24 Jun 2022 08:12:17 GMT
VOLUME [/usr/local/xwiki]
# Fri, 24 Jun 2022 08:12:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jun 2022 08:12:19 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15da1b4c110f7cc460fbf968fb55b77c541f0e3ab87b92d5e6a822cc2c593e1`  
		Last Modified: Tue, 07 Jun 2022 05:10:23 GMT  
		Size: 15.9 MB (15898299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8e9d6a15d13e6f2d5d43f40b76051350cb7090cfcae5300dc1647e3196577a`  
		Last Modified: Tue, 07 Jun 2022 06:44:15 GMT  
		Size: 41.6 MB (41608356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51219ca7d003431d2f9c6ddda7db0a1902cf2b7e4e879625811b086f268b39c`  
		Last Modified: Tue, 07 Jun 2022 06:44:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5aa4900f44b9e3e20168d54fda3a0b78e62d572de1796db20345b70b1d8b3ca`  
		Last Modified: Tue, 07 Jun 2022 11:23:12 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6796806c88914990f15047665e74a4ea1fb933bdf7b8ebf39b1f2a82b723e044`  
		Last Modified: Fri, 10 Jun 2022 02:03:21 GMT  
		Size: 12.3 MB (12264791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca37469fc5a6ebbc5f1a764aabd4ba48b92a85d1396b644e1139994fad2fa34e`  
		Last Modified: Fri, 10 Jun 2022 02:03:20 GMT  
		Size: 208.8 KB (208841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbf4753a12af2d02fd26a953119f6843f7e381cfec0d679d92b04b4e4f5a3d6a`  
		Last Modified: Wed, 22 Jun 2022 04:18:08 GMT  
		Size: 164.2 MB (164164156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acdad91995b0da375c92d6651576276e78123cfbb080e5444a094fc5033c930c`  
		Last Modified: Fri, 24 Jun 2022 08:15:36 GMT  
		Size: 292.6 MB (292641359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:350ecfd793c7e54308d1c7a22f36e2e098e8fdae31cecb75339bfa7f0a8b7af6`  
		Last Modified: Fri, 24 Jun 2022 08:15:14 GMT  
		Size: 795.4 KB (795417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c27ddaa528e0298945c5eca4aa5235bd761f13f40e2b35de068a7977434e571d`  
		Last Modified: Fri, 24 Jun 2022 08:15:14 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9edb1eb483f19a886fd0fcf80dc5c21e5ef36163eb1e8df94a3b80f508fbeff8`  
		Last Modified: Fri, 24 Jun 2022 08:15:14 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d9ff4c9416279f5b0a9e42bf517e29f15992d0a7a0c5d3361f7fbc8472c12d`  
		Last Modified: Fri, 24 Jun 2022 08:15:14 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be06063b865aaeadaa012c84711685856110099c19fa07ac1af19e12fa08cce`  
		Last Modified: Fri, 24 Jun 2022 08:15:14 GMT  
		Size: 2.5 KB (2507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:14`

```console
$ docker pull xwiki@sha256:8b941b575bfdc8c0eb31d9b7f3422c6fe866062a7b465d725d53ec4107ca6144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:14` - linux; amd64

```console
$ docker pull xwiki@sha256:f08dab318ed8416b7ef8fc05f68b5c11c7f486d1b4686584b35fbf916cb81081
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.4 MB (562431476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68a5a2c9d16899b288b020a4b618dae8b4a2aa67718272532c3f92b8caca60fd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:14:23 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 00:14:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:58 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:59 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 06:30:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:30:41 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 06:30:41 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:30:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:35:57 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 06:35:58 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 00:18:07 GMT
COPY dir:360b17da945f7a5c4dcdc8b0602904442d98c06d17157280c607532ec8b6edaa in /usr/local/tomcat 
# Fri, 10 Jun 2022 00:18:12 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 00:18:13 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 00:18:13 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 00:18:13 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:25:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 22 Jun 2022 04:25:05 GMT
ENV XWIKI_VERSION=14.4.1
# Wed, 22 Jun 2022 04:25:05 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.4.1
# Wed, 22 Jun 2022 04:25:05 GMT
ENV XWIKI_DOWNLOAD_SHA256=8e20eba50acee0f157d3cc160306d65e0995b453833c8923f833030f0a469fb4
# Wed, 22 Jun 2022 04:25:42 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 22 Jun 2022 04:25:43 GMT
ENV MYSQL_JDBC_VERSION=8.0.29
# Wed, 22 Jun 2022 04:25:43 GMT
ENV MYSQL_JDBC_SHA256=d4e32d2a6026b5acc00300b73a86c28fb92681ae9629b21048ee67014c911db6
# Wed, 22 Jun 2022 04:25:43 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.29
# Wed, 22 Jun 2022 04:25:43 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.29.jar
# Wed, 22 Jun 2022 04:25:44 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.29.jar
# Wed, 22 Jun 2022 04:25:44 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Wed, 22 Jun 2022 04:25:44 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 22 Jun 2022 04:25:44 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 22 Jun 2022 04:25:45 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 22 Jun 2022 04:25:45 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 22 Jun 2022 04:25:45 GMT
VOLUME [/usr/local/xwiki]
# Wed, 22 Jun 2022 04:25:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jun 2022 04:25:45 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b669251e19038a24bd6cab0baab92077f23163880fac4701fb3efa564350732b`  
		Last Modified: Tue, 07 Jun 2022 00:21:34 GMT  
		Size: 43.3 MB (43267270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf45eff8a02bcdf7a96904e0dc534c78c89a5c860e224fa57780ef2fc2eab99e`  
		Last Modified: Tue, 07 Jun 2022 00:21:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246089a07769500a0adb027d1dc0efbb1254ee07d75dcdc6f8a3ceb8bae3e95f`  
		Last Modified: Tue, 07 Jun 2022 06:48:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3636fe8b4383f769da39b4c598b1e98b53b6d528e34e9d20fac5c17cfefcd866`  
		Last Modified: Fri, 10 Jun 2022 00:40:50 GMT  
		Size: 12.2 MB (12247499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0a0fd2a02961d2a1725c94d0c0f5670c51d5f5f9bad820a96e45791a5d7a32`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 445.5 KB (445476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beba28f927b0599e17785c8f69b8373e61c14da42247f7683f924f80ecae1439`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c54774971cb7c57e8fe14a42f90f7e4cceb67150ff2f3112f9ad46fea390190d`  
		Last Modified: Wed, 22 Jun 2022 04:30:07 GMT  
		Size: 167.5 MB (167492656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:368fa3670d498d9bc0883cd81cf9b9a45d3ccf79365eabe27b779344efefda58`  
		Last Modified: Wed, 22 Jun 2022 04:30:00 GMT  
		Size: 292.0 MB (291982499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb96a08b07f52ad5c126f31fe742e1c114a3239ab5c6fc5641266fa5be00579`  
		Last Modified: Wed, 22 Jun 2022 04:29:42 GMT  
		Size: 2.4 MB (2381172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94af0360a2e049892f0b11539619a1e889f32dcdec1df1a671ffb6032f55437`  
		Last Modified: Wed, 22 Jun 2022 04:29:41 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7255f65a4fc48ef292f0f13fc58a9f76e18f7f3969190698a08ff5907c9e5dd`  
		Last Modified: Wed, 22 Jun 2022 04:29:41 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1695b6d1dbcfb2018bc0a46ec5c66b47f1105c4aff382726932ee462014d294e`  
		Last Modified: Wed, 22 Jun 2022 04:29:41 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec62f61e9a4c7f7d90e61399a76eb18b02a789afbac8e9fcaaa1f8ebc6b10da`  
		Last Modified: Wed, 22 Jun 2022 04:29:41 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:14` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:b4d50e1906ede668b41d744d6050b179dc5523658ba13b4e4cc5a92b98955a71
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.9 MB (554912952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed7a93d82de140d630b2eab42fb4270590bb2efcab4d72dd5a2f2dd8ce842278`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:00:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:35:32 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 06:36:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:36:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:36:20 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 10:50:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 10:50:03 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 10:50:04 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 10:50:05 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 10:50:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:50:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:59:13 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 10:59:14 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 01:28:16 GMT
COPY dir:1fb0204bb532a7d63a0dd2d2677d66a70be0285454d27afba6780853636ba1ef in /usr/local/tomcat 
# Fri, 10 Jun 2022 01:28:22 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 01:28:24 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 01:28:25 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 01:28:26 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:24 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:25 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:09:26 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:09:27 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:10:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 22 Jun 2022 04:10:05 GMT
ENV XWIKI_VERSION=14.4.1
# Wed, 22 Jun 2022 04:10:06 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.4.1
# Wed, 22 Jun 2022 04:10:07 GMT
ENV XWIKI_DOWNLOAD_SHA256=8e20eba50acee0f157d3cc160306d65e0995b453833c8923f833030f0a469fb4
# Wed, 22 Jun 2022 04:10:44 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 22 Jun 2022 04:10:45 GMT
ENV MYSQL_JDBC_VERSION=8.0.29
# Wed, 22 Jun 2022 04:10:45 GMT
ENV MYSQL_JDBC_SHA256=d4e32d2a6026b5acc00300b73a86c28fb92681ae9629b21048ee67014c911db6
# Wed, 22 Jun 2022 04:10:46 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.29
# Wed, 22 Jun 2022 04:10:47 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.29.jar
# Wed, 22 Jun 2022 04:10:48 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.29.jar
# Wed, 22 Jun 2022 04:10:50 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Wed, 22 Jun 2022 04:10:51 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 22 Jun 2022 04:10:52 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 22 Jun 2022 04:10:53 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 22 Jun 2022 04:10:54 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 22 Jun 2022 04:10:54 GMT
VOLUME [/usr/local/xwiki]
# Wed, 22 Jun 2022 04:10:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jun 2022 04:10:56 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15da1b4c110f7cc460fbf968fb55b77c541f0e3ab87b92d5e6a822cc2c593e1`  
		Last Modified: Tue, 07 Jun 2022 05:10:23 GMT  
		Size: 15.9 MB (15898299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8e9d6a15d13e6f2d5d43f40b76051350cb7090cfcae5300dc1647e3196577a`  
		Last Modified: Tue, 07 Jun 2022 06:44:15 GMT  
		Size: 41.6 MB (41608356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51219ca7d003431d2f9c6ddda7db0a1902cf2b7e4e879625811b086f268b39c`  
		Last Modified: Tue, 07 Jun 2022 06:44:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5aa4900f44b9e3e20168d54fda3a0b78e62d572de1796db20345b70b1d8b3ca`  
		Last Modified: Tue, 07 Jun 2022 11:23:12 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6796806c88914990f15047665e74a4ea1fb933bdf7b8ebf39b1f2a82b723e044`  
		Last Modified: Fri, 10 Jun 2022 02:03:21 GMT  
		Size: 12.3 MB (12264791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca37469fc5a6ebbc5f1a764aabd4ba48b92a85d1396b644e1139994fad2fa34e`  
		Last Modified: Fri, 10 Jun 2022 02:03:20 GMT  
		Size: 208.8 KB (208841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c24501792b443d8ecb222b1c49c98ee84d4d76016bdbf8ba61b488fa873f7f`  
		Last Modified: Wed, 22 Jun 2022 04:17:01 GMT  
		Size: 163.4 MB (163365370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d1bb494106d6d36bcf7dd967f0d881aa979803343f00918d55f105d5759bbe`  
		Last Modified: Wed, 22 Jun 2022 04:16:59 GMT  
		Size: 292.0 MB (291982622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a24595bb483532afb5982a7102104c4107076a079eeaa4d5fd0d776abe5a1543`  
		Last Modified: Wed, 22 Jun 2022 04:16:38 GMT  
		Size: 2.4 MB (2381177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff7c257d2e413a9084ca6e6cbd963fb66e757d99cd06e3bd96971b96b7ca0083`  
		Last Modified: Wed, 22 Jun 2022 04:16:37 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:343c1e7e3713943da3994aafca00d9f54df0f67fb6b20d86933ebe4a05623d0e`  
		Last Modified: Wed, 22 Jun 2022 04:16:37 GMT  
		Size: 2.3 KB (2309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e0fa83eef81ca126718a8c16fd8f17e6ead2f37ccfc6a8dbf8e2568d221ac0`  
		Last Modified: Wed, 22 Jun 2022 04:16:37 GMT  
		Size: 5.9 KB (5854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c0f8a5973921c322d0333259d28d3c3ab9fa848afe20830fa1aad3fa46743fc`  
		Last Modified: Wed, 22 Jun 2022 04:16:37 GMT  
		Size: 2.5 KB (2509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:14-mariadb-tomcat`

```console
$ docker pull xwiki@sha256:3db745735e3f4998cf83b2a5dc35cd5b861564cac0ff1f91425512cc46c054ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:14-mariadb-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:5be2c4cf71703a8afc1dc6cd56002d86482ca326367b5a080809603ece9ae80a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.6 MB (560590373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7416cc5f4b70e5175c8fecfe02fb114cdab2e1b5150287649b6d3524c2bcd556`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:14:23 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 00:14:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:58 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:59 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 06:30:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:30:41 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 06:30:41 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:30:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:35:57 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 06:35:58 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 00:18:07 GMT
COPY dir:360b17da945f7a5c4dcdc8b0602904442d98c06d17157280c607532ec8b6edaa in /usr/local/tomcat 
# Fri, 10 Jun 2022 00:18:12 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 00:18:13 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 00:18:13 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 00:18:13 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:25:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 22 Jun 2022 04:25:05 GMT
ENV XWIKI_VERSION=14.4.1
# Wed, 22 Jun 2022 04:25:05 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.4.1
# Wed, 22 Jun 2022 04:25:05 GMT
ENV XWIKI_DOWNLOAD_SHA256=8e20eba50acee0f157d3cc160306d65e0995b453833c8923f833030f0a469fb4
# Wed, 22 Jun 2022 04:25:42 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 22 Jun 2022 04:27:20 GMT
ENV MARIADB_JDBC_VERSION=3.0.5
# Wed, 22 Jun 2022 04:27:20 GMT
ENV MARIADB_JDBC_SHA256=e9532d9bca07c1263c32b00b495bd3ec7f2b79320513cabd762bf39ea09e68d9
# Wed, 22 Jun 2022 04:27:20 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.0.5
# Wed, 22 Jun 2022 04:27:20 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.0.5.jar
# Wed, 22 Jun 2022 04:27:20 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.0.5.jar
# Wed, 22 Jun 2022 04:27:21 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Wed, 22 Jun 2022 04:27:21 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 22 Jun 2022 04:27:21 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 22 Jun 2022 04:27:22 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 22 Jun 2022 04:27:22 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 22 Jun 2022 04:27:22 GMT
VOLUME [/usr/local/xwiki]
# Wed, 22 Jun 2022 04:27:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jun 2022 04:27:22 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b669251e19038a24bd6cab0baab92077f23163880fac4701fb3efa564350732b`  
		Last Modified: Tue, 07 Jun 2022 00:21:34 GMT  
		Size: 43.3 MB (43267270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf45eff8a02bcdf7a96904e0dc534c78c89a5c860e224fa57780ef2fc2eab99e`  
		Last Modified: Tue, 07 Jun 2022 00:21:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246089a07769500a0adb027d1dc0efbb1254ee07d75dcdc6f8a3ceb8bae3e95f`  
		Last Modified: Tue, 07 Jun 2022 06:48:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3636fe8b4383f769da39b4c598b1e98b53b6d528e34e9d20fac5c17cfefcd866`  
		Last Modified: Fri, 10 Jun 2022 00:40:50 GMT  
		Size: 12.2 MB (12247499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0a0fd2a02961d2a1725c94d0c0f5670c51d5f5f9bad820a96e45791a5d7a32`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 445.5 KB (445476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beba28f927b0599e17785c8f69b8373e61c14da42247f7683f924f80ecae1439`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c54774971cb7c57e8fe14a42f90f7e4cceb67150ff2f3112f9ad46fea390190d`  
		Last Modified: Wed, 22 Jun 2022 04:30:07 GMT  
		Size: 167.5 MB (167492656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:368fa3670d498d9bc0883cd81cf9b9a45d3ccf79365eabe27b779344efefda58`  
		Last Modified: Wed, 22 Jun 2022 04:30:00 GMT  
		Size: 292.0 MB (291982499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c1ab918c0e0ec1820084e4da9e0f385f44acb6a9a2c61f37cba3191a960dec1`  
		Last Modified: Wed, 22 Jun 2022 04:31:36 GMT  
		Size: 540.1 KB (540065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2359c2da84be359f352d0435136b09e78a9776b1d22b4dbdd3f6fec942973375`  
		Last Modified: Wed, 22 Jun 2022 04:31:36 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9269ef1e91c8bcc8306aee08c0a04ec885a56ef859428b65c847bec5ddf4d5ce`  
		Last Modified: Wed, 22 Jun 2022 04:31:35 GMT  
		Size: 2.3 KB (2309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b60d3cde6a56696f82809b7ff8a140448d3abe21f2778008cd1c92705cd8cb`  
		Last Modified: Wed, 22 Jun 2022 04:31:35 GMT  
		Size: 5.9 KB (5856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d320a8df62dc7b14288e1ee93b18d239e5ac432d1ac8aab55e511dcbdfbc27`  
		Last Modified: Wed, 22 Jun 2022 04:31:35 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:14-mariadb-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:bda93d405e13407149f8f73a5894a9ac80b447f92ade102dcb003d1fbd9e8a7f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **553.1 MB (553071844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ee73663f1cd3949cf5e95503adb5d84ae70153601cd42f36eea35f77b61d0b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:00:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:35:32 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 06:36:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:36:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:36:20 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 10:50:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 10:50:03 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 10:50:04 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 10:50:05 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 10:50:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:50:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:59:13 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 10:59:14 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 01:28:16 GMT
COPY dir:1fb0204bb532a7d63a0dd2d2677d66a70be0285454d27afba6780853636ba1ef in /usr/local/tomcat 
# Fri, 10 Jun 2022 01:28:22 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 01:28:24 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 01:28:25 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 01:28:26 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:24 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:25 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:09:26 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:09:27 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:10:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 22 Jun 2022 04:10:05 GMT
ENV XWIKI_VERSION=14.4.1
# Wed, 22 Jun 2022 04:10:06 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.4.1
# Wed, 22 Jun 2022 04:10:07 GMT
ENV XWIKI_DOWNLOAD_SHA256=8e20eba50acee0f157d3cc160306d65e0995b453833c8923f833030f0a469fb4
# Wed, 22 Jun 2022 04:10:44 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 22 Jun 2022 04:12:47 GMT
ENV MARIADB_JDBC_VERSION=3.0.5
# Wed, 22 Jun 2022 04:12:48 GMT
ENV MARIADB_JDBC_SHA256=e9532d9bca07c1263c32b00b495bd3ec7f2b79320513cabd762bf39ea09e68d9
# Wed, 22 Jun 2022 04:12:49 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.0.5
# Wed, 22 Jun 2022 04:12:50 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.0.5.jar
# Wed, 22 Jun 2022 04:12:51 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.0.5.jar
# Wed, 22 Jun 2022 04:12:53 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Wed, 22 Jun 2022 04:12:54 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 22 Jun 2022 04:12:55 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 22 Jun 2022 04:12:56 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 22 Jun 2022 04:12:57 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 22 Jun 2022 04:12:57 GMT
VOLUME [/usr/local/xwiki]
# Wed, 22 Jun 2022 04:12:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jun 2022 04:12:59 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15da1b4c110f7cc460fbf968fb55b77c541f0e3ab87b92d5e6a822cc2c593e1`  
		Last Modified: Tue, 07 Jun 2022 05:10:23 GMT  
		Size: 15.9 MB (15898299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8e9d6a15d13e6f2d5d43f40b76051350cb7090cfcae5300dc1647e3196577a`  
		Last Modified: Tue, 07 Jun 2022 06:44:15 GMT  
		Size: 41.6 MB (41608356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51219ca7d003431d2f9c6ddda7db0a1902cf2b7e4e879625811b086f268b39c`  
		Last Modified: Tue, 07 Jun 2022 06:44:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5aa4900f44b9e3e20168d54fda3a0b78e62d572de1796db20345b70b1d8b3ca`  
		Last Modified: Tue, 07 Jun 2022 11:23:12 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6796806c88914990f15047665e74a4ea1fb933bdf7b8ebf39b1f2a82b723e044`  
		Last Modified: Fri, 10 Jun 2022 02:03:21 GMT  
		Size: 12.3 MB (12264791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca37469fc5a6ebbc5f1a764aabd4ba48b92a85d1396b644e1139994fad2fa34e`  
		Last Modified: Fri, 10 Jun 2022 02:03:20 GMT  
		Size: 208.8 KB (208841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c24501792b443d8ecb222b1c49c98ee84d4d76016bdbf8ba61b488fa873f7f`  
		Last Modified: Wed, 22 Jun 2022 04:17:01 GMT  
		Size: 163.4 MB (163365370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d1bb494106d6d36bcf7dd967f0d881aa979803343f00918d55f105d5759bbe`  
		Last Modified: Wed, 22 Jun 2022 04:16:59 GMT  
		Size: 292.0 MB (291982622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba0bfc714e56ec603906f85a8dacd34f5dad693a8c6dbcf8a9567fbca423d16`  
		Last Modified: Wed, 22 Jun 2022 04:18:35 GMT  
		Size: 540.1 KB (540069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e192a89ffea555829e044cd56b10c8021a547d8a56e5a69c0a6714bb461f596d`  
		Last Modified: Wed, 22 Jun 2022 04:18:35 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc8a81604a8c8778019d65f20d4893ebf3957eadbc949f6c2ca6a5ede778ba6d`  
		Last Modified: Wed, 22 Jun 2022 04:18:35 GMT  
		Size: 2.3 KB (2311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d62f47e27689a9f1dfc33daa4881e9da0078b7620dbb8c9c520858ac340b8fb4`  
		Last Modified: Wed, 22 Jun 2022 04:18:34 GMT  
		Size: 5.9 KB (5854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:542f6bbdec9617d4401973008c85e7ea003f6f336c453085de1f99098e8911e4`  
		Last Modified: Wed, 22 Jun 2022 04:18:34 GMT  
		Size: 2.5 KB (2507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:14-mysql-tomcat`

```console
$ docker pull xwiki@sha256:8b941b575bfdc8c0eb31d9b7f3422c6fe866062a7b465d725d53ec4107ca6144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:14-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:f08dab318ed8416b7ef8fc05f68b5c11c7f486d1b4686584b35fbf916cb81081
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.4 MB (562431476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68a5a2c9d16899b288b020a4b618dae8b4a2aa67718272532c3f92b8caca60fd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:14:23 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 00:14:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:58 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:59 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 06:30:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:30:41 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 06:30:41 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:30:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:35:57 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 06:35:58 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 00:18:07 GMT
COPY dir:360b17da945f7a5c4dcdc8b0602904442d98c06d17157280c607532ec8b6edaa in /usr/local/tomcat 
# Fri, 10 Jun 2022 00:18:12 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 00:18:13 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 00:18:13 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 00:18:13 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:25:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 22 Jun 2022 04:25:05 GMT
ENV XWIKI_VERSION=14.4.1
# Wed, 22 Jun 2022 04:25:05 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.4.1
# Wed, 22 Jun 2022 04:25:05 GMT
ENV XWIKI_DOWNLOAD_SHA256=8e20eba50acee0f157d3cc160306d65e0995b453833c8923f833030f0a469fb4
# Wed, 22 Jun 2022 04:25:42 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 22 Jun 2022 04:25:43 GMT
ENV MYSQL_JDBC_VERSION=8.0.29
# Wed, 22 Jun 2022 04:25:43 GMT
ENV MYSQL_JDBC_SHA256=d4e32d2a6026b5acc00300b73a86c28fb92681ae9629b21048ee67014c911db6
# Wed, 22 Jun 2022 04:25:43 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.29
# Wed, 22 Jun 2022 04:25:43 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.29.jar
# Wed, 22 Jun 2022 04:25:44 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.29.jar
# Wed, 22 Jun 2022 04:25:44 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Wed, 22 Jun 2022 04:25:44 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 22 Jun 2022 04:25:44 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 22 Jun 2022 04:25:45 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 22 Jun 2022 04:25:45 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 22 Jun 2022 04:25:45 GMT
VOLUME [/usr/local/xwiki]
# Wed, 22 Jun 2022 04:25:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jun 2022 04:25:45 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b669251e19038a24bd6cab0baab92077f23163880fac4701fb3efa564350732b`  
		Last Modified: Tue, 07 Jun 2022 00:21:34 GMT  
		Size: 43.3 MB (43267270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf45eff8a02bcdf7a96904e0dc534c78c89a5c860e224fa57780ef2fc2eab99e`  
		Last Modified: Tue, 07 Jun 2022 00:21:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246089a07769500a0adb027d1dc0efbb1254ee07d75dcdc6f8a3ceb8bae3e95f`  
		Last Modified: Tue, 07 Jun 2022 06:48:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3636fe8b4383f769da39b4c598b1e98b53b6d528e34e9d20fac5c17cfefcd866`  
		Last Modified: Fri, 10 Jun 2022 00:40:50 GMT  
		Size: 12.2 MB (12247499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0a0fd2a02961d2a1725c94d0c0f5670c51d5f5f9bad820a96e45791a5d7a32`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 445.5 KB (445476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beba28f927b0599e17785c8f69b8373e61c14da42247f7683f924f80ecae1439`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c54774971cb7c57e8fe14a42f90f7e4cceb67150ff2f3112f9ad46fea390190d`  
		Last Modified: Wed, 22 Jun 2022 04:30:07 GMT  
		Size: 167.5 MB (167492656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:368fa3670d498d9bc0883cd81cf9b9a45d3ccf79365eabe27b779344efefda58`  
		Last Modified: Wed, 22 Jun 2022 04:30:00 GMT  
		Size: 292.0 MB (291982499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb96a08b07f52ad5c126f31fe742e1c114a3239ab5c6fc5641266fa5be00579`  
		Last Modified: Wed, 22 Jun 2022 04:29:42 GMT  
		Size: 2.4 MB (2381172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94af0360a2e049892f0b11539619a1e889f32dcdec1df1a671ffb6032f55437`  
		Last Modified: Wed, 22 Jun 2022 04:29:41 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7255f65a4fc48ef292f0f13fc58a9f76e18f7f3969190698a08ff5907c9e5dd`  
		Last Modified: Wed, 22 Jun 2022 04:29:41 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1695b6d1dbcfb2018bc0a46ec5c66b47f1105c4aff382726932ee462014d294e`  
		Last Modified: Wed, 22 Jun 2022 04:29:41 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec62f61e9a4c7f7d90e61399a76eb18b02a789afbac8e9fcaaa1f8ebc6b10da`  
		Last Modified: Wed, 22 Jun 2022 04:29:41 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:14-mysql-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:b4d50e1906ede668b41d744d6050b179dc5523658ba13b4e4cc5a92b98955a71
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.9 MB (554912952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed7a93d82de140d630b2eab42fb4270590bb2efcab4d72dd5a2f2dd8ce842278`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:00:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:35:32 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 06:36:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:36:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:36:20 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 10:50:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 10:50:03 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 10:50:04 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 10:50:05 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 10:50:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:50:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:59:13 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 10:59:14 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 01:28:16 GMT
COPY dir:1fb0204bb532a7d63a0dd2d2677d66a70be0285454d27afba6780853636ba1ef in /usr/local/tomcat 
# Fri, 10 Jun 2022 01:28:22 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 01:28:24 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 01:28:25 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 01:28:26 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:24 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:25 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:09:26 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:09:27 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:10:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 22 Jun 2022 04:10:05 GMT
ENV XWIKI_VERSION=14.4.1
# Wed, 22 Jun 2022 04:10:06 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.4.1
# Wed, 22 Jun 2022 04:10:07 GMT
ENV XWIKI_DOWNLOAD_SHA256=8e20eba50acee0f157d3cc160306d65e0995b453833c8923f833030f0a469fb4
# Wed, 22 Jun 2022 04:10:44 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 22 Jun 2022 04:10:45 GMT
ENV MYSQL_JDBC_VERSION=8.0.29
# Wed, 22 Jun 2022 04:10:45 GMT
ENV MYSQL_JDBC_SHA256=d4e32d2a6026b5acc00300b73a86c28fb92681ae9629b21048ee67014c911db6
# Wed, 22 Jun 2022 04:10:46 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.29
# Wed, 22 Jun 2022 04:10:47 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.29.jar
# Wed, 22 Jun 2022 04:10:48 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.29.jar
# Wed, 22 Jun 2022 04:10:50 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Wed, 22 Jun 2022 04:10:51 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 22 Jun 2022 04:10:52 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 22 Jun 2022 04:10:53 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 22 Jun 2022 04:10:54 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 22 Jun 2022 04:10:54 GMT
VOLUME [/usr/local/xwiki]
# Wed, 22 Jun 2022 04:10:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jun 2022 04:10:56 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15da1b4c110f7cc460fbf968fb55b77c541f0e3ab87b92d5e6a822cc2c593e1`  
		Last Modified: Tue, 07 Jun 2022 05:10:23 GMT  
		Size: 15.9 MB (15898299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8e9d6a15d13e6f2d5d43f40b76051350cb7090cfcae5300dc1647e3196577a`  
		Last Modified: Tue, 07 Jun 2022 06:44:15 GMT  
		Size: 41.6 MB (41608356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51219ca7d003431d2f9c6ddda7db0a1902cf2b7e4e879625811b086f268b39c`  
		Last Modified: Tue, 07 Jun 2022 06:44:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5aa4900f44b9e3e20168d54fda3a0b78e62d572de1796db20345b70b1d8b3ca`  
		Last Modified: Tue, 07 Jun 2022 11:23:12 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6796806c88914990f15047665e74a4ea1fb933bdf7b8ebf39b1f2a82b723e044`  
		Last Modified: Fri, 10 Jun 2022 02:03:21 GMT  
		Size: 12.3 MB (12264791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca37469fc5a6ebbc5f1a764aabd4ba48b92a85d1396b644e1139994fad2fa34e`  
		Last Modified: Fri, 10 Jun 2022 02:03:20 GMT  
		Size: 208.8 KB (208841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c24501792b443d8ecb222b1c49c98ee84d4d76016bdbf8ba61b488fa873f7f`  
		Last Modified: Wed, 22 Jun 2022 04:17:01 GMT  
		Size: 163.4 MB (163365370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d1bb494106d6d36bcf7dd967f0d881aa979803343f00918d55f105d5759bbe`  
		Last Modified: Wed, 22 Jun 2022 04:16:59 GMT  
		Size: 292.0 MB (291982622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a24595bb483532afb5982a7102104c4107076a079eeaa4d5fd0d776abe5a1543`  
		Last Modified: Wed, 22 Jun 2022 04:16:38 GMT  
		Size: 2.4 MB (2381177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff7c257d2e413a9084ca6e6cbd963fb66e757d99cd06e3bd96971b96b7ca0083`  
		Last Modified: Wed, 22 Jun 2022 04:16:37 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:343c1e7e3713943da3994aafca00d9f54df0f67fb6b20d86933ebe4a05623d0e`  
		Last Modified: Wed, 22 Jun 2022 04:16:37 GMT  
		Size: 2.3 KB (2309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e0fa83eef81ca126718a8c16fd8f17e6ead2f37ccfc6a8dbf8e2568d221ac0`  
		Last Modified: Wed, 22 Jun 2022 04:16:37 GMT  
		Size: 5.9 KB (5854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c0f8a5973921c322d0333259d28d3c3ab9fa848afe20830fa1aad3fa46743fc`  
		Last Modified: Wed, 22 Jun 2022 04:16:37 GMT  
		Size: 2.5 KB (2509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:14-postgres-tomcat`

```console
$ docker pull xwiki@sha256:1fabdb2e4da65c0abe19ecbaf0ff7ee43cfa94d27091c3d5748e8211ff99735d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:14-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:be2ec4361ef195cce3e9b320a91b407e3928431c94a7adb57af1f11044876bd6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **561.6 MB (561646591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d6170aaa002127cf799999888c4d5d58bc136c94008910619af04189b3825fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:14:23 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 00:14:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:58 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:59 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 06:30:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:30:41 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 06:30:41 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:30:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:35:57 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 06:35:58 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 00:18:07 GMT
COPY dir:360b17da945f7a5c4dcdc8b0602904442d98c06d17157280c607532ec8b6edaa in /usr/local/tomcat 
# Fri, 10 Jun 2022 00:18:12 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 00:18:13 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 00:18:13 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 00:18:13 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:26:27 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Wed, 22 Jun 2022 04:26:29 GMT
ENV XWIKI_VERSION=14.4.1
# Wed, 22 Jun 2022 04:26:29 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.4.1
# Wed, 22 Jun 2022 04:26:29 GMT
ENV XWIKI_DOWNLOAD_SHA256=8e20eba50acee0f157d3cc160306d65e0995b453833c8923f833030f0a469fb4
# Wed, 22 Jun 2022 04:27:07 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 22 Jun 2022 04:27:08 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Wed, 22 Jun 2022 04:27:08 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 22 Jun 2022 04:27:08 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 22 Jun 2022 04:27:09 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 22 Jun 2022 04:27:09 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 22 Jun 2022 04:27:09 GMT
VOLUME [/usr/local/xwiki]
# Wed, 22 Jun 2022 04:27:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jun 2022 04:27:09 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b669251e19038a24bd6cab0baab92077f23163880fac4701fb3efa564350732b`  
		Last Modified: Tue, 07 Jun 2022 00:21:34 GMT  
		Size: 43.3 MB (43267270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf45eff8a02bcdf7a96904e0dc534c78c89a5c860e224fa57780ef2fc2eab99e`  
		Last Modified: Tue, 07 Jun 2022 00:21:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246089a07769500a0adb027d1dc0efbb1254ee07d75dcdc6f8a3ceb8bae3e95f`  
		Last Modified: Tue, 07 Jun 2022 06:48:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3636fe8b4383f769da39b4c598b1e98b53b6d528e34e9d20fac5c17cfefcd866`  
		Last Modified: Fri, 10 Jun 2022 00:40:50 GMT  
		Size: 12.2 MB (12247499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0a0fd2a02961d2a1725c94d0c0f5670c51d5f5f9bad820a96e45791a5d7a32`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 445.5 KB (445476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beba28f927b0599e17785c8f69b8373e61c14da42247f7683f924f80ecae1439`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:657eec0a2bb289006e136ad46dbd1d85e8ff10712e1477c0fcacb617a19bb242`  
		Last Modified: Wed, 22 Jun 2022 04:31:12 GMT  
		Size: 168.3 MB (168293438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7336ce43765447d78aa2db6c3c2d06f343d8c461acf64bd26ad2da6cdb3802e9`  
		Last Modified: Wed, 22 Jun 2022 04:31:05 GMT  
		Size: 292.0 MB (291982439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed867fb2baa0895487cb447dc1687bb44e7fa6941a1ed692bc25262eb6c8ce84`  
		Last Modified: Wed, 22 Jun 2022 04:30:47 GMT  
		Size: 795.4 KB (795422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffb2ca6524e098e2552dc1ee3c9df3692d579ef2fe4d945c2aefab62c820dfef`  
		Last Modified: Wed, 22 Jun 2022 04:30:46 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7f44840360a683faa6f816201fff0fcc275d3c3c886e55bd98a5b77b283d9f2`  
		Last Modified: Wed, 22 Jun 2022 04:30:46 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea0454030911a4eba98666b0184b8c3241a86aaffd563ef77f78cf31f9103402`  
		Last Modified: Wed, 22 Jun 2022 04:30:46 GMT  
		Size: 5.9 KB (5854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e070314e7d3d33ac915c9e5d8719b2d00e3207754d5b335482a0e76137e50a`  
		Last Modified: Wed, 22 Jun 2022 04:30:46 GMT  
		Size: 2.5 KB (2503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:14-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:b3ce0cb6e854ea382295ea6bb0f34559cb20af7194ac7aa73e10036616745688
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.1 MB (554126019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:964c73cc655f5ead167b952f043637ed76a9a1e4fa99f78c8bc52620b48566db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:00:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:35:32 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 06:36:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:36:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:36:20 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 10:50:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 10:50:03 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 10:50:04 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 10:50:05 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 10:50:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:50:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:59:13 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 10:59:14 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 01:28:16 GMT
COPY dir:1fb0204bb532a7d63a0dd2d2677d66a70be0285454d27afba6780853636ba1ef in /usr/local/tomcat 
# Fri, 10 Jun 2022 01:28:22 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 01:28:24 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 01:28:25 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 01:28:26 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:24 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:25 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:09:26 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:09:27 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:11:42 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Wed, 22 Jun 2022 04:11:43 GMT
ENV XWIKI_VERSION=14.4.1
# Wed, 22 Jun 2022 04:11:43 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.4.1
# Wed, 22 Jun 2022 04:11:44 GMT
ENV XWIKI_DOWNLOAD_SHA256=8e20eba50acee0f157d3cc160306d65e0995b453833c8923f833030f0a469fb4
# Wed, 22 Jun 2022 04:12:23 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 22 Jun 2022 04:12:24 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Wed, 22 Jun 2022 04:12:25 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 22 Jun 2022 04:12:26 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 22 Jun 2022 04:12:27 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 22 Jun 2022 04:12:28 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 22 Jun 2022 04:12:28 GMT
VOLUME [/usr/local/xwiki]
# Wed, 22 Jun 2022 04:12:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jun 2022 04:12:30 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15da1b4c110f7cc460fbf968fb55b77c541f0e3ab87b92d5e6a822cc2c593e1`  
		Last Modified: Tue, 07 Jun 2022 05:10:23 GMT  
		Size: 15.9 MB (15898299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8e9d6a15d13e6f2d5d43f40b76051350cb7090cfcae5300dc1647e3196577a`  
		Last Modified: Tue, 07 Jun 2022 06:44:15 GMT  
		Size: 41.6 MB (41608356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51219ca7d003431d2f9c6ddda7db0a1902cf2b7e4e879625811b086f268b39c`  
		Last Modified: Tue, 07 Jun 2022 06:44:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5aa4900f44b9e3e20168d54fda3a0b78e62d572de1796db20345b70b1d8b3ca`  
		Last Modified: Tue, 07 Jun 2022 11:23:12 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6796806c88914990f15047665e74a4ea1fb933bdf7b8ebf39b1f2a82b723e044`  
		Last Modified: Fri, 10 Jun 2022 02:03:21 GMT  
		Size: 12.3 MB (12264791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca37469fc5a6ebbc5f1a764aabd4ba48b92a85d1396b644e1139994fad2fa34e`  
		Last Modified: Fri, 10 Jun 2022 02:03:20 GMT  
		Size: 208.8 KB (208841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbf4753a12af2d02fd26a953119f6843f7e381cfec0d679d92b04b4e4f5a3d6a`  
		Last Modified: Wed, 22 Jun 2022 04:18:08 GMT  
		Size: 164.2 MB (164164156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8735ad3b7140d98c3eedfd5e132b33810f9ccbd2ef89e37d738de84113c7dc92`  
		Last Modified: Wed, 22 Jun 2022 04:18:07 GMT  
		Size: 292.0 MB (291982533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e05d15dcdbfe55730845a86712aea5417820a8fc73ea492391f4bc8773f273c`  
		Last Modified: Wed, 22 Jun 2022 04:17:46 GMT  
		Size: 795.4 KB (795416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ed4588b795d5cf65bf69167563114888c0924eec209d7f1a1f2f78f04f2e42`  
		Last Modified: Wed, 22 Jun 2022 04:17:45 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f537181948e5040a35cd0252682f25858131a6b14dd2a0cc0f8e9d4deb3dff1`  
		Last Modified: Wed, 22 Jun 2022 04:17:45 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f44b9ff69abe9f98824c9cccb73f52b56acccad5bf10bbf6df522ad974eb8fec`  
		Last Modified: Wed, 22 Jun 2022 04:17:45 GMT  
		Size: 5.9 KB (5851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f781c1d839ed0cddf10a24f41ffa5dc32da0de94c89077f83fd5f3cfa0c62ed6`  
		Last Modified: Wed, 22 Jun 2022 04:17:45 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:14.4`

```console
$ docker pull xwiki@sha256:8b941b575bfdc8c0eb31d9b7f3422c6fe866062a7b465d725d53ec4107ca6144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:14.4` - linux; amd64

```console
$ docker pull xwiki@sha256:f08dab318ed8416b7ef8fc05f68b5c11c7f486d1b4686584b35fbf916cb81081
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.4 MB (562431476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68a5a2c9d16899b288b020a4b618dae8b4a2aa67718272532c3f92b8caca60fd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:14:23 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 00:14:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:58 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:59 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 06:30:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:30:41 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 06:30:41 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:30:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:35:57 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 06:35:58 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 00:18:07 GMT
COPY dir:360b17da945f7a5c4dcdc8b0602904442d98c06d17157280c607532ec8b6edaa in /usr/local/tomcat 
# Fri, 10 Jun 2022 00:18:12 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 00:18:13 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 00:18:13 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 00:18:13 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:25:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 22 Jun 2022 04:25:05 GMT
ENV XWIKI_VERSION=14.4.1
# Wed, 22 Jun 2022 04:25:05 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.4.1
# Wed, 22 Jun 2022 04:25:05 GMT
ENV XWIKI_DOWNLOAD_SHA256=8e20eba50acee0f157d3cc160306d65e0995b453833c8923f833030f0a469fb4
# Wed, 22 Jun 2022 04:25:42 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 22 Jun 2022 04:25:43 GMT
ENV MYSQL_JDBC_VERSION=8.0.29
# Wed, 22 Jun 2022 04:25:43 GMT
ENV MYSQL_JDBC_SHA256=d4e32d2a6026b5acc00300b73a86c28fb92681ae9629b21048ee67014c911db6
# Wed, 22 Jun 2022 04:25:43 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.29
# Wed, 22 Jun 2022 04:25:43 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.29.jar
# Wed, 22 Jun 2022 04:25:44 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.29.jar
# Wed, 22 Jun 2022 04:25:44 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Wed, 22 Jun 2022 04:25:44 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 22 Jun 2022 04:25:44 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 22 Jun 2022 04:25:45 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 22 Jun 2022 04:25:45 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 22 Jun 2022 04:25:45 GMT
VOLUME [/usr/local/xwiki]
# Wed, 22 Jun 2022 04:25:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jun 2022 04:25:45 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b669251e19038a24bd6cab0baab92077f23163880fac4701fb3efa564350732b`  
		Last Modified: Tue, 07 Jun 2022 00:21:34 GMT  
		Size: 43.3 MB (43267270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf45eff8a02bcdf7a96904e0dc534c78c89a5c860e224fa57780ef2fc2eab99e`  
		Last Modified: Tue, 07 Jun 2022 00:21:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246089a07769500a0adb027d1dc0efbb1254ee07d75dcdc6f8a3ceb8bae3e95f`  
		Last Modified: Tue, 07 Jun 2022 06:48:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3636fe8b4383f769da39b4c598b1e98b53b6d528e34e9d20fac5c17cfefcd866`  
		Last Modified: Fri, 10 Jun 2022 00:40:50 GMT  
		Size: 12.2 MB (12247499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0a0fd2a02961d2a1725c94d0c0f5670c51d5f5f9bad820a96e45791a5d7a32`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 445.5 KB (445476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beba28f927b0599e17785c8f69b8373e61c14da42247f7683f924f80ecae1439`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c54774971cb7c57e8fe14a42f90f7e4cceb67150ff2f3112f9ad46fea390190d`  
		Last Modified: Wed, 22 Jun 2022 04:30:07 GMT  
		Size: 167.5 MB (167492656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:368fa3670d498d9bc0883cd81cf9b9a45d3ccf79365eabe27b779344efefda58`  
		Last Modified: Wed, 22 Jun 2022 04:30:00 GMT  
		Size: 292.0 MB (291982499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb96a08b07f52ad5c126f31fe742e1c114a3239ab5c6fc5641266fa5be00579`  
		Last Modified: Wed, 22 Jun 2022 04:29:42 GMT  
		Size: 2.4 MB (2381172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94af0360a2e049892f0b11539619a1e889f32dcdec1df1a671ffb6032f55437`  
		Last Modified: Wed, 22 Jun 2022 04:29:41 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7255f65a4fc48ef292f0f13fc58a9f76e18f7f3969190698a08ff5907c9e5dd`  
		Last Modified: Wed, 22 Jun 2022 04:29:41 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1695b6d1dbcfb2018bc0a46ec5c66b47f1105c4aff382726932ee462014d294e`  
		Last Modified: Wed, 22 Jun 2022 04:29:41 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec62f61e9a4c7f7d90e61399a76eb18b02a789afbac8e9fcaaa1f8ebc6b10da`  
		Last Modified: Wed, 22 Jun 2022 04:29:41 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:14.4` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:b4d50e1906ede668b41d744d6050b179dc5523658ba13b4e4cc5a92b98955a71
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.9 MB (554912952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed7a93d82de140d630b2eab42fb4270590bb2efcab4d72dd5a2f2dd8ce842278`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:00:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:35:32 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 06:36:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:36:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:36:20 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 10:50:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 10:50:03 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 10:50:04 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 10:50:05 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 10:50:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:50:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:59:13 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 10:59:14 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 01:28:16 GMT
COPY dir:1fb0204bb532a7d63a0dd2d2677d66a70be0285454d27afba6780853636ba1ef in /usr/local/tomcat 
# Fri, 10 Jun 2022 01:28:22 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 01:28:24 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 01:28:25 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 01:28:26 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:24 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:25 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:09:26 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:09:27 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:10:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 22 Jun 2022 04:10:05 GMT
ENV XWIKI_VERSION=14.4.1
# Wed, 22 Jun 2022 04:10:06 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.4.1
# Wed, 22 Jun 2022 04:10:07 GMT
ENV XWIKI_DOWNLOAD_SHA256=8e20eba50acee0f157d3cc160306d65e0995b453833c8923f833030f0a469fb4
# Wed, 22 Jun 2022 04:10:44 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 22 Jun 2022 04:10:45 GMT
ENV MYSQL_JDBC_VERSION=8.0.29
# Wed, 22 Jun 2022 04:10:45 GMT
ENV MYSQL_JDBC_SHA256=d4e32d2a6026b5acc00300b73a86c28fb92681ae9629b21048ee67014c911db6
# Wed, 22 Jun 2022 04:10:46 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.29
# Wed, 22 Jun 2022 04:10:47 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.29.jar
# Wed, 22 Jun 2022 04:10:48 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.29.jar
# Wed, 22 Jun 2022 04:10:50 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Wed, 22 Jun 2022 04:10:51 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 22 Jun 2022 04:10:52 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 22 Jun 2022 04:10:53 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 22 Jun 2022 04:10:54 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 22 Jun 2022 04:10:54 GMT
VOLUME [/usr/local/xwiki]
# Wed, 22 Jun 2022 04:10:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jun 2022 04:10:56 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15da1b4c110f7cc460fbf968fb55b77c541f0e3ab87b92d5e6a822cc2c593e1`  
		Last Modified: Tue, 07 Jun 2022 05:10:23 GMT  
		Size: 15.9 MB (15898299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8e9d6a15d13e6f2d5d43f40b76051350cb7090cfcae5300dc1647e3196577a`  
		Last Modified: Tue, 07 Jun 2022 06:44:15 GMT  
		Size: 41.6 MB (41608356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51219ca7d003431d2f9c6ddda7db0a1902cf2b7e4e879625811b086f268b39c`  
		Last Modified: Tue, 07 Jun 2022 06:44:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5aa4900f44b9e3e20168d54fda3a0b78e62d572de1796db20345b70b1d8b3ca`  
		Last Modified: Tue, 07 Jun 2022 11:23:12 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6796806c88914990f15047665e74a4ea1fb933bdf7b8ebf39b1f2a82b723e044`  
		Last Modified: Fri, 10 Jun 2022 02:03:21 GMT  
		Size: 12.3 MB (12264791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca37469fc5a6ebbc5f1a764aabd4ba48b92a85d1396b644e1139994fad2fa34e`  
		Last Modified: Fri, 10 Jun 2022 02:03:20 GMT  
		Size: 208.8 KB (208841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c24501792b443d8ecb222b1c49c98ee84d4d76016bdbf8ba61b488fa873f7f`  
		Last Modified: Wed, 22 Jun 2022 04:17:01 GMT  
		Size: 163.4 MB (163365370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d1bb494106d6d36bcf7dd967f0d881aa979803343f00918d55f105d5759bbe`  
		Last Modified: Wed, 22 Jun 2022 04:16:59 GMT  
		Size: 292.0 MB (291982622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a24595bb483532afb5982a7102104c4107076a079eeaa4d5fd0d776abe5a1543`  
		Last Modified: Wed, 22 Jun 2022 04:16:38 GMT  
		Size: 2.4 MB (2381177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff7c257d2e413a9084ca6e6cbd963fb66e757d99cd06e3bd96971b96b7ca0083`  
		Last Modified: Wed, 22 Jun 2022 04:16:37 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:343c1e7e3713943da3994aafca00d9f54df0f67fb6b20d86933ebe4a05623d0e`  
		Last Modified: Wed, 22 Jun 2022 04:16:37 GMT  
		Size: 2.3 KB (2309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e0fa83eef81ca126718a8c16fd8f17e6ead2f37ccfc6a8dbf8e2568d221ac0`  
		Last Modified: Wed, 22 Jun 2022 04:16:37 GMT  
		Size: 5.9 KB (5854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c0f8a5973921c322d0333259d28d3c3ab9fa848afe20830fa1aad3fa46743fc`  
		Last Modified: Wed, 22 Jun 2022 04:16:37 GMT  
		Size: 2.5 KB (2509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:14.4-mariadb-tomcat`

```console
$ docker pull xwiki@sha256:3db745735e3f4998cf83b2a5dc35cd5b861564cac0ff1f91425512cc46c054ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:14.4-mariadb-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:5be2c4cf71703a8afc1dc6cd56002d86482ca326367b5a080809603ece9ae80a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.6 MB (560590373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7416cc5f4b70e5175c8fecfe02fb114cdab2e1b5150287649b6d3524c2bcd556`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:14:23 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 00:14:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:58 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:59 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 06:30:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:30:41 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 06:30:41 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:30:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:35:57 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 06:35:58 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 00:18:07 GMT
COPY dir:360b17da945f7a5c4dcdc8b0602904442d98c06d17157280c607532ec8b6edaa in /usr/local/tomcat 
# Fri, 10 Jun 2022 00:18:12 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 00:18:13 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 00:18:13 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 00:18:13 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:25:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 22 Jun 2022 04:25:05 GMT
ENV XWIKI_VERSION=14.4.1
# Wed, 22 Jun 2022 04:25:05 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.4.1
# Wed, 22 Jun 2022 04:25:05 GMT
ENV XWIKI_DOWNLOAD_SHA256=8e20eba50acee0f157d3cc160306d65e0995b453833c8923f833030f0a469fb4
# Wed, 22 Jun 2022 04:25:42 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 22 Jun 2022 04:27:20 GMT
ENV MARIADB_JDBC_VERSION=3.0.5
# Wed, 22 Jun 2022 04:27:20 GMT
ENV MARIADB_JDBC_SHA256=e9532d9bca07c1263c32b00b495bd3ec7f2b79320513cabd762bf39ea09e68d9
# Wed, 22 Jun 2022 04:27:20 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.0.5
# Wed, 22 Jun 2022 04:27:20 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.0.5.jar
# Wed, 22 Jun 2022 04:27:20 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.0.5.jar
# Wed, 22 Jun 2022 04:27:21 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Wed, 22 Jun 2022 04:27:21 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 22 Jun 2022 04:27:21 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 22 Jun 2022 04:27:22 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 22 Jun 2022 04:27:22 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 22 Jun 2022 04:27:22 GMT
VOLUME [/usr/local/xwiki]
# Wed, 22 Jun 2022 04:27:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jun 2022 04:27:22 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b669251e19038a24bd6cab0baab92077f23163880fac4701fb3efa564350732b`  
		Last Modified: Tue, 07 Jun 2022 00:21:34 GMT  
		Size: 43.3 MB (43267270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf45eff8a02bcdf7a96904e0dc534c78c89a5c860e224fa57780ef2fc2eab99e`  
		Last Modified: Tue, 07 Jun 2022 00:21:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246089a07769500a0adb027d1dc0efbb1254ee07d75dcdc6f8a3ceb8bae3e95f`  
		Last Modified: Tue, 07 Jun 2022 06:48:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3636fe8b4383f769da39b4c598b1e98b53b6d528e34e9d20fac5c17cfefcd866`  
		Last Modified: Fri, 10 Jun 2022 00:40:50 GMT  
		Size: 12.2 MB (12247499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0a0fd2a02961d2a1725c94d0c0f5670c51d5f5f9bad820a96e45791a5d7a32`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 445.5 KB (445476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beba28f927b0599e17785c8f69b8373e61c14da42247f7683f924f80ecae1439`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c54774971cb7c57e8fe14a42f90f7e4cceb67150ff2f3112f9ad46fea390190d`  
		Last Modified: Wed, 22 Jun 2022 04:30:07 GMT  
		Size: 167.5 MB (167492656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:368fa3670d498d9bc0883cd81cf9b9a45d3ccf79365eabe27b779344efefda58`  
		Last Modified: Wed, 22 Jun 2022 04:30:00 GMT  
		Size: 292.0 MB (291982499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c1ab918c0e0ec1820084e4da9e0f385f44acb6a9a2c61f37cba3191a960dec1`  
		Last Modified: Wed, 22 Jun 2022 04:31:36 GMT  
		Size: 540.1 KB (540065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2359c2da84be359f352d0435136b09e78a9776b1d22b4dbdd3f6fec942973375`  
		Last Modified: Wed, 22 Jun 2022 04:31:36 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9269ef1e91c8bcc8306aee08c0a04ec885a56ef859428b65c847bec5ddf4d5ce`  
		Last Modified: Wed, 22 Jun 2022 04:31:35 GMT  
		Size: 2.3 KB (2309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b60d3cde6a56696f82809b7ff8a140448d3abe21f2778008cd1c92705cd8cb`  
		Last Modified: Wed, 22 Jun 2022 04:31:35 GMT  
		Size: 5.9 KB (5856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d320a8df62dc7b14288e1ee93b18d239e5ac432d1ac8aab55e511dcbdfbc27`  
		Last Modified: Wed, 22 Jun 2022 04:31:35 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:14.4-mariadb-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:bda93d405e13407149f8f73a5894a9ac80b447f92ade102dcb003d1fbd9e8a7f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **553.1 MB (553071844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ee73663f1cd3949cf5e95503adb5d84ae70153601cd42f36eea35f77b61d0b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:00:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:35:32 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 06:36:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:36:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:36:20 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 10:50:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 10:50:03 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 10:50:04 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 10:50:05 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 10:50:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:50:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:59:13 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 10:59:14 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 01:28:16 GMT
COPY dir:1fb0204bb532a7d63a0dd2d2677d66a70be0285454d27afba6780853636ba1ef in /usr/local/tomcat 
# Fri, 10 Jun 2022 01:28:22 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 01:28:24 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 01:28:25 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 01:28:26 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:24 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:25 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:09:26 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:09:27 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:10:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 22 Jun 2022 04:10:05 GMT
ENV XWIKI_VERSION=14.4.1
# Wed, 22 Jun 2022 04:10:06 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.4.1
# Wed, 22 Jun 2022 04:10:07 GMT
ENV XWIKI_DOWNLOAD_SHA256=8e20eba50acee0f157d3cc160306d65e0995b453833c8923f833030f0a469fb4
# Wed, 22 Jun 2022 04:10:44 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 22 Jun 2022 04:12:47 GMT
ENV MARIADB_JDBC_VERSION=3.0.5
# Wed, 22 Jun 2022 04:12:48 GMT
ENV MARIADB_JDBC_SHA256=e9532d9bca07c1263c32b00b495bd3ec7f2b79320513cabd762bf39ea09e68d9
# Wed, 22 Jun 2022 04:12:49 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.0.5
# Wed, 22 Jun 2022 04:12:50 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.0.5.jar
# Wed, 22 Jun 2022 04:12:51 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.0.5.jar
# Wed, 22 Jun 2022 04:12:53 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Wed, 22 Jun 2022 04:12:54 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 22 Jun 2022 04:12:55 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 22 Jun 2022 04:12:56 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 22 Jun 2022 04:12:57 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 22 Jun 2022 04:12:57 GMT
VOLUME [/usr/local/xwiki]
# Wed, 22 Jun 2022 04:12:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jun 2022 04:12:59 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15da1b4c110f7cc460fbf968fb55b77c541f0e3ab87b92d5e6a822cc2c593e1`  
		Last Modified: Tue, 07 Jun 2022 05:10:23 GMT  
		Size: 15.9 MB (15898299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8e9d6a15d13e6f2d5d43f40b76051350cb7090cfcae5300dc1647e3196577a`  
		Last Modified: Tue, 07 Jun 2022 06:44:15 GMT  
		Size: 41.6 MB (41608356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51219ca7d003431d2f9c6ddda7db0a1902cf2b7e4e879625811b086f268b39c`  
		Last Modified: Tue, 07 Jun 2022 06:44:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5aa4900f44b9e3e20168d54fda3a0b78e62d572de1796db20345b70b1d8b3ca`  
		Last Modified: Tue, 07 Jun 2022 11:23:12 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6796806c88914990f15047665e74a4ea1fb933bdf7b8ebf39b1f2a82b723e044`  
		Last Modified: Fri, 10 Jun 2022 02:03:21 GMT  
		Size: 12.3 MB (12264791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca37469fc5a6ebbc5f1a764aabd4ba48b92a85d1396b644e1139994fad2fa34e`  
		Last Modified: Fri, 10 Jun 2022 02:03:20 GMT  
		Size: 208.8 KB (208841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c24501792b443d8ecb222b1c49c98ee84d4d76016bdbf8ba61b488fa873f7f`  
		Last Modified: Wed, 22 Jun 2022 04:17:01 GMT  
		Size: 163.4 MB (163365370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d1bb494106d6d36bcf7dd967f0d881aa979803343f00918d55f105d5759bbe`  
		Last Modified: Wed, 22 Jun 2022 04:16:59 GMT  
		Size: 292.0 MB (291982622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba0bfc714e56ec603906f85a8dacd34f5dad693a8c6dbcf8a9567fbca423d16`  
		Last Modified: Wed, 22 Jun 2022 04:18:35 GMT  
		Size: 540.1 KB (540069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e192a89ffea555829e044cd56b10c8021a547d8a56e5a69c0a6714bb461f596d`  
		Last Modified: Wed, 22 Jun 2022 04:18:35 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc8a81604a8c8778019d65f20d4893ebf3957eadbc949f6c2ca6a5ede778ba6d`  
		Last Modified: Wed, 22 Jun 2022 04:18:35 GMT  
		Size: 2.3 KB (2311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d62f47e27689a9f1dfc33daa4881e9da0078b7620dbb8c9c520858ac340b8fb4`  
		Last Modified: Wed, 22 Jun 2022 04:18:34 GMT  
		Size: 5.9 KB (5854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:542f6bbdec9617d4401973008c85e7ea003f6f336c453085de1f99098e8911e4`  
		Last Modified: Wed, 22 Jun 2022 04:18:34 GMT  
		Size: 2.5 KB (2507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:14.4-mysql-tomcat`

```console
$ docker pull xwiki@sha256:8b941b575bfdc8c0eb31d9b7f3422c6fe866062a7b465d725d53ec4107ca6144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:14.4-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:f08dab318ed8416b7ef8fc05f68b5c11c7f486d1b4686584b35fbf916cb81081
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.4 MB (562431476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68a5a2c9d16899b288b020a4b618dae8b4a2aa67718272532c3f92b8caca60fd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:14:23 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 00:14:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:58 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:59 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 06:30:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:30:41 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 06:30:41 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:30:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:35:57 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 06:35:58 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 00:18:07 GMT
COPY dir:360b17da945f7a5c4dcdc8b0602904442d98c06d17157280c607532ec8b6edaa in /usr/local/tomcat 
# Fri, 10 Jun 2022 00:18:12 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 00:18:13 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 00:18:13 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 00:18:13 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:25:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 22 Jun 2022 04:25:05 GMT
ENV XWIKI_VERSION=14.4.1
# Wed, 22 Jun 2022 04:25:05 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.4.1
# Wed, 22 Jun 2022 04:25:05 GMT
ENV XWIKI_DOWNLOAD_SHA256=8e20eba50acee0f157d3cc160306d65e0995b453833c8923f833030f0a469fb4
# Wed, 22 Jun 2022 04:25:42 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 22 Jun 2022 04:25:43 GMT
ENV MYSQL_JDBC_VERSION=8.0.29
# Wed, 22 Jun 2022 04:25:43 GMT
ENV MYSQL_JDBC_SHA256=d4e32d2a6026b5acc00300b73a86c28fb92681ae9629b21048ee67014c911db6
# Wed, 22 Jun 2022 04:25:43 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.29
# Wed, 22 Jun 2022 04:25:43 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.29.jar
# Wed, 22 Jun 2022 04:25:44 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.29.jar
# Wed, 22 Jun 2022 04:25:44 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Wed, 22 Jun 2022 04:25:44 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 22 Jun 2022 04:25:44 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 22 Jun 2022 04:25:45 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 22 Jun 2022 04:25:45 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 22 Jun 2022 04:25:45 GMT
VOLUME [/usr/local/xwiki]
# Wed, 22 Jun 2022 04:25:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jun 2022 04:25:45 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b669251e19038a24bd6cab0baab92077f23163880fac4701fb3efa564350732b`  
		Last Modified: Tue, 07 Jun 2022 00:21:34 GMT  
		Size: 43.3 MB (43267270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf45eff8a02bcdf7a96904e0dc534c78c89a5c860e224fa57780ef2fc2eab99e`  
		Last Modified: Tue, 07 Jun 2022 00:21:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246089a07769500a0adb027d1dc0efbb1254ee07d75dcdc6f8a3ceb8bae3e95f`  
		Last Modified: Tue, 07 Jun 2022 06:48:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3636fe8b4383f769da39b4c598b1e98b53b6d528e34e9d20fac5c17cfefcd866`  
		Last Modified: Fri, 10 Jun 2022 00:40:50 GMT  
		Size: 12.2 MB (12247499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0a0fd2a02961d2a1725c94d0c0f5670c51d5f5f9bad820a96e45791a5d7a32`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 445.5 KB (445476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beba28f927b0599e17785c8f69b8373e61c14da42247f7683f924f80ecae1439`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c54774971cb7c57e8fe14a42f90f7e4cceb67150ff2f3112f9ad46fea390190d`  
		Last Modified: Wed, 22 Jun 2022 04:30:07 GMT  
		Size: 167.5 MB (167492656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:368fa3670d498d9bc0883cd81cf9b9a45d3ccf79365eabe27b779344efefda58`  
		Last Modified: Wed, 22 Jun 2022 04:30:00 GMT  
		Size: 292.0 MB (291982499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb96a08b07f52ad5c126f31fe742e1c114a3239ab5c6fc5641266fa5be00579`  
		Last Modified: Wed, 22 Jun 2022 04:29:42 GMT  
		Size: 2.4 MB (2381172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94af0360a2e049892f0b11539619a1e889f32dcdec1df1a671ffb6032f55437`  
		Last Modified: Wed, 22 Jun 2022 04:29:41 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7255f65a4fc48ef292f0f13fc58a9f76e18f7f3969190698a08ff5907c9e5dd`  
		Last Modified: Wed, 22 Jun 2022 04:29:41 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1695b6d1dbcfb2018bc0a46ec5c66b47f1105c4aff382726932ee462014d294e`  
		Last Modified: Wed, 22 Jun 2022 04:29:41 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec62f61e9a4c7f7d90e61399a76eb18b02a789afbac8e9fcaaa1f8ebc6b10da`  
		Last Modified: Wed, 22 Jun 2022 04:29:41 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:14.4-mysql-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:b4d50e1906ede668b41d744d6050b179dc5523658ba13b4e4cc5a92b98955a71
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.9 MB (554912952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed7a93d82de140d630b2eab42fb4270590bb2efcab4d72dd5a2f2dd8ce842278`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:00:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:35:32 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 06:36:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:36:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:36:20 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 10:50:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 10:50:03 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 10:50:04 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 10:50:05 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 10:50:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:50:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:59:13 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 10:59:14 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 01:28:16 GMT
COPY dir:1fb0204bb532a7d63a0dd2d2677d66a70be0285454d27afba6780853636ba1ef in /usr/local/tomcat 
# Fri, 10 Jun 2022 01:28:22 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 01:28:24 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 01:28:25 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 01:28:26 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:24 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:25 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:09:26 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:09:27 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:10:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 22 Jun 2022 04:10:05 GMT
ENV XWIKI_VERSION=14.4.1
# Wed, 22 Jun 2022 04:10:06 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.4.1
# Wed, 22 Jun 2022 04:10:07 GMT
ENV XWIKI_DOWNLOAD_SHA256=8e20eba50acee0f157d3cc160306d65e0995b453833c8923f833030f0a469fb4
# Wed, 22 Jun 2022 04:10:44 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 22 Jun 2022 04:10:45 GMT
ENV MYSQL_JDBC_VERSION=8.0.29
# Wed, 22 Jun 2022 04:10:45 GMT
ENV MYSQL_JDBC_SHA256=d4e32d2a6026b5acc00300b73a86c28fb92681ae9629b21048ee67014c911db6
# Wed, 22 Jun 2022 04:10:46 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.29
# Wed, 22 Jun 2022 04:10:47 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.29.jar
# Wed, 22 Jun 2022 04:10:48 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.29.jar
# Wed, 22 Jun 2022 04:10:50 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Wed, 22 Jun 2022 04:10:51 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 22 Jun 2022 04:10:52 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 22 Jun 2022 04:10:53 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 22 Jun 2022 04:10:54 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 22 Jun 2022 04:10:54 GMT
VOLUME [/usr/local/xwiki]
# Wed, 22 Jun 2022 04:10:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jun 2022 04:10:56 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15da1b4c110f7cc460fbf968fb55b77c541f0e3ab87b92d5e6a822cc2c593e1`  
		Last Modified: Tue, 07 Jun 2022 05:10:23 GMT  
		Size: 15.9 MB (15898299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8e9d6a15d13e6f2d5d43f40b76051350cb7090cfcae5300dc1647e3196577a`  
		Last Modified: Tue, 07 Jun 2022 06:44:15 GMT  
		Size: 41.6 MB (41608356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51219ca7d003431d2f9c6ddda7db0a1902cf2b7e4e879625811b086f268b39c`  
		Last Modified: Tue, 07 Jun 2022 06:44:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5aa4900f44b9e3e20168d54fda3a0b78e62d572de1796db20345b70b1d8b3ca`  
		Last Modified: Tue, 07 Jun 2022 11:23:12 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6796806c88914990f15047665e74a4ea1fb933bdf7b8ebf39b1f2a82b723e044`  
		Last Modified: Fri, 10 Jun 2022 02:03:21 GMT  
		Size: 12.3 MB (12264791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca37469fc5a6ebbc5f1a764aabd4ba48b92a85d1396b644e1139994fad2fa34e`  
		Last Modified: Fri, 10 Jun 2022 02:03:20 GMT  
		Size: 208.8 KB (208841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c24501792b443d8ecb222b1c49c98ee84d4d76016bdbf8ba61b488fa873f7f`  
		Last Modified: Wed, 22 Jun 2022 04:17:01 GMT  
		Size: 163.4 MB (163365370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d1bb494106d6d36bcf7dd967f0d881aa979803343f00918d55f105d5759bbe`  
		Last Modified: Wed, 22 Jun 2022 04:16:59 GMT  
		Size: 292.0 MB (291982622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a24595bb483532afb5982a7102104c4107076a079eeaa4d5fd0d776abe5a1543`  
		Last Modified: Wed, 22 Jun 2022 04:16:38 GMT  
		Size: 2.4 MB (2381177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff7c257d2e413a9084ca6e6cbd963fb66e757d99cd06e3bd96971b96b7ca0083`  
		Last Modified: Wed, 22 Jun 2022 04:16:37 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:343c1e7e3713943da3994aafca00d9f54df0f67fb6b20d86933ebe4a05623d0e`  
		Last Modified: Wed, 22 Jun 2022 04:16:37 GMT  
		Size: 2.3 KB (2309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e0fa83eef81ca126718a8c16fd8f17e6ead2f37ccfc6a8dbf8e2568d221ac0`  
		Last Modified: Wed, 22 Jun 2022 04:16:37 GMT  
		Size: 5.9 KB (5854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c0f8a5973921c322d0333259d28d3c3ab9fa848afe20830fa1aad3fa46743fc`  
		Last Modified: Wed, 22 Jun 2022 04:16:37 GMT  
		Size: 2.5 KB (2509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:14.4-postgres-tomcat`

```console
$ docker pull xwiki@sha256:1fabdb2e4da65c0abe19ecbaf0ff7ee43cfa94d27091c3d5748e8211ff99735d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:14.4-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:be2ec4361ef195cce3e9b320a91b407e3928431c94a7adb57af1f11044876bd6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **561.6 MB (561646591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d6170aaa002127cf799999888c4d5d58bc136c94008910619af04189b3825fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:14:23 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 00:14:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:58 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:59 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 06:30:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:30:41 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 06:30:41 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:30:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:35:57 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 06:35:58 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 00:18:07 GMT
COPY dir:360b17da945f7a5c4dcdc8b0602904442d98c06d17157280c607532ec8b6edaa in /usr/local/tomcat 
# Fri, 10 Jun 2022 00:18:12 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 00:18:13 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 00:18:13 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 00:18:13 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:26:27 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Wed, 22 Jun 2022 04:26:29 GMT
ENV XWIKI_VERSION=14.4.1
# Wed, 22 Jun 2022 04:26:29 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.4.1
# Wed, 22 Jun 2022 04:26:29 GMT
ENV XWIKI_DOWNLOAD_SHA256=8e20eba50acee0f157d3cc160306d65e0995b453833c8923f833030f0a469fb4
# Wed, 22 Jun 2022 04:27:07 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 22 Jun 2022 04:27:08 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Wed, 22 Jun 2022 04:27:08 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 22 Jun 2022 04:27:08 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 22 Jun 2022 04:27:09 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 22 Jun 2022 04:27:09 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 22 Jun 2022 04:27:09 GMT
VOLUME [/usr/local/xwiki]
# Wed, 22 Jun 2022 04:27:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jun 2022 04:27:09 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b669251e19038a24bd6cab0baab92077f23163880fac4701fb3efa564350732b`  
		Last Modified: Tue, 07 Jun 2022 00:21:34 GMT  
		Size: 43.3 MB (43267270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf45eff8a02bcdf7a96904e0dc534c78c89a5c860e224fa57780ef2fc2eab99e`  
		Last Modified: Tue, 07 Jun 2022 00:21:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246089a07769500a0adb027d1dc0efbb1254ee07d75dcdc6f8a3ceb8bae3e95f`  
		Last Modified: Tue, 07 Jun 2022 06:48:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3636fe8b4383f769da39b4c598b1e98b53b6d528e34e9d20fac5c17cfefcd866`  
		Last Modified: Fri, 10 Jun 2022 00:40:50 GMT  
		Size: 12.2 MB (12247499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0a0fd2a02961d2a1725c94d0c0f5670c51d5f5f9bad820a96e45791a5d7a32`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 445.5 KB (445476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beba28f927b0599e17785c8f69b8373e61c14da42247f7683f924f80ecae1439`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:657eec0a2bb289006e136ad46dbd1d85e8ff10712e1477c0fcacb617a19bb242`  
		Last Modified: Wed, 22 Jun 2022 04:31:12 GMT  
		Size: 168.3 MB (168293438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7336ce43765447d78aa2db6c3c2d06f343d8c461acf64bd26ad2da6cdb3802e9`  
		Last Modified: Wed, 22 Jun 2022 04:31:05 GMT  
		Size: 292.0 MB (291982439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed867fb2baa0895487cb447dc1687bb44e7fa6941a1ed692bc25262eb6c8ce84`  
		Last Modified: Wed, 22 Jun 2022 04:30:47 GMT  
		Size: 795.4 KB (795422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffb2ca6524e098e2552dc1ee3c9df3692d579ef2fe4d945c2aefab62c820dfef`  
		Last Modified: Wed, 22 Jun 2022 04:30:46 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7f44840360a683faa6f816201fff0fcc275d3c3c886e55bd98a5b77b283d9f2`  
		Last Modified: Wed, 22 Jun 2022 04:30:46 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea0454030911a4eba98666b0184b8c3241a86aaffd563ef77f78cf31f9103402`  
		Last Modified: Wed, 22 Jun 2022 04:30:46 GMT  
		Size: 5.9 KB (5854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e070314e7d3d33ac915c9e5d8719b2d00e3207754d5b335482a0e76137e50a`  
		Last Modified: Wed, 22 Jun 2022 04:30:46 GMT  
		Size: 2.5 KB (2503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:14.4-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:b3ce0cb6e854ea382295ea6bb0f34559cb20af7194ac7aa73e10036616745688
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.1 MB (554126019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:964c73cc655f5ead167b952f043637ed76a9a1e4fa99f78c8bc52620b48566db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:00:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:35:32 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 06:36:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:36:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:36:20 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 10:50:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 10:50:03 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 10:50:04 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 10:50:05 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 10:50:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:50:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:59:13 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 10:59:14 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 01:28:16 GMT
COPY dir:1fb0204bb532a7d63a0dd2d2677d66a70be0285454d27afba6780853636ba1ef in /usr/local/tomcat 
# Fri, 10 Jun 2022 01:28:22 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 01:28:24 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 01:28:25 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 01:28:26 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:24 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:25 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:09:26 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:09:27 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:11:42 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Wed, 22 Jun 2022 04:11:43 GMT
ENV XWIKI_VERSION=14.4.1
# Wed, 22 Jun 2022 04:11:43 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.4.1
# Wed, 22 Jun 2022 04:11:44 GMT
ENV XWIKI_DOWNLOAD_SHA256=8e20eba50acee0f157d3cc160306d65e0995b453833c8923f833030f0a469fb4
# Wed, 22 Jun 2022 04:12:23 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 22 Jun 2022 04:12:24 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Wed, 22 Jun 2022 04:12:25 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 22 Jun 2022 04:12:26 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 22 Jun 2022 04:12:27 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 22 Jun 2022 04:12:28 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 22 Jun 2022 04:12:28 GMT
VOLUME [/usr/local/xwiki]
# Wed, 22 Jun 2022 04:12:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jun 2022 04:12:30 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15da1b4c110f7cc460fbf968fb55b77c541f0e3ab87b92d5e6a822cc2c593e1`  
		Last Modified: Tue, 07 Jun 2022 05:10:23 GMT  
		Size: 15.9 MB (15898299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8e9d6a15d13e6f2d5d43f40b76051350cb7090cfcae5300dc1647e3196577a`  
		Last Modified: Tue, 07 Jun 2022 06:44:15 GMT  
		Size: 41.6 MB (41608356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51219ca7d003431d2f9c6ddda7db0a1902cf2b7e4e879625811b086f268b39c`  
		Last Modified: Tue, 07 Jun 2022 06:44:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5aa4900f44b9e3e20168d54fda3a0b78e62d572de1796db20345b70b1d8b3ca`  
		Last Modified: Tue, 07 Jun 2022 11:23:12 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6796806c88914990f15047665e74a4ea1fb933bdf7b8ebf39b1f2a82b723e044`  
		Last Modified: Fri, 10 Jun 2022 02:03:21 GMT  
		Size: 12.3 MB (12264791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca37469fc5a6ebbc5f1a764aabd4ba48b92a85d1396b644e1139994fad2fa34e`  
		Last Modified: Fri, 10 Jun 2022 02:03:20 GMT  
		Size: 208.8 KB (208841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbf4753a12af2d02fd26a953119f6843f7e381cfec0d679d92b04b4e4f5a3d6a`  
		Last Modified: Wed, 22 Jun 2022 04:18:08 GMT  
		Size: 164.2 MB (164164156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8735ad3b7140d98c3eedfd5e132b33810f9ccbd2ef89e37d738de84113c7dc92`  
		Last Modified: Wed, 22 Jun 2022 04:18:07 GMT  
		Size: 292.0 MB (291982533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e05d15dcdbfe55730845a86712aea5417820a8fc73ea492391f4bc8773f273c`  
		Last Modified: Wed, 22 Jun 2022 04:17:46 GMT  
		Size: 795.4 KB (795416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ed4588b795d5cf65bf69167563114888c0924eec209d7f1a1f2f78f04f2e42`  
		Last Modified: Wed, 22 Jun 2022 04:17:45 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f537181948e5040a35cd0252682f25858131a6b14dd2a0cc0f8e9d4deb3dff1`  
		Last Modified: Wed, 22 Jun 2022 04:17:45 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f44b9ff69abe9f98824c9cccb73f52b56acccad5bf10bbf6df522ad974eb8fec`  
		Last Modified: Wed, 22 Jun 2022 04:17:45 GMT  
		Size: 5.9 KB (5851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f781c1d839ed0cddf10a24f41ffa5dc32da0de94c89077f83fd5f3cfa0c62ed6`  
		Last Modified: Wed, 22 Jun 2022 04:17:45 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:14.4.1`

```console
$ docker pull xwiki@sha256:8b941b575bfdc8c0eb31d9b7f3422c6fe866062a7b465d725d53ec4107ca6144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:14.4.1` - linux; amd64

```console
$ docker pull xwiki@sha256:f08dab318ed8416b7ef8fc05f68b5c11c7f486d1b4686584b35fbf916cb81081
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.4 MB (562431476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68a5a2c9d16899b288b020a4b618dae8b4a2aa67718272532c3f92b8caca60fd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:14:23 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 00:14:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:58 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:59 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 06:30:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:30:41 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 06:30:41 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:30:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:35:57 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 06:35:58 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 00:18:07 GMT
COPY dir:360b17da945f7a5c4dcdc8b0602904442d98c06d17157280c607532ec8b6edaa in /usr/local/tomcat 
# Fri, 10 Jun 2022 00:18:12 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 00:18:13 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 00:18:13 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 00:18:13 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:25:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 22 Jun 2022 04:25:05 GMT
ENV XWIKI_VERSION=14.4.1
# Wed, 22 Jun 2022 04:25:05 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.4.1
# Wed, 22 Jun 2022 04:25:05 GMT
ENV XWIKI_DOWNLOAD_SHA256=8e20eba50acee0f157d3cc160306d65e0995b453833c8923f833030f0a469fb4
# Wed, 22 Jun 2022 04:25:42 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 22 Jun 2022 04:25:43 GMT
ENV MYSQL_JDBC_VERSION=8.0.29
# Wed, 22 Jun 2022 04:25:43 GMT
ENV MYSQL_JDBC_SHA256=d4e32d2a6026b5acc00300b73a86c28fb92681ae9629b21048ee67014c911db6
# Wed, 22 Jun 2022 04:25:43 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.29
# Wed, 22 Jun 2022 04:25:43 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.29.jar
# Wed, 22 Jun 2022 04:25:44 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.29.jar
# Wed, 22 Jun 2022 04:25:44 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Wed, 22 Jun 2022 04:25:44 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 22 Jun 2022 04:25:44 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 22 Jun 2022 04:25:45 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 22 Jun 2022 04:25:45 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 22 Jun 2022 04:25:45 GMT
VOLUME [/usr/local/xwiki]
# Wed, 22 Jun 2022 04:25:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jun 2022 04:25:45 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b669251e19038a24bd6cab0baab92077f23163880fac4701fb3efa564350732b`  
		Last Modified: Tue, 07 Jun 2022 00:21:34 GMT  
		Size: 43.3 MB (43267270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf45eff8a02bcdf7a96904e0dc534c78c89a5c860e224fa57780ef2fc2eab99e`  
		Last Modified: Tue, 07 Jun 2022 00:21:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246089a07769500a0adb027d1dc0efbb1254ee07d75dcdc6f8a3ceb8bae3e95f`  
		Last Modified: Tue, 07 Jun 2022 06:48:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3636fe8b4383f769da39b4c598b1e98b53b6d528e34e9d20fac5c17cfefcd866`  
		Last Modified: Fri, 10 Jun 2022 00:40:50 GMT  
		Size: 12.2 MB (12247499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0a0fd2a02961d2a1725c94d0c0f5670c51d5f5f9bad820a96e45791a5d7a32`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 445.5 KB (445476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beba28f927b0599e17785c8f69b8373e61c14da42247f7683f924f80ecae1439`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c54774971cb7c57e8fe14a42f90f7e4cceb67150ff2f3112f9ad46fea390190d`  
		Last Modified: Wed, 22 Jun 2022 04:30:07 GMT  
		Size: 167.5 MB (167492656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:368fa3670d498d9bc0883cd81cf9b9a45d3ccf79365eabe27b779344efefda58`  
		Last Modified: Wed, 22 Jun 2022 04:30:00 GMT  
		Size: 292.0 MB (291982499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb96a08b07f52ad5c126f31fe742e1c114a3239ab5c6fc5641266fa5be00579`  
		Last Modified: Wed, 22 Jun 2022 04:29:42 GMT  
		Size: 2.4 MB (2381172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94af0360a2e049892f0b11539619a1e889f32dcdec1df1a671ffb6032f55437`  
		Last Modified: Wed, 22 Jun 2022 04:29:41 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7255f65a4fc48ef292f0f13fc58a9f76e18f7f3969190698a08ff5907c9e5dd`  
		Last Modified: Wed, 22 Jun 2022 04:29:41 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1695b6d1dbcfb2018bc0a46ec5c66b47f1105c4aff382726932ee462014d294e`  
		Last Modified: Wed, 22 Jun 2022 04:29:41 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec62f61e9a4c7f7d90e61399a76eb18b02a789afbac8e9fcaaa1f8ebc6b10da`  
		Last Modified: Wed, 22 Jun 2022 04:29:41 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:14.4.1` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:b4d50e1906ede668b41d744d6050b179dc5523658ba13b4e4cc5a92b98955a71
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.9 MB (554912952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed7a93d82de140d630b2eab42fb4270590bb2efcab4d72dd5a2f2dd8ce842278`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:00:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:35:32 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 06:36:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:36:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:36:20 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 10:50:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 10:50:03 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 10:50:04 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 10:50:05 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 10:50:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:50:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:59:13 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 10:59:14 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 01:28:16 GMT
COPY dir:1fb0204bb532a7d63a0dd2d2677d66a70be0285454d27afba6780853636ba1ef in /usr/local/tomcat 
# Fri, 10 Jun 2022 01:28:22 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 01:28:24 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 01:28:25 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 01:28:26 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:24 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:25 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:09:26 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:09:27 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:10:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 22 Jun 2022 04:10:05 GMT
ENV XWIKI_VERSION=14.4.1
# Wed, 22 Jun 2022 04:10:06 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.4.1
# Wed, 22 Jun 2022 04:10:07 GMT
ENV XWIKI_DOWNLOAD_SHA256=8e20eba50acee0f157d3cc160306d65e0995b453833c8923f833030f0a469fb4
# Wed, 22 Jun 2022 04:10:44 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 22 Jun 2022 04:10:45 GMT
ENV MYSQL_JDBC_VERSION=8.0.29
# Wed, 22 Jun 2022 04:10:45 GMT
ENV MYSQL_JDBC_SHA256=d4e32d2a6026b5acc00300b73a86c28fb92681ae9629b21048ee67014c911db6
# Wed, 22 Jun 2022 04:10:46 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.29
# Wed, 22 Jun 2022 04:10:47 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.29.jar
# Wed, 22 Jun 2022 04:10:48 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.29.jar
# Wed, 22 Jun 2022 04:10:50 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Wed, 22 Jun 2022 04:10:51 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 22 Jun 2022 04:10:52 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 22 Jun 2022 04:10:53 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 22 Jun 2022 04:10:54 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 22 Jun 2022 04:10:54 GMT
VOLUME [/usr/local/xwiki]
# Wed, 22 Jun 2022 04:10:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jun 2022 04:10:56 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15da1b4c110f7cc460fbf968fb55b77c541f0e3ab87b92d5e6a822cc2c593e1`  
		Last Modified: Tue, 07 Jun 2022 05:10:23 GMT  
		Size: 15.9 MB (15898299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8e9d6a15d13e6f2d5d43f40b76051350cb7090cfcae5300dc1647e3196577a`  
		Last Modified: Tue, 07 Jun 2022 06:44:15 GMT  
		Size: 41.6 MB (41608356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51219ca7d003431d2f9c6ddda7db0a1902cf2b7e4e879625811b086f268b39c`  
		Last Modified: Tue, 07 Jun 2022 06:44:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5aa4900f44b9e3e20168d54fda3a0b78e62d572de1796db20345b70b1d8b3ca`  
		Last Modified: Tue, 07 Jun 2022 11:23:12 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6796806c88914990f15047665e74a4ea1fb933bdf7b8ebf39b1f2a82b723e044`  
		Last Modified: Fri, 10 Jun 2022 02:03:21 GMT  
		Size: 12.3 MB (12264791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca37469fc5a6ebbc5f1a764aabd4ba48b92a85d1396b644e1139994fad2fa34e`  
		Last Modified: Fri, 10 Jun 2022 02:03:20 GMT  
		Size: 208.8 KB (208841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c24501792b443d8ecb222b1c49c98ee84d4d76016bdbf8ba61b488fa873f7f`  
		Last Modified: Wed, 22 Jun 2022 04:17:01 GMT  
		Size: 163.4 MB (163365370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d1bb494106d6d36bcf7dd967f0d881aa979803343f00918d55f105d5759bbe`  
		Last Modified: Wed, 22 Jun 2022 04:16:59 GMT  
		Size: 292.0 MB (291982622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a24595bb483532afb5982a7102104c4107076a079eeaa4d5fd0d776abe5a1543`  
		Last Modified: Wed, 22 Jun 2022 04:16:38 GMT  
		Size: 2.4 MB (2381177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff7c257d2e413a9084ca6e6cbd963fb66e757d99cd06e3bd96971b96b7ca0083`  
		Last Modified: Wed, 22 Jun 2022 04:16:37 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:343c1e7e3713943da3994aafca00d9f54df0f67fb6b20d86933ebe4a05623d0e`  
		Last Modified: Wed, 22 Jun 2022 04:16:37 GMT  
		Size: 2.3 KB (2309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e0fa83eef81ca126718a8c16fd8f17e6ead2f37ccfc6a8dbf8e2568d221ac0`  
		Last Modified: Wed, 22 Jun 2022 04:16:37 GMT  
		Size: 5.9 KB (5854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c0f8a5973921c322d0333259d28d3c3ab9fa848afe20830fa1aad3fa46743fc`  
		Last Modified: Wed, 22 Jun 2022 04:16:37 GMT  
		Size: 2.5 KB (2509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:14.4.1-mariadb-tomcat`

```console
$ docker pull xwiki@sha256:3db745735e3f4998cf83b2a5dc35cd5b861564cac0ff1f91425512cc46c054ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:14.4.1-mariadb-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:5be2c4cf71703a8afc1dc6cd56002d86482ca326367b5a080809603ece9ae80a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.6 MB (560590373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7416cc5f4b70e5175c8fecfe02fb114cdab2e1b5150287649b6d3524c2bcd556`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:14:23 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 00:14:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:58 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:59 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 06:30:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:30:41 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 06:30:41 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:30:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:35:57 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 06:35:58 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 00:18:07 GMT
COPY dir:360b17da945f7a5c4dcdc8b0602904442d98c06d17157280c607532ec8b6edaa in /usr/local/tomcat 
# Fri, 10 Jun 2022 00:18:12 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 00:18:13 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 00:18:13 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 00:18:13 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:25:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 22 Jun 2022 04:25:05 GMT
ENV XWIKI_VERSION=14.4.1
# Wed, 22 Jun 2022 04:25:05 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.4.1
# Wed, 22 Jun 2022 04:25:05 GMT
ENV XWIKI_DOWNLOAD_SHA256=8e20eba50acee0f157d3cc160306d65e0995b453833c8923f833030f0a469fb4
# Wed, 22 Jun 2022 04:25:42 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 22 Jun 2022 04:27:20 GMT
ENV MARIADB_JDBC_VERSION=3.0.5
# Wed, 22 Jun 2022 04:27:20 GMT
ENV MARIADB_JDBC_SHA256=e9532d9bca07c1263c32b00b495bd3ec7f2b79320513cabd762bf39ea09e68d9
# Wed, 22 Jun 2022 04:27:20 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.0.5
# Wed, 22 Jun 2022 04:27:20 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.0.5.jar
# Wed, 22 Jun 2022 04:27:20 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.0.5.jar
# Wed, 22 Jun 2022 04:27:21 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Wed, 22 Jun 2022 04:27:21 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 22 Jun 2022 04:27:21 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 22 Jun 2022 04:27:22 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 22 Jun 2022 04:27:22 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 22 Jun 2022 04:27:22 GMT
VOLUME [/usr/local/xwiki]
# Wed, 22 Jun 2022 04:27:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jun 2022 04:27:22 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b669251e19038a24bd6cab0baab92077f23163880fac4701fb3efa564350732b`  
		Last Modified: Tue, 07 Jun 2022 00:21:34 GMT  
		Size: 43.3 MB (43267270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf45eff8a02bcdf7a96904e0dc534c78c89a5c860e224fa57780ef2fc2eab99e`  
		Last Modified: Tue, 07 Jun 2022 00:21:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246089a07769500a0adb027d1dc0efbb1254ee07d75dcdc6f8a3ceb8bae3e95f`  
		Last Modified: Tue, 07 Jun 2022 06:48:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3636fe8b4383f769da39b4c598b1e98b53b6d528e34e9d20fac5c17cfefcd866`  
		Last Modified: Fri, 10 Jun 2022 00:40:50 GMT  
		Size: 12.2 MB (12247499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0a0fd2a02961d2a1725c94d0c0f5670c51d5f5f9bad820a96e45791a5d7a32`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 445.5 KB (445476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beba28f927b0599e17785c8f69b8373e61c14da42247f7683f924f80ecae1439`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c54774971cb7c57e8fe14a42f90f7e4cceb67150ff2f3112f9ad46fea390190d`  
		Last Modified: Wed, 22 Jun 2022 04:30:07 GMT  
		Size: 167.5 MB (167492656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:368fa3670d498d9bc0883cd81cf9b9a45d3ccf79365eabe27b779344efefda58`  
		Last Modified: Wed, 22 Jun 2022 04:30:00 GMT  
		Size: 292.0 MB (291982499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c1ab918c0e0ec1820084e4da9e0f385f44acb6a9a2c61f37cba3191a960dec1`  
		Last Modified: Wed, 22 Jun 2022 04:31:36 GMT  
		Size: 540.1 KB (540065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2359c2da84be359f352d0435136b09e78a9776b1d22b4dbdd3f6fec942973375`  
		Last Modified: Wed, 22 Jun 2022 04:31:36 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9269ef1e91c8bcc8306aee08c0a04ec885a56ef859428b65c847bec5ddf4d5ce`  
		Last Modified: Wed, 22 Jun 2022 04:31:35 GMT  
		Size: 2.3 KB (2309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b60d3cde6a56696f82809b7ff8a140448d3abe21f2778008cd1c92705cd8cb`  
		Last Modified: Wed, 22 Jun 2022 04:31:35 GMT  
		Size: 5.9 KB (5856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d320a8df62dc7b14288e1ee93b18d239e5ac432d1ac8aab55e511dcbdfbc27`  
		Last Modified: Wed, 22 Jun 2022 04:31:35 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:14.4.1-mariadb-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:bda93d405e13407149f8f73a5894a9ac80b447f92ade102dcb003d1fbd9e8a7f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **553.1 MB (553071844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ee73663f1cd3949cf5e95503adb5d84ae70153601cd42f36eea35f77b61d0b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:00:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:35:32 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 06:36:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:36:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:36:20 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 10:50:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 10:50:03 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 10:50:04 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 10:50:05 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 10:50:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:50:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:59:13 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 10:59:14 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 01:28:16 GMT
COPY dir:1fb0204bb532a7d63a0dd2d2677d66a70be0285454d27afba6780853636ba1ef in /usr/local/tomcat 
# Fri, 10 Jun 2022 01:28:22 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 01:28:24 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 01:28:25 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 01:28:26 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:24 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:25 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:09:26 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:09:27 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:10:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 22 Jun 2022 04:10:05 GMT
ENV XWIKI_VERSION=14.4.1
# Wed, 22 Jun 2022 04:10:06 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.4.1
# Wed, 22 Jun 2022 04:10:07 GMT
ENV XWIKI_DOWNLOAD_SHA256=8e20eba50acee0f157d3cc160306d65e0995b453833c8923f833030f0a469fb4
# Wed, 22 Jun 2022 04:10:44 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 22 Jun 2022 04:12:47 GMT
ENV MARIADB_JDBC_VERSION=3.0.5
# Wed, 22 Jun 2022 04:12:48 GMT
ENV MARIADB_JDBC_SHA256=e9532d9bca07c1263c32b00b495bd3ec7f2b79320513cabd762bf39ea09e68d9
# Wed, 22 Jun 2022 04:12:49 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.0.5
# Wed, 22 Jun 2022 04:12:50 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.0.5.jar
# Wed, 22 Jun 2022 04:12:51 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.0.5.jar
# Wed, 22 Jun 2022 04:12:53 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Wed, 22 Jun 2022 04:12:54 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 22 Jun 2022 04:12:55 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 22 Jun 2022 04:12:56 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 22 Jun 2022 04:12:57 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 22 Jun 2022 04:12:57 GMT
VOLUME [/usr/local/xwiki]
# Wed, 22 Jun 2022 04:12:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jun 2022 04:12:59 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15da1b4c110f7cc460fbf968fb55b77c541f0e3ab87b92d5e6a822cc2c593e1`  
		Last Modified: Tue, 07 Jun 2022 05:10:23 GMT  
		Size: 15.9 MB (15898299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8e9d6a15d13e6f2d5d43f40b76051350cb7090cfcae5300dc1647e3196577a`  
		Last Modified: Tue, 07 Jun 2022 06:44:15 GMT  
		Size: 41.6 MB (41608356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51219ca7d003431d2f9c6ddda7db0a1902cf2b7e4e879625811b086f268b39c`  
		Last Modified: Tue, 07 Jun 2022 06:44:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5aa4900f44b9e3e20168d54fda3a0b78e62d572de1796db20345b70b1d8b3ca`  
		Last Modified: Tue, 07 Jun 2022 11:23:12 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6796806c88914990f15047665e74a4ea1fb933bdf7b8ebf39b1f2a82b723e044`  
		Last Modified: Fri, 10 Jun 2022 02:03:21 GMT  
		Size: 12.3 MB (12264791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca37469fc5a6ebbc5f1a764aabd4ba48b92a85d1396b644e1139994fad2fa34e`  
		Last Modified: Fri, 10 Jun 2022 02:03:20 GMT  
		Size: 208.8 KB (208841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c24501792b443d8ecb222b1c49c98ee84d4d76016bdbf8ba61b488fa873f7f`  
		Last Modified: Wed, 22 Jun 2022 04:17:01 GMT  
		Size: 163.4 MB (163365370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d1bb494106d6d36bcf7dd967f0d881aa979803343f00918d55f105d5759bbe`  
		Last Modified: Wed, 22 Jun 2022 04:16:59 GMT  
		Size: 292.0 MB (291982622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba0bfc714e56ec603906f85a8dacd34f5dad693a8c6dbcf8a9567fbca423d16`  
		Last Modified: Wed, 22 Jun 2022 04:18:35 GMT  
		Size: 540.1 KB (540069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e192a89ffea555829e044cd56b10c8021a547d8a56e5a69c0a6714bb461f596d`  
		Last Modified: Wed, 22 Jun 2022 04:18:35 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc8a81604a8c8778019d65f20d4893ebf3957eadbc949f6c2ca6a5ede778ba6d`  
		Last Modified: Wed, 22 Jun 2022 04:18:35 GMT  
		Size: 2.3 KB (2311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d62f47e27689a9f1dfc33daa4881e9da0078b7620dbb8c9c520858ac340b8fb4`  
		Last Modified: Wed, 22 Jun 2022 04:18:34 GMT  
		Size: 5.9 KB (5854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:542f6bbdec9617d4401973008c85e7ea003f6f336c453085de1f99098e8911e4`  
		Last Modified: Wed, 22 Jun 2022 04:18:34 GMT  
		Size: 2.5 KB (2507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:14.4.1-mysql-tomcat`

```console
$ docker pull xwiki@sha256:8b941b575bfdc8c0eb31d9b7f3422c6fe866062a7b465d725d53ec4107ca6144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:14.4.1-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:f08dab318ed8416b7ef8fc05f68b5c11c7f486d1b4686584b35fbf916cb81081
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.4 MB (562431476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68a5a2c9d16899b288b020a4b618dae8b4a2aa67718272532c3f92b8caca60fd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:14:23 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 00:14:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:58 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:59 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 06:30:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:30:41 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 06:30:41 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:30:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:35:57 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 06:35:58 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 00:18:07 GMT
COPY dir:360b17da945f7a5c4dcdc8b0602904442d98c06d17157280c607532ec8b6edaa in /usr/local/tomcat 
# Fri, 10 Jun 2022 00:18:12 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 00:18:13 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 00:18:13 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 00:18:13 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:25:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 22 Jun 2022 04:25:05 GMT
ENV XWIKI_VERSION=14.4.1
# Wed, 22 Jun 2022 04:25:05 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.4.1
# Wed, 22 Jun 2022 04:25:05 GMT
ENV XWIKI_DOWNLOAD_SHA256=8e20eba50acee0f157d3cc160306d65e0995b453833c8923f833030f0a469fb4
# Wed, 22 Jun 2022 04:25:42 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 22 Jun 2022 04:25:43 GMT
ENV MYSQL_JDBC_VERSION=8.0.29
# Wed, 22 Jun 2022 04:25:43 GMT
ENV MYSQL_JDBC_SHA256=d4e32d2a6026b5acc00300b73a86c28fb92681ae9629b21048ee67014c911db6
# Wed, 22 Jun 2022 04:25:43 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.29
# Wed, 22 Jun 2022 04:25:43 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.29.jar
# Wed, 22 Jun 2022 04:25:44 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.29.jar
# Wed, 22 Jun 2022 04:25:44 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Wed, 22 Jun 2022 04:25:44 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 22 Jun 2022 04:25:44 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 22 Jun 2022 04:25:45 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 22 Jun 2022 04:25:45 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 22 Jun 2022 04:25:45 GMT
VOLUME [/usr/local/xwiki]
# Wed, 22 Jun 2022 04:25:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jun 2022 04:25:45 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b669251e19038a24bd6cab0baab92077f23163880fac4701fb3efa564350732b`  
		Last Modified: Tue, 07 Jun 2022 00:21:34 GMT  
		Size: 43.3 MB (43267270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf45eff8a02bcdf7a96904e0dc534c78c89a5c860e224fa57780ef2fc2eab99e`  
		Last Modified: Tue, 07 Jun 2022 00:21:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246089a07769500a0adb027d1dc0efbb1254ee07d75dcdc6f8a3ceb8bae3e95f`  
		Last Modified: Tue, 07 Jun 2022 06:48:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3636fe8b4383f769da39b4c598b1e98b53b6d528e34e9d20fac5c17cfefcd866`  
		Last Modified: Fri, 10 Jun 2022 00:40:50 GMT  
		Size: 12.2 MB (12247499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0a0fd2a02961d2a1725c94d0c0f5670c51d5f5f9bad820a96e45791a5d7a32`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 445.5 KB (445476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beba28f927b0599e17785c8f69b8373e61c14da42247f7683f924f80ecae1439`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c54774971cb7c57e8fe14a42f90f7e4cceb67150ff2f3112f9ad46fea390190d`  
		Last Modified: Wed, 22 Jun 2022 04:30:07 GMT  
		Size: 167.5 MB (167492656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:368fa3670d498d9bc0883cd81cf9b9a45d3ccf79365eabe27b779344efefda58`  
		Last Modified: Wed, 22 Jun 2022 04:30:00 GMT  
		Size: 292.0 MB (291982499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb96a08b07f52ad5c126f31fe742e1c114a3239ab5c6fc5641266fa5be00579`  
		Last Modified: Wed, 22 Jun 2022 04:29:42 GMT  
		Size: 2.4 MB (2381172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94af0360a2e049892f0b11539619a1e889f32dcdec1df1a671ffb6032f55437`  
		Last Modified: Wed, 22 Jun 2022 04:29:41 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7255f65a4fc48ef292f0f13fc58a9f76e18f7f3969190698a08ff5907c9e5dd`  
		Last Modified: Wed, 22 Jun 2022 04:29:41 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1695b6d1dbcfb2018bc0a46ec5c66b47f1105c4aff382726932ee462014d294e`  
		Last Modified: Wed, 22 Jun 2022 04:29:41 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec62f61e9a4c7f7d90e61399a76eb18b02a789afbac8e9fcaaa1f8ebc6b10da`  
		Last Modified: Wed, 22 Jun 2022 04:29:41 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:14.4.1-mysql-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:b4d50e1906ede668b41d744d6050b179dc5523658ba13b4e4cc5a92b98955a71
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.9 MB (554912952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed7a93d82de140d630b2eab42fb4270590bb2efcab4d72dd5a2f2dd8ce842278`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:00:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:35:32 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 06:36:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:36:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:36:20 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 10:50:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 10:50:03 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 10:50:04 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 10:50:05 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 10:50:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:50:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:59:13 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 10:59:14 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 01:28:16 GMT
COPY dir:1fb0204bb532a7d63a0dd2d2677d66a70be0285454d27afba6780853636ba1ef in /usr/local/tomcat 
# Fri, 10 Jun 2022 01:28:22 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 01:28:24 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 01:28:25 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 01:28:26 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:24 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:25 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:09:26 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:09:27 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:10:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 22 Jun 2022 04:10:05 GMT
ENV XWIKI_VERSION=14.4.1
# Wed, 22 Jun 2022 04:10:06 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.4.1
# Wed, 22 Jun 2022 04:10:07 GMT
ENV XWIKI_DOWNLOAD_SHA256=8e20eba50acee0f157d3cc160306d65e0995b453833c8923f833030f0a469fb4
# Wed, 22 Jun 2022 04:10:44 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 22 Jun 2022 04:10:45 GMT
ENV MYSQL_JDBC_VERSION=8.0.29
# Wed, 22 Jun 2022 04:10:45 GMT
ENV MYSQL_JDBC_SHA256=d4e32d2a6026b5acc00300b73a86c28fb92681ae9629b21048ee67014c911db6
# Wed, 22 Jun 2022 04:10:46 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.29
# Wed, 22 Jun 2022 04:10:47 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.29.jar
# Wed, 22 Jun 2022 04:10:48 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.29.jar
# Wed, 22 Jun 2022 04:10:50 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Wed, 22 Jun 2022 04:10:51 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 22 Jun 2022 04:10:52 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 22 Jun 2022 04:10:53 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 22 Jun 2022 04:10:54 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 22 Jun 2022 04:10:54 GMT
VOLUME [/usr/local/xwiki]
# Wed, 22 Jun 2022 04:10:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jun 2022 04:10:56 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15da1b4c110f7cc460fbf968fb55b77c541f0e3ab87b92d5e6a822cc2c593e1`  
		Last Modified: Tue, 07 Jun 2022 05:10:23 GMT  
		Size: 15.9 MB (15898299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8e9d6a15d13e6f2d5d43f40b76051350cb7090cfcae5300dc1647e3196577a`  
		Last Modified: Tue, 07 Jun 2022 06:44:15 GMT  
		Size: 41.6 MB (41608356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51219ca7d003431d2f9c6ddda7db0a1902cf2b7e4e879625811b086f268b39c`  
		Last Modified: Tue, 07 Jun 2022 06:44:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5aa4900f44b9e3e20168d54fda3a0b78e62d572de1796db20345b70b1d8b3ca`  
		Last Modified: Tue, 07 Jun 2022 11:23:12 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6796806c88914990f15047665e74a4ea1fb933bdf7b8ebf39b1f2a82b723e044`  
		Last Modified: Fri, 10 Jun 2022 02:03:21 GMT  
		Size: 12.3 MB (12264791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca37469fc5a6ebbc5f1a764aabd4ba48b92a85d1396b644e1139994fad2fa34e`  
		Last Modified: Fri, 10 Jun 2022 02:03:20 GMT  
		Size: 208.8 KB (208841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c24501792b443d8ecb222b1c49c98ee84d4d76016bdbf8ba61b488fa873f7f`  
		Last Modified: Wed, 22 Jun 2022 04:17:01 GMT  
		Size: 163.4 MB (163365370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d1bb494106d6d36bcf7dd967f0d881aa979803343f00918d55f105d5759bbe`  
		Last Modified: Wed, 22 Jun 2022 04:16:59 GMT  
		Size: 292.0 MB (291982622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a24595bb483532afb5982a7102104c4107076a079eeaa4d5fd0d776abe5a1543`  
		Last Modified: Wed, 22 Jun 2022 04:16:38 GMT  
		Size: 2.4 MB (2381177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff7c257d2e413a9084ca6e6cbd963fb66e757d99cd06e3bd96971b96b7ca0083`  
		Last Modified: Wed, 22 Jun 2022 04:16:37 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:343c1e7e3713943da3994aafca00d9f54df0f67fb6b20d86933ebe4a05623d0e`  
		Last Modified: Wed, 22 Jun 2022 04:16:37 GMT  
		Size: 2.3 KB (2309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e0fa83eef81ca126718a8c16fd8f17e6ead2f37ccfc6a8dbf8e2568d221ac0`  
		Last Modified: Wed, 22 Jun 2022 04:16:37 GMT  
		Size: 5.9 KB (5854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c0f8a5973921c322d0333259d28d3c3ab9fa848afe20830fa1aad3fa46743fc`  
		Last Modified: Wed, 22 Jun 2022 04:16:37 GMT  
		Size: 2.5 KB (2509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:14.4.1-postgres-tomcat`

```console
$ docker pull xwiki@sha256:1fabdb2e4da65c0abe19ecbaf0ff7ee43cfa94d27091c3d5748e8211ff99735d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:14.4.1-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:be2ec4361ef195cce3e9b320a91b407e3928431c94a7adb57af1f11044876bd6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **561.6 MB (561646591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d6170aaa002127cf799999888c4d5d58bc136c94008910619af04189b3825fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:14:23 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 00:14:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:58 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:59 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 06:30:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:30:41 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 06:30:41 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:30:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:35:57 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 06:35:58 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 00:18:07 GMT
COPY dir:360b17da945f7a5c4dcdc8b0602904442d98c06d17157280c607532ec8b6edaa in /usr/local/tomcat 
# Fri, 10 Jun 2022 00:18:12 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 00:18:13 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 00:18:13 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 00:18:13 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:26:27 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Wed, 22 Jun 2022 04:26:29 GMT
ENV XWIKI_VERSION=14.4.1
# Wed, 22 Jun 2022 04:26:29 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.4.1
# Wed, 22 Jun 2022 04:26:29 GMT
ENV XWIKI_DOWNLOAD_SHA256=8e20eba50acee0f157d3cc160306d65e0995b453833c8923f833030f0a469fb4
# Wed, 22 Jun 2022 04:27:07 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 22 Jun 2022 04:27:08 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Wed, 22 Jun 2022 04:27:08 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 22 Jun 2022 04:27:08 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 22 Jun 2022 04:27:09 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 22 Jun 2022 04:27:09 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 22 Jun 2022 04:27:09 GMT
VOLUME [/usr/local/xwiki]
# Wed, 22 Jun 2022 04:27:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jun 2022 04:27:09 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b669251e19038a24bd6cab0baab92077f23163880fac4701fb3efa564350732b`  
		Last Modified: Tue, 07 Jun 2022 00:21:34 GMT  
		Size: 43.3 MB (43267270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf45eff8a02bcdf7a96904e0dc534c78c89a5c860e224fa57780ef2fc2eab99e`  
		Last Modified: Tue, 07 Jun 2022 00:21:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246089a07769500a0adb027d1dc0efbb1254ee07d75dcdc6f8a3ceb8bae3e95f`  
		Last Modified: Tue, 07 Jun 2022 06:48:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3636fe8b4383f769da39b4c598b1e98b53b6d528e34e9d20fac5c17cfefcd866`  
		Last Modified: Fri, 10 Jun 2022 00:40:50 GMT  
		Size: 12.2 MB (12247499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0a0fd2a02961d2a1725c94d0c0f5670c51d5f5f9bad820a96e45791a5d7a32`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 445.5 KB (445476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beba28f927b0599e17785c8f69b8373e61c14da42247f7683f924f80ecae1439`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:657eec0a2bb289006e136ad46dbd1d85e8ff10712e1477c0fcacb617a19bb242`  
		Last Modified: Wed, 22 Jun 2022 04:31:12 GMT  
		Size: 168.3 MB (168293438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7336ce43765447d78aa2db6c3c2d06f343d8c461acf64bd26ad2da6cdb3802e9`  
		Last Modified: Wed, 22 Jun 2022 04:31:05 GMT  
		Size: 292.0 MB (291982439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed867fb2baa0895487cb447dc1687bb44e7fa6941a1ed692bc25262eb6c8ce84`  
		Last Modified: Wed, 22 Jun 2022 04:30:47 GMT  
		Size: 795.4 KB (795422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffb2ca6524e098e2552dc1ee3c9df3692d579ef2fe4d945c2aefab62c820dfef`  
		Last Modified: Wed, 22 Jun 2022 04:30:46 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7f44840360a683faa6f816201fff0fcc275d3c3c886e55bd98a5b77b283d9f2`  
		Last Modified: Wed, 22 Jun 2022 04:30:46 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea0454030911a4eba98666b0184b8c3241a86aaffd563ef77f78cf31f9103402`  
		Last Modified: Wed, 22 Jun 2022 04:30:46 GMT  
		Size: 5.9 KB (5854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e070314e7d3d33ac915c9e5d8719b2d00e3207754d5b335482a0e76137e50a`  
		Last Modified: Wed, 22 Jun 2022 04:30:46 GMT  
		Size: 2.5 KB (2503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:14.4.1-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:b3ce0cb6e854ea382295ea6bb0f34559cb20af7194ac7aa73e10036616745688
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.1 MB (554126019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:964c73cc655f5ead167b952f043637ed76a9a1e4fa99f78c8bc52620b48566db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:00:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:35:32 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 06:36:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:36:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:36:20 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 10:50:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 10:50:03 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 10:50:04 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 10:50:05 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 10:50:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:50:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:59:13 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 10:59:14 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 01:28:16 GMT
COPY dir:1fb0204bb532a7d63a0dd2d2677d66a70be0285454d27afba6780853636ba1ef in /usr/local/tomcat 
# Fri, 10 Jun 2022 01:28:22 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 01:28:24 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 01:28:25 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 01:28:26 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:24 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:25 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:09:26 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:09:27 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:11:42 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Wed, 22 Jun 2022 04:11:43 GMT
ENV XWIKI_VERSION=14.4.1
# Wed, 22 Jun 2022 04:11:43 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.4.1
# Wed, 22 Jun 2022 04:11:44 GMT
ENV XWIKI_DOWNLOAD_SHA256=8e20eba50acee0f157d3cc160306d65e0995b453833c8923f833030f0a469fb4
# Wed, 22 Jun 2022 04:12:23 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 22 Jun 2022 04:12:24 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Wed, 22 Jun 2022 04:12:25 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 22 Jun 2022 04:12:26 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 22 Jun 2022 04:12:27 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 22 Jun 2022 04:12:28 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 22 Jun 2022 04:12:28 GMT
VOLUME [/usr/local/xwiki]
# Wed, 22 Jun 2022 04:12:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jun 2022 04:12:30 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15da1b4c110f7cc460fbf968fb55b77c541f0e3ab87b92d5e6a822cc2c593e1`  
		Last Modified: Tue, 07 Jun 2022 05:10:23 GMT  
		Size: 15.9 MB (15898299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8e9d6a15d13e6f2d5d43f40b76051350cb7090cfcae5300dc1647e3196577a`  
		Last Modified: Tue, 07 Jun 2022 06:44:15 GMT  
		Size: 41.6 MB (41608356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51219ca7d003431d2f9c6ddda7db0a1902cf2b7e4e879625811b086f268b39c`  
		Last Modified: Tue, 07 Jun 2022 06:44:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5aa4900f44b9e3e20168d54fda3a0b78e62d572de1796db20345b70b1d8b3ca`  
		Last Modified: Tue, 07 Jun 2022 11:23:12 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6796806c88914990f15047665e74a4ea1fb933bdf7b8ebf39b1f2a82b723e044`  
		Last Modified: Fri, 10 Jun 2022 02:03:21 GMT  
		Size: 12.3 MB (12264791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca37469fc5a6ebbc5f1a764aabd4ba48b92a85d1396b644e1139994fad2fa34e`  
		Last Modified: Fri, 10 Jun 2022 02:03:20 GMT  
		Size: 208.8 KB (208841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbf4753a12af2d02fd26a953119f6843f7e381cfec0d679d92b04b4e4f5a3d6a`  
		Last Modified: Wed, 22 Jun 2022 04:18:08 GMT  
		Size: 164.2 MB (164164156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8735ad3b7140d98c3eedfd5e132b33810f9ccbd2ef89e37d738de84113c7dc92`  
		Last Modified: Wed, 22 Jun 2022 04:18:07 GMT  
		Size: 292.0 MB (291982533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e05d15dcdbfe55730845a86712aea5417820a8fc73ea492391f4bc8773f273c`  
		Last Modified: Wed, 22 Jun 2022 04:17:46 GMT  
		Size: 795.4 KB (795416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ed4588b795d5cf65bf69167563114888c0924eec209d7f1a1f2f78f04f2e42`  
		Last Modified: Wed, 22 Jun 2022 04:17:45 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f537181948e5040a35cd0252682f25858131a6b14dd2a0cc0f8e9d4deb3dff1`  
		Last Modified: Wed, 22 Jun 2022 04:17:45 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f44b9ff69abe9f98824c9cccb73f52b56acccad5bf10bbf6df522ad974eb8fec`  
		Last Modified: Wed, 22 Jun 2022 04:17:45 GMT  
		Size: 5.9 KB (5851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f781c1d839ed0cddf10a24f41ffa5dc32da0de94c89077f83fd5f3cfa0c62ed6`  
		Last Modified: Wed, 22 Jun 2022 04:17:45 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:latest`

```console
$ docker pull xwiki@sha256:8b941b575bfdc8c0eb31d9b7f3422c6fe866062a7b465d725d53ec4107ca6144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:latest` - linux; amd64

```console
$ docker pull xwiki@sha256:f08dab318ed8416b7ef8fc05f68b5c11c7f486d1b4686584b35fbf916cb81081
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.4 MB (562431476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68a5a2c9d16899b288b020a4b618dae8b4a2aa67718272532c3f92b8caca60fd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:14:23 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 00:14:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:58 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:59 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 06:30:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:30:41 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 06:30:41 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:30:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:35:57 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 06:35:58 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 00:18:07 GMT
COPY dir:360b17da945f7a5c4dcdc8b0602904442d98c06d17157280c607532ec8b6edaa in /usr/local/tomcat 
# Fri, 10 Jun 2022 00:18:12 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 00:18:13 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 00:18:13 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 00:18:13 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:25:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 22 Jun 2022 04:25:05 GMT
ENV XWIKI_VERSION=14.4.1
# Wed, 22 Jun 2022 04:25:05 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.4.1
# Wed, 22 Jun 2022 04:25:05 GMT
ENV XWIKI_DOWNLOAD_SHA256=8e20eba50acee0f157d3cc160306d65e0995b453833c8923f833030f0a469fb4
# Wed, 22 Jun 2022 04:25:42 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 22 Jun 2022 04:25:43 GMT
ENV MYSQL_JDBC_VERSION=8.0.29
# Wed, 22 Jun 2022 04:25:43 GMT
ENV MYSQL_JDBC_SHA256=d4e32d2a6026b5acc00300b73a86c28fb92681ae9629b21048ee67014c911db6
# Wed, 22 Jun 2022 04:25:43 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.29
# Wed, 22 Jun 2022 04:25:43 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.29.jar
# Wed, 22 Jun 2022 04:25:44 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.29.jar
# Wed, 22 Jun 2022 04:25:44 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Wed, 22 Jun 2022 04:25:44 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 22 Jun 2022 04:25:44 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 22 Jun 2022 04:25:45 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 22 Jun 2022 04:25:45 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 22 Jun 2022 04:25:45 GMT
VOLUME [/usr/local/xwiki]
# Wed, 22 Jun 2022 04:25:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jun 2022 04:25:45 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b669251e19038a24bd6cab0baab92077f23163880fac4701fb3efa564350732b`  
		Last Modified: Tue, 07 Jun 2022 00:21:34 GMT  
		Size: 43.3 MB (43267270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf45eff8a02bcdf7a96904e0dc534c78c89a5c860e224fa57780ef2fc2eab99e`  
		Last Modified: Tue, 07 Jun 2022 00:21:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246089a07769500a0adb027d1dc0efbb1254ee07d75dcdc6f8a3ceb8bae3e95f`  
		Last Modified: Tue, 07 Jun 2022 06:48:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3636fe8b4383f769da39b4c598b1e98b53b6d528e34e9d20fac5c17cfefcd866`  
		Last Modified: Fri, 10 Jun 2022 00:40:50 GMT  
		Size: 12.2 MB (12247499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0a0fd2a02961d2a1725c94d0c0f5670c51d5f5f9bad820a96e45791a5d7a32`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 445.5 KB (445476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beba28f927b0599e17785c8f69b8373e61c14da42247f7683f924f80ecae1439`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c54774971cb7c57e8fe14a42f90f7e4cceb67150ff2f3112f9ad46fea390190d`  
		Last Modified: Wed, 22 Jun 2022 04:30:07 GMT  
		Size: 167.5 MB (167492656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:368fa3670d498d9bc0883cd81cf9b9a45d3ccf79365eabe27b779344efefda58`  
		Last Modified: Wed, 22 Jun 2022 04:30:00 GMT  
		Size: 292.0 MB (291982499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb96a08b07f52ad5c126f31fe742e1c114a3239ab5c6fc5641266fa5be00579`  
		Last Modified: Wed, 22 Jun 2022 04:29:42 GMT  
		Size: 2.4 MB (2381172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94af0360a2e049892f0b11539619a1e889f32dcdec1df1a671ffb6032f55437`  
		Last Modified: Wed, 22 Jun 2022 04:29:41 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7255f65a4fc48ef292f0f13fc58a9f76e18f7f3969190698a08ff5907c9e5dd`  
		Last Modified: Wed, 22 Jun 2022 04:29:41 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1695b6d1dbcfb2018bc0a46ec5c66b47f1105c4aff382726932ee462014d294e`  
		Last Modified: Wed, 22 Jun 2022 04:29:41 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec62f61e9a4c7f7d90e61399a76eb18b02a789afbac8e9fcaaa1f8ebc6b10da`  
		Last Modified: Wed, 22 Jun 2022 04:29:41 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:latest` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:b4d50e1906ede668b41d744d6050b179dc5523658ba13b4e4cc5a92b98955a71
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.9 MB (554912952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed7a93d82de140d630b2eab42fb4270590bb2efcab4d72dd5a2f2dd8ce842278`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:00:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:35:32 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 06:36:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:36:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:36:20 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 10:50:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 10:50:03 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 10:50:04 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 10:50:05 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 10:50:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:50:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:59:13 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 10:59:14 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 01:28:16 GMT
COPY dir:1fb0204bb532a7d63a0dd2d2677d66a70be0285454d27afba6780853636ba1ef in /usr/local/tomcat 
# Fri, 10 Jun 2022 01:28:22 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 01:28:24 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 01:28:25 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 01:28:26 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:24 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:25 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:09:26 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:09:27 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:10:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 22 Jun 2022 04:10:05 GMT
ENV XWIKI_VERSION=14.4.1
# Wed, 22 Jun 2022 04:10:06 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.4.1
# Wed, 22 Jun 2022 04:10:07 GMT
ENV XWIKI_DOWNLOAD_SHA256=8e20eba50acee0f157d3cc160306d65e0995b453833c8923f833030f0a469fb4
# Wed, 22 Jun 2022 04:10:44 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 22 Jun 2022 04:10:45 GMT
ENV MYSQL_JDBC_VERSION=8.0.29
# Wed, 22 Jun 2022 04:10:45 GMT
ENV MYSQL_JDBC_SHA256=d4e32d2a6026b5acc00300b73a86c28fb92681ae9629b21048ee67014c911db6
# Wed, 22 Jun 2022 04:10:46 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.29
# Wed, 22 Jun 2022 04:10:47 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.29.jar
# Wed, 22 Jun 2022 04:10:48 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.29.jar
# Wed, 22 Jun 2022 04:10:50 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Wed, 22 Jun 2022 04:10:51 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 22 Jun 2022 04:10:52 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 22 Jun 2022 04:10:53 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 22 Jun 2022 04:10:54 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 22 Jun 2022 04:10:54 GMT
VOLUME [/usr/local/xwiki]
# Wed, 22 Jun 2022 04:10:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jun 2022 04:10:56 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15da1b4c110f7cc460fbf968fb55b77c541f0e3ab87b92d5e6a822cc2c593e1`  
		Last Modified: Tue, 07 Jun 2022 05:10:23 GMT  
		Size: 15.9 MB (15898299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8e9d6a15d13e6f2d5d43f40b76051350cb7090cfcae5300dc1647e3196577a`  
		Last Modified: Tue, 07 Jun 2022 06:44:15 GMT  
		Size: 41.6 MB (41608356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51219ca7d003431d2f9c6ddda7db0a1902cf2b7e4e879625811b086f268b39c`  
		Last Modified: Tue, 07 Jun 2022 06:44:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5aa4900f44b9e3e20168d54fda3a0b78e62d572de1796db20345b70b1d8b3ca`  
		Last Modified: Tue, 07 Jun 2022 11:23:12 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6796806c88914990f15047665e74a4ea1fb933bdf7b8ebf39b1f2a82b723e044`  
		Last Modified: Fri, 10 Jun 2022 02:03:21 GMT  
		Size: 12.3 MB (12264791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca37469fc5a6ebbc5f1a764aabd4ba48b92a85d1396b644e1139994fad2fa34e`  
		Last Modified: Fri, 10 Jun 2022 02:03:20 GMT  
		Size: 208.8 KB (208841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c24501792b443d8ecb222b1c49c98ee84d4d76016bdbf8ba61b488fa873f7f`  
		Last Modified: Wed, 22 Jun 2022 04:17:01 GMT  
		Size: 163.4 MB (163365370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d1bb494106d6d36bcf7dd967f0d881aa979803343f00918d55f105d5759bbe`  
		Last Modified: Wed, 22 Jun 2022 04:16:59 GMT  
		Size: 292.0 MB (291982622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a24595bb483532afb5982a7102104c4107076a079eeaa4d5fd0d776abe5a1543`  
		Last Modified: Wed, 22 Jun 2022 04:16:38 GMT  
		Size: 2.4 MB (2381177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff7c257d2e413a9084ca6e6cbd963fb66e757d99cd06e3bd96971b96b7ca0083`  
		Last Modified: Wed, 22 Jun 2022 04:16:37 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:343c1e7e3713943da3994aafca00d9f54df0f67fb6b20d86933ebe4a05623d0e`  
		Last Modified: Wed, 22 Jun 2022 04:16:37 GMT  
		Size: 2.3 KB (2309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e0fa83eef81ca126718a8c16fd8f17e6ead2f37ccfc6a8dbf8e2568d221ac0`  
		Last Modified: Wed, 22 Jun 2022 04:16:37 GMT  
		Size: 5.9 KB (5854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c0f8a5973921c322d0333259d28d3c3ab9fa848afe20830fa1aad3fa46743fc`  
		Last Modified: Wed, 22 Jun 2022 04:16:37 GMT  
		Size: 2.5 KB (2509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:lts`

```console
$ docker pull xwiki@sha256:538c472ff45f7c146d4cfbf1e7b31fb39f111a3d49287f502a6d2f71777ff333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:lts` - linux; amd64

```console
$ docker pull xwiki@sha256:d6bbb60b487ca00096f55242a245f5d8021e42013dc9a65227548a78a0e39f38
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.1 MB (563089744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce3a4cc5ca40c56b140b6c3abe277f24fb0842adc6ec43651543be6f4ba1e449`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:14:23 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 00:14:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:58 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:59 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 06:30:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:30:41 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 06:30:41 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:30:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:35:57 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 06:35:58 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 00:18:07 GMT
COPY dir:360b17da945f7a5c4dcdc8b0602904442d98c06d17157280c607532ec8b6edaa in /usr/local/tomcat 
# Fri, 10 Jun 2022 00:18:12 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 00:18:13 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 00:18:13 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 00:18:13 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:25:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 24 Jun 2022 03:08:16 GMT
ENV XWIKI_VERSION=13.10.7
# Fri, 24 Jun 2022 03:08:16 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10.7
# Fri, 24 Jun 2022 03:08:16 GMT
ENV XWIKI_DOWNLOAD_SHA256=b886e886ed34e8d7bea8feb2e74e94edb3fb88030f90ab68c7bbc87dcf453d00
# Fri, 24 Jun 2022 03:08:54 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 24 Jun 2022 03:08:54 GMT
ENV MYSQL_JDBC_VERSION=8.0.29
# Fri, 24 Jun 2022 03:08:55 GMT
ENV MYSQL_JDBC_SHA256=d4e32d2a6026b5acc00300b73a86c28fb92681ae9629b21048ee67014c911db6
# Fri, 24 Jun 2022 03:08:55 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.29
# Fri, 24 Jun 2022 03:08:55 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.29.jar
# Fri, 24 Jun 2022 03:08:55 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.29.jar
# Fri, 24 Jun 2022 03:08:56 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 24 Jun 2022 03:08:56 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 24 Jun 2022 03:08:56 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 24 Jun 2022 03:08:56 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 24 Jun 2022 03:08:57 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 24 Jun 2022 03:08:57 GMT
VOLUME [/usr/local/xwiki]
# Fri, 24 Jun 2022 03:08:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jun 2022 03:08:57 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b669251e19038a24bd6cab0baab92077f23163880fac4701fb3efa564350732b`  
		Last Modified: Tue, 07 Jun 2022 00:21:34 GMT  
		Size: 43.3 MB (43267270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf45eff8a02bcdf7a96904e0dc534c78c89a5c860e224fa57780ef2fc2eab99e`  
		Last Modified: Tue, 07 Jun 2022 00:21:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246089a07769500a0adb027d1dc0efbb1254ee07d75dcdc6f8a3ceb8bae3e95f`  
		Last Modified: Tue, 07 Jun 2022 06:48:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3636fe8b4383f769da39b4c598b1e98b53b6d528e34e9d20fac5c17cfefcd866`  
		Last Modified: Fri, 10 Jun 2022 00:40:50 GMT  
		Size: 12.2 MB (12247499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0a0fd2a02961d2a1725c94d0c0f5670c51d5f5f9bad820a96e45791a5d7a32`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 445.5 KB (445476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beba28f927b0599e17785c8f69b8373e61c14da42247f7683f924f80ecae1439`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c54774971cb7c57e8fe14a42f90f7e4cceb67150ff2f3112f9ad46fea390190d`  
		Last Modified: Wed, 22 Jun 2022 04:30:07 GMT  
		Size: 167.5 MB (167492656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f8955940c07caf93c5b3787f4d50541ad84d1a6b710568178150ed29fa8c1fa`  
		Last Modified: Fri, 24 Jun 2022 03:11:53 GMT  
		Size: 292.6 MB (292641283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7511706ae08b48d6c19d83e802574606ae85b91839fd444ed4e26a21afa13cd`  
		Last Modified: Fri, 24 Jun 2022 03:11:35 GMT  
		Size: 2.4 MB (2381172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13635cdd2c775430a870517defaca7b40e34781684ba15c1c4bf4a47a22d7a9f`  
		Last Modified: Fri, 24 Jun 2022 03:11:35 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a6406d38ab58e4a678b831cfa2cf3dc65217dfc73299c135a3c2947cbf288b`  
		Last Modified: Fri, 24 Jun 2022 03:11:35 GMT  
		Size: 2.3 KB (2312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:112f72e7060631567b461a6b28b02795ad282cad23c101738ae01981635a0371`  
		Last Modified: Fri, 24 Jun 2022 03:11:35 GMT  
		Size: 5.3 KB (5338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c054adc9f3f529d9b827670e5c7c0878dd4b56f3f90e919891c04cd198e7bbb`  
		Last Modified: Fri, 24 Jun 2022 03:11:35 GMT  
		Size: 2.5 KB (2501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:lts` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:8239f349f41eb1485f92190c846e889c7c6a069deef3e4810d62b3dca3b5cde9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **555.6 MB (555571284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d7ea8edd21d6b5820cbde3f17f19999ebce9e4ad1f0005dd187c3c77c3f8335`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:00:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:35:32 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 06:36:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:36:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:36:20 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 10:50:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 10:50:03 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 10:50:04 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 10:50:05 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 10:50:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:50:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:59:13 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 10:59:14 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 01:28:16 GMT
COPY dir:1fb0204bb532a7d63a0dd2d2677d66a70be0285454d27afba6780853636ba1ef in /usr/local/tomcat 
# Fri, 10 Jun 2022 01:28:22 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 01:28:24 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 01:28:25 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 01:28:26 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:24 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:25 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:09:26 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:09:27 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:10:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 24 Jun 2022 08:10:35 GMT
ENV XWIKI_VERSION=13.10.7
# Fri, 24 Jun 2022 08:10:35 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10.7
# Fri, 24 Jun 2022 08:10:36 GMT
ENV XWIKI_DOWNLOAD_SHA256=b886e886ed34e8d7bea8feb2e74e94edb3fb88030f90ab68c7bbc87dcf453d00
# Fri, 24 Jun 2022 08:11:07 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 24 Jun 2022 08:11:08 GMT
ENV MYSQL_JDBC_VERSION=8.0.29
# Fri, 24 Jun 2022 08:11:08 GMT
ENV MYSQL_JDBC_SHA256=d4e32d2a6026b5acc00300b73a86c28fb92681ae9629b21048ee67014c911db6
# Fri, 24 Jun 2022 08:11:09 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.29
# Fri, 24 Jun 2022 08:11:10 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.29.jar
# Fri, 24 Jun 2022 08:11:11 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.29.jar
# Fri, 24 Jun 2022 08:11:13 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 24 Jun 2022 08:11:14 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 24 Jun 2022 08:11:15 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 24 Jun 2022 08:11:16 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 24 Jun 2022 08:11:17 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 24 Jun 2022 08:11:17 GMT
VOLUME [/usr/local/xwiki]
# Fri, 24 Jun 2022 08:11:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jun 2022 08:11:19 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15da1b4c110f7cc460fbf968fb55b77c541f0e3ab87b92d5e6a822cc2c593e1`  
		Last Modified: Tue, 07 Jun 2022 05:10:23 GMT  
		Size: 15.9 MB (15898299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8e9d6a15d13e6f2d5d43f40b76051350cb7090cfcae5300dc1647e3196577a`  
		Last Modified: Tue, 07 Jun 2022 06:44:15 GMT  
		Size: 41.6 MB (41608356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51219ca7d003431d2f9c6ddda7db0a1902cf2b7e4e879625811b086f268b39c`  
		Last Modified: Tue, 07 Jun 2022 06:44:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5aa4900f44b9e3e20168d54fda3a0b78e62d572de1796db20345b70b1d8b3ca`  
		Last Modified: Tue, 07 Jun 2022 11:23:12 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6796806c88914990f15047665e74a4ea1fb933bdf7b8ebf39b1f2a82b723e044`  
		Last Modified: Fri, 10 Jun 2022 02:03:21 GMT  
		Size: 12.3 MB (12264791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca37469fc5a6ebbc5f1a764aabd4ba48b92a85d1396b644e1139994fad2fa34e`  
		Last Modified: Fri, 10 Jun 2022 02:03:20 GMT  
		Size: 208.8 KB (208841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c24501792b443d8ecb222b1c49c98ee84d4d76016bdbf8ba61b488fa873f7f`  
		Last Modified: Wed, 22 Jun 2022 04:17:01 GMT  
		Size: 163.4 MB (163365370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d4c4674e614cb6318120b7f3b95cc0f15a199054f449c2735cf25af9e2fd68`  
		Last Modified: Fri, 24 Jun 2022 08:14:37 GMT  
		Size: 292.6 MB (292641477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f45433cd06ad26dbb57afb98818c085a9ba114157cc72fa70214f8949e3ccfc`  
		Last Modified: Fri, 24 Jun 2022 08:14:15 GMT  
		Size: 2.4 MB (2381180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f75bf932706df5ca8d04fa02d8711685191f1f1dd7deb53937ba6f1371cb7fc5`  
		Last Modified: Fri, 24 Jun 2022 08:14:14 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04bce02a10640eb0a28ea0cd65126f65a6425540f18bd2acd881ed919828c057`  
		Last Modified: Fri, 24 Jun 2022 08:14:14 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:258f35d21774001fddc3b61192c74e053da90db66513a55c26d096b10ee59564`  
		Last Modified: Fri, 24 Jun 2022 08:14:14 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b877bc26e0f91fafb0bcbe8b609880d5c9cfba95b167970bae7650e06a31d706`  
		Last Modified: Fri, 24 Jun 2022 08:14:14 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:lts-mariadb`

```console
$ docker pull xwiki@sha256:7e992a39803f1553703a95e1c243d3e530a70c492c48ce9f4721f3c0cac22740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:lts-mariadb` - linux; amd64

```console
$ docker pull xwiki@sha256:fe68d60e91e8d3eb0e5d23a11eb5b888b7350043a1edc71fd12266ce62957ac7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **561.2 MB (561248650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c580180cdf614c4e58b233442d12859c0c06fb61a5c351ff96835ef123570549`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:14:23 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 00:14:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:58 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:59 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 06:30:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:30:41 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 06:30:41 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:30:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:35:57 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 06:35:58 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 00:18:07 GMT
COPY dir:360b17da945f7a5c4dcdc8b0602904442d98c06d17157280c607532ec8b6edaa in /usr/local/tomcat 
# Fri, 10 Jun 2022 00:18:12 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 00:18:13 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 00:18:13 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 00:18:13 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:25:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 24 Jun 2022 03:08:16 GMT
ENV XWIKI_VERSION=13.10.7
# Fri, 24 Jun 2022 03:08:16 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10.7
# Fri, 24 Jun 2022 03:08:16 GMT
ENV XWIKI_DOWNLOAD_SHA256=b886e886ed34e8d7bea8feb2e74e94edb3fb88030f90ab68c7bbc87dcf453d00
# Fri, 24 Jun 2022 03:08:54 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 24 Jun 2022 03:10:42 GMT
ENV MARIADB_JDBC_VERSION=3.0.5
# Fri, 24 Jun 2022 03:10:42 GMT
ENV MARIADB_JDBC_SHA256=e9532d9bca07c1263c32b00b495bd3ec7f2b79320513cabd762bf39ea09e68d9
# Fri, 24 Jun 2022 03:10:43 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.0.5
# Fri, 24 Jun 2022 03:10:43 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.0.5.jar
# Fri, 24 Jun 2022 03:10:43 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.0.5.jar
# Fri, 24 Jun 2022 03:10:43 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Fri, 24 Jun 2022 03:10:44 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 24 Jun 2022 03:10:44 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 24 Jun 2022 03:10:44 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 24 Jun 2022 03:10:44 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 24 Jun 2022 03:10:44 GMT
VOLUME [/usr/local/xwiki]
# Fri, 24 Jun 2022 03:10:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jun 2022 03:10:45 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b669251e19038a24bd6cab0baab92077f23163880fac4701fb3efa564350732b`  
		Last Modified: Tue, 07 Jun 2022 00:21:34 GMT  
		Size: 43.3 MB (43267270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf45eff8a02bcdf7a96904e0dc534c78c89a5c860e224fa57780ef2fc2eab99e`  
		Last Modified: Tue, 07 Jun 2022 00:21:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246089a07769500a0adb027d1dc0efbb1254ee07d75dcdc6f8a3ceb8bae3e95f`  
		Last Modified: Tue, 07 Jun 2022 06:48:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3636fe8b4383f769da39b4c598b1e98b53b6d528e34e9d20fac5c17cfefcd866`  
		Last Modified: Fri, 10 Jun 2022 00:40:50 GMT  
		Size: 12.2 MB (12247499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0a0fd2a02961d2a1725c94d0c0f5670c51d5f5f9bad820a96e45791a5d7a32`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 445.5 KB (445476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beba28f927b0599e17785c8f69b8373e61c14da42247f7683f924f80ecae1439`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c54774971cb7c57e8fe14a42f90f7e4cceb67150ff2f3112f9ad46fea390190d`  
		Last Modified: Wed, 22 Jun 2022 04:30:07 GMT  
		Size: 167.5 MB (167492656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f8955940c07caf93c5b3787f4d50541ad84d1a6b710568178150ed29fa8c1fa`  
		Last Modified: Fri, 24 Jun 2022 03:11:53 GMT  
		Size: 292.6 MB (292641283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39e75aa0ee70148e023225e5c15afe6370fae11ad20051cbdc9ad36c048410cb`  
		Last Modified: Fri, 24 Jun 2022 03:13:09 GMT  
		Size: 540.1 KB (540074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a78e618b05c2bd943951d754b0495482861f717b916017efa2d775bd91113d07`  
		Last Modified: Fri, 24 Jun 2022 03:13:08 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77f7e7cac8551052ca6034a6b13460c7245751fa15ed047622af1e3a4bdf80e0`  
		Last Modified: Fri, 24 Jun 2022 03:13:08 GMT  
		Size: 2.3 KB (2313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ac5252f40483fbc8e8acc62ff8428fe4b47a3a203ef6412edda8b83a0bfea19`  
		Last Modified: Fri, 24 Jun 2022 03:13:08 GMT  
		Size: 5.3 KB (5339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea840c472b11a8abe56d67979ba671ee677a5046199e8f29afff0c3f9b6871a`  
		Last Modified: Fri, 24 Jun 2022 03:13:08 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:lts-mariadb` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:f69b33053370bb439577df2ccf0307fb2b1e92e7ad2e3000e27165d0508ce769
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **553.7 MB (553730176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77e99996ea02f728cd4df08569f2a56128eb95625ce333da516f87ca24dfb42d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:00:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:35:32 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 06:36:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:36:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:36:20 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 10:50:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 10:50:03 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 10:50:04 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 10:50:05 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 10:50:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:50:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:59:13 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 10:59:14 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 01:28:16 GMT
COPY dir:1fb0204bb532a7d63a0dd2d2677d66a70be0285454d27afba6780853636ba1ef in /usr/local/tomcat 
# Fri, 10 Jun 2022 01:28:22 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 01:28:24 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 01:28:25 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 01:28:26 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:24 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:25 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:09:26 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:09:27 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:10:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 24 Jun 2022 08:10:35 GMT
ENV XWIKI_VERSION=13.10.7
# Fri, 24 Jun 2022 08:10:35 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10.7
# Fri, 24 Jun 2022 08:10:36 GMT
ENV XWIKI_DOWNLOAD_SHA256=b886e886ed34e8d7bea8feb2e74e94edb3fb88030f90ab68c7bbc87dcf453d00
# Fri, 24 Jun 2022 08:11:07 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 24 Jun 2022 08:12:29 GMT
ENV MARIADB_JDBC_VERSION=3.0.5
# Fri, 24 Jun 2022 08:12:30 GMT
ENV MARIADB_JDBC_SHA256=e9532d9bca07c1263c32b00b495bd3ec7f2b79320513cabd762bf39ea09e68d9
# Fri, 24 Jun 2022 08:12:31 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.0.5
# Fri, 24 Jun 2022 08:12:32 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.0.5.jar
# Fri, 24 Jun 2022 08:12:33 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.0.5.jar
# Fri, 24 Jun 2022 08:12:35 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Fri, 24 Jun 2022 08:12:36 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 24 Jun 2022 08:12:37 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 24 Jun 2022 08:12:38 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 24 Jun 2022 08:12:39 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 24 Jun 2022 08:12:39 GMT
VOLUME [/usr/local/xwiki]
# Fri, 24 Jun 2022 08:12:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jun 2022 08:12:41 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15da1b4c110f7cc460fbf968fb55b77c541f0e3ab87b92d5e6a822cc2c593e1`  
		Last Modified: Tue, 07 Jun 2022 05:10:23 GMT  
		Size: 15.9 MB (15898299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8e9d6a15d13e6f2d5d43f40b76051350cb7090cfcae5300dc1647e3196577a`  
		Last Modified: Tue, 07 Jun 2022 06:44:15 GMT  
		Size: 41.6 MB (41608356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51219ca7d003431d2f9c6ddda7db0a1902cf2b7e4e879625811b086f268b39c`  
		Last Modified: Tue, 07 Jun 2022 06:44:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5aa4900f44b9e3e20168d54fda3a0b78e62d572de1796db20345b70b1d8b3ca`  
		Last Modified: Tue, 07 Jun 2022 11:23:12 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6796806c88914990f15047665e74a4ea1fb933bdf7b8ebf39b1f2a82b723e044`  
		Last Modified: Fri, 10 Jun 2022 02:03:21 GMT  
		Size: 12.3 MB (12264791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca37469fc5a6ebbc5f1a764aabd4ba48b92a85d1396b644e1139994fad2fa34e`  
		Last Modified: Fri, 10 Jun 2022 02:03:20 GMT  
		Size: 208.8 KB (208841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c24501792b443d8ecb222b1c49c98ee84d4d76016bdbf8ba61b488fa873f7f`  
		Last Modified: Wed, 22 Jun 2022 04:17:01 GMT  
		Size: 163.4 MB (163365370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d4c4674e614cb6318120b7f3b95cc0f15a199054f449c2735cf25af9e2fd68`  
		Last Modified: Fri, 24 Jun 2022 08:14:37 GMT  
		Size: 292.6 MB (292641477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55eb49c20075c8f6f6c3474817337eac98d5ecd1d220ca225ede5b5d516ea478`  
		Last Modified: Fri, 24 Jun 2022 08:15:59 GMT  
		Size: 540.1 KB (540068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52ab0fc86a347634df62c569c68f1d90c68af8888bfd6761815c0dc42be1d9e3`  
		Last Modified: Fri, 24 Jun 2022 08:15:58 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:905cc4a353cba057e2dd9dd80f2a18dab3caf4cd39fc0fe50c6e5963c5ea3e55`  
		Last Modified: Fri, 24 Jun 2022 08:15:58 GMT  
		Size: 2.3 KB (2310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7cc5bcac189f250a4bf9f37357b4a4cadc7fc132044e958bcd14c24d26736ec`  
		Last Modified: Fri, 24 Jun 2022 08:15:58 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743fadc0e05f56a8caa0b29a7c3b8fddddca135a6fce4bd23eab3167966f8e5d`  
		Last Modified: Fri, 24 Jun 2022 08:15:58 GMT  
		Size: 2.5 KB (2507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:lts-mariadb-tomcat`

```console
$ docker pull xwiki@sha256:7e992a39803f1553703a95e1c243d3e530a70c492c48ce9f4721f3c0cac22740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:lts-mariadb-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:fe68d60e91e8d3eb0e5d23a11eb5b888b7350043a1edc71fd12266ce62957ac7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **561.2 MB (561248650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c580180cdf614c4e58b233442d12859c0c06fb61a5c351ff96835ef123570549`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:14:23 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 00:14:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:58 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:59 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 06:30:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:30:41 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 06:30:41 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:30:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:35:57 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 06:35:58 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 00:18:07 GMT
COPY dir:360b17da945f7a5c4dcdc8b0602904442d98c06d17157280c607532ec8b6edaa in /usr/local/tomcat 
# Fri, 10 Jun 2022 00:18:12 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 00:18:13 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 00:18:13 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 00:18:13 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:25:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 24 Jun 2022 03:08:16 GMT
ENV XWIKI_VERSION=13.10.7
# Fri, 24 Jun 2022 03:08:16 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10.7
# Fri, 24 Jun 2022 03:08:16 GMT
ENV XWIKI_DOWNLOAD_SHA256=b886e886ed34e8d7bea8feb2e74e94edb3fb88030f90ab68c7bbc87dcf453d00
# Fri, 24 Jun 2022 03:08:54 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 24 Jun 2022 03:10:42 GMT
ENV MARIADB_JDBC_VERSION=3.0.5
# Fri, 24 Jun 2022 03:10:42 GMT
ENV MARIADB_JDBC_SHA256=e9532d9bca07c1263c32b00b495bd3ec7f2b79320513cabd762bf39ea09e68d9
# Fri, 24 Jun 2022 03:10:43 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.0.5
# Fri, 24 Jun 2022 03:10:43 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.0.5.jar
# Fri, 24 Jun 2022 03:10:43 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.0.5.jar
# Fri, 24 Jun 2022 03:10:43 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Fri, 24 Jun 2022 03:10:44 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 24 Jun 2022 03:10:44 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 24 Jun 2022 03:10:44 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 24 Jun 2022 03:10:44 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 24 Jun 2022 03:10:44 GMT
VOLUME [/usr/local/xwiki]
# Fri, 24 Jun 2022 03:10:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jun 2022 03:10:45 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b669251e19038a24bd6cab0baab92077f23163880fac4701fb3efa564350732b`  
		Last Modified: Tue, 07 Jun 2022 00:21:34 GMT  
		Size: 43.3 MB (43267270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf45eff8a02bcdf7a96904e0dc534c78c89a5c860e224fa57780ef2fc2eab99e`  
		Last Modified: Tue, 07 Jun 2022 00:21:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246089a07769500a0adb027d1dc0efbb1254ee07d75dcdc6f8a3ceb8bae3e95f`  
		Last Modified: Tue, 07 Jun 2022 06:48:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3636fe8b4383f769da39b4c598b1e98b53b6d528e34e9d20fac5c17cfefcd866`  
		Last Modified: Fri, 10 Jun 2022 00:40:50 GMT  
		Size: 12.2 MB (12247499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0a0fd2a02961d2a1725c94d0c0f5670c51d5f5f9bad820a96e45791a5d7a32`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 445.5 KB (445476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beba28f927b0599e17785c8f69b8373e61c14da42247f7683f924f80ecae1439`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c54774971cb7c57e8fe14a42f90f7e4cceb67150ff2f3112f9ad46fea390190d`  
		Last Modified: Wed, 22 Jun 2022 04:30:07 GMT  
		Size: 167.5 MB (167492656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f8955940c07caf93c5b3787f4d50541ad84d1a6b710568178150ed29fa8c1fa`  
		Last Modified: Fri, 24 Jun 2022 03:11:53 GMT  
		Size: 292.6 MB (292641283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39e75aa0ee70148e023225e5c15afe6370fae11ad20051cbdc9ad36c048410cb`  
		Last Modified: Fri, 24 Jun 2022 03:13:09 GMT  
		Size: 540.1 KB (540074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a78e618b05c2bd943951d754b0495482861f717b916017efa2d775bd91113d07`  
		Last Modified: Fri, 24 Jun 2022 03:13:08 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77f7e7cac8551052ca6034a6b13460c7245751fa15ed047622af1e3a4bdf80e0`  
		Last Modified: Fri, 24 Jun 2022 03:13:08 GMT  
		Size: 2.3 KB (2313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ac5252f40483fbc8e8acc62ff8428fe4b47a3a203ef6412edda8b83a0bfea19`  
		Last Modified: Fri, 24 Jun 2022 03:13:08 GMT  
		Size: 5.3 KB (5339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea840c472b11a8abe56d67979ba671ee677a5046199e8f29afff0c3f9b6871a`  
		Last Modified: Fri, 24 Jun 2022 03:13:08 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:lts-mariadb-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:f69b33053370bb439577df2ccf0307fb2b1e92e7ad2e3000e27165d0508ce769
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **553.7 MB (553730176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77e99996ea02f728cd4df08569f2a56128eb95625ce333da516f87ca24dfb42d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:00:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:35:32 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 06:36:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:36:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:36:20 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 10:50:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 10:50:03 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 10:50:04 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 10:50:05 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 10:50:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:50:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:59:13 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 10:59:14 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 01:28:16 GMT
COPY dir:1fb0204bb532a7d63a0dd2d2677d66a70be0285454d27afba6780853636ba1ef in /usr/local/tomcat 
# Fri, 10 Jun 2022 01:28:22 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 01:28:24 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 01:28:25 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 01:28:26 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:24 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:25 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:09:26 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:09:27 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:10:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 24 Jun 2022 08:10:35 GMT
ENV XWIKI_VERSION=13.10.7
# Fri, 24 Jun 2022 08:10:35 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10.7
# Fri, 24 Jun 2022 08:10:36 GMT
ENV XWIKI_DOWNLOAD_SHA256=b886e886ed34e8d7bea8feb2e74e94edb3fb88030f90ab68c7bbc87dcf453d00
# Fri, 24 Jun 2022 08:11:07 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 24 Jun 2022 08:12:29 GMT
ENV MARIADB_JDBC_VERSION=3.0.5
# Fri, 24 Jun 2022 08:12:30 GMT
ENV MARIADB_JDBC_SHA256=e9532d9bca07c1263c32b00b495bd3ec7f2b79320513cabd762bf39ea09e68d9
# Fri, 24 Jun 2022 08:12:31 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.0.5
# Fri, 24 Jun 2022 08:12:32 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.0.5.jar
# Fri, 24 Jun 2022 08:12:33 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.0.5.jar
# Fri, 24 Jun 2022 08:12:35 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Fri, 24 Jun 2022 08:12:36 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 24 Jun 2022 08:12:37 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 24 Jun 2022 08:12:38 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 24 Jun 2022 08:12:39 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 24 Jun 2022 08:12:39 GMT
VOLUME [/usr/local/xwiki]
# Fri, 24 Jun 2022 08:12:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jun 2022 08:12:41 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15da1b4c110f7cc460fbf968fb55b77c541f0e3ab87b92d5e6a822cc2c593e1`  
		Last Modified: Tue, 07 Jun 2022 05:10:23 GMT  
		Size: 15.9 MB (15898299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8e9d6a15d13e6f2d5d43f40b76051350cb7090cfcae5300dc1647e3196577a`  
		Last Modified: Tue, 07 Jun 2022 06:44:15 GMT  
		Size: 41.6 MB (41608356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51219ca7d003431d2f9c6ddda7db0a1902cf2b7e4e879625811b086f268b39c`  
		Last Modified: Tue, 07 Jun 2022 06:44:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5aa4900f44b9e3e20168d54fda3a0b78e62d572de1796db20345b70b1d8b3ca`  
		Last Modified: Tue, 07 Jun 2022 11:23:12 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6796806c88914990f15047665e74a4ea1fb933bdf7b8ebf39b1f2a82b723e044`  
		Last Modified: Fri, 10 Jun 2022 02:03:21 GMT  
		Size: 12.3 MB (12264791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca37469fc5a6ebbc5f1a764aabd4ba48b92a85d1396b644e1139994fad2fa34e`  
		Last Modified: Fri, 10 Jun 2022 02:03:20 GMT  
		Size: 208.8 KB (208841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c24501792b443d8ecb222b1c49c98ee84d4d76016bdbf8ba61b488fa873f7f`  
		Last Modified: Wed, 22 Jun 2022 04:17:01 GMT  
		Size: 163.4 MB (163365370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d4c4674e614cb6318120b7f3b95cc0f15a199054f449c2735cf25af9e2fd68`  
		Last Modified: Fri, 24 Jun 2022 08:14:37 GMT  
		Size: 292.6 MB (292641477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55eb49c20075c8f6f6c3474817337eac98d5ecd1d220ca225ede5b5d516ea478`  
		Last Modified: Fri, 24 Jun 2022 08:15:59 GMT  
		Size: 540.1 KB (540068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52ab0fc86a347634df62c569c68f1d90c68af8888bfd6761815c0dc42be1d9e3`  
		Last Modified: Fri, 24 Jun 2022 08:15:58 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:905cc4a353cba057e2dd9dd80f2a18dab3caf4cd39fc0fe50c6e5963c5ea3e55`  
		Last Modified: Fri, 24 Jun 2022 08:15:58 GMT  
		Size: 2.3 KB (2310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7cc5bcac189f250a4bf9f37357b4a4cadc7fc132044e958bcd14c24d26736ec`  
		Last Modified: Fri, 24 Jun 2022 08:15:58 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743fadc0e05f56a8caa0b29a7c3b8fddddca135a6fce4bd23eab3167966f8e5d`  
		Last Modified: Fri, 24 Jun 2022 08:15:58 GMT  
		Size: 2.5 KB (2507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:lts-mysql`

```console
$ docker pull xwiki@sha256:538c472ff45f7c146d4cfbf1e7b31fb39f111a3d49287f502a6d2f71777ff333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:lts-mysql` - linux; amd64

```console
$ docker pull xwiki@sha256:d6bbb60b487ca00096f55242a245f5d8021e42013dc9a65227548a78a0e39f38
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.1 MB (563089744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce3a4cc5ca40c56b140b6c3abe277f24fb0842adc6ec43651543be6f4ba1e449`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:14:23 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 00:14:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:58 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:59 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 06:30:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:30:41 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 06:30:41 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:30:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:35:57 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 06:35:58 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 00:18:07 GMT
COPY dir:360b17da945f7a5c4dcdc8b0602904442d98c06d17157280c607532ec8b6edaa in /usr/local/tomcat 
# Fri, 10 Jun 2022 00:18:12 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 00:18:13 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 00:18:13 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 00:18:13 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:25:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 24 Jun 2022 03:08:16 GMT
ENV XWIKI_VERSION=13.10.7
# Fri, 24 Jun 2022 03:08:16 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10.7
# Fri, 24 Jun 2022 03:08:16 GMT
ENV XWIKI_DOWNLOAD_SHA256=b886e886ed34e8d7bea8feb2e74e94edb3fb88030f90ab68c7bbc87dcf453d00
# Fri, 24 Jun 2022 03:08:54 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 24 Jun 2022 03:08:54 GMT
ENV MYSQL_JDBC_VERSION=8.0.29
# Fri, 24 Jun 2022 03:08:55 GMT
ENV MYSQL_JDBC_SHA256=d4e32d2a6026b5acc00300b73a86c28fb92681ae9629b21048ee67014c911db6
# Fri, 24 Jun 2022 03:08:55 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.29
# Fri, 24 Jun 2022 03:08:55 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.29.jar
# Fri, 24 Jun 2022 03:08:55 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.29.jar
# Fri, 24 Jun 2022 03:08:56 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 24 Jun 2022 03:08:56 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 24 Jun 2022 03:08:56 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 24 Jun 2022 03:08:56 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 24 Jun 2022 03:08:57 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 24 Jun 2022 03:08:57 GMT
VOLUME [/usr/local/xwiki]
# Fri, 24 Jun 2022 03:08:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jun 2022 03:08:57 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b669251e19038a24bd6cab0baab92077f23163880fac4701fb3efa564350732b`  
		Last Modified: Tue, 07 Jun 2022 00:21:34 GMT  
		Size: 43.3 MB (43267270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf45eff8a02bcdf7a96904e0dc534c78c89a5c860e224fa57780ef2fc2eab99e`  
		Last Modified: Tue, 07 Jun 2022 00:21:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246089a07769500a0adb027d1dc0efbb1254ee07d75dcdc6f8a3ceb8bae3e95f`  
		Last Modified: Tue, 07 Jun 2022 06:48:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3636fe8b4383f769da39b4c598b1e98b53b6d528e34e9d20fac5c17cfefcd866`  
		Last Modified: Fri, 10 Jun 2022 00:40:50 GMT  
		Size: 12.2 MB (12247499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0a0fd2a02961d2a1725c94d0c0f5670c51d5f5f9bad820a96e45791a5d7a32`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 445.5 KB (445476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beba28f927b0599e17785c8f69b8373e61c14da42247f7683f924f80ecae1439`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c54774971cb7c57e8fe14a42f90f7e4cceb67150ff2f3112f9ad46fea390190d`  
		Last Modified: Wed, 22 Jun 2022 04:30:07 GMT  
		Size: 167.5 MB (167492656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f8955940c07caf93c5b3787f4d50541ad84d1a6b710568178150ed29fa8c1fa`  
		Last Modified: Fri, 24 Jun 2022 03:11:53 GMT  
		Size: 292.6 MB (292641283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7511706ae08b48d6c19d83e802574606ae85b91839fd444ed4e26a21afa13cd`  
		Last Modified: Fri, 24 Jun 2022 03:11:35 GMT  
		Size: 2.4 MB (2381172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13635cdd2c775430a870517defaca7b40e34781684ba15c1c4bf4a47a22d7a9f`  
		Last Modified: Fri, 24 Jun 2022 03:11:35 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a6406d38ab58e4a678b831cfa2cf3dc65217dfc73299c135a3c2947cbf288b`  
		Last Modified: Fri, 24 Jun 2022 03:11:35 GMT  
		Size: 2.3 KB (2312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:112f72e7060631567b461a6b28b02795ad282cad23c101738ae01981635a0371`  
		Last Modified: Fri, 24 Jun 2022 03:11:35 GMT  
		Size: 5.3 KB (5338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c054adc9f3f529d9b827670e5c7c0878dd4b56f3f90e919891c04cd198e7bbb`  
		Last Modified: Fri, 24 Jun 2022 03:11:35 GMT  
		Size: 2.5 KB (2501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:lts-mysql` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:8239f349f41eb1485f92190c846e889c7c6a069deef3e4810d62b3dca3b5cde9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **555.6 MB (555571284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d7ea8edd21d6b5820cbde3f17f19999ebce9e4ad1f0005dd187c3c77c3f8335`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:00:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:35:32 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 06:36:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:36:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:36:20 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 10:50:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 10:50:03 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 10:50:04 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 10:50:05 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 10:50:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:50:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:59:13 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 10:59:14 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 01:28:16 GMT
COPY dir:1fb0204bb532a7d63a0dd2d2677d66a70be0285454d27afba6780853636ba1ef in /usr/local/tomcat 
# Fri, 10 Jun 2022 01:28:22 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 01:28:24 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 01:28:25 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 01:28:26 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:24 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:25 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:09:26 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:09:27 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:10:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 24 Jun 2022 08:10:35 GMT
ENV XWIKI_VERSION=13.10.7
# Fri, 24 Jun 2022 08:10:35 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10.7
# Fri, 24 Jun 2022 08:10:36 GMT
ENV XWIKI_DOWNLOAD_SHA256=b886e886ed34e8d7bea8feb2e74e94edb3fb88030f90ab68c7bbc87dcf453d00
# Fri, 24 Jun 2022 08:11:07 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 24 Jun 2022 08:11:08 GMT
ENV MYSQL_JDBC_VERSION=8.0.29
# Fri, 24 Jun 2022 08:11:08 GMT
ENV MYSQL_JDBC_SHA256=d4e32d2a6026b5acc00300b73a86c28fb92681ae9629b21048ee67014c911db6
# Fri, 24 Jun 2022 08:11:09 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.29
# Fri, 24 Jun 2022 08:11:10 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.29.jar
# Fri, 24 Jun 2022 08:11:11 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.29.jar
# Fri, 24 Jun 2022 08:11:13 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 24 Jun 2022 08:11:14 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 24 Jun 2022 08:11:15 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 24 Jun 2022 08:11:16 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 24 Jun 2022 08:11:17 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 24 Jun 2022 08:11:17 GMT
VOLUME [/usr/local/xwiki]
# Fri, 24 Jun 2022 08:11:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jun 2022 08:11:19 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15da1b4c110f7cc460fbf968fb55b77c541f0e3ab87b92d5e6a822cc2c593e1`  
		Last Modified: Tue, 07 Jun 2022 05:10:23 GMT  
		Size: 15.9 MB (15898299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8e9d6a15d13e6f2d5d43f40b76051350cb7090cfcae5300dc1647e3196577a`  
		Last Modified: Tue, 07 Jun 2022 06:44:15 GMT  
		Size: 41.6 MB (41608356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51219ca7d003431d2f9c6ddda7db0a1902cf2b7e4e879625811b086f268b39c`  
		Last Modified: Tue, 07 Jun 2022 06:44:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5aa4900f44b9e3e20168d54fda3a0b78e62d572de1796db20345b70b1d8b3ca`  
		Last Modified: Tue, 07 Jun 2022 11:23:12 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6796806c88914990f15047665e74a4ea1fb933bdf7b8ebf39b1f2a82b723e044`  
		Last Modified: Fri, 10 Jun 2022 02:03:21 GMT  
		Size: 12.3 MB (12264791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca37469fc5a6ebbc5f1a764aabd4ba48b92a85d1396b644e1139994fad2fa34e`  
		Last Modified: Fri, 10 Jun 2022 02:03:20 GMT  
		Size: 208.8 KB (208841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c24501792b443d8ecb222b1c49c98ee84d4d76016bdbf8ba61b488fa873f7f`  
		Last Modified: Wed, 22 Jun 2022 04:17:01 GMT  
		Size: 163.4 MB (163365370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d4c4674e614cb6318120b7f3b95cc0f15a199054f449c2735cf25af9e2fd68`  
		Last Modified: Fri, 24 Jun 2022 08:14:37 GMT  
		Size: 292.6 MB (292641477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f45433cd06ad26dbb57afb98818c085a9ba114157cc72fa70214f8949e3ccfc`  
		Last Modified: Fri, 24 Jun 2022 08:14:15 GMT  
		Size: 2.4 MB (2381180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f75bf932706df5ca8d04fa02d8711685191f1f1dd7deb53937ba6f1371cb7fc5`  
		Last Modified: Fri, 24 Jun 2022 08:14:14 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04bce02a10640eb0a28ea0cd65126f65a6425540f18bd2acd881ed919828c057`  
		Last Modified: Fri, 24 Jun 2022 08:14:14 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:258f35d21774001fddc3b61192c74e053da90db66513a55c26d096b10ee59564`  
		Last Modified: Fri, 24 Jun 2022 08:14:14 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b877bc26e0f91fafb0bcbe8b609880d5c9cfba95b167970bae7650e06a31d706`  
		Last Modified: Fri, 24 Jun 2022 08:14:14 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:lts-mysql-tomcat`

```console
$ docker pull xwiki@sha256:538c472ff45f7c146d4cfbf1e7b31fb39f111a3d49287f502a6d2f71777ff333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:lts-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:d6bbb60b487ca00096f55242a245f5d8021e42013dc9a65227548a78a0e39f38
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.1 MB (563089744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce3a4cc5ca40c56b140b6c3abe277f24fb0842adc6ec43651543be6f4ba1e449`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:14:23 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 00:14:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:58 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:59 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 06:30:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:30:41 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 06:30:41 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:30:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:35:57 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 06:35:58 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 00:18:07 GMT
COPY dir:360b17da945f7a5c4dcdc8b0602904442d98c06d17157280c607532ec8b6edaa in /usr/local/tomcat 
# Fri, 10 Jun 2022 00:18:12 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 00:18:13 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 00:18:13 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 00:18:13 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:25:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 24 Jun 2022 03:08:16 GMT
ENV XWIKI_VERSION=13.10.7
# Fri, 24 Jun 2022 03:08:16 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10.7
# Fri, 24 Jun 2022 03:08:16 GMT
ENV XWIKI_DOWNLOAD_SHA256=b886e886ed34e8d7bea8feb2e74e94edb3fb88030f90ab68c7bbc87dcf453d00
# Fri, 24 Jun 2022 03:08:54 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 24 Jun 2022 03:08:54 GMT
ENV MYSQL_JDBC_VERSION=8.0.29
# Fri, 24 Jun 2022 03:08:55 GMT
ENV MYSQL_JDBC_SHA256=d4e32d2a6026b5acc00300b73a86c28fb92681ae9629b21048ee67014c911db6
# Fri, 24 Jun 2022 03:08:55 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.29
# Fri, 24 Jun 2022 03:08:55 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.29.jar
# Fri, 24 Jun 2022 03:08:55 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.29.jar
# Fri, 24 Jun 2022 03:08:56 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 24 Jun 2022 03:08:56 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 24 Jun 2022 03:08:56 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 24 Jun 2022 03:08:56 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 24 Jun 2022 03:08:57 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 24 Jun 2022 03:08:57 GMT
VOLUME [/usr/local/xwiki]
# Fri, 24 Jun 2022 03:08:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jun 2022 03:08:57 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b669251e19038a24bd6cab0baab92077f23163880fac4701fb3efa564350732b`  
		Last Modified: Tue, 07 Jun 2022 00:21:34 GMT  
		Size: 43.3 MB (43267270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf45eff8a02bcdf7a96904e0dc534c78c89a5c860e224fa57780ef2fc2eab99e`  
		Last Modified: Tue, 07 Jun 2022 00:21:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246089a07769500a0adb027d1dc0efbb1254ee07d75dcdc6f8a3ceb8bae3e95f`  
		Last Modified: Tue, 07 Jun 2022 06:48:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3636fe8b4383f769da39b4c598b1e98b53b6d528e34e9d20fac5c17cfefcd866`  
		Last Modified: Fri, 10 Jun 2022 00:40:50 GMT  
		Size: 12.2 MB (12247499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0a0fd2a02961d2a1725c94d0c0f5670c51d5f5f9bad820a96e45791a5d7a32`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 445.5 KB (445476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beba28f927b0599e17785c8f69b8373e61c14da42247f7683f924f80ecae1439`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c54774971cb7c57e8fe14a42f90f7e4cceb67150ff2f3112f9ad46fea390190d`  
		Last Modified: Wed, 22 Jun 2022 04:30:07 GMT  
		Size: 167.5 MB (167492656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f8955940c07caf93c5b3787f4d50541ad84d1a6b710568178150ed29fa8c1fa`  
		Last Modified: Fri, 24 Jun 2022 03:11:53 GMT  
		Size: 292.6 MB (292641283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7511706ae08b48d6c19d83e802574606ae85b91839fd444ed4e26a21afa13cd`  
		Last Modified: Fri, 24 Jun 2022 03:11:35 GMT  
		Size: 2.4 MB (2381172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13635cdd2c775430a870517defaca7b40e34781684ba15c1c4bf4a47a22d7a9f`  
		Last Modified: Fri, 24 Jun 2022 03:11:35 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a6406d38ab58e4a678b831cfa2cf3dc65217dfc73299c135a3c2947cbf288b`  
		Last Modified: Fri, 24 Jun 2022 03:11:35 GMT  
		Size: 2.3 KB (2312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:112f72e7060631567b461a6b28b02795ad282cad23c101738ae01981635a0371`  
		Last Modified: Fri, 24 Jun 2022 03:11:35 GMT  
		Size: 5.3 KB (5338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c054adc9f3f529d9b827670e5c7c0878dd4b56f3f90e919891c04cd198e7bbb`  
		Last Modified: Fri, 24 Jun 2022 03:11:35 GMT  
		Size: 2.5 KB (2501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:lts-mysql-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:8239f349f41eb1485f92190c846e889c7c6a069deef3e4810d62b3dca3b5cde9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **555.6 MB (555571284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d7ea8edd21d6b5820cbde3f17f19999ebce9e4ad1f0005dd187c3c77c3f8335`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:00:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:35:32 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 06:36:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:36:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:36:20 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 10:50:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 10:50:03 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 10:50:04 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 10:50:05 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 10:50:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:50:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:59:13 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 10:59:14 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 01:28:16 GMT
COPY dir:1fb0204bb532a7d63a0dd2d2677d66a70be0285454d27afba6780853636ba1ef in /usr/local/tomcat 
# Fri, 10 Jun 2022 01:28:22 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 01:28:24 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 01:28:25 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 01:28:26 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:24 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:25 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:09:26 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:09:27 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:10:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 24 Jun 2022 08:10:35 GMT
ENV XWIKI_VERSION=13.10.7
# Fri, 24 Jun 2022 08:10:35 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10.7
# Fri, 24 Jun 2022 08:10:36 GMT
ENV XWIKI_DOWNLOAD_SHA256=b886e886ed34e8d7bea8feb2e74e94edb3fb88030f90ab68c7bbc87dcf453d00
# Fri, 24 Jun 2022 08:11:07 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 24 Jun 2022 08:11:08 GMT
ENV MYSQL_JDBC_VERSION=8.0.29
# Fri, 24 Jun 2022 08:11:08 GMT
ENV MYSQL_JDBC_SHA256=d4e32d2a6026b5acc00300b73a86c28fb92681ae9629b21048ee67014c911db6
# Fri, 24 Jun 2022 08:11:09 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.29
# Fri, 24 Jun 2022 08:11:10 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.29.jar
# Fri, 24 Jun 2022 08:11:11 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.29.jar
# Fri, 24 Jun 2022 08:11:13 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 24 Jun 2022 08:11:14 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 24 Jun 2022 08:11:15 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 24 Jun 2022 08:11:16 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 24 Jun 2022 08:11:17 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 24 Jun 2022 08:11:17 GMT
VOLUME [/usr/local/xwiki]
# Fri, 24 Jun 2022 08:11:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jun 2022 08:11:19 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15da1b4c110f7cc460fbf968fb55b77c541f0e3ab87b92d5e6a822cc2c593e1`  
		Last Modified: Tue, 07 Jun 2022 05:10:23 GMT  
		Size: 15.9 MB (15898299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8e9d6a15d13e6f2d5d43f40b76051350cb7090cfcae5300dc1647e3196577a`  
		Last Modified: Tue, 07 Jun 2022 06:44:15 GMT  
		Size: 41.6 MB (41608356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51219ca7d003431d2f9c6ddda7db0a1902cf2b7e4e879625811b086f268b39c`  
		Last Modified: Tue, 07 Jun 2022 06:44:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5aa4900f44b9e3e20168d54fda3a0b78e62d572de1796db20345b70b1d8b3ca`  
		Last Modified: Tue, 07 Jun 2022 11:23:12 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6796806c88914990f15047665e74a4ea1fb933bdf7b8ebf39b1f2a82b723e044`  
		Last Modified: Fri, 10 Jun 2022 02:03:21 GMT  
		Size: 12.3 MB (12264791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca37469fc5a6ebbc5f1a764aabd4ba48b92a85d1396b644e1139994fad2fa34e`  
		Last Modified: Fri, 10 Jun 2022 02:03:20 GMT  
		Size: 208.8 KB (208841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c24501792b443d8ecb222b1c49c98ee84d4d76016bdbf8ba61b488fa873f7f`  
		Last Modified: Wed, 22 Jun 2022 04:17:01 GMT  
		Size: 163.4 MB (163365370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d4c4674e614cb6318120b7f3b95cc0f15a199054f449c2735cf25af9e2fd68`  
		Last Modified: Fri, 24 Jun 2022 08:14:37 GMT  
		Size: 292.6 MB (292641477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f45433cd06ad26dbb57afb98818c085a9ba114157cc72fa70214f8949e3ccfc`  
		Last Modified: Fri, 24 Jun 2022 08:14:15 GMT  
		Size: 2.4 MB (2381180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f75bf932706df5ca8d04fa02d8711685191f1f1dd7deb53937ba6f1371cb7fc5`  
		Last Modified: Fri, 24 Jun 2022 08:14:14 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04bce02a10640eb0a28ea0cd65126f65a6425540f18bd2acd881ed919828c057`  
		Last Modified: Fri, 24 Jun 2022 08:14:14 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:258f35d21774001fddc3b61192c74e053da90db66513a55c26d096b10ee59564`  
		Last Modified: Fri, 24 Jun 2022 08:14:14 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b877bc26e0f91fafb0bcbe8b609880d5c9cfba95b167970bae7650e06a31d706`  
		Last Modified: Fri, 24 Jun 2022 08:14:14 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:lts-postgres`

```console
$ docker pull xwiki@sha256:b250edc19f4cc72d051ff836bc6a66dad2884231ad972b66018917572d37c35d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:lts-postgres` - linux; amd64

```console
$ docker pull xwiki@sha256:638d7630646963b18a849058a847b7caab4ded28712b60b0d6d1900f56b0c537
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.3 MB (562304923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79cad287c34ddcfc1a8b8fa8c65cb34197ee741da2b4c8d387d6e0ad78009ec9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:14:23 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 00:14:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:58 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:59 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 06:30:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:30:41 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 06:30:41 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:30:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:35:57 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 06:35:58 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 00:18:07 GMT
COPY dir:360b17da945f7a5c4dcdc8b0602904442d98c06d17157280c607532ec8b6edaa in /usr/local/tomcat 
# Fri, 10 Jun 2022 00:18:12 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 00:18:13 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 00:18:13 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 00:18:13 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:26:27 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 24 Jun 2022 03:09:04 GMT
ENV XWIKI_VERSION=13.10.7
# Fri, 24 Jun 2022 03:09:04 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10.7
# Fri, 24 Jun 2022 03:09:05 GMT
ENV XWIKI_DOWNLOAD_SHA256=b886e886ed34e8d7bea8feb2e74e94edb3fb88030f90ab68c7bbc87dcf453d00
# Fri, 24 Jun 2022 03:10:26 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 24 Jun 2022 03:10:28 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 24 Jun 2022 03:10:28 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 24 Jun 2022 03:10:28 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 24 Jun 2022 03:10:29 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 24 Jun 2022 03:10:29 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 24 Jun 2022 03:10:29 GMT
VOLUME [/usr/local/xwiki]
# Fri, 24 Jun 2022 03:10:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jun 2022 03:10:29 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b669251e19038a24bd6cab0baab92077f23163880fac4701fb3efa564350732b`  
		Last Modified: Tue, 07 Jun 2022 00:21:34 GMT  
		Size: 43.3 MB (43267270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf45eff8a02bcdf7a96904e0dc534c78c89a5c860e224fa57780ef2fc2eab99e`  
		Last Modified: Tue, 07 Jun 2022 00:21:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246089a07769500a0adb027d1dc0efbb1254ee07d75dcdc6f8a3ceb8bae3e95f`  
		Last Modified: Tue, 07 Jun 2022 06:48:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3636fe8b4383f769da39b4c598b1e98b53b6d528e34e9d20fac5c17cfefcd866`  
		Last Modified: Fri, 10 Jun 2022 00:40:50 GMT  
		Size: 12.2 MB (12247499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0a0fd2a02961d2a1725c94d0c0f5670c51d5f5f9bad820a96e45791a5d7a32`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 445.5 KB (445476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beba28f927b0599e17785c8f69b8373e61c14da42247f7683f924f80ecae1439`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:657eec0a2bb289006e136ad46dbd1d85e8ff10712e1477c0fcacb617a19bb242`  
		Last Modified: Wed, 22 Jun 2022 04:31:12 GMT  
		Size: 168.3 MB (168293438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:136be306a609540683e370b2425b4d3703542a79224441c6337af82ee1698ca2`  
		Last Modified: Fri, 24 Jun 2022 03:12:46 GMT  
		Size: 292.6 MB (292641286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3769fbd23a38bb2c2737d30cd4a790f8ad775a99a63e6591de2df21d750f52`  
		Last Modified: Fri, 24 Jun 2022 03:12:29 GMT  
		Size: 795.4 KB (795424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:155517bc4fff02081a754dd1ac5674da90d74db9792a871f64983196cbd2b573`  
		Last Modified: Fri, 24 Jun 2022 03:12:28 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e9d584cf5548a2a612999b7b8fb340c4a38d8e9b31fd9ab73ca09cb173eb0f`  
		Last Modified: Fri, 24 Jun 2022 03:12:28 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2330650c98390edb3e1e7bd4d667c7b4e344da794f180c208aa1c92872db10cc`  
		Last Modified: Fri, 24 Jun 2022 03:12:29 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9458af98469686b7341e974f7343a72938ca0fa6984c887bb8d0a160375881ee`  
		Last Modified: Fri, 24 Jun 2022 03:12:29 GMT  
		Size: 2.5 KB (2503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:lts-postgres` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:bb8443f4c39a1e5e1eaa389c87f32b928bccad2f727705a2e02afcc1b98ac2bf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.8 MB (554784337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99d205394842fb0b6709b682ff9d39e01d0ade2e25f08c11c4c8c766f9ccd182`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:00:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:35:32 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 06:36:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:36:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:36:20 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 10:50:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 10:50:03 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 10:50:04 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 10:50:05 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 10:50:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:50:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:59:13 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 10:59:14 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 01:28:16 GMT
COPY dir:1fb0204bb532a7d63a0dd2d2677d66a70be0285454d27afba6780853636ba1ef in /usr/local/tomcat 
# Fri, 10 Jun 2022 01:28:22 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 01:28:24 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 01:28:25 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 01:28:26 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:24 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:25 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:09:26 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:09:27 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:11:42 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 24 Jun 2022 08:11:28 GMT
ENV XWIKI_VERSION=13.10.7
# Fri, 24 Jun 2022 08:11:29 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10.7
# Fri, 24 Jun 2022 08:11:30 GMT
ENV XWIKI_DOWNLOAD_SHA256=b886e886ed34e8d7bea8feb2e74e94edb3fb88030f90ab68c7bbc87dcf453d00
# Fri, 24 Jun 2022 08:12:12 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 24 Jun 2022 08:12:13 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 24 Jun 2022 08:12:14 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 24 Jun 2022 08:12:15 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 24 Jun 2022 08:12:16 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 24 Jun 2022 08:12:17 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 24 Jun 2022 08:12:17 GMT
VOLUME [/usr/local/xwiki]
# Fri, 24 Jun 2022 08:12:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jun 2022 08:12:19 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15da1b4c110f7cc460fbf968fb55b77c541f0e3ab87b92d5e6a822cc2c593e1`  
		Last Modified: Tue, 07 Jun 2022 05:10:23 GMT  
		Size: 15.9 MB (15898299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8e9d6a15d13e6f2d5d43f40b76051350cb7090cfcae5300dc1647e3196577a`  
		Last Modified: Tue, 07 Jun 2022 06:44:15 GMT  
		Size: 41.6 MB (41608356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51219ca7d003431d2f9c6ddda7db0a1902cf2b7e4e879625811b086f268b39c`  
		Last Modified: Tue, 07 Jun 2022 06:44:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5aa4900f44b9e3e20168d54fda3a0b78e62d572de1796db20345b70b1d8b3ca`  
		Last Modified: Tue, 07 Jun 2022 11:23:12 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6796806c88914990f15047665e74a4ea1fb933bdf7b8ebf39b1f2a82b723e044`  
		Last Modified: Fri, 10 Jun 2022 02:03:21 GMT  
		Size: 12.3 MB (12264791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca37469fc5a6ebbc5f1a764aabd4ba48b92a85d1396b644e1139994fad2fa34e`  
		Last Modified: Fri, 10 Jun 2022 02:03:20 GMT  
		Size: 208.8 KB (208841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbf4753a12af2d02fd26a953119f6843f7e381cfec0d679d92b04b4e4f5a3d6a`  
		Last Modified: Wed, 22 Jun 2022 04:18:08 GMT  
		Size: 164.2 MB (164164156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acdad91995b0da375c92d6651576276e78123cfbb080e5444a094fc5033c930c`  
		Last Modified: Fri, 24 Jun 2022 08:15:36 GMT  
		Size: 292.6 MB (292641359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:350ecfd793c7e54308d1c7a22f36e2e098e8fdae31cecb75339bfa7f0a8b7af6`  
		Last Modified: Fri, 24 Jun 2022 08:15:14 GMT  
		Size: 795.4 KB (795417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c27ddaa528e0298945c5eca4aa5235bd761f13f40e2b35de068a7977434e571d`  
		Last Modified: Fri, 24 Jun 2022 08:15:14 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9edb1eb483f19a886fd0fcf80dc5c21e5ef36163eb1e8df94a3b80f508fbeff8`  
		Last Modified: Fri, 24 Jun 2022 08:15:14 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d9ff4c9416279f5b0a9e42bf517e29f15992d0a7a0c5d3361f7fbc8472c12d`  
		Last Modified: Fri, 24 Jun 2022 08:15:14 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be06063b865aaeadaa012c84711685856110099c19fa07ac1af19e12fa08cce`  
		Last Modified: Fri, 24 Jun 2022 08:15:14 GMT  
		Size: 2.5 KB (2507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:lts-postgres-tomcat`

```console
$ docker pull xwiki@sha256:b250edc19f4cc72d051ff836bc6a66dad2884231ad972b66018917572d37c35d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:lts-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:638d7630646963b18a849058a847b7caab4ded28712b60b0d6d1900f56b0c537
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.3 MB (562304923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79cad287c34ddcfc1a8b8fa8c65cb34197ee741da2b4c8d387d6e0ad78009ec9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:14:23 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 00:14:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:58 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:59 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 06:30:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:30:41 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 06:30:41 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:30:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:35:57 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 06:35:58 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 00:18:07 GMT
COPY dir:360b17da945f7a5c4dcdc8b0602904442d98c06d17157280c607532ec8b6edaa in /usr/local/tomcat 
# Fri, 10 Jun 2022 00:18:12 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 00:18:13 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 00:18:13 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 00:18:13 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:26:27 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 24 Jun 2022 03:09:04 GMT
ENV XWIKI_VERSION=13.10.7
# Fri, 24 Jun 2022 03:09:04 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10.7
# Fri, 24 Jun 2022 03:09:05 GMT
ENV XWIKI_DOWNLOAD_SHA256=b886e886ed34e8d7bea8feb2e74e94edb3fb88030f90ab68c7bbc87dcf453d00
# Fri, 24 Jun 2022 03:10:26 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 24 Jun 2022 03:10:28 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 24 Jun 2022 03:10:28 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 24 Jun 2022 03:10:28 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 24 Jun 2022 03:10:29 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 24 Jun 2022 03:10:29 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 24 Jun 2022 03:10:29 GMT
VOLUME [/usr/local/xwiki]
# Fri, 24 Jun 2022 03:10:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jun 2022 03:10:29 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b669251e19038a24bd6cab0baab92077f23163880fac4701fb3efa564350732b`  
		Last Modified: Tue, 07 Jun 2022 00:21:34 GMT  
		Size: 43.3 MB (43267270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf45eff8a02bcdf7a96904e0dc534c78c89a5c860e224fa57780ef2fc2eab99e`  
		Last Modified: Tue, 07 Jun 2022 00:21:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246089a07769500a0adb027d1dc0efbb1254ee07d75dcdc6f8a3ceb8bae3e95f`  
		Last Modified: Tue, 07 Jun 2022 06:48:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3636fe8b4383f769da39b4c598b1e98b53b6d528e34e9d20fac5c17cfefcd866`  
		Last Modified: Fri, 10 Jun 2022 00:40:50 GMT  
		Size: 12.2 MB (12247499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0a0fd2a02961d2a1725c94d0c0f5670c51d5f5f9bad820a96e45791a5d7a32`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 445.5 KB (445476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beba28f927b0599e17785c8f69b8373e61c14da42247f7683f924f80ecae1439`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:657eec0a2bb289006e136ad46dbd1d85e8ff10712e1477c0fcacb617a19bb242`  
		Last Modified: Wed, 22 Jun 2022 04:31:12 GMT  
		Size: 168.3 MB (168293438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:136be306a609540683e370b2425b4d3703542a79224441c6337af82ee1698ca2`  
		Last Modified: Fri, 24 Jun 2022 03:12:46 GMT  
		Size: 292.6 MB (292641286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3769fbd23a38bb2c2737d30cd4a790f8ad775a99a63e6591de2df21d750f52`  
		Last Modified: Fri, 24 Jun 2022 03:12:29 GMT  
		Size: 795.4 KB (795424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:155517bc4fff02081a754dd1ac5674da90d74db9792a871f64983196cbd2b573`  
		Last Modified: Fri, 24 Jun 2022 03:12:28 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e9d584cf5548a2a612999b7b8fb340c4a38d8e9b31fd9ab73ca09cb173eb0f`  
		Last Modified: Fri, 24 Jun 2022 03:12:28 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2330650c98390edb3e1e7bd4d667c7b4e344da794f180c208aa1c92872db10cc`  
		Last Modified: Fri, 24 Jun 2022 03:12:29 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9458af98469686b7341e974f7343a72938ca0fa6984c887bb8d0a160375881ee`  
		Last Modified: Fri, 24 Jun 2022 03:12:29 GMT  
		Size: 2.5 KB (2503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:lts-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:bb8443f4c39a1e5e1eaa389c87f32b928bccad2f727705a2e02afcc1b98ac2bf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.8 MB (554784337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99d205394842fb0b6709b682ff9d39e01d0ade2e25f08c11c4c8c766f9ccd182`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:00:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:35:32 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 06:36:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:36:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:36:20 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 10:50:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 10:50:03 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 10:50:04 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 10:50:05 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 10:50:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:50:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:59:13 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 10:59:14 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 01:28:16 GMT
COPY dir:1fb0204bb532a7d63a0dd2d2677d66a70be0285454d27afba6780853636ba1ef in /usr/local/tomcat 
# Fri, 10 Jun 2022 01:28:22 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 01:28:24 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 01:28:25 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 01:28:26 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:24 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:25 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:09:26 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:09:27 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:11:42 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 24 Jun 2022 08:11:28 GMT
ENV XWIKI_VERSION=13.10.7
# Fri, 24 Jun 2022 08:11:29 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10.7
# Fri, 24 Jun 2022 08:11:30 GMT
ENV XWIKI_DOWNLOAD_SHA256=b886e886ed34e8d7bea8feb2e74e94edb3fb88030f90ab68c7bbc87dcf453d00
# Fri, 24 Jun 2022 08:12:12 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 24 Jun 2022 08:12:13 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 24 Jun 2022 08:12:14 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 24 Jun 2022 08:12:15 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 24 Jun 2022 08:12:16 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 24 Jun 2022 08:12:17 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 24 Jun 2022 08:12:17 GMT
VOLUME [/usr/local/xwiki]
# Fri, 24 Jun 2022 08:12:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jun 2022 08:12:19 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15da1b4c110f7cc460fbf968fb55b77c541f0e3ab87b92d5e6a822cc2c593e1`  
		Last Modified: Tue, 07 Jun 2022 05:10:23 GMT  
		Size: 15.9 MB (15898299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8e9d6a15d13e6f2d5d43f40b76051350cb7090cfcae5300dc1647e3196577a`  
		Last Modified: Tue, 07 Jun 2022 06:44:15 GMT  
		Size: 41.6 MB (41608356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51219ca7d003431d2f9c6ddda7db0a1902cf2b7e4e879625811b086f268b39c`  
		Last Modified: Tue, 07 Jun 2022 06:44:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5aa4900f44b9e3e20168d54fda3a0b78e62d572de1796db20345b70b1d8b3ca`  
		Last Modified: Tue, 07 Jun 2022 11:23:12 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6796806c88914990f15047665e74a4ea1fb933bdf7b8ebf39b1f2a82b723e044`  
		Last Modified: Fri, 10 Jun 2022 02:03:21 GMT  
		Size: 12.3 MB (12264791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca37469fc5a6ebbc5f1a764aabd4ba48b92a85d1396b644e1139994fad2fa34e`  
		Last Modified: Fri, 10 Jun 2022 02:03:20 GMT  
		Size: 208.8 KB (208841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbf4753a12af2d02fd26a953119f6843f7e381cfec0d679d92b04b4e4f5a3d6a`  
		Last Modified: Wed, 22 Jun 2022 04:18:08 GMT  
		Size: 164.2 MB (164164156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acdad91995b0da375c92d6651576276e78123cfbb080e5444a094fc5033c930c`  
		Last Modified: Fri, 24 Jun 2022 08:15:36 GMT  
		Size: 292.6 MB (292641359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:350ecfd793c7e54308d1c7a22f36e2e098e8fdae31cecb75339bfa7f0a8b7af6`  
		Last Modified: Fri, 24 Jun 2022 08:15:14 GMT  
		Size: 795.4 KB (795417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c27ddaa528e0298945c5eca4aa5235bd761f13f40e2b35de068a7977434e571d`  
		Last Modified: Fri, 24 Jun 2022 08:15:14 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9edb1eb483f19a886fd0fcf80dc5c21e5ef36163eb1e8df94a3b80f508fbeff8`  
		Last Modified: Fri, 24 Jun 2022 08:15:14 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d9ff4c9416279f5b0a9e42bf517e29f15992d0a7a0c5d3361f7fbc8472c12d`  
		Last Modified: Fri, 24 Jun 2022 08:15:14 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be06063b865aaeadaa012c84711685856110099c19fa07ac1af19e12fa08cce`  
		Last Modified: Fri, 24 Jun 2022 08:15:14 GMT  
		Size: 2.5 KB (2507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:mariadb-tomcat`

```console
$ docker pull xwiki@sha256:3db745735e3f4998cf83b2a5dc35cd5b861564cac0ff1f91425512cc46c054ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:mariadb-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:5be2c4cf71703a8afc1dc6cd56002d86482ca326367b5a080809603ece9ae80a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.6 MB (560590373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7416cc5f4b70e5175c8fecfe02fb114cdab2e1b5150287649b6d3524c2bcd556`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:14:23 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 00:14:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:58 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:59 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 06:30:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:30:41 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 06:30:41 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:30:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:35:57 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 06:35:58 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 00:18:07 GMT
COPY dir:360b17da945f7a5c4dcdc8b0602904442d98c06d17157280c607532ec8b6edaa in /usr/local/tomcat 
# Fri, 10 Jun 2022 00:18:12 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 00:18:13 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 00:18:13 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 00:18:13 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:25:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 22 Jun 2022 04:25:05 GMT
ENV XWIKI_VERSION=14.4.1
# Wed, 22 Jun 2022 04:25:05 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.4.1
# Wed, 22 Jun 2022 04:25:05 GMT
ENV XWIKI_DOWNLOAD_SHA256=8e20eba50acee0f157d3cc160306d65e0995b453833c8923f833030f0a469fb4
# Wed, 22 Jun 2022 04:25:42 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 22 Jun 2022 04:27:20 GMT
ENV MARIADB_JDBC_VERSION=3.0.5
# Wed, 22 Jun 2022 04:27:20 GMT
ENV MARIADB_JDBC_SHA256=e9532d9bca07c1263c32b00b495bd3ec7f2b79320513cabd762bf39ea09e68d9
# Wed, 22 Jun 2022 04:27:20 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.0.5
# Wed, 22 Jun 2022 04:27:20 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.0.5.jar
# Wed, 22 Jun 2022 04:27:20 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.0.5.jar
# Wed, 22 Jun 2022 04:27:21 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Wed, 22 Jun 2022 04:27:21 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 22 Jun 2022 04:27:21 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 22 Jun 2022 04:27:22 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 22 Jun 2022 04:27:22 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 22 Jun 2022 04:27:22 GMT
VOLUME [/usr/local/xwiki]
# Wed, 22 Jun 2022 04:27:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jun 2022 04:27:22 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b669251e19038a24bd6cab0baab92077f23163880fac4701fb3efa564350732b`  
		Last Modified: Tue, 07 Jun 2022 00:21:34 GMT  
		Size: 43.3 MB (43267270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf45eff8a02bcdf7a96904e0dc534c78c89a5c860e224fa57780ef2fc2eab99e`  
		Last Modified: Tue, 07 Jun 2022 00:21:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246089a07769500a0adb027d1dc0efbb1254ee07d75dcdc6f8a3ceb8bae3e95f`  
		Last Modified: Tue, 07 Jun 2022 06:48:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3636fe8b4383f769da39b4c598b1e98b53b6d528e34e9d20fac5c17cfefcd866`  
		Last Modified: Fri, 10 Jun 2022 00:40:50 GMT  
		Size: 12.2 MB (12247499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0a0fd2a02961d2a1725c94d0c0f5670c51d5f5f9bad820a96e45791a5d7a32`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 445.5 KB (445476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beba28f927b0599e17785c8f69b8373e61c14da42247f7683f924f80ecae1439`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c54774971cb7c57e8fe14a42f90f7e4cceb67150ff2f3112f9ad46fea390190d`  
		Last Modified: Wed, 22 Jun 2022 04:30:07 GMT  
		Size: 167.5 MB (167492656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:368fa3670d498d9bc0883cd81cf9b9a45d3ccf79365eabe27b779344efefda58`  
		Last Modified: Wed, 22 Jun 2022 04:30:00 GMT  
		Size: 292.0 MB (291982499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c1ab918c0e0ec1820084e4da9e0f385f44acb6a9a2c61f37cba3191a960dec1`  
		Last Modified: Wed, 22 Jun 2022 04:31:36 GMT  
		Size: 540.1 KB (540065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2359c2da84be359f352d0435136b09e78a9776b1d22b4dbdd3f6fec942973375`  
		Last Modified: Wed, 22 Jun 2022 04:31:36 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9269ef1e91c8bcc8306aee08c0a04ec885a56ef859428b65c847bec5ddf4d5ce`  
		Last Modified: Wed, 22 Jun 2022 04:31:35 GMT  
		Size: 2.3 KB (2309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b60d3cde6a56696f82809b7ff8a140448d3abe21f2778008cd1c92705cd8cb`  
		Last Modified: Wed, 22 Jun 2022 04:31:35 GMT  
		Size: 5.9 KB (5856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d320a8df62dc7b14288e1ee93b18d239e5ac432d1ac8aab55e511dcbdfbc27`  
		Last Modified: Wed, 22 Jun 2022 04:31:35 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:mariadb-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:bda93d405e13407149f8f73a5894a9ac80b447f92ade102dcb003d1fbd9e8a7f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **553.1 MB (553071844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ee73663f1cd3949cf5e95503adb5d84ae70153601cd42f36eea35f77b61d0b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:00:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:35:32 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 06:36:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:36:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:36:20 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 10:50:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 10:50:03 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 10:50:04 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 10:50:05 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 10:50:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:50:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:59:13 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 10:59:14 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 01:28:16 GMT
COPY dir:1fb0204bb532a7d63a0dd2d2677d66a70be0285454d27afba6780853636ba1ef in /usr/local/tomcat 
# Fri, 10 Jun 2022 01:28:22 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 01:28:24 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 01:28:25 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 01:28:26 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:24 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:25 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:09:26 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:09:27 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:10:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 22 Jun 2022 04:10:05 GMT
ENV XWIKI_VERSION=14.4.1
# Wed, 22 Jun 2022 04:10:06 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.4.1
# Wed, 22 Jun 2022 04:10:07 GMT
ENV XWIKI_DOWNLOAD_SHA256=8e20eba50acee0f157d3cc160306d65e0995b453833c8923f833030f0a469fb4
# Wed, 22 Jun 2022 04:10:44 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 22 Jun 2022 04:12:47 GMT
ENV MARIADB_JDBC_VERSION=3.0.5
# Wed, 22 Jun 2022 04:12:48 GMT
ENV MARIADB_JDBC_SHA256=e9532d9bca07c1263c32b00b495bd3ec7f2b79320513cabd762bf39ea09e68d9
# Wed, 22 Jun 2022 04:12:49 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.0.5
# Wed, 22 Jun 2022 04:12:50 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.0.5.jar
# Wed, 22 Jun 2022 04:12:51 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.0.5.jar
# Wed, 22 Jun 2022 04:12:53 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Wed, 22 Jun 2022 04:12:54 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 22 Jun 2022 04:12:55 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 22 Jun 2022 04:12:56 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 22 Jun 2022 04:12:57 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 22 Jun 2022 04:12:57 GMT
VOLUME [/usr/local/xwiki]
# Wed, 22 Jun 2022 04:12:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jun 2022 04:12:59 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15da1b4c110f7cc460fbf968fb55b77c541f0e3ab87b92d5e6a822cc2c593e1`  
		Last Modified: Tue, 07 Jun 2022 05:10:23 GMT  
		Size: 15.9 MB (15898299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8e9d6a15d13e6f2d5d43f40b76051350cb7090cfcae5300dc1647e3196577a`  
		Last Modified: Tue, 07 Jun 2022 06:44:15 GMT  
		Size: 41.6 MB (41608356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51219ca7d003431d2f9c6ddda7db0a1902cf2b7e4e879625811b086f268b39c`  
		Last Modified: Tue, 07 Jun 2022 06:44:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5aa4900f44b9e3e20168d54fda3a0b78e62d572de1796db20345b70b1d8b3ca`  
		Last Modified: Tue, 07 Jun 2022 11:23:12 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6796806c88914990f15047665e74a4ea1fb933bdf7b8ebf39b1f2a82b723e044`  
		Last Modified: Fri, 10 Jun 2022 02:03:21 GMT  
		Size: 12.3 MB (12264791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca37469fc5a6ebbc5f1a764aabd4ba48b92a85d1396b644e1139994fad2fa34e`  
		Last Modified: Fri, 10 Jun 2022 02:03:20 GMT  
		Size: 208.8 KB (208841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c24501792b443d8ecb222b1c49c98ee84d4d76016bdbf8ba61b488fa873f7f`  
		Last Modified: Wed, 22 Jun 2022 04:17:01 GMT  
		Size: 163.4 MB (163365370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d1bb494106d6d36bcf7dd967f0d881aa979803343f00918d55f105d5759bbe`  
		Last Modified: Wed, 22 Jun 2022 04:16:59 GMT  
		Size: 292.0 MB (291982622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba0bfc714e56ec603906f85a8dacd34f5dad693a8c6dbcf8a9567fbca423d16`  
		Last Modified: Wed, 22 Jun 2022 04:18:35 GMT  
		Size: 540.1 KB (540069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e192a89ffea555829e044cd56b10c8021a547d8a56e5a69c0a6714bb461f596d`  
		Last Modified: Wed, 22 Jun 2022 04:18:35 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc8a81604a8c8778019d65f20d4893ebf3957eadbc949f6c2ca6a5ede778ba6d`  
		Last Modified: Wed, 22 Jun 2022 04:18:35 GMT  
		Size: 2.3 KB (2311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d62f47e27689a9f1dfc33daa4881e9da0078b7620dbb8c9c520858ac340b8fb4`  
		Last Modified: Wed, 22 Jun 2022 04:18:34 GMT  
		Size: 5.9 KB (5854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:542f6bbdec9617d4401973008c85e7ea003f6f336c453085de1f99098e8911e4`  
		Last Modified: Wed, 22 Jun 2022 04:18:34 GMT  
		Size: 2.5 KB (2507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:mysql-tomcat`

```console
$ docker pull xwiki@sha256:8b941b575bfdc8c0eb31d9b7f3422c6fe866062a7b465d725d53ec4107ca6144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:f08dab318ed8416b7ef8fc05f68b5c11c7f486d1b4686584b35fbf916cb81081
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.4 MB (562431476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68a5a2c9d16899b288b020a4b618dae8b4a2aa67718272532c3f92b8caca60fd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:14:23 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 00:14:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:58 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:59 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 06:30:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:30:41 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 06:30:41 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:30:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:35:57 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 06:35:58 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 00:18:07 GMT
COPY dir:360b17da945f7a5c4dcdc8b0602904442d98c06d17157280c607532ec8b6edaa in /usr/local/tomcat 
# Fri, 10 Jun 2022 00:18:12 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 00:18:13 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 00:18:13 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 00:18:13 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:25:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 22 Jun 2022 04:25:05 GMT
ENV XWIKI_VERSION=14.4.1
# Wed, 22 Jun 2022 04:25:05 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.4.1
# Wed, 22 Jun 2022 04:25:05 GMT
ENV XWIKI_DOWNLOAD_SHA256=8e20eba50acee0f157d3cc160306d65e0995b453833c8923f833030f0a469fb4
# Wed, 22 Jun 2022 04:25:42 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 22 Jun 2022 04:25:43 GMT
ENV MYSQL_JDBC_VERSION=8.0.29
# Wed, 22 Jun 2022 04:25:43 GMT
ENV MYSQL_JDBC_SHA256=d4e32d2a6026b5acc00300b73a86c28fb92681ae9629b21048ee67014c911db6
# Wed, 22 Jun 2022 04:25:43 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.29
# Wed, 22 Jun 2022 04:25:43 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.29.jar
# Wed, 22 Jun 2022 04:25:44 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.29.jar
# Wed, 22 Jun 2022 04:25:44 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Wed, 22 Jun 2022 04:25:44 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 22 Jun 2022 04:25:44 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 22 Jun 2022 04:25:45 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 22 Jun 2022 04:25:45 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 22 Jun 2022 04:25:45 GMT
VOLUME [/usr/local/xwiki]
# Wed, 22 Jun 2022 04:25:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jun 2022 04:25:45 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b669251e19038a24bd6cab0baab92077f23163880fac4701fb3efa564350732b`  
		Last Modified: Tue, 07 Jun 2022 00:21:34 GMT  
		Size: 43.3 MB (43267270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf45eff8a02bcdf7a96904e0dc534c78c89a5c860e224fa57780ef2fc2eab99e`  
		Last Modified: Tue, 07 Jun 2022 00:21:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246089a07769500a0adb027d1dc0efbb1254ee07d75dcdc6f8a3ceb8bae3e95f`  
		Last Modified: Tue, 07 Jun 2022 06:48:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3636fe8b4383f769da39b4c598b1e98b53b6d528e34e9d20fac5c17cfefcd866`  
		Last Modified: Fri, 10 Jun 2022 00:40:50 GMT  
		Size: 12.2 MB (12247499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0a0fd2a02961d2a1725c94d0c0f5670c51d5f5f9bad820a96e45791a5d7a32`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 445.5 KB (445476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beba28f927b0599e17785c8f69b8373e61c14da42247f7683f924f80ecae1439`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c54774971cb7c57e8fe14a42f90f7e4cceb67150ff2f3112f9ad46fea390190d`  
		Last Modified: Wed, 22 Jun 2022 04:30:07 GMT  
		Size: 167.5 MB (167492656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:368fa3670d498d9bc0883cd81cf9b9a45d3ccf79365eabe27b779344efefda58`  
		Last Modified: Wed, 22 Jun 2022 04:30:00 GMT  
		Size: 292.0 MB (291982499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb96a08b07f52ad5c126f31fe742e1c114a3239ab5c6fc5641266fa5be00579`  
		Last Modified: Wed, 22 Jun 2022 04:29:42 GMT  
		Size: 2.4 MB (2381172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94af0360a2e049892f0b11539619a1e889f32dcdec1df1a671ffb6032f55437`  
		Last Modified: Wed, 22 Jun 2022 04:29:41 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7255f65a4fc48ef292f0f13fc58a9f76e18f7f3969190698a08ff5907c9e5dd`  
		Last Modified: Wed, 22 Jun 2022 04:29:41 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1695b6d1dbcfb2018bc0a46ec5c66b47f1105c4aff382726932ee462014d294e`  
		Last Modified: Wed, 22 Jun 2022 04:29:41 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec62f61e9a4c7f7d90e61399a76eb18b02a789afbac8e9fcaaa1f8ebc6b10da`  
		Last Modified: Wed, 22 Jun 2022 04:29:41 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:mysql-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:b4d50e1906ede668b41d744d6050b179dc5523658ba13b4e4cc5a92b98955a71
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.9 MB (554912952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed7a93d82de140d630b2eab42fb4270590bb2efcab4d72dd5a2f2dd8ce842278`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:00:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:35:32 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 06:36:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:36:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:36:20 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 10:50:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 10:50:03 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 10:50:04 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 10:50:05 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 10:50:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:50:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:59:13 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 10:59:14 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 01:28:16 GMT
COPY dir:1fb0204bb532a7d63a0dd2d2677d66a70be0285454d27afba6780853636ba1ef in /usr/local/tomcat 
# Fri, 10 Jun 2022 01:28:22 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 01:28:24 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 01:28:25 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 01:28:26 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:24 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:25 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:09:26 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:09:27 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:10:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 22 Jun 2022 04:10:05 GMT
ENV XWIKI_VERSION=14.4.1
# Wed, 22 Jun 2022 04:10:06 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.4.1
# Wed, 22 Jun 2022 04:10:07 GMT
ENV XWIKI_DOWNLOAD_SHA256=8e20eba50acee0f157d3cc160306d65e0995b453833c8923f833030f0a469fb4
# Wed, 22 Jun 2022 04:10:44 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 22 Jun 2022 04:10:45 GMT
ENV MYSQL_JDBC_VERSION=8.0.29
# Wed, 22 Jun 2022 04:10:45 GMT
ENV MYSQL_JDBC_SHA256=d4e32d2a6026b5acc00300b73a86c28fb92681ae9629b21048ee67014c911db6
# Wed, 22 Jun 2022 04:10:46 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.29
# Wed, 22 Jun 2022 04:10:47 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.29.jar
# Wed, 22 Jun 2022 04:10:48 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.29.jar
# Wed, 22 Jun 2022 04:10:50 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Wed, 22 Jun 2022 04:10:51 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 22 Jun 2022 04:10:52 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 22 Jun 2022 04:10:53 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 22 Jun 2022 04:10:54 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 22 Jun 2022 04:10:54 GMT
VOLUME [/usr/local/xwiki]
# Wed, 22 Jun 2022 04:10:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jun 2022 04:10:56 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15da1b4c110f7cc460fbf968fb55b77c541f0e3ab87b92d5e6a822cc2c593e1`  
		Last Modified: Tue, 07 Jun 2022 05:10:23 GMT  
		Size: 15.9 MB (15898299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8e9d6a15d13e6f2d5d43f40b76051350cb7090cfcae5300dc1647e3196577a`  
		Last Modified: Tue, 07 Jun 2022 06:44:15 GMT  
		Size: 41.6 MB (41608356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51219ca7d003431d2f9c6ddda7db0a1902cf2b7e4e879625811b086f268b39c`  
		Last Modified: Tue, 07 Jun 2022 06:44:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5aa4900f44b9e3e20168d54fda3a0b78e62d572de1796db20345b70b1d8b3ca`  
		Last Modified: Tue, 07 Jun 2022 11:23:12 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6796806c88914990f15047665e74a4ea1fb933bdf7b8ebf39b1f2a82b723e044`  
		Last Modified: Fri, 10 Jun 2022 02:03:21 GMT  
		Size: 12.3 MB (12264791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca37469fc5a6ebbc5f1a764aabd4ba48b92a85d1396b644e1139994fad2fa34e`  
		Last Modified: Fri, 10 Jun 2022 02:03:20 GMT  
		Size: 208.8 KB (208841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c24501792b443d8ecb222b1c49c98ee84d4d76016bdbf8ba61b488fa873f7f`  
		Last Modified: Wed, 22 Jun 2022 04:17:01 GMT  
		Size: 163.4 MB (163365370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d1bb494106d6d36bcf7dd967f0d881aa979803343f00918d55f105d5759bbe`  
		Last Modified: Wed, 22 Jun 2022 04:16:59 GMT  
		Size: 292.0 MB (291982622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a24595bb483532afb5982a7102104c4107076a079eeaa4d5fd0d776abe5a1543`  
		Last Modified: Wed, 22 Jun 2022 04:16:38 GMT  
		Size: 2.4 MB (2381177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff7c257d2e413a9084ca6e6cbd963fb66e757d99cd06e3bd96971b96b7ca0083`  
		Last Modified: Wed, 22 Jun 2022 04:16:37 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:343c1e7e3713943da3994aafca00d9f54df0f67fb6b20d86933ebe4a05623d0e`  
		Last Modified: Wed, 22 Jun 2022 04:16:37 GMT  
		Size: 2.3 KB (2309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e0fa83eef81ca126718a8c16fd8f17e6ead2f37ccfc6a8dbf8e2568d221ac0`  
		Last Modified: Wed, 22 Jun 2022 04:16:37 GMT  
		Size: 5.9 KB (5854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c0f8a5973921c322d0333259d28d3c3ab9fa848afe20830fa1aad3fa46743fc`  
		Last Modified: Wed, 22 Jun 2022 04:16:37 GMT  
		Size: 2.5 KB (2509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:postgres-tomcat`

```console
$ docker pull xwiki@sha256:1fabdb2e4da65c0abe19ecbaf0ff7ee43cfa94d27091c3d5748e8211ff99735d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:be2ec4361ef195cce3e9b320a91b407e3928431c94a7adb57af1f11044876bd6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **561.6 MB (561646591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d6170aaa002127cf799999888c4d5d58bc136c94008910619af04189b3825fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:14:23 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 00:14:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:58 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:59 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 06:30:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:30:41 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 06:30:41 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:30:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:35:57 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 06:35:58 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 00:18:07 GMT
COPY dir:360b17da945f7a5c4dcdc8b0602904442d98c06d17157280c607532ec8b6edaa in /usr/local/tomcat 
# Fri, 10 Jun 2022 00:18:12 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 00:18:13 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 00:18:13 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 00:18:13 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:26:27 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Wed, 22 Jun 2022 04:26:29 GMT
ENV XWIKI_VERSION=14.4.1
# Wed, 22 Jun 2022 04:26:29 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.4.1
# Wed, 22 Jun 2022 04:26:29 GMT
ENV XWIKI_DOWNLOAD_SHA256=8e20eba50acee0f157d3cc160306d65e0995b453833c8923f833030f0a469fb4
# Wed, 22 Jun 2022 04:27:07 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 22 Jun 2022 04:27:08 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Wed, 22 Jun 2022 04:27:08 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 22 Jun 2022 04:27:08 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 22 Jun 2022 04:27:09 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 22 Jun 2022 04:27:09 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 22 Jun 2022 04:27:09 GMT
VOLUME [/usr/local/xwiki]
# Wed, 22 Jun 2022 04:27:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jun 2022 04:27:09 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b669251e19038a24bd6cab0baab92077f23163880fac4701fb3efa564350732b`  
		Last Modified: Tue, 07 Jun 2022 00:21:34 GMT  
		Size: 43.3 MB (43267270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf45eff8a02bcdf7a96904e0dc534c78c89a5c860e224fa57780ef2fc2eab99e`  
		Last Modified: Tue, 07 Jun 2022 00:21:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246089a07769500a0adb027d1dc0efbb1254ee07d75dcdc6f8a3ceb8bae3e95f`  
		Last Modified: Tue, 07 Jun 2022 06:48:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3636fe8b4383f769da39b4c598b1e98b53b6d528e34e9d20fac5c17cfefcd866`  
		Last Modified: Fri, 10 Jun 2022 00:40:50 GMT  
		Size: 12.2 MB (12247499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0a0fd2a02961d2a1725c94d0c0f5670c51d5f5f9bad820a96e45791a5d7a32`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 445.5 KB (445476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beba28f927b0599e17785c8f69b8373e61c14da42247f7683f924f80ecae1439`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:657eec0a2bb289006e136ad46dbd1d85e8ff10712e1477c0fcacb617a19bb242`  
		Last Modified: Wed, 22 Jun 2022 04:31:12 GMT  
		Size: 168.3 MB (168293438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7336ce43765447d78aa2db6c3c2d06f343d8c461acf64bd26ad2da6cdb3802e9`  
		Last Modified: Wed, 22 Jun 2022 04:31:05 GMT  
		Size: 292.0 MB (291982439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed867fb2baa0895487cb447dc1687bb44e7fa6941a1ed692bc25262eb6c8ce84`  
		Last Modified: Wed, 22 Jun 2022 04:30:47 GMT  
		Size: 795.4 KB (795422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffb2ca6524e098e2552dc1ee3c9df3692d579ef2fe4d945c2aefab62c820dfef`  
		Last Modified: Wed, 22 Jun 2022 04:30:46 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7f44840360a683faa6f816201fff0fcc275d3c3c886e55bd98a5b77b283d9f2`  
		Last Modified: Wed, 22 Jun 2022 04:30:46 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea0454030911a4eba98666b0184b8c3241a86aaffd563ef77f78cf31f9103402`  
		Last Modified: Wed, 22 Jun 2022 04:30:46 GMT  
		Size: 5.9 KB (5854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e070314e7d3d33ac915c9e5d8719b2d00e3207754d5b335482a0e76137e50a`  
		Last Modified: Wed, 22 Jun 2022 04:30:46 GMT  
		Size: 2.5 KB (2503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:b3ce0cb6e854ea382295ea6bb0f34559cb20af7194ac7aa73e10036616745688
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.1 MB (554126019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:964c73cc655f5ead167b952f043637ed76a9a1e4fa99f78c8bc52620b48566db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:00:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:35:32 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 06:36:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:36:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:36:20 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 10:50:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 10:50:03 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 10:50:04 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 10:50:05 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 10:50:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:50:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:59:13 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 10:59:14 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 01:28:16 GMT
COPY dir:1fb0204bb532a7d63a0dd2d2677d66a70be0285454d27afba6780853636ba1ef in /usr/local/tomcat 
# Fri, 10 Jun 2022 01:28:22 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 01:28:24 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 01:28:25 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 01:28:26 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:24 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:25 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:09:26 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:09:27 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:11:42 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Wed, 22 Jun 2022 04:11:43 GMT
ENV XWIKI_VERSION=14.4.1
# Wed, 22 Jun 2022 04:11:43 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.4.1
# Wed, 22 Jun 2022 04:11:44 GMT
ENV XWIKI_DOWNLOAD_SHA256=8e20eba50acee0f157d3cc160306d65e0995b453833c8923f833030f0a469fb4
# Wed, 22 Jun 2022 04:12:23 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 22 Jun 2022 04:12:24 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Wed, 22 Jun 2022 04:12:25 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 22 Jun 2022 04:12:26 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 22 Jun 2022 04:12:27 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 22 Jun 2022 04:12:28 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 22 Jun 2022 04:12:28 GMT
VOLUME [/usr/local/xwiki]
# Wed, 22 Jun 2022 04:12:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jun 2022 04:12:30 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15da1b4c110f7cc460fbf968fb55b77c541f0e3ab87b92d5e6a822cc2c593e1`  
		Last Modified: Tue, 07 Jun 2022 05:10:23 GMT  
		Size: 15.9 MB (15898299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8e9d6a15d13e6f2d5d43f40b76051350cb7090cfcae5300dc1647e3196577a`  
		Last Modified: Tue, 07 Jun 2022 06:44:15 GMT  
		Size: 41.6 MB (41608356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51219ca7d003431d2f9c6ddda7db0a1902cf2b7e4e879625811b086f268b39c`  
		Last Modified: Tue, 07 Jun 2022 06:44:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5aa4900f44b9e3e20168d54fda3a0b78e62d572de1796db20345b70b1d8b3ca`  
		Last Modified: Tue, 07 Jun 2022 11:23:12 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6796806c88914990f15047665e74a4ea1fb933bdf7b8ebf39b1f2a82b723e044`  
		Last Modified: Fri, 10 Jun 2022 02:03:21 GMT  
		Size: 12.3 MB (12264791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca37469fc5a6ebbc5f1a764aabd4ba48b92a85d1396b644e1139994fad2fa34e`  
		Last Modified: Fri, 10 Jun 2022 02:03:20 GMT  
		Size: 208.8 KB (208841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbf4753a12af2d02fd26a953119f6843f7e381cfec0d679d92b04b4e4f5a3d6a`  
		Last Modified: Wed, 22 Jun 2022 04:18:08 GMT  
		Size: 164.2 MB (164164156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8735ad3b7140d98c3eedfd5e132b33810f9ccbd2ef89e37d738de84113c7dc92`  
		Last Modified: Wed, 22 Jun 2022 04:18:07 GMT  
		Size: 292.0 MB (291982533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e05d15dcdbfe55730845a86712aea5417820a8fc73ea492391f4bc8773f273c`  
		Last Modified: Wed, 22 Jun 2022 04:17:46 GMT  
		Size: 795.4 KB (795416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ed4588b795d5cf65bf69167563114888c0924eec209d7f1a1f2f78f04f2e42`  
		Last Modified: Wed, 22 Jun 2022 04:17:45 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f537181948e5040a35cd0252682f25858131a6b14dd2a0cc0f8e9d4deb3dff1`  
		Last Modified: Wed, 22 Jun 2022 04:17:45 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f44b9ff69abe9f98824c9cccb73f52b56acccad5bf10bbf6df522ad974eb8fec`  
		Last Modified: Wed, 22 Jun 2022 04:17:45 GMT  
		Size: 5.9 KB (5851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f781c1d839ed0cddf10a24f41ffa5dc32da0de94c89077f83fd5f3cfa0c62ed6`  
		Last Modified: Wed, 22 Jun 2022 04:17:45 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:stable`

```console
$ docker pull xwiki@sha256:8b941b575bfdc8c0eb31d9b7f3422c6fe866062a7b465d725d53ec4107ca6144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:stable` - linux; amd64

```console
$ docker pull xwiki@sha256:f08dab318ed8416b7ef8fc05f68b5c11c7f486d1b4686584b35fbf916cb81081
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.4 MB (562431476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68a5a2c9d16899b288b020a4b618dae8b4a2aa67718272532c3f92b8caca60fd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:14:23 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 00:14:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:58 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:59 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 06:30:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:30:41 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 06:30:41 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:30:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:35:57 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 06:35:58 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 00:18:07 GMT
COPY dir:360b17da945f7a5c4dcdc8b0602904442d98c06d17157280c607532ec8b6edaa in /usr/local/tomcat 
# Fri, 10 Jun 2022 00:18:12 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 00:18:13 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 00:18:13 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 00:18:13 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:25:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 22 Jun 2022 04:25:05 GMT
ENV XWIKI_VERSION=14.4.1
# Wed, 22 Jun 2022 04:25:05 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.4.1
# Wed, 22 Jun 2022 04:25:05 GMT
ENV XWIKI_DOWNLOAD_SHA256=8e20eba50acee0f157d3cc160306d65e0995b453833c8923f833030f0a469fb4
# Wed, 22 Jun 2022 04:25:42 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 22 Jun 2022 04:25:43 GMT
ENV MYSQL_JDBC_VERSION=8.0.29
# Wed, 22 Jun 2022 04:25:43 GMT
ENV MYSQL_JDBC_SHA256=d4e32d2a6026b5acc00300b73a86c28fb92681ae9629b21048ee67014c911db6
# Wed, 22 Jun 2022 04:25:43 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.29
# Wed, 22 Jun 2022 04:25:43 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.29.jar
# Wed, 22 Jun 2022 04:25:44 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.29.jar
# Wed, 22 Jun 2022 04:25:44 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Wed, 22 Jun 2022 04:25:44 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 22 Jun 2022 04:25:44 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 22 Jun 2022 04:25:45 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 22 Jun 2022 04:25:45 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 22 Jun 2022 04:25:45 GMT
VOLUME [/usr/local/xwiki]
# Wed, 22 Jun 2022 04:25:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jun 2022 04:25:45 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b669251e19038a24bd6cab0baab92077f23163880fac4701fb3efa564350732b`  
		Last Modified: Tue, 07 Jun 2022 00:21:34 GMT  
		Size: 43.3 MB (43267270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf45eff8a02bcdf7a96904e0dc534c78c89a5c860e224fa57780ef2fc2eab99e`  
		Last Modified: Tue, 07 Jun 2022 00:21:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246089a07769500a0adb027d1dc0efbb1254ee07d75dcdc6f8a3ceb8bae3e95f`  
		Last Modified: Tue, 07 Jun 2022 06:48:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3636fe8b4383f769da39b4c598b1e98b53b6d528e34e9d20fac5c17cfefcd866`  
		Last Modified: Fri, 10 Jun 2022 00:40:50 GMT  
		Size: 12.2 MB (12247499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0a0fd2a02961d2a1725c94d0c0f5670c51d5f5f9bad820a96e45791a5d7a32`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 445.5 KB (445476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beba28f927b0599e17785c8f69b8373e61c14da42247f7683f924f80ecae1439`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c54774971cb7c57e8fe14a42f90f7e4cceb67150ff2f3112f9ad46fea390190d`  
		Last Modified: Wed, 22 Jun 2022 04:30:07 GMT  
		Size: 167.5 MB (167492656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:368fa3670d498d9bc0883cd81cf9b9a45d3ccf79365eabe27b779344efefda58`  
		Last Modified: Wed, 22 Jun 2022 04:30:00 GMT  
		Size: 292.0 MB (291982499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb96a08b07f52ad5c126f31fe742e1c114a3239ab5c6fc5641266fa5be00579`  
		Last Modified: Wed, 22 Jun 2022 04:29:42 GMT  
		Size: 2.4 MB (2381172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94af0360a2e049892f0b11539619a1e889f32dcdec1df1a671ffb6032f55437`  
		Last Modified: Wed, 22 Jun 2022 04:29:41 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7255f65a4fc48ef292f0f13fc58a9f76e18f7f3969190698a08ff5907c9e5dd`  
		Last Modified: Wed, 22 Jun 2022 04:29:41 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1695b6d1dbcfb2018bc0a46ec5c66b47f1105c4aff382726932ee462014d294e`  
		Last Modified: Wed, 22 Jun 2022 04:29:41 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec62f61e9a4c7f7d90e61399a76eb18b02a789afbac8e9fcaaa1f8ebc6b10da`  
		Last Modified: Wed, 22 Jun 2022 04:29:41 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:stable` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:b4d50e1906ede668b41d744d6050b179dc5523658ba13b4e4cc5a92b98955a71
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.9 MB (554912952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed7a93d82de140d630b2eab42fb4270590bb2efcab4d72dd5a2f2dd8ce842278`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:00:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:35:32 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 06:36:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:36:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:36:20 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 10:50:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 10:50:03 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 10:50:04 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 10:50:05 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 10:50:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:50:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:59:13 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 10:59:14 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 01:28:16 GMT
COPY dir:1fb0204bb532a7d63a0dd2d2677d66a70be0285454d27afba6780853636ba1ef in /usr/local/tomcat 
# Fri, 10 Jun 2022 01:28:22 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 01:28:24 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 01:28:25 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 01:28:26 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:24 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:25 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:09:26 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:09:27 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:10:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 22 Jun 2022 04:10:05 GMT
ENV XWIKI_VERSION=14.4.1
# Wed, 22 Jun 2022 04:10:06 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.4.1
# Wed, 22 Jun 2022 04:10:07 GMT
ENV XWIKI_DOWNLOAD_SHA256=8e20eba50acee0f157d3cc160306d65e0995b453833c8923f833030f0a469fb4
# Wed, 22 Jun 2022 04:10:44 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 22 Jun 2022 04:10:45 GMT
ENV MYSQL_JDBC_VERSION=8.0.29
# Wed, 22 Jun 2022 04:10:45 GMT
ENV MYSQL_JDBC_SHA256=d4e32d2a6026b5acc00300b73a86c28fb92681ae9629b21048ee67014c911db6
# Wed, 22 Jun 2022 04:10:46 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.29
# Wed, 22 Jun 2022 04:10:47 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.29.jar
# Wed, 22 Jun 2022 04:10:48 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.29.jar
# Wed, 22 Jun 2022 04:10:50 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Wed, 22 Jun 2022 04:10:51 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 22 Jun 2022 04:10:52 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 22 Jun 2022 04:10:53 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 22 Jun 2022 04:10:54 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 22 Jun 2022 04:10:54 GMT
VOLUME [/usr/local/xwiki]
# Wed, 22 Jun 2022 04:10:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jun 2022 04:10:56 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15da1b4c110f7cc460fbf968fb55b77c541f0e3ab87b92d5e6a822cc2c593e1`  
		Last Modified: Tue, 07 Jun 2022 05:10:23 GMT  
		Size: 15.9 MB (15898299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8e9d6a15d13e6f2d5d43f40b76051350cb7090cfcae5300dc1647e3196577a`  
		Last Modified: Tue, 07 Jun 2022 06:44:15 GMT  
		Size: 41.6 MB (41608356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51219ca7d003431d2f9c6ddda7db0a1902cf2b7e4e879625811b086f268b39c`  
		Last Modified: Tue, 07 Jun 2022 06:44:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5aa4900f44b9e3e20168d54fda3a0b78e62d572de1796db20345b70b1d8b3ca`  
		Last Modified: Tue, 07 Jun 2022 11:23:12 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6796806c88914990f15047665e74a4ea1fb933bdf7b8ebf39b1f2a82b723e044`  
		Last Modified: Fri, 10 Jun 2022 02:03:21 GMT  
		Size: 12.3 MB (12264791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca37469fc5a6ebbc5f1a764aabd4ba48b92a85d1396b644e1139994fad2fa34e`  
		Last Modified: Fri, 10 Jun 2022 02:03:20 GMT  
		Size: 208.8 KB (208841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c24501792b443d8ecb222b1c49c98ee84d4d76016bdbf8ba61b488fa873f7f`  
		Last Modified: Wed, 22 Jun 2022 04:17:01 GMT  
		Size: 163.4 MB (163365370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d1bb494106d6d36bcf7dd967f0d881aa979803343f00918d55f105d5759bbe`  
		Last Modified: Wed, 22 Jun 2022 04:16:59 GMT  
		Size: 292.0 MB (291982622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a24595bb483532afb5982a7102104c4107076a079eeaa4d5fd0d776abe5a1543`  
		Last Modified: Wed, 22 Jun 2022 04:16:38 GMT  
		Size: 2.4 MB (2381177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff7c257d2e413a9084ca6e6cbd963fb66e757d99cd06e3bd96971b96b7ca0083`  
		Last Modified: Wed, 22 Jun 2022 04:16:37 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:343c1e7e3713943da3994aafca00d9f54df0f67fb6b20d86933ebe4a05623d0e`  
		Last Modified: Wed, 22 Jun 2022 04:16:37 GMT  
		Size: 2.3 KB (2309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e0fa83eef81ca126718a8c16fd8f17e6ead2f37ccfc6a8dbf8e2568d221ac0`  
		Last Modified: Wed, 22 Jun 2022 04:16:37 GMT  
		Size: 5.9 KB (5854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c0f8a5973921c322d0333259d28d3c3ab9fa848afe20830fa1aad3fa46743fc`  
		Last Modified: Wed, 22 Jun 2022 04:16:37 GMT  
		Size: 2.5 KB (2509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:stable-mariadb`

```console
$ docker pull xwiki@sha256:3db745735e3f4998cf83b2a5dc35cd5b861564cac0ff1f91425512cc46c054ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:stable-mariadb` - linux; amd64

```console
$ docker pull xwiki@sha256:5be2c4cf71703a8afc1dc6cd56002d86482ca326367b5a080809603ece9ae80a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.6 MB (560590373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7416cc5f4b70e5175c8fecfe02fb114cdab2e1b5150287649b6d3524c2bcd556`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:14:23 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 00:14:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:58 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:59 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 06:30:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:30:41 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 06:30:41 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:30:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:35:57 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 06:35:58 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 00:18:07 GMT
COPY dir:360b17da945f7a5c4dcdc8b0602904442d98c06d17157280c607532ec8b6edaa in /usr/local/tomcat 
# Fri, 10 Jun 2022 00:18:12 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 00:18:13 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 00:18:13 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 00:18:13 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:25:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 22 Jun 2022 04:25:05 GMT
ENV XWIKI_VERSION=14.4.1
# Wed, 22 Jun 2022 04:25:05 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.4.1
# Wed, 22 Jun 2022 04:25:05 GMT
ENV XWIKI_DOWNLOAD_SHA256=8e20eba50acee0f157d3cc160306d65e0995b453833c8923f833030f0a469fb4
# Wed, 22 Jun 2022 04:25:42 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 22 Jun 2022 04:27:20 GMT
ENV MARIADB_JDBC_VERSION=3.0.5
# Wed, 22 Jun 2022 04:27:20 GMT
ENV MARIADB_JDBC_SHA256=e9532d9bca07c1263c32b00b495bd3ec7f2b79320513cabd762bf39ea09e68d9
# Wed, 22 Jun 2022 04:27:20 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.0.5
# Wed, 22 Jun 2022 04:27:20 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.0.5.jar
# Wed, 22 Jun 2022 04:27:20 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.0.5.jar
# Wed, 22 Jun 2022 04:27:21 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Wed, 22 Jun 2022 04:27:21 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 22 Jun 2022 04:27:21 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 22 Jun 2022 04:27:22 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 22 Jun 2022 04:27:22 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 22 Jun 2022 04:27:22 GMT
VOLUME [/usr/local/xwiki]
# Wed, 22 Jun 2022 04:27:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jun 2022 04:27:22 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b669251e19038a24bd6cab0baab92077f23163880fac4701fb3efa564350732b`  
		Last Modified: Tue, 07 Jun 2022 00:21:34 GMT  
		Size: 43.3 MB (43267270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf45eff8a02bcdf7a96904e0dc534c78c89a5c860e224fa57780ef2fc2eab99e`  
		Last Modified: Tue, 07 Jun 2022 00:21:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246089a07769500a0adb027d1dc0efbb1254ee07d75dcdc6f8a3ceb8bae3e95f`  
		Last Modified: Tue, 07 Jun 2022 06:48:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3636fe8b4383f769da39b4c598b1e98b53b6d528e34e9d20fac5c17cfefcd866`  
		Last Modified: Fri, 10 Jun 2022 00:40:50 GMT  
		Size: 12.2 MB (12247499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0a0fd2a02961d2a1725c94d0c0f5670c51d5f5f9bad820a96e45791a5d7a32`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 445.5 KB (445476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beba28f927b0599e17785c8f69b8373e61c14da42247f7683f924f80ecae1439`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c54774971cb7c57e8fe14a42f90f7e4cceb67150ff2f3112f9ad46fea390190d`  
		Last Modified: Wed, 22 Jun 2022 04:30:07 GMT  
		Size: 167.5 MB (167492656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:368fa3670d498d9bc0883cd81cf9b9a45d3ccf79365eabe27b779344efefda58`  
		Last Modified: Wed, 22 Jun 2022 04:30:00 GMT  
		Size: 292.0 MB (291982499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c1ab918c0e0ec1820084e4da9e0f385f44acb6a9a2c61f37cba3191a960dec1`  
		Last Modified: Wed, 22 Jun 2022 04:31:36 GMT  
		Size: 540.1 KB (540065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2359c2da84be359f352d0435136b09e78a9776b1d22b4dbdd3f6fec942973375`  
		Last Modified: Wed, 22 Jun 2022 04:31:36 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9269ef1e91c8bcc8306aee08c0a04ec885a56ef859428b65c847bec5ddf4d5ce`  
		Last Modified: Wed, 22 Jun 2022 04:31:35 GMT  
		Size: 2.3 KB (2309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b60d3cde6a56696f82809b7ff8a140448d3abe21f2778008cd1c92705cd8cb`  
		Last Modified: Wed, 22 Jun 2022 04:31:35 GMT  
		Size: 5.9 KB (5856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d320a8df62dc7b14288e1ee93b18d239e5ac432d1ac8aab55e511dcbdfbc27`  
		Last Modified: Wed, 22 Jun 2022 04:31:35 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:stable-mariadb` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:bda93d405e13407149f8f73a5894a9ac80b447f92ade102dcb003d1fbd9e8a7f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **553.1 MB (553071844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ee73663f1cd3949cf5e95503adb5d84ae70153601cd42f36eea35f77b61d0b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:00:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:35:32 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 06:36:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:36:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:36:20 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 10:50:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 10:50:03 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 10:50:04 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 10:50:05 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 10:50:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:50:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:59:13 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 10:59:14 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 01:28:16 GMT
COPY dir:1fb0204bb532a7d63a0dd2d2677d66a70be0285454d27afba6780853636ba1ef in /usr/local/tomcat 
# Fri, 10 Jun 2022 01:28:22 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 01:28:24 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 01:28:25 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 01:28:26 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:24 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:25 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:09:26 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:09:27 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:10:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 22 Jun 2022 04:10:05 GMT
ENV XWIKI_VERSION=14.4.1
# Wed, 22 Jun 2022 04:10:06 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.4.1
# Wed, 22 Jun 2022 04:10:07 GMT
ENV XWIKI_DOWNLOAD_SHA256=8e20eba50acee0f157d3cc160306d65e0995b453833c8923f833030f0a469fb4
# Wed, 22 Jun 2022 04:10:44 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 22 Jun 2022 04:12:47 GMT
ENV MARIADB_JDBC_VERSION=3.0.5
# Wed, 22 Jun 2022 04:12:48 GMT
ENV MARIADB_JDBC_SHA256=e9532d9bca07c1263c32b00b495bd3ec7f2b79320513cabd762bf39ea09e68d9
# Wed, 22 Jun 2022 04:12:49 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.0.5
# Wed, 22 Jun 2022 04:12:50 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.0.5.jar
# Wed, 22 Jun 2022 04:12:51 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.0.5.jar
# Wed, 22 Jun 2022 04:12:53 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Wed, 22 Jun 2022 04:12:54 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 22 Jun 2022 04:12:55 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 22 Jun 2022 04:12:56 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 22 Jun 2022 04:12:57 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 22 Jun 2022 04:12:57 GMT
VOLUME [/usr/local/xwiki]
# Wed, 22 Jun 2022 04:12:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jun 2022 04:12:59 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15da1b4c110f7cc460fbf968fb55b77c541f0e3ab87b92d5e6a822cc2c593e1`  
		Last Modified: Tue, 07 Jun 2022 05:10:23 GMT  
		Size: 15.9 MB (15898299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8e9d6a15d13e6f2d5d43f40b76051350cb7090cfcae5300dc1647e3196577a`  
		Last Modified: Tue, 07 Jun 2022 06:44:15 GMT  
		Size: 41.6 MB (41608356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51219ca7d003431d2f9c6ddda7db0a1902cf2b7e4e879625811b086f268b39c`  
		Last Modified: Tue, 07 Jun 2022 06:44:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5aa4900f44b9e3e20168d54fda3a0b78e62d572de1796db20345b70b1d8b3ca`  
		Last Modified: Tue, 07 Jun 2022 11:23:12 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6796806c88914990f15047665e74a4ea1fb933bdf7b8ebf39b1f2a82b723e044`  
		Last Modified: Fri, 10 Jun 2022 02:03:21 GMT  
		Size: 12.3 MB (12264791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca37469fc5a6ebbc5f1a764aabd4ba48b92a85d1396b644e1139994fad2fa34e`  
		Last Modified: Fri, 10 Jun 2022 02:03:20 GMT  
		Size: 208.8 KB (208841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c24501792b443d8ecb222b1c49c98ee84d4d76016bdbf8ba61b488fa873f7f`  
		Last Modified: Wed, 22 Jun 2022 04:17:01 GMT  
		Size: 163.4 MB (163365370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d1bb494106d6d36bcf7dd967f0d881aa979803343f00918d55f105d5759bbe`  
		Last Modified: Wed, 22 Jun 2022 04:16:59 GMT  
		Size: 292.0 MB (291982622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba0bfc714e56ec603906f85a8dacd34f5dad693a8c6dbcf8a9567fbca423d16`  
		Last Modified: Wed, 22 Jun 2022 04:18:35 GMT  
		Size: 540.1 KB (540069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e192a89ffea555829e044cd56b10c8021a547d8a56e5a69c0a6714bb461f596d`  
		Last Modified: Wed, 22 Jun 2022 04:18:35 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc8a81604a8c8778019d65f20d4893ebf3957eadbc949f6c2ca6a5ede778ba6d`  
		Last Modified: Wed, 22 Jun 2022 04:18:35 GMT  
		Size: 2.3 KB (2311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d62f47e27689a9f1dfc33daa4881e9da0078b7620dbb8c9c520858ac340b8fb4`  
		Last Modified: Wed, 22 Jun 2022 04:18:34 GMT  
		Size: 5.9 KB (5854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:542f6bbdec9617d4401973008c85e7ea003f6f336c453085de1f99098e8911e4`  
		Last Modified: Wed, 22 Jun 2022 04:18:34 GMT  
		Size: 2.5 KB (2507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:stable-mariadb-tomcat`

```console
$ docker pull xwiki@sha256:3db745735e3f4998cf83b2a5dc35cd5b861564cac0ff1f91425512cc46c054ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:stable-mariadb-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:5be2c4cf71703a8afc1dc6cd56002d86482ca326367b5a080809603ece9ae80a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.6 MB (560590373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7416cc5f4b70e5175c8fecfe02fb114cdab2e1b5150287649b6d3524c2bcd556`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:14:23 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 00:14:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:58 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:59 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 06:30:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:30:41 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 06:30:41 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:30:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:35:57 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 06:35:58 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 00:18:07 GMT
COPY dir:360b17da945f7a5c4dcdc8b0602904442d98c06d17157280c607532ec8b6edaa in /usr/local/tomcat 
# Fri, 10 Jun 2022 00:18:12 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 00:18:13 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 00:18:13 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 00:18:13 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:25:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 22 Jun 2022 04:25:05 GMT
ENV XWIKI_VERSION=14.4.1
# Wed, 22 Jun 2022 04:25:05 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.4.1
# Wed, 22 Jun 2022 04:25:05 GMT
ENV XWIKI_DOWNLOAD_SHA256=8e20eba50acee0f157d3cc160306d65e0995b453833c8923f833030f0a469fb4
# Wed, 22 Jun 2022 04:25:42 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 22 Jun 2022 04:27:20 GMT
ENV MARIADB_JDBC_VERSION=3.0.5
# Wed, 22 Jun 2022 04:27:20 GMT
ENV MARIADB_JDBC_SHA256=e9532d9bca07c1263c32b00b495bd3ec7f2b79320513cabd762bf39ea09e68d9
# Wed, 22 Jun 2022 04:27:20 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.0.5
# Wed, 22 Jun 2022 04:27:20 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.0.5.jar
# Wed, 22 Jun 2022 04:27:20 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.0.5.jar
# Wed, 22 Jun 2022 04:27:21 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Wed, 22 Jun 2022 04:27:21 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 22 Jun 2022 04:27:21 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 22 Jun 2022 04:27:22 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 22 Jun 2022 04:27:22 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 22 Jun 2022 04:27:22 GMT
VOLUME [/usr/local/xwiki]
# Wed, 22 Jun 2022 04:27:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jun 2022 04:27:22 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b669251e19038a24bd6cab0baab92077f23163880fac4701fb3efa564350732b`  
		Last Modified: Tue, 07 Jun 2022 00:21:34 GMT  
		Size: 43.3 MB (43267270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf45eff8a02bcdf7a96904e0dc534c78c89a5c860e224fa57780ef2fc2eab99e`  
		Last Modified: Tue, 07 Jun 2022 00:21:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246089a07769500a0adb027d1dc0efbb1254ee07d75dcdc6f8a3ceb8bae3e95f`  
		Last Modified: Tue, 07 Jun 2022 06:48:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3636fe8b4383f769da39b4c598b1e98b53b6d528e34e9d20fac5c17cfefcd866`  
		Last Modified: Fri, 10 Jun 2022 00:40:50 GMT  
		Size: 12.2 MB (12247499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0a0fd2a02961d2a1725c94d0c0f5670c51d5f5f9bad820a96e45791a5d7a32`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 445.5 KB (445476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beba28f927b0599e17785c8f69b8373e61c14da42247f7683f924f80ecae1439`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c54774971cb7c57e8fe14a42f90f7e4cceb67150ff2f3112f9ad46fea390190d`  
		Last Modified: Wed, 22 Jun 2022 04:30:07 GMT  
		Size: 167.5 MB (167492656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:368fa3670d498d9bc0883cd81cf9b9a45d3ccf79365eabe27b779344efefda58`  
		Last Modified: Wed, 22 Jun 2022 04:30:00 GMT  
		Size: 292.0 MB (291982499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c1ab918c0e0ec1820084e4da9e0f385f44acb6a9a2c61f37cba3191a960dec1`  
		Last Modified: Wed, 22 Jun 2022 04:31:36 GMT  
		Size: 540.1 KB (540065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2359c2da84be359f352d0435136b09e78a9776b1d22b4dbdd3f6fec942973375`  
		Last Modified: Wed, 22 Jun 2022 04:31:36 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9269ef1e91c8bcc8306aee08c0a04ec885a56ef859428b65c847bec5ddf4d5ce`  
		Last Modified: Wed, 22 Jun 2022 04:31:35 GMT  
		Size: 2.3 KB (2309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b60d3cde6a56696f82809b7ff8a140448d3abe21f2778008cd1c92705cd8cb`  
		Last Modified: Wed, 22 Jun 2022 04:31:35 GMT  
		Size: 5.9 KB (5856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d320a8df62dc7b14288e1ee93b18d239e5ac432d1ac8aab55e511dcbdfbc27`  
		Last Modified: Wed, 22 Jun 2022 04:31:35 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:stable-mariadb-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:bda93d405e13407149f8f73a5894a9ac80b447f92ade102dcb003d1fbd9e8a7f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **553.1 MB (553071844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ee73663f1cd3949cf5e95503adb5d84ae70153601cd42f36eea35f77b61d0b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:00:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:35:32 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 06:36:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:36:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:36:20 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 10:50:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 10:50:03 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 10:50:04 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 10:50:05 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 10:50:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:50:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:59:13 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 10:59:14 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 01:28:16 GMT
COPY dir:1fb0204bb532a7d63a0dd2d2677d66a70be0285454d27afba6780853636ba1ef in /usr/local/tomcat 
# Fri, 10 Jun 2022 01:28:22 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 01:28:24 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 01:28:25 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 01:28:26 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:24 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:25 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:09:26 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:09:27 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:10:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 22 Jun 2022 04:10:05 GMT
ENV XWIKI_VERSION=14.4.1
# Wed, 22 Jun 2022 04:10:06 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.4.1
# Wed, 22 Jun 2022 04:10:07 GMT
ENV XWIKI_DOWNLOAD_SHA256=8e20eba50acee0f157d3cc160306d65e0995b453833c8923f833030f0a469fb4
# Wed, 22 Jun 2022 04:10:44 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 22 Jun 2022 04:12:47 GMT
ENV MARIADB_JDBC_VERSION=3.0.5
# Wed, 22 Jun 2022 04:12:48 GMT
ENV MARIADB_JDBC_SHA256=e9532d9bca07c1263c32b00b495bd3ec7f2b79320513cabd762bf39ea09e68d9
# Wed, 22 Jun 2022 04:12:49 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.0.5
# Wed, 22 Jun 2022 04:12:50 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.0.5.jar
# Wed, 22 Jun 2022 04:12:51 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.0.5.jar
# Wed, 22 Jun 2022 04:12:53 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Wed, 22 Jun 2022 04:12:54 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 22 Jun 2022 04:12:55 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 22 Jun 2022 04:12:56 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 22 Jun 2022 04:12:57 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 22 Jun 2022 04:12:57 GMT
VOLUME [/usr/local/xwiki]
# Wed, 22 Jun 2022 04:12:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jun 2022 04:12:59 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15da1b4c110f7cc460fbf968fb55b77c541f0e3ab87b92d5e6a822cc2c593e1`  
		Last Modified: Tue, 07 Jun 2022 05:10:23 GMT  
		Size: 15.9 MB (15898299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8e9d6a15d13e6f2d5d43f40b76051350cb7090cfcae5300dc1647e3196577a`  
		Last Modified: Tue, 07 Jun 2022 06:44:15 GMT  
		Size: 41.6 MB (41608356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51219ca7d003431d2f9c6ddda7db0a1902cf2b7e4e879625811b086f268b39c`  
		Last Modified: Tue, 07 Jun 2022 06:44:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5aa4900f44b9e3e20168d54fda3a0b78e62d572de1796db20345b70b1d8b3ca`  
		Last Modified: Tue, 07 Jun 2022 11:23:12 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6796806c88914990f15047665e74a4ea1fb933bdf7b8ebf39b1f2a82b723e044`  
		Last Modified: Fri, 10 Jun 2022 02:03:21 GMT  
		Size: 12.3 MB (12264791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca37469fc5a6ebbc5f1a764aabd4ba48b92a85d1396b644e1139994fad2fa34e`  
		Last Modified: Fri, 10 Jun 2022 02:03:20 GMT  
		Size: 208.8 KB (208841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c24501792b443d8ecb222b1c49c98ee84d4d76016bdbf8ba61b488fa873f7f`  
		Last Modified: Wed, 22 Jun 2022 04:17:01 GMT  
		Size: 163.4 MB (163365370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d1bb494106d6d36bcf7dd967f0d881aa979803343f00918d55f105d5759bbe`  
		Last Modified: Wed, 22 Jun 2022 04:16:59 GMT  
		Size: 292.0 MB (291982622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba0bfc714e56ec603906f85a8dacd34f5dad693a8c6dbcf8a9567fbca423d16`  
		Last Modified: Wed, 22 Jun 2022 04:18:35 GMT  
		Size: 540.1 KB (540069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e192a89ffea555829e044cd56b10c8021a547d8a56e5a69c0a6714bb461f596d`  
		Last Modified: Wed, 22 Jun 2022 04:18:35 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc8a81604a8c8778019d65f20d4893ebf3957eadbc949f6c2ca6a5ede778ba6d`  
		Last Modified: Wed, 22 Jun 2022 04:18:35 GMT  
		Size: 2.3 KB (2311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d62f47e27689a9f1dfc33daa4881e9da0078b7620dbb8c9c520858ac340b8fb4`  
		Last Modified: Wed, 22 Jun 2022 04:18:34 GMT  
		Size: 5.9 KB (5854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:542f6bbdec9617d4401973008c85e7ea003f6f336c453085de1f99098e8911e4`  
		Last Modified: Wed, 22 Jun 2022 04:18:34 GMT  
		Size: 2.5 KB (2507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:stable-mysql`

```console
$ docker pull xwiki@sha256:8b941b575bfdc8c0eb31d9b7f3422c6fe866062a7b465d725d53ec4107ca6144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:stable-mysql` - linux; amd64

```console
$ docker pull xwiki@sha256:f08dab318ed8416b7ef8fc05f68b5c11c7f486d1b4686584b35fbf916cb81081
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.4 MB (562431476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68a5a2c9d16899b288b020a4b618dae8b4a2aa67718272532c3f92b8caca60fd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:14:23 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 00:14:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:58 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:59 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 06:30:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:30:41 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 06:30:41 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:30:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:35:57 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 06:35:58 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 00:18:07 GMT
COPY dir:360b17da945f7a5c4dcdc8b0602904442d98c06d17157280c607532ec8b6edaa in /usr/local/tomcat 
# Fri, 10 Jun 2022 00:18:12 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 00:18:13 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 00:18:13 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 00:18:13 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:25:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 22 Jun 2022 04:25:05 GMT
ENV XWIKI_VERSION=14.4.1
# Wed, 22 Jun 2022 04:25:05 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.4.1
# Wed, 22 Jun 2022 04:25:05 GMT
ENV XWIKI_DOWNLOAD_SHA256=8e20eba50acee0f157d3cc160306d65e0995b453833c8923f833030f0a469fb4
# Wed, 22 Jun 2022 04:25:42 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 22 Jun 2022 04:25:43 GMT
ENV MYSQL_JDBC_VERSION=8.0.29
# Wed, 22 Jun 2022 04:25:43 GMT
ENV MYSQL_JDBC_SHA256=d4e32d2a6026b5acc00300b73a86c28fb92681ae9629b21048ee67014c911db6
# Wed, 22 Jun 2022 04:25:43 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.29
# Wed, 22 Jun 2022 04:25:43 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.29.jar
# Wed, 22 Jun 2022 04:25:44 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.29.jar
# Wed, 22 Jun 2022 04:25:44 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Wed, 22 Jun 2022 04:25:44 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 22 Jun 2022 04:25:44 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 22 Jun 2022 04:25:45 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 22 Jun 2022 04:25:45 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 22 Jun 2022 04:25:45 GMT
VOLUME [/usr/local/xwiki]
# Wed, 22 Jun 2022 04:25:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jun 2022 04:25:45 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b669251e19038a24bd6cab0baab92077f23163880fac4701fb3efa564350732b`  
		Last Modified: Tue, 07 Jun 2022 00:21:34 GMT  
		Size: 43.3 MB (43267270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf45eff8a02bcdf7a96904e0dc534c78c89a5c860e224fa57780ef2fc2eab99e`  
		Last Modified: Tue, 07 Jun 2022 00:21:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246089a07769500a0adb027d1dc0efbb1254ee07d75dcdc6f8a3ceb8bae3e95f`  
		Last Modified: Tue, 07 Jun 2022 06:48:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3636fe8b4383f769da39b4c598b1e98b53b6d528e34e9d20fac5c17cfefcd866`  
		Last Modified: Fri, 10 Jun 2022 00:40:50 GMT  
		Size: 12.2 MB (12247499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0a0fd2a02961d2a1725c94d0c0f5670c51d5f5f9bad820a96e45791a5d7a32`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 445.5 KB (445476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beba28f927b0599e17785c8f69b8373e61c14da42247f7683f924f80ecae1439`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c54774971cb7c57e8fe14a42f90f7e4cceb67150ff2f3112f9ad46fea390190d`  
		Last Modified: Wed, 22 Jun 2022 04:30:07 GMT  
		Size: 167.5 MB (167492656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:368fa3670d498d9bc0883cd81cf9b9a45d3ccf79365eabe27b779344efefda58`  
		Last Modified: Wed, 22 Jun 2022 04:30:00 GMT  
		Size: 292.0 MB (291982499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb96a08b07f52ad5c126f31fe742e1c114a3239ab5c6fc5641266fa5be00579`  
		Last Modified: Wed, 22 Jun 2022 04:29:42 GMT  
		Size: 2.4 MB (2381172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94af0360a2e049892f0b11539619a1e889f32dcdec1df1a671ffb6032f55437`  
		Last Modified: Wed, 22 Jun 2022 04:29:41 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7255f65a4fc48ef292f0f13fc58a9f76e18f7f3969190698a08ff5907c9e5dd`  
		Last Modified: Wed, 22 Jun 2022 04:29:41 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1695b6d1dbcfb2018bc0a46ec5c66b47f1105c4aff382726932ee462014d294e`  
		Last Modified: Wed, 22 Jun 2022 04:29:41 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec62f61e9a4c7f7d90e61399a76eb18b02a789afbac8e9fcaaa1f8ebc6b10da`  
		Last Modified: Wed, 22 Jun 2022 04:29:41 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:stable-mysql` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:b4d50e1906ede668b41d744d6050b179dc5523658ba13b4e4cc5a92b98955a71
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.9 MB (554912952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed7a93d82de140d630b2eab42fb4270590bb2efcab4d72dd5a2f2dd8ce842278`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:00:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:35:32 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 06:36:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:36:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:36:20 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 10:50:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 10:50:03 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 10:50:04 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 10:50:05 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 10:50:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:50:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:59:13 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 10:59:14 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 01:28:16 GMT
COPY dir:1fb0204bb532a7d63a0dd2d2677d66a70be0285454d27afba6780853636ba1ef in /usr/local/tomcat 
# Fri, 10 Jun 2022 01:28:22 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 01:28:24 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 01:28:25 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 01:28:26 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:24 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:25 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:09:26 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:09:27 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:10:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 22 Jun 2022 04:10:05 GMT
ENV XWIKI_VERSION=14.4.1
# Wed, 22 Jun 2022 04:10:06 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.4.1
# Wed, 22 Jun 2022 04:10:07 GMT
ENV XWIKI_DOWNLOAD_SHA256=8e20eba50acee0f157d3cc160306d65e0995b453833c8923f833030f0a469fb4
# Wed, 22 Jun 2022 04:10:44 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 22 Jun 2022 04:10:45 GMT
ENV MYSQL_JDBC_VERSION=8.0.29
# Wed, 22 Jun 2022 04:10:45 GMT
ENV MYSQL_JDBC_SHA256=d4e32d2a6026b5acc00300b73a86c28fb92681ae9629b21048ee67014c911db6
# Wed, 22 Jun 2022 04:10:46 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.29
# Wed, 22 Jun 2022 04:10:47 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.29.jar
# Wed, 22 Jun 2022 04:10:48 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.29.jar
# Wed, 22 Jun 2022 04:10:50 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Wed, 22 Jun 2022 04:10:51 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 22 Jun 2022 04:10:52 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 22 Jun 2022 04:10:53 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 22 Jun 2022 04:10:54 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 22 Jun 2022 04:10:54 GMT
VOLUME [/usr/local/xwiki]
# Wed, 22 Jun 2022 04:10:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jun 2022 04:10:56 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15da1b4c110f7cc460fbf968fb55b77c541f0e3ab87b92d5e6a822cc2c593e1`  
		Last Modified: Tue, 07 Jun 2022 05:10:23 GMT  
		Size: 15.9 MB (15898299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8e9d6a15d13e6f2d5d43f40b76051350cb7090cfcae5300dc1647e3196577a`  
		Last Modified: Tue, 07 Jun 2022 06:44:15 GMT  
		Size: 41.6 MB (41608356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51219ca7d003431d2f9c6ddda7db0a1902cf2b7e4e879625811b086f268b39c`  
		Last Modified: Tue, 07 Jun 2022 06:44:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5aa4900f44b9e3e20168d54fda3a0b78e62d572de1796db20345b70b1d8b3ca`  
		Last Modified: Tue, 07 Jun 2022 11:23:12 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6796806c88914990f15047665e74a4ea1fb933bdf7b8ebf39b1f2a82b723e044`  
		Last Modified: Fri, 10 Jun 2022 02:03:21 GMT  
		Size: 12.3 MB (12264791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca37469fc5a6ebbc5f1a764aabd4ba48b92a85d1396b644e1139994fad2fa34e`  
		Last Modified: Fri, 10 Jun 2022 02:03:20 GMT  
		Size: 208.8 KB (208841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c24501792b443d8ecb222b1c49c98ee84d4d76016bdbf8ba61b488fa873f7f`  
		Last Modified: Wed, 22 Jun 2022 04:17:01 GMT  
		Size: 163.4 MB (163365370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d1bb494106d6d36bcf7dd967f0d881aa979803343f00918d55f105d5759bbe`  
		Last Modified: Wed, 22 Jun 2022 04:16:59 GMT  
		Size: 292.0 MB (291982622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a24595bb483532afb5982a7102104c4107076a079eeaa4d5fd0d776abe5a1543`  
		Last Modified: Wed, 22 Jun 2022 04:16:38 GMT  
		Size: 2.4 MB (2381177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff7c257d2e413a9084ca6e6cbd963fb66e757d99cd06e3bd96971b96b7ca0083`  
		Last Modified: Wed, 22 Jun 2022 04:16:37 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:343c1e7e3713943da3994aafca00d9f54df0f67fb6b20d86933ebe4a05623d0e`  
		Last Modified: Wed, 22 Jun 2022 04:16:37 GMT  
		Size: 2.3 KB (2309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e0fa83eef81ca126718a8c16fd8f17e6ead2f37ccfc6a8dbf8e2568d221ac0`  
		Last Modified: Wed, 22 Jun 2022 04:16:37 GMT  
		Size: 5.9 KB (5854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c0f8a5973921c322d0333259d28d3c3ab9fa848afe20830fa1aad3fa46743fc`  
		Last Modified: Wed, 22 Jun 2022 04:16:37 GMT  
		Size: 2.5 KB (2509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:stable-mysql-tomcat`

```console
$ docker pull xwiki@sha256:8b941b575bfdc8c0eb31d9b7f3422c6fe866062a7b465d725d53ec4107ca6144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:stable-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:f08dab318ed8416b7ef8fc05f68b5c11c7f486d1b4686584b35fbf916cb81081
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.4 MB (562431476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68a5a2c9d16899b288b020a4b618dae8b4a2aa67718272532c3f92b8caca60fd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:14:23 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 00:14:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:58 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:59 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 06:30:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:30:41 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 06:30:41 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:30:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:35:57 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 06:35:58 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 00:18:07 GMT
COPY dir:360b17da945f7a5c4dcdc8b0602904442d98c06d17157280c607532ec8b6edaa in /usr/local/tomcat 
# Fri, 10 Jun 2022 00:18:12 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 00:18:13 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 00:18:13 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 00:18:13 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:25:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 22 Jun 2022 04:25:05 GMT
ENV XWIKI_VERSION=14.4.1
# Wed, 22 Jun 2022 04:25:05 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.4.1
# Wed, 22 Jun 2022 04:25:05 GMT
ENV XWIKI_DOWNLOAD_SHA256=8e20eba50acee0f157d3cc160306d65e0995b453833c8923f833030f0a469fb4
# Wed, 22 Jun 2022 04:25:42 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 22 Jun 2022 04:25:43 GMT
ENV MYSQL_JDBC_VERSION=8.0.29
# Wed, 22 Jun 2022 04:25:43 GMT
ENV MYSQL_JDBC_SHA256=d4e32d2a6026b5acc00300b73a86c28fb92681ae9629b21048ee67014c911db6
# Wed, 22 Jun 2022 04:25:43 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.29
# Wed, 22 Jun 2022 04:25:43 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.29.jar
# Wed, 22 Jun 2022 04:25:44 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.29.jar
# Wed, 22 Jun 2022 04:25:44 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Wed, 22 Jun 2022 04:25:44 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 22 Jun 2022 04:25:44 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 22 Jun 2022 04:25:45 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 22 Jun 2022 04:25:45 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 22 Jun 2022 04:25:45 GMT
VOLUME [/usr/local/xwiki]
# Wed, 22 Jun 2022 04:25:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jun 2022 04:25:45 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b669251e19038a24bd6cab0baab92077f23163880fac4701fb3efa564350732b`  
		Last Modified: Tue, 07 Jun 2022 00:21:34 GMT  
		Size: 43.3 MB (43267270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf45eff8a02bcdf7a96904e0dc534c78c89a5c860e224fa57780ef2fc2eab99e`  
		Last Modified: Tue, 07 Jun 2022 00:21:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246089a07769500a0adb027d1dc0efbb1254ee07d75dcdc6f8a3ceb8bae3e95f`  
		Last Modified: Tue, 07 Jun 2022 06:48:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3636fe8b4383f769da39b4c598b1e98b53b6d528e34e9d20fac5c17cfefcd866`  
		Last Modified: Fri, 10 Jun 2022 00:40:50 GMT  
		Size: 12.2 MB (12247499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0a0fd2a02961d2a1725c94d0c0f5670c51d5f5f9bad820a96e45791a5d7a32`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 445.5 KB (445476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beba28f927b0599e17785c8f69b8373e61c14da42247f7683f924f80ecae1439`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c54774971cb7c57e8fe14a42f90f7e4cceb67150ff2f3112f9ad46fea390190d`  
		Last Modified: Wed, 22 Jun 2022 04:30:07 GMT  
		Size: 167.5 MB (167492656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:368fa3670d498d9bc0883cd81cf9b9a45d3ccf79365eabe27b779344efefda58`  
		Last Modified: Wed, 22 Jun 2022 04:30:00 GMT  
		Size: 292.0 MB (291982499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb96a08b07f52ad5c126f31fe742e1c114a3239ab5c6fc5641266fa5be00579`  
		Last Modified: Wed, 22 Jun 2022 04:29:42 GMT  
		Size: 2.4 MB (2381172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94af0360a2e049892f0b11539619a1e889f32dcdec1df1a671ffb6032f55437`  
		Last Modified: Wed, 22 Jun 2022 04:29:41 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7255f65a4fc48ef292f0f13fc58a9f76e18f7f3969190698a08ff5907c9e5dd`  
		Last Modified: Wed, 22 Jun 2022 04:29:41 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1695b6d1dbcfb2018bc0a46ec5c66b47f1105c4aff382726932ee462014d294e`  
		Last Modified: Wed, 22 Jun 2022 04:29:41 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec62f61e9a4c7f7d90e61399a76eb18b02a789afbac8e9fcaaa1f8ebc6b10da`  
		Last Modified: Wed, 22 Jun 2022 04:29:41 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:stable-mysql-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:b4d50e1906ede668b41d744d6050b179dc5523658ba13b4e4cc5a92b98955a71
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.9 MB (554912952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed7a93d82de140d630b2eab42fb4270590bb2efcab4d72dd5a2f2dd8ce842278`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:00:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:35:32 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 06:36:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:36:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:36:20 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 10:50:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 10:50:03 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 10:50:04 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 10:50:05 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 10:50:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:50:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:59:13 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 10:59:14 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 01:28:16 GMT
COPY dir:1fb0204bb532a7d63a0dd2d2677d66a70be0285454d27afba6780853636ba1ef in /usr/local/tomcat 
# Fri, 10 Jun 2022 01:28:22 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 01:28:24 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 01:28:25 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 01:28:26 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:24 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:25 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:09:26 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:09:27 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:10:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 22 Jun 2022 04:10:05 GMT
ENV XWIKI_VERSION=14.4.1
# Wed, 22 Jun 2022 04:10:06 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.4.1
# Wed, 22 Jun 2022 04:10:07 GMT
ENV XWIKI_DOWNLOAD_SHA256=8e20eba50acee0f157d3cc160306d65e0995b453833c8923f833030f0a469fb4
# Wed, 22 Jun 2022 04:10:44 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 22 Jun 2022 04:10:45 GMT
ENV MYSQL_JDBC_VERSION=8.0.29
# Wed, 22 Jun 2022 04:10:45 GMT
ENV MYSQL_JDBC_SHA256=d4e32d2a6026b5acc00300b73a86c28fb92681ae9629b21048ee67014c911db6
# Wed, 22 Jun 2022 04:10:46 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.29
# Wed, 22 Jun 2022 04:10:47 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.29.jar
# Wed, 22 Jun 2022 04:10:48 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.29.jar
# Wed, 22 Jun 2022 04:10:50 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Wed, 22 Jun 2022 04:10:51 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 22 Jun 2022 04:10:52 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 22 Jun 2022 04:10:53 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 22 Jun 2022 04:10:54 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 22 Jun 2022 04:10:54 GMT
VOLUME [/usr/local/xwiki]
# Wed, 22 Jun 2022 04:10:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jun 2022 04:10:56 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15da1b4c110f7cc460fbf968fb55b77c541f0e3ab87b92d5e6a822cc2c593e1`  
		Last Modified: Tue, 07 Jun 2022 05:10:23 GMT  
		Size: 15.9 MB (15898299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8e9d6a15d13e6f2d5d43f40b76051350cb7090cfcae5300dc1647e3196577a`  
		Last Modified: Tue, 07 Jun 2022 06:44:15 GMT  
		Size: 41.6 MB (41608356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51219ca7d003431d2f9c6ddda7db0a1902cf2b7e4e879625811b086f268b39c`  
		Last Modified: Tue, 07 Jun 2022 06:44:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5aa4900f44b9e3e20168d54fda3a0b78e62d572de1796db20345b70b1d8b3ca`  
		Last Modified: Tue, 07 Jun 2022 11:23:12 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6796806c88914990f15047665e74a4ea1fb933bdf7b8ebf39b1f2a82b723e044`  
		Last Modified: Fri, 10 Jun 2022 02:03:21 GMT  
		Size: 12.3 MB (12264791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca37469fc5a6ebbc5f1a764aabd4ba48b92a85d1396b644e1139994fad2fa34e`  
		Last Modified: Fri, 10 Jun 2022 02:03:20 GMT  
		Size: 208.8 KB (208841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c24501792b443d8ecb222b1c49c98ee84d4d76016bdbf8ba61b488fa873f7f`  
		Last Modified: Wed, 22 Jun 2022 04:17:01 GMT  
		Size: 163.4 MB (163365370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d1bb494106d6d36bcf7dd967f0d881aa979803343f00918d55f105d5759bbe`  
		Last Modified: Wed, 22 Jun 2022 04:16:59 GMT  
		Size: 292.0 MB (291982622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a24595bb483532afb5982a7102104c4107076a079eeaa4d5fd0d776abe5a1543`  
		Last Modified: Wed, 22 Jun 2022 04:16:38 GMT  
		Size: 2.4 MB (2381177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff7c257d2e413a9084ca6e6cbd963fb66e757d99cd06e3bd96971b96b7ca0083`  
		Last Modified: Wed, 22 Jun 2022 04:16:37 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:343c1e7e3713943da3994aafca00d9f54df0f67fb6b20d86933ebe4a05623d0e`  
		Last Modified: Wed, 22 Jun 2022 04:16:37 GMT  
		Size: 2.3 KB (2309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e0fa83eef81ca126718a8c16fd8f17e6ead2f37ccfc6a8dbf8e2568d221ac0`  
		Last Modified: Wed, 22 Jun 2022 04:16:37 GMT  
		Size: 5.9 KB (5854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c0f8a5973921c322d0333259d28d3c3ab9fa848afe20830fa1aad3fa46743fc`  
		Last Modified: Wed, 22 Jun 2022 04:16:37 GMT  
		Size: 2.5 KB (2509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:stable-postgres`

```console
$ docker pull xwiki@sha256:1fabdb2e4da65c0abe19ecbaf0ff7ee43cfa94d27091c3d5748e8211ff99735d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:stable-postgres` - linux; amd64

```console
$ docker pull xwiki@sha256:be2ec4361ef195cce3e9b320a91b407e3928431c94a7adb57af1f11044876bd6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **561.6 MB (561646591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d6170aaa002127cf799999888c4d5d58bc136c94008910619af04189b3825fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:14:23 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 00:14:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:58 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:59 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 06:30:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:30:41 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 06:30:41 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:30:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:35:57 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 06:35:58 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 00:18:07 GMT
COPY dir:360b17da945f7a5c4dcdc8b0602904442d98c06d17157280c607532ec8b6edaa in /usr/local/tomcat 
# Fri, 10 Jun 2022 00:18:12 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 00:18:13 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 00:18:13 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 00:18:13 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:26:27 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Wed, 22 Jun 2022 04:26:29 GMT
ENV XWIKI_VERSION=14.4.1
# Wed, 22 Jun 2022 04:26:29 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.4.1
# Wed, 22 Jun 2022 04:26:29 GMT
ENV XWIKI_DOWNLOAD_SHA256=8e20eba50acee0f157d3cc160306d65e0995b453833c8923f833030f0a469fb4
# Wed, 22 Jun 2022 04:27:07 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 22 Jun 2022 04:27:08 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Wed, 22 Jun 2022 04:27:08 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 22 Jun 2022 04:27:08 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 22 Jun 2022 04:27:09 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 22 Jun 2022 04:27:09 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 22 Jun 2022 04:27:09 GMT
VOLUME [/usr/local/xwiki]
# Wed, 22 Jun 2022 04:27:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jun 2022 04:27:09 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b669251e19038a24bd6cab0baab92077f23163880fac4701fb3efa564350732b`  
		Last Modified: Tue, 07 Jun 2022 00:21:34 GMT  
		Size: 43.3 MB (43267270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf45eff8a02bcdf7a96904e0dc534c78c89a5c860e224fa57780ef2fc2eab99e`  
		Last Modified: Tue, 07 Jun 2022 00:21:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246089a07769500a0adb027d1dc0efbb1254ee07d75dcdc6f8a3ceb8bae3e95f`  
		Last Modified: Tue, 07 Jun 2022 06:48:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3636fe8b4383f769da39b4c598b1e98b53b6d528e34e9d20fac5c17cfefcd866`  
		Last Modified: Fri, 10 Jun 2022 00:40:50 GMT  
		Size: 12.2 MB (12247499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0a0fd2a02961d2a1725c94d0c0f5670c51d5f5f9bad820a96e45791a5d7a32`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 445.5 KB (445476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beba28f927b0599e17785c8f69b8373e61c14da42247f7683f924f80ecae1439`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:657eec0a2bb289006e136ad46dbd1d85e8ff10712e1477c0fcacb617a19bb242`  
		Last Modified: Wed, 22 Jun 2022 04:31:12 GMT  
		Size: 168.3 MB (168293438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7336ce43765447d78aa2db6c3c2d06f343d8c461acf64bd26ad2da6cdb3802e9`  
		Last Modified: Wed, 22 Jun 2022 04:31:05 GMT  
		Size: 292.0 MB (291982439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed867fb2baa0895487cb447dc1687bb44e7fa6941a1ed692bc25262eb6c8ce84`  
		Last Modified: Wed, 22 Jun 2022 04:30:47 GMT  
		Size: 795.4 KB (795422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffb2ca6524e098e2552dc1ee3c9df3692d579ef2fe4d945c2aefab62c820dfef`  
		Last Modified: Wed, 22 Jun 2022 04:30:46 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7f44840360a683faa6f816201fff0fcc275d3c3c886e55bd98a5b77b283d9f2`  
		Last Modified: Wed, 22 Jun 2022 04:30:46 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea0454030911a4eba98666b0184b8c3241a86aaffd563ef77f78cf31f9103402`  
		Last Modified: Wed, 22 Jun 2022 04:30:46 GMT  
		Size: 5.9 KB (5854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e070314e7d3d33ac915c9e5d8719b2d00e3207754d5b335482a0e76137e50a`  
		Last Modified: Wed, 22 Jun 2022 04:30:46 GMT  
		Size: 2.5 KB (2503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:stable-postgres` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:b3ce0cb6e854ea382295ea6bb0f34559cb20af7194ac7aa73e10036616745688
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.1 MB (554126019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:964c73cc655f5ead167b952f043637ed76a9a1e4fa99f78c8bc52620b48566db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:00:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:35:32 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 06:36:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:36:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:36:20 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 10:50:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 10:50:03 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 10:50:04 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 10:50:05 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 10:50:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:50:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:59:13 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 10:59:14 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 01:28:16 GMT
COPY dir:1fb0204bb532a7d63a0dd2d2677d66a70be0285454d27afba6780853636ba1ef in /usr/local/tomcat 
# Fri, 10 Jun 2022 01:28:22 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 01:28:24 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 01:28:25 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 01:28:26 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:24 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:25 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:09:26 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:09:27 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:11:42 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Wed, 22 Jun 2022 04:11:43 GMT
ENV XWIKI_VERSION=14.4.1
# Wed, 22 Jun 2022 04:11:43 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.4.1
# Wed, 22 Jun 2022 04:11:44 GMT
ENV XWIKI_DOWNLOAD_SHA256=8e20eba50acee0f157d3cc160306d65e0995b453833c8923f833030f0a469fb4
# Wed, 22 Jun 2022 04:12:23 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 22 Jun 2022 04:12:24 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Wed, 22 Jun 2022 04:12:25 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 22 Jun 2022 04:12:26 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 22 Jun 2022 04:12:27 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 22 Jun 2022 04:12:28 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 22 Jun 2022 04:12:28 GMT
VOLUME [/usr/local/xwiki]
# Wed, 22 Jun 2022 04:12:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jun 2022 04:12:30 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15da1b4c110f7cc460fbf968fb55b77c541f0e3ab87b92d5e6a822cc2c593e1`  
		Last Modified: Tue, 07 Jun 2022 05:10:23 GMT  
		Size: 15.9 MB (15898299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8e9d6a15d13e6f2d5d43f40b76051350cb7090cfcae5300dc1647e3196577a`  
		Last Modified: Tue, 07 Jun 2022 06:44:15 GMT  
		Size: 41.6 MB (41608356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51219ca7d003431d2f9c6ddda7db0a1902cf2b7e4e879625811b086f268b39c`  
		Last Modified: Tue, 07 Jun 2022 06:44:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5aa4900f44b9e3e20168d54fda3a0b78e62d572de1796db20345b70b1d8b3ca`  
		Last Modified: Tue, 07 Jun 2022 11:23:12 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6796806c88914990f15047665e74a4ea1fb933bdf7b8ebf39b1f2a82b723e044`  
		Last Modified: Fri, 10 Jun 2022 02:03:21 GMT  
		Size: 12.3 MB (12264791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca37469fc5a6ebbc5f1a764aabd4ba48b92a85d1396b644e1139994fad2fa34e`  
		Last Modified: Fri, 10 Jun 2022 02:03:20 GMT  
		Size: 208.8 KB (208841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbf4753a12af2d02fd26a953119f6843f7e381cfec0d679d92b04b4e4f5a3d6a`  
		Last Modified: Wed, 22 Jun 2022 04:18:08 GMT  
		Size: 164.2 MB (164164156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8735ad3b7140d98c3eedfd5e132b33810f9ccbd2ef89e37d738de84113c7dc92`  
		Last Modified: Wed, 22 Jun 2022 04:18:07 GMT  
		Size: 292.0 MB (291982533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e05d15dcdbfe55730845a86712aea5417820a8fc73ea492391f4bc8773f273c`  
		Last Modified: Wed, 22 Jun 2022 04:17:46 GMT  
		Size: 795.4 KB (795416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ed4588b795d5cf65bf69167563114888c0924eec209d7f1a1f2f78f04f2e42`  
		Last Modified: Wed, 22 Jun 2022 04:17:45 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f537181948e5040a35cd0252682f25858131a6b14dd2a0cc0f8e9d4deb3dff1`  
		Last Modified: Wed, 22 Jun 2022 04:17:45 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f44b9ff69abe9f98824c9cccb73f52b56acccad5bf10bbf6df522ad974eb8fec`  
		Last Modified: Wed, 22 Jun 2022 04:17:45 GMT  
		Size: 5.9 KB (5851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f781c1d839ed0cddf10a24f41ffa5dc32da0de94c89077f83fd5f3cfa0c62ed6`  
		Last Modified: Wed, 22 Jun 2022 04:17:45 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:stable-postgres-tomcat`

```console
$ docker pull xwiki@sha256:1fabdb2e4da65c0abe19ecbaf0ff7ee43cfa94d27091c3d5748e8211ff99735d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:stable-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:be2ec4361ef195cce3e9b320a91b407e3928431c94a7adb57af1f11044876bd6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **561.6 MB (561646591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d6170aaa002127cf799999888c4d5d58bc136c94008910619af04189b3825fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:14:23 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 00:14:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:58 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:59 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 06:30:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:30:41 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 06:30:41 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:30:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:35:57 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 06:35:58 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 00:18:07 GMT
COPY dir:360b17da945f7a5c4dcdc8b0602904442d98c06d17157280c607532ec8b6edaa in /usr/local/tomcat 
# Fri, 10 Jun 2022 00:18:12 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 00:18:13 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 00:18:13 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 00:18:13 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:26:27 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Wed, 22 Jun 2022 04:26:29 GMT
ENV XWIKI_VERSION=14.4.1
# Wed, 22 Jun 2022 04:26:29 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.4.1
# Wed, 22 Jun 2022 04:26:29 GMT
ENV XWIKI_DOWNLOAD_SHA256=8e20eba50acee0f157d3cc160306d65e0995b453833c8923f833030f0a469fb4
# Wed, 22 Jun 2022 04:27:07 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 22 Jun 2022 04:27:08 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Wed, 22 Jun 2022 04:27:08 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 22 Jun 2022 04:27:08 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 22 Jun 2022 04:27:09 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 22 Jun 2022 04:27:09 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 22 Jun 2022 04:27:09 GMT
VOLUME [/usr/local/xwiki]
# Wed, 22 Jun 2022 04:27:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jun 2022 04:27:09 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b669251e19038a24bd6cab0baab92077f23163880fac4701fb3efa564350732b`  
		Last Modified: Tue, 07 Jun 2022 00:21:34 GMT  
		Size: 43.3 MB (43267270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf45eff8a02bcdf7a96904e0dc534c78c89a5c860e224fa57780ef2fc2eab99e`  
		Last Modified: Tue, 07 Jun 2022 00:21:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246089a07769500a0adb027d1dc0efbb1254ee07d75dcdc6f8a3ceb8bae3e95f`  
		Last Modified: Tue, 07 Jun 2022 06:48:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3636fe8b4383f769da39b4c598b1e98b53b6d528e34e9d20fac5c17cfefcd866`  
		Last Modified: Fri, 10 Jun 2022 00:40:50 GMT  
		Size: 12.2 MB (12247499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0a0fd2a02961d2a1725c94d0c0f5670c51d5f5f9bad820a96e45791a5d7a32`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 445.5 KB (445476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beba28f927b0599e17785c8f69b8373e61c14da42247f7683f924f80ecae1439`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:657eec0a2bb289006e136ad46dbd1d85e8ff10712e1477c0fcacb617a19bb242`  
		Last Modified: Wed, 22 Jun 2022 04:31:12 GMT  
		Size: 168.3 MB (168293438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7336ce43765447d78aa2db6c3c2d06f343d8c461acf64bd26ad2da6cdb3802e9`  
		Last Modified: Wed, 22 Jun 2022 04:31:05 GMT  
		Size: 292.0 MB (291982439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed867fb2baa0895487cb447dc1687bb44e7fa6941a1ed692bc25262eb6c8ce84`  
		Last Modified: Wed, 22 Jun 2022 04:30:47 GMT  
		Size: 795.4 KB (795422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffb2ca6524e098e2552dc1ee3c9df3692d579ef2fe4d945c2aefab62c820dfef`  
		Last Modified: Wed, 22 Jun 2022 04:30:46 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7f44840360a683faa6f816201fff0fcc275d3c3c886e55bd98a5b77b283d9f2`  
		Last Modified: Wed, 22 Jun 2022 04:30:46 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea0454030911a4eba98666b0184b8c3241a86aaffd563ef77f78cf31f9103402`  
		Last Modified: Wed, 22 Jun 2022 04:30:46 GMT  
		Size: 5.9 KB (5854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e070314e7d3d33ac915c9e5d8719b2d00e3207754d5b335482a0e76137e50a`  
		Last Modified: Wed, 22 Jun 2022 04:30:46 GMT  
		Size: 2.5 KB (2503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:stable-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:b3ce0cb6e854ea382295ea6bb0f34559cb20af7194ac7aa73e10036616745688
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.1 MB (554126019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:964c73cc655f5ead167b952f043637ed76a9a1e4fa99f78c8bc52620b48566db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:00:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:35:32 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 06:36:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:36:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:36:20 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 10:50:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 10:50:03 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 10:50:04 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 10:50:05 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 10:50:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:50:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:59:13 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 10:59:14 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 01:28:16 GMT
COPY dir:1fb0204bb532a7d63a0dd2d2677d66a70be0285454d27afba6780853636ba1ef in /usr/local/tomcat 
# Fri, 10 Jun 2022 01:28:22 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 01:28:24 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 01:28:25 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 01:28:26 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:24 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:25 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:09:26 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:09:27 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:11:42 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Wed, 22 Jun 2022 04:11:43 GMT
ENV XWIKI_VERSION=14.4.1
# Wed, 22 Jun 2022 04:11:43 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.4.1
# Wed, 22 Jun 2022 04:11:44 GMT
ENV XWIKI_DOWNLOAD_SHA256=8e20eba50acee0f157d3cc160306d65e0995b453833c8923f833030f0a469fb4
# Wed, 22 Jun 2022 04:12:23 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 22 Jun 2022 04:12:24 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Wed, 22 Jun 2022 04:12:25 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 22 Jun 2022 04:12:26 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 22 Jun 2022 04:12:27 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 22 Jun 2022 04:12:28 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 22 Jun 2022 04:12:28 GMT
VOLUME [/usr/local/xwiki]
# Wed, 22 Jun 2022 04:12:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jun 2022 04:12:30 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15da1b4c110f7cc460fbf968fb55b77c541f0e3ab87b92d5e6a822cc2c593e1`  
		Last Modified: Tue, 07 Jun 2022 05:10:23 GMT  
		Size: 15.9 MB (15898299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8e9d6a15d13e6f2d5d43f40b76051350cb7090cfcae5300dc1647e3196577a`  
		Last Modified: Tue, 07 Jun 2022 06:44:15 GMT  
		Size: 41.6 MB (41608356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51219ca7d003431d2f9c6ddda7db0a1902cf2b7e4e879625811b086f268b39c`  
		Last Modified: Tue, 07 Jun 2022 06:44:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5aa4900f44b9e3e20168d54fda3a0b78e62d572de1796db20345b70b1d8b3ca`  
		Last Modified: Tue, 07 Jun 2022 11:23:12 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6796806c88914990f15047665e74a4ea1fb933bdf7b8ebf39b1f2a82b723e044`  
		Last Modified: Fri, 10 Jun 2022 02:03:21 GMT  
		Size: 12.3 MB (12264791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca37469fc5a6ebbc5f1a764aabd4ba48b92a85d1396b644e1139994fad2fa34e`  
		Last Modified: Fri, 10 Jun 2022 02:03:20 GMT  
		Size: 208.8 KB (208841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbf4753a12af2d02fd26a953119f6843f7e381cfec0d679d92b04b4e4f5a3d6a`  
		Last Modified: Wed, 22 Jun 2022 04:18:08 GMT  
		Size: 164.2 MB (164164156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8735ad3b7140d98c3eedfd5e132b33810f9ccbd2ef89e37d738de84113c7dc92`  
		Last Modified: Wed, 22 Jun 2022 04:18:07 GMT  
		Size: 292.0 MB (291982533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e05d15dcdbfe55730845a86712aea5417820a8fc73ea492391f4bc8773f273c`  
		Last Modified: Wed, 22 Jun 2022 04:17:46 GMT  
		Size: 795.4 KB (795416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ed4588b795d5cf65bf69167563114888c0924eec209d7f1a1f2f78f04f2e42`  
		Last Modified: Wed, 22 Jun 2022 04:17:45 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f537181948e5040a35cd0252682f25858131a6b14dd2a0cc0f8e9d4deb3dff1`  
		Last Modified: Wed, 22 Jun 2022 04:17:45 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f44b9ff69abe9f98824c9cccb73f52b56acccad5bf10bbf6df522ad974eb8fec`  
		Last Modified: Wed, 22 Jun 2022 04:17:45 GMT  
		Size: 5.9 KB (5851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f781c1d839ed0cddf10a24f41ffa5dc32da0de94c89077f83fd5f3cfa0c62ed6`  
		Last Modified: Wed, 22 Jun 2022 04:17:45 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
