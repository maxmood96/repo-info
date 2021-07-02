<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `xwiki`

-	[`xwiki:12`](#xwiki12)
-	[`xwiki:12-mysql-tomcat`](#xwiki12-mysql-tomcat)
-	[`xwiki:12-postgres-tomcat`](#xwiki12-postgres-tomcat)
-	[`xwiki:12.10`](#xwiki1210)
-	[`xwiki:12.10-mysql-tomcat`](#xwiki1210-mysql-tomcat)
-	[`xwiki:12.10-postgres-tomcat`](#xwiki1210-postgres-tomcat)
-	[`xwiki:12.10.8`](#xwiki12108)
-	[`xwiki:12.10.8-mysql-tomcat`](#xwiki12108-mysql-tomcat)
-	[`xwiki:12.10.8-postgres-tomcat`](#xwiki12108-postgres-tomcat)
-	[`xwiki:13`](#xwiki13)
-	[`xwiki:13-mysql-tomcat`](#xwiki13-mysql-tomcat)
-	[`xwiki:13-postgres-tomcat`](#xwiki13-postgres-tomcat)
-	[`xwiki:13.4`](#xwiki134)
-	[`xwiki:13.4-mysql-tomcat`](#xwiki134-mysql-tomcat)
-	[`xwiki:13.4-postgres-tomcat`](#xwiki134-postgres-tomcat)
-	[`xwiki:13.4.1`](#xwiki1341)
-	[`xwiki:13.4.1-mysql-tomcat`](#xwiki1341-mysql-tomcat)
-	[`xwiki:13.4.1-postgres-tomcat`](#xwiki1341-postgres-tomcat)
-	[`xwiki:13.5`](#xwiki135)
-	[`xwiki:13.5-mysql-tomcat`](#xwiki135-mysql-tomcat)
-	[`xwiki:13.5-postgres-tomcat`](#xwiki135-postgres-tomcat)
-	[`xwiki:13.5.0`](#xwiki1350)
-	[`xwiki:13.5.0-mysql-tomcat`](#xwiki1350-mysql-tomcat)
-	[`xwiki:13.5.0-postgres-tomcat`](#xwiki1350-postgres-tomcat)
-	[`xwiki:latest`](#xwikilatest)
-	[`xwiki:lts`](#xwikilts)
-	[`xwiki:lts-mysql`](#xwikilts-mysql)
-	[`xwiki:lts-mysql-tomcat`](#xwikilts-mysql-tomcat)
-	[`xwiki:lts-postgres`](#xwikilts-postgres)
-	[`xwiki:lts-postgres-tomcat`](#xwikilts-postgres-tomcat)
-	[`xwiki:mysql-tomcat`](#xwikimysql-tomcat)
-	[`xwiki:postgres-tomcat`](#xwikipostgres-tomcat)
-	[`xwiki:stable`](#xwikistable)
-	[`xwiki:stable-mysql`](#xwikistable-mysql)
-	[`xwiki:stable-mysql-tomcat`](#xwikistable-mysql-tomcat)
-	[`xwiki:stable-postgres`](#xwikistable-postgres)
-	[`xwiki:stable-postgres-tomcat`](#xwikistable-postgres-tomcat)

## `xwiki:12`

```console
$ docker pull xwiki@sha256:1e197bef02015dace9ca4075b7a489059028049229bb8149ddca1b4406ef6262
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `xwiki:12` - linux; amd64

```console
$ docker pull xwiki@sha256:7936f677de247db3696317f0abf61992a7b1fda926c034feff859dc1bedf33a0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **718.3 MB (718287590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be287ce42e05979127e95d83cdfa051698ff58dcc7eee07d251c2c10c73f25de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:28:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 18 Jun 2021 00:29:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:29:44 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Fri, 18 Jun 2021 00:29:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 18 Jun 2021 00:29:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Jun 2021 00:29:55 GMT
CMD ["jshell"]
# Tue, 22 Jun 2021 22:44:10 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 22 Jun 2021 22:44:11 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 22 Jun 2021 22:44:12 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 22 Jun 2021 22:44:12 GMT
WORKDIR /usr/local/tomcat
# Tue, 22 Jun 2021 22:44:12 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 22:44:12 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 23:10:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 22 Jun 2021 23:10:49 GMT
ENV TOMCAT_MAJOR=8
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_VERSION=8.5.68
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_SHA512=673f8d295d6f6b8e53b30c9c81989a3586341f9660f00e61a131153f54f0ce9d41bf8f49960ef477d3ec81610e1c75c1684c8676e9ebe5015486334c443d82e5
# Fri, 02 Jul 2021 20:10:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 02 Jul 2021 20:10:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 02 Jul 2021 20:10:28 GMT
EXPOSE 8080
# Fri, 02 Jul 2021 20:10:29 GMT
CMD ["catalina.sh" "run"]
# Fri, 02 Jul 2021 21:20:19 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Fri, 02 Jul 2021 21:22:31 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 02 Jul 2021 21:24:55 GMT
ENV XWIKI_VERSION=12.10.8
# Fri, 02 Jul 2021 21:24:55 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.8
# Fri, 02 Jul 2021 21:24:56 GMT
ENV XWIKI_DOWNLOAD_SHA256=739471e78f8b2550849d1a869c27313c4c71b12bb9b6c9c26f77c81a993dff2e
# Fri, 02 Jul 2021 21:25:34 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 02 Jul 2021 21:25:35 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Fri, 02 Jul 2021 21:25:36 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Fri, 02 Jul 2021 21:25:36 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Fri, 02 Jul 2021 21:25:36 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Fri, 02 Jul 2021 21:25:36 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Fri, 02 Jul 2021 21:25:38 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 02 Jul 2021 21:25:38 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 02 Jul 2021 21:25:38 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 02 Jul 2021 21:25:39 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 02 Jul 2021 21:25:39 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 02 Jul 2021 21:25:40 GMT
VOLUME [/usr/local/xwiki]
# Fri, 02 Jul 2021 21:25:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Jul 2021 21:25:40 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7766c75e8fade5c21578ec8566d2929e7238f9ac1dbe88551bf2f147b76c65`  
		Last Modified: Fri, 18 Jun 2021 00:39:29 GMT  
		Size: 16.0 MB (16033037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3025761fffcd095f302e914141cd91fdce2a0d7b76c4f13f96753ef8b9cc4151`  
		Last Modified: Fri, 18 Jun 2021 00:40:26 GMT  
		Size: 193.7 MB (193651024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fa731efc631621d3f50f90fbbcb2b097a684e8d8cb0315be61e939425e2c89`  
		Last Modified: Tue, 22 Jun 2021 23:19:37 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838b070fdc3792c062bb5b6c96d57e95aa826e3f672720a26fe4ce42e09f62a6`  
		Last Modified: Fri, 02 Jul 2021 20:35:19 GMT  
		Size: 12.4 MB (12449570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b092812f8972255279e884ddd841c549e700a49cbf30502b609090da11a8366`  
		Last Modified: Fri, 02 Jul 2021 20:35:17 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e0c6fa70e8651d71566b155d1603cdada3e0ef5e24989a737ff1331e504248`  
		Last Modified: Fri, 02 Jul 2021 21:29:22 GMT  
		Size: 167.7 MB (167687703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33d752b3691d8364086e45b10dcc929096fe97831218327789b39c0af5be2e81`  
		Last Modified: Fri, 02 Jul 2021 21:31:14 GMT  
		Size: 297.6 MB (297643037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d959af1053745fc9b0c7ae7926ade05e2947dbb626102064ad082c1ac72a00`  
		Last Modified: Fri, 02 Jul 2021 21:30:55 GMT  
		Size: 2.3 MB (2257825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff5014a54fd4da4d0be9e135f6a07d40d5de45808375fe6a5b2a8a92ea8e8115`  
		Last Modified: Fri, 02 Jul 2021 21:30:55 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3370fff0d5efea5884d25b00529d409ae92a9b41417f26fdb3fd64cf7b91fcdf`  
		Last Modified: Fri, 02 Jul 2021 21:30:55 GMT  
		Size: 2.3 KB (2317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85a15beb11b7db1ec710c7b1d91da098c06771ab705ca520461418b9391d9cb`  
		Last Modified: Fri, 02 Jul 2021 21:30:55 GMT  
		Size: 5.2 KB (5233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:152cfc2ed6695c687023da931551401c2a615598639526788449524fce177722`  
		Last Modified: Fri, 02 Jul 2021 21:30:55 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:12-mysql-tomcat`

```console
$ docker pull xwiki@sha256:1e197bef02015dace9ca4075b7a489059028049229bb8149ddca1b4406ef6262
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `xwiki:12-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:7936f677de247db3696317f0abf61992a7b1fda926c034feff859dc1bedf33a0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **718.3 MB (718287590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be287ce42e05979127e95d83cdfa051698ff58dcc7eee07d251c2c10c73f25de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:28:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 18 Jun 2021 00:29:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:29:44 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Fri, 18 Jun 2021 00:29:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 18 Jun 2021 00:29:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Jun 2021 00:29:55 GMT
CMD ["jshell"]
# Tue, 22 Jun 2021 22:44:10 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 22 Jun 2021 22:44:11 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 22 Jun 2021 22:44:12 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 22 Jun 2021 22:44:12 GMT
WORKDIR /usr/local/tomcat
# Tue, 22 Jun 2021 22:44:12 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 22:44:12 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 23:10:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 22 Jun 2021 23:10:49 GMT
ENV TOMCAT_MAJOR=8
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_VERSION=8.5.68
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_SHA512=673f8d295d6f6b8e53b30c9c81989a3586341f9660f00e61a131153f54f0ce9d41bf8f49960ef477d3ec81610e1c75c1684c8676e9ebe5015486334c443d82e5
# Fri, 02 Jul 2021 20:10:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 02 Jul 2021 20:10:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 02 Jul 2021 20:10:28 GMT
EXPOSE 8080
# Fri, 02 Jul 2021 20:10:29 GMT
CMD ["catalina.sh" "run"]
# Fri, 02 Jul 2021 21:20:19 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Fri, 02 Jul 2021 21:22:31 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 02 Jul 2021 21:24:55 GMT
ENV XWIKI_VERSION=12.10.8
# Fri, 02 Jul 2021 21:24:55 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.8
# Fri, 02 Jul 2021 21:24:56 GMT
ENV XWIKI_DOWNLOAD_SHA256=739471e78f8b2550849d1a869c27313c4c71b12bb9b6c9c26f77c81a993dff2e
# Fri, 02 Jul 2021 21:25:34 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 02 Jul 2021 21:25:35 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Fri, 02 Jul 2021 21:25:36 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Fri, 02 Jul 2021 21:25:36 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Fri, 02 Jul 2021 21:25:36 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Fri, 02 Jul 2021 21:25:36 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Fri, 02 Jul 2021 21:25:38 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 02 Jul 2021 21:25:38 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 02 Jul 2021 21:25:38 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 02 Jul 2021 21:25:39 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 02 Jul 2021 21:25:39 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 02 Jul 2021 21:25:40 GMT
VOLUME [/usr/local/xwiki]
# Fri, 02 Jul 2021 21:25:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Jul 2021 21:25:40 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7766c75e8fade5c21578ec8566d2929e7238f9ac1dbe88551bf2f147b76c65`  
		Last Modified: Fri, 18 Jun 2021 00:39:29 GMT  
		Size: 16.0 MB (16033037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3025761fffcd095f302e914141cd91fdce2a0d7b76c4f13f96753ef8b9cc4151`  
		Last Modified: Fri, 18 Jun 2021 00:40:26 GMT  
		Size: 193.7 MB (193651024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fa731efc631621d3f50f90fbbcb2b097a684e8d8cb0315be61e939425e2c89`  
		Last Modified: Tue, 22 Jun 2021 23:19:37 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838b070fdc3792c062bb5b6c96d57e95aa826e3f672720a26fe4ce42e09f62a6`  
		Last Modified: Fri, 02 Jul 2021 20:35:19 GMT  
		Size: 12.4 MB (12449570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b092812f8972255279e884ddd841c549e700a49cbf30502b609090da11a8366`  
		Last Modified: Fri, 02 Jul 2021 20:35:17 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e0c6fa70e8651d71566b155d1603cdada3e0ef5e24989a737ff1331e504248`  
		Last Modified: Fri, 02 Jul 2021 21:29:22 GMT  
		Size: 167.7 MB (167687703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33d752b3691d8364086e45b10dcc929096fe97831218327789b39c0af5be2e81`  
		Last Modified: Fri, 02 Jul 2021 21:31:14 GMT  
		Size: 297.6 MB (297643037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d959af1053745fc9b0c7ae7926ade05e2947dbb626102064ad082c1ac72a00`  
		Last Modified: Fri, 02 Jul 2021 21:30:55 GMT  
		Size: 2.3 MB (2257825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff5014a54fd4da4d0be9e135f6a07d40d5de45808375fe6a5b2a8a92ea8e8115`  
		Last Modified: Fri, 02 Jul 2021 21:30:55 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3370fff0d5efea5884d25b00529d409ae92a9b41417f26fdb3fd64cf7b91fcdf`  
		Last Modified: Fri, 02 Jul 2021 21:30:55 GMT  
		Size: 2.3 KB (2317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85a15beb11b7db1ec710c7b1d91da098c06771ab705ca520461418b9391d9cb`  
		Last Modified: Fri, 02 Jul 2021 21:30:55 GMT  
		Size: 5.2 KB (5233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:152cfc2ed6695c687023da931551401c2a615598639526788449524fce177722`  
		Last Modified: Fri, 02 Jul 2021 21:30:55 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:12-postgres-tomcat`

```console
$ docker pull xwiki@sha256:d4ad52384a2f234abfaa1a4fcf325fcec293c3d503304b17b635c2c39dda9bb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:12-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:dcddc6098a29ac5c80cf67b5dc8c672016c3d7dcb5aa5cb67cc1a9c8650202ba
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **717.6 MB (717625228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ad1634308c9f2ace73759c7eee6fdf3d6598f9918206d93a361aa793c8c1879`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:28:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 18 Jun 2021 00:29:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:29:44 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Fri, 18 Jun 2021 00:29:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 18 Jun 2021 00:29:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Jun 2021 00:29:55 GMT
CMD ["jshell"]
# Tue, 22 Jun 2021 22:44:10 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 22 Jun 2021 22:44:11 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 22 Jun 2021 22:44:12 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 22 Jun 2021 22:44:12 GMT
WORKDIR /usr/local/tomcat
# Tue, 22 Jun 2021 22:44:12 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 22:44:12 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 23:10:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 22 Jun 2021 23:10:49 GMT
ENV TOMCAT_MAJOR=8
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_VERSION=8.5.68
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_SHA512=673f8d295d6f6b8e53b30c9c81989a3586341f9660f00e61a131153f54f0ce9d41bf8f49960ef477d3ec81610e1c75c1684c8676e9ebe5015486334c443d82e5
# Fri, 02 Jul 2021 20:10:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 02 Jul 2021 20:10:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 02 Jul 2021 20:10:28 GMT
EXPOSE 8080
# Fri, 02 Jul 2021 20:10:29 GMT
CMD ["catalina.sh" "run"]
# Fri, 02 Jul 2021 21:20:19 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Fri, 02 Jul 2021 21:24:00 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 02 Jul 2021 21:25:46 GMT
ENV XWIKI_VERSION=12.10.8
# Fri, 02 Jul 2021 21:25:46 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.8
# Fri, 02 Jul 2021 21:25:46 GMT
ENV XWIKI_DOWNLOAD_SHA256=739471e78f8b2550849d1a869c27313c4c71b12bb9b6c9c26f77c81a993dff2e
# Fri, 02 Jul 2021 21:26:24 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 02 Jul 2021 21:26:26 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 02 Jul 2021 21:26:26 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 02 Jul 2021 21:26:26 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 02 Jul 2021 21:26:27 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 02 Jul 2021 21:26:28 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 02 Jul 2021 21:26:28 GMT
VOLUME [/usr/local/xwiki]
# Fri, 02 Jul 2021 21:26:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Jul 2021 21:26:28 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7766c75e8fade5c21578ec8566d2929e7238f9ac1dbe88551bf2f147b76c65`  
		Last Modified: Fri, 18 Jun 2021 00:39:29 GMT  
		Size: 16.0 MB (16033037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3025761fffcd095f302e914141cd91fdce2a0d7b76c4f13f96753ef8b9cc4151`  
		Last Modified: Fri, 18 Jun 2021 00:40:26 GMT  
		Size: 193.7 MB (193651024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fa731efc631621d3f50f90fbbcb2b097a684e8d8cb0315be61e939425e2c89`  
		Last Modified: Tue, 22 Jun 2021 23:19:37 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838b070fdc3792c062bb5b6c96d57e95aa826e3f672720a26fe4ce42e09f62a6`  
		Last Modified: Fri, 02 Jul 2021 20:35:19 GMT  
		Size: 12.4 MB (12449570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b092812f8972255279e884ddd841c549e700a49cbf30502b609090da11a8366`  
		Last Modified: Fri, 02 Jul 2021 20:35:17 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632cb72d9488b73892dc69501fcea55c5c81f21d67fb024c3d81a13dd8e181f2`  
		Last Modified: Fri, 02 Jul 2021 21:30:30 GMT  
		Size: 168.5 MB (168487456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa26e65e7bdcfa431b794bb86fb835d0ba92125cc1f674909deb60817b0ffc7`  
		Last Modified: Fri, 02 Jul 2021 21:32:08 GMT  
		Size: 297.6 MB (297643176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:778bdda6cf557625368df98f86b4555d4484fa3578482c0f622ba8d20ce3334f`  
		Last Modified: Fri, 02 Jul 2021 21:31:48 GMT  
		Size: 795.4 KB (795418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f1b4a5284c1fb17dc78353b7d19eca4c02c7f51faf45f50b6fe6a3e44f17f88`  
		Last Modified: Fri, 02 Jul 2021 21:31:47 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f7600885f2faa71d2a0ce2f1b6baeabed4422fba71f131890e69726d9cfce9`  
		Last Modified: Fri, 02 Jul 2021 21:31:47 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e682ee044d627db17e38f2f2ff093a8cea613bd97d7109a738de6426281da84a`  
		Last Modified: Fri, 02 Jul 2021 21:31:47 GMT  
		Size: 5.2 KB (5235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ea14025ccd7f5ae72333faa029b366380ce839017cdb4025860c68672b8b96`  
		Last Modified: Fri, 02 Jul 2021 21:31:47 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:12-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:0ddf979c392d089c97254e695ee7ee8858c7226de04fa721a5058bd40bd0ea7f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **709.0 MB (708983644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea2131062ee3bd998cc1ad9d0c7efa828713dee230fab020f49d5e46a40cfe0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 17 Jun 2021 23:53:58 GMT
ADD file:9e94a579f0495fce8fac6889d0b9b2cd576d5b3ce9f18ff913ad99a503756769 in / 
# Thu, 17 Jun 2021 23:53:59 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:31:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 18 Jun 2021 00:31:32 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:31:58 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Fri, 18 Jun 2021 00:32:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 18 Jun 2021 00:32:10 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Jun 2021 00:32:10 GMT
CMD ["jshell"]
# Tue, 22 Jun 2021 23:25:06 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 22 Jun 2021 23:25:06 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 22 Jun 2021 23:25:07 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 22 Jun 2021 23:25:07 GMT
WORKDIR /usr/local/tomcat
# Tue, 22 Jun 2021 23:25:07 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 23:25:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 23:30:28 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 22 Jun 2021 23:30:29 GMT
ENV TOMCAT_MAJOR=8
# Tue, 22 Jun 2021 23:30:29 GMT
ENV TOMCAT_VERSION=8.5.68
# Tue, 22 Jun 2021 23:30:29 GMT
ENV TOMCAT_SHA512=673f8d295d6f6b8e53b30c9c81989a3586341f9660f00e61a131153f54f0ce9d41bf8f49960ef477d3ec81610e1c75c1684c8676e9ebe5015486334c443d82e5
# Fri, 02 Jul 2021 20:14:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 02 Jul 2021 20:14:25 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 02 Jul 2021 20:14:26 GMT
EXPOSE 8080
# Fri, 02 Jul 2021 20:14:26 GMT
CMD ["catalina.sh" "run"]
# Fri, 02 Jul 2021 22:10:38 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Fri, 02 Jul 2021 22:11:13 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 02 Jul 2021 22:12:05 GMT
ENV XWIKI_VERSION=12.10.8
# Fri, 02 Jul 2021 22:12:05 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.8
# Fri, 02 Jul 2021 22:12:05 GMT
ENV XWIKI_DOWNLOAD_SHA256=739471e78f8b2550849d1a869c27313c4c71b12bb9b6c9c26f77c81a993dff2e
# Fri, 02 Jul 2021 22:12:42 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 02 Jul 2021 22:12:44 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 02 Jul 2021 22:12:44 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 02 Jul 2021 22:12:44 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 02 Jul 2021 22:12:45 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 02 Jul 2021 22:12:45 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 02 Jul 2021 22:12:46 GMT
VOLUME [/usr/local/xwiki]
# Fri, 02 Jul 2021 22:12:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Jul 2021 22:12:46 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:6f86eded34a1950318569803a7e0c689175ebd9d76faf08798f88ac133b98a11`  
		Last Modified: Thu, 17 Jun 2021 23:56:04 GMT  
		Size: 27.2 MB (27158803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff470c6007f78550376884f4972cc5c767c6adc6f7d6002adddbddfb4600ea4b`  
		Last Modified: Fri, 18 Jun 2021 00:35:11 GMT  
		Size: 15.9 MB (15894169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a125d809875539cb0e1d2b0483b6223a65a2867db6c0df786d36feb6fa9bf260`  
		Last Modified: Fri, 18 Jun 2021 00:36:10 GMT  
		Size: 190.4 MB (190379258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599d9b9dba394414fe824f147f376772ae86db1750dd0c0865717476c25cd040`  
		Last Modified: Tue, 22 Jun 2021 23:41:56 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdf80a91fe0ee7a8d615c877013dd3f0f57f510581a488bb24e1d945dd212f30`  
		Last Modified: Fri, 02 Jul 2021 20:43:37 GMT  
		Size: 12.4 MB (12448780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f63370a9da1ce6088a59891070b42f6fe7d136d05c91aeb21d50398be035dbe`  
		Last Modified: Fri, 02 Jul 2021 20:43:34 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daed3696500a526a0b524e45ca20d612b3afdfbdf4e3b965b2384c9359de9952`  
		Last Modified: Fri, 02 Jul 2021 22:14:47 GMT  
		Size: 164.7 MB (164652294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2bdca7c7fda93fd53c72d634b26796ed47fea3732fa34e654e80f24a29e45d`  
		Last Modified: Fri, 02 Jul 2021 22:15:40 GMT  
		Size: 297.6 MB (297643088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1973f14560a22aba4dcd67d7d766ce12b6412478de10ca1ede26d89eef4ce002`  
		Last Modified: Fri, 02 Jul 2021 22:15:17 GMT  
		Size: 795.4 KB (795416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28dc40d8ca6a5141c9bb915f8bc1e4f7f6c72d41b8f9a67c68e1d7aef8ed4ef3`  
		Last Modified: Fri, 02 Jul 2021 22:15:17 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d684d9972a40fa0638d09f2706b84bd0fb4f24abd756f55d946d7fb7aac6509d`  
		Last Modified: Fri, 02 Jul 2021 22:15:17 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3cfc79bfb8d63baad54ecca1877c3f744947d18ec52ee2d7fc6ff840340841d`  
		Last Modified: Fri, 02 Jul 2021 22:15:17 GMT  
		Size: 5.2 KB (5230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7936b27fcebcf1c11910fcd1c354d7fe295b8a31ab83f21dd105e77e7edb3f0a`  
		Last Modified: Fri, 02 Jul 2021 22:15:17 GMT  
		Size: 2.5 KB (2501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:12.10`

```console
$ docker pull xwiki@sha256:1e197bef02015dace9ca4075b7a489059028049229bb8149ddca1b4406ef6262
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `xwiki:12.10` - linux; amd64

```console
$ docker pull xwiki@sha256:7936f677de247db3696317f0abf61992a7b1fda926c034feff859dc1bedf33a0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **718.3 MB (718287590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be287ce42e05979127e95d83cdfa051698ff58dcc7eee07d251c2c10c73f25de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:28:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 18 Jun 2021 00:29:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:29:44 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Fri, 18 Jun 2021 00:29:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 18 Jun 2021 00:29:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Jun 2021 00:29:55 GMT
CMD ["jshell"]
# Tue, 22 Jun 2021 22:44:10 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 22 Jun 2021 22:44:11 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 22 Jun 2021 22:44:12 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 22 Jun 2021 22:44:12 GMT
WORKDIR /usr/local/tomcat
# Tue, 22 Jun 2021 22:44:12 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 22:44:12 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 23:10:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 22 Jun 2021 23:10:49 GMT
ENV TOMCAT_MAJOR=8
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_VERSION=8.5.68
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_SHA512=673f8d295d6f6b8e53b30c9c81989a3586341f9660f00e61a131153f54f0ce9d41bf8f49960ef477d3ec81610e1c75c1684c8676e9ebe5015486334c443d82e5
# Fri, 02 Jul 2021 20:10:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 02 Jul 2021 20:10:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 02 Jul 2021 20:10:28 GMT
EXPOSE 8080
# Fri, 02 Jul 2021 20:10:29 GMT
CMD ["catalina.sh" "run"]
# Fri, 02 Jul 2021 21:20:19 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Fri, 02 Jul 2021 21:22:31 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 02 Jul 2021 21:24:55 GMT
ENV XWIKI_VERSION=12.10.8
# Fri, 02 Jul 2021 21:24:55 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.8
# Fri, 02 Jul 2021 21:24:56 GMT
ENV XWIKI_DOWNLOAD_SHA256=739471e78f8b2550849d1a869c27313c4c71b12bb9b6c9c26f77c81a993dff2e
# Fri, 02 Jul 2021 21:25:34 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 02 Jul 2021 21:25:35 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Fri, 02 Jul 2021 21:25:36 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Fri, 02 Jul 2021 21:25:36 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Fri, 02 Jul 2021 21:25:36 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Fri, 02 Jul 2021 21:25:36 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Fri, 02 Jul 2021 21:25:38 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 02 Jul 2021 21:25:38 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 02 Jul 2021 21:25:38 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 02 Jul 2021 21:25:39 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 02 Jul 2021 21:25:39 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 02 Jul 2021 21:25:40 GMT
VOLUME [/usr/local/xwiki]
# Fri, 02 Jul 2021 21:25:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Jul 2021 21:25:40 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7766c75e8fade5c21578ec8566d2929e7238f9ac1dbe88551bf2f147b76c65`  
		Last Modified: Fri, 18 Jun 2021 00:39:29 GMT  
		Size: 16.0 MB (16033037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3025761fffcd095f302e914141cd91fdce2a0d7b76c4f13f96753ef8b9cc4151`  
		Last Modified: Fri, 18 Jun 2021 00:40:26 GMT  
		Size: 193.7 MB (193651024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fa731efc631621d3f50f90fbbcb2b097a684e8d8cb0315be61e939425e2c89`  
		Last Modified: Tue, 22 Jun 2021 23:19:37 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838b070fdc3792c062bb5b6c96d57e95aa826e3f672720a26fe4ce42e09f62a6`  
		Last Modified: Fri, 02 Jul 2021 20:35:19 GMT  
		Size: 12.4 MB (12449570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b092812f8972255279e884ddd841c549e700a49cbf30502b609090da11a8366`  
		Last Modified: Fri, 02 Jul 2021 20:35:17 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e0c6fa70e8651d71566b155d1603cdada3e0ef5e24989a737ff1331e504248`  
		Last Modified: Fri, 02 Jul 2021 21:29:22 GMT  
		Size: 167.7 MB (167687703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33d752b3691d8364086e45b10dcc929096fe97831218327789b39c0af5be2e81`  
		Last Modified: Fri, 02 Jul 2021 21:31:14 GMT  
		Size: 297.6 MB (297643037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d959af1053745fc9b0c7ae7926ade05e2947dbb626102064ad082c1ac72a00`  
		Last Modified: Fri, 02 Jul 2021 21:30:55 GMT  
		Size: 2.3 MB (2257825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff5014a54fd4da4d0be9e135f6a07d40d5de45808375fe6a5b2a8a92ea8e8115`  
		Last Modified: Fri, 02 Jul 2021 21:30:55 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3370fff0d5efea5884d25b00529d409ae92a9b41417f26fdb3fd64cf7b91fcdf`  
		Last Modified: Fri, 02 Jul 2021 21:30:55 GMT  
		Size: 2.3 KB (2317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85a15beb11b7db1ec710c7b1d91da098c06771ab705ca520461418b9391d9cb`  
		Last Modified: Fri, 02 Jul 2021 21:30:55 GMT  
		Size: 5.2 KB (5233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:152cfc2ed6695c687023da931551401c2a615598639526788449524fce177722`  
		Last Modified: Fri, 02 Jul 2021 21:30:55 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:12.10-mysql-tomcat`

```console
$ docker pull xwiki@sha256:1e197bef02015dace9ca4075b7a489059028049229bb8149ddca1b4406ef6262
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `xwiki:12.10-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:7936f677de247db3696317f0abf61992a7b1fda926c034feff859dc1bedf33a0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **718.3 MB (718287590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be287ce42e05979127e95d83cdfa051698ff58dcc7eee07d251c2c10c73f25de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:28:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 18 Jun 2021 00:29:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:29:44 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Fri, 18 Jun 2021 00:29:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 18 Jun 2021 00:29:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Jun 2021 00:29:55 GMT
CMD ["jshell"]
# Tue, 22 Jun 2021 22:44:10 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 22 Jun 2021 22:44:11 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 22 Jun 2021 22:44:12 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 22 Jun 2021 22:44:12 GMT
WORKDIR /usr/local/tomcat
# Tue, 22 Jun 2021 22:44:12 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 22:44:12 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 23:10:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 22 Jun 2021 23:10:49 GMT
ENV TOMCAT_MAJOR=8
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_VERSION=8.5.68
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_SHA512=673f8d295d6f6b8e53b30c9c81989a3586341f9660f00e61a131153f54f0ce9d41bf8f49960ef477d3ec81610e1c75c1684c8676e9ebe5015486334c443d82e5
# Fri, 02 Jul 2021 20:10:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 02 Jul 2021 20:10:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 02 Jul 2021 20:10:28 GMT
EXPOSE 8080
# Fri, 02 Jul 2021 20:10:29 GMT
CMD ["catalina.sh" "run"]
# Fri, 02 Jul 2021 21:20:19 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Fri, 02 Jul 2021 21:22:31 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 02 Jul 2021 21:24:55 GMT
ENV XWIKI_VERSION=12.10.8
# Fri, 02 Jul 2021 21:24:55 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.8
# Fri, 02 Jul 2021 21:24:56 GMT
ENV XWIKI_DOWNLOAD_SHA256=739471e78f8b2550849d1a869c27313c4c71b12bb9b6c9c26f77c81a993dff2e
# Fri, 02 Jul 2021 21:25:34 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 02 Jul 2021 21:25:35 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Fri, 02 Jul 2021 21:25:36 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Fri, 02 Jul 2021 21:25:36 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Fri, 02 Jul 2021 21:25:36 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Fri, 02 Jul 2021 21:25:36 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Fri, 02 Jul 2021 21:25:38 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 02 Jul 2021 21:25:38 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 02 Jul 2021 21:25:38 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 02 Jul 2021 21:25:39 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 02 Jul 2021 21:25:39 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 02 Jul 2021 21:25:40 GMT
VOLUME [/usr/local/xwiki]
# Fri, 02 Jul 2021 21:25:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Jul 2021 21:25:40 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7766c75e8fade5c21578ec8566d2929e7238f9ac1dbe88551bf2f147b76c65`  
		Last Modified: Fri, 18 Jun 2021 00:39:29 GMT  
		Size: 16.0 MB (16033037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3025761fffcd095f302e914141cd91fdce2a0d7b76c4f13f96753ef8b9cc4151`  
		Last Modified: Fri, 18 Jun 2021 00:40:26 GMT  
		Size: 193.7 MB (193651024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fa731efc631621d3f50f90fbbcb2b097a684e8d8cb0315be61e939425e2c89`  
		Last Modified: Tue, 22 Jun 2021 23:19:37 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838b070fdc3792c062bb5b6c96d57e95aa826e3f672720a26fe4ce42e09f62a6`  
		Last Modified: Fri, 02 Jul 2021 20:35:19 GMT  
		Size: 12.4 MB (12449570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b092812f8972255279e884ddd841c549e700a49cbf30502b609090da11a8366`  
		Last Modified: Fri, 02 Jul 2021 20:35:17 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e0c6fa70e8651d71566b155d1603cdada3e0ef5e24989a737ff1331e504248`  
		Last Modified: Fri, 02 Jul 2021 21:29:22 GMT  
		Size: 167.7 MB (167687703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33d752b3691d8364086e45b10dcc929096fe97831218327789b39c0af5be2e81`  
		Last Modified: Fri, 02 Jul 2021 21:31:14 GMT  
		Size: 297.6 MB (297643037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d959af1053745fc9b0c7ae7926ade05e2947dbb626102064ad082c1ac72a00`  
		Last Modified: Fri, 02 Jul 2021 21:30:55 GMT  
		Size: 2.3 MB (2257825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff5014a54fd4da4d0be9e135f6a07d40d5de45808375fe6a5b2a8a92ea8e8115`  
		Last Modified: Fri, 02 Jul 2021 21:30:55 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3370fff0d5efea5884d25b00529d409ae92a9b41417f26fdb3fd64cf7b91fcdf`  
		Last Modified: Fri, 02 Jul 2021 21:30:55 GMT  
		Size: 2.3 KB (2317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85a15beb11b7db1ec710c7b1d91da098c06771ab705ca520461418b9391d9cb`  
		Last Modified: Fri, 02 Jul 2021 21:30:55 GMT  
		Size: 5.2 KB (5233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:152cfc2ed6695c687023da931551401c2a615598639526788449524fce177722`  
		Last Modified: Fri, 02 Jul 2021 21:30:55 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:12.10-postgres-tomcat`

```console
$ docker pull xwiki@sha256:d4ad52384a2f234abfaa1a4fcf325fcec293c3d503304b17b635c2c39dda9bb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:12.10-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:dcddc6098a29ac5c80cf67b5dc8c672016c3d7dcb5aa5cb67cc1a9c8650202ba
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **717.6 MB (717625228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ad1634308c9f2ace73759c7eee6fdf3d6598f9918206d93a361aa793c8c1879`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:28:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 18 Jun 2021 00:29:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:29:44 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Fri, 18 Jun 2021 00:29:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 18 Jun 2021 00:29:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Jun 2021 00:29:55 GMT
CMD ["jshell"]
# Tue, 22 Jun 2021 22:44:10 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 22 Jun 2021 22:44:11 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 22 Jun 2021 22:44:12 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 22 Jun 2021 22:44:12 GMT
WORKDIR /usr/local/tomcat
# Tue, 22 Jun 2021 22:44:12 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 22:44:12 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 23:10:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 22 Jun 2021 23:10:49 GMT
ENV TOMCAT_MAJOR=8
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_VERSION=8.5.68
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_SHA512=673f8d295d6f6b8e53b30c9c81989a3586341f9660f00e61a131153f54f0ce9d41bf8f49960ef477d3ec81610e1c75c1684c8676e9ebe5015486334c443d82e5
# Fri, 02 Jul 2021 20:10:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 02 Jul 2021 20:10:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 02 Jul 2021 20:10:28 GMT
EXPOSE 8080
# Fri, 02 Jul 2021 20:10:29 GMT
CMD ["catalina.sh" "run"]
# Fri, 02 Jul 2021 21:20:19 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Fri, 02 Jul 2021 21:24:00 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 02 Jul 2021 21:25:46 GMT
ENV XWIKI_VERSION=12.10.8
# Fri, 02 Jul 2021 21:25:46 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.8
# Fri, 02 Jul 2021 21:25:46 GMT
ENV XWIKI_DOWNLOAD_SHA256=739471e78f8b2550849d1a869c27313c4c71b12bb9b6c9c26f77c81a993dff2e
# Fri, 02 Jul 2021 21:26:24 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 02 Jul 2021 21:26:26 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 02 Jul 2021 21:26:26 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 02 Jul 2021 21:26:26 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 02 Jul 2021 21:26:27 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 02 Jul 2021 21:26:28 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 02 Jul 2021 21:26:28 GMT
VOLUME [/usr/local/xwiki]
# Fri, 02 Jul 2021 21:26:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Jul 2021 21:26:28 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7766c75e8fade5c21578ec8566d2929e7238f9ac1dbe88551bf2f147b76c65`  
		Last Modified: Fri, 18 Jun 2021 00:39:29 GMT  
		Size: 16.0 MB (16033037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3025761fffcd095f302e914141cd91fdce2a0d7b76c4f13f96753ef8b9cc4151`  
		Last Modified: Fri, 18 Jun 2021 00:40:26 GMT  
		Size: 193.7 MB (193651024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fa731efc631621d3f50f90fbbcb2b097a684e8d8cb0315be61e939425e2c89`  
		Last Modified: Tue, 22 Jun 2021 23:19:37 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838b070fdc3792c062bb5b6c96d57e95aa826e3f672720a26fe4ce42e09f62a6`  
		Last Modified: Fri, 02 Jul 2021 20:35:19 GMT  
		Size: 12.4 MB (12449570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b092812f8972255279e884ddd841c549e700a49cbf30502b609090da11a8366`  
		Last Modified: Fri, 02 Jul 2021 20:35:17 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632cb72d9488b73892dc69501fcea55c5c81f21d67fb024c3d81a13dd8e181f2`  
		Last Modified: Fri, 02 Jul 2021 21:30:30 GMT  
		Size: 168.5 MB (168487456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa26e65e7bdcfa431b794bb86fb835d0ba92125cc1f674909deb60817b0ffc7`  
		Last Modified: Fri, 02 Jul 2021 21:32:08 GMT  
		Size: 297.6 MB (297643176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:778bdda6cf557625368df98f86b4555d4484fa3578482c0f622ba8d20ce3334f`  
		Last Modified: Fri, 02 Jul 2021 21:31:48 GMT  
		Size: 795.4 KB (795418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f1b4a5284c1fb17dc78353b7d19eca4c02c7f51faf45f50b6fe6a3e44f17f88`  
		Last Modified: Fri, 02 Jul 2021 21:31:47 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f7600885f2faa71d2a0ce2f1b6baeabed4422fba71f131890e69726d9cfce9`  
		Last Modified: Fri, 02 Jul 2021 21:31:47 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e682ee044d627db17e38f2f2ff093a8cea613bd97d7109a738de6426281da84a`  
		Last Modified: Fri, 02 Jul 2021 21:31:47 GMT  
		Size: 5.2 KB (5235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ea14025ccd7f5ae72333faa029b366380ce839017cdb4025860c68672b8b96`  
		Last Modified: Fri, 02 Jul 2021 21:31:47 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:12.10-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:0ddf979c392d089c97254e695ee7ee8858c7226de04fa721a5058bd40bd0ea7f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **709.0 MB (708983644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea2131062ee3bd998cc1ad9d0c7efa828713dee230fab020f49d5e46a40cfe0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 17 Jun 2021 23:53:58 GMT
ADD file:9e94a579f0495fce8fac6889d0b9b2cd576d5b3ce9f18ff913ad99a503756769 in / 
# Thu, 17 Jun 2021 23:53:59 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:31:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 18 Jun 2021 00:31:32 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:31:58 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Fri, 18 Jun 2021 00:32:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 18 Jun 2021 00:32:10 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Jun 2021 00:32:10 GMT
CMD ["jshell"]
# Tue, 22 Jun 2021 23:25:06 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 22 Jun 2021 23:25:06 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 22 Jun 2021 23:25:07 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 22 Jun 2021 23:25:07 GMT
WORKDIR /usr/local/tomcat
# Tue, 22 Jun 2021 23:25:07 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 23:25:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 23:30:28 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 22 Jun 2021 23:30:29 GMT
ENV TOMCAT_MAJOR=8
# Tue, 22 Jun 2021 23:30:29 GMT
ENV TOMCAT_VERSION=8.5.68
# Tue, 22 Jun 2021 23:30:29 GMT
ENV TOMCAT_SHA512=673f8d295d6f6b8e53b30c9c81989a3586341f9660f00e61a131153f54f0ce9d41bf8f49960ef477d3ec81610e1c75c1684c8676e9ebe5015486334c443d82e5
# Fri, 02 Jul 2021 20:14:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 02 Jul 2021 20:14:25 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 02 Jul 2021 20:14:26 GMT
EXPOSE 8080
# Fri, 02 Jul 2021 20:14:26 GMT
CMD ["catalina.sh" "run"]
# Fri, 02 Jul 2021 22:10:38 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Fri, 02 Jul 2021 22:11:13 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 02 Jul 2021 22:12:05 GMT
ENV XWIKI_VERSION=12.10.8
# Fri, 02 Jul 2021 22:12:05 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.8
# Fri, 02 Jul 2021 22:12:05 GMT
ENV XWIKI_DOWNLOAD_SHA256=739471e78f8b2550849d1a869c27313c4c71b12bb9b6c9c26f77c81a993dff2e
# Fri, 02 Jul 2021 22:12:42 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 02 Jul 2021 22:12:44 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 02 Jul 2021 22:12:44 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 02 Jul 2021 22:12:44 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 02 Jul 2021 22:12:45 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 02 Jul 2021 22:12:45 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 02 Jul 2021 22:12:46 GMT
VOLUME [/usr/local/xwiki]
# Fri, 02 Jul 2021 22:12:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Jul 2021 22:12:46 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:6f86eded34a1950318569803a7e0c689175ebd9d76faf08798f88ac133b98a11`  
		Last Modified: Thu, 17 Jun 2021 23:56:04 GMT  
		Size: 27.2 MB (27158803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff470c6007f78550376884f4972cc5c767c6adc6f7d6002adddbddfb4600ea4b`  
		Last Modified: Fri, 18 Jun 2021 00:35:11 GMT  
		Size: 15.9 MB (15894169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a125d809875539cb0e1d2b0483b6223a65a2867db6c0df786d36feb6fa9bf260`  
		Last Modified: Fri, 18 Jun 2021 00:36:10 GMT  
		Size: 190.4 MB (190379258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599d9b9dba394414fe824f147f376772ae86db1750dd0c0865717476c25cd040`  
		Last Modified: Tue, 22 Jun 2021 23:41:56 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdf80a91fe0ee7a8d615c877013dd3f0f57f510581a488bb24e1d945dd212f30`  
		Last Modified: Fri, 02 Jul 2021 20:43:37 GMT  
		Size: 12.4 MB (12448780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f63370a9da1ce6088a59891070b42f6fe7d136d05c91aeb21d50398be035dbe`  
		Last Modified: Fri, 02 Jul 2021 20:43:34 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daed3696500a526a0b524e45ca20d612b3afdfbdf4e3b965b2384c9359de9952`  
		Last Modified: Fri, 02 Jul 2021 22:14:47 GMT  
		Size: 164.7 MB (164652294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2bdca7c7fda93fd53c72d634b26796ed47fea3732fa34e654e80f24a29e45d`  
		Last Modified: Fri, 02 Jul 2021 22:15:40 GMT  
		Size: 297.6 MB (297643088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1973f14560a22aba4dcd67d7d766ce12b6412478de10ca1ede26d89eef4ce002`  
		Last Modified: Fri, 02 Jul 2021 22:15:17 GMT  
		Size: 795.4 KB (795416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28dc40d8ca6a5141c9bb915f8bc1e4f7f6c72d41b8f9a67c68e1d7aef8ed4ef3`  
		Last Modified: Fri, 02 Jul 2021 22:15:17 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d684d9972a40fa0638d09f2706b84bd0fb4f24abd756f55d946d7fb7aac6509d`  
		Last Modified: Fri, 02 Jul 2021 22:15:17 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3cfc79bfb8d63baad54ecca1877c3f744947d18ec52ee2d7fc6ff840340841d`  
		Last Modified: Fri, 02 Jul 2021 22:15:17 GMT  
		Size: 5.2 KB (5230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7936b27fcebcf1c11910fcd1c354d7fe295b8a31ab83f21dd105e77e7edb3f0a`  
		Last Modified: Fri, 02 Jul 2021 22:15:17 GMT  
		Size: 2.5 KB (2501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:12.10.8`

```console
$ docker pull xwiki@sha256:1e197bef02015dace9ca4075b7a489059028049229bb8149ddca1b4406ef6262
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `xwiki:12.10.8` - linux; amd64

```console
$ docker pull xwiki@sha256:7936f677de247db3696317f0abf61992a7b1fda926c034feff859dc1bedf33a0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **718.3 MB (718287590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be287ce42e05979127e95d83cdfa051698ff58dcc7eee07d251c2c10c73f25de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:28:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 18 Jun 2021 00:29:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:29:44 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Fri, 18 Jun 2021 00:29:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 18 Jun 2021 00:29:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Jun 2021 00:29:55 GMT
CMD ["jshell"]
# Tue, 22 Jun 2021 22:44:10 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 22 Jun 2021 22:44:11 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 22 Jun 2021 22:44:12 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 22 Jun 2021 22:44:12 GMT
WORKDIR /usr/local/tomcat
# Tue, 22 Jun 2021 22:44:12 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 22:44:12 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 23:10:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 22 Jun 2021 23:10:49 GMT
ENV TOMCAT_MAJOR=8
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_VERSION=8.5.68
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_SHA512=673f8d295d6f6b8e53b30c9c81989a3586341f9660f00e61a131153f54f0ce9d41bf8f49960ef477d3ec81610e1c75c1684c8676e9ebe5015486334c443d82e5
# Fri, 02 Jul 2021 20:10:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 02 Jul 2021 20:10:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 02 Jul 2021 20:10:28 GMT
EXPOSE 8080
# Fri, 02 Jul 2021 20:10:29 GMT
CMD ["catalina.sh" "run"]
# Fri, 02 Jul 2021 21:20:19 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Fri, 02 Jul 2021 21:22:31 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 02 Jul 2021 21:24:55 GMT
ENV XWIKI_VERSION=12.10.8
# Fri, 02 Jul 2021 21:24:55 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.8
# Fri, 02 Jul 2021 21:24:56 GMT
ENV XWIKI_DOWNLOAD_SHA256=739471e78f8b2550849d1a869c27313c4c71b12bb9b6c9c26f77c81a993dff2e
# Fri, 02 Jul 2021 21:25:34 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 02 Jul 2021 21:25:35 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Fri, 02 Jul 2021 21:25:36 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Fri, 02 Jul 2021 21:25:36 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Fri, 02 Jul 2021 21:25:36 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Fri, 02 Jul 2021 21:25:36 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Fri, 02 Jul 2021 21:25:38 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 02 Jul 2021 21:25:38 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 02 Jul 2021 21:25:38 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 02 Jul 2021 21:25:39 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 02 Jul 2021 21:25:39 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 02 Jul 2021 21:25:40 GMT
VOLUME [/usr/local/xwiki]
# Fri, 02 Jul 2021 21:25:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Jul 2021 21:25:40 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7766c75e8fade5c21578ec8566d2929e7238f9ac1dbe88551bf2f147b76c65`  
		Last Modified: Fri, 18 Jun 2021 00:39:29 GMT  
		Size: 16.0 MB (16033037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3025761fffcd095f302e914141cd91fdce2a0d7b76c4f13f96753ef8b9cc4151`  
		Last Modified: Fri, 18 Jun 2021 00:40:26 GMT  
		Size: 193.7 MB (193651024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fa731efc631621d3f50f90fbbcb2b097a684e8d8cb0315be61e939425e2c89`  
		Last Modified: Tue, 22 Jun 2021 23:19:37 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838b070fdc3792c062bb5b6c96d57e95aa826e3f672720a26fe4ce42e09f62a6`  
		Last Modified: Fri, 02 Jul 2021 20:35:19 GMT  
		Size: 12.4 MB (12449570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b092812f8972255279e884ddd841c549e700a49cbf30502b609090da11a8366`  
		Last Modified: Fri, 02 Jul 2021 20:35:17 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e0c6fa70e8651d71566b155d1603cdada3e0ef5e24989a737ff1331e504248`  
		Last Modified: Fri, 02 Jul 2021 21:29:22 GMT  
		Size: 167.7 MB (167687703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33d752b3691d8364086e45b10dcc929096fe97831218327789b39c0af5be2e81`  
		Last Modified: Fri, 02 Jul 2021 21:31:14 GMT  
		Size: 297.6 MB (297643037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d959af1053745fc9b0c7ae7926ade05e2947dbb626102064ad082c1ac72a00`  
		Last Modified: Fri, 02 Jul 2021 21:30:55 GMT  
		Size: 2.3 MB (2257825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff5014a54fd4da4d0be9e135f6a07d40d5de45808375fe6a5b2a8a92ea8e8115`  
		Last Modified: Fri, 02 Jul 2021 21:30:55 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3370fff0d5efea5884d25b00529d409ae92a9b41417f26fdb3fd64cf7b91fcdf`  
		Last Modified: Fri, 02 Jul 2021 21:30:55 GMT  
		Size: 2.3 KB (2317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85a15beb11b7db1ec710c7b1d91da098c06771ab705ca520461418b9391d9cb`  
		Last Modified: Fri, 02 Jul 2021 21:30:55 GMT  
		Size: 5.2 KB (5233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:152cfc2ed6695c687023da931551401c2a615598639526788449524fce177722`  
		Last Modified: Fri, 02 Jul 2021 21:30:55 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:12.10.8-mysql-tomcat`

```console
$ docker pull xwiki@sha256:1e197bef02015dace9ca4075b7a489059028049229bb8149ddca1b4406ef6262
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `xwiki:12.10.8-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:7936f677de247db3696317f0abf61992a7b1fda926c034feff859dc1bedf33a0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **718.3 MB (718287590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be287ce42e05979127e95d83cdfa051698ff58dcc7eee07d251c2c10c73f25de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:28:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 18 Jun 2021 00:29:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:29:44 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Fri, 18 Jun 2021 00:29:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 18 Jun 2021 00:29:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Jun 2021 00:29:55 GMT
CMD ["jshell"]
# Tue, 22 Jun 2021 22:44:10 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 22 Jun 2021 22:44:11 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 22 Jun 2021 22:44:12 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 22 Jun 2021 22:44:12 GMT
WORKDIR /usr/local/tomcat
# Tue, 22 Jun 2021 22:44:12 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 22:44:12 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 23:10:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 22 Jun 2021 23:10:49 GMT
ENV TOMCAT_MAJOR=8
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_VERSION=8.5.68
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_SHA512=673f8d295d6f6b8e53b30c9c81989a3586341f9660f00e61a131153f54f0ce9d41bf8f49960ef477d3ec81610e1c75c1684c8676e9ebe5015486334c443d82e5
# Fri, 02 Jul 2021 20:10:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 02 Jul 2021 20:10:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 02 Jul 2021 20:10:28 GMT
EXPOSE 8080
# Fri, 02 Jul 2021 20:10:29 GMT
CMD ["catalina.sh" "run"]
# Fri, 02 Jul 2021 21:20:19 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Fri, 02 Jul 2021 21:22:31 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 02 Jul 2021 21:24:55 GMT
ENV XWIKI_VERSION=12.10.8
# Fri, 02 Jul 2021 21:24:55 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.8
# Fri, 02 Jul 2021 21:24:56 GMT
ENV XWIKI_DOWNLOAD_SHA256=739471e78f8b2550849d1a869c27313c4c71b12bb9b6c9c26f77c81a993dff2e
# Fri, 02 Jul 2021 21:25:34 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 02 Jul 2021 21:25:35 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Fri, 02 Jul 2021 21:25:36 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Fri, 02 Jul 2021 21:25:36 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Fri, 02 Jul 2021 21:25:36 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Fri, 02 Jul 2021 21:25:36 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Fri, 02 Jul 2021 21:25:38 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 02 Jul 2021 21:25:38 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 02 Jul 2021 21:25:38 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 02 Jul 2021 21:25:39 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 02 Jul 2021 21:25:39 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 02 Jul 2021 21:25:40 GMT
VOLUME [/usr/local/xwiki]
# Fri, 02 Jul 2021 21:25:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Jul 2021 21:25:40 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7766c75e8fade5c21578ec8566d2929e7238f9ac1dbe88551bf2f147b76c65`  
		Last Modified: Fri, 18 Jun 2021 00:39:29 GMT  
		Size: 16.0 MB (16033037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3025761fffcd095f302e914141cd91fdce2a0d7b76c4f13f96753ef8b9cc4151`  
		Last Modified: Fri, 18 Jun 2021 00:40:26 GMT  
		Size: 193.7 MB (193651024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fa731efc631621d3f50f90fbbcb2b097a684e8d8cb0315be61e939425e2c89`  
		Last Modified: Tue, 22 Jun 2021 23:19:37 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838b070fdc3792c062bb5b6c96d57e95aa826e3f672720a26fe4ce42e09f62a6`  
		Last Modified: Fri, 02 Jul 2021 20:35:19 GMT  
		Size: 12.4 MB (12449570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b092812f8972255279e884ddd841c549e700a49cbf30502b609090da11a8366`  
		Last Modified: Fri, 02 Jul 2021 20:35:17 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e0c6fa70e8651d71566b155d1603cdada3e0ef5e24989a737ff1331e504248`  
		Last Modified: Fri, 02 Jul 2021 21:29:22 GMT  
		Size: 167.7 MB (167687703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33d752b3691d8364086e45b10dcc929096fe97831218327789b39c0af5be2e81`  
		Last Modified: Fri, 02 Jul 2021 21:31:14 GMT  
		Size: 297.6 MB (297643037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d959af1053745fc9b0c7ae7926ade05e2947dbb626102064ad082c1ac72a00`  
		Last Modified: Fri, 02 Jul 2021 21:30:55 GMT  
		Size: 2.3 MB (2257825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff5014a54fd4da4d0be9e135f6a07d40d5de45808375fe6a5b2a8a92ea8e8115`  
		Last Modified: Fri, 02 Jul 2021 21:30:55 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3370fff0d5efea5884d25b00529d409ae92a9b41417f26fdb3fd64cf7b91fcdf`  
		Last Modified: Fri, 02 Jul 2021 21:30:55 GMT  
		Size: 2.3 KB (2317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85a15beb11b7db1ec710c7b1d91da098c06771ab705ca520461418b9391d9cb`  
		Last Modified: Fri, 02 Jul 2021 21:30:55 GMT  
		Size: 5.2 KB (5233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:152cfc2ed6695c687023da931551401c2a615598639526788449524fce177722`  
		Last Modified: Fri, 02 Jul 2021 21:30:55 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:12.10.8-postgres-tomcat`

```console
$ docker pull xwiki@sha256:d4ad52384a2f234abfaa1a4fcf325fcec293c3d503304b17b635c2c39dda9bb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:12.10.8-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:dcddc6098a29ac5c80cf67b5dc8c672016c3d7dcb5aa5cb67cc1a9c8650202ba
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **717.6 MB (717625228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ad1634308c9f2ace73759c7eee6fdf3d6598f9918206d93a361aa793c8c1879`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:28:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 18 Jun 2021 00:29:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:29:44 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Fri, 18 Jun 2021 00:29:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 18 Jun 2021 00:29:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Jun 2021 00:29:55 GMT
CMD ["jshell"]
# Tue, 22 Jun 2021 22:44:10 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 22 Jun 2021 22:44:11 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 22 Jun 2021 22:44:12 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 22 Jun 2021 22:44:12 GMT
WORKDIR /usr/local/tomcat
# Tue, 22 Jun 2021 22:44:12 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 22:44:12 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 23:10:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 22 Jun 2021 23:10:49 GMT
ENV TOMCAT_MAJOR=8
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_VERSION=8.5.68
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_SHA512=673f8d295d6f6b8e53b30c9c81989a3586341f9660f00e61a131153f54f0ce9d41bf8f49960ef477d3ec81610e1c75c1684c8676e9ebe5015486334c443d82e5
# Fri, 02 Jul 2021 20:10:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 02 Jul 2021 20:10:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 02 Jul 2021 20:10:28 GMT
EXPOSE 8080
# Fri, 02 Jul 2021 20:10:29 GMT
CMD ["catalina.sh" "run"]
# Fri, 02 Jul 2021 21:20:19 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Fri, 02 Jul 2021 21:24:00 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 02 Jul 2021 21:25:46 GMT
ENV XWIKI_VERSION=12.10.8
# Fri, 02 Jul 2021 21:25:46 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.8
# Fri, 02 Jul 2021 21:25:46 GMT
ENV XWIKI_DOWNLOAD_SHA256=739471e78f8b2550849d1a869c27313c4c71b12bb9b6c9c26f77c81a993dff2e
# Fri, 02 Jul 2021 21:26:24 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 02 Jul 2021 21:26:26 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 02 Jul 2021 21:26:26 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 02 Jul 2021 21:26:26 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 02 Jul 2021 21:26:27 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 02 Jul 2021 21:26:28 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 02 Jul 2021 21:26:28 GMT
VOLUME [/usr/local/xwiki]
# Fri, 02 Jul 2021 21:26:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Jul 2021 21:26:28 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7766c75e8fade5c21578ec8566d2929e7238f9ac1dbe88551bf2f147b76c65`  
		Last Modified: Fri, 18 Jun 2021 00:39:29 GMT  
		Size: 16.0 MB (16033037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3025761fffcd095f302e914141cd91fdce2a0d7b76c4f13f96753ef8b9cc4151`  
		Last Modified: Fri, 18 Jun 2021 00:40:26 GMT  
		Size: 193.7 MB (193651024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fa731efc631621d3f50f90fbbcb2b097a684e8d8cb0315be61e939425e2c89`  
		Last Modified: Tue, 22 Jun 2021 23:19:37 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838b070fdc3792c062bb5b6c96d57e95aa826e3f672720a26fe4ce42e09f62a6`  
		Last Modified: Fri, 02 Jul 2021 20:35:19 GMT  
		Size: 12.4 MB (12449570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b092812f8972255279e884ddd841c549e700a49cbf30502b609090da11a8366`  
		Last Modified: Fri, 02 Jul 2021 20:35:17 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632cb72d9488b73892dc69501fcea55c5c81f21d67fb024c3d81a13dd8e181f2`  
		Last Modified: Fri, 02 Jul 2021 21:30:30 GMT  
		Size: 168.5 MB (168487456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa26e65e7bdcfa431b794bb86fb835d0ba92125cc1f674909deb60817b0ffc7`  
		Last Modified: Fri, 02 Jul 2021 21:32:08 GMT  
		Size: 297.6 MB (297643176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:778bdda6cf557625368df98f86b4555d4484fa3578482c0f622ba8d20ce3334f`  
		Last Modified: Fri, 02 Jul 2021 21:31:48 GMT  
		Size: 795.4 KB (795418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f1b4a5284c1fb17dc78353b7d19eca4c02c7f51faf45f50b6fe6a3e44f17f88`  
		Last Modified: Fri, 02 Jul 2021 21:31:47 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f7600885f2faa71d2a0ce2f1b6baeabed4422fba71f131890e69726d9cfce9`  
		Last Modified: Fri, 02 Jul 2021 21:31:47 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e682ee044d627db17e38f2f2ff093a8cea613bd97d7109a738de6426281da84a`  
		Last Modified: Fri, 02 Jul 2021 21:31:47 GMT  
		Size: 5.2 KB (5235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ea14025ccd7f5ae72333faa029b366380ce839017cdb4025860c68672b8b96`  
		Last Modified: Fri, 02 Jul 2021 21:31:47 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:12.10.8-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:0ddf979c392d089c97254e695ee7ee8858c7226de04fa721a5058bd40bd0ea7f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **709.0 MB (708983644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea2131062ee3bd998cc1ad9d0c7efa828713dee230fab020f49d5e46a40cfe0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 17 Jun 2021 23:53:58 GMT
ADD file:9e94a579f0495fce8fac6889d0b9b2cd576d5b3ce9f18ff913ad99a503756769 in / 
# Thu, 17 Jun 2021 23:53:59 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:31:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 18 Jun 2021 00:31:32 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:31:58 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Fri, 18 Jun 2021 00:32:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 18 Jun 2021 00:32:10 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Jun 2021 00:32:10 GMT
CMD ["jshell"]
# Tue, 22 Jun 2021 23:25:06 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 22 Jun 2021 23:25:06 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 22 Jun 2021 23:25:07 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 22 Jun 2021 23:25:07 GMT
WORKDIR /usr/local/tomcat
# Tue, 22 Jun 2021 23:25:07 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 23:25:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 23:30:28 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 22 Jun 2021 23:30:29 GMT
ENV TOMCAT_MAJOR=8
# Tue, 22 Jun 2021 23:30:29 GMT
ENV TOMCAT_VERSION=8.5.68
# Tue, 22 Jun 2021 23:30:29 GMT
ENV TOMCAT_SHA512=673f8d295d6f6b8e53b30c9c81989a3586341f9660f00e61a131153f54f0ce9d41bf8f49960ef477d3ec81610e1c75c1684c8676e9ebe5015486334c443d82e5
# Fri, 02 Jul 2021 20:14:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 02 Jul 2021 20:14:25 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 02 Jul 2021 20:14:26 GMT
EXPOSE 8080
# Fri, 02 Jul 2021 20:14:26 GMT
CMD ["catalina.sh" "run"]
# Fri, 02 Jul 2021 22:10:38 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Fri, 02 Jul 2021 22:11:13 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 02 Jul 2021 22:12:05 GMT
ENV XWIKI_VERSION=12.10.8
# Fri, 02 Jul 2021 22:12:05 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.8
# Fri, 02 Jul 2021 22:12:05 GMT
ENV XWIKI_DOWNLOAD_SHA256=739471e78f8b2550849d1a869c27313c4c71b12bb9b6c9c26f77c81a993dff2e
# Fri, 02 Jul 2021 22:12:42 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 02 Jul 2021 22:12:44 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 02 Jul 2021 22:12:44 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 02 Jul 2021 22:12:44 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 02 Jul 2021 22:12:45 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 02 Jul 2021 22:12:45 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 02 Jul 2021 22:12:46 GMT
VOLUME [/usr/local/xwiki]
# Fri, 02 Jul 2021 22:12:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Jul 2021 22:12:46 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:6f86eded34a1950318569803a7e0c689175ebd9d76faf08798f88ac133b98a11`  
		Last Modified: Thu, 17 Jun 2021 23:56:04 GMT  
		Size: 27.2 MB (27158803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff470c6007f78550376884f4972cc5c767c6adc6f7d6002adddbddfb4600ea4b`  
		Last Modified: Fri, 18 Jun 2021 00:35:11 GMT  
		Size: 15.9 MB (15894169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a125d809875539cb0e1d2b0483b6223a65a2867db6c0df786d36feb6fa9bf260`  
		Last Modified: Fri, 18 Jun 2021 00:36:10 GMT  
		Size: 190.4 MB (190379258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599d9b9dba394414fe824f147f376772ae86db1750dd0c0865717476c25cd040`  
		Last Modified: Tue, 22 Jun 2021 23:41:56 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdf80a91fe0ee7a8d615c877013dd3f0f57f510581a488bb24e1d945dd212f30`  
		Last Modified: Fri, 02 Jul 2021 20:43:37 GMT  
		Size: 12.4 MB (12448780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f63370a9da1ce6088a59891070b42f6fe7d136d05c91aeb21d50398be035dbe`  
		Last Modified: Fri, 02 Jul 2021 20:43:34 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daed3696500a526a0b524e45ca20d612b3afdfbdf4e3b965b2384c9359de9952`  
		Last Modified: Fri, 02 Jul 2021 22:14:47 GMT  
		Size: 164.7 MB (164652294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2bdca7c7fda93fd53c72d634b26796ed47fea3732fa34e654e80f24a29e45d`  
		Last Modified: Fri, 02 Jul 2021 22:15:40 GMT  
		Size: 297.6 MB (297643088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1973f14560a22aba4dcd67d7d766ce12b6412478de10ca1ede26d89eef4ce002`  
		Last Modified: Fri, 02 Jul 2021 22:15:17 GMT  
		Size: 795.4 KB (795416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28dc40d8ca6a5141c9bb915f8bc1e4f7f6c72d41b8f9a67c68e1d7aef8ed4ef3`  
		Last Modified: Fri, 02 Jul 2021 22:15:17 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d684d9972a40fa0638d09f2706b84bd0fb4f24abd756f55d946d7fb7aac6509d`  
		Last Modified: Fri, 02 Jul 2021 22:15:17 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3cfc79bfb8d63baad54ecca1877c3f744947d18ec52ee2d7fc6ff840340841d`  
		Last Modified: Fri, 02 Jul 2021 22:15:17 GMT  
		Size: 5.2 KB (5230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7936b27fcebcf1c11910fcd1c354d7fe295b8a31ab83f21dd105e77e7edb3f0a`  
		Last Modified: Fri, 02 Jul 2021 22:15:17 GMT  
		Size: 2.5 KB (2501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13`

```console
$ docker pull xwiki@sha256:4eb72b2458ef8747b19e51ad101bf1e0a7b6959db0434d39f4b1abea7229002a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `xwiki:13` - linux; amd64

```console
$ docker pull xwiki@sha256:107067a099d5528b862d89ac83906bfadc1050c5afdb4df595d97c10276ca0b7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **724.9 MB (724906978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65c402c5f0d76e8b941063942552357d8aa1bd590d0a2ef6251038d241b52e2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:28:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 18 Jun 2021 00:29:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:29:44 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Fri, 18 Jun 2021 00:29:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 18 Jun 2021 00:29:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Jun 2021 00:29:55 GMT
CMD ["jshell"]
# Tue, 22 Jun 2021 22:44:10 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 22 Jun 2021 22:44:11 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 22 Jun 2021 22:44:12 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 22 Jun 2021 22:44:12 GMT
WORKDIR /usr/local/tomcat
# Tue, 22 Jun 2021 22:44:12 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 22:44:12 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 23:10:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 22 Jun 2021 23:10:49 GMT
ENV TOMCAT_MAJOR=8
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_VERSION=8.5.68
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_SHA512=673f8d295d6f6b8e53b30c9c81989a3586341f9660f00e61a131153f54f0ce9d41bf8f49960ef477d3ec81610e1c75c1684c8676e9ebe5015486334c443d82e5
# Fri, 02 Jul 2021 20:10:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 02 Jul 2021 20:10:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 02 Jul 2021 20:10:28 GMT
EXPOSE 8080
# Fri, 02 Jul 2021 20:10:29 GMT
CMD ["catalina.sh" "run"]
# Fri, 02 Jul 2021 21:20:19 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Fri, 02 Jul 2021 21:22:31 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 02 Jul 2021 21:22:32 GMT
ENV XWIKI_VERSION=13.5
# Fri, 02 Jul 2021 21:22:33 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.5
# Fri, 02 Jul 2021 21:22:33 GMT
ENV XWIKI_DOWNLOAD_SHA256=3294abb19636ab2e51930f88fa9a449dd98f1aa5b2ca8d6b1a32a5ff4dd22889
# Fri, 02 Jul 2021 21:23:12 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 02 Jul 2021 21:23:13 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Fri, 02 Jul 2021 21:23:13 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Fri, 02 Jul 2021 21:23:13 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Fri, 02 Jul 2021 21:23:13 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Fri, 02 Jul 2021 21:23:14 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Fri, 02 Jul 2021 21:23:15 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 02 Jul 2021 21:23:15 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 02 Jul 2021 21:23:15 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 02 Jul 2021 21:23:16 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 02 Jul 2021 21:23:17 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 02 Jul 2021 21:23:17 GMT
VOLUME [/usr/local/xwiki]
# Fri, 02 Jul 2021 21:23:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Jul 2021 21:23:17 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7766c75e8fade5c21578ec8566d2929e7238f9ac1dbe88551bf2f147b76c65`  
		Last Modified: Fri, 18 Jun 2021 00:39:29 GMT  
		Size: 16.0 MB (16033037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3025761fffcd095f302e914141cd91fdce2a0d7b76c4f13f96753ef8b9cc4151`  
		Last Modified: Fri, 18 Jun 2021 00:40:26 GMT  
		Size: 193.7 MB (193651024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fa731efc631621d3f50f90fbbcb2b097a684e8d8cb0315be61e939425e2c89`  
		Last Modified: Tue, 22 Jun 2021 23:19:37 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838b070fdc3792c062bb5b6c96d57e95aa826e3f672720a26fe4ce42e09f62a6`  
		Last Modified: Fri, 02 Jul 2021 20:35:19 GMT  
		Size: 12.4 MB (12449570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b092812f8972255279e884ddd841c549e700a49cbf30502b609090da11a8366`  
		Last Modified: Fri, 02 Jul 2021 20:35:17 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e0c6fa70e8651d71566b155d1603cdada3e0ef5e24989a737ff1331e504248`  
		Last Modified: Fri, 02 Jul 2021 21:29:22 GMT  
		Size: 167.7 MB (167687703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9681302d705266a8fda7b06cbedec7e60d3cbe8d3a7cd396de641c01629e1f2`  
		Last Modified: Fri, 02 Jul 2021 21:29:16 GMT  
		Size: 304.3 MB (304262474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:febdbb1e1ba93a3409f287bcf8b6971cdf6b5bd7192b5905ab0d7af2b96ead9a`  
		Last Modified: Fri, 02 Jul 2021 21:28:55 GMT  
		Size: 2.3 MB (2257829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca2789ef5e5b874e548c7a49a34f758e42756de18eac72edeff0189ab67149f5`  
		Last Modified: Fri, 02 Jul 2021 21:28:54 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe89a44c02a00b967200a2582dfd5ddf10e55eaab30ce22d4e2bb8005c1ebdb2`  
		Last Modified: Fri, 02 Jul 2021 21:28:54 GMT  
		Size: 2.3 KB (2320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf13ef31df43a7fad037054463d308cac6589cf505de9902895ae97a7f94eca`  
		Last Modified: Fri, 02 Jul 2021 21:28:54 GMT  
		Size: 5.2 KB (5176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cce921ec85eee9de8e6ba6260d7d1d4983b70de2f8f1cf11217f5d209d3da50`  
		Last Modified: Fri, 02 Jul 2021 21:28:54 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13-mysql-tomcat`

```console
$ docker pull xwiki@sha256:4eb72b2458ef8747b19e51ad101bf1e0a7b6959db0434d39f4b1abea7229002a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `xwiki:13-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:107067a099d5528b862d89ac83906bfadc1050c5afdb4df595d97c10276ca0b7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **724.9 MB (724906978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65c402c5f0d76e8b941063942552357d8aa1bd590d0a2ef6251038d241b52e2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:28:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 18 Jun 2021 00:29:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:29:44 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Fri, 18 Jun 2021 00:29:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 18 Jun 2021 00:29:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Jun 2021 00:29:55 GMT
CMD ["jshell"]
# Tue, 22 Jun 2021 22:44:10 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 22 Jun 2021 22:44:11 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 22 Jun 2021 22:44:12 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 22 Jun 2021 22:44:12 GMT
WORKDIR /usr/local/tomcat
# Tue, 22 Jun 2021 22:44:12 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 22:44:12 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 23:10:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 22 Jun 2021 23:10:49 GMT
ENV TOMCAT_MAJOR=8
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_VERSION=8.5.68
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_SHA512=673f8d295d6f6b8e53b30c9c81989a3586341f9660f00e61a131153f54f0ce9d41bf8f49960ef477d3ec81610e1c75c1684c8676e9ebe5015486334c443d82e5
# Fri, 02 Jul 2021 20:10:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 02 Jul 2021 20:10:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 02 Jul 2021 20:10:28 GMT
EXPOSE 8080
# Fri, 02 Jul 2021 20:10:29 GMT
CMD ["catalina.sh" "run"]
# Fri, 02 Jul 2021 21:20:19 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Fri, 02 Jul 2021 21:22:31 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 02 Jul 2021 21:22:32 GMT
ENV XWIKI_VERSION=13.5
# Fri, 02 Jul 2021 21:22:33 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.5
# Fri, 02 Jul 2021 21:22:33 GMT
ENV XWIKI_DOWNLOAD_SHA256=3294abb19636ab2e51930f88fa9a449dd98f1aa5b2ca8d6b1a32a5ff4dd22889
# Fri, 02 Jul 2021 21:23:12 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 02 Jul 2021 21:23:13 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Fri, 02 Jul 2021 21:23:13 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Fri, 02 Jul 2021 21:23:13 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Fri, 02 Jul 2021 21:23:13 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Fri, 02 Jul 2021 21:23:14 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Fri, 02 Jul 2021 21:23:15 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 02 Jul 2021 21:23:15 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 02 Jul 2021 21:23:15 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 02 Jul 2021 21:23:16 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 02 Jul 2021 21:23:17 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 02 Jul 2021 21:23:17 GMT
VOLUME [/usr/local/xwiki]
# Fri, 02 Jul 2021 21:23:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Jul 2021 21:23:17 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7766c75e8fade5c21578ec8566d2929e7238f9ac1dbe88551bf2f147b76c65`  
		Last Modified: Fri, 18 Jun 2021 00:39:29 GMT  
		Size: 16.0 MB (16033037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3025761fffcd095f302e914141cd91fdce2a0d7b76c4f13f96753ef8b9cc4151`  
		Last Modified: Fri, 18 Jun 2021 00:40:26 GMT  
		Size: 193.7 MB (193651024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fa731efc631621d3f50f90fbbcb2b097a684e8d8cb0315be61e939425e2c89`  
		Last Modified: Tue, 22 Jun 2021 23:19:37 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838b070fdc3792c062bb5b6c96d57e95aa826e3f672720a26fe4ce42e09f62a6`  
		Last Modified: Fri, 02 Jul 2021 20:35:19 GMT  
		Size: 12.4 MB (12449570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b092812f8972255279e884ddd841c549e700a49cbf30502b609090da11a8366`  
		Last Modified: Fri, 02 Jul 2021 20:35:17 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e0c6fa70e8651d71566b155d1603cdada3e0ef5e24989a737ff1331e504248`  
		Last Modified: Fri, 02 Jul 2021 21:29:22 GMT  
		Size: 167.7 MB (167687703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9681302d705266a8fda7b06cbedec7e60d3cbe8d3a7cd396de641c01629e1f2`  
		Last Modified: Fri, 02 Jul 2021 21:29:16 GMT  
		Size: 304.3 MB (304262474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:febdbb1e1ba93a3409f287bcf8b6971cdf6b5bd7192b5905ab0d7af2b96ead9a`  
		Last Modified: Fri, 02 Jul 2021 21:28:55 GMT  
		Size: 2.3 MB (2257829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca2789ef5e5b874e548c7a49a34f758e42756de18eac72edeff0189ab67149f5`  
		Last Modified: Fri, 02 Jul 2021 21:28:54 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe89a44c02a00b967200a2582dfd5ddf10e55eaab30ce22d4e2bb8005c1ebdb2`  
		Last Modified: Fri, 02 Jul 2021 21:28:54 GMT  
		Size: 2.3 KB (2320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf13ef31df43a7fad037054463d308cac6589cf505de9902895ae97a7f94eca`  
		Last Modified: Fri, 02 Jul 2021 21:28:54 GMT  
		Size: 5.2 KB (5176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cce921ec85eee9de8e6ba6260d7d1d4983b70de2f8f1cf11217f5d209d3da50`  
		Last Modified: Fri, 02 Jul 2021 21:28:54 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13-postgres-tomcat`

```console
$ docker pull xwiki@sha256:373a16b9f83d74cf54fd8d02441d4da3edb024b7661d91cd49bcfc6a14bb1d70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:13-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:f17c5ea6ceb05de50779f4f500d499c28d8a59cc6fefb33bef030e86d763e3c8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **724.2 MB (724244461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bfac1762ee5527ba0f46f2bc750dd1a00ce4874164963fabb2317767a6920f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:28:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 18 Jun 2021 00:29:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:29:44 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Fri, 18 Jun 2021 00:29:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 18 Jun 2021 00:29:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Jun 2021 00:29:55 GMT
CMD ["jshell"]
# Tue, 22 Jun 2021 22:44:10 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 22 Jun 2021 22:44:11 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 22 Jun 2021 22:44:12 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 22 Jun 2021 22:44:12 GMT
WORKDIR /usr/local/tomcat
# Tue, 22 Jun 2021 22:44:12 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 22:44:12 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 23:10:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 22 Jun 2021 23:10:49 GMT
ENV TOMCAT_MAJOR=8
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_VERSION=8.5.68
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_SHA512=673f8d295d6f6b8e53b30c9c81989a3586341f9660f00e61a131153f54f0ce9d41bf8f49960ef477d3ec81610e1c75c1684c8676e9ebe5015486334c443d82e5
# Fri, 02 Jul 2021 20:10:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 02 Jul 2021 20:10:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 02 Jul 2021 20:10:28 GMT
EXPOSE 8080
# Fri, 02 Jul 2021 20:10:29 GMT
CMD ["catalina.sh" "run"]
# Fri, 02 Jul 2021 21:20:19 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Fri, 02 Jul 2021 21:24:00 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 02 Jul 2021 21:24:01 GMT
ENV XWIKI_VERSION=13.5
# Fri, 02 Jul 2021 21:24:02 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.5
# Fri, 02 Jul 2021 21:24:02 GMT
ENV XWIKI_DOWNLOAD_SHA256=3294abb19636ab2e51930f88fa9a449dd98f1aa5b2ca8d6b1a32a5ff4dd22889
# Fri, 02 Jul 2021 21:24:41 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 02 Jul 2021 21:24:43 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 02 Jul 2021 21:24:43 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 02 Jul 2021 21:24:43 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 02 Jul 2021 21:24:44 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 02 Jul 2021 21:24:44 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 02 Jul 2021 21:24:45 GMT
VOLUME [/usr/local/xwiki]
# Fri, 02 Jul 2021 21:24:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Jul 2021 21:24:45 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7766c75e8fade5c21578ec8566d2929e7238f9ac1dbe88551bf2f147b76c65`  
		Last Modified: Fri, 18 Jun 2021 00:39:29 GMT  
		Size: 16.0 MB (16033037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3025761fffcd095f302e914141cd91fdce2a0d7b76c4f13f96753ef8b9cc4151`  
		Last Modified: Fri, 18 Jun 2021 00:40:26 GMT  
		Size: 193.7 MB (193651024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fa731efc631621d3f50f90fbbcb2b097a684e8d8cb0315be61e939425e2c89`  
		Last Modified: Tue, 22 Jun 2021 23:19:37 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838b070fdc3792c062bb5b6c96d57e95aa826e3f672720a26fe4ce42e09f62a6`  
		Last Modified: Fri, 02 Jul 2021 20:35:19 GMT  
		Size: 12.4 MB (12449570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b092812f8972255279e884ddd841c549e700a49cbf30502b609090da11a8366`  
		Last Modified: Fri, 02 Jul 2021 20:35:17 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632cb72d9488b73892dc69501fcea55c5c81f21d67fb024c3d81a13dd8e181f2`  
		Last Modified: Fri, 02 Jul 2021 21:30:30 GMT  
		Size: 168.5 MB (168487456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:767ddc1d5cc9d5ea1633a6812c6ad9d5f34045978d5451c81891ce6f3d12c337`  
		Last Modified: Fri, 02 Jul 2021 21:30:23 GMT  
		Size: 304.3 MB (304262477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b361707c0e73c7c324926a78689157d0b6e250f7501eccc39fd5dd4c44fa403c`  
		Last Modified: Fri, 02 Jul 2021 21:30:03 GMT  
		Size: 795.4 KB (795417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ebb2929fba6c692b148e1983d179a4b6aaa3474acadd557b98b46b3407cc31`  
		Last Modified: Fri, 02 Jul 2021 21:30:02 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31106cd81f9c71416e86249b91978b7bf077a7322566b0ce8cff5777639c6358`  
		Last Modified: Fri, 02 Jul 2021 21:30:02 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba012baa8e78ea94911aa405fbe7309d2afd806ee6809951d80b27fd08634b48`  
		Last Modified: Fri, 02 Jul 2021 21:30:03 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f5f84a4d0710d3a48a6098de893e454ea3d1c673040570260ed3b86f264e372`  
		Last Modified: Fri, 02 Jul 2021 21:30:02 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:13-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:52f4e634a6f13313406cc5cf0c1a342b4a80b74137ec9db23cbb46238c15c6cb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **715.6 MB (715603005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:905b3bf926ec7e0141e17ed2b04a0fc56d67a05567245b5c4afa09ec343d90b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 17 Jun 2021 23:53:58 GMT
ADD file:9e94a579f0495fce8fac6889d0b9b2cd576d5b3ce9f18ff913ad99a503756769 in / 
# Thu, 17 Jun 2021 23:53:59 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:31:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 18 Jun 2021 00:31:32 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:31:58 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Fri, 18 Jun 2021 00:32:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 18 Jun 2021 00:32:10 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Jun 2021 00:32:10 GMT
CMD ["jshell"]
# Tue, 22 Jun 2021 23:25:06 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 22 Jun 2021 23:25:06 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 22 Jun 2021 23:25:07 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 22 Jun 2021 23:25:07 GMT
WORKDIR /usr/local/tomcat
# Tue, 22 Jun 2021 23:25:07 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 23:25:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 23:30:28 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 22 Jun 2021 23:30:29 GMT
ENV TOMCAT_MAJOR=8
# Tue, 22 Jun 2021 23:30:29 GMT
ENV TOMCAT_VERSION=8.5.68
# Tue, 22 Jun 2021 23:30:29 GMT
ENV TOMCAT_SHA512=673f8d295d6f6b8e53b30c9c81989a3586341f9660f00e61a131153f54f0ce9d41bf8f49960ef477d3ec81610e1c75c1684c8676e9ebe5015486334c443d82e5
# Fri, 02 Jul 2021 20:14:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 02 Jul 2021 20:14:25 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 02 Jul 2021 20:14:26 GMT
EXPOSE 8080
# Fri, 02 Jul 2021 20:14:26 GMT
CMD ["catalina.sh" "run"]
# Fri, 02 Jul 2021 22:10:38 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Fri, 02 Jul 2021 22:11:13 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 02 Jul 2021 22:11:14 GMT
ENV XWIKI_VERSION=13.5
# Fri, 02 Jul 2021 22:11:14 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.5
# Fri, 02 Jul 2021 22:11:14 GMT
ENV XWIKI_DOWNLOAD_SHA256=3294abb19636ab2e51930f88fa9a449dd98f1aa5b2ca8d6b1a32a5ff4dd22889
# Fri, 02 Jul 2021 22:11:53 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 02 Jul 2021 22:11:54 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 02 Jul 2021 22:11:55 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 02 Jul 2021 22:11:55 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 02 Jul 2021 22:11:56 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 02 Jul 2021 22:11:56 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 02 Jul 2021 22:11:56 GMT
VOLUME [/usr/local/xwiki]
# Fri, 02 Jul 2021 22:11:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Jul 2021 22:11:56 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:6f86eded34a1950318569803a7e0c689175ebd9d76faf08798f88ac133b98a11`  
		Last Modified: Thu, 17 Jun 2021 23:56:04 GMT  
		Size: 27.2 MB (27158803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff470c6007f78550376884f4972cc5c767c6adc6f7d6002adddbddfb4600ea4b`  
		Last Modified: Fri, 18 Jun 2021 00:35:11 GMT  
		Size: 15.9 MB (15894169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a125d809875539cb0e1d2b0483b6223a65a2867db6c0df786d36feb6fa9bf260`  
		Last Modified: Fri, 18 Jun 2021 00:36:10 GMT  
		Size: 190.4 MB (190379258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599d9b9dba394414fe824f147f376772ae86db1750dd0c0865717476c25cd040`  
		Last Modified: Tue, 22 Jun 2021 23:41:56 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdf80a91fe0ee7a8d615c877013dd3f0f57f510581a488bb24e1d945dd212f30`  
		Last Modified: Fri, 02 Jul 2021 20:43:37 GMT  
		Size: 12.4 MB (12448780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f63370a9da1ce6088a59891070b42f6fe7d136d05c91aeb21d50398be035dbe`  
		Last Modified: Fri, 02 Jul 2021 20:43:34 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daed3696500a526a0b524e45ca20d612b3afdfbdf4e3b965b2384c9359de9952`  
		Last Modified: Fri, 02 Jul 2021 22:14:47 GMT  
		Size: 164.7 MB (164652294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a220e402041502b22a6098d44ced1d4099eae462963ccb07ab34997ae5350a4f`  
		Last Modified: Fri, 02 Jul 2021 22:14:43 GMT  
		Size: 304.3 MB (304262497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbe6d99c11bcf58c14ff7bd941299f80845365b2889062754658a6c30cbd8753`  
		Last Modified: Fri, 02 Jul 2021 22:14:20 GMT  
		Size: 795.4 KB (795415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6332f69ccc13af037975d4d700ab40f7a705e023f2574050671862a4151bbf9a`  
		Last Modified: Fri, 02 Jul 2021 22:14:19 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643f173e80f63080795f37afcb10709e14e4cfd799ae3b2fecccd4f205c05ed6`  
		Last Modified: Fri, 02 Jul 2021 22:14:19 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b91509711133471fa08ab523dab7699c2455003c7c247042893074f443700b`  
		Last Modified: Fri, 02 Jul 2021 22:14:20 GMT  
		Size: 5.2 KB (5173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca603534af32c6957d57352e18622eab0f5a32b16b1dc811586d6315f649725`  
		Last Modified: Fri, 02 Jul 2021 22:14:19 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13.4`

```console
$ docker pull xwiki@sha256:f6fb72d450a8f7c2b384df0619f6e1bfe37ac97c687e463ebc54571b06fa2e7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `xwiki:13.4` - linux; amd64

```console
$ docker pull xwiki@sha256:1aa388260a80c44d2b0e57e51edde1a7fbd2f3e4e78d0b12c253ed9655616a02
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **724.1 MB (724134760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af3b4a91f503c294b2bba0fc375b8324eade374d1f20913b17e0edde1e21d0ff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:28:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 18 Jun 2021 00:29:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:29:44 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Fri, 18 Jun 2021 00:29:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 18 Jun 2021 00:29:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Jun 2021 00:29:55 GMT
CMD ["jshell"]
# Tue, 22 Jun 2021 22:44:10 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 22 Jun 2021 22:44:11 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 22 Jun 2021 22:44:12 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 22 Jun 2021 22:44:12 GMT
WORKDIR /usr/local/tomcat
# Tue, 22 Jun 2021 22:44:12 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 22:44:12 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 23:10:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 22 Jun 2021 23:10:49 GMT
ENV TOMCAT_MAJOR=8
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_VERSION=8.5.68
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_SHA512=673f8d295d6f6b8e53b30c9c81989a3586341f9660f00e61a131153f54f0ce9d41bf8f49960ef477d3ec81610e1c75c1684c8676e9ebe5015486334c443d82e5
# Fri, 02 Jul 2021 20:10:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 02 Jul 2021 20:10:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 02 Jul 2021 20:10:28 GMT
EXPOSE 8080
# Fri, 02 Jul 2021 20:10:29 GMT
CMD ["catalina.sh" "run"]
# Fri, 02 Jul 2021 21:20:19 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Fri, 02 Jul 2021 21:22:31 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 02 Jul 2021 21:26:36 GMT
ENV XWIKI_VERSION=13.4.1
# Fri, 02 Jul 2021 21:26:36 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.4.1
# Fri, 02 Jul 2021 21:26:36 GMT
ENV XWIKI_DOWNLOAD_SHA256=efdc6fa585ad66134f2e8204445f675f6912ce843375a3f4e7d8a307bb0ae2d4
# Fri, 02 Jul 2021 21:27:16 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 02 Jul 2021 21:27:17 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Fri, 02 Jul 2021 21:27:17 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Fri, 02 Jul 2021 21:27:17 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Fri, 02 Jul 2021 21:27:17 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Fri, 02 Jul 2021 21:27:18 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Fri, 02 Jul 2021 21:27:19 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 02 Jul 2021 21:27:19 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 02 Jul 2021 21:27:19 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 02 Jul 2021 21:27:20 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 02 Jul 2021 21:27:21 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 02 Jul 2021 21:27:21 GMT
VOLUME [/usr/local/xwiki]
# Fri, 02 Jul 2021 21:27:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Jul 2021 21:27:21 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7766c75e8fade5c21578ec8566d2929e7238f9ac1dbe88551bf2f147b76c65`  
		Last Modified: Fri, 18 Jun 2021 00:39:29 GMT  
		Size: 16.0 MB (16033037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3025761fffcd095f302e914141cd91fdce2a0d7b76c4f13f96753ef8b9cc4151`  
		Last Modified: Fri, 18 Jun 2021 00:40:26 GMT  
		Size: 193.7 MB (193651024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fa731efc631621d3f50f90fbbcb2b097a684e8d8cb0315be61e939425e2c89`  
		Last Modified: Tue, 22 Jun 2021 23:19:37 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838b070fdc3792c062bb5b6c96d57e95aa826e3f672720a26fe4ce42e09f62a6`  
		Last Modified: Fri, 02 Jul 2021 20:35:19 GMT  
		Size: 12.4 MB (12449570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b092812f8972255279e884ddd841c549e700a49cbf30502b609090da11a8366`  
		Last Modified: Fri, 02 Jul 2021 20:35:17 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e0c6fa70e8651d71566b155d1603cdada3e0ef5e24989a737ff1331e504248`  
		Last Modified: Fri, 02 Jul 2021 21:29:22 GMT  
		Size: 167.7 MB (167687703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb926659fe16543d6269e1b7184704319bbffc787c0264022ec07d9d0d387621`  
		Last Modified: Fri, 02 Jul 2021 21:32:47 GMT  
		Size: 303.5 MB (303490264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cce08814f3dc9c2ee97eb9a41ba0e52e0b28b8d6fad82ae85a86e54e1879f489`  
		Last Modified: Fri, 02 Jul 2021 21:32:29 GMT  
		Size: 2.3 MB (2257826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb321821c5d89587d085ce2c0004a44dd1f8d5c192ae48e8fb37ea8afceab02`  
		Last Modified: Fri, 02 Jul 2021 21:32:29 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3f154f0e3dca96f6dfd40915bdb4595a7923ce4e3c1b372838e7b9f0b30faea`  
		Last Modified: Fri, 02 Jul 2021 21:32:29 GMT  
		Size: 2.3 KB (2318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b757be61a683b1e9dc97b103ca9b3f5320d6737a63dfa9680ac64c82d90c5d5c`  
		Last Modified: Fri, 02 Jul 2021 21:32:29 GMT  
		Size: 5.2 KB (5173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80b311bfd85d1751c718c5a5f62846c6bb36317821322f4a93d570b2651a3e5a`  
		Last Modified: Fri, 02 Jul 2021 21:32:29 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13.4-mysql-tomcat`

```console
$ docker pull xwiki@sha256:f6fb72d450a8f7c2b384df0619f6e1bfe37ac97c687e463ebc54571b06fa2e7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `xwiki:13.4-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:1aa388260a80c44d2b0e57e51edde1a7fbd2f3e4e78d0b12c253ed9655616a02
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **724.1 MB (724134760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af3b4a91f503c294b2bba0fc375b8324eade374d1f20913b17e0edde1e21d0ff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:28:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 18 Jun 2021 00:29:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:29:44 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Fri, 18 Jun 2021 00:29:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 18 Jun 2021 00:29:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Jun 2021 00:29:55 GMT
CMD ["jshell"]
# Tue, 22 Jun 2021 22:44:10 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 22 Jun 2021 22:44:11 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 22 Jun 2021 22:44:12 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 22 Jun 2021 22:44:12 GMT
WORKDIR /usr/local/tomcat
# Tue, 22 Jun 2021 22:44:12 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 22:44:12 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 23:10:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 22 Jun 2021 23:10:49 GMT
ENV TOMCAT_MAJOR=8
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_VERSION=8.5.68
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_SHA512=673f8d295d6f6b8e53b30c9c81989a3586341f9660f00e61a131153f54f0ce9d41bf8f49960ef477d3ec81610e1c75c1684c8676e9ebe5015486334c443d82e5
# Fri, 02 Jul 2021 20:10:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 02 Jul 2021 20:10:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 02 Jul 2021 20:10:28 GMT
EXPOSE 8080
# Fri, 02 Jul 2021 20:10:29 GMT
CMD ["catalina.sh" "run"]
# Fri, 02 Jul 2021 21:20:19 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Fri, 02 Jul 2021 21:22:31 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 02 Jul 2021 21:26:36 GMT
ENV XWIKI_VERSION=13.4.1
# Fri, 02 Jul 2021 21:26:36 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.4.1
# Fri, 02 Jul 2021 21:26:36 GMT
ENV XWIKI_DOWNLOAD_SHA256=efdc6fa585ad66134f2e8204445f675f6912ce843375a3f4e7d8a307bb0ae2d4
# Fri, 02 Jul 2021 21:27:16 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 02 Jul 2021 21:27:17 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Fri, 02 Jul 2021 21:27:17 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Fri, 02 Jul 2021 21:27:17 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Fri, 02 Jul 2021 21:27:17 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Fri, 02 Jul 2021 21:27:18 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Fri, 02 Jul 2021 21:27:19 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 02 Jul 2021 21:27:19 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 02 Jul 2021 21:27:19 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 02 Jul 2021 21:27:20 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 02 Jul 2021 21:27:21 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 02 Jul 2021 21:27:21 GMT
VOLUME [/usr/local/xwiki]
# Fri, 02 Jul 2021 21:27:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Jul 2021 21:27:21 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7766c75e8fade5c21578ec8566d2929e7238f9ac1dbe88551bf2f147b76c65`  
		Last Modified: Fri, 18 Jun 2021 00:39:29 GMT  
		Size: 16.0 MB (16033037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3025761fffcd095f302e914141cd91fdce2a0d7b76c4f13f96753ef8b9cc4151`  
		Last Modified: Fri, 18 Jun 2021 00:40:26 GMT  
		Size: 193.7 MB (193651024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fa731efc631621d3f50f90fbbcb2b097a684e8d8cb0315be61e939425e2c89`  
		Last Modified: Tue, 22 Jun 2021 23:19:37 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838b070fdc3792c062bb5b6c96d57e95aa826e3f672720a26fe4ce42e09f62a6`  
		Last Modified: Fri, 02 Jul 2021 20:35:19 GMT  
		Size: 12.4 MB (12449570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b092812f8972255279e884ddd841c549e700a49cbf30502b609090da11a8366`  
		Last Modified: Fri, 02 Jul 2021 20:35:17 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e0c6fa70e8651d71566b155d1603cdada3e0ef5e24989a737ff1331e504248`  
		Last Modified: Fri, 02 Jul 2021 21:29:22 GMT  
		Size: 167.7 MB (167687703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb926659fe16543d6269e1b7184704319bbffc787c0264022ec07d9d0d387621`  
		Last Modified: Fri, 02 Jul 2021 21:32:47 GMT  
		Size: 303.5 MB (303490264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cce08814f3dc9c2ee97eb9a41ba0e52e0b28b8d6fad82ae85a86e54e1879f489`  
		Last Modified: Fri, 02 Jul 2021 21:32:29 GMT  
		Size: 2.3 MB (2257826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb321821c5d89587d085ce2c0004a44dd1f8d5c192ae48e8fb37ea8afceab02`  
		Last Modified: Fri, 02 Jul 2021 21:32:29 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3f154f0e3dca96f6dfd40915bdb4595a7923ce4e3c1b372838e7b9f0b30faea`  
		Last Modified: Fri, 02 Jul 2021 21:32:29 GMT  
		Size: 2.3 KB (2318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b757be61a683b1e9dc97b103ca9b3f5320d6737a63dfa9680ac64c82d90c5d5c`  
		Last Modified: Fri, 02 Jul 2021 21:32:29 GMT  
		Size: 5.2 KB (5173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80b311bfd85d1751c718c5a5f62846c6bb36317821322f4a93d570b2651a3e5a`  
		Last Modified: Fri, 02 Jul 2021 21:32:29 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13.4-postgres-tomcat`

```console
$ docker pull xwiki@sha256:6912c21cb039e477796492ab74ce335edb842644fcae5980ad47b40f2d92c5d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:13.4-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:5498b4d279cf5e5e5c1a94ac5329117b59b52fc256952c8441ed87de49510074
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **723.5 MB (723472261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bd0e3cbc273d269673e7a939c632e0b9537c5fb7571470adc051f7a3e7d9d8c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:28:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 18 Jun 2021 00:29:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:29:44 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Fri, 18 Jun 2021 00:29:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 18 Jun 2021 00:29:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Jun 2021 00:29:55 GMT
CMD ["jshell"]
# Tue, 22 Jun 2021 22:44:10 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 22 Jun 2021 22:44:11 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 22 Jun 2021 22:44:12 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 22 Jun 2021 22:44:12 GMT
WORKDIR /usr/local/tomcat
# Tue, 22 Jun 2021 22:44:12 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 22:44:12 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 23:10:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 22 Jun 2021 23:10:49 GMT
ENV TOMCAT_MAJOR=8
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_VERSION=8.5.68
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_SHA512=673f8d295d6f6b8e53b30c9c81989a3586341f9660f00e61a131153f54f0ce9d41bf8f49960ef477d3ec81610e1c75c1684c8676e9ebe5015486334c443d82e5
# Fri, 02 Jul 2021 20:10:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 02 Jul 2021 20:10:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 02 Jul 2021 20:10:28 GMT
EXPOSE 8080
# Fri, 02 Jul 2021 20:10:29 GMT
CMD ["catalina.sh" "run"]
# Fri, 02 Jul 2021 21:20:19 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Fri, 02 Jul 2021 21:24:00 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 02 Jul 2021 21:27:27 GMT
ENV XWIKI_VERSION=13.4.1
# Fri, 02 Jul 2021 21:27:27 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.4.1
# Fri, 02 Jul 2021 21:27:27 GMT
ENV XWIKI_DOWNLOAD_SHA256=efdc6fa585ad66134f2e8204445f675f6912ce843375a3f4e7d8a307bb0ae2d4
# Fri, 02 Jul 2021 21:28:06 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 02 Jul 2021 21:28:08 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 02 Jul 2021 21:28:08 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 02 Jul 2021 21:28:08 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 02 Jul 2021 21:28:09 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 02 Jul 2021 21:28:09 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 02 Jul 2021 21:28:10 GMT
VOLUME [/usr/local/xwiki]
# Fri, 02 Jul 2021 21:28:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Jul 2021 21:28:10 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7766c75e8fade5c21578ec8566d2929e7238f9ac1dbe88551bf2f147b76c65`  
		Last Modified: Fri, 18 Jun 2021 00:39:29 GMT  
		Size: 16.0 MB (16033037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3025761fffcd095f302e914141cd91fdce2a0d7b76c4f13f96753ef8b9cc4151`  
		Last Modified: Fri, 18 Jun 2021 00:40:26 GMT  
		Size: 193.7 MB (193651024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fa731efc631621d3f50f90fbbcb2b097a684e8d8cb0315be61e939425e2c89`  
		Last Modified: Tue, 22 Jun 2021 23:19:37 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838b070fdc3792c062bb5b6c96d57e95aa826e3f672720a26fe4ce42e09f62a6`  
		Last Modified: Fri, 02 Jul 2021 20:35:19 GMT  
		Size: 12.4 MB (12449570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b092812f8972255279e884ddd841c549e700a49cbf30502b609090da11a8366`  
		Last Modified: Fri, 02 Jul 2021 20:35:17 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632cb72d9488b73892dc69501fcea55c5c81f21d67fb024c3d81a13dd8e181f2`  
		Last Modified: Fri, 02 Jul 2021 21:30:30 GMT  
		Size: 168.5 MB (168487456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fcc4894aae41ce3e21774e51d6ab895b9d98fd7e568f0143a83e42ba6c56427`  
		Last Modified: Fri, 02 Jul 2021 21:33:23 GMT  
		Size: 303.5 MB (303490293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d355b8bead477f7d305574a122bb19f337b292071efcf019d82ff554d335ac66`  
		Last Modified: Fri, 02 Jul 2021 21:33:05 GMT  
		Size: 795.4 KB (795415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a71eadd1b2b54e49d28db0c47bd436d1e3217439a80bf89b204bbb5e0ce895b6`  
		Last Modified: Fri, 02 Jul 2021 21:33:04 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a140553afaa84d12ba72894f8adb24037c02da2ab77006829401fa0c4650f0e`  
		Last Modified: Fri, 02 Jul 2021 21:33:05 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:797300b91be5d6d44a5690f8dd67a2f8d39877396af9de85c870819d8509b14f`  
		Last Modified: Fri, 02 Jul 2021 21:33:05 GMT  
		Size: 5.2 KB (5171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6733aca94a99028e27b6f3a1e19a2c6a57ea8aa436e561fcc0f9bd625995ef48`  
		Last Modified: Fri, 02 Jul 2021 21:33:05 GMT  
		Size: 2.5 KB (2501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:13.4-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:5e7bb9f516d8cb2302183987b74644a9bf85dcba166d6a1bc0a9300460016df8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **714.8 MB (714830761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e12df77fa4d87344726d4a907635c1978c3fa9ec488a4fc1f3989c96d66d7102`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 17 Jun 2021 23:53:58 GMT
ADD file:9e94a579f0495fce8fac6889d0b9b2cd576d5b3ce9f18ff913ad99a503756769 in / 
# Thu, 17 Jun 2021 23:53:59 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:31:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 18 Jun 2021 00:31:32 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:31:58 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Fri, 18 Jun 2021 00:32:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 18 Jun 2021 00:32:10 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Jun 2021 00:32:10 GMT
CMD ["jshell"]
# Tue, 22 Jun 2021 23:25:06 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 22 Jun 2021 23:25:06 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 22 Jun 2021 23:25:07 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 22 Jun 2021 23:25:07 GMT
WORKDIR /usr/local/tomcat
# Tue, 22 Jun 2021 23:25:07 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 23:25:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 23:30:28 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 22 Jun 2021 23:30:29 GMT
ENV TOMCAT_MAJOR=8
# Tue, 22 Jun 2021 23:30:29 GMT
ENV TOMCAT_VERSION=8.5.68
# Tue, 22 Jun 2021 23:30:29 GMT
ENV TOMCAT_SHA512=673f8d295d6f6b8e53b30c9c81989a3586341f9660f00e61a131153f54f0ce9d41bf8f49960ef477d3ec81610e1c75c1684c8676e9ebe5015486334c443d82e5
# Fri, 02 Jul 2021 20:14:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 02 Jul 2021 20:14:25 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 02 Jul 2021 20:14:26 GMT
EXPOSE 8080
# Fri, 02 Jul 2021 20:14:26 GMT
CMD ["catalina.sh" "run"]
# Fri, 02 Jul 2021 22:10:38 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Fri, 02 Jul 2021 22:11:13 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 02 Jul 2021 22:12:57 GMT
ENV XWIKI_VERSION=13.4.1
# Fri, 02 Jul 2021 22:12:57 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.4.1
# Fri, 02 Jul 2021 22:12:57 GMT
ENV XWIKI_DOWNLOAD_SHA256=efdc6fa585ad66134f2e8204445f675f6912ce843375a3f4e7d8a307bb0ae2d4
# Fri, 02 Jul 2021 22:13:35 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 02 Jul 2021 22:13:36 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 02 Jul 2021 22:13:36 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 02 Jul 2021 22:13:37 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 02 Jul 2021 22:13:37 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 02 Jul 2021 22:13:38 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 02 Jul 2021 22:13:38 GMT
VOLUME [/usr/local/xwiki]
# Fri, 02 Jul 2021 22:13:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Jul 2021 22:13:38 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:6f86eded34a1950318569803a7e0c689175ebd9d76faf08798f88ac133b98a11`  
		Last Modified: Thu, 17 Jun 2021 23:56:04 GMT  
		Size: 27.2 MB (27158803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff470c6007f78550376884f4972cc5c767c6adc6f7d6002adddbddfb4600ea4b`  
		Last Modified: Fri, 18 Jun 2021 00:35:11 GMT  
		Size: 15.9 MB (15894169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a125d809875539cb0e1d2b0483b6223a65a2867db6c0df786d36feb6fa9bf260`  
		Last Modified: Fri, 18 Jun 2021 00:36:10 GMT  
		Size: 190.4 MB (190379258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599d9b9dba394414fe824f147f376772ae86db1750dd0c0865717476c25cd040`  
		Last Modified: Tue, 22 Jun 2021 23:41:56 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdf80a91fe0ee7a8d615c877013dd3f0f57f510581a488bb24e1d945dd212f30`  
		Last Modified: Fri, 02 Jul 2021 20:43:37 GMT  
		Size: 12.4 MB (12448780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f63370a9da1ce6088a59891070b42f6fe7d136d05c91aeb21d50398be035dbe`  
		Last Modified: Fri, 02 Jul 2021 20:43:34 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daed3696500a526a0b524e45ca20d612b3afdfbdf4e3b965b2384c9359de9952`  
		Last Modified: Fri, 02 Jul 2021 22:14:47 GMT  
		Size: 164.7 MB (164652294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c3ce163385d5c3f01c8199fbd4cb222bb4048d5ff49a06765f65ca9e9ee8639`  
		Last Modified: Fri, 02 Jul 2021 22:16:28 GMT  
		Size: 303.5 MB (303490263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ab71ffd0909056a83edde823f2b642cb24ad94d39aa226ae96f93612d8eac8`  
		Last Modified: Fri, 02 Jul 2021 22:16:05 GMT  
		Size: 795.4 KB (795415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba54c170b1ee6361908e2a62ad0a9f045317cb1a0bb6fe282d215d903b3d58c`  
		Last Modified: Fri, 02 Jul 2021 22:16:05 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b0c1226a52f4b385b63ddef7e7b381fd8988669fadb883b9804a4e99f26666c`  
		Last Modified: Fri, 02 Jul 2021 22:16:05 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:701de273a3a9a9a77746f1bb9413498ad66acfd4d8cf87c11de91a925a16c1f6`  
		Last Modified: Fri, 02 Jul 2021 22:16:04 GMT  
		Size: 5.2 KB (5172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a22a9051dc87108a1bfae60deac2d6b4637590db7f8e0db27f70b330eaea972`  
		Last Modified: Fri, 02 Jul 2021 22:16:05 GMT  
		Size: 2.5 KB (2500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13.4.1`

```console
$ docker pull xwiki@sha256:f6fb72d450a8f7c2b384df0619f6e1bfe37ac97c687e463ebc54571b06fa2e7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `xwiki:13.4.1` - linux; amd64

```console
$ docker pull xwiki@sha256:1aa388260a80c44d2b0e57e51edde1a7fbd2f3e4e78d0b12c253ed9655616a02
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **724.1 MB (724134760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af3b4a91f503c294b2bba0fc375b8324eade374d1f20913b17e0edde1e21d0ff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:28:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 18 Jun 2021 00:29:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:29:44 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Fri, 18 Jun 2021 00:29:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 18 Jun 2021 00:29:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Jun 2021 00:29:55 GMT
CMD ["jshell"]
# Tue, 22 Jun 2021 22:44:10 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 22 Jun 2021 22:44:11 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 22 Jun 2021 22:44:12 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 22 Jun 2021 22:44:12 GMT
WORKDIR /usr/local/tomcat
# Tue, 22 Jun 2021 22:44:12 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 22:44:12 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 23:10:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 22 Jun 2021 23:10:49 GMT
ENV TOMCAT_MAJOR=8
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_VERSION=8.5.68
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_SHA512=673f8d295d6f6b8e53b30c9c81989a3586341f9660f00e61a131153f54f0ce9d41bf8f49960ef477d3ec81610e1c75c1684c8676e9ebe5015486334c443d82e5
# Fri, 02 Jul 2021 20:10:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 02 Jul 2021 20:10:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 02 Jul 2021 20:10:28 GMT
EXPOSE 8080
# Fri, 02 Jul 2021 20:10:29 GMT
CMD ["catalina.sh" "run"]
# Fri, 02 Jul 2021 21:20:19 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Fri, 02 Jul 2021 21:22:31 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 02 Jul 2021 21:26:36 GMT
ENV XWIKI_VERSION=13.4.1
# Fri, 02 Jul 2021 21:26:36 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.4.1
# Fri, 02 Jul 2021 21:26:36 GMT
ENV XWIKI_DOWNLOAD_SHA256=efdc6fa585ad66134f2e8204445f675f6912ce843375a3f4e7d8a307bb0ae2d4
# Fri, 02 Jul 2021 21:27:16 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 02 Jul 2021 21:27:17 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Fri, 02 Jul 2021 21:27:17 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Fri, 02 Jul 2021 21:27:17 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Fri, 02 Jul 2021 21:27:17 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Fri, 02 Jul 2021 21:27:18 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Fri, 02 Jul 2021 21:27:19 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 02 Jul 2021 21:27:19 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 02 Jul 2021 21:27:19 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 02 Jul 2021 21:27:20 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 02 Jul 2021 21:27:21 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 02 Jul 2021 21:27:21 GMT
VOLUME [/usr/local/xwiki]
# Fri, 02 Jul 2021 21:27:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Jul 2021 21:27:21 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7766c75e8fade5c21578ec8566d2929e7238f9ac1dbe88551bf2f147b76c65`  
		Last Modified: Fri, 18 Jun 2021 00:39:29 GMT  
		Size: 16.0 MB (16033037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3025761fffcd095f302e914141cd91fdce2a0d7b76c4f13f96753ef8b9cc4151`  
		Last Modified: Fri, 18 Jun 2021 00:40:26 GMT  
		Size: 193.7 MB (193651024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fa731efc631621d3f50f90fbbcb2b097a684e8d8cb0315be61e939425e2c89`  
		Last Modified: Tue, 22 Jun 2021 23:19:37 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838b070fdc3792c062bb5b6c96d57e95aa826e3f672720a26fe4ce42e09f62a6`  
		Last Modified: Fri, 02 Jul 2021 20:35:19 GMT  
		Size: 12.4 MB (12449570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b092812f8972255279e884ddd841c549e700a49cbf30502b609090da11a8366`  
		Last Modified: Fri, 02 Jul 2021 20:35:17 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e0c6fa70e8651d71566b155d1603cdada3e0ef5e24989a737ff1331e504248`  
		Last Modified: Fri, 02 Jul 2021 21:29:22 GMT  
		Size: 167.7 MB (167687703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb926659fe16543d6269e1b7184704319bbffc787c0264022ec07d9d0d387621`  
		Last Modified: Fri, 02 Jul 2021 21:32:47 GMT  
		Size: 303.5 MB (303490264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cce08814f3dc9c2ee97eb9a41ba0e52e0b28b8d6fad82ae85a86e54e1879f489`  
		Last Modified: Fri, 02 Jul 2021 21:32:29 GMT  
		Size: 2.3 MB (2257826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb321821c5d89587d085ce2c0004a44dd1f8d5c192ae48e8fb37ea8afceab02`  
		Last Modified: Fri, 02 Jul 2021 21:32:29 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3f154f0e3dca96f6dfd40915bdb4595a7923ce4e3c1b372838e7b9f0b30faea`  
		Last Modified: Fri, 02 Jul 2021 21:32:29 GMT  
		Size: 2.3 KB (2318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b757be61a683b1e9dc97b103ca9b3f5320d6737a63dfa9680ac64c82d90c5d5c`  
		Last Modified: Fri, 02 Jul 2021 21:32:29 GMT  
		Size: 5.2 KB (5173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80b311bfd85d1751c718c5a5f62846c6bb36317821322f4a93d570b2651a3e5a`  
		Last Modified: Fri, 02 Jul 2021 21:32:29 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13.4.1-mysql-tomcat`

```console
$ docker pull xwiki@sha256:f6fb72d450a8f7c2b384df0619f6e1bfe37ac97c687e463ebc54571b06fa2e7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `xwiki:13.4.1-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:1aa388260a80c44d2b0e57e51edde1a7fbd2f3e4e78d0b12c253ed9655616a02
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **724.1 MB (724134760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af3b4a91f503c294b2bba0fc375b8324eade374d1f20913b17e0edde1e21d0ff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:28:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 18 Jun 2021 00:29:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:29:44 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Fri, 18 Jun 2021 00:29:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 18 Jun 2021 00:29:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Jun 2021 00:29:55 GMT
CMD ["jshell"]
# Tue, 22 Jun 2021 22:44:10 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 22 Jun 2021 22:44:11 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 22 Jun 2021 22:44:12 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 22 Jun 2021 22:44:12 GMT
WORKDIR /usr/local/tomcat
# Tue, 22 Jun 2021 22:44:12 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 22:44:12 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 23:10:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 22 Jun 2021 23:10:49 GMT
ENV TOMCAT_MAJOR=8
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_VERSION=8.5.68
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_SHA512=673f8d295d6f6b8e53b30c9c81989a3586341f9660f00e61a131153f54f0ce9d41bf8f49960ef477d3ec81610e1c75c1684c8676e9ebe5015486334c443d82e5
# Fri, 02 Jul 2021 20:10:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 02 Jul 2021 20:10:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 02 Jul 2021 20:10:28 GMT
EXPOSE 8080
# Fri, 02 Jul 2021 20:10:29 GMT
CMD ["catalina.sh" "run"]
# Fri, 02 Jul 2021 21:20:19 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Fri, 02 Jul 2021 21:22:31 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 02 Jul 2021 21:26:36 GMT
ENV XWIKI_VERSION=13.4.1
# Fri, 02 Jul 2021 21:26:36 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.4.1
# Fri, 02 Jul 2021 21:26:36 GMT
ENV XWIKI_DOWNLOAD_SHA256=efdc6fa585ad66134f2e8204445f675f6912ce843375a3f4e7d8a307bb0ae2d4
# Fri, 02 Jul 2021 21:27:16 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 02 Jul 2021 21:27:17 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Fri, 02 Jul 2021 21:27:17 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Fri, 02 Jul 2021 21:27:17 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Fri, 02 Jul 2021 21:27:17 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Fri, 02 Jul 2021 21:27:18 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Fri, 02 Jul 2021 21:27:19 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 02 Jul 2021 21:27:19 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 02 Jul 2021 21:27:19 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 02 Jul 2021 21:27:20 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 02 Jul 2021 21:27:21 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 02 Jul 2021 21:27:21 GMT
VOLUME [/usr/local/xwiki]
# Fri, 02 Jul 2021 21:27:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Jul 2021 21:27:21 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7766c75e8fade5c21578ec8566d2929e7238f9ac1dbe88551bf2f147b76c65`  
		Last Modified: Fri, 18 Jun 2021 00:39:29 GMT  
		Size: 16.0 MB (16033037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3025761fffcd095f302e914141cd91fdce2a0d7b76c4f13f96753ef8b9cc4151`  
		Last Modified: Fri, 18 Jun 2021 00:40:26 GMT  
		Size: 193.7 MB (193651024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fa731efc631621d3f50f90fbbcb2b097a684e8d8cb0315be61e939425e2c89`  
		Last Modified: Tue, 22 Jun 2021 23:19:37 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838b070fdc3792c062bb5b6c96d57e95aa826e3f672720a26fe4ce42e09f62a6`  
		Last Modified: Fri, 02 Jul 2021 20:35:19 GMT  
		Size: 12.4 MB (12449570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b092812f8972255279e884ddd841c549e700a49cbf30502b609090da11a8366`  
		Last Modified: Fri, 02 Jul 2021 20:35:17 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e0c6fa70e8651d71566b155d1603cdada3e0ef5e24989a737ff1331e504248`  
		Last Modified: Fri, 02 Jul 2021 21:29:22 GMT  
		Size: 167.7 MB (167687703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb926659fe16543d6269e1b7184704319bbffc787c0264022ec07d9d0d387621`  
		Last Modified: Fri, 02 Jul 2021 21:32:47 GMT  
		Size: 303.5 MB (303490264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cce08814f3dc9c2ee97eb9a41ba0e52e0b28b8d6fad82ae85a86e54e1879f489`  
		Last Modified: Fri, 02 Jul 2021 21:32:29 GMT  
		Size: 2.3 MB (2257826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb321821c5d89587d085ce2c0004a44dd1f8d5c192ae48e8fb37ea8afceab02`  
		Last Modified: Fri, 02 Jul 2021 21:32:29 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3f154f0e3dca96f6dfd40915bdb4595a7923ce4e3c1b372838e7b9f0b30faea`  
		Last Modified: Fri, 02 Jul 2021 21:32:29 GMT  
		Size: 2.3 KB (2318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b757be61a683b1e9dc97b103ca9b3f5320d6737a63dfa9680ac64c82d90c5d5c`  
		Last Modified: Fri, 02 Jul 2021 21:32:29 GMT  
		Size: 5.2 KB (5173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80b311bfd85d1751c718c5a5f62846c6bb36317821322f4a93d570b2651a3e5a`  
		Last Modified: Fri, 02 Jul 2021 21:32:29 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13.4.1-postgres-tomcat`

```console
$ docker pull xwiki@sha256:6912c21cb039e477796492ab74ce335edb842644fcae5980ad47b40f2d92c5d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:13.4.1-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:5498b4d279cf5e5e5c1a94ac5329117b59b52fc256952c8441ed87de49510074
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **723.5 MB (723472261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bd0e3cbc273d269673e7a939c632e0b9537c5fb7571470adc051f7a3e7d9d8c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:28:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 18 Jun 2021 00:29:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:29:44 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Fri, 18 Jun 2021 00:29:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 18 Jun 2021 00:29:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Jun 2021 00:29:55 GMT
CMD ["jshell"]
# Tue, 22 Jun 2021 22:44:10 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 22 Jun 2021 22:44:11 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 22 Jun 2021 22:44:12 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 22 Jun 2021 22:44:12 GMT
WORKDIR /usr/local/tomcat
# Tue, 22 Jun 2021 22:44:12 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 22:44:12 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 23:10:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 22 Jun 2021 23:10:49 GMT
ENV TOMCAT_MAJOR=8
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_VERSION=8.5.68
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_SHA512=673f8d295d6f6b8e53b30c9c81989a3586341f9660f00e61a131153f54f0ce9d41bf8f49960ef477d3ec81610e1c75c1684c8676e9ebe5015486334c443d82e5
# Fri, 02 Jul 2021 20:10:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 02 Jul 2021 20:10:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 02 Jul 2021 20:10:28 GMT
EXPOSE 8080
# Fri, 02 Jul 2021 20:10:29 GMT
CMD ["catalina.sh" "run"]
# Fri, 02 Jul 2021 21:20:19 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Fri, 02 Jul 2021 21:24:00 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 02 Jul 2021 21:27:27 GMT
ENV XWIKI_VERSION=13.4.1
# Fri, 02 Jul 2021 21:27:27 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.4.1
# Fri, 02 Jul 2021 21:27:27 GMT
ENV XWIKI_DOWNLOAD_SHA256=efdc6fa585ad66134f2e8204445f675f6912ce843375a3f4e7d8a307bb0ae2d4
# Fri, 02 Jul 2021 21:28:06 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 02 Jul 2021 21:28:08 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 02 Jul 2021 21:28:08 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 02 Jul 2021 21:28:08 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 02 Jul 2021 21:28:09 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 02 Jul 2021 21:28:09 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 02 Jul 2021 21:28:10 GMT
VOLUME [/usr/local/xwiki]
# Fri, 02 Jul 2021 21:28:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Jul 2021 21:28:10 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7766c75e8fade5c21578ec8566d2929e7238f9ac1dbe88551bf2f147b76c65`  
		Last Modified: Fri, 18 Jun 2021 00:39:29 GMT  
		Size: 16.0 MB (16033037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3025761fffcd095f302e914141cd91fdce2a0d7b76c4f13f96753ef8b9cc4151`  
		Last Modified: Fri, 18 Jun 2021 00:40:26 GMT  
		Size: 193.7 MB (193651024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fa731efc631621d3f50f90fbbcb2b097a684e8d8cb0315be61e939425e2c89`  
		Last Modified: Tue, 22 Jun 2021 23:19:37 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838b070fdc3792c062bb5b6c96d57e95aa826e3f672720a26fe4ce42e09f62a6`  
		Last Modified: Fri, 02 Jul 2021 20:35:19 GMT  
		Size: 12.4 MB (12449570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b092812f8972255279e884ddd841c549e700a49cbf30502b609090da11a8366`  
		Last Modified: Fri, 02 Jul 2021 20:35:17 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632cb72d9488b73892dc69501fcea55c5c81f21d67fb024c3d81a13dd8e181f2`  
		Last Modified: Fri, 02 Jul 2021 21:30:30 GMT  
		Size: 168.5 MB (168487456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fcc4894aae41ce3e21774e51d6ab895b9d98fd7e568f0143a83e42ba6c56427`  
		Last Modified: Fri, 02 Jul 2021 21:33:23 GMT  
		Size: 303.5 MB (303490293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d355b8bead477f7d305574a122bb19f337b292071efcf019d82ff554d335ac66`  
		Last Modified: Fri, 02 Jul 2021 21:33:05 GMT  
		Size: 795.4 KB (795415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a71eadd1b2b54e49d28db0c47bd436d1e3217439a80bf89b204bbb5e0ce895b6`  
		Last Modified: Fri, 02 Jul 2021 21:33:04 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a140553afaa84d12ba72894f8adb24037c02da2ab77006829401fa0c4650f0e`  
		Last Modified: Fri, 02 Jul 2021 21:33:05 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:797300b91be5d6d44a5690f8dd67a2f8d39877396af9de85c870819d8509b14f`  
		Last Modified: Fri, 02 Jul 2021 21:33:05 GMT  
		Size: 5.2 KB (5171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6733aca94a99028e27b6f3a1e19a2c6a57ea8aa436e561fcc0f9bd625995ef48`  
		Last Modified: Fri, 02 Jul 2021 21:33:05 GMT  
		Size: 2.5 KB (2501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:13.4.1-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:5e7bb9f516d8cb2302183987b74644a9bf85dcba166d6a1bc0a9300460016df8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **714.8 MB (714830761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e12df77fa4d87344726d4a907635c1978c3fa9ec488a4fc1f3989c96d66d7102`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 17 Jun 2021 23:53:58 GMT
ADD file:9e94a579f0495fce8fac6889d0b9b2cd576d5b3ce9f18ff913ad99a503756769 in / 
# Thu, 17 Jun 2021 23:53:59 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:31:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 18 Jun 2021 00:31:32 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:31:58 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Fri, 18 Jun 2021 00:32:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 18 Jun 2021 00:32:10 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Jun 2021 00:32:10 GMT
CMD ["jshell"]
# Tue, 22 Jun 2021 23:25:06 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 22 Jun 2021 23:25:06 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 22 Jun 2021 23:25:07 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 22 Jun 2021 23:25:07 GMT
WORKDIR /usr/local/tomcat
# Tue, 22 Jun 2021 23:25:07 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 23:25:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 23:30:28 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 22 Jun 2021 23:30:29 GMT
ENV TOMCAT_MAJOR=8
# Tue, 22 Jun 2021 23:30:29 GMT
ENV TOMCAT_VERSION=8.5.68
# Tue, 22 Jun 2021 23:30:29 GMT
ENV TOMCAT_SHA512=673f8d295d6f6b8e53b30c9c81989a3586341f9660f00e61a131153f54f0ce9d41bf8f49960ef477d3ec81610e1c75c1684c8676e9ebe5015486334c443d82e5
# Fri, 02 Jul 2021 20:14:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 02 Jul 2021 20:14:25 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 02 Jul 2021 20:14:26 GMT
EXPOSE 8080
# Fri, 02 Jul 2021 20:14:26 GMT
CMD ["catalina.sh" "run"]
# Fri, 02 Jul 2021 22:10:38 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Fri, 02 Jul 2021 22:11:13 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 02 Jul 2021 22:12:57 GMT
ENV XWIKI_VERSION=13.4.1
# Fri, 02 Jul 2021 22:12:57 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.4.1
# Fri, 02 Jul 2021 22:12:57 GMT
ENV XWIKI_DOWNLOAD_SHA256=efdc6fa585ad66134f2e8204445f675f6912ce843375a3f4e7d8a307bb0ae2d4
# Fri, 02 Jul 2021 22:13:35 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 02 Jul 2021 22:13:36 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 02 Jul 2021 22:13:36 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 02 Jul 2021 22:13:37 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 02 Jul 2021 22:13:37 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 02 Jul 2021 22:13:38 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 02 Jul 2021 22:13:38 GMT
VOLUME [/usr/local/xwiki]
# Fri, 02 Jul 2021 22:13:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Jul 2021 22:13:38 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:6f86eded34a1950318569803a7e0c689175ebd9d76faf08798f88ac133b98a11`  
		Last Modified: Thu, 17 Jun 2021 23:56:04 GMT  
		Size: 27.2 MB (27158803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff470c6007f78550376884f4972cc5c767c6adc6f7d6002adddbddfb4600ea4b`  
		Last Modified: Fri, 18 Jun 2021 00:35:11 GMT  
		Size: 15.9 MB (15894169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a125d809875539cb0e1d2b0483b6223a65a2867db6c0df786d36feb6fa9bf260`  
		Last Modified: Fri, 18 Jun 2021 00:36:10 GMT  
		Size: 190.4 MB (190379258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599d9b9dba394414fe824f147f376772ae86db1750dd0c0865717476c25cd040`  
		Last Modified: Tue, 22 Jun 2021 23:41:56 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdf80a91fe0ee7a8d615c877013dd3f0f57f510581a488bb24e1d945dd212f30`  
		Last Modified: Fri, 02 Jul 2021 20:43:37 GMT  
		Size: 12.4 MB (12448780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f63370a9da1ce6088a59891070b42f6fe7d136d05c91aeb21d50398be035dbe`  
		Last Modified: Fri, 02 Jul 2021 20:43:34 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daed3696500a526a0b524e45ca20d612b3afdfbdf4e3b965b2384c9359de9952`  
		Last Modified: Fri, 02 Jul 2021 22:14:47 GMT  
		Size: 164.7 MB (164652294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c3ce163385d5c3f01c8199fbd4cb222bb4048d5ff49a06765f65ca9e9ee8639`  
		Last Modified: Fri, 02 Jul 2021 22:16:28 GMT  
		Size: 303.5 MB (303490263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ab71ffd0909056a83edde823f2b642cb24ad94d39aa226ae96f93612d8eac8`  
		Last Modified: Fri, 02 Jul 2021 22:16:05 GMT  
		Size: 795.4 KB (795415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba54c170b1ee6361908e2a62ad0a9f045317cb1a0bb6fe282d215d903b3d58c`  
		Last Modified: Fri, 02 Jul 2021 22:16:05 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b0c1226a52f4b385b63ddef7e7b381fd8988669fadb883b9804a4e99f26666c`  
		Last Modified: Fri, 02 Jul 2021 22:16:05 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:701de273a3a9a9a77746f1bb9413498ad66acfd4d8cf87c11de91a925a16c1f6`  
		Last Modified: Fri, 02 Jul 2021 22:16:04 GMT  
		Size: 5.2 KB (5172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a22a9051dc87108a1bfae60deac2d6b4637590db7f8e0db27f70b330eaea972`  
		Last Modified: Fri, 02 Jul 2021 22:16:05 GMT  
		Size: 2.5 KB (2500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13.5`

```console
$ docker pull xwiki@sha256:4eb72b2458ef8747b19e51ad101bf1e0a7b6959db0434d39f4b1abea7229002a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `xwiki:13.5` - linux; amd64

```console
$ docker pull xwiki@sha256:107067a099d5528b862d89ac83906bfadc1050c5afdb4df595d97c10276ca0b7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **724.9 MB (724906978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65c402c5f0d76e8b941063942552357d8aa1bd590d0a2ef6251038d241b52e2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:28:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 18 Jun 2021 00:29:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:29:44 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Fri, 18 Jun 2021 00:29:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 18 Jun 2021 00:29:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Jun 2021 00:29:55 GMT
CMD ["jshell"]
# Tue, 22 Jun 2021 22:44:10 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 22 Jun 2021 22:44:11 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 22 Jun 2021 22:44:12 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 22 Jun 2021 22:44:12 GMT
WORKDIR /usr/local/tomcat
# Tue, 22 Jun 2021 22:44:12 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 22:44:12 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 23:10:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 22 Jun 2021 23:10:49 GMT
ENV TOMCAT_MAJOR=8
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_VERSION=8.5.68
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_SHA512=673f8d295d6f6b8e53b30c9c81989a3586341f9660f00e61a131153f54f0ce9d41bf8f49960ef477d3ec81610e1c75c1684c8676e9ebe5015486334c443d82e5
# Fri, 02 Jul 2021 20:10:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 02 Jul 2021 20:10:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 02 Jul 2021 20:10:28 GMT
EXPOSE 8080
# Fri, 02 Jul 2021 20:10:29 GMT
CMD ["catalina.sh" "run"]
# Fri, 02 Jul 2021 21:20:19 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Fri, 02 Jul 2021 21:22:31 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 02 Jul 2021 21:22:32 GMT
ENV XWIKI_VERSION=13.5
# Fri, 02 Jul 2021 21:22:33 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.5
# Fri, 02 Jul 2021 21:22:33 GMT
ENV XWIKI_DOWNLOAD_SHA256=3294abb19636ab2e51930f88fa9a449dd98f1aa5b2ca8d6b1a32a5ff4dd22889
# Fri, 02 Jul 2021 21:23:12 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 02 Jul 2021 21:23:13 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Fri, 02 Jul 2021 21:23:13 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Fri, 02 Jul 2021 21:23:13 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Fri, 02 Jul 2021 21:23:13 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Fri, 02 Jul 2021 21:23:14 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Fri, 02 Jul 2021 21:23:15 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 02 Jul 2021 21:23:15 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 02 Jul 2021 21:23:15 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 02 Jul 2021 21:23:16 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 02 Jul 2021 21:23:17 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 02 Jul 2021 21:23:17 GMT
VOLUME [/usr/local/xwiki]
# Fri, 02 Jul 2021 21:23:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Jul 2021 21:23:17 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7766c75e8fade5c21578ec8566d2929e7238f9ac1dbe88551bf2f147b76c65`  
		Last Modified: Fri, 18 Jun 2021 00:39:29 GMT  
		Size: 16.0 MB (16033037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3025761fffcd095f302e914141cd91fdce2a0d7b76c4f13f96753ef8b9cc4151`  
		Last Modified: Fri, 18 Jun 2021 00:40:26 GMT  
		Size: 193.7 MB (193651024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fa731efc631621d3f50f90fbbcb2b097a684e8d8cb0315be61e939425e2c89`  
		Last Modified: Tue, 22 Jun 2021 23:19:37 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838b070fdc3792c062bb5b6c96d57e95aa826e3f672720a26fe4ce42e09f62a6`  
		Last Modified: Fri, 02 Jul 2021 20:35:19 GMT  
		Size: 12.4 MB (12449570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b092812f8972255279e884ddd841c549e700a49cbf30502b609090da11a8366`  
		Last Modified: Fri, 02 Jul 2021 20:35:17 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e0c6fa70e8651d71566b155d1603cdada3e0ef5e24989a737ff1331e504248`  
		Last Modified: Fri, 02 Jul 2021 21:29:22 GMT  
		Size: 167.7 MB (167687703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9681302d705266a8fda7b06cbedec7e60d3cbe8d3a7cd396de641c01629e1f2`  
		Last Modified: Fri, 02 Jul 2021 21:29:16 GMT  
		Size: 304.3 MB (304262474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:febdbb1e1ba93a3409f287bcf8b6971cdf6b5bd7192b5905ab0d7af2b96ead9a`  
		Last Modified: Fri, 02 Jul 2021 21:28:55 GMT  
		Size: 2.3 MB (2257829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca2789ef5e5b874e548c7a49a34f758e42756de18eac72edeff0189ab67149f5`  
		Last Modified: Fri, 02 Jul 2021 21:28:54 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe89a44c02a00b967200a2582dfd5ddf10e55eaab30ce22d4e2bb8005c1ebdb2`  
		Last Modified: Fri, 02 Jul 2021 21:28:54 GMT  
		Size: 2.3 KB (2320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf13ef31df43a7fad037054463d308cac6589cf505de9902895ae97a7f94eca`  
		Last Modified: Fri, 02 Jul 2021 21:28:54 GMT  
		Size: 5.2 KB (5176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cce921ec85eee9de8e6ba6260d7d1d4983b70de2f8f1cf11217f5d209d3da50`  
		Last Modified: Fri, 02 Jul 2021 21:28:54 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13.5-mysql-tomcat`

```console
$ docker pull xwiki@sha256:4eb72b2458ef8747b19e51ad101bf1e0a7b6959db0434d39f4b1abea7229002a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `xwiki:13.5-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:107067a099d5528b862d89ac83906bfadc1050c5afdb4df595d97c10276ca0b7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **724.9 MB (724906978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65c402c5f0d76e8b941063942552357d8aa1bd590d0a2ef6251038d241b52e2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:28:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 18 Jun 2021 00:29:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:29:44 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Fri, 18 Jun 2021 00:29:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 18 Jun 2021 00:29:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Jun 2021 00:29:55 GMT
CMD ["jshell"]
# Tue, 22 Jun 2021 22:44:10 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 22 Jun 2021 22:44:11 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 22 Jun 2021 22:44:12 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 22 Jun 2021 22:44:12 GMT
WORKDIR /usr/local/tomcat
# Tue, 22 Jun 2021 22:44:12 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 22:44:12 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 23:10:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 22 Jun 2021 23:10:49 GMT
ENV TOMCAT_MAJOR=8
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_VERSION=8.5.68
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_SHA512=673f8d295d6f6b8e53b30c9c81989a3586341f9660f00e61a131153f54f0ce9d41bf8f49960ef477d3ec81610e1c75c1684c8676e9ebe5015486334c443d82e5
# Fri, 02 Jul 2021 20:10:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 02 Jul 2021 20:10:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 02 Jul 2021 20:10:28 GMT
EXPOSE 8080
# Fri, 02 Jul 2021 20:10:29 GMT
CMD ["catalina.sh" "run"]
# Fri, 02 Jul 2021 21:20:19 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Fri, 02 Jul 2021 21:22:31 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 02 Jul 2021 21:22:32 GMT
ENV XWIKI_VERSION=13.5
# Fri, 02 Jul 2021 21:22:33 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.5
# Fri, 02 Jul 2021 21:22:33 GMT
ENV XWIKI_DOWNLOAD_SHA256=3294abb19636ab2e51930f88fa9a449dd98f1aa5b2ca8d6b1a32a5ff4dd22889
# Fri, 02 Jul 2021 21:23:12 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 02 Jul 2021 21:23:13 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Fri, 02 Jul 2021 21:23:13 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Fri, 02 Jul 2021 21:23:13 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Fri, 02 Jul 2021 21:23:13 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Fri, 02 Jul 2021 21:23:14 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Fri, 02 Jul 2021 21:23:15 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 02 Jul 2021 21:23:15 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 02 Jul 2021 21:23:15 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 02 Jul 2021 21:23:16 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 02 Jul 2021 21:23:17 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 02 Jul 2021 21:23:17 GMT
VOLUME [/usr/local/xwiki]
# Fri, 02 Jul 2021 21:23:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Jul 2021 21:23:17 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7766c75e8fade5c21578ec8566d2929e7238f9ac1dbe88551bf2f147b76c65`  
		Last Modified: Fri, 18 Jun 2021 00:39:29 GMT  
		Size: 16.0 MB (16033037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3025761fffcd095f302e914141cd91fdce2a0d7b76c4f13f96753ef8b9cc4151`  
		Last Modified: Fri, 18 Jun 2021 00:40:26 GMT  
		Size: 193.7 MB (193651024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fa731efc631621d3f50f90fbbcb2b097a684e8d8cb0315be61e939425e2c89`  
		Last Modified: Tue, 22 Jun 2021 23:19:37 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838b070fdc3792c062bb5b6c96d57e95aa826e3f672720a26fe4ce42e09f62a6`  
		Last Modified: Fri, 02 Jul 2021 20:35:19 GMT  
		Size: 12.4 MB (12449570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b092812f8972255279e884ddd841c549e700a49cbf30502b609090da11a8366`  
		Last Modified: Fri, 02 Jul 2021 20:35:17 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e0c6fa70e8651d71566b155d1603cdada3e0ef5e24989a737ff1331e504248`  
		Last Modified: Fri, 02 Jul 2021 21:29:22 GMT  
		Size: 167.7 MB (167687703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9681302d705266a8fda7b06cbedec7e60d3cbe8d3a7cd396de641c01629e1f2`  
		Last Modified: Fri, 02 Jul 2021 21:29:16 GMT  
		Size: 304.3 MB (304262474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:febdbb1e1ba93a3409f287bcf8b6971cdf6b5bd7192b5905ab0d7af2b96ead9a`  
		Last Modified: Fri, 02 Jul 2021 21:28:55 GMT  
		Size: 2.3 MB (2257829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca2789ef5e5b874e548c7a49a34f758e42756de18eac72edeff0189ab67149f5`  
		Last Modified: Fri, 02 Jul 2021 21:28:54 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe89a44c02a00b967200a2582dfd5ddf10e55eaab30ce22d4e2bb8005c1ebdb2`  
		Last Modified: Fri, 02 Jul 2021 21:28:54 GMT  
		Size: 2.3 KB (2320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf13ef31df43a7fad037054463d308cac6589cf505de9902895ae97a7f94eca`  
		Last Modified: Fri, 02 Jul 2021 21:28:54 GMT  
		Size: 5.2 KB (5176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cce921ec85eee9de8e6ba6260d7d1d4983b70de2f8f1cf11217f5d209d3da50`  
		Last Modified: Fri, 02 Jul 2021 21:28:54 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13.5-postgres-tomcat`

```console
$ docker pull xwiki@sha256:373a16b9f83d74cf54fd8d02441d4da3edb024b7661d91cd49bcfc6a14bb1d70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:13.5-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:f17c5ea6ceb05de50779f4f500d499c28d8a59cc6fefb33bef030e86d763e3c8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **724.2 MB (724244461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bfac1762ee5527ba0f46f2bc750dd1a00ce4874164963fabb2317767a6920f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:28:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 18 Jun 2021 00:29:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:29:44 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Fri, 18 Jun 2021 00:29:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 18 Jun 2021 00:29:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Jun 2021 00:29:55 GMT
CMD ["jshell"]
# Tue, 22 Jun 2021 22:44:10 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 22 Jun 2021 22:44:11 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 22 Jun 2021 22:44:12 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 22 Jun 2021 22:44:12 GMT
WORKDIR /usr/local/tomcat
# Tue, 22 Jun 2021 22:44:12 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 22:44:12 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 23:10:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 22 Jun 2021 23:10:49 GMT
ENV TOMCAT_MAJOR=8
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_VERSION=8.5.68
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_SHA512=673f8d295d6f6b8e53b30c9c81989a3586341f9660f00e61a131153f54f0ce9d41bf8f49960ef477d3ec81610e1c75c1684c8676e9ebe5015486334c443d82e5
# Fri, 02 Jul 2021 20:10:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 02 Jul 2021 20:10:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 02 Jul 2021 20:10:28 GMT
EXPOSE 8080
# Fri, 02 Jul 2021 20:10:29 GMT
CMD ["catalina.sh" "run"]
# Fri, 02 Jul 2021 21:20:19 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Fri, 02 Jul 2021 21:24:00 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 02 Jul 2021 21:24:01 GMT
ENV XWIKI_VERSION=13.5
# Fri, 02 Jul 2021 21:24:02 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.5
# Fri, 02 Jul 2021 21:24:02 GMT
ENV XWIKI_DOWNLOAD_SHA256=3294abb19636ab2e51930f88fa9a449dd98f1aa5b2ca8d6b1a32a5ff4dd22889
# Fri, 02 Jul 2021 21:24:41 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 02 Jul 2021 21:24:43 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 02 Jul 2021 21:24:43 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 02 Jul 2021 21:24:43 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 02 Jul 2021 21:24:44 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 02 Jul 2021 21:24:44 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 02 Jul 2021 21:24:45 GMT
VOLUME [/usr/local/xwiki]
# Fri, 02 Jul 2021 21:24:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Jul 2021 21:24:45 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7766c75e8fade5c21578ec8566d2929e7238f9ac1dbe88551bf2f147b76c65`  
		Last Modified: Fri, 18 Jun 2021 00:39:29 GMT  
		Size: 16.0 MB (16033037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3025761fffcd095f302e914141cd91fdce2a0d7b76c4f13f96753ef8b9cc4151`  
		Last Modified: Fri, 18 Jun 2021 00:40:26 GMT  
		Size: 193.7 MB (193651024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fa731efc631621d3f50f90fbbcb2b097a684e8d8cb0315be61e939425e2c89`  
		Last Modified: Tue, 22 Jun 2021 23:19:37 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838b070fdc3792c062bb5b6c96d57e95aa826e3f672720a26fe4ce42e09f62a6`  
		Last Modified: Fri, 02 Jul 2021 20:35:19 GMT  
		Size: 12.4 MB (12449570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b092812f8972255279e884ddd841c549e700a49cbf30502b609090da11a8366`  
		Last Modified: Fri, 02 Jul 2021 20:35:17 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632cb72d9488b73892dc69501fcea55c5c81f21d67fb024c3d81a13dd8e181f2`  
		Last Modified: Fri, 02 Jul 2021 21:30:30 GMT  
		Size: 168.5 MB (168487456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:767ddc1d5cc9d5ea1633a6812c6ad9d5f34045978d5451c81891ce6f3d12c337`  
		Last Modified: Fri, 02 Jul 2021 21:30:23 GMT  
		Size: 304.3 MB (304262477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b361707c0e73c7c324926a78689157d0b6e250f7501eccc39fd5dd4c44fa403c`  
		Last Modified: Fri, 02 Jul 2021 21:30:03 GMT  
		Size: 795.4 KB (795417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ebb2929fba6c692b148e1983d179a4b6aaa3474acadd557b98b46b3407cc31`  
		Last Modified: Fri, 02 Jul 2021 21:30:02 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31106cd81f9c71416e86249b91978b7bf077a7322566b0ce8cff5777639c6358`  
		Last Modified: Fri, 02 Jul 2021 21:30:02 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba012baa8e78ea94911aa405fbe7309d2afd806ee6809951d80b27fd08634b48`  
		Last Modified: Fri, 02 Jul 2021 21:30:03 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f5f84a4d0710d3a48a6098de893e454ea3d1c673040570260ed3b86f264e372`  
		Last Modified: Fri, 02 Jul 2021 21:30:02 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:13.5-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:52f4e634a6f13313406cc5cf0c1a342b4a80b74137ec9db23cbb46238c15c6cb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **715.6 MB (715603005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:905b3bf926ec7e0141e17ed2b04a0fc56d67a05567245b5c4afa09ec343d90b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 17 Jun 2021 23:53:58 GMT
ADD file:9e94a579f0495fce8fac6889d0b9b2cd576d5b3ce9f18ff913ad99a503756769 in / 
# Thu, 17 Jun 2021 23:53:59 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:31:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 18 Jun 2021 00:31:32 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:31:58 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Fri, 18 Jun 2021 00:32:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 18 Jun 2021 00:32:10 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Jun 2021 00:32:10 GMT
CMD ["jshell"]
# Tue, 22 Jun 2021 23:25:06 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 22 Jun 2021 23:25:06 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 22 Jun 2021 23:25:07 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 22 Jun 2021 23:25:07 GMT
WORKDIR /usr/local/tomcat
# Tue, 22 Jun 2021 23:25:07 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 23:25:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 23:30:28 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 22 Jun 2021 23:30:29 GMT
ENV TOMCAT_MAJOR=8
# Tue, 22 Jun 2021 23:30:29 GMT
ENV TOMCAT_VERSION=8.5.68
# Tue, 22 Jun 2021 23:30:29 GMT
ENV TOMCAT_SHA512=673f8d295d6f6b8e53b30c9c81989a3586341f9660f00e61a131153f54f0ce9d41bf8f49960ef477d3ec81610e1c75c1684c8676e9ebe5015486334c443d82e5
# Fri, 02 Jul 2021 20:14:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 02 Jul 2021 20:14:25 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 02 Jul 2021 20:14:26 GMT
EXPOSE 8080
# Fri, 02 Jul 2021 20:14:26 GMT
CMD ["catalina.sh" "run"]
# Fri, 02 Jul 2021 22:10:38 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Fri, 02 Jul 2021 22:11:13 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 02 Jul 2021 22:11:14 GMT
ENV XWIKI_VERSION=13.5
# Fri, 02 Jul 2021 22:11:14 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.5
# Fri, 02 Jul 2021 22:11:14 GMT
ENV XWIKI_DOWNLOAD_SHA256=3294abb19636ab2e51930f88fa9a449dd98f1aa5b2ca8d6b1a32a5ff4dd22889
# Fri, 02 Jul 2021 22:11:53 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 02 Jul 2021 22:11:54 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 02 Jul 2021 22:11:55 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 02 Jul 2021 22:11:55 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 02 Jul 2021 22:11:56 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 02 Jul 2021 22:11:56 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 02 Jul 2021 22:11:56 GMT
VOLUME [/usr/local/xwiki]
# Fri, 02 Jul 2021 22:11:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Jul 2021 22:11:56 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:6f86eded34a1950318569803a7e0c689175ebd9d76faf08798f88ac133b98a11`  
		Last Modified: Thu, 17 Jun 2021 23:56:04 GMT  
		Size: 27.2 MB (27158803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff470c6007f78550376884f4972cc5c767c6adc6f7d6002adddbddfb4600ea4b`  
		Last Modified: Fri, 18 Jun 2021 00:35:11 GMT  
		Size: 15.9 MB (15894169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a125d809875539cb0e1d2b0483b6223a65a2867db6c0df786d36feb6fa9bf260`  
		Last Modified: Fri, 18 Jun 2021 00:36:10 GMT  
		Size: 190.4 MB (190379258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599d9b9dba394414fe824f147f376772ae86db1750dd0c0865717476c25cd040`  
		Last Modified: Tue, 22 Jun 2021 23:41:56 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdf80a91fe0ee7a8d615c877013dd3f0f57f510581a488bb24e1d945dd212f30`  
		Last Modified: Fri, 02 Jul 2021 20:43:37 GMT  
		Size: 12.4 MB (12448780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f63370a9da1ce6088a59891070b42f6fe7d136d05c91aeb21d50398be035dbe`  
		Last Modified: Fri, 02 Jul 2021 20:43:34 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daed3696500a526a0b524e45ca20d612b3afdfbdf4e3b965b2384c9359de9952`  
		Last Modified: Fri, 02 Jul 2021 22:14:47 GMT  
		Size: 164.7 MB (164652294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a220e402041502b22a6098d44ced1d4099eae462963ccb07ab34997ae5350a4f`  
		Last Modified: Fri, 02 Jul 2021 22:14:43 GMT  
		Size: 304.3 MB (304262497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbe6d99c11bcf58c14ff7bd941299f80845365b2889062754658a6c30cbd8753`  
		Last Modified: Fri, 02 Jul 2021 22:14:20 GMT  
		Size: 795.4 KB (795415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6332f69ccc13af037975d4d700ab40f7a705e023f2574050671862a4151bbf9a`  
		Last Modified: Fri, 02 Jul 2021 22:14:19 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643f173e80f63080795f37afcb10709e14e4cfd799ae3b2fecccd4f205c05ed6`  
		Last Modified: Fri, 02 Jul 2021 22:14:19 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b91509711133471fa08ab523dab7699c2455003c7c247042893074f443700b`  
		Last Modified: Fri, 02 Jul 2021 22:14:20 GMT  
		Size: 5.2 KB (5173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca603534af32c6957d57352e18622eab0f5a32b16b1dc811586d6315f649725`  
		Last Modified: Fri, 02 Jul 2021 22:14:19 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13.5.0`

```console
$ docker pull xwiki@sha256:4eb72b2458ef8747b19e51ad101bf1e0a7b6959db0434d39f4b1abea7229002a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `xwiki:13.5.0` - linux; amd64

```console
$ docker pull xwiki@sha256:107067a099d5528b862d89ac83906bfadc1050c5afdb4df595d97c10276ca0b7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **724.9 MB (724906978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65c402c5f0d76e8b941063942552357d8aa1bd590d0a2ef6251038d241b52e2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:28:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 18 Jun 2021 00:29:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:29:44 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Fri, 18 Jun 2021 00:29:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 18 Jun 2021 00:29:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Jun 2021 00:29:55 GMT
CMD ["jshell"]
# Tue, 22 Jun 2021 22:44:10 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 22 Jun 2021 22:44:11 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 22 Jun 2021 22:44:12 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 22 Jun 2021 22:44:12 GMT
WORKDIR /usr/local/tomcat
# Tue, 22 Jun 2021 22:44:12 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 22:44:12 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 23:10:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 22 Jun 2021 23:10:49 GMT
ENV TOMCAT_MAJOR=8
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_VERSION=8.5.68
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_SHA512=673f8d295d6f6b8e53b30c9c81989a3586341f9660f00e61a131153f54f0ce9d41bf8f49960ef477d3ec81610e1c75c1684c8676e9ebe5015486334c443d82e5
# Fri, 02 Jul 2021 20:10:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 02 Jul 2021 20:10:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 02 Jul 2021 20:10:28 GMT
EXPOSE 8080
# Fri, 02 Jul 2021 20:10:29 GMT
CMD ["catalina.sh" "run"]
# Fri, 02 Jul 2021 21:20:19 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Fri, 02 Jul 2021 21:22:31 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 02 Jul 2021 21:22:32 GMT
ENV XWIKI_VERSION=13.5
# Fri, 02 Jul 2021 21:22:33 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.5
# Fri, 02 Jul 2021 21:22:33 GMT
ENV XWIKI_DOWNLOAD_SHA256=3294abb19636ab2e51930f88fa9a449dd98f1aa5b2ca8d6b1a32a5ff4dd22889
# Fri, 02 Jul 2021 21:23:12 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 02 Jul 2021 21:23:13 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Fri, 02 Jul 2021 21:23:13 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Fri, 02 Jul 2021 21:23:13 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Fri, 02 Jul 2021 21:23:13 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Fri, 02 Jul 2021 21:23:14 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Fri, 02 Jul 2021 21:23:15 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 02 Jul 2021 21:23:15 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 02 Jul 2021 21:23:15 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 02 Jul 2021 21:23:16 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 02 Jul 2021 21:23:17 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 02 Jul 2021 21:23:17 GMT
VOLUME [/usr/local/xwiki]
# Fri, 02 Jul 2021 21:23:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Jul 2021 21:23:17 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7766c75e8fade5c21578ec8566d2929e7238f9ac1dbe88551bf2f147b76c65`  
		Last Modified: Fri, 18 Jun 2021 00:39:29 GMT  
		Size: 16.0 MB (16033037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3025761fffcd095f302e914141cd91fdce2a0d7b76c4f13f96753ef8b9cc4151`  
		Last Modified: Fri, 18 Jun 2021 00:40:26 GMT  
		Size: 193.7 MB (193651024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fa731efc631621d3f50f90fbbcb2b097a684e8d8cb0315be61e939425e2c89`  
		Last Modified: Tue, 22 Jun 2021 23:19:37 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838b070fdc3792c062bb5b6c96d57e95aa826e3f672720a26fe4ce42e09f62a6`  
		Last Modified: Fri, 02 Jul 2021 20:35:19 GMT  
		Size: 12.4 MB (12449570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b092812f8972255279e884ddd841c549e700a49cbf30502b609090da11a8366`  
		Last Modified: Fri, 02 Jul 2021 20:35:17 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e0c6fa70e8651d71566b155d1603cdada3e0ef5e24989a737ff1331e504248`  
		Last Modified: Fri, 02 Jul 2021 21:29:22 GMT  
		Size: 167.7 MB (167687703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9681302d705266a8fda7b06cbedec7e60d3cbe8d3a7cd396de641c01629e1f2`  
		Last Modified: Fri, 02 Jul 2021 21:29:16 GMT  
		Size: 304.3 MB (304262474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:febdbb1e1ba93a3409f287bcf8b6971cdf6b5bd7192b5905ab0d7af2b96ead9a`  
		Last Modified: Fri, 02 Jul 2021 21:28:55 GMT  
		Size: 2.3 MB (2257829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca2789ef5e5b874e548c7a49a34f758e42756de18eac72edeff0189ab67149f5`  
		Last Modified: Fri, 02 Jul 2021 21:28:54 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe89a44c02a00b967200a2582dfd5ddf10e55eaab30ce22d4e2bb8005c1ebdb2`  
		Last Modified: Fri, 02 Jul 2021 21:28:54 GMT  
		Size: 2.3 KB (2320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf13ef31df43a7fad037054463d308cac6589cf505de9902895ae97a7f94eca`  
		Last Modified: Fri, 02 Jul 2021 21:28:54 GMT  
		Size: 5.2 KB (5176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cce921ec85eee9de8e6ba6260d7d1d4983b70de2f8f1cf11217f5d209d3da50`  
		Last Modified: Fri, 02 Jul 2021 21:28:54 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13.5.0-mysql-tomcat`

```console
$ docker pull xwiki@sha256:4eb72b2458ef8747b19e51ad101bf1e0a7b6959db0434d39f4b1abea7229002a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `xwiki:13.5.0-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:107067a099d5528b862d89ac83906bfadc1050c5afdb4df595d97c10276ca0b7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **724.9 MB (724906978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65c402c5f0d76e8b941063942552357d8aa1bd590d0a2ef6251038d241b52e2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:28:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 18 Jun 2021 00:29:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:29:44 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Fri, 18 Jun 2021 00:29:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 18 Jun 2021 00:29:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Jun 2021 00:29:55 GMT
CMD ["jshell"]
# Tue, 22 Jun 2021 22:44:10 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 22 Jun 2021 22:44:11 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 22 Jun 2021 22:44:12 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 22 Jun 2021 22:44:12 GMT
WORKDIR /usr/local/tomcat
# Tue, 22 Jun 2021 22:44:12 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 22:44:12 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 23:10:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 22 Jun 2021 23:10:49 GMT
ENV TOMCAT_MAJOR=8
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_VERSION=8.5.68
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_SHA512=673f8d295d6f6b8e53b30c9c81989a3586341f9660f00e61a131153f54f0ce9d41bf8f49960ef477d3ec81610e1c75c1684c8676e9ebe5015486334c443d82e5
# Fri, 02 Jul 2021 20:10:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 02 Jul 2021 20:10:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 02 Jul 2021 20:10:28 GMT
EXPOSE 8080
# Fri, 02 Jul 2021 20:10:29 GMT
CMD ["catalina.sh" "run"]
# Fri, 02 Jul 2021 21:20:19 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Fri, 02 Jul 2021 21:22:31 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 02 Jul 2021 21:22:32 GMT
ENV XWIKI_VERSION=13.5
# Fri, 02 Jul 2021 21:22:33 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.5
# Fri, 02 Jul 2021 21:22:33 GMT
ENV XWIKI_DOWNLOAD_SHA256=3294abb19636ab2e51930f88fa9a449dd98f1aa5b2ca8d6b1a32a5ff4dd22889
# Fri, 02 Jul 2021 21:23:12 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 02 Jul 2021 21:23:13 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Fri, 02 Jul 2021 21:23:13 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Fri, 02 Jul 2021 21:23:13 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Fri, 02 Jul 2021 21:23:13 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Fri, 02 Jul 2021 21:23:14 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Fri, 02 Jul 2021 21:23:15 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 02 Jul 2021 21:23:15 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 02 Jul 2021 21:23:15 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 02 Jul 2021 21:23:16 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 02 Jul 2021 21:23:17 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 02 Jul 2021 21:23:17 GMT
VOLUME [/usr/local/xwiki]
# Fri, 02 Jul 2021 21:23:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Jul 2021 21:23:17 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7766c75e8fade5c21578ec8566d2929e7238f9ac1dbe88551bf2f147b76c65`  
		Last Modified: Fri, 18 Jun 2021 00:39:29 GMT  
		Size: 16.0 MB (16033037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3025761fffcd095f302e914141cd91fdce2a0d7b76c4f13f96753ef8b9cc4151`  
		Last Modified: Fri, 18 Jun 2021 00:40:26 GMT  
		Size: 193.7 MB (193651024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fa731efc631621d3f50f90fbbcb2b097a684e8d8cb0315be61e939425e2c89`  
		Last Modified: Tue, 22 Jun 2021 23:19:37 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838b070fdc3792c062bb5b6c96d57e95aa826e3f672720a26fe4ce42e09f62a6`  
		Last Modified: Fri, 02 Jul 2021 20:35:19 GMT  
		Size: 12.4 MB (12449570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b092812f8972255279e884ddd841c549e700a49cbf30502b609090da11a8366`  
		Last Modified: Fri, 02 Jul 2021 20:35:17 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e0c6fa70e8651d71566b155d1603cdada3e0ef5e24989a737ff1331e504248`  
		Last Modified: Fri, 02 Jul 2021 21:29:22 GMT  
		Size: 167.7 MB (167687703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9681302d705266a8fda7b06cbedec7e60d3cbe8d3a7cd396de641c01629e1f2`  
		Last Modified: Fri, 02 Jul 2021 21:29:16 GMT  
		Size: 304.3 MB (304262474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:febdbb1e1ba93a3409f287bcf8b6971cdf6b5bd7192b5905ab0d7af2b96ead9a`  
		Last Modified: Fri, 02 Jul 2021 21:28:55 GMT  
		Size: 2.3 MB (2257829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca2789ef5e5b874e548c7a49a34f758e42756de18eac72edeff0189ab67149f5`  
		Last Modified: Fri, 02 Jul 2021 21:28:54 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe89a44c02a00b967200a2582dfd5ddf10e55eaab30ce22d4e2bb8005c1ebdb2`  
		Last Modified: Fri, 02 Jul 2021 21:28:54 GMT  
		Size: 2.3 KB (2320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf13ef31df43a7fad037054463d308cac6589cf505de9902895ae97a7f94eca`  
		Last Modified: Fri, 02 Jul 2021 21:28:54 GMT  
		Size: 5.2 KB (5176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cce921ec85eee9de8e6ba6260d7d1d4983b70de2f8f1cf11217f5d209d3da50`  
		Last Modified: Fri, 02 Jul 2021 21:28:54 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13.5.0-postgres-tomcat`

```console
$ docker pull xwiki@sha256:373a16b9f83d74cf54fd8d02441d4da3edb024b7661d91cd49bcfc6a14bb1d70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:13.5.0-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:f17c5ea6ceb05de50779f4f500d499c28d8a59cc6fefb33bef030e86d763e3c8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **724.2 MB (724244461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bfac1762ee5527ba0f46f2bc750dd1a00ce4874164963fabb2317767a6920f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:28:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 18 Jun 2021 00:29:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:29:44 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Fri, 18 Jun 2021 00:29:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 18 Jun 2021 00:29:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Jun 2021 00:29:55 GMT
CMD ["jshell"]
# Tue, 22 Jun 2021 22:44:10 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 22 Jun 2021 22:44:11 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 22 Jun 2021 22:44:12 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 22 Jun 2021 22:44:12 GMT
WORKDIR /usr/local/tomcat
# Tue, 22 Jun 2021 22:44:12 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 22:44:12 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 23:10:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 22 Jun 2021 23:10:49 GMT
ENV TOMCAT_MAJOR=8
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_VERSION=8.5.68
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_SHA512=673f8d295d6f6b8e53b30c9c81989a3586341f9660f00e61a131153f54f0ce9d41bf8f49960ef477d3ec81610e1c75c1684c8676e9ebe5015486334c443d82e5
# Fri, 02 Jul 2021 20:10:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 02 Jul 2021 20:10:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 02 Jul 2021 20:10:28 GMT
EXPOSE 8080
# Fri, 02 Jul 2021 20:10:29 GMT
CMD ["catalina.sh" "run"]
# Fri, 02 Jul 2021 21:20:19 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Fri, 02 Jul 2021 21:24:00 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 02 Jul 2021 21:24:01 GMT
ENV XWIKI_VERSION=13.5
# Fri, 02 Jul 2021 21:24:02 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.5
# Fri, 02 Jul 2021 21:24:02 GMT
ENV XWIKI_DOWNLOAD_SHA256=3294abb19636ab2e51930f88fa9a449dd98f1aa5b2ca8d6b1a32a5ff4dd22889
# Fri, 02 Jul 2021 21:24:41 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 02 Jul 2021 21:24:43 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 02 Jul 2021 21:24:43 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 02 Jul 2021 21:24:43 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 02 Jul 2021 21:24:44 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 02 Jul 2021 21:24:44 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 02 Jul 2021 21:24:45 GMT
VOLUME [/usr/local/xwiki]
# Fri, 02 Jul 2021 21:24:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Jul 2021 21:24:45 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7766c75e8fade5c21578ec8566d2929e7238f9ac1dbe88551bf2f147b76c65`  
		Last Modified: Fri, 18 Jun 2021 00:39:29 GMT  
		Size: 16.0 MB (16033037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3025761fffcd095f302e914141cd91fdce2a0d7b76c4f13f96753ef8b9cc4151`  
		Last Modified: Fri, 18 Jun 2021 00:40:26 GMT  
		Size: 193.7 MB (193651024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fa731efc631621d3f50f90fbbcb2b097a684e8d8cb0315be61e939425e2c89`  
		Last Modified: Tue, 22 Jun 2021 23:19:37 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838b070fdc3792c062bb5b6c96d57e95aa826e3f672720a26fe4ce42e09f62a6`  
		Last Modified: Fri, 02 Jul 2021 20:35:19 GMT  
		Size: 12.4 MB (12449570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b092812f8972255279e884ddd841c549e700a49cbf30502b609090da11a8366`  
		Last Modified: Fri, 02 Jul 2021 20:35:17 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632cb72d9488b73892dc69501fcea55c5c81f21d67fb024c3d81a13dd8e181f2`  
		Last Modified: Fri, 02 Jul 2021 21:30:30 GMT  
		Size: 168.5 MB (168487456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:767ddc1d5cc9d5ea1633a6812c6ad9d5f34045978d5451c81891ce6f3d12c337`  
		Last Modified: Fri, 02 Jul 2021 21:30:23 GMT  
		Size: 304.3 MB (304262477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b361707c0e73c7c324926a78689157d0b6e250f7501eccc39fd5dd4c44fa403c`  
		Last Modified: Fri, 02 Jul 2021 21:30:03 GMT  
		Size: 795.4 KB (795417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ebb2929fba6c692b148e1983d179a4b6aaa3474acadd557b98b46b3407cc31`  
		Last Modified: Fri, 02 Jul 2021 21:30:02 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31106cd81f9c71416e86249b91978b7bf077a7322566b0ce8cff5777639c6358`  
		Last Modified: Fri, 02 Jul 2021 21:30:02 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba012baa8e78ea94911aa405fbe7309d2afd806ee6809951d80b27fd08634b48`  
		Last Modified: Fri, 02 Jul 2021 21:30:03 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f5f84a4d0710d3a48a6098de893e454ea3d1c673040570260ed3b86f264e372`  
		Last Modified: Fri, 02 Jul 2021 21:30:02 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:13.5.0-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:52f4e634a6f13313406cc5cf0c1a342b4a80b74137ec9db23cbb46238c15c6cb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **715.6 MB (715603005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:905b3bf926ec7e0141e17ed2b04a0fc56d67a05567245b5c4afa09ec343d90b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 17 Jun 2021 23:53:58 GMT
ADD file:9e94a579f0495fce8fac6889d0b9b2cd576d5b3ce9f18ff913ad99a503756769 in / 
# Thu, 17 Jun 2021 23:53:59 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:31:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 18 Jun 2021 00:31:32 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:31:58 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Fri, 18 Jun 2021 00:32:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 18 Jun 2021 00:32:10 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Jun 2021 00:32:10 GMT
CMD ["jshell"]
# Tue, 22 Jun 2021 23:25:06 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 22 Jun 2021 23:25:06 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 22 Jun 2021 23:25:07 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 22 Jun 2021 23:25:07 GMT
WORKDIR /usr/local/tomcat
# Tue, 22 Jun 2021 23:25:07 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 23:25:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 23:30:28 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 22 Jun 2021 23:30:29 GMT
ENV TOMCAT_MAJOR=8
# Tue, 22 Jun 2021 23:30:29 GMT
ENV TOMCAT_VERSION=8.5.68
# Tue, 22 Jun 2021 23:30:29 GMT
ENV TOMCAT_SHA512=673f8d295d6f6b8e53b30c9c81989a3586341f9660f00e61a131153f54f0ce9d41bf8f49960ef477d3ec81610e1c75c1684c8676e9ebe5015486334c443d82e5
# Fri, 02 Jul 2021 20:14:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 02 Jul 2021 20:14:25 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 02 Jul 2021 20:14:26 GMT
EXPOSE 8080
# Fri, 02 Jul 2021 20:14:26 GMT
CMD ["catalina.sh" "run"]
# Fri, 02 Jul 2021 22:10:38 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Fri, 02 Jul 2021 22:11:13 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 02 Jul 2021 22:11:14 GMT
ENV XWIKI_VERSION=13.5
# Fri, 02 Jul 2021 22:11:14 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.5
# Fri, 02 Jul 2021 22:11:14 GMT
ENV XWIKI_DOWNLOAD_SHA256=3294abb19636ab2e51930f88fa9a449dd98f1aa5b2ca8d6b1a32a5ff4dd22889
# Fri, 02 Jul 2021 22:11:53 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 02 Jul 2021 22:11:54 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 02 Jul 2021 22:11:55 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 02 Jul 2021 22:11:55 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 02 Jul 2021 22:11:56 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 02 Jul 2021 22:11:56 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 02 Jul 2021 22:11:56 GMT
VOLUME [/usr/local/xwiki]
# Fri, 02 Jul 2021 22:11:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Jul 2021 22:11:56 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:6f86eded34a1950318569803a7e0c689175ebd9d76faf08798f88ac133b98a11`  
		Last Modified: Thu, 17 Jun 2021 23:56:04 GMT  
		Size: 27.2 MB (27158803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff470c6007f78550376884f4972cc5c767c6adc6f7d6002adddbddfb4600ea4b`  
		Last Modified: Fri, 18 Jun 2021 00:35:11 GMT  
		Size: 15.9 MB (15894169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a125d809875539cb0e1d2b0483b6223a65a2867db6c0df786d36feb6fa9bf260`  
		Last Modified: Fri, 18 Jun 2021 00:36:10 GMT  
		Size: 190.4 MB (190379258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599d9b9dba394414fe824f147f376772ae86db1750dd0c0865717476c25cd040`  
		Last Modified: Tue, 22 Jun 2021 23:41:56 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdf80a91fe0ee7a8d615c877013dd3f0f57f510581a488bb24e1d945dd212f30`  
		Last Modified: Fri, 02 Jul 2021 20:43:37 GMT  
		Size: 12.4 MB (12448780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f63370a9da1ce6088a59891070b42f6fe7d136d05c91aeb21d50398be035dbe`  
		Last Modified: Fri, 02 Jul 2021 20:43:34 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daed3696500a526a0b524e45ca20d612b3afdfbdf4e3b965b2384c9359de9952`  
		Last Modified: Fri, 02 Jul 2021 22:14:47 GMT  
		Size: 164.7 MB (164652294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a220e402041502b22a6098d44ced1d4099eae462963ccb07ab34997ae5350a4f`  
		Last Modified: Fri, 02 Jul 2021 22:14:43 GMT  
		Size: 304.3 MB (304262497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbe6d99c11bcf58c14ff7bd941299f80845365b2889062754658a6c30cbd8753`  
		Last Modified: Fri, 02 Jul 2021 22:14:20 GMT  
		Size: 795.4 KB (795415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6332f69ccc13af037975d4d700ab40f7a705e023f2574050671862a4151bbf9a`  
		Last Modified: Fri, 02 Jul 2021 22:14:19 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643f173e80f63080795f37afcb10709e14e4cfd799ae3b2fecccd4f205c05ed6`  
		Last Modified: Fri, 02 Jul 2021 22:14:19 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b91509711133471fa08ab523dab7699c2455003c7c247042893074f443700b`  
		Last Modified: Fri, 02 Jul 2021 22:14:20 GMT  
		Size: 5.2 KB (5173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca603534af32c6957d57352e18622eab0f5a32b16b1dc811586d6315f649725`  
		Last Modified: Fri, 02 Jul 2021 22:14:19 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:latest`

```console
$ docker pull xwiki@sha256:4eb72b2458ef8747b19e51ad101bf1e0a7b6959db0434d39f4b1abea7229002a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `xwiki:latest` - linux; amd64

```console
$ docker pull xwiki@sha256:107067a099d5528b862d89ac83906bfadc1050c5afdb4df595d97c10276ca0b7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **724.9 MB (724906978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65c402c5f0d76e8b941063942552357d8aa1bd590d0a2ef6251038d241b52e2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:28:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 18 Jun 2021 00:29:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:29:44 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Fri, 18 Jun 2021 00:29:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 18 Jun 2021 00:29:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Jun 2021 00:29:55 GMT
CMD ["jshell"]
# Tue, 22 Jun 2021 22:44:10 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 22 Jun 2021 22:44:11 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 22 Jun 2021 22:44:12 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 22 Jun 2021 22:44:12 GMT
WORKDIR /usr/local/tomcat
# Tue, 22 Jun 2021 22:44:12 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 22:44:12 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 23:10:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 22 Jun 2021 23:10:49 GMT
ENV TOMCAT_MAJOR=8
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_VERSION=8.5.68
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_SHA512=673f8d295d6f6b8e53b30c9c81989a3586341f9660f00e61a131153f54f0ce9d41bf8f49960ef477d3ec81610e1c75c1684c8676e9ebe5015486334c443d82e5
# Fri, 02 Jul 2021 20:10:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 02 Jul 2021 20:10:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 02 Jul 2021 20:10:28 GMT
EXPOSE 8080
# Fri, 02 Jul 2021 20:10:29 GMT
CMD ["catalina.sh" "run"]
# Fri, 02 Jul 2021 21:20:19 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Fri, 02 Jul 2021 21:22:31 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 02 Jul 2021 21:22:32 GMT
ENV XWIKI_VERSION=13.5
# Fri, 02 Jul 2021 21:22:33 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.5
# Fri, 02 Jul 2021 21:22:33 GMT
ENV XWIKI_DOWNLOAD_SHA256=3294abb19636ab2e51930f88fa9a449dd98f1aa5b2ca8d6b1a32a5ff4dd22889
# Fri, 02 Jul 2021 21:23:12 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 02 Jul 2021 21:23:13 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Fri, 02 Jul 2021 21:23:13 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Fri, 02 Jul 2021 21:23:13 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Fri, 02 Jul 2021 21:23:13 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Fri, 02 Jul 2021 21:23:14 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Fri, 02 Jul 2021 21:23:15 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 02 Jul 2021 21:23:15 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 02 Jul 2021 21:23:15 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 02 Jul 2021 21:23:16 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 02 Jul 2021 21:23:17 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 02 Jul 2021 21:23:17 GMT
VOLUME [/usr/local/xwiki]
# Fri, 02 Jul 2021 21:23:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Jul 2021 21:23:17 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7766c75e8fade5c21578ec8566d2929e7238f9ac1dbe88551bf2f147b76c65`  
		Last Modified: Fri, 18 Jun 2021 00:39:29 GMT  
		Size: 16.0 MB (16033037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3025761fffcd095f302e914141cd91fdce2a0d7b76c4f13f96753ef8b9cc4151`  
		Last Modified: Fri, 18 Jun 2021 00:40:26 GMT  
		Size: 193.7 MB (193651024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fa731efc631621d3f50f90fbbcb2b097a684e8d8cb0315be61e939425e2c89`  
		Last Modified: Tue, 22 Jun 2021 23:19:37 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838b070fdc3792c062bb5b6c96d57e95aa826e3f672720a26fe4ce42e09f62a6`  
		Last Modified: Fri, 02 Jul 2021 20:35:19 GMT  
		Size: 12.4 MB (12449570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b092812f8972255279e884ddd841c549e700a49cbf30502b609090da11a8366`  
		Last Modified: Fri, 02 Jul 2021 20:35:17 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e0c6fa70e8651d71566b155d1603cdada3e0ef5e24989a737ff1331e504248`  
		Last Modified: Fri, 02 Jul 2021 21:29:22 GMT  
		Size: 167.7 MB (167687703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9681302d705266a8fda7b06cbedec7e60d3cbe8d3a7cd396de641c01629e1f2`  
		Last Modified: Fri, 02 Jul 2021 21:29:16 GMT  
		Size: 304.3 MB (304262474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:febdbb1e1ba93a3409f287bcf8b6971cdf6b5bd7192b5905ab0d7af2b96ead9a`  
		Last Modified: Fri, 02 Jul 2021 21:28:55 GMT  
		Size: 2.3 MB (2257829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca2789ef5e5b874e548c7a49a34f758e42756de18eac72edeff0189ab67149f5`  
		Last Modified: Fri, 02 Jul 2021 21:28:54 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe89a44c02a00b967200a2582dfd5ddf10e55eaab30ce22d4e2bb8005c1ebdb2`  
		Last Modified: Fri, 02 Jul 2021 21:28:54 GMT  
		Size: 2.3 KB (2320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf13ef31df43a7fad037054463d308cac6589cf505de9902895ae97a7f94eca`  
		Last Modified: Fri, 02 Jul 2021 21:28:54 GMT  
		Size: 5.2 KB (5176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cce921ec85eee9de8e6ba6260d7d1d4983b70de2f8f1cf11217f5d209d3da50`  
		Last Modified: Fri, 02 Jul 2021 21:28:54 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:lts`

```console
$ docker pull xwiki@sha256:1e197bef02015dace9ca4075b7a489059028049229bb8149ddca1b4406ef6262
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `xwiki:lts` - linux; amd64

```console
$ docker pull xwiki@sha256:7936f677de247db3696317f0abf61992a7b1fda926c034feff859dc1bedf33a0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **718.3 MB (718287590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be287ce42e05979127e95d83cdfa051698ff58dcc7eee07d251c2c10c73f25de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:28:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 18 Jun 2021 00:29:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:29:44 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Fri, 18 Jun 2021 00:29:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 18 Jun 2021 00:29:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Jun 2021 00:29:55 GMT
CMD ["jshell"]
# Tue, 22 Jun 2021 22:44:10 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 22 Jun 2021 22:44:11 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 22 Jun 2021 22:44:12 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 22 Jun 2021 22:44:12 GMT
WORKDIR /usr/local/tomcat
# Tue, 22 Jun 2021 22:44:12 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 22:44:12 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 23:10:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 22 Jun 2021 23:10:49 GMT
ENV TOMCAT_MAJOR=8
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_VERSION=8.5.68
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_SHA512=673f8d295d6f6b8e53b30c9c81989a3586341f9660f00e61a131153f54f0ce9d41bf8f49960ef477d3ec81610e1c75c1684c8676e9ebe5015486334c443d82e5
# Fri, 02 Jul 2021 20:10:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 02 Jul 2021 20:10:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 02 Jul 2021 20:10:28 GMT
EXPOSE 8080
# Fri, 02 Jul 2021 20:10:29 GMT
CMD ["catalina.sh" "run"]
# Fri, 02 Jul 2021 21:20:19 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Fri, 02 Jul 2021 21:22:31 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 02 Jul 2021 21:24:55 GMT
ENV XWIKI_VERSION=12.10.8
# Fri, 02 Jul 2021 21:24:55 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.8
# Fri, 02 Jul 2021 21:24:56 GMT
ENV XWIKI_DOWNLOAD_SHA256=739471e78f8b2550849d1a869c27313c4c71b12bb9b6c9c26f77c81a993dff2e
# Fri, 02 Jul 2021 21:25:34 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 02 Jul 2021 21:25:35 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Fri, 02 Jul 2021 21:25:36 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Fri, 02 Jul 2021 21:25:36 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Fri, 02 Jul 2021 21:25:36 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Fri, 02 Jul 2021 21:25:36 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Fri, 02 Jul 2021 21:25:38 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 02 Jul 2021 21:25:38 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 02 Jul 2021 21:25:38 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 02 Jul 2021 21:25:39 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 02 Jul 2021 21:25:39 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 02 Jul 2021 21:25:40 GMT
VOLUME [/usr/local/xwiki]
# Fri, 02 Jul 2021 21:25:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Jul 2021 21:25:40 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7766c75e8fade5c21578ec8566d2929e7238f9ac1dbe88551bf2f147b76c65`  
		Last Modified: Fri, 18 Jun 2021 00:39:29 GMT  
		Size: 16.0 MB (16033037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3025761fffcd095f302e914141cd91fdce2a0d7b76c4f13f96753ef8b9cc4151`  
		Last Modified: Fri, 18 Jun 2021 00:40:26 GMT  
		Size: 193.7 MB (193651024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fa731efc631621d3f50f90fbbcb2b097a684e8d8cb0315be61e939425e2c89`  
		Last Modified: Tue, 22 Jun 2021 23:19:37 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838b070fdc3792c062bb5b6c96d57e95aa826e3f672720a26fe4ce42e09f62a6`  
		Last Modified: Fri, 02 Jul 2021 20:35:19 GMT  
		Size: 12.4 MB (12449570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b092812f8972255279e884ddd841c549e700a49cbf30502b609090da11a8366`  
		Last Modified: Fri, 02 Jul 2021 20:35:17 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e0c6fa70e8651d71566b155d1603cdada3e0ef5e24989a737ff1331e504248`  
		Last Modified: Fri, 02 Jul 2021 21:29:22 GMT  
		Size: 167.7 MB (167687703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33d752b3691d8364086e45b10dcc929096fe97831218327789b39c0af5be2e81`  
		Last Modified: Fri, 02 Jul 2021 21:31:14 GMT  
		Size: 297.6 MB (297643037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d959af1053745fc9b0c7ae7926ade05e2947dbb626102064ad082c1ac72a00`  
		Last Modified: Fri, 02 Jul 2021 21:30:55 GMT  
		Size: 2.3 MB (2257825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff5014a54fd4da4d0be9e135f6a07d40d5de45808375fe6a5b2a8a92ea8e8115`  
		Last Modified: Fri, 02 Jul 2021 21:30:55 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3370fff0d5efea5884d25b00529d409ae92a9b41417f26fdb3fd64cf7b91fcdf`  
		Last Modified: Fri, 02 Jul 2021 21:30:55 GMT  
		Size: 2.3 KB (2317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85a15beb11b7db1ec710c7b1d91da098c06771ab705ca520461418b9391d9cb`  
		Last Modified: Fri, 02 Jul 2021 21:30:55 GMT  
		Size: 5.2 KB (5233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:152cfc2ed6695c687023da931551401c2a615598639526788449524fce177722`  
		Last Modified: Fri, 02 Jul 2021 21:30:55 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:lts-mysql`

```console
$ docker pull xwiki@sha256:1e197bef02015dace9ca4075b7a489059028049229bb8149ddca1b4406ef6262
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `xwiki:lts-mysql` - linux; amd64

```console
$ docker pull xwiki@sha256:7936f677de247db3696317f0abf61992a7b1fda926c034feff859dc1bedf33a0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **718.3 MB (718287590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be287ce42e05979127e95d83cdfa051698ff58dcc7eee07d251c2c10c73f25de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:28:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 18 Jun 2021 00:29:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:29:44 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Fri, 18 Jun 2021 00:29:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 18 Jun 2021 00:29:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Jun 2021 00:29:55 GMT
CMD ["jshell"]
# Tue, 22 Jun 2021 22:44:10 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 22 Jun 2021 22:44:11 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 22 Jun 2021 22:44:12 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 22 Jun 2021 22:44:12 GMT
WORKDIR /usr/local/tomcat
# Tue, 22 Jun 2021 22:44:12 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 22:44:12 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 23:10:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 22 Jun 2021 23:10:49 GMT
ENV TOMCAT_MAJOR=8
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_VERSION=8.5.68
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_SHA512=673f8d295d6f6b8e53b30c9c81989a3586341f9660f00e61a131153f54f0ce9d41bf8f49960ef477d3ec81610e1c75c1684c8676e9ebe5015486334c443d82e5
# Fri, 02 Jul 2021 20:10:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 02 Jul 2021 20:10:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 02 Jul 2021 20:10:28 GMT
EXPOSE 8080
# Fri, 02 Jul 2021 20:10:29 GMT
CMD ["catalina.sh" "run"]
# Fri, 02 Jul 2021 21:20:19 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Fri, 02 Jul 2021 21:22:31 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 02 Jul 2021 21:24:55 GMT
ENV XWIKI_VERSION=12.10.8
# Fri, 02 Jul 2021 21:24:55 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.8
# Fri, 02 Jul 2021 21:24:56 GMT
ENV XWIKI_DOWNLOAD_SHA256=739471e78f8b2550849d1a869c27313c4c71b12bb9b6c9c26f77c81a993dff2e
# Fri, 02 Jul 2021 21:25:34 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 02 Jul 2021 21:25:35 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Fri, 02 Jul 2021 21:25:36 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Fri, 02 Jul 2021 21:25:36 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Fri, 02 Jul 2021 21:25:36 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Fri, 02 Jul 2021 21:25:36 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Fri, 02 Jul 2021 21:25:38 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 02 Jul 2021 21:25:38 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 02 Jul 2021 21:25:38 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 02 Jul 2021 21:25:39 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 02 Jul 2021 21:25:39 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 02 Jul 2021 21:25:40 GMT
VOLUME [/usr/local/xwiki]
# Fri, 02 Jul 2021 21:25:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Jul 2021 21:25:40 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7766c75e8fade5c21578ec8566d2929e7238f9ac1dbe88551bf2f147b76c65`  
		Last Modified: Fri, 18 Jun 2021 00:39:29 GMT  
		Size: 16.0 MB (16033037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3025761fffcd095f302e914141cd91fdce2a0d7b76c4f13f96753ef8b9cc4151`  
		Last Modified: Fri, 18 Jun 2021 00:40:26 GMT  
		Size: 193.7 MB (193651024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fa731efc631621d3f50f90fbbcb2b097a684e8d8cb0315be61e939425e2c89`  
		Last Modified: Tue, 22 Jun 2021 23:19:37 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838b070fdc3792c062bb5b6c96d57e95aa826e3f672720a26fe4ce42e09f62a6`  
		Last Modified: Fri, 02 Jul 2021 20:35:19 GMT  
		Size: 12.4 MB (12449570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b092812f8972255279e884ddd841c549e700a49cbf30502b609090da11a8366`  
		Last Modified: Fri, 02 Jul 2021 20:35:17 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e0c6fa70e8651d71566b155d1603cdada3e0ef5e24989a737ff1331e504248`  
		Last Modified: Fri, 02 Jul 2021 21:29:22 GMT  
		Size: 167.7 MB (167687703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33d752b3691d8364086e45b10dcc929096fe97831218327789b39c0af5be2e81`  
		Last Modified: Fri, 02 Jul 2021 21:31:14 GMT  
		Size: 297.6 MB (297643037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d959af1053745fc9b0c7ae7926ade05e2947dbb626102064ad082c1ac72a00`  
		Last Modified: Fri, 02 Jul 2021 21:30:55 GMT  
		Size: 2.3 MB (2257825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff5014a54fd4da4d0be9e135f6a07d40d5de45808375fe6a5b2a8a92ea8e8115`  
		Last Modified: Fri, 02 Jul 2021 21:30:55 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3370fff0d5efea5884d25b00529d409ae92a9b41417f26fdb3fd64cf7b91fcdf`  
		Last Modified: Fri, 02 Jul 2021 21:30:55 GMT  
		Size: 2.3 KB (2317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85a15beb11b7db1ec710c7b1d91da098c06771ab705ca520461418b9391d9cb`  
		Last Modified: Fri, 02 Jul 2021 21:30:55 GMT  
		Size: 5.2 KB (5233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:152cfc2ed6695c687023da931551401c2a615598639526788449524fce177722`  
		Last Modified: Fri, 02 Jul 2021 21:30:55 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:lts-mysql-tomcat`

```console
$ docker pull xwiki@sha256:1e197bef02015dace9ca4075b7a489059028049229bb8149ddca1b4406ef6262
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `xwiki:lts-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:7936f677de247db3696317f0abf61992a7b1fda926c034feff859dc1bedf33a0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **718.3 MB (718287590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be287ce42e05979127e95d83cdfa051698ff58dcc7eee07d251c2c10c73f25de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:28:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 18 Jun 2021 00:29:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:29:44 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Fri, 18 Jun 2021 00:29:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 18 Jun 2021 00:29:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Jun 2021 00:29:55 GMT
CMD ["jshell"]
# Tue, 22 Jun 2021 22:44:10 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 22 Jun 2021 22:44:11 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 22 Jun 2021 22:44:12 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 22 Jun 2021 22:44:12 GMT
WORKDIR /usr/local/tomcat
# Tue, 22 Jun 2021 22:44:12 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 22:44:12 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 23:10:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 22 Jun 2021 23:10:49 GMT
ENV TOMCAT_MAJOR=8
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_VERSION=8.5.68
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_SHA512=673f8d295d6f6b8e53b30c9c81989a3586341f9660f00e61a131153f54f0ce9d41bf8f49960ef477d3ec81610e1c75c1684c8676e9ebe5015486334c443d82e5
# Fri, 02 Jul 2021 20:10:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 02 Jul 2021 20:10:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 02 Jul 2021 20:10:28 GMT
EXPOSE 8080
# Fri, 02 Jul 2021 20:10:29 GMT
CMD ["catalina.sh" "run"]
# Fri, 02 Jul 2021 21:20:19 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Fri, 02 Jul 2021 21:22:31 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 02 Jul 2021 21:24:55 GMT
ENV XWIKI_VERSION=12.10.8
# Fri, 02 Jul 2021 21:24:55 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.8
# Fri, 02 Jul 2021 21:24:56 GMT
ENV XWIKI_DOWNLOAD_SHA256=739471e78f8b2550849d1a869c27313c4c71b12bb9b6c9c26f77c81a993dff2e
# Fri, 02 Jul 2021 21:25:34 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 02 Jul 2021 21:25:35 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Fri, 02 Jul 2021 21:25:36 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Fri, 02 Jul 2021 21:25:36 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Fri, 02 Jul 2021 21:25:36 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Fri, 02 Jul 2021 21:25:36 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Fri, 02 Jul 2021 21:25:38 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 02 Jul 2021 21:25:38 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 02 Jul 2021 21:25:38 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 02 Jul 2021 21:25:39 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 02 Jul 2021 21:25:39 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 02 Jul 2021 21:25:40 GMT
VOLUME [/usr/local/xwiki]
# Fri, 02 Jul 2021 21:25:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Jul 2021 21:25:40 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7766c75e8fade5c21578ec8566d2929e7238f9ac1dbe88551bf2f147b76c65`  
		Last Modified: Fri, 18 Jun 2021 00:39:29 GMT  
		Size: 16.0 MB (16033037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3025761fffcd095f302e914141cd91fdce2a0d7b76c4f13f96753ef8b9cc4151`  
		Last Modified: Fri, 18 Jun 2021 00:40:26 GMT  
		Size: 193.7 MB (193651024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fa731efc631621d3f50f90fbbcb2b097a684e8d8cb0315be61e939425e2c89`  
		Last Modified: Tue, 22 Jun 2021 23:19:37 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838b070fdc3792c062bb5b6c96d57e95aa826e3f672720a26fe4ce42e09f62a6`  
		Last Modified: Fri, 02 Jul 2021 20:35:19 GMT  
		Size: 12.4 MB (12449570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b092812f8972255279e884ddd841c549e700a49cbf30502b609090da11a8366`  
		Last Modified: Fri, 02 Jul 2021 20:35:17 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e0c6fa70e8651d71566b155d1603cdada3e0ef5e24989a737ff1331e504248`  
		Last Modified: Fri, 02 Jul 2021 21:29:22 GMT  
		Size: 167.7 MB (167687703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33d752b3691d8364086e45b10dcc929096fe97831218327789b39c0af5be2e81`  
		Last Modified: Fri, 02 Jul 2021 21:31:14 GMT  
		Size: 297.6 MB (297643037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d959af1053745fc9b0c7ae7926ade05e2947dbb626102064ad082c1ac72a00`  
		Last Modified: Fri, 02 Jul 2021 21:30:55 GMT  
		Size: 2.3 MB (2257825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff5014a54fd4da4d0be9e135f6a07d40d5de45808375fe6a5b2a8a92ea8e8115`  
		Last Modified: Fri, 02 Jul 2021 21:30:55 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3370fff0d5efea5884d25b00529d409ae92a9b41417f26fdb3fd64cf7b91fcdf`  
		Last Modified: Fri, 02 Jul 2021 21:30:55 GMT  
		Size: 2.3 KB (2317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85a15beb11b7db1ec710c7b1d91da098c06771ab705ca520461418b9391d9cb`  
		Last Modified: Fri, 02 Jul 2021 21:30:55 GMT  
		Size: 5.2 KB (5233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:152cfc2ed6695c687023da931551401c2a615598639526788449524fce177722`  
		Last Modified: Fri, 02 Jul 2021 21:30:55 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:lts-postgres`

```console
$ docker pull xwiki@sha256:d4ad52384a2f234abfaa1a4fcf325fcec293c3d503304b17b635c2c39dda9bb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:lts-postgres` - linux; amd64

```console
$ docker pull xwiki@sha256:dcddc6098a29ac5c80cf67b5dc8c672016c3d7dcb5aa5cb67cc1a9c8650202ba
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **717.6 MB (717625228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ad1634308c9f2ace73759c7eee6fdf3d6598f9918206d93a361aa793c8c1879`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:28:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 18 Jun 2021 00:29:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:29:44 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Fri, 18 Jun 2021 00:29:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 18 Jun 2021 00:29:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Jun 2021 00:29:55 GMT
CMD ["jshell"]
# Tue, 22 Jun 2021 22:44:10 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 22 Jun 2021 22:44:11 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 22 Jun 2021 22:44:12 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 22 Jun 2021 22:44:12 GMT
WORKDIR /usr/local/tomcat
# Tue, 22 Jun 2021 22:44:12 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 22:44:12 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 23:10:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 22 Jun 2021 23:10:49 GMT
ENV TOMCAT_MAJOR=8
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_VERSION=8.5.68
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_SHA512=673f8d295d6f6b8e53b30c9c81989a3586341f9660f00e61a131153f54f0ce9d41bf8f49960ef477d3ec81610e1c75c1684c8676e9ebe5015486334c443d82e5
# Fri, 02 Jul 2021 20:10:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 02 Jul 2021 20:10:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 02 Jul 2021 20:10:28 GMT
EXPOSE 8080
# Fri, 02 Jul 2021 20:10:29 GMT
CMD ["catalina.sh" "run"]
# Fri, 02 Jul 2021 21:20:19 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Fri, 02 Jul 2021 21:24:00 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 02 Jul 2021 21:25:46 GMT
ENV XWIKI_VERSION=12.10.8
# Fri, 02 Jul 2021 21:25:46 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.8
# Fri, 02 Jul 2021 21:25:46 GMT
ENV XWIKI_DOWNLOAD_SHA256=739471e78f8b2550849d1a869c27313c4c71b12bb9b6c9c26f77c81a993dff2e
# Fri, 02 Jul 2021 21:26:24 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 02 Jul 2021 21:26:26 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 02 Jul 2021 21:26:26 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 02 Jul 2021 21:26:26 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 02 Jul 2021 21:26:27 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 02 Jul 2021 21:26:28 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 02 Jul 2021 21:26:28 GMT
VOLUME [/usr/local/xwiki]
# Fri, 02 Jul 2021 21:26:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Jul 2021 21:26:28 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7766c75e8fade5c21578ec8566d2929e7238f9ac1dbe88551bf2f147b76c65`  
		Last Modified: Fri, 18 Jun 2021 00:39:29 GMT  
		Size: 16.0 MB (16033037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3025761fffcd095f302e914141cd91fdce2a0d7b76c4f13f96753ef8b9cc4151`  
		Last Modified: Fri, 18 Jun 2021 00:40:26 GMT  
		Size: 193.7 MB (193651024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fa731efc631621d3f50f90fbbcb2b097a684e8d8cb0315be61e939425e2c89`  
		Last Modified: Tue, 22 Jun 2021 23:19:37 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838b070fdc3792c062bb5b6c96d57e95aa826e3f672720a26fe4ce42e09f62a6`  
		Last Modified: Fri, 02 Jul 2021 20:35:19 GMT  
		Size: 12.4 MB (12449570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b092812f8972255279e884ddd841c549e700a49cbf30502b609090da11a8366`  
		Last Modified: Fri, 02 Jul 2021 20:35:17 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632cb72d9488b73892dc69501fcea55c5c81f21d67fb024c3d81a13dd8e181f2`  
		Last Modified: Fri, 02 Jul 2021 21:30:30 GMT  
		Size: 168.5 MB (168487456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa26e65e7bdcfa431b794bb86fb835d0ba92125cc1f674909deb60817b0ffc7`  
		Last Modified: Fri, 02 Jul 2021 21:32:08 GMT  
		Size: 297.6 MB (297643176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:778bdda6cf557625368df98f86b4555d4484fa3578482c0f622ba8d20ce3334f`  
		Last Modified: Fri, 02 Jul 2021 21:31:48 GMT  
		Size: 795.4 KB (795418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f1b4a5284c1fb17dc78353b7d19eca4c02c7f51faf45f50b6fe6a3e44f17f88`  
		Last Modified: Fri, 02 Jul 2021 21:31:47 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f7600885f2faa71d2a0ce2f1b6baeabed4422fba71f131890e69726d9cfce9`  
		Last Modified: Fri, 02 Jul 2021 21:31:47 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e682ee044d627db17e38f2f2ff093a8cea613bd97d7109a738de6426281da84a`  
		Last Modified: Fri, 02 Jul 2021 21:31:47 GMT  
		Size: 5.2 KB (5235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ea14025ccd7f5ae72333faa029b366380ce839017cdb4025860c68672b8b96`  
		Last Modified: Fri, 02 Jul 2021 21:31:47 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:lts-postgres` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:0ddf979c392d089c97254e695ee7ee8858c7226de04fa721a5058bd40bd0ea7f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **709.0 MB (708983644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea2131062ee3bd998cc1ad9d0c7efa828713dee230fab020f49d5e46a40cfe0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 17 Jun 2021 23:53:58 GMT
ADD file:9e94a579f0495fce8fac6889d0b9b2cd576d5b3ce9f18ff913ad99a503756769 in / 
# Thu, 17 Jun 2021 23:53:59 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:31:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 18 Jun 2021 00:31:32 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:31:58 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Fri, 18 Jun 2021 00:32:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 18 Jun 2021 00:32:10 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Jun 2021 00:32:10 GMT
CMD ["jshell"]
# Tue, 22 Jun 2021 23:25:06 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 22 Jun 2021 23:25:06 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 22 Jun 2021 23:25:07 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 22 Jun 2021 23:25:07 GMT
WORKDIR /usr/local/tomcat
# Tue, 22 Jun 2021 23:25:07 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 23:25:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 23:30:28 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 22 Jun 2021 23:30:29 GMT
ENV TOMCAT_MAJOR=8
# Tue, 22 Jun 2021 23:30:29 GMT
ENV TOMCAT_VERSION=8.5.68
# Tue, 22 Jun 2021 23:30:29 GMT
ENV TOMCAT_SHA512=673f8d295d6f6b8e53b30c9c81989a3586341f9660f00e61a131153f54f0ce9d41bf8f49960ef477d3ec81610e1c75c1684c8676e9ebe5015486334c443d82e5
# Fri, 02 Jul 2021 20:14:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 02 Jul 2021 20:14:25 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 02 Jul 2021 20:14:26 GMT
EXPOSE 8080
# Fri, 02 Jul 2021 20:14:26 GMT
CMD ["catalina.sh" "run"]
# Fri, 02 Jul 2021 22:10:38 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Fri, 02 Jul 2021 22:11:13 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 02 Jul 2021 22:12:05 GMT
ENV XWIKI_VERSION=12.10.8
# Fri, 02 Jul 2021 22:12:05 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.8
# Fri, 02 Jul 2021 22:12:05 GMT
ENV XWIKI_DOWNLOAD_SHA256=739471e78f8b2550849d1a869c27313c4c71b12bb9b6c9c26f77c81a993dff2e
# Fri, 02 Jul 2021 22:12:42 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 02 Jul 2021 22:12:44 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 02 Jul 2021 22:12:44 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 02 Jul 2021 22:12:44 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 02 Jul 2021 22:12:45 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 02 Jul 2021 22:12:45 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 02 Jul 2021 22:12:46 GMT
VOLUME [/usr/local/xwiki]
# Fri, 02 Jul 2021 22:12:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Jul 2021 22:12:46 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:6f86eded34a1950318569803a7e0c689175ebd9d76faf08798f88ac133b98a11`  
		Last Modified: Thu, 17 Jun 2021 23:56:04 GMT  
		Size: 27.2 MB (27158803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff470c6007f78550376884f4972cc5c767c6adc6f7d6002adddbddfb4600ea4b`  
		Last Modified: Fri, 18 Jun 2021 00:35:11 GMT  
		Size: 15.9 MB (15894169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a125d809875539cb0e1d2b0483b6223a65a2867db6c0df786d36feb6fa9bf260`  
		Last Modified: Fri, 18 Jun 2021 00:36:10 GMT  
		Size: 190.4 MB (190379258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599d9b9dba394414fe824f147f376772ae86db1750dd0c0865717476c25cd040`  
		Last Modified: Tue, 22 Jun 2021 23:41:56 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdf80a91fe0ee7a8d615c877013dd3f0f57f510581a488bb24e1d945dd212f30`  
		Last Modified: Fri, 02 Jul 2021 20:43:37 GMT  
		Size: 12.4 MB (12448780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f63370a9da1ce6088a59891070b42f6fe7d136d05c91aeb21d50398be035dbe`  
		Last Modified: Fri, 02 Jul 2021 20:43:34 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daed3696500a526a0b524e45ca20d612b3afdfbdf4e3b965b2384c9359de9952`  
		Last Modified: Fri, 02 Jul 2021 22:14:47 GMT  
		Size: 164.7 MB (164652294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2bdca7c7fda93fd53c72d634b26796ed47fea3732fa34e654e80f24a29e45d`  
		Last Modified: Fri, 02 Jul 2021 22:15:40 GMT  
		Size: 297.6 MB (297643088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1973f14560a22aba4dcd67d7d766ce12b6412478de10ca1ede26d89eef4ce002`  
		Last Modified: Fri, 02 Jul 2021 22:15:17 GMT  
		Size: 795.4 KB (795416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28dc40d8ca6a5141c9bb915f8bc1e4f7f6c72d41b8f9a67c68e1d7aef8ed4ef3`  
		Last Modified: Fri, 02 Jul 2021 22:15:17 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d684d9972a40fa0638d09f2706b84bd0fb4f24abd756f55d946d7fb7aac6509d`  
		Last Modified: Fri, 02 Jul 2021 22:15:17 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3cfc79bfb8d63baad54ecca1877c3f744947d18ec52ee2d7fc6ff840340841d`  
		Last Modified: Fri, 02 Jul 2021 22:15:17 GMT  
		Size: 5.2 KB (5230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7936b27fcebcf1c11910fcd1c354d7fe295b8a31ab83f21dd105e77e7edb3f0a`  
		Last Modified: Fri, 02 Jul 2021 22:15:17 GMT  
		Size: 2.5 KB (2501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:lts-postgres-tomcat`

```console
$ docker pull xwiki@sha256:d4ad52384a2f234abfaa1a4fcf325fcec293c3d503304b17b635c2c39dda9bb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:lts-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:dcddc6098a29ac5c80cf67b5dc8c672016c3d7dcb5aa5cb67cc1a9c8650202ba
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **717.6 MB (717625228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ad1634308c9f2ace73759c7eee6fdf3d6598f9918206d93a361aa793c8c1879`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:28:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 18 Jun 2021 00:29:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:29:44 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Fri, 18 Jun 2021 00:29:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 18 Jun 2021 00:29:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Jun 2021 00:29:55 GMT
CMD ["jshell"]
# Tue, 22 Jun 2021 22:44:10 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 22 Jun 2021 22:44:11 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 22 Jun 2021 22:44:12 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 22 Jun 2021 22:44:12 GMT
WORKDIR /usr/local/tomcat
# Tue, 22 Jun 2021 22:44:12 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 22:44:12 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 23:10:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 22 Jun 2021 23:10:49 GMT
ENV TOMCAT_MAJOR=8
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_VERSION=8.5.68
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_SHA512=673f8d295d6f6b8e53b30c9c81989a3586341f9660f00e61a131153f54f0ce9d41bf8f49960ef477d3ec81610e1c75c1684c8676e9ebe5015486334c443d82e5
# Fri, 02 Jul 2021 20:10:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 02 Jul 2021 20:10:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 02 Jul 2021 20:10:28 GMT
EXPOSE 8080
# Fri, 02 Jul 2021 20:10:29 GMT
CMD ["catalina.sh" "run"]
# Fri, 02 Jul 2021 21:20:19 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Fri, 02 Jul 2021 21:24:00 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 02 Jul 2021 21:25:46 GMT
ENV XWIKI_VERSION=12.10.8
# Fri, 02 Jul 2021 21:25:46 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.8
# Fri, 02 Jul 2021 21:25:46 GMT
ENV XWIKI_DOWNLOAD_SHA256=739471e78f8b2550849d1a869c27313c4c71b12bb9b6c9c26f77c81a993dff2e
# Fri, 02 Jul 2021 21:26:24 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 02 Jul 2021 21:26:26 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 02 Jul 2021 21:26:26 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 02 Jul 2021 21:26:26 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 02 Jul 2021 21:26:27 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 02 Jul 2021 21:26:28 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 02 Jul 2021 21:26:28 GMT
VOLUME [/usr/local/xwiki]
# Fri, 02 Jul 2021 21:26:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Jul 2021 21:26:28 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7766c75e8fade5c21578ec8566d2929e7238f9ac1dbe88551bf2f147b76c65`  
		Last Modified: Fri, 18 Jun 2021 00:39:29 GMT  
		Size: 16.0 MB (16033037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3025761fffcd095f302e914141cd91fdce2a0d7b76c4f13f96753ef8b9cc4151`  
		Last Modified: Fri, 18 Jun 2021 00:40:26 GMT  
		Size: 193.7 MB (193651024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fa731efc631621d3f50f90fbbcb2b097a684e8d8cb0315be61e939425e2c89`  
		Last Modified: Tue, 22 Jun 2021 23:19:37 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838b070fdc3792c062bb5b6c96d57e95aa826e3f672720a26fe4ce42e09f62a6`  
		Last Modified: Fri, 02 Jul 2021 20:35:19 GMT  
		Size: 12.4 MB (12449570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b092812f8972255279e884ddd841c549e700a49cbf30502b609090da11a8366`  
		Last Modified: Fri, 02 Jul 2021 20:35:17 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632cb72d9488b73892dc69501fcea55c5c81f21d67fb024c3d81a13dd8e181f2`  
		Last Modified: Fri, 02 Jul 2021 21:30:30 GMT  
		Size: 168.5 MB (168487456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa26e65e7bdcfa431b794bb86fb835d0ba92125cc1f674909deb60817b0ffc7`  
		Last Modified: Fri, 02 Jul 2021 21:32:08 GMT  
		Size: 297.6 MB (297643176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:778bdda6cf557625368df98f86b4555d4484fa3578482c0f622ba8d20ce3334f`  
		Last Modified: Fri, 02 Jul 2021 21:31:48 GMT  
		Size: 795.4 KB (795418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f1b4a5284c1fb17dc78353b7d19eca4c02c7f51faf45f50b6fe6a3e44f17f88`  
		Last Modified: Fri, 02 Jul 2021 21:31:47 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f7600885f2faa71d2a0ce2f1b6baeabed4422fba71f131890e69726d9cfce9`  
		Last Modified: Fri, 02 Jul 2021 21:31:47 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e682ee044d627db17e38f2f2ff093a8cea613bd97d7109a738de6426281da84a`  
		Last Modified: Fri, 02 Jul 2021 21:31:47 GMT  
		Size: 5.2 KB (5235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ea14025ccd7f5ae72333faa029b366380ce839017cdb4025860c68672b8b96`  
		Last Modified: Fri, 02 Jul 2021 21:31:47 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:lts-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:0ddf979c392d089c97254e695ee7ee8858c7226de04fa721a5058bd40bd0ea7f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **709.0 MB (708983644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea2131062ee3bd998cc1ad9d0c7efa828713dee230fab020f49d5e46a40cfe0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 17 Jun 2021 23:53:58 GMT
ADD file:9e94a579f0495fce8fac6889d0b9b2cd576d5b3ce9f18ff913ad99a503756769 in / 
# Thu, 17 Jun 2021 23:53:59 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:31:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 18 Jun 2021 00:31:32 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:31:58 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Fri, 18 Jun 2021 00:32:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 18 Jun 2021 00:32:10 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Jun 2021 00:32:10 GMT
CMD ["jshell"]
# Tue, 22 Jun 2021 23:25:06 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 22 Jun 2021 23:25:06 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 22 Jun 2021 23:25:07 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 22 Jun 2021 23:25:07 GMT
WORKDIR /usr/local/tomcat
# Tue, 22 Jun 2021 23:25:07 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 23:25:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 23:30:28 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 22 Jun 2021 23:30:29 GMT
ENV TOMCAT_MAJOR=8
# Tue, 22 Jun 2021 23:30:29 GMT
ENV TOMCAT_VERSION=8.5.68
# Tue, 22 Jun 2021 23:30:29 GMT
ENV TOMCAT_SHA512=673f8d295d6f6b8e53b30c9c81989a3586341f9660f00e61a131153f54f0ce9d41bf8f49960ef477d3ec81610e1c75c1684c8676e9ebe5015486334c443d82e5
# Fri, 02 Jul 2021 20:14:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 02 Jul 2021 20:14:25 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 02 Jul 2021 20:14:26 GMT
EXPOSE 8080
# Fri, 02 Jul 2021 20:14:26 GMT
CMD ["catalina.sh" "run"]
# Fri, 02 Jul 2021 22:10:38 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Fri, 02 Jul 2021 22:11:13 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 02 Jul 2021 22:12:05 GMT
ENV XWIKI_VERSION=12.10.8
# Fri, 02 Jul 2021 22:12:05 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.8
# Fri, 02 Jul 2021 22:12:05 GMT
ENV XWIKI_DOWNLOAD_SHA256=739471e78f8b2550849d1a869c27313c4c71b12bb9b6c9c26f77c81a993dff2e
# Fri, 02 Jul 2021 22:12:42 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 02 Jul 2021 22:12:44 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 02 Jul 2021 22:12:44 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 02 Jul 2021 22:12:44 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 02 Jul 2021 22:12:45 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 02 Jul 2021 22:12:45 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 02 Jul 2021 22:12:46 GMT
VOLUME [/usr/local/xwiki]
# Fri, 02 Jul 2021 22:12:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Jul 2021 22:12:46 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:6f86eded34a1950318569803a7e0c689175ebd9d76faf08798f88ac133b98a11`  
		Last Modified: Thu, 17 Jun 2021 23:56:04 GMT  
		Size: 27.2 MB (27158803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff470c6007f78550376884f4972cc5c767c6adc6f7d6002adddbddfb4600ea4b`  
		Last Modified: Fri, 18 Jun 2021 00:35:11 GMT  
		Size: 15.9 MB (15894169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a125d809875539cb0e1d2b0483b6223a65a2867db6c0df786d36feb6fa9bf260`  
		Last Modified: Fri, 18 Jun 2021 00:36:10 GMT  
		Size: 190.4 MB (190379258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599d9b9dba394414fe824f147f376772ae86db1750dd0c0865717476c25cd040`  
		Last Modified: Tue, 22 Jun 2021 23:41:56 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdf80a91fe0ee7a8d615c877013dd3f0f57f510581a488bb24e1d945dd212f30`  
		Last Modified: Fri, 02 Jul 2021 20:43:37 GMT  
		Size: 12.4 MB (12448780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f63370a9da1ce6088a59891070b42f6fe7d136d05c91aeb21d50398be035dbe`  
		Last Modified: Fri, 02 Jul 2021 20:43:34 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daed3696500a526a0b524e45ca20d612b3afdfbdf4e3b965b2384c9359de9952`  
		Last Modified: Fri, 02 Jul 2021 22:14:47 GMT  
		Size: 164.7 MB (164652294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2bdca7c7fda93fd53c72d634b26796ed47fea3732fa34e654e80f24a29e45d`  
		Last Modified: Fri, 02 Jul 2021 22:15:40 GMT  
		Size: 297.6 MB (297643088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1973f14560a22aba4dcd67d7d766ce12b6412478de10ca1ede26d89eef4ce002`  
		Last Modified: Fri, 02 Jul 2021 22:15:17 GMT  
		Size: 795.4 KB (795416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28dc40d8ca6a5141c9bb915f8bc1e4f7f6c72d41b8f9a67c68e1d7aef8ed4ef3`  
		Last Modified: Fri, 02 Jul 2021 22:15:17 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d684d9972a40fa0638d09f2706b84bd0fb4f24abd756f55d946d7fb7aac6509d`  
		Last Modified: Fri, 02 Jul 2021 22:15:17 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3cfc79bfb8d63baad54ecca1877c3f744947d18ec52ee2d7fc6ff840340841d`  
		Last Modified: Fri, 02 Jul 2021 22:15:17 GMT  
		Size: 5.2 KB (5230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7936b27fcebcf1c11910fcd1c354d7fe295b8a31ab83f21dd105e77e7edb3f0a`  
		Last Modified: Fri, 02 Jul 2021 22:15:17 GMT  
		Size: 2.5 KB (2501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:mysql-tomcat`

```console
$ docker pull xwiki@sha256:4eb72b2458ef8747b19e51ad101bf1e0a7b6959db0434d39f4b1abea7229002a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `xwiki:mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:107067a099d5528b862d89ac83906bfadc1050c5afdb4df595d97c10276ca0b7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **724.9 MB (724906978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65c402c5f0d76e8b941063942552357d8aa1bd590d0a2ef6251038d241b52e2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:28:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 18 Jun 2021 00:29:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:29:44 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Fri, 18 Jun 2021 00:29:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 18 Jun 2021 00:29:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Jun 2021 00:29:55 GMT
CMD ["jshell"]
# Tue, 22 Jun 2021 22:44:10 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 22 Jun 2021 22:44:11 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 22 Jun 2021 22:44:12 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 22 Jun 2021 22:44:12 GMT
WORKDIR /usr/local/tomcat
# Tue, 22 Jun 2021 22:44:12 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 22:44:12 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 23:10:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 22 Jun 2021 23:10:49 GMT
ENV TOMCAT_MAJOR=8
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_VERSION=8.5.68
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_SHA512=673f8d295d6f6b8e53b30c9c81989a3586341f9660f00e61a131153f54f0ce9d41bf8f49960ef477d3ec81610e1c75c1684c8676e9ebe5015486334c443d82e5
# Fri, 02 Jul 2021 20:10:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 02 Jul 2021 20:10:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 02 Jul 2021 20:10:28 GMT
EXPOSE 8080
# Fri, 02 Jul 2021 20:10:29 GMT
CMD ["catalina.sh" "run"]
# Fri, 02 Jul 2021 21:20:19 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Fri, 02 Jul 2021 21:22:31 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 02 Jul 2021 21:22:32 GMT
ENV XWIKI_VERSION=13.5
# Fri, 02 Jul 2021 21:22:33 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.5
# Fri, 02 Jul 2021 21:22:33 GMT
ENV XWIKI_DOWNLOAD_SHA256=3294abb19636ab2e51930f88fa9a449dd98f1aa5b2ca8d6b1a32a5ff4dd22889
# Fri, 02 Jul 2021 21:23:12 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 02 Jul 2021 21:23:13 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Fri, 02 Jul 2021 21:23:13 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Fri, 02 Jul 2021 21:23:13 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Fri, 02 Jul 2021 21:23:13 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Fri, 02 Jul 2021 21:23:14 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Fri, 02 Jul 2021 21:23:15 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 02 Jul 2021 21:23:15 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 02 Jul 2021 21:23:15 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 02 Jul 2021 21:23:16 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 02 Jul 2021 21:23:17 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 02 Jul 2021 21:23:17 GMT
VOLUME [/usr/local/xwiki]
# Fri, 02 Jul 2021 21:23:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Jul 2021 21:23:17 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7766c75e8fade5c21578ec8566d2929e7238f9ac1dbe88551bf2f147b76c65`  
		Last Modified: Fri, 18 Jun 2021 00:39:29 GMT  
		Size: 16.0 MB (16033037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3025761fffcd095f302e914141cd91fdce2a0d7b76c4f13f96753ef8b9cc4151`  
		Last Modified: Fri, 18 Jun 2021 00:40:26 GMT  
		Size: 193.7 MB (193651024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fa731efc631621d3f50f90fbbcb2b097a684e8d8cb0315be61e939425e2c89`  
		Last Modified: Tue, 22 Jun 2021 23:19:37 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838b070fdc3792c062bb5b6c96d57e95aa826e3f672720a26fe4ce42e09f62a6`  
		Last Modified: Fri, 02 Jul 2021 20:35:19 GMT  
		Size: 12.4 MB (12449570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b092812f8972255279e884ddd841c549e700a49cbf30502b609090da11a8366`  
		Last Modified: Fri, 02 Jul 2021 20:35:17 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e0c6fa70e8651d71566b155d1603cdada3e0ef5e24989a737ff1331e504248`  
		Last Modified: Fri, 02 Jul 2021 21:29:22 GMT  
		Size: 167.7 MB (167687703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9681302d705266a8fda7b06cbedec7e60d3cbe8d3a7cd396de641c01629e1f2`  
		Last Modified: Fri, 02 Jul 2021 21:29:16 GMT  
		Size: 304.3 MB (304262474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:febdbb1e1ba93a3409f287bcf8b6971cdf6b5bd7192b5905ab0d7af2b96ead9a`  
		Last Modified: Fri, 02 Jul 2021 21:28:55 GMT  
		Size: 2.3 MB (2257829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca2789ef5e5b874e548c7a49a34f758e42756de18eac72edeff0189ab67149f5`  
		Last Modified: Fri, 02 Jul 2021 21:28:54 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe89a44c02a00b967200a2582dfd5ddf10e55eaab30ce22d4e2bb8005c1ebdb2`  
		Last Modified: Fri, 02 Jul 2021 21:28:54 GMT  
		Size: 2.3 KB (2320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf13ef31df43a7fad037054463d308cac6589cf505de9902895ae97a7f94eca`  
		Last Modified: Fri, 02 Jul 2021 21:28:54 GMT  
		Size: 5.2 KB (5176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cce921ec85eee9de8e6ba6260d7d1d4983b70de2f8f1cf11217f5d209d3da50`  
		Last Modified: Fri, 02 Jul 2021 21:28:54 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:postgres-tomcat`

```console
$ docker pull xwiki@sha256:373a16b9f83d74cf54fd8d02441d4da3edb024b7661d91cd49bcfc6a14bb1d70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:f17c5ea6ceb05de50779f4f500d499c28d8a59cc6fefb33bef030e86d763e3c8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **724.2 MB (724244461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bfac1762ee5527ba0f46f2bc750dd1a00ce4874164963fabb2317767a6920f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:28:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 18 Jun 2021 00:29:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:29:44 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Fri, 18 Jun 2021 00:29:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 18 Jun 2021 00:29:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Jun 2021 00:29:55 GMT
CMD ["jshell"]
# Tue, 22 Jun 2021 22:44:10 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 22 Jun 2021 22:44:11 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 22 Jun 2021 22:44:12 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 22 Jun 2021 22:44:12 GMT
WORKDIR /usr/local/tomcat
# Tue, 22 Jun 2021 22:44:12 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 22:44:12 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 23:10:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 22 Jun 2021 23:10:49 GMT
ENV TOMCAT_MAJOR=8
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_VERSION=8.5.68
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_SHA512=673f8d295d6f6b8e53b30c9c81989a3586341f9660f00e61a131153f54f0ce9d41bf8f49960ef477d3ec81610e1c75c1684c8676e9ebe5015486334c443d82e5
# Fri, 02 Jul 2021 20:10:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 02 Jul 2021 20:10:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 02 Jul 2021 20:10:28 GMT
EXPOSE 8080
# Fri, 02 Jul 2021 20:10:29 GMT
CMD ["catalina.sh" "run"]
# Fri, 02 Jul 2021 21:20:19 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Fri, 02 Jul 2021 21:24:00 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 02 Jul 2021 21:24:01 GMT
ENV XWIKI_VERSION=13.5
# Fri, 02 Jul 2021 21:24:02 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.5
# Fri, 02 Jul 2021 21:24:02 GMT
ENV XWIKI_DOWNLOAD_SHA256=3294abb19636ab2e51930f88fa9a449dd98f1aa5b2ca8d6b1a32a5ff4dd22889
# Fri, 02 Jul 2021 21:24:41 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 02 Jul 2021 21:24:43 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 02 Jul 2021 21:24:43 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 02 Jul 2021 21:24:43 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 02 Jul 2021 21:24:44 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 02 Jul 2021 21:24:44 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 02 Jul 2021 21:24:45 GMT
VOLUME [/usr/local/xwiki]
# Fri, 02 Jul 2021 21:24:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Jul 2021 21:24:45 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7766c75e8fade5c21578ec8566d2929e7238f9ac1dbe88551bf2f147b76c65`  
		Last Modified: Fri, 18 Jun 2021 00:39:29 GMT  
		Size: 16.0 MB (16033037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3025761fffcd095f302e914141cd91fdce2a0d7b76c4f13f96753ef8b9cc4151`  
		Last Modified: Fri, 18 Jun 2021 00:40:26 GMT  
		Size: 193.7 MB (193651024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fa731efc631621d3f50f90fbbcb2b097a684e8d8cb0315be61e939425e2c89`  
		Last Modified: Tue, 22 Jun 2021 23:19:37 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838b070fdc3792c062bb5b6c96d57e95aa826e3f672720a26fe4ce42e09f62a6`  
		Last Modified: Fri, 02 Jul 2021 20:35:19 GMT  
		Size: 12.4 MB (12449570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b092812f8972255279e884ddd841c549e700a49cbf30502b609090da11a8366`  
		Last Modified: Fri, 02 Jul 2021 20:35:17 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632cb72d9488b73892dc69501fcea55c5c81f21d67fb024c3d81a13dd8e181f2`  
		Last Modified: Fri, 02 Jul 2021 21:30:30 GMT  
		Size: 168.5 MB (168487456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:767ddc1d5cc9d5ea1633a6812c6ad9d5f34045978d5451c81891ce6f3d12c337`  
		Last Modified: Fri, 02 Jul 2021 21:30:23 GMT  
		Size: 304.3 MB (304262477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b361707c0e73c7c324926a78689157d0b6e250f7501eccc39fd5dd4c44fa403c`  
		Last Modified: Fri, 02 Jul 2021 21:30:03 GMT  
		Size: 795.4 KB (795417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ebb2929fba6c692b148e1983d179a4b6aaa3474acadd557b98b46b3407cc31`  
		Last Modified: Fri, 02 Jul 2021 21:30:02 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31106cd81f9c71416e86249b91978b7bf077a7322566b0ce8cff5777639c6358`  
		Last Modified: Fri, 02 Jul 2021 21:30:02 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba012baa8e78ea94911aa405fbe7309d2afd806ee6809951d80b27fd08634b48`  
		Last Modified: Fri, 02 Jul 2021 21:30:03 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f5f84a4d0710d3a48a6098de893e454ea3d1c673040570260ed3b86f264e372`  
		Last Modified: Fri, 02 Jul 2021 21:30:02 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:52f4e634a6f13313406cc5cf0c1a342b4a80b74137ec9db23cbb46238c15c6cb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **715.6 MB (715603005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:905b3bf926ec7e0141e17ed2b04a0fc56d67a05567245b5c4afa09ec343d90b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 17 Jun 2021 23:53:58 GMT
ADD file:9e94a579f0495fce8fac6889d0b9b2cd576d5b3ce9f18ff913ad99a503756769 in / 
# Thu, 17 Jun 2021 23:53:59 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:31:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 18 Jun 2021 00:31:32 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:31:58 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Fri, 18 Jun 2021 00:32:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 18 Jun 2021 00:32:10 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Jun 2021 00:32:10 GMT
CMD ["jshell"]
# Tue, 22 Jun 2021 23:25:06 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 22 Jun 2021 23:25:06 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 22 Jun 2021 23:25:07 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 22 Jun 2021 23:25:07 GMT
WORKDIR /usr/local/tomcat
# Tue, 22 Jun 2021 23:25:07 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 23:25:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 23:30:28 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 22 Jun 2021 23:30:29 GMT
ENV TOMCAT_MAJOR=8
# Tue, 22 Jun 2021 23:30:29 GMT
ENV TOMCAT_VERSION=8.5.68
# Tue, 22 Jun 2021 23:30:29 GMT
ENV TOMCAT_SHA512=673f8d295d6f6b8e53b30c9c81989a3586341f9660f00e61a131153f54f0ce9d41bf8f49960ef477d3ec81610e1c75c1684c8676e9ebe5015486334c443d82e5
# Fri, 02 Jul 2021 20:14:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 02 Jul 2021 20:14:25 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 02 Jul 2021 20:14:26 GMT
EXPOSE 8080
# Fri, 02 Jul 2021 20:14:26 GMT
CMD ["catalina.sh" "run"]
# Fri, 02 Jul 2021 22:10:38 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Fri, 02 Jul 2021 22:11:13 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 02 Jul 2021 22:11:14 GMT
ENV XWIKI_VERSION=13.5
# Fri, 02 Jul 2021 22:11:14 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.5
# Fri, 02 Jul 2021 22:11:14 GMT
ENV XWIKI_DOWNLOAD_SHA256=3294abb19636ab2e51930f88fa9a449dd98f1aa5b2ca8d6b1a32a5ff4dd22889
# Fri, 02 Jul 2021 22:11:53 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 02 Jul 2021 22:11:54 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 02 Jul 2021 22:11:55 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 02 Jul 2021 22:11:55 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 02 Jul 2021 22:11:56 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 02 Jul 2021 22:11:56 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 02 Jul 2021 22:11:56 GMT
VOLUME [/usr/local/xwiki]
# Fri, 02 Jul 2021 22:11:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Jul 2021 22:11:56 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:6f86eded34a1950318569803a7e0c689175ebd9d76faf08798f88ac133b98a11`  
		Last Modified: Thu, 17 Jun 2021 23:56:04 GMT  
		Size: 27.2 MB (27158803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff470c6007f78550376884f4972cc5c767c6adc6f7d6002adddbddfb4600ea4b`  
		Last Modified: Fri, 18 Jun 2021 00:35:11 GMT  
		Size: 15.9 MB (15894169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a125d809875539cb0e1d2b0483b6223a65a2867db6c0df786d36feb6fa9bf260`  
		Last Modified: Fri, 18 Jun 2021 00:36:10 GMT  
		Size: 190.4 MB (190379258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599d9b9dba394414fe824f147f376772ae86db1750dd0c0865717476c25cd040`  
		Last Modified: Tue, 22 Jun 2021 23:41:56 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdf80a91fe0ee7a8d615c877013dd3f0f57f510581a488bb24e1d945dd212f30`  
		Last Modified: Fri, 02 Jul 2021 20:43:37 GMT  
		Size: 12.4 MB (12448780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f63370a9da1ce6088a59891070b42f6fe7d136d05c91aeb21d50398be035dbe`  
		Last Modified: Fri, 02 Jul 2021 20:43:34 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daed3696500a526a0b524e45ca20d612b3afdfbdf4e3b965b2384c9359de9952`  
		Last Modified: Fri, 02 Jul 2021 22:14:47 GMT  
		Size: 164.7 MB (164652294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a220e402041502b22a6098d44ced1d4099eae462963ccb07ab34997ae5350a4f`  
		Last Modified: Fri, 02 Jul 2021 22:14:43 GMT  
		Size: 304.3 MB (304262497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbe6d99c11bcf58c14ff7bd941299f80845365b2889062754658a6c30cbd8753`  
		Last Modified: Fri, 02 Jul 2021 22:14:20 GMT  
		Size: 795.4 KB (795415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6332f69ccc13af037975d4d700ab40f7a705e023f2574050671862a4151bbf9a`  
		Last Modified: Fri, 02 Jul 2021 22:14:19 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643f173e80f63080795f37afcb10709e14e4cfd799ae3b2fecccd4f205c05ed6`  
		Last Modified: Fri, 02 Jul 2021 22:14:19 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b91509711133471fa08ab523dab7699c2455003c7c247042893074f443700b`  
		Last Modified: Fri, 02 Jul 2021 22:14:20 GMT  
		Size: 5.2 KB (5173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca603534af32c6957d57352e18622eab0f5a32b16b1dc811586d6315f649725`  
		Last Modified: Fri, 02 Jul 2021 22:14:19 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:stable`

```console
$ docker pull xwiki@sha256:4eb72b2458ef8747b19e51ad101bf1e0a7b6959db0434d39f4b1abea7229002a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `xwiki:stable` - linux; amd64

```console
$ docker pull xwiki@sha256:107067a099d5528b862d89ac83906bfadc1050c5afdb4df595d97c10276ca0b7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **724.9 MB (724906978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65c402c5f0d76e8b941063942552357d8aa1bd590d0a2ef6251038d241b52e2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:28:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 18 Jun 2021 00:29:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:29:44 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Fri, 18 Jun 2021 00:29:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 18 Jun 2021 00:29:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Jun 2021 00:29:55 GMT
CMD ["jshell"]
# Tue, 22 Jun 2021 22:44:10 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 22 Jun 2021 22:44:11 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 22 Jun 2021 22:44:12 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 22 Jun 2021 22:44:12 GMT
WORKDIR /usr/local/tomcat
# Tue, 22 Jun 2021 22:44:12 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 22:44:12 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 23:10:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 22 Jun 2021 23:10:49 GMT
ENV TOMCAT_MAJOR=8
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_VERSION=8.5.68
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_SHA512=673f8d295d6f6b8e53b30c9c81989a3586341f9660f00e61a131153f54f0ce9d41bf8f49960ef477d3ec81610e1c75c1684c8676e9ebe5015486334c443d82e5
# Fri, 02 Jul 2021 20:10:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 02 Jul 2021 20:10:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 02 Jul 2021 20:10:28 GMT
EXPOSE 8080
# Fri, 02 Jul 2021 20:10:29 GMT
CMD ["catalina.sh" "run"]
# Fri, 02 Jul 2021 21:20:19 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Fri, 02 Jul 2021 21:22:31 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 02 Jul 2021 21:22:32 GMT
ENV XWIKI_VERSION=13.5
# Fri, 02 Jul 2021 21:22:33 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.5
# Fri, 02 Jul 2021 21:22:33 GMT
ENV XWIKI_DOWNLOAD_SHA256=3294abb19636ab2e51930f88fa9a449dd98f1aa5b2ca8d6b1a32a5ff4dd22889
# Fri, 02 Jul 2021 21:23:12 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 02 Jul 2021 21:23:13 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Fri, 02 Jul 2021 21:23:13 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Fri, 02 Jul 2021 21:23:13 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Fri, 02 Jul 2021 21:23:13 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Fri, 02 Jul 2021 21:23:14 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Fri, 02 Jul 2021 21:23:15 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 02 Jul 2021 21:23:15 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 02 Jul 2021 21:23:15 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 02 Jul 2021 21:23:16 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 02 Jul 2021 21:23:17 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 02 Jul 2021 21:23:17 GMT
VOLUME [/usr/local/xwiki]
# Fri, 02 Jul 2021 21:23:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Jul 2021 21:23:17 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7766c75e8fade5c21578ec8566d2929e7238f9ac1dbe88551bf2f147b76c65`  
		Last Modified: Fri, 18 Jun 2021 00:39:29 GMT  
		Size: 16.0 MB (16033037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3025761fffcd095f302e914141cd91fdce2a0d7b76c4f13f96753ef8b9cc4151`  
		Last Modified: Fri, 18 Jun 2021 00:40:26 GMT  
		Size: 193.7 MB (193651024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fa731efc631621d3f50f90fbbcb2b097a684e8d8cb0315be61e939425e2c89`  
		Last Modified: Tue, 22 Jun 2021 23:19:37 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838b070fdc3792c062bb5b6c96d57e95aa826e3f672720a26fe4ce42e09f62a6`  
		Last Modified: Fri, 02 Jul 2021 20:35:19 GMT  
		Size: 12.4 MB (12449570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b092812f8972255279e884ddd841c549e700a49cbf30502b609090da11a8366`  
		Last Modified: Fri, 02 Jul 2021 20:35:17 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e0c6fa70e8651d71566b155d1603cdada3e0ef5e24989a737ff1331e504248`  
		Last Modified: Fri, 02 Jul 2021 21:29:22 GMT  
		Size: 167.7 MB (167687703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9681302d705266a8fda7b06cbedec7e60d3cbe8d3a7cd396de641c01629e1f2`  
		Last Modified: Fri, 02 Jul 2021 21:29:16 GMT  
		Size: 304.3 MB (304262474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:febdbb1e1ba93a3409f287bcf8b6971cdf6b5bd7192b5905ab0d7af2b96ead9a`  
		Last Modified: Fri, 02 Jul 2021 21:28:55 GMT  
		Size: 2.3 MB (2257829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca2789ef5e5b874e548c7a49a34f758e42756de18eac72edeff0189ab67149f5`  
		Last Modified: Fri, 02 Jul 2021 21:28:54 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe89a44c02a00b967200a2582dfd5ddf10e55eaab30ce22d4e2bb8005c1ebdb2`  
		Last Modified: Fri, 02 Jul 2021 21:28:54 GMT  
		Size: 2.3 KB (2320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf13ef31df43a7fad037054463d308cac6589cf505de9902895ae97a7f94eca`  
		Last Modified: Fri, 02 Jul 2021 21:28:54 GMT  
		Size: 5.2 KB (5176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cce921ec85eee9de8e6ba6260d7d1d4983b70de2f8f1cf11217f5d209d3da50`  
		Last Modified: Fri, 02 Jul 2021 21:28:54 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:stable-mysql`

```console
$ docker pull xwiki@sha256:4eb72b2458ef8747b19e51ad101bf1e0a7b6959db0434d39f4b1abea7229002a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `xwiki:stable-mysql` - linux; amd64

```console
$ docker pull xwiki@sha256:107067a099d5528b862d89ac83906bfadc1050c5afdb4df595d97c10276ca0b7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **724.9 MB (724906978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65c402c5f0d76e8b941063942552357d8aa1bd590d0a2ef6251038d241b52e2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:28:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 18 Jun 2021 00:29:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:29:44 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Fri, 18 Jun 2021 00:29:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 18 Jun 2021 00:29:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Jun 2021 00:29:55 GMT
CMD ["jshell"]
# Tue, 22 Jun 2021 22:44:10 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 22 Jun 2021 22:44:11 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 22 Jun 2021 22:44:12 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 22 Jun 2021 22:44:12 GMT
WORKDIR /usr/local/tomcat
# Tue, 22 Jun 2021 22:44:12 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 22:44:12 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 23:10:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 22 Jun 2021 23:10:49 GMT
ENV TOMCAT_MAJOR=8
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_VERSION=8.5.68
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_SHA512=673f8d295d6f6b8e53b30c9c81989a3586341f9660f00e61a131153f54f0ce9d41bf8f49960ef477d3ec81610e1c75c1684c8676e9ebe5015486334c443d82e5
# Fri, 02 Jul 2021 20:10:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 02 Jul 2021 20:10:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 02 Jul 2021 20:10:28 GMT
EXPOSE 8080
# Fri, 02 Jul 2021 20:10:29 GMT
CMD ["catalina.sh" "run"]
# Fri, 02 Jul 2021 21:20:19 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Fri, 02 Jul 2021 21:22:31 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 02 Jul 2021 21:22:32 GMT
ENV XWIKI_VERSION=13.5
# Fri, 02 Jul 2021 21:22:33 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.5
# Fri, 02 Jul 2021 21:22:33 GMT
ENV XWIKI_DOWNLOAD_SHA256=3294abb19636ab2e51930f88fa9a449dd98f1aa5b2ca8d6b1a32a5ff4dd22889
# Fri, 02 Jul 2021 21:23:12 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 02 Jul 2021 21:23:13 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Fri, 02 Jul 2021 21:23:13 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Fri, 02 Jul 2021 21:23:13 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Fri, 02 Jul 2021 21:23:13 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Fri, 02 Jul 2021 21:23:14 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Fri, 02 Jul 2021 21:23:15 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 02 Jul 2021 21:23:15 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 02 Jul 2021 21:23:15 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 02 Jul 2021 21:23:16 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 02 Jul 2021 21:23:17 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 02 Jul 2021 21:23:17 GMT
VOLUME [/usr/local/xwiki]
# Fri, 02 Jul 2021 21:23:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Jul 2021 21:23:17 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7766c75e8fade5c21578ec8566d2929e7238f9ac1dbe88551bf2f147b76c65`  
		Last Modified: Fri, 18 Jun 2021 00:39:29 GMT  
		Size: 16.0 MB (16033037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3025761fffcd095f302e914141cd91fdce2a0d7b76c4f13f96753ef8b9cc4151`  
		Last Modified: Fri, 18 Jun 2021 00:40:26 GMT  
		Size: 193.7 MB (193651024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fa731efc631621d3f50f90fbbcb2b097a684e8d8cb0315be61e939425e2c89`  
		Last Modified: Tue, 22 Jun 2021 23:19:37 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838b070fdc3792c062bb5b6c96d57e95aa826e3f672720a26fe4ce42e09f62a6`  
		Last Modified: Fri, 02 Jul 2021 20:35:19 GMT  
		Size: 12.4 MB (12449570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b092812f8972255279e884ddd841c549e700a49cbf30502b609090da11a8366`  
		Last Modified: Fri, 02 Jul 2021 20:35:17 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e0c6fa70e8651d71566b155d1603cdada3e0ef5e24989a737ff1331e504248`  
		Last Modified: Fri, 02 Jul 2021 21:29:22 GMT  
		Size: 167.7 MB (167687703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9681302d705266a8fda7b06cbedec7e60d3cbe8d3a7cd396de641c01629e1f2`  
		Last Modified: Fri, 02 Jul 2021 21:29:16 GMT  
		Size: 304.3 MB (304262474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:febdbb1e1ba93a3409f287bcf8b6971cdf6b5bd7192b5905ab0d7af2b96ead9a`  
		Last Modified: Fri, 02 Jul 2021 21:28:55 GMT  
		Size: 2.3 MB (2257829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca2789ef5e5b874e548c7a49a34f758e42756de18eac72edeff0189ab67149f5`  
		Last Modified: Fri, 02 Jul 2021 21:28:54 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe89a44c02a00b967200a2582dfd5ddf10e55eaab30ce22d4e2bb8005c1ebdb2`  
		Last Modified: Fri, 02 Jul 2021 21:28:54 GMT  
		Size: 2.3 KB (2320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf13ef31df43a7fad037054463d308cac6589cf505de9902895ae97a7f94eca`  
		Last Modified: Fri, 02 Jul 2021 21:28:54 GMT  
		Size: 5.2 KB (5176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cce921ec85eee9de8e6ba6260d7d1d4983b70de2f8f1cf11217f5d209d3da50`  
		Last Modified: Fri, 02 Jul 2021 21:28:54 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:stable-mysql-tomcat`

```console
$ docker pull xwiki@sha256:4eb72b2458ef8747b19e51ad101bf1e0a7b6959db0434d39f4b1abea7229002a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `xwiki:stable-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:107067a099d5528b862d89ac83906bfadc1050c5afdb4df595d97c10276ca0b7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **724.9 MB (724906978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65c402c5f0d76e8b941063942552357d8aa1bd590d0a2ef6251038d241b52e2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:28:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 18 Jun 2021 00:29:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:29:44 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Fri, 18 Jun 2021 00:29:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 18 Jun 2021 00:29:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Jun 2021 00:29:55 GMT
CMD ["jshell"]
# Tue, 22 Jun 2021 22:44:10 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 22 Jun 2021 22:44:11 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 22 Jun 2021 22:44:12 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 22 Jun 2021 22:44:12 GMT
WORKDIR /usr/local/tomcat
# Tue, 22 Jun 2021 22:44:12 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 22:44:12 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 23:10:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 22 Jun 2021 23:10:49 GMT
ENV TOMCAT_MAJOR=8
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_VERSION=8.5.68
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_SHA512=673f8d295d6f6b8e53b30c9c81989a3586341f9660f00e61a131153f54f0ce9d41bf8f49960ef477d3ec81610e1c75c1684c8676e9ebe5015486334c443d82e5
# Fri, 02 Jul 2021 20:10:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 02 Jul 2021 20:10:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 02 Jul 2021 20:10:28 GMT
EXPOSE 8080
# Fri, 02 Jul 2021 20:10:29 GMT
CMD ["catalina.sh" "run"]
# Fri, 02 Jul 2021 21:20:19 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Fri, 02 Jul 2021 21:22:31 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 02 Jul 2021 21:22:32 GMT
ENV XWIKI_VERSION=13.5
# Fri, 02 Jul 2021 21:22:33 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.5
# Fri, 02 Jul 2021 21:22:33 GMT
ENV XWIKI_DOWNLOAD_SHA256=3294abb19636ab2e51930f88fa9a449dd98f1aa5b2ca8d6b1a32a5ff4dd22889
# Fri, 02 Jul 2021 21:23:12 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 02 Jul 2021 21:23:13 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Fri, 02 Jul 2021 21:23:13 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Fri, 02 Jul 2021 21:23:13 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Fri, 02 Jul 2021 21:23:13 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Fri, 02 Jul 2021 21:23:14 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Fri, 02 Jul 2021 21:23:15 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 02 Jul 2021 21:23:15 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 02 Jul 2021 21:23:15 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 02 Jul 2021 21:23:16 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 02 Jul 2021 21:23:17 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 02 Jul 2021 21:23:17 GMT
VOLUME [/usr/local/xwiki]
# Fri, 02 Jul 2021 21:23:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Jul 2021 21:23:17 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7766c75e8fade5c21578ec8566d2929e7238f9ac1dbe88551bf2f147b76c65`  
		Last Modified: Fri, 18 Jun 2021 00:39:29 GMT  
		Size: 16.0 MB (16033037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3025761fffcd095f302e914141cd91fdce2a0d7b76c4f13f96753ef8b9cc4151`  
		Last Modified: Fri, 18 Jun 2021 00:40:26 GMT  
		Size: 193.7 MB (193651024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fa731efc631621d3f50f90fbbcb2b097a684e8d8cb0315be61e939425e2c89`  
		Last Modified: Tue, 22 Jun 2021 23:19:37 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838b070fdc3792c062bb5b6c96d57e95aa826e3f672720a26fe4ce42e09f62a6`  
		Last Modified: Fri, 02 Jul 2021 20:35:19 GMT  
		Size: 12.4 MB (12449570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b092812f8972255279e884ddd841c549e700a49cbf30502b609090da11a8366`  
		Last Modified: Fri, 02 Jul 2021 20:35:17 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e0c6fa70e8651d71566b155d1603cdada3e0ef5e24989a737ff1331e504248`  
		Last Modified: Fri, 02 Jul 2021 21:29:22 GMT  
		Size: 167.7 MB (167687703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9681302d705266a8fda7b06cbedec7e60d3cbe8d3a7cd396de641c01629e1f2`  
		Last Modified: Fri, 02 Jul 2021 21:29:16 GMT  
		Size: 304.3 MB (304262474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:febdbb1e1ba93a3409f287bcf8b6971cdf6b5bd7192b5905ab0d7af2b96ead9a`  
		Last Modified: Fri, 02 Jul 2021 21:28:55 GMT  
		Size: 2.3 MB (2257829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca2789ef5e5b874e548c7a49a34f758e42756de18eac72edeff0189ab67149f5`  
		Last Modified: Fri, 02 Jul 2021 21:28:54 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe89a44c02a00b967200a2582dfd5ddf10e55eaab30ce22d4e2bb8005c1ebdb2`  
		Last Modified: Fri, 02 Jul 2021 21:28:54 GMT  
		Size: 2.3 KB (2320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf13ef31df43a7fad037054463d308cac6589cf505de9902895ae97a7f94eca`  
		Last Modified: Fri, 02 Jul 2021 21:28:54 GMT  
		Size: 5.2 KB (5176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cce921ec85eee9de8e6ba6260d7d1d4983b70de2f8f1cf11217f5d209d3da50`  
		Last Modified: Fri, 02 Jul 2021 21:28:54 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:stable-postgres`

```console
$ docker pull xwiki@sha256:373a16b9f83d74cf54fd8d02441d4da3edb024b7661d91cd49bcfc6a14bb1d70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:stable-postgres` - linux; amd64

```console
$ docker pull xwiki@sha256:f17c5ea6ceb05de50779f4f500d499c28d8a59cc6fefb33bef030e86d763e3c8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **724.2 MB (724244461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bfac1762ee5527ba0f46f2bc750dd1a00ce4874164963fabb2317767a6920f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:28:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 18 Jun 2021 00:29:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:29:44 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Fri, 18 Jun 2021 00:29:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 18 Jun 2021 00:29:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Jun 2021 00:29:55 GMT
CMD ["jshell"]
# Tue, 22 Jun 2021 22:44:10 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 22 Jun 2021 22:44:11 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 22 Jun 2021 22:44:12 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 22 Jun 2021 22:44:12 GMT
WORKDIR /usr/local/tomcat
# Tue, 22 Jun 2021 22:44:12 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 22:44:12 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 23:10:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 22 Jun 2021 23:10:49 GMT
ENV TOMCAT_MAJOR=8
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_VERSION=8.5.68
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_SHA512=673f8d295d6f6b8e53b30c9c81989a3586341f9660f00e61a131153f54f0ce9d41bf8f49960ef477d3ec81610e1c75c1684c8676e9ebe5015486334c443d82e5
# Fri, 02 Jul 2021 20:10:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 02 Jul 2021 20:10:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 02 Jul 2021 20:10:28 GMT
EXPOSE 8080
# Fri, 02 Jul 2021 20:10:29 GMT
CMD ["catalina.sh" "run"]
# Fri, 02 Jul 2021 21:20:19 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Fri, 02 Jul 2021 21:24:00 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 02 Jul 2021 21:24:01 GMT
ENV XWIKI_VERSION=13.5
# Fri, 02 Jul 2021 21:24:02 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.5
# Fri, 02 Jul 2021 21:24:02 GMT
ENV XWIKI_DOWNLOAD_SHA256=3294abb19636ab2e51930f88fa9a449dd98f1aa5b2ca8d6b1a32a5ff4dd22889
# Fri, 02 Jul 2021 21:24:41 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 02 Jul 2021 21:24:43 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 02 Jul 2021 21:24:43 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 02 Jul 2021 21:24:43 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 02 Jul 2021 21:24:44 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 02 Jul 2021 21:24:44 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 02 Jul 2021 21:24:45 GMT
VOLUME [/usr/local/xwiki]
# Fri, 02 Jul 2021 21:24:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Jul 2021 21:24:45 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7766c75e8fade5c21578ec8566d2929e7238f9ac1dbe88551bf2f147b76c65`  
		Last Modified: Fri, 18 Jun 2021 00:39:29 GMT  
		Size: 16.0 MB (16033037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3025761fffcd095f302e914141cd91fdce2a0d7b76c4f13f96753ef8b9cc4151`  
		Last Modified: Fri, 18 Jun 2021 00:40:26 GMT  
		Size: 193.7 MB (193651024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fa731efc631621d3f50f90fbbcb2b097a684e8d8cb0315be61e939425e2c89`  
		Last Modified: Tue, 22 Jun 2021 23:19:37 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838b070fdc3792c062bb5b6c96d57e95aa826e3f672720a26fe4ce42e09f62a6`  
		Last Modified: Fri, 02 Jul 2021 20:35:19 GMT  
		Size: 12.4 MB (12449570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b092812f8972255279e884ddd841c549e700a49cbf30502b609090da11a8366`  
		Last Modified: Fri, 02 Jul 2021 20:35:17 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632cb72d9488b73892dc69501fcea55c5c81f21d67fb024c3d81a13dd8e181f2`  
		Last Modified: Fri, 02 Jul 2021 21:30:30 GMT  
		Size: 168.5 MB (168487456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:767ddc1d5cc9d5ea1633a6812c6ad9d5f34045978d5451c81891ce6f3d12c337`  
		Last Modified: Fri, 02 Jul 2021 21:30:23 GMT  
		Size: 304.3 MB (304262477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b361707c0e73c7c324926a78689157d0b6e250f7501eccc39fd5dd4c44fa403c`  
		Last Modified: Fri, 02 Jul 2021 21:30:03 GMT  
		Size: 795.4 KB (795417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ebb2929fba6c692b148e1983d179a4b6aaa3474acadd557b98b46b3407cc31`  
		Last Modified: Fri, 02 Jul 2021 21:30:02 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31106cd81f9c71416e86249b91978b7bf077a7322566b0ce8cff5777639c6358`  
		Last Modified: Fri, 02 Jul 2021 21:30:02 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba012baa8e78ea94911aa405fbe7309d2afd806ee6809951d80b27fd08634b48`  
		Last Modified: Fri, 02 Jul 2021 21:30:03 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f5f84a4d0710d3a48a6098de893e454ea3d1c673040570260ed3b86f264e372`  
		Last Modified: Fri, 02 Jul 2021 21:30:02 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:stable-postgres` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:52f4e634a6f13313406cc5cf0c1a342b4a80b74137ec9db23cbb46238c15c6cb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **715.6 MB (715603005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:905b3bf926ec7e0141e17ed2b04a0fc56d67a05567245b5c4afa09ec343d90b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 17 Jun 2021 23:53:58 GMT
ADD file:9e94a579f0495fce8fac6889d0b9b2cd576d5b3ce9f18ff913ad99a503756769 in / 
# Thu, 17 Jun 2021 23:53:59 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:31:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 18 Jun 2021 00:31:32 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:31:58 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Fri, 18 Jun 2021 00:32:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 18 Jun 2021 00:32:10 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Jun 2021 00:32:10 GMT
CMD ["jshell"]
# Tue, 22 Jun 2021 23:25:06 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 22 Jun 2021 23:25:06 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 22 Jun 2021 23:25:07 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 22 Jun 2021 23:25:07 GMT
WORKDIR /usr/local/tomcat
# Tue, 22 Jun 2021 23:25:07 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 23:25:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 23:30:28 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 22 Jun 2021 23:30:29 GMT
ENV TOMCAT_MAJOR=8
# Tue, 22 Jun 2021 23:30:29 GMT
ENV TOMCAT_VERSION=8.5.68
# Tue, 22 Jun 2021 23:30:29 GMT
ENV TOMCAT_SHA512=673f8d295d6f6b8e53b30c9c81989a3586341f9660f00e61a131153f54f0ce9d41bf8f49960ef477d3ec81610e1c75c1684c8676e9ebe5015486334c443d82e5
# Fri, 02 Jul 2021 20:14:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 02 Jul 2021 20:14:25 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 02 Jul 2021 20:14:26 GMT
EXPOSE 8080
# Fri, 02 Jul 2021 20:14:26 GMT
CMD ["catalina.sh" "run"]
# Fri, 02 Jul 2021 22:10:38 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Fri, 02 Jul 2021 22:11:13 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 02 Jul 2021 22:11:14 GMT
ENV XWIKI_VERSION=13.5
# Fri, 02 Jul 2021 22:11:14 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.5
# Fri, 02 Jul 2021 22:11:14 GMT
ENV XWIKI_DOWNLOAD_SHA256=3294abb19636ab2e51930f88fa9a449dd98f1aa5b2ca8d6b1a32a5ff4dd22889
# Fri, 02 Jul 2021 22:11:53 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 02 Jul 2021 22:11:54 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 02 Jul 2021 22:11:55 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 02 Jul 2021 22:11:55 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 02 Jul 2021 22:11:56 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 02 Jul 2021 22:11:56 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 02 Jul 2021 22:11:56 GMT
VOLUME [/usr/local/xwiki]
# Fri, 02 Jul 2021 22:11:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Jul 2021 22:11:56 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:6f86eded34a1950318569803a7e0c689175ebd9d76faf08798f88ac133b98a11`  
		Last Modified: Thu, 17 Jun 2021 23:56:04 GMT  
		Size: 27.2 MB (27158803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff470c6007f78550376884f4972cc5c767c6adc6f7d6002adddbddfb4600ea4b`  
		Last Modified: Fri, 18 Jun 2021 00:35:11 GMT  
		Size: 15.9 MB (15894169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a125d809875539cb0e1d2b0483b6223a65a2867db6c0df786d36feb6fa9bf260`  
		Last Modified: Fri, 18 Jun 2021 00:36:10 GMT  
		Size: 190.4 MB (190379258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599d9b9dba394414fe824f147f376772ae86db1750dd0c0865717476c25cd040`  
		Last Modified: Tue, 22 Jun 2021 23:41:56 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdf80a91fe0ee7a8d615c877013dd3f0f57f510581a488bb24e1d945dd212f30`  
		Last Modified: Fri, 02 Jul 2021 20:43:37 GMT  
		Size: 12.4 MB (12448780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f63370a9da1ce6088a59891070b42f6fe7d136d05c91aeb21d50398be035dbe`  
		Last Modified: Fri, 02 Jul 2021 20:43:34 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daed3696500a526a0b524e45ca20d612b3afdfbdf4e3b965b2384c9359de9952`  
		Last Modified: Fri, 02 Jul 2021 22:14:47 GMT  
		Size: 164.7 MB (164652294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a220e402041502b22a6098d44ced1d4099eae462963ccb07ab34997ae5350a4f`  
		Last Modified: Fri, 02 Jul 2021 22:14:43 GMT  
		Size: 304.3 MB (304262497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbe6d99c11bcf58c14ff7bd941299f80845365b2889062754658a6c30cbd8753`  
		Last Modified: Fri, 02 Jul 2021 22:14:20 GMT  
		Size: 795.4 KB (795415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6332f69ccc13af037975d4d700ab40f7a705e023f2574050671862a4151bbf9a`  
		Last Modified: Fri, 02 Jul 2021 22:14:19 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643f173e80f63080795f37afcb10709e14e4cfd799ae3b2fecccd4f205c05ed6`  
		Last Modified: Fri, 02 Jul 2021 22:14:19 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b91509711133471fa08ab523dab7699c2455003c7c247042893074f443700b`  
		Last Modified: Fri, 02 Jul 2021 22:14:20 GMT  
		Size: 5.2 KB (5173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca603534af32c6957d57352e18622eab0f5a32b16b1dc811586d6315f649725`  
		Last Modified: Fri, 02 Jul 2021 22:14:19 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:stable-postgres-tomcat`

```console
$ docker pull xwiki@sha256:373a16b9f83d74cf54fd8d02441d4da3edb024b7661d91cd49bcfc6a14bb1d70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:stable-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:f17c5ea6ceb05de50779f4f500d499c28d8a59cc6fefb33bef030e86d763e3c8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **724.2 MB (724244461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bfac1762ee5527ba0f46f2bc750dd1a00ce4874164963fabb2317767a6920f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:28:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 18 Jun 2021 00:29:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:29:44 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Fri, 18 Jun 2021 00:29:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 18 Jun 2021 00:29:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Jun 2021 00:29:55 GMT
CMD ["jshell"]
# Tue, 22 Jun 2021 22:44:10 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 22 Jun 2021 22:44:11 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 22 Jun 2021 22:44:12 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 22 Jun 2021 22:44:12 GMT
WORKDIR /usr/local/tomcat
# Tue, 22 Jun 2021 22:44:12 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 22:44:12 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 23:10:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 22 Jun 2021 23:10:49 GMT
ENV TOMCAT_MAJOR=8
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_VERSION=8.5.68
# Tue, 22 Jun 2021 23:10:50 GMT
ENV TOMCAT_SHA512=673f8d295d6f6b8e53b30c9c81989a3586341f9660f00e61a131153f54f0ce9d41bf8f49960ef477d3ec81610e1c75c1684c8676e9ebe5015486334c443d82e5
# Fri, 02 Jul 2021 20:10:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 02 Jul 2021 20:10:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 02 Jul 2021 20:10:28 GMT
EXPOSE 8080
# Fri, 02 Jul 2021 20:10:29 GMT
CMD ["catalina.sh" "run"]
# Fri, 02 Jul 2021 21:20:19 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Fri, 02 Jul 2021 21:24:00 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 02 Jul 2021 21:24:01 GMT
ENV XWIKI_VERSION=13.5
# Fri, 02 Jul 2021 21:24:02 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.5
# Fri, 02 Jul 2021 21:24:02 GMT
ENV XWIKI_DOWNLOAD_SHA256=3294abb19636ab2e51930f88fa9a449dd98f1aa5b2ca8d6b1a32a5ff4dd22889
# Fri, 02 Jul 2021 21:24:41 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 02 Jul 2021 21:24:43 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 02 Jul 2021 21:24:43 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 02 Jul 2021 21:24:43 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 02 Jul 2021 21:24:44 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 02 Jul 2021 21:24:44 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 02 Jul 2021 21:24:45 GMT
VOLUME [/usr/local/xwiki]
# Fri, 02 Jul 2021 21:24:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Jul 2021 21:24:45 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7766c75e8fade5c21578ec8566d2929e7238f9ac1dbe88551bf2f147b76c65`  
		Last Modified: Fri, 18 Jun 2021 00:39:29 GMT  
		Size: 16.0 MB (16033037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3025761fffcd095f302e914141cd91fdce2a0d7b76c4f13f96753ef8b9cc4151`  
		Last Modified: Fri, 18 Jun 2021 00:40:26 GMT  
		Size: 193.7 MB (193651024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fa731efc631621d3f50f90fbbcb2b097a684e8d8cb0315be61e939425e2c89`  
		Last Modified: Tue, 22 Jun 2021 23:19:37 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838b070fdc3792c062bb5b6c96d57e95aa826e3f672720a26fe4ce42e09f62a6`  
		Last Modified: Fri, 02 Jul 2021 20:35:19 GMT  
		Size: 12.4 MB (12449570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b092812f8972255279e884ddd841c549e700a49cbf30502b609090da11a8366`  
		Last Modified: Fri, 02 Jul 2021 20:35:17 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632cb72d9488b73892dc69501fcea55c5c81f21d67fb024c3d81a13dd8e181f2`  
		Last Modified: Fri, 02 Jul 2021 21:30:30 GMT  
		Size: 168.5 MB (168487456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:767ddc1d5cc9d5ea1633a6812c6ad9d5f34045978d5451c81891ce6f3d12c337`  
		Last Modified: Fri, 02 Jul 2021 21:30:23 GMT  
		Size: 304.3 MB (304262477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b361707c0e73c7c324926a78689157d0b6e250f7501eccc39fd5dd4c44fa403c`  
		Last Modified: Fri, 02 Jul 2021 21:30:03 GMT  
		Size: 795.4 KB (795417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ebb2929fba6c692b148e1983d179a4b6aaa3474acadd557b98b46b3407cc31`  
		Last Modified: Fri, 02 Jul 2021 21:30:02 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31106cd81f9c71416e86249b91978b7bf077a7322566b0ce8cff5777639c6358`  
		Last Modified: Fri, 02 Jul 2021 21:30:02 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba012baa8e78ea94911aa405fbe7309d2afd806ee6809951d80b27fd08634b48`  
		Last Modified: Fri, 02 Jul 2021 21:30:03 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f5f84a4d0710d3a48a6098de893e454ea3d1c673040570260ed3b86f264e372`  
		Last Modified: Fri, 02 Jul 2021 21:30:02 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:stable-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:52f4e634a6f13313406cc5cf0c1a342b4a80b74137ec9db23cbb46238c15c6cb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **715.6 MB (715603005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:905b3bf926ec7e0141e17ed2b04a0fc56d67a05567245b5c4afa09ec343d90b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 17 Jun 2021 23:53:58 GMT
ADD file:9e94a579f0495fce8fac6889d0b9b2cd576d5b3ce9f18ff913ad99a503756769 in / 
# Thu, 17 Jun 2021 23:53:59 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:31:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 18 Jun 2021 00:31:32 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:31:58 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Fri, 18 Jun 2021 00:32:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 18 Jun 2021 00:32:10 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Jun 2021 00:32:10 GMT
CMD ["jshell"]
# Tue, 22 Jun 2021 23:25:06 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 22 Jun 2021 23:25:06 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 22 Jun 2021 23:25:07 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 22 Jun 2021 23:25:07 GMT
WORKDIR /usr/local/tomcat
# Tue, 22 Jun 2021 23:25:07 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 23:25:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 22 Jun 2021 23:30:28 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 22 Jun 2021 23:30:29 GMT
ENV TOMCAT_MAJOR=8
# Tue, 22 Jun 2021 23:30:29 GMT
ENV TOMCAT_VERSION=8.5.68
# Tue, 22 Jun 2021 23:30:29 GMT
ENV TOMCAT_SHA512=673f8d295d6f6b8e53b30c9c81989a3586341f9660f00e61a131153f54f0ce9d41bf8f49960ef477d3ec81610e1c75c1684c8676e9ebe5015486334c443d82e5
# Fri, 02 Jul 2021 20:14:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 02 Jul 2021 20:14:25 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 02 Jul 2021 20:14:26 GMT
EXPOSE 8080
# Fri, 02 Jul 2021 20:14:26 GMT
CMD ["catalina.sh" "run"]
# Fri, 02 Jul 2021 22:10:38 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Fri, 02 Jul 2021 22:11:13 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 02 Jul 2021 22:11:14 GMT
ENV XWIKI_VERSION=13.5
# Fri, 02 Jul 2021 22:11:14 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.5
# Fri, 02 Jul 2021 22:11:14 GMT
ENV XWIKI_DOWNLOAD_SHA256=3294abb19636ab2e51930f88fa9a449dd98f1aa5b2ca8d6b1a32a5ff4dd22889
# Fri, 02 Jul 2021 22:11:53 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 02 Jul 2021 22:11:54 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 02 Jul 2021 22:11:55 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 02 Jul 2021 22:11:55 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 02 Jul 2021 22:11:56 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 02 Jul 2021 22:11:56 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 02 Jul 2021 22:11:56 GMT
VOLUME [/usr/local/xwiki]
# Fri, 02 Jul 2021 22:11:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Jul 2021 22:11:56 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:6f86eded34a1950318569803a7e0c689175ebd9d76faf08798f88ac133b98a11`  
		Last Modified: Thu, 17 Jun 2021 23:56:04 GMT  
		Size: 27.2 MB (27158803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff470c6007f78550376884f4972cc5c767c6adc6f7d6002adddbddfb4600ea4b`  
		Last Modified: Fri, 18 Jun 2021 00:35:11 GMT  
		Size: 15.9 MB (15894169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a125d809875539cb0e1d2b0483b6223a65a2867db6c0df786d36feb6fa9bf260`  
		Last Modified: Fri, 18 Jun 2021 00:36:10 GMT  
		Size: 190.4 MB (190379258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599d9b9dba394414fe824f147f376772ae86db1750dd0c0865717476c25cd040`  
		Last Modified: Tue, 22 Jun 2021 23:41:56 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdf80a91fe0ee7a8d615c877013dd3f0f57f510581a488bb24e1d945dd212f30`  
		Last Modified: Fri, 02 Jul 2021 20:43:37 GMT  
		Size: 12.4 MB (12448780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f63370a9da1ce6088a59891070b42f6fe7d136d05c91aeb21d50398be035dbe`  
		Last Modified: Fri, 02 Jul 2021 20:43:34 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daed3696500a526a0b524e45ca20d612b3afdfbdf4e3b965b2384c9359de9952`  
		Last Modified: Fri, 02 Jul 2021 22:14:47 GMT  
		Size: 164.7 MB (164652294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a220e402041502b22a6098d44ced1d4099eae462963ccb07ab34997ae5350a4f`  
		Last Modified: Fri, 02 Jul 2021 22:14:43 GMT  
		Size: 304.3 MB (304262497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbe6d99c11bcf58c14ff7bd941299f80845365b2889062754658a6c30cbd8753`  
		Last Modified: Fri, 02 Jul 2021 22:14:20 GMT  
		Size: 795.4 KB (795415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6332f69ccc13af037975d4d700ab40f7a705e023f2574050671862a4151bbf9a`  
		Last Modified: Fri, 02 Jul 2021 22:14:19 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643f173e80f63080795f37afcb10709e14e4cfd799ae3b2fecccd4f205c05ed6`  
		Last Modified: Fri, 02 Jul 2021 22:14:19 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b91509711133471fa08ab523dab7699c2455003c7c247042893074f443700b`  
		Last Modified: Fri, 02 Jul 2021 22:14:20 GMT  
		Size: 5.2 KB (5173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca603534af32c6957d57352e18622eab0f5a32b16b1dc811586d6315f649725`  
		Last Modified: Fri, 02 Jul 2021 22:14:19 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
