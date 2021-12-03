<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `xwiki`

-	[`xwiki:12`](#xwiki12)
-	[`xwiki:12-mysql-tomcat`](#xwiki12-mysql-tomcat)
-	[`xwiki:12-postgres-tomcat`](#xwiki12-postgres-tomcat)
-	[`xwiki:12.10`](#xwiki1210)
-	[`xwiki:12.10-mysql-tomcat`](#xwiki1210-mysql-tomcat)
-	[`xwiki:12.10-postgres-tomcat`](#xwiki1210-postgres-tomcat)
-	[`xwiki:12.10.10`](#xwiki121010)
-	[`xwiki:12.10.10-mysql-tomcat`](#xwiki121010-mysql-tomcat)
-	[`xwiki:12.10.10-postgres-tomcat`](#xwiki121010-postgres-tomcat)
-	[`xwiki:13`](#xwiki13)
-	[`xwiki:13-mysql-tomcat`](#xwiki13-mysql-tomcat)
-	[`xwiki:13-postgres-tomcat`](#xwiki13-postgres-tomcat)
-	[`xwiki:13.10`](#xwiki1310)
-	[`xwiki:13.10-mysql-tomcat`](#xwiki1310-mysql-tomcat)
-	[`xwiki:13.10-postgres-tomcat`](#xwiki1310-postgres-tomcat)
-	[`xwiki:13.10.0`](#xwiki13100)
-	[`xwiki:13.10.0-mysql-tomcat`](#xwiki13100-mysql-tomcat)
-	[`xwiki:13.10.0-postgres-tomcat`](#xwiki13100-postgres-tomcat)
-	[`xwiki:13.4`](#xwiki134)
-	[`xwiki:13.4-mysql-tomcat`](#xwiki134-mysql-tomcat)
-	[`xwiki:13.4-postgres-tomcat`](#xwiki134-postgres-tomcat)
-	[`xwiki:13.4.5`](#xwiki1345)
-	[`xwiki:13.4.5-mysql-tomcat`](#xwiki1345-mysql-tomcat)
-	[`xwiki:13.4.5-postgres-tomcat`](#xwiki1345-postgres-tomcat)
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
$ docker pull xwiki@sha256:0c452bd65de374236c5c106311276ae850620d39c3d6a8a225b5a6883d2eaf9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:12` - linux; amd64

```console
$ docker pull xwiki@sha256:bc8aaceaa6d467495242300c981dd77491cea326c58f7385481125a224888af2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.9 MB (835934777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daf03bf371ed121b6f8890ce6bebb499d4cfa8314d1de1f32552e4f86d0582f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:07 GMT
ADD file:e777355768c63f735e5458c7e0ada7f556f27d0493b3af35dc7c34f9c4294ea9 in / 
# Thu, 02 Dec 2021 02:48:08 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:39:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Dec 2021 03:40:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:34:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:34:20 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 02 Dec 2021 11:34:22 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 02 Dec 2021 11:34:22 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 11:34:22 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 11:34:23 GMT
ENV JAVA_VERSION=11.0.13
# Thu, 02 Dec 2021 11:34:48 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_x64_linux_11.0.13_8.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_aarch64_linux_11.0.13_8.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 02 Dec 2021 11:34:49 GMT
CMD ["jshell"]
# Fri, 03 Dec 2021 14:11:49 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Dec 2021 14:11:50 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Dec 2021 14:11:50 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 03 Dec 2021 14:11:51 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Dec 2021 14:11:51 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 14:11:51 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 14:27:34 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 03 Dec 2021 14:27:34 GMT
ENV TOMCAT_MAJOR=9
# Fri, 03 Dec 2021 14:27:34 GMT
ENV TOMCAT_VERSION=9.0.55
# Fri, 03 Dec 2021 14:27:35 GMT
ENV TOMCAT_SHA512=a0c480b8bba09069bda3b57f54e658450a59d799474ad587dead0ffbf5074c16ee3f9f9c13312d0ff3227c7034589dabf25941fbd672838e9baeee9661e024dc
# Fri, 03 Dec 2021 14:28:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 03 Dec 2021 14:28:03 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 03 Dec 2021 14:28:03 GMT
EXPOSE 8080
# Fri, 03 Dec 2021 14:28:03 GMT
CMD ["catalina.sh" "run"]
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 03 Dec 2021 20:52:45 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 20:54:56 GMT
ENV XWIKI_VERSION=12.10.10
# Fri, 03 Dec 2021 20:54:56 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.10
# Fri, 03 Dec 2021 20:54:56 GMT
ENV XWIKI_DOWNLOAD_SHA256=42364fd6a3d575c78969ebb12a7d28360ccff3b478379cf30232d6611ccbe9e0
# Fri, 03 Dec 2021 20:55:45 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 03 Dec 2021 20:55:46 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Fri, 03 Dec 2021 20:55:46 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Fri, 03 Dec 2021 20:55:46 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Fri, 03 Dec 2021 20:55:46 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Fri, 03 Dec 2021 20:55:46 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Fri, 03 Dec 2021 20:55:47 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 03 Dec 2021 20:55:48 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 03 Dec 2021 20:55:48 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 03 Dec 2021 20:55:49 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 03 Dec 2021 20:55:49 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 03 Dec 2021 20:55:49 GMT
VOLUME [/usr/local/xwiki]
# Fri, 03 Dec 2021 20:55:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Dec 2021 20:55:49 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:5e0b432e8ba9d9029a000e627840b98ffc1ed0c5172075b7d3e869be0df0fe9b`  
		Last Modified: Thu, 02 Dec 2021 02:53:18 GMT  
		Size: 54.9 MB (54932878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84cfd68b5cea612a8343c346bfa5bd6c486769010d12f7ec86b23c74887feb2`  
		Last Modified: Thu, 02 Dec 2021 03:49:22 GMT  
		Size: 5.2 MB (5153424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b8f2315954535f1e27cd13d777e73da4a787b0aebf4241d225beff3c91cbb1`  
		Last Modified: Thu, 02 Dec 2021 03:49:23 GMT  
		Size: 10.9 MB (10871995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0598fa43a7e793a76c198e8d45d8810394e1cfc943b2673d7fcf5a6fdc4f45b3`  
		Last Modified: Thu, 02 Dec 2021 03:49:46 GMT  
		Size: 54.6 MB (54567844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d35e3be804184359e0904389b149de16f159e30436d7a8a970aef67a4d155b`  
		Last Modified: Thu, 02 Dec 2021 11:54:46 GMT  
		Size: 5.4 MB (5420076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc448a0c88bee4d3cf6a928aa2b4cf499f4cb05034093c581342d414188a566`  
		Last Modified: Thu, 02 Dec 2021 11:54:45 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbdff6e5955b8bcd2e24b1a49fa4ec593ad333133c52911832aa2a7893f542da`  
		Last Modified: Thu, 02 Dec 2021 11:55:04 GMT  
		Size: 203.1 MB (203118915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5daf3771e3d8c27aa89cbcfef659790a2218e319899d49fbccde199e1780a5ef`  
		Last Modified: Fri, 03 Dec 2021 14:54:53 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5434ab540d864811e12dac3650eb0bc67bc8f6d7a6cb1f3c832e2c078c45302c`  
		Last Modified: Fri, 03 Dec 2021 15:08:17 GMT  
		Size: 12.5 MB (12523151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f43f4b2f615c39e867b3110fbc83f1d8fa2b72e4788cdcc91ea5dd73e97102`  
		Last Modified: Fri, 03 Dec 2021 15:08:16 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb64e66bc904d2f87948ce847a95dfa536c19132b599dc7f18ee2fec72ce7a8`  
		Last Modified: Fri, 03 Dec 2021 20:57:50 GMT  
		Size: 189.4 MB (189410805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:322c3fa9aeb088d28eaf87bee8cc347dd2446ec513406bfcc94fe921c47ef232`  
		Last Modified: Fri, 03 Dec 2021 20:59:42 GMT  
		Size: 297.7 MB (297665996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90fcdaa3c2b3eab89db62dbbc268566389c9d3aeca137f15cbdb15b0d7eaffe9`  
		Last Modified: Fri, 03 Dec 2021 20:59:25 GMT  
		Size: 2.3 MB (2257807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d51c8a2c6527bec03b855db0bdb4b58452c4af299cc4f40fc1690573eedb2676`  
		Last Modified: Fri, 03 Dec 2021 20:59:25 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56b515d1801ae6cbeea27c7f418568eb18e5310be586bb180e59cb2ddb54b41c`  
		Last Modified: Fri, 03 Dec 2021 20:59:25 GMT  
		Size: 2.3 KB (2303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9098d697724f1d37cb1cbc0032ca0057920efbebe8ff19f8391d8b88182881b6`  
		Last Modified: Fri, 03 Dec 2021 20:59:25 GMT  
		Size: 5.2 KB (5224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00faacd3e28eae83a4d5fa60009ec43904a971ad076d496b8ba65a2cc6331f3e`  
		Last Modified: Fri, 03 Dec 2021 20:59:25 GMT  
		Size: 2.5 KB (2501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:12-mysql-tomcat`

```console
$ docker pull xwiki@sha256:0c452bd65de374236c5c106311276ae850620d39c3d6a8a225b5a6883d2eaf9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:12-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:bc8aaceaa6d467495242300c981dd77491cea326c58f7385481125a224888af2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.9 MB (835934777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daf03bf371ed121b6f8890ce6bebb499d4cfa8314d1de1f32552e4f86d0582f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:07 GMT
ADD file:e777355768c63f735e5458c7e0ada7f556f27d0493b3af35dc7c34f9c4294ea9 in / 
# Thu, 02 Dec 2021 02:48:08 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:39:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Dec 2021 03:40:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:34:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:34:20 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 02 Dec 2021 11:34:22 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 02 Dec 2021 11:34:22 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 11:34:22 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 11:34:23 GMT
ENV JAVA_VERSION=11.0.13
# Thu, 02 Dec 2021 11:34:48 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_x64_linux_11.0.13_8.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_aarch64_linux_11.0.13_8.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 02 Dec 2021 11:34:49 GMT
CMD ["jshell"]
# Fri, 03 Dec 2021 14:11:49 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Dec 2021 14:11:50 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Dec 2021 14:11:50 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 03 Dec 2021 14:11:51 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Dec 2021 14:11:51 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 14:11:51 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 14:27:34 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 03 Dec 2021 14:27:34 GMT
ENV TOMCAT_MAJOR=9
# Fri, 03 Dec 2021 14:27:34 GMT
ENV TOMCAT_VERSION=9.0.55
# Fri, 03 Dec 2021 14:27:35 GMT
ENV TOMCAT_SHA512=a0c480b8bba09069bda3b57f54e658450a59d799474ad587dead0ffbf5074c16ee3f9f9c13312d0ff3227c7034589dabf25941fbd672838e9baeee9661e024dc
# Fri, 03 Dec 2021 14:28:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 03 Dec 2021 14:28:03 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 03 Dec 2021 14:28:03 GMT
EXPOSE 8080
# Fri, 03 Dec 2021 14:28:03 GMT
CMD ["catalina.sh" "run"]
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 03 Dec 2021 20:52:45 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 20:54:56 GMT
ENV XWIKI_VERSION=12.10.10
# Fri, 03 Dec 2021 20:54:56 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.10
# Fri, 03 Dec 2021 20:54:56 GMT
ENV XWIKI_DOWNLOAD_SHA256=42364fd6a3d575c78969ebb12a7d28360ccff3b478379cf30232d6611ccbe9e0
# Fri, 03 Dec 2021 20:55:45 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 03 Dec 2021 20:55:46 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Fri, 03 Dec 2021 20:55:46 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Fri, 03 Dec 2021 20:55:46 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Fri, 03 Dec 2021 20:55:46 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Fri, 03 Dec 2021 20:55:46 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Fri, 03 Dec 2021 20:55:47 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 03 Dec 2021 20:55:48 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 03 Dec 2021 20:55:48 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 03 Dec 2021 20:55:49 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 03 Dec 2021 20:55:49 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 03 Dec 2021 20:55:49 GMT
VOLUME [/usr/local/xwiki]
# Fri, 03 Dec 2021 20:55:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Dec 2021 20:55:49 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:5e0b432e8ba9d9029a000e627840b98ffc1ed0c5172075b7d3e869be0df0fe9b`  
		Last Modified: Thu, 02 Dec 2021 02:53:18 GMT  
		Size: 54.9 MB (54932878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84cfd68b5cea612a8343c346bfa5bd6c486769010d12f7ec86b23c74887feb2`  
		Last Modified: Thu, 02 Dec 2021 03:49:22 GMT  
		Size: 5.2 MB (5153424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b8f2315954535f1e27cd13d777e73da4a787b0aebf4241d225beff3c91cbb1`  
		Last Modified: Thu, 02 Dec 2021 03:49:23 GMT  
		Size: 10.9 MB (10871995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0598fa43a7e793a76c198e8d45d8810394e1cfc943b2673d7fcf5a6fdc4f45b3`  
		Last Modified: Thu, 02 Dec 2021 03:49:46 GMT  
		Size: 54.6 MB (54567844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d35e3be804184359e0904389b149de16f159e30436d7a8a970aef67a4d155b`  
		Last Modified: Thu, 02 Dec 2021 11:54:46 GMT  
		Size: 5.4 MB (5420076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc448a0c88bee4d3cf6a928aa2b4cf499f4cb05034093c581342d414188a566`  
		Last Modified: Thu, 02 Dec 2021 11:54:45 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbdff6e5955b8bcd2e24b1a49fa4ec593ad333133c52911832aa2a7893f542da`  
		Last Modified: Thu, 02 Dec 2021 11:55:04 GMT  
		Size: 203.1 MB (203118915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5daf3771e3d8c27aa89cbcfef659790a2218e319899d49fbccde199e1780a5ef`  
		Last Modified: Fri, 03 Dec 2021 14:54:53 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5434ab540d864811e12dac3650eb0bc67bc8f6d7a6cb1f3c832e2c078c45302c`  
		Last Modified: Fri, 03 Dec 2021 15:08:17 GMT  
		Size: 12.5 MB (12523151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f43f4b2f615c39e867b3110fbc83f1d8fa2b72e4788cdcc91ea5dd73e97102`  
		Last Modified: Fri, 03 Dec 2021 15:08:16 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb64e66bc904d2f87948ce847a95dfa536c19132b599dc7f18ee2fec72ce7a8`  
		Last Modified: Fri, 03 Dec 2021 20:57:50 GMT  
		Size: 189.4 MB (189410805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:322c3fa9aeb088d28eaf87bee8cc347dd2446ec513406bfcc94fe921c47ef232`  
		Last Modified: Fri, 03 Dec 2021 20:59:42 GMT  
		Size: 297.7 MB (297665996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90fcdaa3c2b3eab89db62dbbc268566389c9d3aeca137f15cbdb15b0d7eaffe9`  
		Last Modified: Fri, 03 Dec 2021 20:59:25 GMT  
		Size: 2.3 MB (2257807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d51c8a2c6527bec03b855db0bdb4b58452c4af299cc4f40fc1690573eedb2676`  
		Last Modified: Fri, 03 Dec 2021 20:59:25 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56b515d1801ae6cbeea27c7f418568eb18e5310be586bb180e59cb2ddb54b41c`  
		Last Modified: Fri, 03 Dec 2021 20:59:25 GMT  
		Size: 2.3 KB (2303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9098d697724f1d37cb1cbc0032ca0057920efbebe8ff19f8391d8b88182881b6`  
		Last Modified: Fri, 03 Dec 2021 20:59:25 GMT  
		Size: 5.2 KB (5224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00faacd3e28eae83a4d5fa60009ec43904a971ad076d496b8ba65a2cc6331f3e`  
		Last Modified: Fri, 03 Dec 2021 20:59:25 GMT  
		Size: 2.5 KB (2501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:12-postgres-tomcat`

```console
$ docker pull xwiki@sha256:33059b78ebe52d5089e0f0d0228b20ee00e97884213ea98e79d3c23d0265a18e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:12-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:b6da64a702495f77148d7907115512347ed792c3e13745f700877be9196acfaf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.4 MB (835398749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8000205aad7fbc2729bde9231f8618248a910cad7dc4c0f6ecc6c3f82ab0f7e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:07 GMT
ADD file:e777355768c63f735e5458c7e0ada7f556f27d0493b3af35dc7c34f9c4294ea9 in / 
# Thu, 02 Dec 2021 02:48:08 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:39:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Dec 2021 03:40:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:34:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:34:20 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 02 Dec 2021 11:34:22 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 02 Dec 2021 11:34:22 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 11:34:22 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 11:34:23 GMT
ENV JAVA_VERSION=11.0.13
# Thu, 02 Dec 2021 11:34:48 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_x64_linux_11.0.13_8.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_aarch64_linux_11.0.13_8.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 02 Dec 2021 11:34:49 GMT
CMD ["jshell"]
# Fri, 03 Dec 2021 14:11:49 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Dec 2021 14:11:50 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Dec 2021 14:11:50 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 03 Dec 2021 14:11:51 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Dec 2021 14:11:51 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 14:11:51 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 14:27:34 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 03 Dec 2021 14:27:34 GMT
ENV TOMCAT_MAJOR=9
# Fri, 03 Dec 2021 14:27:34 GMT
ENV TOMCAT_VERSION=9.0.55
# Fri, 03 Dec 2021 14:27:35 GMT
ENV TOMCAT_SHA512=a0c480b8bba09069bda3b57f54e658450a59d799474ad587dead0ffbf5074c16ee3f9f9c13312d0ff3227c7034589dabf25941fbd672838e9baeee9661e024dc
# Fri, 03 Dec 2021 14:28:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 03 Dec 2021 14:28:03 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 03 Dec 2021 14:28:03 GMT
EXPOSE 8080
# Fri, 03 Dec 2021 14:28:03 GMT
CMD ["catalina.sh" "run"]
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 03 Dec 2021 20:54:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 20:55:53 GMT
ENV XWIKI_VERSION=12.10.10
# Fri, 03 Dec 2021 20:55:53 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.10
# Fri, 03 Dec 2021 20:55:53 GMT
ENV XWIKI_DOWNLOAD_SHA256=42364fd6a3d575c78969ebb12a7d28360ccff3b478379cf30232d6611ccbe9e0
# Fri, 03 Dec 2021 20:56:32 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 03 Dec 2021 20:56:34 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 03 Dec 2021 20:56:34 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 03 Dec 2021 20:56:34 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 03 Dec 2021 20:56:35 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 03 Dec 2021 20:56:35 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 03 Dec 2021 20:56:36 GMT
VOLUME [/usr/local/xwiki]
# Fri, 03 Dec 2021 20:56:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Dec 2021 20:56:36 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:5e0b432e8ba9d9029a000e627840b98ffc1ed0c5172075b7d3e869be0df0fe9b`  
		Last Modified: Thu, 02 Dec 2021 02:53:18 GMT  
		Size: 54.9 MB (54932878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84cfd68b5cea612a8343c346bfa5bd6c486769010d12f7ec86b23c74887feb2`  
		Last Modified: Thu, 02 Dec 2021 03:49:22 GMT  
		Size: 5.2 MB (5153424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b8f2315954535f1e27cd13d777e73da4a787b0aebf4241d225beff3c91cbb1`  
		Last Modified: Thu, 02 Dec 2021 03:49:23 GMT  
		Size: 10.9 MB (10871995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0598fa43a7e793a76c198e8d45d8810394e1cfc943b2673d7fcf5a6fdc4f45b3`  
		Last Modified: Thu, 02 Dec 2021 03:49:46 GMT  
		Size: 54.6 MB (54567844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d35e3be804184359e0904389b149de16f159e30436d7a8a970aef67a4d155b`  
		Last Modified: Thu, 02 Dec 2021 11:54:46 GMT  
		Size: 5.4 MB (5420076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc448a0c88bee4d3cf6a928aa2b4cf499f4cb05034093c581342d414188a566`  
		Last Modified: Thu, 02 Dec 2021 11:54:45 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbdff6e5955b8bcd2e24b1a49fa4ec593ad333133c52911832aa2a7893f542da`  
		Last Modified: Thu, 02 Dec 2021 11:55:04 GMT  
		Size: 203.1 MB (203118915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5daf3771e3d8c27aa89cbcfef659790a2218e319899d49fbccde199e1780a5ef`  
		Last Modified: Fri, 03 Dec 2021 14:54:53 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5434ab540d864811e12dac3650eb0bc67bc8f6d7a6cb1f3c832e2c078c45302c`  
		Last Modified: Fri, 03 Dec 2021 15:08:17 GMT  
		Size: 12.5 MB (12523151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f43f4b2f615c39e867b3110fbc83f1d8fa2b72e4788cdcc91ea5dd73e97102`  
		Last Modified: Fri, 03 Dec 2021 15:08:16 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c96c2f945ecec7eda758824db2032432765e7a0128ef11d3c1841ac2dc2e5d95`  
		Last Modified: Fri, 03 Dec 2021 20:59:00 GMT  
		Size: 190.3 MB (190286185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98dd220d8d99ab2f82e0c4d98e1eda554b20e4cdd518e4863383ad47a2ede008`  
		Last Modified: Fri, 03 Dec 2021 21:00:34 GMT  
		Size: 297.7 MB (297666042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68c6a4d55d8aedc737c28c16053a45f219463db9f442fd0139d5dd559732b8dc`  
		Last Modified: Fri, 03 Dec 2021 21:00:17 GMT  
		Size: 846.2 KB (846205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68bf6e53b283f66ee03293c481736522efbf14497b1b2e32a0f7df3b5a68f310`  
		Last Modified: Fri, 03 Dec 2021 21:00:17 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5872a387705493894041a0e0d185f7b63f35ba540ce218ce8a3a93f95139b77f`  
		Last Modified: Fri, 03 Dec 2021 21:00:17 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18ed072c9481ea2501ceb7126460fd9ed5efbfc1d82a60714d95c4780535d991`  
		Last Modified: Fri, 03 Dec 2021 21:00:17 GMT  
		Size: 5.2 KB (5225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f365d0250ccd4d7fe8466796da2ba876f11c83b4daddc69875dfc1a7033a79b0`  
		Last Modified: Fri, 03 Dec 2021 21:00:17 GMT  
		Size: 2.5 KB (2503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:12-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:c2c5faf2f199eb1abe110535577faa2262fb300d8d92907861ba0ff310dabde1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **826.0 MB (826035753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78f13512af2ef156fa16d62503f8cd4483448d6e15b959fcb2dfa4015f230659`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 02 Dec 2021 08:07:54 GMT
ADD file:998dc1c35eeeed1ddf46156aeb337fb9b8cbb4855caf994201167a1061f4ecbf in / 
# Thu, 02 Dec 2021 08:07:55 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 09:53:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 09:53:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Dec 2021 09:53:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:07:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:07:23 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 02 Dec 2021 11:07:24 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 02 Dec 2021 11:07:25 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 11:07:26 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 11:07:27 GMT
ENV JAVA_VERSION=11.0.13
# Thu, 02 Dec 2021 11:07:49 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_x64_linux_11.0.13_8.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_aarch64_linux_11.0.13_8.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 02 Dec 2021 11:07:50 GMT
CMD ["jshell"]
# Fri, 03 Dec 2021 10:33:28 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Dec 2021 10:33:28 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Dec 2021 10:33:30 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 03 Dec 2021 10:33:30 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Dec 2021 10:33:31 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 10:33:32 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 10:54:19 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 03 Dec 2021 10:54:20 GMT
ENV TOMCAT_MAJOR=9
# Fri, 03 Dec 2021 10:54:21 GMT
ENV TOMCAT_VERSION=9.0.55
# Fri, 03 Dec 2021 10:54:22 GMT
ENV TOMCAT_SHA512=a0c480b8bba09069bda3b57f54e658450a59d799474ad587dead0ffbf5074c16ee3f9f9c13312d0ff3227c7034589dabf25941fbd672838e9baeee9661e024dc
# Fri, 03 Dec 2021 10:54:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 03 Dec 2021 10:54:45 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 03 Dec 2021 10:54:45 GMT
EXPOSE 8080
# Fri, 03 Dec 2021 10:54:46 GMT
CMD ["catalina.sh" "run"]
# Fri, 03 Dec 2021 16:34:04 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 03 Dec 2021 16:34:05 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 16:34:05 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 16:34:06 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 03 Dec 2021 16:34:07 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 03 Dec 2021 16:34:08 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 03 Dec 2021 16:34:43 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 16:34:44 GMT
ENV XWIKI_VERSION=12.10.10
# Fri, 03 Dec 2021 16:34:45 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.10
# Fri, 03 Dec 2021 16:34:46 GMT
ENV XWIKI_DOWNLOAD_SHA256=42364fd6a3d575c78969ebb12a7d28360ccff3b478379cf30232d6611ccbe9e0
# Fri, 03 Dec 2021 16:36:07 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 03 Dec 2021 16:36:09 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 03 Dec 2021 16:36:10 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 03 Dec 2021 16:36:11 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 03 Dec 2021 16:36:12 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 03 Dec 2021 16:36:14 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 03 Dec 2021 16:36:15 GMT
VOLUME [/usr/local/xwiki]
# Fri, 03 Dec 2021 16:36:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Dec 2021 16:36:16 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:6476cb406b24c94f24348db05d154b814b14ee38860dea1625080e7e08295a80`  
		Last Modified: Thu, 02 Dec 2021 08:40:14 GMT  
		Size: 53.6 MB (53619027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96565d527970b1cc982493f96d6b317b1fbfdd7bf0ea6fd58d44942bb4f597c5`  
		Last Modified: Thu, 02 Dec 2021 10:02:24 GMT  
		Size: 4.9 MB (4937631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8c15f93136056df893ba8088992a38e90dc37210fd6ebb712413fd045c58de`  
		Last Modified: Thu, 02 Dec 2021 10:02:25 GMT  
		Size: 10.7 MB (10655914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee42e24e52cb2f9b50ab14328865298f5ae6ac159219db890afc6366ec641a46`  
		Last Modified: Thu, 02 Dec 2021 10:02:46 GMT  
		Size: 54.7 MB (54669690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1ddc61edfde0dfa7da5e868dfebc0df6e44b7c94700ae79892d861abc32f97`  
		Last Modified: Thu, 02 Dec 2021 11:31:06 GMT  
		Size: 5.4 MB (5420180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:804b3e7e3a2930efff5c50600a2c162b8f2af073ec54a3c44314cc36e68d1a75`  
		Last Modified: Thu, 02 Dec 2021 11:31:05 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c15c25e9529bccafc0b750eb33fb972a05d42a09303dc760b67f89ea21b0bce0`  
		Last Modified: Thu, 02 Dec 2021 11:31:26 GMT  
		Size: 200.7 MB (200712890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac1b17d7ee052527ef86a2354f093548ac170d6d3318a79fa9916fd616c2c40f`  
		Last Modified: Fri, 03 Dec 2021 11:33:43 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8926fc06c65e9a17e2a3110e422fbebb73f63463202846b0b6addc004fd06d`  
		Last Modified: Fri, 03 Dec 2021 11:49:18 GMT  
		Size: 12.3 MB (12292070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56905cdb16153e42e333c2819b26aec2f74860d5924cbe3cf1952f737953c4d`  
		Last Modified: Fri, 03 Dec 2021 16:37:29 GMT  
		Size: 185.2 MB (185204101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b630d0a06c79c04946d7044a763e8bcfa3048eba1ee5917c5d73fbfc202e1cfd`  
		Last Modified: Fri, 03 Dec 2021 16:37:26 GMT  
		Size: 297.7 MB (297666166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c967f3c4012d8a61def666f59f0bb438b973b040c024ca5c194f0bc0f9ac33d1`  
		Last Modified: Fri, 03 Dec 2021 16:37:03 GMT  
		Size: 846.2 KB (846206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e42a536c4ff68942cbe6d89a2a025d4ff95d2d9c502e704b6e3981f2165b1b41`  
		Last Modified: Fri, 03 Dec 2021 16:37:03 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75dec884c2231050cbed8f6719547b3af625afb7df02cc793a7435570a75c981`  
		Last Modified: Fri, 03 Dec 2021 16:37:03 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2481f87da9b8547832e3c87fbe6f23b1e2a9a244bb522970461f859e242e089`  
		Last Modified: Fri, 03 Dec 2021 16:37:03 GMT  
		Size: 5.2 KB (5224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fac7412501c0d3bf5e64c52bf821fbae7b3be8223bc771b9b01062f15e73f60`  
		Last Modified: Fri, 03 Dec 2021 16:37:03 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:12.10`

```console
$ docker pull xwiki@sha256:0c452bd65de374236c5c106311276ae850620d39c3d6a8a225b5a6883d2eaf9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:12.10` - linux; amd64

```console
$ docker pull xwiki@sha256:bc8aaceaa6d467495242300c981dd77491cea326c58f7385481125a224888af2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.9 MB (835934777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daf03bf371ed121b6f8890ce6bebb499d4cfa8314d1de1f32552e4f86d0582f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:07 GMT
ADD file:e777355768c63f735e5458c7e0ada7f556f27d0493b3af35dc7c34f9c4294ea9 in / 
# Thu, 02 Dec 2021 02:48:08 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:39:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Dec 2021 03:40:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:34:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:34:20 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 02 Dec 2021 11:34:22 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 02 Dec 2021 11:34:22 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 11:34:22 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 11:34:23 GMT
ENV JAVA_VERSION=11.0.13
# Thu, 02 Dec 2021 11:34:48 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_x64_linux_11.0.13_8.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_aarch64_linux_11.0.13_8.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 02 Dec 2021 11:34:49 GMT
CMD ["jshell"]
# Fri, 03 Dec 2021 14:11:49 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Dec 2021 14:11:50 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Dec 2021 14:11:50 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 03 Dec 2021 14:11:51 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Dec 2021 14:11:51 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 14:11:51 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 14:27:34 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 03 Dec 2021 14:27:34 GMT
ENV TOMCAT_MAJOR=9
# Fri, 03 Dec 2021 14:27:34 GMT
ENV TOMCAT_VERSION=9.0.55
# Fri, 03 Dec 2021 14:27:35 GMT
ENV TOMCAT_SHA512=a0c480b8bba09069bda3b57f54e658450a59d799474ad587dead0ffbf5074c16ee3f9f9c13312d0ff3227c7034589dabf25941fbd672838e9baeee9661e024dc
# Fri, 03 Dec 2021 14:28:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 03 Dec 2021 14:28:03 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 03 Dec 2021 14:28:03 GMT
EXPOSE 8080
# Fri, 03 Dec 2021 14:28:03 GMT
CMD ["catalina.sh" "run"]
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 03 Dec 2021 20:52:45 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 20:54:56 GMT
ENV XWIKI_VERSION=12.10.10
# Fri, 03 Dec 2021 20:54:56 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.10
# Fri, 03 Dec 2021 20:54:56 GMT
ENV XWIKI_DOWNLOAD_SHA256=42364fd6a3d575c78969ebb12a7d28360ccff3b478379cf30232d6611ccbe9e0
# Fri, 03 Dec 2021 20:55:45 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 03 Dec 2021 20:55:46 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Fri, 03 Dec 2021 20:55:46 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Fri, 03 Dec 2021 20:55:46 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Fri, 03 Dec 2021 20:55:46 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Fri, 03 Dec 2021 20:55:46 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Fri, 03 Dec 2021 20:55:47 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 03 Dec 2021 20:55:48 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 03 Dec 2021 20:55:48 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 03 Dec 2021 20:55:49 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 03 Dec 2021 20:55:49 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 03 Dec 2021 20:55:49 GMT
VOLUME [/usr/local/xwiki]
# Fri, 03 Dec 2021 20:55:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Dec 2021 20:55:49 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:5e0b432e8ba9d9029a000e627840b98ffc1ed0c5172075b7d3e869be0df0fe9b`  
		Last Modified: Thu, 02 Dec 2021 02:53:18 GMT  
		Size: 54.9 MB (54932878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84cfd68b5cea612a8343c346bfa5bd6c486769010d12f7ec86b23c74887feb2`  
		Last Modified: Thu, 02 Dec 2021 03:49:22 GMT  
		Size: 5.2 MB (5153424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b8f2315954535f1e27cd13d777e73da4a787b0aebf4241d225beff3c91cbb1`  
		Last Modified: Thu, 02 Dec 2021 03:49:23 GMT  
		Size: 10.9 MB (10871995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0598fa43a7e793a76c198e8d45d8810394e1cfc943b2673d7fcf5a6fdc4f45b3`  
		Last Modified: Thu, 02 Dec 2021 03:49:46 GMT  
		Size: 54.6 MB (54567844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d35e3be804184359e0904389b149de16f159e30436d7a8a970aef67a4d155b`  
		Last Modified: Thu, 02 Dec 2021 11:54:46 GMT  
		Size: 5.4 MB (5420076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc448a0c88bee4d3cf6a928aa2b4cf499f4cb05034093c581342d414188a566`  
		Last Modified: Thu, 02 Dec 2021 11:54:45 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbdff6e5955b8bcd2e24b1a49fa4ec593ad333133c52911832aa2a7893f542da`  
		Last Modified: Thu, 02 Dec 2021 11:55:04 GMT  
		Size: 203.1 MB (203118915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5daf3771e3d8c27aa89cbcfef659790a2218e319899d49fbccde199e1780a5ef`  
		Last Modified: Fri, 03 Dec 2021 14:54:53 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5434ab540d864811e12dac3650eb0bc67bc8f6d7a6cb1f3c832e2c078c45302c`  
		Last Modified: Fri, 03 Dec 2021 15:08:17 GMT  
		Size: 12.5 MB (12523151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f43f4b2f615c39e867b3110fbc83f1d8fa2b72e4788cdcc91ea5dd73e97102`  
		Last Modified: Fri, 03 Dec 2021 15:08:16 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb64e66bc904d2f87948ce847a95dfa536c19132b599dc7f18ee2fec72ce7a8`  
		Last Modified: Fri, 03 Dec 2021 20:57:50 GMT  
		Size: 189.4 MB (189410805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:322c3fa9aeb088d28eaf87bee8cc347dd2446ec513406bfcc94fe921c47ef232`  
		Last Modified: Fri, 03 Dec 2021 20:59:42 GMT  
		Size: 297.7 MB (297665996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90fcdaa3c2b3eab89db62dbbc268566389c9d3aeca137f15cbdb15b0d7eaffe9`  
		Last Modified: Fri, 03 Dec 2021 20:59:25 GMT  
		Size: 2.3 MB (2257807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d51c8a2c6527bec03b855db0bdb4b58452c4af299cc4f40fc1690573eedb2676`  
		Last Modified: Fri, 03 Dec 2021 20:59:25 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56b515d1801ae6cbeea27c7f418568eb18e5310be586bb180e59cb2ddb54b41c`  
		Last Modified: Fri, 03 Dec 2021 20:59:25 GMT  
		Size: 2.3 KB (2303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9098d697724f1d37cb1cbc0032ca0057920efbebe8ff19f8391d8b88182881b6`  
		Last Modified: Fri, 03 Dec 2021 20:59:25 GMT  
		Size: 5.2 KB (5224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00faacd3e28eae83a4d5fa60009ec43904a971ad076d496b8ba65a2cc6331f3e`  
		Last Modified: Fri, 03 Dec 2021 20:59:25 GMT  
		Size: 2.5 KB (2501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:12.10-mysql-tomcat`

```console
$ docker pull xwiki@sha256:0c452bd65de374236c5c106311276ae850620d39c3d6a8a225b5a6883d2eaf9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:12.10-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:bc8aaceaa6d467495242300c981dd77491cea326c58f7385481125a224888af2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.9 MB (835934777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daf03bf371ed121b6f8890ce6bebb499d4cfa8314d1de1f32552e4f86d0582f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:07 GMT
ADD file:e777355768c63f735e5458c7e0ada7f556f27d0493b3af35dc7c34f9c4294ea9 in / 
# Thu, 02 Dec 2021 02:48:08 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:39:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Dec 2021 03:40:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:34:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:34:20 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 02 Dec 2021 11:34:22 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 02 Dec 2021 11:34:22 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 11:34:22 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 11:34:23 GMT
ENV JAVA_VERSION=11.0.13
# Thu, 02 Dec 2021 11:34:48 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_x64_linux_11.0.13_8.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_aarch64_linux_11.0.13_8.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 02 Dec 2021 11:34:49 GMT
CMD ["jshell"]
# Fri, 03 Dec 2021 14:11:49 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Dec 2021 14:11:50 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Dec 2021 14:11:50 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 03 Dec 2021 14:11:51 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Dec 2021 14:11:51 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 14:11:51 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 14:27:34 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 03 Dec 2021 14:27:34 GMT
ENV TOMCAT_MAJOR=9
# Fri, 03 Dec 2021 14:27:34 GMT
ENV TOMCAT_VERSION=9.0.55
# Fri, 03 Dec 2021 14:27:35 GMT
ENV TOMCAT_SHA512=a0c480b8bba09069bda3b57f54e658450a59d799474ad587dead0ffbf5074c16ee3f9f9c13312d0ff3227c7034589dabf25941fbd672838e9baeee9661e024dc
# Fri, 03 Dec 2021 14:28:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 03 Dec 2021 14:28:03 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 03 Dec 2021 14:28:03 GMT
EXPOSE 8080
# Fri, 03 Dec 2021 14:28:03 GMT
CMD ["catalina.sh" "run"]
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 03 Dec 2021 20:52:45 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 20:54:56 GMT
ENV XWIKI_VERSION=12.10.10
# Fri, 03 Dec 2021 20:54:56 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.10
# Fri, 03 Dec 2021 20:54:56 GMT
ENV XWIKI_DOWNLOAD_SHA256=42364fd6a3d575c78969ebb12a7d28360ccff3b478379cf30232d6611ccbe9e0
# Fri, 03 Dec 2021 20:55:45 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 03 Dec 2021 20:55:46 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Fri, 03 Dec 2021 20:55:46 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Fri, 03 Dec 2021 20:55:46 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Fri, 03 Dec 2021 20:55:46 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Fri, 03 Dec 2021 20:55:46 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Fri, 03 Dec 2021 20:55:47 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 03 Dec 2021 20:55:48 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 03 Dec 2021 20:55:48 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 03 Dec 2021 20:55:49 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 03 Dec 2021 20:55:49 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 03 Dec 2021 20:55:49 GMT
VOLUME [/usr/local/xwiki]
# Fri, 03 Dec 2021 20:55:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Dec 2021 20:55:49 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:5e0b432e8ba9d9029a000e627840b98ffc1ed0c5172075b7d3e869be0df0fe9b`  
		Last Modified: Thu, 02 Dec 2021 02:53:18 GMT  
		Size: 54.9 MB (54932878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84cfd68b5cea612a8343c346bfa5bd6c486769010d12f7ec86b23c74887feb2`  
		Last Modified: Thu, 02 Dec 2021 03:49:22 GMT  
		Size: 5.2 MB (5153424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b8f2315954535f1e27cd13d777e73da4a787b0aebf4241d225beff3c91cbb1`  
		Last Modified: Thu, 02 Dec 2021 03:49:23 GMT  
		Size: 10.9 MB (10871995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0598fa43a7e793a76c198e8d45d8810394e1cfc943b2673d7fcf5a6fdc4f45b3`  
		Last Modified: Thu, 02 Dec 2021 03:49:46 GMT  
		Size: 54.6 MB (54567844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d35e3be804184359e0904389b149de16f159e30436d7a8a970aef67a4d155b`  
		Last Modified: Thu, 02 Dec 2021 11:54:46 GMT  
		Size: 5.4 MB (5420076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc448a0c88bee4d3cf6a928aa2b4cf499f4cb05034093c581342d414188a566`  
		Last Modified: Thu, 02 Dec 2021 11:54:45 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbdff6e5955b8bcd2e24b1a49fa4ec593ad333133c52911832aa2a7893f542da`  
		Last Modified: Thu, 02 Dec 2021 11:55:04 GMT  
		Size: 203.1 MB (203118915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5daf3771e3d8c27aa89cbcfef659790a2218e319899d49fbccde199e1780a5ef`  
		Last Modified: Fri, 03 Dec 2021 14:54:53 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5434ab540d864811e12dac3650eb0bc67bc8f6d7a6cb1f3c832e2c078c45302c`  
		Last Modified: Fri, 03 Dec 2021 15:08:17 GMT  
		Size: 12.5 MB (12523151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f43f4b2f615c39e867b3110fbc83f1d8fa2b72e4788cdcc91ea5dd73e97102`  
		Last Modified: Fri, 03 Dec 2021 15:08:16 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb64e66bc904d2f87948ce847a95dfa536c19132b599dc7f18ee2fec72ce7a8`  
		Last Modified: Fri, 03 Dec 2021 20:57:50 GMT  
		Size: 189.4 MB (189410805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:322c3fa9aeb088d28eaf87bee8cc347dd2446ec513406bfcc94fe921c47ef232`  
		Last Modified: Fri, 03 Dec 2021 20:59:42 GMT  
		Size: 297.7 MB (297665996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90fcdaa3c2b3eab89db62dbbc268566389c9d3aeca137f15cbdb15b0d7eaffe9`  
		Last Modified: Fri, 03 Dec 2021 20:59:25 GMT  
		Size: 2.3 MB (2257807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d51c8a2c6527bec03b855db0bdb4b58452c4af299cc4f40fc1690573eedb2676`  
		Last Modified: Fri, 03 Dec 2021 20:59:25 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56b515d1801ae6cbeea27c7f418568eb18e5310be586bb180e59cb2ddb54b41c`  
		Last Modified: Fri, 03 Dec 2021 20:59:25 GMT  
		Size: 2.3 KB (2303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9098d697724f1d37cb1cbc0032ca0057920efbebe8ff19f8391d8b88182881b6`  
		Last Modified: Fri, 03 Dec 2021 20:59:25 GMT  
		Size: 5.2 KB (5224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00faacd3e28eae83a4d5fa60009ec43904a971ad076d496b8ba65a2cc6331f3e`  
		Last Modified: Fri, 03 Dec 2021 20:59:25 GMT  
		Size: 2.5 KB (2501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:12.10-postgres-tomcat`

```console
$ docker pull xwiki@sha256:33059b78ebe52d5089e0f0d0228b20ee00e97884213ea98e79d3c23d0265a18e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:12.10-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:b6da64a702495f77148d7907115512347ed792c3e13745f700877be9196acfaf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.4 MB (835398749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8000205aad7fbc2729bde9231f8618248a910cad7dc4c0f6ecc6c3f82ab0f7e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:07 GMT
ADD file:e777355768c63f735e5458c7e0ada7f556f27d0493b3af35dc7c34f9c4294ea9 in / 
# Thu, 02 Dec 2021 02:48:08 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:39:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Dec 2021 03:40:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:34:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:34:20 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 02 Dec 2021 11:34:22 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 02 Dec 2021 11:34:22 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 11:34:22 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 11:34:23 GMT
ENV JAVA_VERSION=11.0.13
# Thu, 02 Dec 2021 11:34:48 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_x64_linux_11.0.13_8.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_aarch64_linux_11.0.13_8.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 02 Dec 2021 11:34:49 GMT
CMD ["jshell"]
# Fri, 03 Dec 2021 14:11:49 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Dec 2021 14:11:50 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Dec 2021 14:11:50 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 03 Dec 2021 14:11:51 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Dec 2021 14:11:51 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 14:11:51 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 14:27:34 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 03 Dec 2021 14:27:34 GMT
ENV TOMCAT_MAJOR=9
# Fri, 03 Dec 2021 14:27:34 GMT
ENV TOMCAT_VERSION=9.0.55
# Fri, 03 Dec 2021 14:27:35 GMT
ENV TOMCAT_SHA512=a0c480b8bba09069bda3b57f54e658450a59d799474ad587dead0ffbf5074c16ee3f9f9c13312d0ff3227c7034589dabf25941fbd672838e9baeee9661e024dc
# Fri, 03 Dec 2021 14:28:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 03 Dec 2021 14:28:03 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 03 Dec 2021 14:28:03 GMT
EXPOSE 8080
# Fri, 03 Dec 2021 14:28:03 GMT
CMD ["catalina.sh" "run"]
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 03 Dec 2021 20:54:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 20:55:53 GMT
ENV XWIKI_VERSION=12.10.10
# Fri, 03 Dec 2021 20:55:53 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.10
# Fri, 03 Dec 2021 20:55:53 GMT
ENV XWIKI_DOWNLOAD_SHA256=42364fd6a3d575c78969ebb12a7d28360ccff3b478379cf30232d6611ccbe9e0
# Fri, 03 Dec 2021 20:56:32 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 03 Dec 2021 20:56:34 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 03 Dec 2021 20:56:34 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 03 Dec 2021 20:56:34 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 03 Dec 2021 20:56:35 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 03 Dec 2021 20:56:35 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 03 Dec 2021 20:56:36 GMT
VOLUME [/usr/local/xwiki]
# Fri, 03 Dec 2021 20:56:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Dec 2021 20:56:36 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:5e0b432e8ba9d9029a000e627840b98ffc1ed0c5172075b7d3e869be0df0fe9b`  
		Last Modified: Thu, 02 Dec 2021 02:53:18 GMT  
		Size: 54.9 MB (54932878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84cfd68b5cea612a8343c346bfa5bd6c486769010d12f7ec86b23c74887feb2`  
		Last Modified: Thu, 02 Dec 2021 03:49:22 GMT  
		Size: 5.2 MB (5153424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b8f2315954535f1e27cd13d777e73da4a787b0aebf4241d225beff3c91cbb1`  
		Last Modified: Thu, 02 Dec 2021 03:49:23 GMT  
		Size: 10.9 MB (10871995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0598fa43a7e793a76c198e8d45d8810394e1cfc943b2673d7fcf5a6fdc4f45b3`  
		Last Modified: Thu, 02 Dec 2021 03:49:46 GMT  
		Size: 54.6 MB (54567844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d35e3be804184359e0904389b149de16f159e30436d7a8a970aef67a4d155b`  
		Last Modified: Thu, 02 Dec 2021 11:54:46 GMT  
		Size: 5.4 MB (5420076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc448a0c88bee4d3cf6a928aa2b4cf499f4cb05034093c581342d414188a566`  
		Last Modified: Thu, 02 Dec 2021 11:54:45 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbdff6e5955b8bcd2e24b1a49fa4ec593ad333133c52911832aa2a7893f542da`  
		Last Modified: Thu, 02 Dec 2021 11:55:04 GMT  
		Size: 203.1 MB (203118915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5daf3771e3d8c27aa89cbcfef659790a2218e319899d49fbccde199e1780a5ef`  
		Last Modified: Fri, 03 Dec 2021 14:54:53 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5434ab540d864811e12dac3650eb0bc67bc8f6d7a6cb1f3c832e2c078c45302c`  
		Last Modified: Fri, 03 Dec 2021 15:08:17 GMT  
		Size: 12.5 MB (12523151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f43f4b2f615c39e867b3110fbc83f1d8fa2b72e4788cdcc91ea5dd73e97102`  
		Last Modified: Fri, 03 Dec 2021 15:08:16 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c96c2f945ecec7eda758824db2032432765e7a0128ef11d3c1841ac2dc2e5d95`  
		Last Modified: Fri, 03 Dec 2021 20:59:00 GMT  
		Size: 190.3 MB (190286185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98dd220d8d99ab2f82e0c4d98e1eda554b20e4cdd518e4863383ad47a2ede008`  
		Last Modified: Fri, 03 Dec 2021 21:00:34 GMT  
		Size: 297.7 MB (297666042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68c6a4d55d8aedc737c28c16053a45f219463db9f442fd0139d5dd559732b8dc`  
		Last Modified: Fri, 03 Dec 2021 21:00:17 GMT  
		Size: 846.2 KB (846205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68bf6e53b283f66ee03293c481736522efbf14497b1b2e32a0f7df3b5a68f310`  
		Last Modified: Fri, 03 Dec 2021 21:00:17 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5872a387705493894041a0e0d185f7b63f35ba540ce218ce8a3a93f95139b77f`  
		Last Modified: Fri, 03 Dec 2021 21:00:17 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18ed072c9481ea2501ceb7126460fd9ed5efbfc1d82a60714d95c4780535d991`  
		Last Modified: Fri, 03 Dec 2021 21:00:17 GMT  
		Size: 5.2 KB (5225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f365d0250ccd4d7fe8466796da2ba876f11c83b4daddc69875dfc1a7033a79b0`  
		Last Modified: Fri, 03 Dec 2021 21:00:17 GMT  
		Size: 2.5 KB (2503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:12.10-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:c2c5faf2f199eb1abe110535577faa2262fb300d8d92907861ba0ff310dabde1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **826.0 MB (826035753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78f13512af2ef156fa16d62503f8cd4483448d6e15b959fcb2dfa4015f230659`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 02 Dec 2021 08:07:54 GMT
ADD file:998dc1c35eeeed1ddf46156aeb337fb9b8cbb4855caf994201167a1061f4ecbf in / 
# Thu, 02 Dec 2021 08:07:55 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 09:53:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 09:53:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Dec 2021 09:53:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:07:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:07:23 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 02 Dec 2021 11:07:24 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 02 Dec 2021 11:07:25 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 11:07:26 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 11:07:27 GMT
ENV JAVA_VERSION=11.0.13
# Thu, 02 Dec 2021 11:07:49 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_x64_linux_11.0.13_8.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_aarch64_linux_11.0.13_8.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 02 Dec 2021 11:07:50 GMT
CMD ["jshell"]
# Fri, 03 Dec 2021 10:33:28 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Dec 2021 10:33:28 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Dec 2021 10:33:30 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 03 Dec 2021 10:33:30 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Dec 2021 10:33:31 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 10:33:32 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 10:54:19 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 03 Dec 2021 10:54:20 GMT
ENV TOMCAT_MAJOR=9
# Fri, 03 Dec 2021 10:54:21 GMT
ENV TOMCAT_VERSION=9.0.55
# Fri, 03 Dec 2021 10:54:22 GMT
ENV TOMCAT_SHA512=a0c480b8bba09069bda3b57f54e658450a59d799474ad587dead0ffbf5074c16ee3f9f9c13312d0ff3227c7034589dabf25941fbd672838e9baeee9661e024dc
# Fri, 03 Dec 2021 10:54:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 03 Dec 2021 10:54:45 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 03 Dec 2021 10:54:45 GMT
EXPOSE 8080
# Fri, 03 Dec 2021 10:54:46 GMT
CMD ["catalina.sh" "run"]
# Fri, 03 Dec 2021 16:34:04 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 03 Dec 2021 16:34:05 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 16:34:05 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 16:34:06 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 03 Dec 2021 16:34:07 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 03 Dec 2021 16:34:08 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 03 Dec 2021 16:34:43 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 16:34:44 GMT
ENV XWIKI_VERSION=12.10.10
# Fri, 03 Dec 2021 16:34:45 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.10
# Fri, 03 Dec 2021 16:34:46 GMT
ENV XWIKI_DOWNLOAD_SHA256=42364fd6a3d575c78969ebb12a7d28360ccff3b478379cf30232d6611ccbe9e0
# Fri, 03 Dec 2021 16:36:07 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 03 Dec 2021 16:36:09 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 03 Dec 2021 16:36:10 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 03 Dec 2021 16:36:11 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 03 Dec 2021 16:36:12 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 03 Dec 2021 16:36:14 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 03 Dec 2021 16:36:15 GMT
VOLUME [/usr/local/xwiki]
# Fri, 03 Dec 2021 16:36:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Dec 2021 16:36:16 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:6476cb406b24c94f24348db05d154b814b14ee38860dea1625080e7e08295a80`  
		Last Modified: Thu, 02 Dec 2021 08:40:14 GMT  
		Size: 53.6 MB (53619027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96565d527970b1cc982493f96d6b317b1fbfdd7bf0ea6fd58d44942bb4f597c5`  
		Last Modified: Thu, 02 Dec 2021 10:02:24 GMT  
		Size: 4.9 MB (4937631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8c15f93136056df893ba8088992a38e90dc37210fd6ebb712413fd045c58de`  
		Last Modified: Thu, 02 Dec 2021 10:02:25 GMT  
		Size: 10.7 MB (10655914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee42e24e52cb2f9b50ab14328865298f5ae6ac159219db890afc6366ec641a46`  
		Last Modified: Thu, 02 Dec 2021 10:02:46 GMT  
		Size: 54.7 MB (54669690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1ddc61edfde0dfa7da5e868dfebc0df6e44b7c94700ae79892d861abc32f97`  
		Last Modified: Thu, 02 Dec 2021 11:31:06 GMT  
		Size: 5.4 MB (5420180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:804b3e7e3a2930efff5c50600a2c162b8f2af073ec54a3c44314cc36e68d1a75`  
		Last Modified: Thu, 02 Dec 2021 11:31:05 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c15c25e9529bccafc0b750eb33fb972a05d42a09303dc760b67f89ea21b0bce0`  
		Last Modified: Thu, 02 Dec 2021 11:31:26 GMT  
		Size: 200.7 MB (200712890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac1b17d7ee052527ef86a2354f093548ac170d6d3318a79fa9916fd616c2c40f`  
		Last Modified: Fri, 03 Dec 2021 11:33:43 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8926fc06c65e9a17e2a3110e422fbebb73f63463202846b0b6addc004fd06d`  
		Last Modified: Fri, 03 Dec 2021 11:49:18 GMT  
		Size: 12.3 MB (12292070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56905cdb16153e42e333c2819b26aec2f74860d5924cbe3cf1952f737953c4d`  
		Last Modified: Fri, 03 Dec 2021 16:37:29 GMT  
		Size: 185.2 MB (185204101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b630d0a06c79c04946d7044a763e8bcfa3048eba1ee5917c5d73fbfc202e1cfd`  
		Last Modified: Fri, 03 Dec 2021 16:37:26 GMT  
		Size: 297.7 MB (297666166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c967f3c4012d8a61def666f59f0bb438b973b040c024ca5c194f0bc0f9ac33d1`  
		Last Modified: Fri, 03 Dec 2021 16:37:03 GMT  
		Size: 846.2 KB (846206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e42a536c4ff68942cbe6d89a2a025d4ff95d2d9c502e704b6e3981f2165b1b41`  
		Last Modified: Fri, 03 Dec 2021 16:37:03 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75dec884c2231050cbed8f6719547b3af625afb7df02cc793a7435570a75c981`  
		Last Modified: Fri, 03 Dec 2021 16:37:03 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2481f87da9b8547832e3c87fbe6f23b1e2a9a244bb522970461f859e242e089`  
		Last Modified: Fri, 03 Dec 2021 16:37:03 GMT  
		Size: 5.2 KB (5224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fac7412501c0d3bf5e64c52bf821fbae7b3be8223bc771b9b01062f15e73f60`  
		Last Modified: Fri, 03 Dec 2021 16:37:03 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:12.10.10`

```console
$ docker pull xwiki@sha256:0c452bd65de374236c5c106311276ae850620d39c3d6a8a225b5a6883d2eaf9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:12.10.10` - linux; amd64

```console
$ docker pull xwiki@sha256:bc8aaceaa6d467495242300c981dd77491cea326c58f7385481125a224888af2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.9 MB (835934777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daf03bf371ed121b6f8890ce6bebb499d4cfa8314d1de1f32552e4f86d0582f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:07 GMT
ADD file:e777355768c63f735e5458c7e0ada7f556f27d0493b3af35dc7c34f9c4294ea9 in / 
# Thu, 02 Dec 2021 02:48:08 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:39:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Dec 2021 03:40:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:34:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:34:20 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 02 Dec 2021 11:34:22 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 02 Dec 2021 11:34:22 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 11:34:22 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 11:34:23 GMT
ENV JAVA_VERSION=11.0.13
# Thu, 02 Dec 2021 11:34:48 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_x64_linux_11.0.13_8.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_aarch64_linux_11.0.13_8.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 02 Dec 2021 11:34:49 GMT
CMD ["jshell"]
# Fri, 03 Dec 2021 14:11:49 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Dec 2021 14:11:50 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Dec 2021 14:11:50 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 03 Dec 2021 14:11:51 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Dec 2021 14:11:51 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 14:11:51 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 14:27:34 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 03 Dec 2021 14:27:34 GMT
ENV TOMCAT_MAJOR=9
# Fri, 03 Dec 2021 14:27:34 GMT
ENV TOMCAT_VERSION=9.0.55
# Fri, 03 Dec 2021 14:27:35 GMT
ENV TOMCAT_SHA512=a0c480b8bba09069bda3b57f54e658450a59d799474ad587dead0ffbf5074c16ee3f9f9c13312d0ff3227c7034589dabf25941fbd672838e9baeee9661e024dc
# Fri, 03 Dec 2021 14:28:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 03 Dec 2021 14:28:03 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 03 Dec 2021 14:28:03 GMT
EXPOSE 8080
# Fri, 03 Dec 2021 14:28:03 GMT
CMD ["catalina.sh" "run"]
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 03 Dec 2021 20:52:45 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 20:54:56 GMT
ENV XWIKI_VERSION=12.10.10
# Fri, 03 Dec 2021 20:54:56 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.10
# Fri, 03 Dec 2021 20:54:56 GMT
ENV XWIKI_DOWNLOAD_SHA256=42364fd6a3d575c78969ebb12a7d28360ccff3b478379cf30232d6611ccbe9e0
# Fri, 03 Dec 2021 20:55:45 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 03 Dec 2021 20:55:46 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Fri, 03 Dec 2021 20:55:46 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Fri, 03 Dec 2021 20:55:46 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Fri, 03 Dec 2021 20:55:46 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Fri, 03 Dec 2021 20:55:46 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Fri, 03 Dec 2021 20:55:47 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 03 Dec 2021 20:55:48 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 03 Dec 2021 20:55:48 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 03 Dec 2021 20:55:49 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 03 Dec 2021 20:55:49 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 03 Dec 2021 20:55:49 GMT
VOLUME [/usr/local/xwiki]
# Fri, 03 Dec 2021 20:55:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Dec 2021 20:55:49 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:5e0b432e8ba9d9029a000e627840b98ffc1ed0c5172075b7d3e869be0df0fe9b`  
		Last Modified: Thu, 02 Dec 2021 02:53:18 GMT  
		Size: 54.9 MB (54932878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84cfd68b5cea612a8343c346bfa5bd6c486769010d12f7ec86b23c74887feb2`  
		Last Modified: Thu, 02 Dec 2021 03:49:22 GMT  
		Size: 5.2 MB (5153424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b8f2315954535f1e27cd13d777e73da4a787b0aebf4241d225beff3c91cbb1`  
		Last Modified: Thu, 02 Dec 2021 03:49:23 GMT  
		Size: 10.9 MB (10871995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0598fa43a7e793a76c198e8d45d8810394e1cfc943b2673d7fcf5a6fdc4f45b3`  
		Last Modified: Thu, 02 Dec 2021 03:49:46 GMT  
		Size: 54.6 MB (54567844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d35e3be804184359e0904389b149de16f159e30436d7a8a970aef67a4d155b`  
		Last Modified: Thu, 02 Dec 2021 11:54:46 GMT  
		Size: 5.4 MB (5420076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc448a0c88bee4d3cf6a928aa2b4cf499f4cb05034093c581342d414188a566`  
		Last Modified: Thu, 02 Dec 2021 11:54:45 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbdff6e5955b8bcd2e24b1a49fa4ec593ad333133c52911832aa2a7893f542da`  
		Last Modified: Thu, 02 Dec 2021 11:55:04 GMT  
		Size: 203.1 MB (203118915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5daf3771e3d8c27aa89cbcfef659790a2218e319899d49fbccde199e1780a5ef`  
		Last Modified: Fri, 03 Dec 2021 14:54:53 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5434ab540d864811e12dac3650eb0bc67bc8f6d7a6cb1f3c832e2c078c45302c`  
		Last Modified: Fri, 03 Dec 2021 15:08:17 GMT  
		Size: 12.5 MB (12523151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f43f4b2f615c39e867b3110fbc83f1d8fa2b72e4788cdcc91ea5dd73e97102`  
		Last Modified: Fri, 03 Dec 2021 15:08:16 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb64e66bc904d2f87948ce847a95dfa536c19132b599dc7f18ee2fec72ce7a8`  
		Last Modified: Fri, 03 Dec 2021 20:57:50 GMT  
		Size: 189.4 MB (189410805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:322c3fa9aeb088d28eaf87bee8cc347dd2446ec513406bfcc94fe921c47ef232`  
		Last Modified: Fri, 03 Dec 2021 20:59:42 GMT  
		Size: 297.7 MB (297665996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90fcdaa3c2b3eab89db62dbbc268566389c9d3aeca137f15cbdb15b0d7eaffe9`  
		Last Modified: Fri, 03 Dec 2021 20:59:25 GMT  
		Size: 2.3 MB (2257807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d51c8a2c6527bec03b855db0bdb4b58452c4af299cc4f40fc1690573eedb2676`  
		Last Modified: Fri, 03 Dec 2021 20:59:25 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56b515d1801ae6cbeea27c7f418568eb18e5310be586bb180e59cb2ddb54b41c`  
		Last Modified: Fri, 03 Dec 2021 20:59:25 GMT  
		Size: 2.3 KB (2303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9098d697724f1d37cb1cbc0032ca0057920efbebe8ff19f8391d8b88182881b6`  
		Last Modified: Fri, 03 Dec 2021 20:59:25 GMT  
		Size: 5.2 KB (5224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00faacd3e28eae83a4d5fa60009ec43904a971ad076d496b8ba65a2cc6331f3e`  
		Last Modified: Fri, 03 Dec 2021 20:59:25 GMT  
		Size: 2.5 KB (2501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:12.10.10-mysql-tomcat`

```console
$ docker pull xwiki@sha256:0c452bd65de374236c5c106311276ae850620d39c3d6a8a225b5a6883d2eaf9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:12.10.10-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:bc8aaceaa6d467495242300c981dd77491cea326c58f7385481125a224888af2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.9 MB (835934777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daf03bf371ed121b6f8890ce6bebb499d4cfa8314d1de1f32552e4f86d0582f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:07 GMT
ADD file:e777355768c63f735e5458c7e0ada7f556f27d0493b3af35dc7c34f9c4294ea9 in / 
# Thu, 02 Dec 2021 02:48:08 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:39:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Dec 2021 03:40:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:34:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:34:20 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 02 Dec 2021 11:34:22 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 02 Dec 2021 11:34:22 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 11:34:22 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 11:34:23 GMT
ENV JAVA_VERSION=11.0.13
# Thu, 02 Dec 2021 11:34:48 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_x64_linux_11.0.13_8.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_aarch64_linux_11.0.13_8.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 02 Dec 2021 11:34:49 GMT
CMD ["jshell"]
# Fri, 03 Dec 2021 14:11:49 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Dec 2021 14:11:50 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Dec 2021 14:11:50 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 03 Dec 2021 14:11:51 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Dec 2021 14:11:51 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 14:11:51 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 14:27:34 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 03 Dec 2021 14:27:34 GMT
ENV TOMCAT_MAJOR=9
# Fri, 03 Dec 2021 14:27:34 GMT
ENV TOMCAT_VERSION=9.0.55
# Fri, 03 Dec 2021 14:27:35 GMT
ENV TOMCAT_SHA512=a0c480b8bba09069bda3b57f54e658450a59d799474ad587dead0ffbf5074c16ee3f9f9c13312d0ff3227c7034589dabf25941fbd672838e9baeee9661e024dc
# Fri, 03 Dec 2021 14:28:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 03 Dec 2021 14:28:03 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 03 Dec 2021 14:28:03 GMT
EXPOSE 8080
# Fri, 03 Dec 2021 14:28:03 GMT
CMD ["catalina.sh" "run"]
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 03 Dec 2021 20:52:45 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 20:54:56 GMT
ENV XWIKI_VERSION=12.10.10
# Fri, 03 Dec 2021 20:54:56 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.10
# Fri, 03 Dec 2021 20:54:56 GMT
ENV XWIKI_DOWNLOAD_SHA256=42364fd6a3d575c78969ebb12a7d28360ccff3b478379cf30232d6611ccbe9e0
# Fri, 03 Dec 2021 20:55:45 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 03 Dec 2021 20:55:46 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Fri, 03 Dec 2021 20:55:46 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Fri, 03 Dec 2021 20:55:46 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Fri, 03 Dec 2021 20:55:46 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Fri, 03 Dec 2021 20:55:46 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Fri, 03 Dec 2021 20:55:47 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 03 Dec 2021 20:55:48 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 03 Dec 2021 20:55:48 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 03 Dec 2021 20:55:49 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 03 Dec 2021 20:55:49 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 03 Dec 2021 20:55:49 GMT
VOLUME [/usr/local/xwiki]
# Fri, 03 Dec 2021 20:55:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Dec 2021 20:55:49 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:5e0b432e8ba9d9029a000e627840b98ffc1ed0c5172075b7d3e869be0df0fe9b`  
		Last Modified: Thu, 02 Dec 2021 02:53:18 GMT  
		Size: 54.9 MB (54932878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84cfd68b5cea612a8343c346bfa5bd6c486769010d12f7ec86b23c74887feb2`  
		Last Modified: Thu, 02 Dec 2021 03:49:22 GMT  
		Size: 5.2 MB (5153424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b8f2315954535f1e27cd13d777e73da4a787b0aebf4241d225beff3c91cbb1`  
		Last Modified: Thu, 02 Dec 2021 03:49:23 GMT  
		Size: 10.9 MB (10871995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0598fa43a7e793a76c198e8d45d8810394e1cfc943b2673d7fcf5a6fdc4f45b3`  
		Last Modified: Thu, 02 Dec 2021 03:49:46 GMT  
		Size: 54.6 MB (54567844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d35e3be804184359e0904389b149de16f159e30436d7a8a970aef67a4d155b`  
		Last Modified: Thu, 02 Dec 2021 11:54:46 GMT  
		Size: 5.4 MB (5420076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc448a0c88bee4d3cf6a928aa2b4cf499f4cb05034093c581342d414188a566`  
		Last Modified: Thu, 02 Dec 2021 11:54:45 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbdff6e5955b8bcd2e24b1a49fa4ec593ad333133c52911832aa2a7893f542da`  
		Last Modified: Thu, 02 Dec 2021 11:55:04 GMT  
		Size: 203.1 MB (203118915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5daf3771e3d8c27aa89cbcfef659790a2218e319899d49fbccde199e1780a5ef`  
		Last Modified: Fri, 03 Dec 2021 14:54:53 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5434ab540d864811e12dac3650eb0bc67bc8f6d7a6cb1f3c832e2c078c45302c`  
		Last Modified: Fri, 03 Dec 2021 15:08:17 GMT  
		Size: 12.5 MB (12523151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f43f4b2f615c39e867b3110fbc83f1d8fa2b72e4788cdcc91ea5dd73e97102`  
		Last Modified: Fri, 03 Dec 2021 15:08:16 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb64e66bc904d2f87948ce847a95dfa536c19132b599dc7f18ee2fec72ce7a8`  
		Last Modified: Fri, 03 Dec 2021 20:57:50 GMT  
		Size: 189.4 MB (189410805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:322c3fa9aeb088d28eaf87bee8cc347dd2446ec513406bfcc94fe921c47ef232`  
		Last Modified: Fri, 03 Dec 2021 20:59:42 GMT  
		Size: 297.7 MB (297665996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90fcdaa3c2b3eab89db62dbbc268566389c9d3aeca137f15cbdb15b0d7eaffe9`  
		Last Modified: Fri, 03 Dec 2021 20:59:25 GMT  
		Size: 2.3 MB (2257807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d51c8a2c6527bec03b855db0bdb4b58452c4af299cc4f40fc1690573eedb2676`  
		Last Modified: Fri, 03 Dec 2021 20:59:25 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56b515d1801ae6cbeea27c7f418568eb18e5310be586bb180e59cb2ddb54b41c`  
		Last Modified: Fri, 03 Dec 2021 20:59:25 GMT  
		Size: 2.3 KB (2303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9098d697724f1d37cb1cbc0032ca0057920efbebe8ff19f8391d8b88182881b6`  
		Last Modified: Fri, 03 Dec 2021 20:59:25 GMT  
		Size: 5.2 KB (5224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00faacd3e28eae83a4d5fa60009ec43904a971ad076d496b8ba65a2cc6331f3e`  
		Last Modified: Fri, 03 Dec 2021 20:59:25 GMT  
		Size: 2.5 KB (2501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:12.10.10-postgres-tomcat`

```console
$ docker pull xwiki@sha256:33059b78ebe52d5089e0f0d0228b20ee00e97884213ea98e79d3c23d0265a18e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:12.10.10-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:b6da64a702495f77148d7907115512347ed792c3e13745f700877be9196acfaf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.4 MB (835398749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8000205aad7fbc2729bde9231f8618248a910cad7dc4c0f6ecc6c3f82ab0f7e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:07 GMT
ADD file:e777355768c63f735e5458c7e0ada7f556f27d0493b3af35dc7c34f9c4294ea9 in / 
# Thu, 02 Dec 2021 02:48:08 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:39:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Dec 2021 03:40:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:34:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:34:20 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 02 Dec 2021 11:34:22 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 02 Dec 2021 11:34:22 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 11:34:22 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 11:34:23 GMT
ENV JAVA_VERSION=11.0.13
# Thu, 02 Dec 2021 11:34:48 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_x64_linux_11.0.13_8.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_aarch64_linux_11.0.13_8.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 02 Dec 2021 11:34:49 GMT
CMD ["jshell"]
# Fri, 03 Dec 2021 14:11:49 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Dec 2021 14:11:50 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Dec 2021 14:11:50 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 03 Dec 2021 14:11:51 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Dec 2021 14:11:51 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 14:11:51 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 14:27:34 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 03 Dec 2021 14:27:34 GMT
ENV TOMCAT_MAJOR=9
# Fri, 03 Dec 2021 14:27:34 GMT
ENV TOMCAT_VERSION=9.0.55
# Fri, 03 Dec 2021 14:27:35 GMT
ENV TOMCAT_SHA512=a0c480b8bba09069bda3b57f54e658450a59d799474ad587dead0ffbf5074c16ee3f9f9c13312d0ff3227c7034589dabf25941fbd672838e9baeee9661e024dc
# Fri, 03 Dec 2021 14:28:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 03 Dec 2021 14:28:03 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 03 Dec 2021 14:28:03 GMT
EXPOSE 8080
# Fri, 03 Dec 2021 14:28:03 GMT
CMD ["catalina.sh" "run"]
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 03 Dec 2021 20:54:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 20:55:53 GMT
ENV XWIKI_VERSION=12.10.10
# Fri, 03 Dec 2021 20:55:53 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.10
# Fri, 03 Dec 2021 20:55:53 GMT
ENV XWIKI_DOWNLOAD_SHA256=42364fd6a3d575c78969ebb12a7d28360ccff3b478379cf30232d6611ccbe9e0
# Fri, 03 Dec 2021 20:56:32 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 03 Dec 2021 20:56:34 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 03 Dec 2021 20:56:34 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 03 Dec 2021 20:56:34 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 03 Dec 2021 20:56:35 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 03 Dec 2021 20:56:35 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 03 Dec 2021 20:56:36 GMT
VOLUME [/usr/local/xwiki]
# Fri, 03 Dec 2021 20:56:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Dec 2021 20:56:36 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:5e0b432e8ba9d9029a000e627840b98ffc1ed0c5172075b7d3e869be0df0fe9b`  
		Last Modified: Thu, 02 Dec 2021 02:53:18 GMT  
		Size: 54.9 MB (54932878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84cfd68b5cea612a8343c346bfa5bd6c486769010d12f7ec86b23c74887feb2`  
		Last Modified: Thu, 02 Dec 2021 03:49:22 GMT  
		Size: 5.2 MB (5153424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b8f2315954535f1e27cd13d777e73da4a787b0aebf4241d225beff3c91cbb1`  
		Last Modified: Thu, 02 Dec 2021 03:49:23 GMT  
		Size: 10.9 MB (10871995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0598fa43a7e793a76c198e8d45d8810394e1cfc943b2673d7fcf5a6fdc4f45b3`  
		Last Modified: Thu, 02 Dec 2021 03:49:46 GMT  
		Size: 54.6 MB (54567844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d35e3be804184359e0904389b149de16f159e30436d7a8a970aef67a4d155b`  
		Last Modified: Thu, 02 Dec 2021 11:54:46 GMT  
		Size: 5.4 MB (5420076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc448a0c88bee4d3cf6a928aa2b4cf499f4cb05034093c581342d414188a566`  
		Last Modified: Thu, 02 Dec 2021 11:54:45 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbdff6e5955b8bcd2e24b1a49fa4ec593ad333133c52911832aa2a7893f542da`  
		Last Modified: Thu, 02 Dec 2021 11:55:04 GMT  
		Size: 203.1 MB (203118915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5daf3771e3d8c27aa89cbcfef659790a2218e319899d49fbccde199e1780a5ef`  
		Last Modified: Fri, 03 Dec 2021 14:54:53 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5434ab540d864811e12dac3650eb0bc67bc8f6d7a6cb1f3c832e2c078c45302c`  
		Last Modified: Fri, 03 Dec 2021 15:08:17 GMT  
		Size: 12.5 MB (12523151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f43f4b2f615c39e867b3110fbc83f1d8fa2b72e4788cdcc91ea5dd73e97102`  
		Last Modified: Fri, 03 Dec 2021 15:08:16 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c96c2f945ecec7eda758824db2032432765e7a0128ef11d3c1841ac2dc2e5d95`  
		Last Modified: Fri, 03 Dec 2021 20:59:00 GMT  
		Size: 190.3 MB (190286185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98dd220d8d99ab2f82e0c4d98e1eda554b20e4cdd518e4863383ad47a2ede008`  
		Last Modified: Fri, 03 Dec 2021 21:00:34 GMT  
		Size: 297.7 MB (297666042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68c6a4d55d8aedc737c28c16053a45f219463db9f442fd0139d5dd559732b8dc`  
		Last Modified: Fri, 03 Dec 2021 21:00:17 GMT  
		Size: 846.2 KB (846205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68bf6e53b283f66ee03293c481736522efbf14497b1b2e32a0f7df3b5a68f310`  
		Last Modified: Fri, 03 Dec 2021 21:00:17 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5872a387705493894041a0e0d185f7b63f35ba540ce218ce8a3a93f95139b77f`  
		Last Modified: Fri, 03 Dec 2021 21:00:17 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18ed072c9481ea2501ceb7126460fd9ed5efbfc1d82a60714d95c4780535d991`  
		Last Modified: Fri, 03 Dec 2021 21:00:17 GMT  
		Size: 5.2 KB (5225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f365d0250ccd4d7fe8466796da2ba876f11c83b4daddc69875dfc1a7033a79b0`  
		Last Modified: Fri, 03 Dec 2021 21:00:17 GMT  
		Size: 2.5 KB (2503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:12.10.10-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:c2c5faf2f199eb1abe110535577faa2262fb300d8d92907861ba0ff310dabde1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **826.0 MB (826035753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78f13512af2ef156fa16d62503f8cd4483448d6e15b959fcb2dfa4015f230659`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 02 Dec 2021 08:07:54 GMT
ADD file:998dc1c35eeeed1ddf46156aeb337fb9b8cbb4855caf994201167a1061f4ecbf in / 
# Thu, 02 Dec 2021 08:07:55 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 09:53:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 09:53:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Dec 2021 09:53:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:07:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:07:23 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 02 Dec 2021 11:07:24 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 02 Dec 2021 11:07:25 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 11:07:26 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 11:07:27 GMT
ENV JAVA_VERSION=11.0.13
# Thu, 02 Dec 2021 11:07:49 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_x64_linux_11.0.13_8.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_aarch64_linux_11.0.13_8.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 02 Dec 2021 11:07:50 GMT
CMD ["jshell"]
# Fri, 03 Dec 2021 10:33:28 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Dec 2021 10:33:28 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Dec 2021 10:33:30 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 03 Dec 2021 10:33:30 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Dec 2021 10:33:31 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 10:33:32 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 10:54:19 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 03 Dec 2021 10:54:20 GMT
ENV TOMCAT_MAJOR=9
# Fri, 03 Dec 2021 10:54:21 GMT
ENV TOMCAT_VERSION=9.0.55
# Fri, 03 Dec 2021 10:54:22 GMT
ENV TOMCAT_SHA512=a0c480b8bba09069bda3b57f54e658450a59d799474ad587dead0ffbf5074c16ee3f9f9c13312d0ff3227c7034589dabf25941fbd672838e9baeee9661e024dc
# Fri, 03 Dec 2021 10:54:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 03 Dec 2021 10:54:45 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 03 Dec 2021 10:54:45 GMT
EXPOSE 8080
# Fri, 03 Dec 2021 10:54:46 GMT
CMD ["catalina.sh" "run"]
# Fri, 03 Dec 2021 16:34:04 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 03 Dec 2021 16:34:05 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 16:34:05 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 16:34:06 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 03 Dec 2021 16:34:07 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 03 Dec 2021 16:34:08 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 03 Dec 2021 16:34:43 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 16:34:44 GMT
ENV XWIKI_VERSION=12.10.10
# Fri, 03 Dec 2021 16:34:45 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.10
# Fri, 03 Dec 2021 16:34:46 GMT
ENV XWIKI_DOWNLOAD_SHA256=42364fd6a3d575c78969ebb12a7d28360ccff3b478379cf30232d6611ccbe9e0
# Fri, 03 Dec 2021 16:36:07 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 03 Dec 2021 16:36:09 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 03 Dec 2021 16:36:10 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 03 Dec 2021 16:36:11 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 03 Dec 2021 16:36:12 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 03 Dec 2021 16:36:14 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 03 Dec 2021 16:36:15 GMT
VOLUME [/usr/local/xwiki]
# Fri, 03 Dec 2021 16:36:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Dec 2021 16:36:16 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:6476cb406b24c94f24348db05d154b814b14ee38860dea1625080e7e08295a80`  
		Last Modified: Thu, 02 Dec 2021 08:40:14 GMT  
		Size: 53.6 MB (53619027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96565d527970b1cc982493f96d6b317b1fbfdd7bf0ea6fd58d44942bb4f597c5`  
		Last Modified: Thu, 02 Dec 2021 10:02:24 GMT  
		Size: 4.9 MB (4937631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8c15f93136056df893ba8088992a38e90dc37210fd6ebb712413fd045c58de`  
		Last Modified: Thu, 02 Dec 2021 10:02:25 GMT  
		Size: 10.7 MB (10655914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee42e24e52cb2f9b50ab14328865298f5ae6ac159219db890afc6366ec641a46`  
		Last Modified: Thu, 02 Dec 2021 10:02:46 GMT  
		Size: 54.7 MB (54669690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1ddc61edfde0dfa7da5e868dfebc0df6e44b7c94700ae79892d861abc32f97`  
		Last Modified: Thu, 02 Dec 2021 11:31:06 GMT  
		Size: 5.4 MB (5420180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:804b3e7e3a2930efff5c50600a2c162b8f2af073ec54a3c44314cc36e68d1a75`  
		Last Modified: Thu, 02 Dec 2021 11:31:05 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c15c25e9529bccafc0b750eb33fb972a05d42a09303dc760b67f89ea21b0bce0`  
		Last Modified: Thu, 02 Dec 2021 11:31:26 GMT  
		Size: 200.7 MB (200712890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac1b17d7ee052527ef86a2354f093548ac170d6d3318a79fa9916fd616c2c40f`  
		Last Modified: Fri, 03 Dec 2021 11:33:43 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8926fc06c65e9a17e2a3110e422fbebb73f63463202846b0b6addc004fd06d`  
		Last Modified: Fri, 03 Dec 2021 11:49:18 GMT  
		Size: 12.3 MB (12292070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56905cdb16153e42e333c2819b26aec2f74860d5924cbe3cf1952f737953c4d`  
		Last Modified: Fri, 03 Dec 2021 16:37:29 GMT  
		Size: 185.2 MB (185204101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b630d0a06c79c04946d7044a763e8bcfa3048eba1ee5917c5d73fbfc202e1cfd`  
		Last Modified: Fri, 03 Dec 2021 16:37:26 GMT  
		Size: 297.7 MB (297666166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c967f3c4012d8a61def666f59f0bb438b973b040c024ca5c194f0bc0f9ac33d1`  
		Last Modified: Fri, 03 Dec 2021 16:37:03 GMT  
		Size: 846.2 KB (846206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e42a536c4ff68942cbe6d89a2a025d4ff95d2d9c502e704b6e3981f2165b1b41`  
		Last Modified: Fri, 03 Dec 2021 16:37:03 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75dec884c2231050cbed8f6719547b3af625afb7df02cc793a7435570a75c981`  
		Last Modified: Fri, 03 Dec 2021 16:37:03 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2481f87da9b8547832e3c87fbe6f23b1e2a9a244bb522970461f859e242e089`  
		Last Modified: Fri, 03 Dec 2021 16:37:03 GMT  
		Size: 5.2 KB (5224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fac7412501c0d3bf5e64c52bf821fbae7b3be8223bc771b9b01062f15e73f60`  
		Last Modified: Fri, 03 Dec 2021 16:37:03 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13`

```console
$ docker pull xwiki@sha256:f8be6bb37b7e4385597a7186a40f6d8bcde4f9c609d13f34149ace9ac4d5fdeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:13` - linux; amd64

```console
$ docker pull xwiki@sha256:7340a02a837d6d8a7751bb8369c2d9a97643fd4e2530e1bc0098f235933f1e3d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **830.7 MB (830657270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:696e0182c57281cf1de1eefe88fa5d95fde87e191f5464d26c10b3687b03fa51`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:07 GMT
ADD file:e777355768c63f735e5458c7e0ada7f556f27d0493b3af35dc7c34f9c4294ea9 in / 
# Thu, 02 Dec 2021 02:48:08 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:39:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Dec 2021 03:40:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:34:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:34:20 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 02 Dec 2021 11:34:22 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 02 Dec 2021 11:34:22 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 11:34:22 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 11:34:23 GMT
ENV JAVA_VERSION=11.0.13
# Thu, 02 Dec 2021 11:34:48 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_x64_linux_11.0.13_8.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_aarch64_linux_11.0.13_8.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 02 Dec 2021 11:34:49 GMT
CMD ["jshell"]
# Fri, 03 Dec 2021 14:11:49 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Dec 2021 14:11:50 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Dec 2021 14:11:50 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 03 Dec 2021 14:11:51 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Dec 2021 14:11:51 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 14:11:51 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 14:27:34 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 03 Dec 2021 14:27:34 GMT
ENV TOMCAT_MAJOR=9
# Fri, 03 Dec 2021 14:27:34 GMT
ENV TOMCAT_VERSION=9.0.55
# Fri, 03 Dec 2021 14:27:35 GMT
ENV TOMCAT_SHA512=a0c480b8bba09069bda3b57f54e658450a59d799474ad587dead0ffbf5074c16ee3f9f9c13312d0ff3227c7034589dabf25941fbd672838e9baeee9661e024dc
# Fri, 03 Dec 2021 14:28:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 03 Dec 2021 14:28:03 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 03 Dec 2021 14:28:03 GMT
EXPOSE 8080
# Fri, 03 Dec 2021 14:28:03 GMT
CMD ["catalina.sh" "run"]
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 03 Dec 2021 20:52:45 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 20:52:47 GMT
ENV XWIKI_VERSION=13.10
# Fri, 03 Dec 2021 20:52:47 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10
# Fri, 03 Dec 2021 20:52:47 GMT
ENV XWIKI_DOWNLOAD_SHA256=863455ef741ec70539ab89b9981790909f3319b626a107e62fa42c8797df032b
# Fri, 03 Dec 2021 20:53:24 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 03 Dec 2021 20:53:25 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Fri, 03 Dec 2021 20:53:25 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Fri, 03 Dec 2021 20:53:25 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Fri, 03 Dec 2021 20:53:25 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Fri, 03 Dec 2021 20:53:25 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Fri, 03 Dec 2021 20:53:26 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 03 Dec 2021 20:53:27 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 03 Dec 2021 20:53:27 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 03 Dec 2021 20:53:28 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 03 Dec 2021 20:53:28 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 03 Dec 2021 20:53:28 GMT
VOLUME [/usr/local/xwiki]
# Fri, 03 Dec 2021 20:53:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Dec 2021 20:53:29 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:5e0b432e8ba9d9029a000e627840b98ffc1ed0c5172075b7d3e869be0df0fe9b`  
		Last Modified: Thu, 02 Dec 2021 02:53:18 GMT  
		Size: 54.9 MB (54932878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84cfd68b5cea612a8343c346bfa5bd6c486769010d12f7ec86b23c74887feb2`  
		Last Modified: Thu, 02 Dec 2021 03:49:22 GMT  
		Size: 5.2 MB (5153424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b8f2315954535f1e27cd13d777e73da4a787b0aebf4241d225beff3c91cbb1`  
		Last Modified: Thu, 02 Dec 2021 03:49:23 GMT  
		Size: 10.9 MB (10871995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0598fa43a7e793a76c198e8d45d8810394e1cfc943b2673d7fcf5a6fdc4f45b3`  
		Last Modified: Thu, 02 Dec 2021 03:49:46 GMT  
		Size: 54.6 MB (54567844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d35e3be804184359e0904389b149de16f159e30436d7a8a970aef67a4d155b`  
		Last Modified: Thu, 02 Dec 2021 11:54:46 GMT  
		Size: 5.4 MB (5420076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc448a0c88bee4d3cf6a928aa2b4cf499f4cb05034093c581342d414188a566`  
		Last Modified: Thu, 02 Dec 2021 11:54:45 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbdff6e5955b8bcd2e24b1a49fa4ec593ad333133c52911832aa2a7893f542da`  
		Last Modified: Thu, 02 Dec 2021 11:55:04 GMT  
		Size: 203.1 MB (203118915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5daf3771e3d8c27aa89cbcfef659790a2218e319899d49fbccde199e1780a5ef`  
		Last Modified: Fri, 03 Dec 2021 14:54:53 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5434ab540d864811e12dac3650eb0bc67bc8f6d7a6cb1f3c832e2c078c45302c`  
		Last Modified: Fri, 03 Dec 2021 15:08:17 GMT  
		Size: 12.5 MB (12523151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f43f4b2f615c39e867b3110fbc83f1d8fa2b72e4788cdcc91ea5dd73e97102`  
		Last Modified: Fri, 03 Dec 2021 15:08:16 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb64e66bc904d2f87948ce847a95dfa536c19132b599dc7f18ee2fec72ce7a8`  
		Last Modified: Fri, 03 Dec 2021 20:57:50 GMT  
		Size: 189.4 MB (189410805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eda7eb7430a70eef3ce565f0ad28fd9afcc0377bc9ba457bf47563dcf4ca3f25`  
		Last Modified: Fri, 03 Dec 2021 20:57:41 GMT  
		Size: 292.4 MB (292388360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f5388154bcdeb77283073eb4e763658b195a0a27693e1e7c35365485f30f18`  
		Last Modified: Fri, 03 Dec 2021 20:57:22 GMT  
		Size: 2.3 MB (2257828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696eeb26f8bf39548fdbc5946f4443b479ce079f2b4ff73d95ab70f4a77cd237`  
		Last Modified: Fri, 03 Dec 2021 20:57:22 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63b2a04633d035bab8bf65756959a3f6c27236b10f2df105c97760f087d2df0`  
		Last Modified: Fri, 03 Dec 2021 20:57:22 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7ba76bd956a9b63d4559a4144316330627c7dd1ceb4a8ad858ff6462db79078`  
		Last Modified: Fri, 03 Dec 2021 20:57:22 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8cd927e7dbd6905e1a2b5bb99be19019b586b787ad91f5e988fe85277cc44e`  
		Last Modified: Fri, 03 Dec 2021 20:57:22 GMT  
		Size: 2.5 KB (2500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13-mysql-tomcat`

```console
$ docker pull xwiki@sha256:f8be6bb37b7e4385597a7186a40f6d8bcde4f9c609d13f34149ace9ac4d5fdeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:13-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:7340a02a837d6d8a7751bb8369c2d9a97643fd4e2530e1bc0098f235933f1e3d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **830.7 MB (830657270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:696e0182c57281cf1de1eefe88fa5d95fde87e191f5464d26c10b3687b03fa51`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:07 GMT
ADD file:e777355768c63f735e5458c7e0ada7f556f27d0493b3af35dc7c34f9c4294ea9 in / 
# Thu, 02 Dec 2021 02:48:08 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:39:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Dec 2021 03:40:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:34:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:34:20 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 02 Dec 2021 11:34:22 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 02 Dec 2021 11:34:22 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 11:34:22 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 11:34:23 GMT
ENV JAVA_VERSION=11.0.13
# Thu, 02 Dec 2021 11:34:48 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_x64_linux_11.0.13_8.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_aarch64_linux_11.0.13_8.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 02 Dec 2021 11:34:49 GMT
CMD ["jshell"]
# Fri, 03 Dec 2021 14:11:49 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Dec 2021 14:11:50 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Dec 2021 14:11:50 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 03 Dec 2021 14:11:51 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Dec 2021 14:11:51 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 14:11:51 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 14:27:34 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 03 Dec 2021 14:27:34 GMT
ENV TOMCAT_MAJOR=9
# Fri, 03 Dec 2021 14:27:34 GMT
ENV TOMCAT_VERSION=9.0.55
# Fri, 03 Dec 2021 14:27:35 GMT
ENV TOMCAT_SHA512=a0c480b8bba09069bda3b57f54e658450a59d799474ad587dead0ffbf5074c16ee3f9f9c13312d0ff3227c7034589dabf25941fbd672838e9baeee9661e024dc
# Fri, 03 Dec 2021 14:28:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 03 Dec 2021 14:28:03 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 03 Dec 2021 14:28:03 GMT
EXPOSE 8080
# Fri, 03 Dec 2021 14:28:03 GMT
CMD ["catalina.sh" "run"]
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 03 Dec 2021 20:52:45 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 20:52:47 GMT
ENV XWIKI_VERSION=13.10
# Fri, 03 Dec 2021 20:52:47 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10
# Fri, 03 Dec 2021 20:52:47 GMT
ENV XWIKI_DOWNLOAD_SHA256=863455ef741ec70539ab89b9981790909f3319b626a107e62fa42c8797df032b
# Fri, 03 Dec 2021 20:53:24 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 03 Dec 2021 20:53:25 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Fri, 03 Dec 2021 20:53:25 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Fri, 03 Dec 2021 20:53:25 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Fri, 03 Dec 2021 20:53:25 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Fri, 03 Dec 2021 20:53:25 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Fri, 03 Dec 2021 20:53:26 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 03 Dec 2021 20:53:27 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 03 Dec 2021 20:53:27 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 03 Dec 2021 20:53:28 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 03 Dec 2021 20:53:28 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 03 Dec 2021 20:53:28 GMT
VOLUME [/usr/local/xwiki]
# Fri, 03 Dec 2021 20:53:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Dec 2021 20:53:29 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:5e0b432e8ba9d9029a000e627840b98ffc1ed0c5172075b7d3e869be0df0fe9b`  
		Last Modified: Thu, 02 Dec 2021 02:53:18 GMT  
		Size: 54.9 MB (54932878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84cfd68b5cea612a8343c346bfa5bd6c486769010d12f7ec86b23c74887feb2`  
		Last Modified: Thu, 02 Dec 2021 03:49:22 GMT  
		Size: 5.2 MB (5153424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b8f2315954535f1e27cd13d777e73da4a787b0aebf4241d225beff3c91cbb1`  
		Last Modified: Thu, 02 Dec 2021 03:49:23 GMT  
		Size: 10.9 MB (10871995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0598fa43a7e793a76c198e8d45d8810394e1cfc943b2673d7fcf5a6fdc4f45b3`  
		Last Modified: Thu, 02 Dec 2021 03:49:46 GMT  
		Size: 54.6 MB (54567844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d35e3be804184359e0904389b149de16f159e30436d7a8a970aef67a4d155b`  
		Last Modified: Thu, 02 Dec 2021 11:54:46 GMT  
		Size: 5.4 MB (5420076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc448a0c88bee4d3cf6a928aa2b4cf499f4cb05034093c581342d414188a566`  
		Last Modified: Thu, 02 Dec 2021 11:54:45 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbdff6e5955b8bcd2e24b1a49fa4ec593ad333133c52911832aa2a7893f542da`  
		Last Modified: Thu, 02 Dec 2021 11:55:04 GMT  
		Size: 203.1 MB (203118915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5daf3771e3d8c27aa89cbcfef659790a2218e319899d49fbccde199e1780a5ef`  
		Last Modified: Fri, 03 Dec 2021 14:54:53 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5434ab540d864811e12dac3650eb0bc67bc8f6d7a6cb1f3c832e2c078c45302c`  
		Last Modified: Fri, 03 Dec 2021 15:08:17 GMT  
		Size: 12.5 MB (12523151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f43f4b2f615c39e867b3110fbc83f1d8fa2b72e4788cdcc91ea5dd73e97102`  
		Last Modified: Fri, 03 Dec 2021 15:08:16 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb64e66bc904d2f87948ce847a95dfa536c19132b599dc7f18ee2fec72ce7a8`  
		Last Modified: Fri, 03 Dec 2021 20:57:50 GMT  
		Size: 189.4 MB (189410805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eda7eb7430a70eef3ce565f0ad28fd9afcc0377bc9ba457bf47563dcf4ca3f25`  
		Last Modified: Fri, 03 Dec 2021 20:57:41 GMT  
		Size: 292.4 MB (292388360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f5388154bcdeb77283073eb4e763658b195a0a27693e1e7c35365485f30f18`  
		Last Modified: Fri, 03 Dec 2021 20:57:22 GMT  
		Size: 2.3 MB (2257828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696eeb26f8bf39548fdbc5946f4443b479ce079f2b4ff73d95ab70f4a77cd237`  
		Last Modified: Fri, 03 Dec 2021 20:57:22 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63b2a04633d035bab8bf65756959a3f6c27236b10f2df105c97760f087d2df0`  
		Last Modified: Fri, 03 Dec 2021 20:57:22 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7ba76bd956a9b63d4559a4144316330627c7dd1ceb4a8ad858ff6462db79078`  
		Last Modified: Fri, 03 Dec 2021 20:57:22 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8cd927e7dbd6905e1a2b5bb99be19019b586b787ad91f5e988fe85277cc44e`  
		Last Modified: Fri, 03 Dec 2021 20:57:22 GMT  
		Size: 2.5 KB (2500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13-postgres-tomcat`

```console
$ docker pull xwiki@sha256:d50518708792e2f5ed32a8f64476cd86137ae4114fa48cb8273da99ee32bff2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:13-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:0c3fe8d2f8b7734919c768321233164aa60eba53cceb0a4de73f20fbd761b63e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **830.1 MB (830121178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e1da45be61cdd50a06bd28b7845169b75250986f288972a8b05b50ded4a22c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:07 GMT
ADD file:e777355768c63f735e5458c7e0ada7f556f27d0493b3af35dc7c34f9c4294ea9 in / 
# Thu, 02 Dec 2021 02:48:08 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:39:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Dec 2021 03:40:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:34:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:34:20 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 02 Dec 2021 11:34:22 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 02 Dec 2021 11:34:22 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 11:34:22 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 11:34:23 GMT
ENV JAVA_VERSION=11.0.13
# Thu, 02 Dec 2021 11:34:48 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_x64_linux_11.0.13_8.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_aarch64_linux_11.0.13_8.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 02 Dec 2021 11:34:49 GMT
CMD ["jshell"]
# Fri, 03 Dec 2021 14:11:49 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Dec 2021 14:11:50 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Dec 2021 14:11:50 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 03 Dec 2021 14:11:51 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Dec 2021 14:11:51 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 14:11:51 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 14:27:34 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 03 Dec 2021 14:27:34 GMT
ENV TOMCAT_MAJOR=9
# Fri, 03 Dec 2021 14:27:34 GMT
ENV TOMCAT_VERSION=9.0.55
# Fri, 03 Dec 2021 14:27:35 GMT
ENV TOMCAT_SHA512=a0c480b8bba09069bda3b57f54e658450a59d799474ad587dead0ffbf5074c16ee3f9f9c13312d0ff3227c7034589dabf25941fbd672838e9baeee9661e024dc
# Fri, 03 Dec 2021 14:28:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 03 Dec 2021 14:28:03 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 03 Dec 2021 14:28:03 GMT
EXPOSE 8080
# Fri, 03 Dec 2021 14:28:03 GMT
CMD ["catalina.sh" "run"]
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 03 Dec 2021 20:54:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 20:54:05 GMT
ENV XWIKI_VERSION=13.10
# Fri, 03 Dec 2021 20:54:05 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10
# Fri, 03 Dec 2021 20:54:05 GMT
ENV XWIKI_DOWNLOAD_SHA256=863455ef741ec70539ab89b9981790909f3319b626a107e62fa42c8797df032b
# Fri, 03 Dec 2021 20:54:44 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 03 Dec 2021 20:54:45 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 03 Dec 2021 20:54:46 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 03 Dec 2021 20:54:46 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 03 Dec 2021 20:54:47 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 03 Dec 2021 20:54:47 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 03 Dec 2021 20:54:47 GMT
VOLUME [/usr/local/xwiki]
# Fri, 03 Dec 2021 20:54:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Dec 2021 20:54:47 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:5e0b432e8ba9d9029a000e627840b98ffc1ed0c5172075b7d3e869be0df0fe9b`  
		Last Modified: Thu, 02 Dec 2021 02:53:18 GMT  
		Size: 54.9 MB (54932878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84cfd68b5cea612a8343c346bfa5bd6c486769010d12f7ec86b23c74887feb2`  
		Last Modified: Thu, 02 Dec 2021 03:49:22 GMT  
		Size: 5.2 MB (5153424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b8f2315954535f1e27cd13d777e73da4a787b0aebf4241d225beff3c91cbb1`  
		Last Modified: Thu, 02 Dec 2021 03:49:23 GMT  
		Size: 10.9 MB (10871995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0598fa43a7e793a76c198e8d45d8810394e1cfc943b2673d7fcf5a6fdc4f45b3`  
		Last Modified: Thu, 02 Dec 2021 03:49:46 GMT  
		Size: 54.6 MB (54567844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d35e3be804184359e0904389b149de16f159e30436d7a8a970aef67a4d155b`  
		Last Modified: Thu, 02 Dec 2021 11:54:46 GMT  
		Size: 5.4 MB (5420076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc448a0c88bee4d3cf6a928aa2b4cf499f4cb05034093c581342d414188a566`  
		Last Modified: Thu, 02 Dec 2021 11:54:45 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbdff6e5955b8bcd2e24b1a49fa4ec593ad333133c52911832aa2a7893f542da`  
		Last Modified: Thu, 02 Dec 2021 11:55:04 GMT  
		Size: 203.1 MB (203118915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5daf3771e3d8c27aa89cbcfef659790a2218e319899d49fbccde199e1780a5ef`  
		Last Modified: Fri, 03 Dec 2021 14:54:53 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5434ab540d864811e12dac3650eb0bc67bc8f6d7a6cb1f3c832e2c078c45302c`  
		Last Modified: Fri, 03 Dec 2021 15:08:17 GMT  
		Size: 12.5 MB (12523151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f43f4b2f615c39e867b3110fbc83f1d8fa2b72e4788cdcc91ea5dd73e97102`  
		Last Modified: Fri, 03 Dec 2021 15:08:16 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c96c2f945ecec7eda758824db2032432765e7a0128ef11d3c1841ac2dc2e5d95`  
		Last Modified: Fri, 03 Dec 2021 20:59:00 GMT  
		Size: 190.3 MB (190286185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:955cdd39f0085f569763841337c25acef25604257a3de6773891e0bdcadb872d`  
		Last Modified: Fri, 03 Dec 2021 20:58:51 GMT  
		Size: 292.4 MB (292388346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc39c66a904202841f30554fedfe28bc6396c82f817ed5ebefbaed3429b82dd9`  
		Last Modified: Fri, 03 Dec 2021 20:58:32 GMT  
		Size: 846.2 KB (846214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e85be07558e39d22dc2b4a004d91020698ea370e5fb7cf4c99b2a31d3749f6e7`  
		Last Modified: Fri, 03 Dec 2021 20:58:31 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8586fc44e80ce8805adcde54de3c1551ca1c8f7f7e73e7b2d2cd66c38f935be`  
		Last Modified: Fri, 03 Dec 2021 20:58:31 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb2fe06d239087be98bf79090e52955d9ec293fbff5f6db1ff93dd7fee9e488`  
		Last Modified: Fri, 03 Dec 2021 20:58:31 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff38395ff2cff70633d42e627db200f34e988de4c7de698114b9c085bd6c201e`  
		Last Modified: Fri, 03 Dec 2021 20:58:31 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:13-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:9791c7dc4989df351c585fcb8eb26596e4a50fdf07313003f37c81bd58d2f84f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **820.8 MB (820758295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a04e1e74e2fd570283613fa3d4d622b67d64a5b21bd3df1e905b07839c312c74`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 02 Dec 2021 08:07:54 GMT
ADD file:998dc1c35eeeed1ddf46156aeb337fb9b8cbb4855caf994201167a1061f4ecbf in / 
# Thu, 02 Dec 2021 08:07:55 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 09:53:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 09:53:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Dec 2021 09:53:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:07:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:07:23 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 02 Dec 2021 11:07:24 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 02 Dec 2021 11:07:25 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 11:07:26 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 11:07:27 GMT
ENV JAVA_VERSION=11.0.13
# Thu, 02 Dec 2021 11:07:49 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_x64_linux_11.0.13_8.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_aarch64_linux_11.0.13_8.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 02 Dec 2021 11:07:50 GMT
CMD ["jshell"]
# Fri, 03 Dec 2021 10:33:28 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Dec 2021 10:33:28 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Dec 2021 10:33:30 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 03 Dec 2021 10:33:30 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Dec 2021 10:33:31 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 10:33:32 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 10:54:19 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 03 Dec 2021 10:54:20 GMT
ENV TOMCAT_MAJOR=9
# Fri, 03 Dec 2021 10:54:21 GMT
ENV TOMCAT_VERSION=9.0.55
# Fri, 03 Dec 2021 10:54:22 GMT
ENV TOMCAT_SHA512=a0c480b8bba09069bda3b57f54e658450a59d799474ad587dead0ffbf5074c16ee3f9f9c13312d0ff3227c7034589dabf25941fbd672838e9baeee9661e024dc
# Fri, 03 Dec 2021 10:54:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 03 Dec 2021 10:54:45 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 03 Dec 2021 10:54:45 GMT
EXPOSE 8080
# Fri, 03 Dec 2021 10:54:46 GMT
CMD ["catalina.sh" "run"]
# Fri, 03 Dec 2021 16:34:04 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 03 Dec 2021 16:34:05 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 16:34:05 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 16:34:06 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 03 Dec 2021 16:34:07 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 03 Dec 2021 16:34:08 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 03 Dec 2021 16:34:43 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 20:40:41 GMT
ENV XWIKI_VERSION=13.10
# Fri, 03 Dec 2021 20:40:42 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10
# Fri, 03 Dec 2021 20:40:43 GMT
ENV XWIKI_DOWNLOAD_SHA256=863455ef741ec70539ab89b9981790909f3319b626a107e62fa42c8797df032b
# Fri, 03 Dec 2021 20:42:05 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 03 Dec 2021 20:42:07 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 03 Dec 2021 20:42:08 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 03 Dec 2021 20:42:09 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 03 Dec 2021 20:42:10 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 03 Dec 2021 20:42:11 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 03 Dec 2021 20:42:12 GMT
VOLUME [/usr/local/xwiki]
# Fri, 03 Dec 2021 20:42:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Dec 2021 20:42:14 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:6476cb406b24c94f24348db05d154b814b14ee38860dea1625080e7e08295a80`  
		Last Modified: Thu, 02 Dec 2021 08:40:14 GMT  
		Size: 53.6 MB (53619027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96565d527970b1cc982493f96d6b317b1fbfdd7bf0ea6fd58d44942bb4f597c5`  
		Last Modified: Thu, 02 Dec 2021 10:02:24 GMT  
		Size: 4.9 MB (4937631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8c15f93136056df893ba8088992a38e90dc37210fd6ebb712413fd045c58de`  
		Last Modified: Thu, 02 Dec 2021 10:02:25 GMT  
		Size: 10.7 MB (10655914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee42e24e52cb2f9b50ab14328865298f5ae6ac159219db890afc6366ec641a46`  
		Last Modified: Thu, 02 Dec 2021 10:02:46 GMT  
		Size: 54.7 MB (54669690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1ddc61edfde0dfa7da5e868dfebc0df6e44b7c94700ae79892d861abc32f97`  
		Last Modified: Thu, 02 Dec 2021 11:31:06 GMT  
		Size: 5.4 MB (5420180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:804b3e7e3a2930efff5c50600a2c162b8f2af073ec54a3c44314cc36e68d1a75`  
		Last Modified: Thu, 02 Dec 2021 11:31:05 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c15c25e9529bccafc0b750eb33fb972a05d42a09303dc760b67f89ea21b0bce0`  
		Last Modified: Thu, 02 Dec 2021 11:31:26 GMT  
		Size: 200.7 MB (200712890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac1b17d7ee052527ef86a2354f093548ac170d6d3318a79fa9916fd616c2c40f`  
		Last Modified: Fri, 03 Dec 2021 11:33:43 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8926fc06c65e9a17e2a3110e422fbebb73f63463202846b0b6addc004fd06d`  
		Last Modified: Fri, 03 Dec 2021 11:49:18 GMT  
		Size: 12.3 MB (12292070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56905cdb16153e42e333c2819b26aec2f74860d5924cbe3cf1952f737953c4d`  
		Last Modified: Fri, 03 Dec 2021 16:37:29 GMT  
		Size: 185.2 MB (185204101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb1a3f2a620897e3ef5f866de2723c108b289d8308a9c3fea23ed2d98413c95`  
		Last Modified: Fri, 03 Dec 2021 20:43:19 GMT  
		Size: 292.4 MB (292388612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19092ac47724d18b94e705918c5687646e63dc774df241652ec6c77177eb0ad`  
		Last Modified: Fri, 03 Dec 2021 20:42:56 GMT  
		Size: 846.2 KB (846209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8959324a980da8d5711d1b493e27fea4054370769e11fe27b0341d928e7cad7b`  
		Last Modified: Fri, 03 Dec 2021 20:42:56 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3315518eeae081a901de36d667f5894a3bd974fdaa2943e8f6eff269b353b34d`  
		Last Modified: Fri, 03 Dec 2021 20:42:56 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b25a16e439c94dc4b0d402bdc659b525b4bc914799cb79e15e289e26f5eabdd7`  
		Last Modified: Fri, 03 Dec 2021 20:42:56 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0747fe5f75ab79fb9a9f111b719dec4f788fe07fcecc62412907b32ff5e2e9c`  
		Last Modified: Fri, 03 Dec 2021 20:42:56 GMT  
		Size: 2.5 KB (2500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13.10`

```console
$ docker pull xwiki@sha256:f8be6bb37b7e4385597a7186a40f6d8bcde4f9c609d13f34149ace9ac4d5fdeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:13.10` - linux; amd64

```console
$ docker pull xwiki@sha256:7340a02a837d6d8a7751bb8369c2d9a97643fd4e2530e1bc0098f235933f1e3d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **830.7 MB (830657270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:696e0182c57281cf1de1eefe88fa5d95fde87e191f5464d26c10b3687b03fa51`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:07 GMT
ADD file:e777355768c63f735e5458c7e0ada7f556f27d0493b3af35dc7c34f9c4294ea9 in / 
# Thu, 02 Dec 2021 02:48:08 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:39:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Dec 2021 03:40:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:34:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:34:20 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 02 Dec 2021 11:34:22 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 02 Dec 2021 11:34:22 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 11:34:22 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 11:34:23 GMT
ENV JAVA_VERSION=11.0.13
# Thu, 02 Dec 2021 11:34:48 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_x64_linux_11.0.13_8.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_aarch64_linux_11.0.13_8.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 02 Dec 2021 11:34:49 GMT
CMD ["jshell"]
# Fri, 03 Dec 2021 14:11:49 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Dec 2021 14:11:50 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Dec 2021 14:11:50 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 03 Dec 2021 14:11:51 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Dec 2021 14:11:51 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 14:11:51 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 14:27:34 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 03 Dec 2021 14:27:34 GMT
ENV TOMCAT_MAJOR=9
# Fri, 03 Dec 2021 14:27:34 GMT
ENV TOMCAT_VERSION=9.0.55
# Fri, 03 Dec 2021 14:27:35 GMT
ENV TOMCAT_SHA512=a0c480b8bba09069bda3b57f54e658450a59d799474ad587dead0ffbf5074c16ee3f9f9c13312d0ff3227c7034589dabf25941fbd672838e9baeee9661e024dc
# Fri, 03 Dec 2021 14:28:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 03 Dec 2021 14:28:03 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 03 Dec 2021 14:28:03 GMT
EXPOSE 8080
# Fri, 03 Dec 2021 14:28:03 GMT
CMD ["catalina.sh" "run"]
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 03 Dec 2021 20:52:45 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 20:52:47 GMT
ENV XWIKI_VERSION=13.10
# Fri, 03 Dec 2021 20:52:47 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10
# Fri, 03 Dec 2021 20:52:47 GMT
ENV XWIKI_DOWNLOAD_SHA256=863455ef741ec70539ab89b9981790909f3319b626a107e62fa42c8797df032b
# Fri, 03 Dec 2021 20:53:24 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 03 Dec 2021 20:53:25 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Fri, 03 Dec 2021 20:53:25 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Fri, 03 Dec 2021 20:53:25 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Fri, 03 Dec 2021 20:53:25 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Fri, 03 Dec 2021 20:53:25 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Fri, 03 Dec 2021 20:53:26 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 03 Dec 2021 20:53:27 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 03 Dec 2021 20:53:27 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 03 Dec 2021 20:53:28 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 03 Dec 2021 20:53:28 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 03 Dec 2021 20:53:28 GMT
VOLUME [/usr/local/xwiki]
# Fri, 03 Dec 2021 20:53:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Dec 2021 20:53:29 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:5e0b432e8ba9d9029a000e627840b98ffc1ed0c5172075b7d3e869be0df0fe9b`  
		Last Modified: Thu, 02 Dec 2021 02:53:18 GMT  
		Size: 54.9 MB (54932878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84cfd68b5cea612a8343c346bfa5bd6c486769010d12f7ec86b23c74887feb2`  
		Last Modified: Thu, 02 Dec 2021 03:49:22 GMT  
		Size: 5.2 MB (5153424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b8f2315954535f1e27cd13d777e73da4a787b0aebf4241d225beff3c91cbb1`  
		Last Modified: Thu, 02 Dec 2021 03:49:23 GMT  
		Size: 10.9 MB (10871995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0598fa43a7e793a76c198e8d45d8810394e1cfc943b2673d7fcf5a6fdc4f45b3`  
		Last Modified: Thu, 02 Dec 2021 03:49:46 GMT  
		Size: 54.6 MB (54567844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d35e3be804184359e0904389b149de16f159e30436d7a8a970aef67a4d155b`  
		Last Modified: Thu, 02 Dec 2021 11:54:46 GMT  
		Size: 5.4 MB (5420076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc448a0c88bee4d3cf6a928aa2b4cf499f4cb05034093c581342d414188a566`  
		Last Modified: Thu, 02 Dec 2021 11:54:45 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbdff6e5955b8bcd2e24b1a49fa4ec593ad333133c52911832aa2a7893f542da`  
		Last Modified: Thu, 02 Dec 2021 11:55:04 GMT  
		Size: 203.1 MB (203118915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5daf3771e3d8c27aa89cbcfef659790a2218e319899d49fbccde199e1780a5ef`  
		Last Modified: Fri, 03 Dec 2021 14:54:53 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5434ab540d864811e12dac3650eb0bc67bc8f6d7a6cb1f3c832e2c078c45302c`  
		Last Modified: Fri, 03 Dec 2021 15:08:17 GMT  
		Size: 12.5 MB (12523151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f43f4b2f615c39e867b3110fbc83f1d8fa2b72e4788cdcc91ea5dd73e97102`  
		Last Modified: Fri, 03 Dec 2021 15:08:16 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb64e66bc904d2f87948ce847a95dfa536c19132b599dc7f18ee2fec72ce7a8`  
		Last Modified: Fri, 03 Dec 2021 20:57:50 GMT  
		Size: 189.4 MB (189410805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eda7eb7430a70eef3ce565f0ad28fd9afcc0377bc9ba457bf47563dcf4ca3f25`  
		Last Modified: Fri, 03 Dec 2021 20:57:41 GMT  
		Size: 292.4 MB (292388360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f5388154bcdeb77283073eb4e763658b195a0a27693e1e7c35365485f30f18`  
		Last Modified: Fri, 03 Dec 2021 20:57:22 GMT  
		Size: 2.3 MB (2257828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696eeb26f8bf39548fdbc5946f4443b479ce079f2b4ff73d95ab70f4a77cd237`  
		Last Modified: Fri, 03 Dec 2021 20:57:22 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63b2a04633d035bab8bf65756959a3f6c27236b10f2df105c97760f087d2df0`  
		Last Modified: Fri, 03 Dec 2021 20:57:22 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7ba76bd956a9b63d4559a4144316330627c7dd1ceb4a8ad858ff6462db79078`  
		Last Modified: Fri, 03 Dec 2021 20:57:22 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8cd927e7dbd6905e1a2b5bb99be19019b586b787ad91f5e988fe85277cc44e`  
		Last Modified: Fri, 03 Dec 2021 20:57:22 GMT  
		Size: 2.5 KB (2500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13.10-mysql-tomcat`

```console
$ docker pull xwiki@sha256:f8be6bb37b7e4385597a7186a40f6d8bcde4f9c609d13f34149ace9ac4d5fdeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:13.10-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:7340a02a837d6d8a7751bb8369c2d9a97643fd4e2530e1bc0098f235933f1e3d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **830.7 MB (830657270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:696e0182c57281cf1de1eefe88fa5d95fde87e191f5464d26c10b3687b03fa51`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:07 GMT
ADD file:e777355768c63f735e5458c7e0ada7f556f27d0493b3af35dc7c34f9c4294ea9 in / 
# Thu, 02 Dec 2021 02:48:08 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:39:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Dec 2021 03:40:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:34:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:34:20 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 02 Dec 2021 11:34:22 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 02 Dec 2021 11:34:22 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 11:34:22 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 11:34:23 GMT
ENV JAVA_VERSION=11.0.13
# Thu, 02 Dec 2021 11:34:48 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_x64_linux_11.0.13_8.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_aarch64_linux_11.0.13_8.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 02 Dec 2021 11:34:49 GMT
CMD ["jshell"]
# Fri, 03 Dec 2021 14:11:49 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Dec 2021 14:11:50 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Dec 2021 14:11:50 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 03 Dec 2021 14:11:51 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Dec 2021 14:11:51 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 14:11:51 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 14:27:34 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 03 Dec 2021 14:27:34 GMT
ENV TOMCAT_MAJOR=9
# Fri, 03 Dec 2021 14:27:34 GMT
ENV TOMCAT_VERSION=9.0.55
# Fri, 03 Dec 2021 14:27:35 GMT
ENV TOMCAT_SHA512=a0c480b8bba09069bda3b57f54e658450a59d799474ad587dead0ffbf5074c16ee3f9f9c13312d0ff3227c7034589dabf25941fbd672838e9baeee9661e024dc
# Fri, 03 Dec 2021 14:28:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 03 Dec 2021 14:28:03 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 03 Dec 2021 14:28:03 GMT
EXPOSE 8080
# Fri, 03 Dec 2021 14:28:03 GMT
CMD ["catalina.sh" "run"]
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 03 Dec 2021 20:52:45 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 20:52:47 GMT
ENV XWIKI_VERSION=13.10
# Fri, 03 Dec 2021 20:52:47 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10
# Fri, 03 Dec 2021 20:52:47 GMT
ENV XWIKI_DOWNLOAD_SHA256=863455ef741ec70539ab89b9981790909f3319b626a107e62fa42c8797df032b
# Fri, 03 Dec 2021 20:53:24 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 03 Dec 2021 20:53:25 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Fri, 03 Dec 2021 20:53:25 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Fri, 03 Dec 2021 20:53:25 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Fri, 03 Dec 2021 20:53:25 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Fri, 03 Dec 2021 20:53:25 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Fri, 03 Dec 2021 20:53:26 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 03 Dec 2021 20:53:27 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 03 Dec 2021 20:53:27 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 03 Dec 2021 20:53:28 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 03 Dec 2021 20:53:28 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 03 Dec 2021 20:53:28 GMT
VOLUME [/usr/local/xwiki]
# Fri, 03 Dec 2021 20:53:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Dec 2021 20:53:29 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:5e0b432e8ba9d9029a000e627840b98ffc1ed0c5172075b7d3e869be0df0fe9b`  
		Last Modified: Thu, 02 Dec 2021 02:53:18 GMT  
		Size: 54.9 MB (54932878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84cfd68b5cea612a8343c346bfa5bd6c486769010d12f7ec86b23c74887feb2`  
		Last Modified: Thu, 02 Dec 2021 03:49:22 GMT  
		Size: 5.2 MB (5153424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b8f2315954535f1e27cd13d777e73da4a787b0aebf4241d225beff3c91cbb1`  
		Last Modified: Thu, 02 Dec 2021 03:49:23 GMT  
		Size: 10.9 MB (10871995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0598fa43a7e793a76c198e8d45d8810394e1cfc943b2673d7fcf5a6fdc4f45b3`  
		Last Modified: Thu, 02 Dec 2021 03:49:46 GMT  
		Size: 54.6 MB (54567844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d35e3be804184359e0904389b149de16f159e30436d7a8a970aef67a4d155b`  
		Last Modified: Thu, 02 Dec 2021 11:54:46 GMT  
		Size: 5.4 MB (5420076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc448a0c88bee4d3cf6a928aa2b4cf499f4cb05034093c581342d414188a566`  
		Last Modified: Thu, 02 Dec 2021 11:54:45 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbdff6e5955b8bcd2e24b1a49fa4ec593ad333133c52911832aa2a7893f542da`  
		Last Modified: Thu, 02 Dec 2021 11:55:04 GMT  
		Size: 203.1 MB (203118915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5daf3771e3d8c27aa89cbcfef659790a2218e319899d49fbccde199e1780a5ef`  
		Last Modified: Fri, 03 Dec 2021 14:54:53 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5434ab540d864811e12dac3650eb0bc67bc8f6d7a6cb1f3c832e2c078c45302c`  
		Last Modified: Fri, 03 Dec 2021 15:08:17 GMT  
		Size: 12.5 MB (12523151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f43f4b2f615c39e867b3110fbc83f1d8fa2b72e4788cdcc91ea5dd73e97102`  
		Last Modified: Fri, 03 Dec 2021 15:08:16 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb64e66bc904d2f87948ce847a95dfa536c19132b599dc7f18ee2fec72ce7a8`  
		Last Modified: Fri, 03 Dec 2021 20:57:50 GMT  
		Size: 189.4 MB (189410805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eda7eb7430a70eef3ce565f0ad28fd9afcc0377bc9ba457bf47563dcf4ca3f25`  
		Last Modified: Fri, 03 Dec 2021 20:57:41 GMT  
		Size: 292.4 MB (292388360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f5388154bcdeb77283073eb4e763658b195a0a27693e1e7c35365485f30f18`  
		Last Modified: Fri, 03 Dec 2021 20:57:22 GMT  
		Size: 2.3 MB (2257828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696eeb26f8bf39548fdbc5946f4443b479ce079f2b4ff73d95ab70f4a77cd237`  
		Last Modified: Fri, 03 Dec 2021 20:57:22 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63b2a04633d035bab8bf65756959a3f6c27236b10f2df105c97760f087d2df0`  
		Last Modified: Fri, 03 Dec 2021 20:57:22 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7ba76bd956a9b63d4559a4144316330627c7dd1ceb4a8ad858ff6462db79078`  
		Last Modified: Fri, 03 Dec 2021 20:57:22 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8cd927e7dbd6905e1a2b5bb99be19019b586b787ad91f5e988fe85277cc44e`  
		Last Modified: Fri, 03 Dec 2021 20:57:22 GMT  
		Size: 2.5 KB (2500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13.10-postgres-tomcat`

```console
$ docker pull xwiki@sha256:d50518708792e2f5ed32a8f64476cd86137ae4114fa48cb8273da99ee32bff2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:13.10-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:0c3fe8d2f8b7734919c768321233164aa60eba53cceb0a4de73f20fbd761b63e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **830.1 MB (830121178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e1da45be61cdd50a06bd28b7845169b75250986f288972a8b05b50ded4a22c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:07 GMT
ADD file:e777355768c63f735e5458c7e0ada7f556f27d0493b3af35dc7c34f9c4294ea9 in / 
# Thu, 02 Dec 2021 02:48:08 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:39:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Dec 2021 03:40:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:34:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:34:20 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 02 Dec 2021 11:34:22 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 02 Dec 2021 11:34:22 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 11:34:22 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 11:34:23 GMT
ENV JAVA_VERSION=11.0.13
# Thu, 02 Dec 2021 11:34:48 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_x64_linux_11.0.13_8.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_aarch64_linux_11.0.13_8.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 02 Dec 2021 11:34:49 GMT
CMD ["jshell"]
# Fri, 03 Dec 2021 14:11:49 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Dec 2021 14:11:50 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Dec 2021 14:11:50 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 03 Dec 2021 14:11:51 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Dec 2021 14:11:51 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 14:11:51 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 14:27:34 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 03 Dec 2021 14:27:34 GMT
ENV TOMCAT_MAJOR=9
# Fri, 03 Dec 2021 14:27:34 GMT
ENV TOMCAT_VERSION=9.0.55
# Fri, 03 Dec 2021 14:27:35 GMT
ENV TOMCAT_SHA512=a0c480b8bba09069bda3b57f54e658450a59d799474ad587dead0ffbf5074c16ee3f9f9c13312d0ff3227c7034589dabf25941fbd672838e9baeee9661e024dc
# Fri, 03 Dec 2021 14:28:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 03 Dec 2021 14:28:03 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 03 Dec 2021 14:28:03 GMT
EXPOSE 8080
# Fri, 03 Dec 2021 14:28:03 GMT
CMD ["catalina.sh" "run"]
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 03 Dec 2021 20:54:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 20:54:05 GMT
ENV XWIKI_VERSION=13.10
# Fri, 03 Dec 2021 20:54:05 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10
# Fri, 03 Dec 2021 20:54:05 GMT
ENV XWIKI_DOWNLOAD_SHA256=863455ef741ec70539ab89b9981790909f3319b626a107e62fa42c8797df032b
# Fri, 03 Dec 2021 20:54:44 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 03 Dec 2021 20:54:45 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 03 Dec 2021 20:54:46 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 03 Dec 2021 20:54:46 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 03 Dec 2021 20:54:47 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 03 Dec 2021 20:54:47 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 03 Dec 2021 20:54:47 GMT
VOLUME [/usr/local/xwiki]
# Fri, 03 Dec 2021 20:54:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Dec 2021 20:54:47 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:5e0b432e8ba9d9029a000e627840b98ffc1ed0c5172075b7d3e869be0df0fe9b`  
		Last Modified: Thu, 02 Dec 2021 02:53:18 GMT  
		Size: 54.9 MB (54932878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84cfd68b5cea612a8343c346bfa5bd6c486769010d12f7ec86b23c74887feb2`  
		Last Modified: Thu, 02 Dec 2021 03:49:22 GMT  
		Size: 5.2 MB (5153424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b8f2315954535f1e27cd13d777e73da4a787b0aebf4241d225beff3c91cbb1`  
		Last Modified: Thu, 02 Dec 2021 03:49:23 GMT  
		Size: 10.9 MB (10871995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0598fa43a7e793a76c198e8d45d8810394e1cfc943b2673d7fcf5a6fdc4f45b3`  
		Last Modified: Thu, 02 Dec 2021 03:49:46 GMT  
		Size: 54.6 MB (54567844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d35e3be804184359e0904389b149de16f159e30436d7a8a970aef67a4d155b`  
		Last Modified: Thu, 02 Dec 2021 11:54:46 GMT  
		Size: 5.4 MB (5420076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc448a0c88bee4d3cf6a928aa2b4cf499f4cb05034093c581342d414188a566`  
		Last Modified: Thu, 02 Dec 2021 11:54:45 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbdff6e5955b8bcd2e24b1a49fa4ec593ad333133c52911832aa2a7893f542da`  
		Last Modified: Thu, 02 Dec 2021 11:55:04 GMT  
		Size: 203.1 MB (203118915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5daf3771e3d8c27aa89cbcfef659790a2218e319899d49fbccde199e1780a5ef`  
		Last Modified: Fri, 03 Dec 2021 14:54:53 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5434ab540d864811e12dac3650eb0bc67bc8f6d7a6cb1f3c832e2c078c45302c`  
		Last Modified: Fri, 03 Dec 2021 15:08:17 GMT  
		Size: 12.5 MB (12523151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f43f4b2f615c39e867b3110fbc83f1d8fa2b72e4788cdcc91ea5dd73e97102`  
		Last Modified: Fri, 03 Dec 2021 15:08:16 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c96c2f945ecec7eda758824db2032432765e7a0128ef11d3c1841ac2dc2e5d95`  
		Last Modified: Fri, 03 Dec 2021 20:59:00 GMT  
		Size: 190.3 MB (190286185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:955cdd39f0085f569763841337c25acef25604257a3de6773891e0bdcadb872d`  
		Last Modified: Fri, 03 Dec 2021 20:58:51 GMT  
		Size: 292.4 MB (292388346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc39c66a904202841f30554fedfe28bc6396c82f817ed5ebefbaed3429b82dd9`  
		Last Modified: Fri, 03 Dec 2021 20:58:32 GMT  
		Size: 846.2 KB (846214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e85be07558e39d22dc2b4a004d91020698ea370e5fb7cf4c99b2a31d3749f6e7`  
		Last Modified: Fri, 03 Dec 2021 20:58:31 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8586fc44e80ce8805adcde54de3c1551ca1c8f7f7e73e7b2d2cd66c38f935be`  
		Last Modified: Fri, 03 Dec 2021 20:58:31 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb2fe06d239087be98bf79090e52955d9ec293fbff5f6db1ff93dd7fee9e488`  
		Last Modified: Fri, 03 Dec 2021 20:58:31 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff38395ff2cff70633d42e627db200f34e988de4c7de698114b9c085bd6c201e`  
		Last Modified: Fri, 03 Dec 2021 20:58:31 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:13.10-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:9791c7dc4989df351c585fcb8eb26596e4a50fdf07313003f37c81bd58d2f84f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **820.8 MB (820758295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a04e1e74e2fd570283613fa3d4d622b67d64a5b21bd3df1e905b07839c312c74`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 02 Dec 2021 08:07:54 GMT
ADD file:998dc1c35eeeed1ddf46156aeb337fb9b8cbb4855caf994201167a1061f4ecbf in / 
# Thu, 02 Dec 2021 08:07:55 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 09:53:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 09:53:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Dec 2021 09:53:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:07:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:07:23 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 02 Dec 2021 11:07:24 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 02 Dec 2021 11:07:25 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 11:07:26 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 11:07:27 GMT
ENV JAVA_VERSION=11.0.13
# Thu, 02 Dec 2021 11:07:49 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_x64_linux_11.0.13_8.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_aarch64_linux_11.0.13_8.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 02 Dec 2021 11:07:50 GMT
CMD ["jshell"]
# Fri, 03 Dec 2021 10:33:28 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Dec 2021 10:33:28 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Dec 2021 10:33:30 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 03 Dec 2021 10:33:30 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Dec 2021 10:33:31 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 10:33:32 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 10:54:19 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 03 Dec 2021 10:54:20 GMT
ENV TOMCAT_MAJOR=9
# Fri, 03 Dec 2021 10:54:21 GMT
ENV TOMCAT_VERSION=9.0.55
# Fri, 03 Dec 2021 10:54:22 GMT
ENV TOMCAT_SHA512=a0c480b8bba09069bda3b57f54e658450a59d799474ad587dead0ffbf5074c16ee3f9f9c13312d0ff3227c7034589dabf25941fbd672838e9baeee9661e024dc
# Fri, 03 Dec 2021 10:54:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 03 Dec 2021 10:54:45 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 03 Dec 2021 10:54:45 GMT
EXPOSE 8080
# Fri, 03 Dec 2021 10:54:46 GMT
CMD ["catalina.sh" "run"]
# Fri, 03 Dec 2021 16:34:04 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 03 Dec 2021 16:34:05 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 16:34:05 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 16:34:06 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 03 Dec 2021 16:34:07 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 03 Dec 2021 16:34:08 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 03 Dec 2021 16:34:43 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 20:40:41 GMT
ENV XWIKI_VERSION=13.10
# Fri, 03 Dec 2021 20:40:42 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10
# Fri, 03 Dec 2021 20:40:43 GMT
ENV XWIKI_DOWNLOAD_SHA256=863455ef741ec70539ab89b9981790909f3319b626a107e62fa42c8797df032b
# Fri, 03 Dec 2021 20:42:05 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 03 Dec 2021 20:42:07 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 03 Dec 2021 20:42:08 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 03 Dec 2021 20:42:09 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 03 Dec 2021 20:42:10 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 03 Dec 2021 20:42:11 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 03 Dec 2021 20:42:12 GMT
VOLUME [/usr/local/xwiki]
# Fri, 03 Dec 2021 20:42:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Dec 2021 20:42:14 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:6476cb406b24c94f24348db05d154b814b14ee38860dea1625080e7e08295a80`  
		Last Modified: Thu, 02 Dec 2021 08:40:14 GMT  
		Size: 53.6 MB (53619027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96565d527970b1cc982493f96d6b317b1fbfdd7bf0ea6fd58d44942bb4f597c5`  
		Last Modified: Thu, 02 Dec 2021 10:02:24 GMT  
		Size: 4.9 MB (4937631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8c15f93136056df893ba8088992a38e90dc37210fd6ebb712413fd045c58de`  
		Last Modified: Thu, 02 Dec 2021 10:02:25 GMT  
		Size: 10.7 MB (10655914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee42e24e52cb2f9b50ab14328865298f5ae6ac159219db890afc6366ec641a46`  
		Last Modified: Thu, 02 Dec 2021 10:02:46 GMT  
		Size: 54.7 MB (54669690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1ddc61edfde0dfa7da5e868dfebc0df6e44b7c94700ae79892d861abc32f97`  
		Last Modified: Thu, 02 Dec 2021 11:31:06 GMT  
		Size: 5.4 MB (5420180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:804b3e7e3a2930efff5c50600a2c162b8f2af073ec54a3c44314cc36e68d1a75`  
		Last Modified: Thu, 02 Dec 2021 11:31:05 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c15c25e9529bccafc0b750eb33fb972a05d42a09303dc760b67f89ea21b0bce0`  
		Last Modified: Thu, 02 Dec 2021 11:31:26 GMT  
		Size: 200.7 MB (200712890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac1b17d7ee052527ef86a2354f093548ac170d6d3318a79fa9916fd616c2c40f`  
		Last Modified: Fri, 03 Dec 2021 11:33:43 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8926fc06c65e9a17e2a3110e422fbebb73f63463202846b0b6addc004fd06d`  
		Last Modified: Fri, 03 Dec 2021 11:49:18 GMT  
		Size: 12.3 MB (12292070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56905cdb16153e42e333c2819b26aec2f74860d5924cbe3cf1952f737953c4d`  
		Last Modified: Fri, 03 Dec 2021 16:37:29 GMT  
		Size: 185.2 MB (185204101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb1a3f2a620897e3ef5f866de2723c108b289d8308a9c3fea23ed2d98413c95`  
		Last Modified: Fri, 03 Dec 2021 20:43:19 GMT  
		Size: 292.4 MB (292388612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19092ac47724d18b94e705918c5687646e63dc774df241652ec6c77177eb0ad`  
		Last Modified: Fri, 03 Dec 2021 20:42:56 GMT  
		Size: 846.2 KB (846209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8959324a980da8d5711d1b493e27fea4054370769e11fe27b0341d928e7cad7b`  
		Last Modified: Fri, 03 Dec 2021 20:42:56 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3315518eeae081a901de36d667f5894a3bd974fdaa2943e8f6eff269b353b34d`  
		Last Modified: Fri, 03 Dec 2021 20:42:56 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b25a16e439c94dc4b0d402bdc659b525b4bc914799cb79e15e289e26f5eabdd7`  
		Last Modified: Fri, 03 Dec 2021 20:42:56 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0747fe5f75ab79fb9a9f111b719dec4f788fe07fcecc62412907b32ff5e2e9c`  
		Last Modified: Fri, 03 Dec 2021 20:42:56 GMT  
		Size: 2.5 KB (2500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13.10.0`

```console
$ docker pull xwiki@sha256:f8be6bb37b7e4385597a7186a40f6d8bcde4f9c609d13f34149ace9ac4d5fdeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:13.10.0` - linux; amd64

```console
$ docker pull xwiki@sha256:7340a02a837d6d8a7751bb8369c2d9a97643fd4e2530e1bc0098f235933f1e3d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **830.7 MB (830657270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:696e0182c57281cf1de1eefe88fa5d95fde87e191f5464d26c10b3687b03fa51`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:07 GMT
ADD file:e777355768c63f735e5458c7e0ada7f556f27d0493b3af35dc7c34f9c4294ea9 in / 
# Thu, 02 Dec 2021 02:48:08 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:39:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Dec 2021 03:40:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:34:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:34:20 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 02 Dec 2021 11:34:22 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 02 Dec 2021 11:34:22 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 11:34:22 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 11:34:23 GMT
ENV JAVA_VERSION=11.0.13
# Thu, 02 Dec 2021 11:34:48 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_x64_linux_11.0.13_8.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_aarch64_linux_11.0.13_8.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 02 Dec 2021 11:34:49 GMT
CMD ["jshell"]
# Fri, 03 Dec 2021 14:11:49 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Dec 2021 14:11:50 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Dec 2021 14:11:50 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 03 Dec 2021 14:11:51 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Dec 2021 14:11:51 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 14:11:51 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 14:27:34 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 03 Dec 2021 14:27:34 GMT
ENV TOMCAT_MAJOR=9
# Fri, 03 Dec 2021 14:27:34 GMT
ENV TOMCAT_VERSION=9.0.55
# Fri, 03 Dec 2021 14:27:35 GMT
ENV TOMCAT_SHA512=a0c480b8bba09069bda3b57f54e658450a59d799474ad587dead0ffbf5074c16ee3f9f9c13312d0ff3227c7034589dabf25941fbd672838e9baeee9661e024dc
# Fri, 03 Dec 2021 14:28:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 03 Dec 2021 14:28:03 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 03 Dec 2021 14:28:03 GMT
EXPOSE 8080
# Fri, 03 Dec 2021 14:28:03 GMT
CMD ["catalina.sh" "run"]
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 03 Dec 2021 20:52:45 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 20:52:47 GMT
ENV XWIKI_VERSION=13.10
# Fri, 03 Dec 2021 20:52:47 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10
# Fri, 03 Dec 2021 20:52:47 GMT
ENV XWIKI_DOWNLOAD_SHA256=863455ef741ec70539ab89b9981790909f3319b626a107e62fa42c8797df032b
# Fri, 03 Dec 2021 20:53:24 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 03 Dec 2021 20:53:25 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Fri, 03 Dec 2021 20:53:25 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Fri, 03 Dec 2021 20:53:25 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Fri, 03 Dec 2021 20:53:25 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Fri, 03 Dec 2021 20:53:25 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Fri, 03 Dec 2021 20:53:26 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 03 Dec 2021 20:53:27 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 03 Dec 2021 20:53:27 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 03 Dec 2021 20:53:28 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 03 Dec 2021 20:53:28 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 03 Dec 2021 20:53:28 GMT
VOLUME [/usr/local/xwiki]
# Fri, 03 Dec 2021 20:53:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Dec 2021 20:53:29 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:5e0b432e8ba9d9029a000e627840b98ffc1ed0c5172075b7d3e869be0df0fe9b`  
		Last Modified: Thu, 02 Dec 2021 02:53:18 GMT  
		Size: 54.9 MB (54932878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84cfd68b5cea612a8343c346bfa5bd6c486769010d12f7ec86b23c74887feb2`  
		Last Modified: Thu, 02 Dec 2021 03:49:22 GMT  
		Size: 5.2 MB (5153424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b8f2315954535f1e27cd13d777e73da4a787b0aebf4241d225beff3c91cbb1`  
		Last Modified: Thu, 02 Dec 2021 03:49:23 GMT  
		Size: 10.9 MB (10871995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0598fa43a7e793a76c198e8d45d8810394e1cfc943b2673d7fcf5a6fdc4f45b3`  
		Last Modified: Thu, 02 Dec 2021 03:49:46 GMT  
		Size: 54.6 MB (54567844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d35e3be804184359e0904389b149de16f159e30436d7a8a970aef67a4d155b`  
		Last Modified: Thu, 02 Dec 2021 11:54:46 GMT  
		Size: 5.4 MB (5420076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc448a0c88bee4d3cf6a928aa2b4cf499f4cb05034093c581342d414188a566`  
		Last Modified: Thu, 02 Dec 2021 11:54:45 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbdff6e5955b8bcd2e24b1a49fa4ec593ad333133c52911832aa2a7893f542da`  
		Last Modified: Thu, 02 Dec 2021 11:55:04 GMT  
		Size: 203.1 MB (203118915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5daf3771e3d8c27aa89cbcfef659790a2218e319899d49fbccde199e1780a5ef`  
		Last Modified: Fri, 03 Dec 2021 14:54:53 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5434ab540d864811e12dac3650eb0bc67bc8f6d7a6cb1f3c832e2c078c45302c`  
		Last Modified: Fri, 03 Dec 2021 15:08:17 GMT  
		Size: 12.5 MB (12523151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f43f4b2f615c39e867b3110fbc83f1d8fa2b72e4788cdcc91ea5dd73e97102`  
		Last Modified: Fri, 03 Dec 2021 15:08:16 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb64e66bc904d2f87948ce847a95dfa536c19132b599dc7f18ee2fec72ce7a8`  
		Last Modified: Fri, 03 Dec 2021 20:57:50 GMT  
		Size: 189.4 MB (189410805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eda7eb7430a70eef3ce565f0ad28fd9afcc0377bc9ba457bf47563dcf4ca3f25`  
		Last Modified: Fri, 03 Dec 2021 20:57:41 GMT  
		Size: 292.4 MB (292388360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f5388154bcdeb77283073eb4e763658b195a0a27693e1e7c35365485f30f18`  
		Last Modified: Fri, 03 Dec 2021 20:57:22 GMT  
		Size: 2.3 MB (2257828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696eeb26f8bf39548fdbc5946f4443b479ce079f2b4ff73d95ab70f4a77cd237`  
		Last Modified: Fri, 03 Dec 2021 20:57:22 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63b2a04633d035bab8bf65756959a3f6c27236b10f2df105c97760f087d2df0`  
		Last Modified: Fri, 03 Dec 2021 20:57:22 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7ba76bd956a9b63d4559a4144316330627c7dd1ceb4a8ad858ff6462db79078`  
		Last Modified: Fri, 03 Dec 2021 20:57:22 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8cd927e7dbd6905e1a2b5bb99be19019b586b787ad91f5e988fe85277cc44e`  
		Last Modified: Fri, 03 Dec 2021 20:57:22 GMT  
		Size: 2.5 KB (2500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13.10.0-mysql-tomcat`

```console
$ docker pull xwiki@sha256:f8be6bb37b7e4385597a7186a40f6d8bcde4f9c609d13f34149ace9ac4d5fdeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:13.10.0-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:7340a02a837d6d8a7751bb8369c2d9a97643fd4e2530e1bc0098f235933f1e3d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **830.7 MB (830657270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:696e0182c57281cf1de1eefe88fa5d95fde87e191f5464d26c10b3687b03fa51`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:07 GMT
ADD file:e777355768c63f735e5458c7e0ada7f556f27d0493b3af35dc7c34f9c4294ea9 in / 
# Thu, 02 Dec 2021 02:48:08 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:39:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Dec 2021 03:40:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:34:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:34:20 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 02 Dec 2021 11:34:22 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 02 Dec 2021 11:34:22 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 11:34:22 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 11:34:23 GMT
ENV JAVA_VERSION=11.0.13
# Thu, 02 Dec 2021 11:34:48 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_x64_linux_11.0.13_8.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_aarch64_linux_11.0.13_8.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 02 Dec 2021 11:34:49 GMT
CMD ["jshell"]
# Fri, 03 Dec 2021 14:11:49 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Dec 2021 14:11:50 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Dec 2021 14:11:50 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 03 Dec 2021 14:11:51 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Dec 2021 14:11:51 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 14:11:51 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 14:27:34 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 03 Dec 2021 14:27:34 GMT
ENV TOMCAT_MAJOR=9
# Fri, 03 Dec 2021 14:27:34 GMT
ENV TOMCAT_VERSION=9.0.55
# Fri, 03 Dec 2021 14:27:35 GMT
ENV TOMCAT_SHA512=a0c480b8bba09069bda3b57f54e658450a59d799474ad587dead0ffbf5074c16ee3f9f9c13312d0ff3227c7034589dabf25941fbd672838e9baeee9661e024dc
# Fri, 03 Dec 2021 14:28:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 03 Dec 2021 14:28:03 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 03 Dec 2021 14:28:03 GMT
EXPOSE 8080
# Fri, 03 Dec 2021 14:28:03 GMT
CMD ["catalina.sh" "run"]
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 03 Dec 2021 20:52:45 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 20:52:47 GMT
ENV XWIKI_VERSION=13.10
# Fri, 03 Dec 2021 20:52:47 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10
# Fri, 03 Dec 2021 20:52:47 GMT
ENV XWIKI_DOWNLOAD_SHA256=863455ef741ec70539ab89b9981790909f3319b626a107e62fa42c8797df032b
# Fri, 03 Dec 2021 20:53:24 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 03 Dec 2021 20:53:25 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Fri, 03 Dec 2021 20:53:25 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Fri, 03 Dec 2021 20:53:25 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Fri, 03 Dec 2021 20:53:25 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Fri, 03 Dec 2021 20:53:25 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Fri, 03 Dec 2021 20:53:26 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 03 Dec 2021 20:53:27 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 03 Dec 2021 20:53:27 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 03 Dec 2021 20:53:28 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 03 Dec 2021 20:53:28 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 03 Dec 2021 20:53:28 GMT
VOLUME [/usr/local/xwiki]
# Fri, 03 Dec 2021 20:53:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Dec 2021 20:53:29 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:5e0b432e8ba9d9029a000e627840b98ffc1ed0c5172075b7d3e869be0df0fe9b`  
		Last Modified: Thu, 02 Dec 2021 02:53:18 GMT  
		Size: 54.9 MB (54932878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84cfd68b5cea612a8343c346bfa5bd6c486769010d12f7ec86b23c74887feb2`  
		Last Modified: Thu, 02 Dec 2021 03:49:22 GMT  
		Size: 5.2 MB (5153424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b8f2315954535f1e27cd13d777e73da4a787b0aebf4241d225beff3c91cbb1`  
		Last Modified: Thu, 02 Dec 2021 03:49:23 GMT  
		Size: 10.9 MB (10871995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0598fa43a7e793a76c198e8d45d8810394e1cfc943b2673d7fcf5a6fdc4f45b3`  
		Last Modified: Thu, 02 Dec 2021 03:49:46 GMT  
		Size: 54.6 MB (54567844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d35e3be804184359e0904389b149de16f159e30436d7a8a970aef67a4d155b`  
		Last Modified: Thu, 02 Dec 2021 11:54:46 GMT  
		Size: 5.4 MB (5420076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc448a0c88bee4d3cf6a928aa2b4cf499f4cb05034093c581342d414188a566`  
		Last Modified: Thu, 02 Dec 2021 11:54:45 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbdff6e5955b8bcd2e24b1a49fa4ec593ad333133c52911832aa2a7893f542da`  
		Last Modified: Thu, 02 Dec 2021 11:55:04 GMT  
		Size: 203.1 MB (203118915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5daf3771e3d8c27aa89cbcfef659790a2218e319899d49fbccde199e1780a5ef`  
		Last Modified: Fri, 03 Dec 2021 14:54:53 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5434ab540d864811e12dac3650eb0bc67bc8f6d7a6cb1f3c832e2c078c45302c`  
		Last Modified: Fri, 03 Dec 2021 15:08:17 GMT  
		Size: 12.5 MB (12523151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f43f4b2f615c39e867b3110fbc83f1d8fa2b72e4788cdcc91ea5dd73e97102`  
		Last Modified: Fri, 03 Dec 2021 15:08:16 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb64e66bc904d2f87948ce847a95dfa536c19132b599dc7f18ee2fec72ce7a8`  
		Last Modified: Fri, 03 Dec 2021 20:57:50 GMT  
		Size: 189.4 MB (189410805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eda7eb7430a70eef3ce565f0ad28fd9afcc0377bc9ba457bf47563dcf4ca3f25`  
		Last Modified: Fri, 03 Dec 2021 20:57:41 GMT  
		Size: 292.4 MB (292388360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f5388154bcdeb77283073eb4e763658b195a0a27693e1e7c35365485f30f18`  
		Last Modified: Fri, 03 Dec 2021 20:57:22 GMT  
		Size: 2.3 MB (2257828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696eeb26f8bf39548fdbc5946f4443b479ce079f2b4ff73d95ab70f4a77cd237`  
		Last Modified: Fri, 03 Dec 2021 20:57:22 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63b2a04633d035bab8bf65756959a3f6c27236b10f2df105c97760f087d2df0`  
		Last Modified: Fri, 03 Dec 2021 20:57:22 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7ba76bd956a9b63d4559a4144316330627c7dd1ceb4a8ad858ff6462db79078`  
		Last Modified: Fri, 03 Dec 2021 20:57:22 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8cd927e7dbd6905e1a2b5bb99be19019b586b787ad91f5e988fe85277cc44e`  
		Last Modified: Fri, 03 Dec 2021 20:57:22 GMT  
		Size: 2.5 KB (2500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13.10.0-postgres-tomcat`

```console
$ docker pull xwiki@sha256:d50518708792e2f5ed32a8f64476cd86137ae4114fa48cb8273da99ee32bff2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:13.10.0-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:0c3fe8d2f8b7734919c768321233164aa60eba53cceb0a4de73f20fbd761b63e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **830.1 MB (830121178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e1da45be61cdd50a06bd28b7845169b75250986f288972a8b05b50ded4a22c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:07 GMT
ADD file:e777355768c63f735e5458c7e0ada7f556f27d0493b3af35dc7c34f9c4294ea9 in / 
# Thu, 02 Dec 2021 02:48:08 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:39:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Dec 2021 03:40:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:34:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:34:20 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 02 Dec 2021 11:34:22 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 02 Dec 2021 11:34:22 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 11:34:22 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 11:34:23 GMT
ENV JAVA_VERSION=11.0.13
# Thu, 02 Dec 2021 11:34:48 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_x64_linux_11.0.13_8.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_aarch64_linux_11.0.13_8.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 02 Dec 2021 11:34:49 GMT
CMD ["jshell"]
# Fri, 03 Dec 2021 14:11:49 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Dec 2021 14:11:50 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Dec 2021 14:11:50 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 03 Dec 2021 14:11:51 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Dec 2021 14:11:51 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 14:11:51 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 14:27:34 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 03 Dec 2021 14:27:34 GMT
ENV TOMCAT_MAJOR=9
# Fri, 03 Dec 2021 14:27:34 GMT
ENV TOMCAT_VERSION=9.0.55
# Fri, 03 Dec 2021 14:27:35 GMT
ENV TOMCAT_SHA512=a0c480b8bba09069bda3b57f54e658450a59d799474ad587dead0ffbf5074c16ee3f9f9c13312d0ff3227c7034589dabf25941fbd672838e9baeee9661e024dc
# Fri, 03 Dec 2021 14:28:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 03 Dec 2021 14:28:03 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 03 Dec 2021 14:28:03 GMT
EXPOSE 8080
# Fri, 03 Dec 2021 14:28:03 GMT
CMD ["catalina.sh" "run"]
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 03 Dec 2021 20:54:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 20:54:05 GMT
ENV XWIKI_VERSION=13.10
# Fri, 03 Dec 2021 20:54:05 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10
# Fri, 03 Dec 2021 20:54:05 GMT
ENV XWIKI_DOWNLOAD_SHA256=863455ef741ec70539ab89b9981790909f3319b626a107e62fa42c8797df032b
# Fri, 03 Dec 2021 20:54:44 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 03 Dec 2021 20:54:45 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 03 Dec 2021 20:54:46 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 03 Dec 2021 20:54:46 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 03 Dec 2021 20:54:47 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 03 Dec 2021 20:54:47 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 03 Dec 2021 20:54:47 GMT
VOLUME [/usr/local/xwiki]
# Fri, 03 Dec 2021 20:54:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Dec 2021 20:54:47 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:5e0b432e8ba9d9029a000e627840b98ffc1ed0c5172075b7d3e869be0df0fe9b`  
		Last Modified: Thu, 02 Dec 2021 02:53:18 GMT  
		Size: 54.9 MB (54932878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84cfd68b5cea612a8343c346bfa5bd6c486769010d12f7ec86b23c74887feb2`  
		Last Modified: Thu, 02 Dec 2021 03:49:22 GMT  
		Size: 5.2 MB (5153424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b8f2315954535f1e27cd13d777e73da4a787b0aebf4241d225beff3c91cbb1`  
		Last Modified: Thu, 02 Dec 2021 03:49:23 GMT  
		Size: 10.9 MB (10871995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0598fa43a7e793a76c198e8d45d8810394e1cfc943b2673d7fcf5a6fdc4f45b3`  
		Last Modified: Thu, 02 Dec 2021 03:49:46 GMT  
		Size: 54.6 MB (54567844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d35e3be804184359e0904389b149de16f159e30436d7a8a970aef67a4d155b`  
		Last Modified: Thu, 02 Dec 2021 11:54:46 GMT  
		Size: 5.4 MB (5420076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc448a0c88bee4d3cf6a928aa2b4cf499f4cb05034093c581342d414188a566`  
		Last Modified: Thu, 02 Dec 2021 11:54:45 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbdff6e5955b8bcd2e24b1a49fa4ec593ad333133c52911832aa2a7893f542da`  
		Last Modified: Thu, 02 Dec 2021 11:55:04 GMT  
		Size: 203.1 MB (203118915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5daf3771e3d8c27aa89cbcfef659790a2218e319899d49fbccde199e1780a5ef`  
		Last Modified: Fri, 03 Dec 2021 14:54:53 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5434ab540d864811e12dac3650eb0bc67bc8f6d7a6cb1f3c832e2c078c45302c`  
		Last Modified: Fri, 03 Dec 2021 15:08:17 GMT  
		Size: 12.5 MB (12523151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f43f4b2f615c39e867b3110fbc83f1d8fa2b72e4788cdcc91ea5dd73e97102`  
		Last Modified: Fri, 03 Dec 2021 15:08:16 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c96c2f945ecec7eda758824db2032432765e7a0128ef11d3c1841ac2dc2e5d95`  
		Last Modified: Fri, 03 Dec 2021 20:59:00 GMT  
		Size: 190.3 MB (190286185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:955cdd39f0085f569763841337c25acef25604257a3de6773891e0bdcadb872d`  
		Last Modified: Fri, 03 Dec 2021 20:58:51 GMT  
		Size: 292.4 MB (292388346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc39c66a904202841f30554fedfe28bc6396c82f817ed5ebefbaed3429b82dd9`  
		Last Modified: Fri, 03 Dec 2021 20:58:32 GMT  
		Size: 846.2 KB (846214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e85be07558e39d22dc2b4a004d91020698ea370e5fb7cf4c99b2a31d3749f6e7`  
		Last Modified: Fri, 03 Dec 2021 20:58:31 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8586fc44e80ce8805adcde54de3c1551ca1c8f7f7e73e7b2d2cd66c38f935be`  
		Last Modified: Fri, 03 Dec 2021 20:58:31 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb2fe06d239087be98bf79090e52955d9ec293fbff5f6db1ff93dd7fee9e488`  
		Last Modified: Fri, 03 Dec 2021 20:58:31 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff38395ff2cff70633d42e627db200f34e988de4c7de698114b9c085bd6c201e`  
		Last Modified: Fri, 03 Dec 2021 20:58:31 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:13.10.0-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:9791c7dc4989df351c585fcb8eb26596e4a50fdf07313003f37c81bd58d2f84f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **820.8 MB (820758295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a04e1e74e2fd570283613fa3d4d622b67d64a5b21bd3df1e905b07839c312c74`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 02 Dec 2021 08:07:54 GMT
ADD file:998dc1c35eeeed1ddf46156aeb337fb9b8cbb4855caf994201167a1061f4ecbf in / 
# Thu, 02 Dec 2021 08:07:55 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 09:53:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 09:53:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Dec 2021 09:53:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:07:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:07:23 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 02 Dec 2021 11:07:24 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 02 Dec 2021 11:07:25 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 11:07:26 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 11:07:27 GMT
ENV JAVA_VERSION=11.0.13
# Thu, 02 Dec 2021 11:07:49 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_x64_linux_11.0.13_8.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_aarch64_linux_11.0.13_8.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 02 Dec 2021 11:07:50 GMT
CMD ["jshell"]
# Fri, 03 Dec 2021 10:33:28 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Dec 2021 10:33:28 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Dec 2021 10:33:30 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 03 Dec 2021 10:33:30 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Dec 2021 10:33:31 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 10:33:32 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 10:54:19 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 03 Dec 2021 10:54:20 GMT
ENV TOMCAT_MAJOR=9
# Fri, 03 Dec 2021 10:54:21 GMT
ENV TOMCAT_VERSION=9.0.55
# Fri, 03 Dec 2021 10:54:22 GMT
ENV TOMCAT_SHA512=a0c480b8bba09069bda3b57f54e658450a59d799474ad587dead0ffbf5074c16ee3f9f9c13312d0ff3227c7034589dabf25941fbd672838e9baeee9661e024dc
# Fri, 03 Dec 2021 10:54:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 03 Dec 2021 10:54:45 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 03 Dec 2021 10:54:45 GMT
EXPOSE 8080
# Fri, 03 Dec 2021 10:54:46 GMT
CMD ["catalina.sh" "run"]
# Fri, 03 Dec 2021 16:34:04 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 03 Dec 2021 16:34:05 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 16:34:05 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 16:34:06 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 03 Dec 2021 16:34:07 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 03 Dec 2021 16:34:08 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 03 Dec 2021 16:34:43 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 20:40:41 GMT
ENV XWIKI_VERSION=13.10
# Fri, 03 Dec 2021 20:40:42 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10
# Fri, 03 Dec 2021 20:40:43 GMT
ENV XWIKI_DOWNLOAD_SHA256=863455ef741ec70539ab89b9981790909f3319b626a107e62fa42c8797df032b
# Fri, 03 Dec 2021 20:42:05 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 03 Dec 2021 20:42:07 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 03 Dec 2021 20:42:08 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 03 Dec 2021 20:42:09 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 03 Dec 2021 20:42:10 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 03 Dec 2021 20:42:11 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 03 Dec 2021 20:42:12 GMT
VOLUME [/usr/local/xwiki]
# Fri, 03 Dec 2021 20:42:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Dec 2021 20:42:14 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:6476cb406b24c94f24348db05d154b814b14ee38860dea1625080e7e08295a80`  
		Last Modified: Thu, 02 Dec 2021 08:40:14 GMT  
		Size: 53.6 MB (53619027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96565d527970b1cc982493f96d6b317b1fbfdd7bf0ea6fd58d44942bb4f597c5`  
		Last Modified: Thu, 02 Dec 2021 10:02:24 GMT  
		Size: 4.9 MB (4937631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8c15f93136056df893ba8088992a38e90dc37210fd6ebb712413fd045c58de`  
		Last Modified: Thu, 02 Dec 2021 10:02:25 GMT  
		Size: 10.7 MB (10655914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee42e24e52cb2f9b50ab14328865298f5ae6ac159219db890afc6366ec641a46`  
		Last Modified: Thu, 02 Dec 2021 10:02:46 GMT  
		Size: 54.7 MB (54669690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1ddc61edfde0dfa7da5e868dfebc0df6e44b7c94700ae79892d861abc32f97`  
		Last Modified: Thu, 02 Dec 2021 11:31:06 GMT  
		Size: 5.4 MB (5420180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:804b3e7e3a2930efff5c50600a2c162b8f2af073ec54a3c44314cc36e68d1a75`  
		Last Modified: Thu, 02 Dec 2021 11:31:05 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c15c25e9529bccafc0b750eb33fb972a05d42a09303dc760b67f89ea21b0bce0`  
		Last Modified: Thu, 02 Dec 2021 11:31:26 GMT  
		Size: 200.7 MB (200712890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac1b17d7ee052527ef86a2354f093548ac170d6d3318a79fa9916fd616c2c40f`  
		Last Modified: Fri, 03 Dec 2021 11:33:43 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8926fc06c65e9a17e2a3110e422fbebb73f63463202846b0b6addc004fd06d`  
		Last Modified: Fri, 03 Dec 2021 11:49:18 GMT  
		Size: 12.3 MB (12292070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56905cdb16153e42e333c2819b26aec2f74860d5924cbe3cf1952f737953c4d`  
		Last Modified: Fri, 03 Dec 2021 16:37:29 GMT  
		Size: 185.2 MB (185204101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb1a3f2a620897e3ef5f866de2723c108b289d8308a9c3fea23ed2d98413c95`  
		Last Modified: Fri, 03 Dec 2021 20:43:19 GMT  
		Size: 292.4 MB (292388612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19092ac47724d18b94e705918c5687646e63dc774df241652ec6c77177eb0ad`  
		Last Modified: Fri, 03 Dec 2021 20:42:56 GMT  
		Size: 846.2 KB (846209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8959324a980da8d5711d1b493e27fea4054370769e11fe27b0341d928e7cad7b`  
		Last Modified: Fri, 03 Dec 2021 20:42:56 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3315518eeae081a901de36d667f5894a3bd974fdaa2943e8f6eff269b353b34d`  
		Last Modified: Fri, 03 Dec 2021 20:42:56 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b25a16e439c94dc4b0d402bdc659b525b4bc914799cb79e15e289e26f5eabdd7`  
		Last Modified: Fri, 03 Dec 2021 20:42:56 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0747fe5f75ab79fb9a9f111b719dec4f788fe07fcecc62412907b32ff5e2e9c`  
		Last Modified: Fri, 03 Dec 2021 20:42:56 GMT  
		Size: 2.5 KB (2500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13.4`

```console
$ docker pull xwiki@sha256:1e21933d29bd18c06cb518964881462a3d32e7a65be657a7aadc3ff55a9ad419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:13.4` - linux; amd64

```console
$ docker pull xwiki@sha256:c9e51c0a96a5c1a1bc2c452ad13fe6101c9088f62e052a540afd034195bcce36
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **723.3 MB (723289453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0e2e0b1cdcc31584120fcea351dcd515d273353019d89fd3a46aeb34fcaad6c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Sat, 16 Oct 2021 00:37:47 GMT
ADD file:5d68d27cc15a80653c93d3a0b262a28112d47a46326ff5fc2dfbf7fa3b9a0ce8 in / 
# Sat, 16 Oct 2021 00:37:47 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 02:44:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 29 Nov 2021 20:21:51 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 29 Nov 2021 20:22:21 GMT
ENV JAVA_VERSION=jdk-11.0.13+8
# Mon, 29 Nov 2021 20:22:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a77013bff10a5e9c59159231dd5c4bd071fc4c24beed42bd49b82803ba9506ef';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.13_8.tar.gz';          ;;        armhf|arm)          ESUM='61ee45c4ef21a85a116a87e1bca2e2a420b3af432be8d801bd52c660ffebaa9f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_arm_linux_hotspot_11.0.13_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='82f14cda71cff99c878bf8400598a87235adb6c81b0337f7077c27e5cac1190c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.13_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='9d280d86fdf6a7d9e5cbf54dc37f1d6d09dfe676ff5c684802fdfa3932eee63e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.13_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3b1c0c34be4c894e64135a454f2d5aaa4bd10aea04ec2fa0c0efe6bb26528e30';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.13_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 29 Nov 2021 20:22:33 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Nov 2021 20:22:34 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Mon, 29 Nov 2021 20:22:34 GMT
CMD ["jshell"]
# Tue, 30 Nov 2021 01:27:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 30 Nov 2021 01:27:42 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Nov 2021 01:27:42 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 30 Nov 2021 01:27:43 GMT
WORKDIR /usr/local/tomcat
# Tue, 30 Nov 2021 01:27:43 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 30 Nov 2021 01:27:43 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 30 Nov 2021 01:40:07 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 30 Nov 2021 01:40:07 GMT
ENV TOMCAT_MAJOR=8
# Tue, 30 Nov 2021 01:40:07 GMT
ENV TOMCAT_VERSION=8.5.73
# Tue, 30 Nov 2021 01:40:07 GMT
ENV TOMCAT_SHA512=4d33760d007acc5271ba0f946d2be96f6146d4632e411c9b72d351fc49d08355e8b84b051713a2f580e0f633cbe4409b7e9bb0e62f3af8d1094c6e4b3fdb96f0
# Tue, 30 Nov 2021 01:40:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Tue, 30 Nov 2021 01:40:49 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 30 Nov 2021 01:40:50 GMT
EXPOSE 8080
# Tue, 30 Nov 2021 01:40:50 GMT
CMD ["catalina.sh" "run"]
# Tue, 30 Nov 2021 09:39:43 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Tue, 30 Nov 2021 09:42:17 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 30 Nov 2021 09:46:20 GMT
ENV XWIKI_VERSION=13.4.5
# Tue, 30 Nov 2021 09:46:20 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.4.5
# Tue, 30 Nov 2021 09:46:21 GMT
ENV XWIKI_DOWNLOAD_SHA256=4cb70d74525813e55142f3246da5218c006790b8a77f4a0784fa86e01046e6e8
# Tue, 30 Nov 2021 09:47:01 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 30 Nov 2021 09:47:02 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Tue, 30 Nov 2021 09:47:02 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Tue, 30 Nov 2021 09:47:02 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Tue, 30 Nov 2021 09:47:02 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Tue, 30 Nov 2021 09:47:03 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Tue, 30 Nov 2021 09:47:04 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Tue, 30 Nov 2021 09:47:04 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 30 Nov 2021 09:47:04 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 30 Nov 2021 09:47:05 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 30 Nov 2021 09:47:05 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 30 Nov 2021 09:47:05 GMT
VOLUME [/usr/local/xwiki]
# Tue, 30 Nov 2021 09:47:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Nov 2021 09:47:06 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:7b1a6ab2e44dbac178598dabe7cff59bd67233dba0b27e4fbd1f9d4b3c877a54`  
		Last Modified: Thu, 07 Oct 2021 23:44:23 GMT  
		Size: 28.6 MB (28567101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c122ee837fa892e5fdd4f7c857600f80a7b8fa855d2475bb325372d55eaff04`  
		Last Modified: Mon, 29 Nov 2021 20:25:31 GMT  
		Size: 24.8 MB (24814948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df03d17a1d16d4f310f47ff0900289f9beec130c2f7a84d52ba93541c6f8f048`  
		Last Modified: Mon, 29 Nov 2021 20:26:21 GMT  
		Size: 193.8 MB (193801823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05d1597bd18adb0195f9d09ada1bc1261137834d5cb3b4ad5ee2cbc4e010261a`  
		Last Modified: Mon, 29 Nov 2021 20:26:07 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:717fd106c6af49e826736948af01d427d93170e8f8f066a5ffa923f3fca9e42d`  
		Last Modified: Tue, 30 Nov 2021 01:52:44 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f8b23582a59f35340387a2a4eb8c5530b353af32264f9336493ab3dc542bd59`  
		Last Modified: Tue, 30 Nov 2021 02:02:43 GMT  
		Size: 11.7 MB (11715854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba49d9e52fa20ba48959c0c396d028f3afe2626427eb9789fa3d3807b6911a7`  
		Last Modified: Tue, 30 Nov 2021 02:02:41 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2794b6353daa0dcb188e5b766ea4a556a25f1803cc514973ac17a0ba97b87440`  
		Last Modified: Tue, 30 Nov 2021 09:49:06 GMT  
		Size: 158.7 MB (158716143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16cd02a09b667d83ac9f29a36faf83d1c2b7e215c832bd0bad1c0d210f8f13c8`  
		Last Modified: Tue, 30 Nov 2021 09:52:28 GMT  
		Size: 303.4 MB (303403958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d443002d1baed689a280fd7243f2cf305f21bf53f713a3c6c0b2d25877b2155`  
		Last Modified: Tue, 30 Nov 2021 09:52:09 GMT  
		Size: 2.3 MB (2257827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e338cb6750edd410bbd5f67307d7c3353fd9e8eb7d169c351a5fec887f67a8`  
		Last Modified: Tue, 30 Nov 2021 09:52:09 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3be79c5a4d8d4505cdec257889ddb66dec5c4116d850f263724120bc9a625f`  
		Last Modified: Tue, 30 Nov 2021 09:52:09 GMT  
		Size: 2.3 KB (2316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7912b8364e0805f6e8a57ebfc2079550975c2af2647d273c4dd4515ed54a06f`  
		Last Modified: Tue, 30 Nov 2021 09:52:09 GMT  
		Size: 5.2 KB (5172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0da0254c87f35d551efcff22597fa45f4d50a63272a8bb71509922d2d8a6b386`  
		Last Modified: Tue, 30 Nov 2021 09:52:09 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13.4-mysql-tomcat`

```console
$ docker pull xwiki@sha256:1e21933d29bd18c06cb518964881462a3d32e7a65be657a7aadc3ff55a9ad419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:13.4-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:c9e51c0a96a5c1a1bc2c452ad13fe6101c9088f62e052a540afd034195bcce36
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **723.3 MB (723289453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0e2e0b1cdcc31584120fcea351dcd515d273353019d89fd3a46aeb34fcaad6c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Sat, 16 Oct 2021 00:37:47 GMT
ADD file:5d68d27cc15a80653c93d3a0b262a28112d47a46326ff5fc2dfbf7fa3b9a0ce8 in / 
# Sat, 16 Oct 2021 00:37:47 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 02:44:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 29 Nov 2021 20:21:51 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 29 Nov 2021 20:22:21 GMT
ENV JAVA_VERSION=jdk-11.0.13+8
# Mon, 29 Nov 2021 20:22:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a77013bff10a5e9c59159231dd5c4bd071fc4c24beed42bd49b82803ba9506ef';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.13_8.tar.gz';          ;;        armhf|arm)          ESUM='61ee45c4ef21a85a116a87e1bca2e2a420b3af432be8d801bd52c660ffebaa9f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_arm_linux_hotspot_11.0.13_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='82f14cda71cff99c878bf8400598a87235adb6c81b0337f7077c27e5cac1190c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.13_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='9d280d86fdf6a7d9e5cbf54dc37f1d6d09dfe676ff5c684802fdfa3932eee63e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.13_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3b1c0c34be4c894e64135a454f2d5aaa4bd10aea04ec2fa0c0efe6bb26528e30';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.13_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 29 Nov 2021 20:22:33 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Nov 2021 20:22:34 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Mon, 29 Nov 2021 20:22:34 GMT
CMD ["jshell"]
# Tue, 30 Nov 2021 01:27:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 30 Nov 2021 01:27:42 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Nov 2021 01:27:42 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 30 Nov 2021 01:27:43 GMT
WORKDIR /usr/local/tomcat
# Tue, 30 Nov 2021 01:27:43 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 30 Nov 2021 01:27:43 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 30 Nov 2021 01:40:07 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 30 Nov 2021 01:40:07 GMT
ENV TOMCAT_MAJOR=8
# Tue, 30 Nov 2021 01:40:07 GMT
ENV TOMCAT_VERSION=8.5.73
# Tue, 30 Nov 2021 01:40:07 GMT
ENV TOMCAT_SHA512=4d33760d007acc5271ba0f946d2be96f6146d4632e411c9b72d351fc49d08355e8b84b051713a2f580e0f633cbe4409b7e9bb0e62f3af8d1094c6e4b3fdb96f0
# Tue, 30 Nov 2021 01:40:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Tue, 30 Nov 2021 01:40:49 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 30 Nov 2021 01:40:50 GMT
EXPOSE 8080
# Tue, 30 Nov 2021 01:40:50 GMT
CMD ["catalina.sh" "run"]
# Tue, 30 Nov 2021 09:39:43 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Tue, 30 Nov 2021 09:42:17 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 30 Nov 2021 09:46:20 GMT
ENV XWIKI_VERSION=13.4.5
# Tue, 30 Nov 2021 09:46:20 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.4.5
# Tue, 30 Nov 2021 09:46:21 GMT
ENV XWIKI_DOWNLOAD_SHA256=4cb70d74525813e55142f3246da5218c006790b8a77f4a0784fa86e01046e6e8
# Tue, 30 Nov 2021 09:47:01 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 30 Nov 2021 09:47:02 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Tue, 30 Nov 2021 09:47:02 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Tue, 30 Nov 2021 09:47:02 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Tue, 30 Nov 2021 09:47:02 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Tue, 30 Nov 2021 09:47:03 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Tue, 30 Nov 2021 09:47:04 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Tue, 30 Nov 2021 09:47:04 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 30 Nov 2021 09:47:04 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 30 Nov 2021 09:47:05 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 30 Nov 2021 09:47:05 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 30 Nov 2021 09:47:05 GMT
VOLUME [/usr/local/xwiki]
# Tue, 30 Nov 2021 09:47:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Nov 2021 09:47:06 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:7b1a6ab2e44dbac178598dabe7cff59bd67233dba0b27e4fbd1f9d4b3c877a54`  
		Last Modified: Thu, 07 Oct 2021 23:44:23 GMT  
		Size: 28.6 MB (28567101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c122ee837fa892e5fdd4f7c857600f80a7b8fa855d2475bb325372d55eaff04`  
		Last Modified: Mon, 29 Nov 2021 20:25:31 GMT  
		Size: 24.8 MB (24814948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df03d17a1d16d4f310f47ff0900289f9beec130c2f7a84d52ba93541c6f8f048`  
		Last Modified: Mon, 29 Nov 2021 20:26:21 GMT  
		Size: 193.8 MB (193801823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05d1597bd18adb0195f9d09ada1bc1261137834d5cb3b4ad5ee2cbc4e010261a`  
		Last Modified: Mon, 29 Nov 2021 20:26:07 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:717fd106c6af49e826736948af01d427d93170e8f8f066a5ffa923f3fca9e42d`  
		Last Modified: Tue, 30 Nov 2021 01:52:44 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f8b23582a59f35340387a2a4eb8c5530b353af32264f9336493ab3dc542bd59`  
		Last Modified: Tue, 30 Nov 2021 02:02:43 GMT  
		Size: 11.7 MB (11715854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba49d9e52fa20ba48959c0c396d028f3afe2626427eb9789fa3d3807b6911a7`  
		Last Modified: Tue, 30 Nov 2021 02:02:41 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2794b6353daa0dcb188e5b766ea4a556a25f1803cc514973ac17a0ba97b87440`  
		Last Modified: Tue, 30 Nov 2021 09:49:06 GMT  
		Size: 158.7 MB (158716143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16cd02a09b667d83ac9f29a36faf83d1c2b7e215c832bd0bad1c0d210f8f13c8`  
		Last Modified: Tue, 30 Nov 2021 09:52:28 GMT  
		Size: 303.4 MB (303403958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d443002d1baed689a280fd7243f2cf305f21bf53f713a3c6c0b2d25877b2155`  
		Last Modified: Tue, 30 Nov 2021 09:52:09 GMT  
		Size: 2.3 MB (2257827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e338cb6750edd410bbd5f67307d7c3353fd9e8eb7d169c351a5fec887f67a8`  
		Last Modified: Tue, 30 Nov 2021 09:52:09 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3be79c5a4d8d4505cdec257889ddb66dec5c4116d850f263724120bc9a625f`  
		Last Modified: Tue, 30 Nov 2021 09:52:09 GMT  
		Size: 2.3 KB (2316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7912b8364e0805f6e8a57ebfc2079550975c2af2647d273c4dd4515ed54a06f`  
		Last Modified: Tue, 30 Nov 2021 09:52:09 GMT  
		Size: 5.2 KB (5172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0da0254c87f35d551efcff22597fa45f4d50a63272a8bb71509922d2d8a6b386`  
		Last Modified: Tue, 30 Nov 2021 09:52:09 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13.4-postgres-tomcat`

```console
$ docker pull xwiki@sha256:5e23080acc366c3f591f9b49a9b2a12b3d1f0035cb4dec430ec60fe1191f270b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:13.4-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:0a9e9b8187595e780f2df0d4a7c9aec45846e85e712faeb1b9288844f0f8fb2a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.6 MB (722627946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfaf1387fab202c643b0cfa7e592c28d338bdc36c6db40bdf6d4d584584964c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Sat, 16 Oct 2021 00:37:47 GMT
ADD file:5d68d27cc15a80653c93d3a0b262a28112d47a46326ff5fc2dfbf7fa3b9a0ce8 in / 
# Sat, 16 Oct 2021 00:37:47 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 02:44:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 29 Nov 2021 20:21:51 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 29 Nov 2021 20:22:21 GMT
ENV JAVA_VERSION=jdk-11.0.13+8
# Mon, 29 Nov 2021 20:22:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a77013bff10a5e9c59159231dd5c4bd071fc4c24beed42bd49b82803ba9506ef';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.13_8.tar.gz';          ;;        armhf|arm)          ESUM='61ee45c4ef21a85a116a87e1bca2e2a420b3af432be8d801bd52c660ffebaa9f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_arm_linux_hotspot_11.0.13_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='82f14cda71cff99c878bf8400598a87235adb6c81b0337f7077c27e5cac1190c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.13_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='9d280d86fdf6a7d9e5cbf54dc37f1d6d09dfe676ff5c684802fdfa3932eee63e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.13_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3b1c0c34be4c894e64135a454f2d5aaa4bd10aea04ec2fa0c0efe6bb26528e30';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.13_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 29 Nov 2021 20:22:33 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Nov 2021 20:22:34 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Mon, 29 Nov 2021 20:22:34 GMT
CMD ["jshell"]
# Tue, 30 Nov 2021 01:27:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 30 Nov 2021 01:27:42 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Nov 2021 01:27:42 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 30 Nov 2021 01:27:43 GMT
WORKDIR /usr/local/tomcat
# Tue, 30 Nov 2021 01:27:43 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 30 Nov 2021 01:27:43 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 30 Nov 2021 01:40:07 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 30 Nov 2021 01:40:07 GMT
ENV TOMCAT_MAJOR=8
# Tue, 30 Nov 2021 01:40:07 GMT
ENV TOMCAT_VERSION=8.5.73
# Tue, 30 Nov 2021 01:40:07 GMT
ENV TOMCAT_SHA512=4d33760d007acc5271ba0f946d2be96f6146d4632e411c9b72d351fc49d08355e8b84b051713a2f580e0f633cbe4409b7e9bb0e62f3af8d1094c6e4b3fdb96f0
# Tue, 30 Nov 2021 01:40:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Tue, 30 Nov 2021 01:40:49 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 30 Nov 2021 01:40:50 GMT
EXPOSE 8080
# Tue, 30 Nov 2021 01:40:50 GMT
CMD ["catalina.sh" "run"]
# Tue, 30 Nov 2021 09:39:43 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Tue, 30 Nov 2021 09:43:54 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Tue, 30 Nov 2021 09:47:09 GMT
ENV XWIKI_VERSION=13.4.5
# Tue, 30 Nov 2021 09:47:09 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.4.5
# Tue, 30 Nov 2021 09:47:09 GMT
ENV XWIKI_DOWNLOAD_SHA256=4cb70d74525813e55142f3246da5218c006790b8a77f4a0784fa86e01046e6e8
# Tue, 30 Nov 2021 09:47:48 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 30 Nov 2021 09:47:51 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Tue, 30 Nov 2021 09:47:51 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 30 Nov 2021 09:47:51 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 30 Nov 2021 09:47:52 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 30 Nov 2021 09:47:53 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 30 Nov 2021 09:47:53 GMT
VOLUME [/usr/local/xwiki]
# Tue, 30 Nov 2021 09:47:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Nov 2021 09:47:53 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:7b1a6ab2e44dbac178598dabe7cff59bd67233dba0b27e4fbd1f9d4b3c877a54`  
		Last Modified: Thu, 07 Oct 2021 23:44:23 GMT  
		Size: 28.6 MB (28567101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c122ee837fa892e5fdd4f7c857600f80a7b8fa855d2475bb325372d55eaff04`  
		Last Modified: Mon, 29 Nov 2021 20:25:31 GMT  
		Size: 24.8 MB (24814948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df03d17a1d16d4f310f47ff0900289f9beec130c2f7a84d52ba93541c6f8f048`  
		Last Modified: Mon, 29 Nov 2021 20:26:21 GMT  
		Size: 193.8 MB (193801823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05d1597bd18adb0195f9d09ada1bc1261137834d5cb3b4ad5ee2cbc4e010261a`  
		Last Modified: Mon, 29 Nov 2021 20:26:07 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:717fd106c6af49e826736948af01d427d93170e8f8f066a5ffa923f3fca9e42d`  
		Last Modified: Tue, 30 Nov 2021 01:52:44 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f8b23582a59f35340387a2a4eb8c5530b353af32264f9336493ab3dc542bd59`  
		Last Modified: Tue, 30 Nov 2021 02:02:43 GMT  
		Size: 11.7 MB (11715854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba49d9e52fa20ba48959c0c396d028f3afe2626427eb9789fa3d3807b6911a7`  
		Last Modified: Tue, 30 Nov 2021 02:02:41 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44aa2597bc2f761695888ffdfb30b757ae13010ccd9b6b5a5424fea9ff7742cb`  
		Last Modified: Tue, 30 Nov 2021 09:50:12 GMT  
		Size: 159.5 MB (159516889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bd0475c2ce00cb2a9fc26ea990302ff713a02705d4a14f05e7cffbd558aa935`  
		Last Modified: Tue, 30 Nov 2021 09:53:03 GMT  
		Size: 303.4 MB (303403961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec6ec6af8ee497dbd32a1607292aea3f6ba3a00c9950144774d52db6012b86ae`  
		Last Modified: Tue, 30 Nov 2021 09:52:45 GMT  
		Size: 795.4 KB (795418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c7aadecbe511cab8f9e76c7515f792c8e79de11590617497c54281696e9648c`  
		Last Modified: Tue, 30 Nov 2021 09:52:44 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8937ca2eac7b237e8fbb3bea023af9008d408f52f10b4d7528abcc8f897274c4`  
		Last Modified: Tue, 30 Nov 2021 09:52:44 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd96297e8f1ea791e66adea13987f72342d29dfbcb16911abd1f278d21996690`  
		Last Modified: Tue, 30 Nov 2021 09:52:44 GMT  
		Size: 5.2 KB (5172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12155b3dec676fc427f05923079ccc1b3146a7bd125d2f535409d9637013baac`  
		Last Modified: Tue, 30 Nov 2021 09:52:44 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:13.4-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:cce59b4ef05c7b2b63764083d74152aa059f946b4b5d7a7c9a8df42e32146104
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **713.5 MB (713457382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6429e34a1646818fbdffa2ad4d326f954155fc501000048985abbed568630184`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Sat, 16 Oct 2021 01:47:45 GMT
ADD file:ff4909f2124325dac58d43c617132325934ed48a5ab4c534d05f931fcf700a2f in / 
# Sat, 16 Oct 2021 01:47:45 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 03:25:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 29 Nov 2021 19:40:01 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 29 Nov 2021 19:40:43 GMT
ENV JAVA_VERSION=jdk-11.0.13+8
# Mon, 29 Nov 2021 19:40:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a77013bff10a5e9c59159231dd5c4bd071fc4c24beed42bd49b82803ba9506ef';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.13_8.tar.gz';          ;;        armhf|arm)          ESUM='61ee45c4ef21a85a116a87e1bca2e2a420b3af432be8d801bd52c660ffebaa9f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_arm_linux_hotspot_11.0.13_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='82f14cda71cff99c878bf8400598a87235adb6c81b0337f7077c27e5cac1190c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.13_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='9d280d86fdf6a7d9e5cbf54dc37f1d6d09dfe676ff5c684802fdfa3932eee63e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.13_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3b1c0c34be4c894e64135a454f2d5aaa4bd10aea04ec2fa0c0efe6bb26528e30';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.13_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 29 Nov 2021 19:40:54 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Nov 2021 19:40:56 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Mon, 29 Nov 2021 19:40:57 GMT
CMD ["jshell"]
# Mon, 29 Nov 2021 21:17:19 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 29 Nov 2021 21:17:19 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Nov 2021 21:17:20 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 29 Nov 2021 21:17:21 GMT
WORKDIR /usr/local/tomcat
# Mon, 29 Nov 2021 21:17:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 29 Nov 2021 21:17:23 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 29 Nov 2021 21:34:34 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Mon, 29 Nov 2021 21:34:34 GMT
ENV TOMCAT_MAJOR=8
# Mon, 29 Nov 2021 21:34:35 GMT
ENV TOMCAT_VERSION=8.5.73
# Mon, 29 Nov 2021 21:34:36 GMT
ENV TOMCAT_SHA512=4d33760d007acc5271ba0f946d2be96f6146d4632e411c9b72d351fc49d08355e8b84b051713a2f580e0f633cbe4409b7e9bb0e62f3af8d1094c6e4b3fdb96f0
# Mon, 29 Nov 2021 21:35:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Mon, 29 Nov 2021 21:35:19 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Mon, 29 Nov 2021 21:35:19 GMT
EXPOSE 8080
# Mon, 29 Nov 2021 21:35:20 GMT
CMD ["catalina.sh" "run"]
# Mon, 29 Nov 2021 22:27:59 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Mon, 29 Nov 2021 22:28:37 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Mon, 29 Nov 2021 22:32:08 GMT
ENV XWIKI_VERSION=13.4.5
# Mon, 29 Nov 2021 22:32:09 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.4.5
# Mon, 29 Nov 2021 22:32:09 GMT
ENV XWIKI_DOWNLOAD_SHA256=4cb70d74525813e55142f3246da5218c006790b8a77f4a0784fa86e01046e6e8
# Mon, 29 Nov 2021 22:33:29 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Mon, 29 Nov 2021 22:33:30 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Mon, 29 Nov 2021 22:33:31 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Mon, 29 Nov 2021 22:33:32 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Mon, 29 Nov 2021 22:33:33 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Mon, 29 Nov 2021 22:33:34 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Mon, 29 Nov 2021 22:33:34 GMT
VOLUME [/usr/local/xwiki]
# Mon, 29 Nov 2021 22:33:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Nov 2021 22:33:36 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:a39c84e173f038958d338f55a9e8ee64bb6643e8ac6ae98e08ca65146e668d86`  
		Last Modified: Sat, 09 Oct 2021 15:32:18 GMT  
		Size: 27.2 MB (27170900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa42563dc02061b51ce62bff7340de9cea06ea720e8658d2a7693902aa8f700`  
		Last Modified: Mon, 29 Nov 2021 19:44:11 GMT  
		Size: 24.8 MB (24763049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77dd3dbd51783712818d90400820b5551c26f9e95104696e464e50825f558696`  
		Last Modified: Mon, 29 Nov 2021 19:45:13 GMT  
		Size: 190.5 MB (190512910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d56062c543a893b6c3d9bcc6775756d6debb5e849c02ba88d0d340523e6716a`  
		Last Modified: Mon, 29 Nov 2021 19:44:48 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:093c7df785877b00b055e2251b5b23c8563d6b4b8c4b3aa854596360557161d2`  
		Last Modified: Mon, 29 Nov 2021 21:56:01 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd78c30d612f0efcbedc574e44a2ad22bd91511b439b9b597605925512d0f64`  
		Last Modified: Mon, 29 Nov 2021 22:07:31 GMT  
		Size: 11.5 MB (11494827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e17fa2e98d378f2b12e1473caf2bc3b7642a888a5ef3bd0b6f68334ab6e2639`  
		Last Modified: Mon, 29 Nov 2021 22:34:38 GMT  
		Size: 155.3 MB (155304821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf960b0bca1c8791867458967c1f0ee46bfe1bb8c98e2c5f08544520c59f5dd1`  
		Last Modified: Mon, 29 Nov 2021 22:36:12 GMT  
		Size: 303.4 MB (303403692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2870c756160c6e7d97499c6aac0dcfdc792ce65568eba224f58097156f2e38`  
		Last Modified: Mon, 29 Nov 2021 22:35:50 GMT  
		Size: 795.4 KB (795420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d4e71364735c47ecec7229fb4fd45e410d92f048cd63d7adf0c3b4a491b99e6`  
		Last Modified: Mon, 29 Nov 2021 22:35:49 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:234d5215f92891ba0bf18c8baf28290bd0d08fd908dddea8dd378a245740af53`  
		Last Modified: Mon, 29 Nov 2021 22:35:50 GMT  
		Size: 2.5 KB (2467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e558095c54434d508864b8a4c17bc9c55a9f0b702dd05defa2daac5a38c0f0fd`  
		Last Modified: Mon, 29 Nov 2021 22:35:49 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66782e31fb66ffa7ea507d07f3e765e04a747b3e53bcf8fbe40afef11d6cc429`  
		Last Modified: Mon, 29 Nov 2021 22:35:50 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13.4.5`

```console
$ docker pull xwiki@sha256:1e21933d29bd18c06cb518964881462a3d32e7a65be657a7aadc3ff55a9ad419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:13.4.5` - linux; amd64

```console
$ docker pull xwiki@sha256:c9e51c0a96a5c1a1bc2c452ad13fe6101c9088f62e052a540afd034195bcce36
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **723.3 MB (723289453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0e2e0b1cdcc31584120fcea351dcd515d273353019d89fd3a46aeb34fcaad6c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Sat, 16 Oct 2021 00:37:47 GMT
ADD file:5d68d27cc15a80653c93d3a0b262a28112d47a46326ff5fc2dfbf7fa3b9a0ce8 in / 
# Sat, 16 Oct 2021 00:37:47 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 02:44:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 29 Nov 2021 20:21:51 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 29 Nov 2021 20:22:21 GMT
ENV JAVA_VERSION=jdk-11.0.13+8
# Mon, 29 Nov 2021 20:22:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a77013bff10a5e9c59159231dd5c4bd071fc4c24beed42bd49b82803ba9506ef';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.13_8.tar.gz';          ;;        armhf|arm)          ESUM='61ee45c4ef21a85a116a87e1bca2e2a420b3af432be8d801bd52c660ffebaa9f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_arm_linux_hotspot_11.0.13_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='82f14cda71cff99c878bf8400598a87235adb6c81b0337f7077c27e5cac1190c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.13_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='9d280d86fdf6a7d9e5cbf54dc37f1d6d09dfe676ff5c684802fdfa3932eee63e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.13_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3b1c0c34be4c894e64135a454f2d5aaa4bd10aea04ec2fa0c0efe6bb26528e30';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.13_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 29 Nov 2021 20:22:33 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Nov 2021 20:22:34 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Mon, 29 Nov 2021 20:22:34 GMT
CMD ["jshell"]
# Tue, 30 Nov 2021 01:27:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 30 Nov 2021 01:27:42 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Nov 2021 01:27:42 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 30 Nov 2021 01:27:43 GMT
WORKDIR /usr/local/tomcat
# Tue, 30 Nov 2021 01:27:43 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 30 Nov 2021 01:27:43 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 30 Nov 2021 01:40:07 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 30 Nov 2021 01:40:07 GMT
ENV TOMCAT_MAJOR=8
# Tue, 30 Nov 2021 01:40:07 GMT
ENV TOMCAT_VERSION=8.5.73
# Tue, 30 Nov 2021 01:40:07 GMT
ENV TOMCAT_SHA512=4d33760d007acc5271ba0f946d2be96f6146d4632e411c9b72d351fc49d08355e8b84b051713a2f580e0f633cbe4409b7e9bb0e62f3af8d1094c6e4b3fdb96f0
# Tue, 30 Nov 2021 01:40:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Tue, 30 Nov 2021 01:40:49 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 30 Nov 2021 01:40:50 GMT
EXPOSE 8080
# Tue, 30 Nov 2021 01:40:50 GMT
CMD ["catalina.sh" "run"]
# Tue, 30 Nov 2021 09:39:43 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Tue, 30 Nov 2021 09:42:17 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 30 Nov 2021 09:46:20 GMT
ENV XWIKI_VERSION=13.4.5
# Tue, 30 Nov 2021 09:46:20 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.4.5
# Tue, 30 Nov 2021 09:46:21 GMT
ENV XWIKI_DOWNLOAD_SHA256=4cb70d74525813e55142f3246da5218c006790b8a77f4a0784fa86e01046e6e8
# Tue, 30 Nov 2021 09:47:01 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 30 Nov 2021 09:47:02 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Tue, 30 Nov 2021 09:47:02 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Tue, 30 Nov 2021 09:47:02 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Tue, 30 Nov 2021 09:47:02 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Tue, 30 Nov 2021 09:47:03 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Tue, 30 Nov 2021 09:47:04 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Tue, 30 Nov 2021 09:47:04 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 30 Nov 2021 09:47:04 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 30 Nov 2021 09:47:05 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 30 Nov 2021 09:47:05 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 30 Nov 2021 09:47:05 GMT
VOLUME [/usr/local/xwiki]
# Tue, 30 Nov 2021 09:47:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Nov 2021 09:47:06 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:7b1a6ab2e44dbac178598dabe7cff59bd67233dba0b27e4fbd1f9d4b3c877a54`  
		Last Modified: Thu, 07 Oct 2021 23:44:23 GMT  
		Size: 28.6 MB (28567101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c122ee837fa892e5fdd4f7c857600f80a7b8fa855d2475bb325372d55eaff04`  
		Last Modified: Mon, 29 Nov 2021 20:25:31 GMT  
		Size: 24.8 MB (24814948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df03d17a1d16d4f310f47ff0900289f9beec130c2f7a84d52ba93541c6f8f048`  
		Last Modified: Mon, 29 Nov 2021 20:26:21 GMT  
		Size: 193.8 MB (193801823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05d1597bd18adb0195f9d09ada1bc1261137834d5cb3b4ad5ee2cbc4e010261a`  
		Last Modified: Mon, 29 Nov 2021 20:26:07 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:717fd106c6af49e826736948af01d427d93170e8f8f066a5ffa923f3fca9e42d`  
		Last Modified: Tue, 30 Nov 2021 01:52:44 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f8b23582a59f35340387a2a4eb8c5530b353af32264f9336493ab3dc542bd59`  
		Last Modified: Tue, 30 Nov 2021 02:02:43 GMT  
		Size: 11.7 MB (11715854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba49d9e52fa20ba48959c0c396d028f3afe2626427eb9789fa3d3807b6911a7`  
		Last Modified: Tue, 30 Nov 2021 02:02:41 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2794b6353daa0dcb188e5b766ea4a556a25f1803cc514973ac17a0ba97b87440`  
		Last Modified: Tue, 30 Nov 2021 09:49:06 GMT  
		Size: 158.7 MB (158716143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16cd02a09b667d83ac9f29a36faf83d1c2b7e215c832bd0bad1c0d210f8f13c8`  
		Last Modified: Tue, 30 Nov 2021 09:52:28 GMT  
		Size: 303.4 MB (303403958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d443002d1baed689a280fd7243f2cf305f21bf53f713a3c6c0b2d25877b2155`  
		Last Modified: Tue, 30 Nov 2021 09:52:09 GMT  
		Size: 2.3 MB (2257827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e338cb6750edd410bbd5f67307d7c3353fd9e8eb7d169c351a5fec887f67a8`  
		Last Modified: Tue, 30 Nov 2021 09:52:09 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3be79c5a4d8d4505cdec257889ddb66dec5c4116d850f263724120bc9a625f`  
		Last Modified: Tue, 30 Nov 2021 09:52:09 GMT  
		Size: 2.3 KB (2316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7912b8364e0805f6e8a57ebfc2079550975c2af2647d273c4dd4515ed54a06f`  
		Last Modified: Tue, 30 Nov 2021 09:52:09 GMT  
		Size: 5.2 KB (5172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0da0254c87f35d551efcff22597fa45f4d50a63272a8bb71509922d2d8a6b386`  
		Last Modified: Tue, 30 Nov 2021 09:52:09 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13.4.5-mysql-tomcat`

```console
$ docker pull xwiki@sha256:1e21933d29bd18c06cb518964881462a3d32e7a65be657a7aadc3ff55a9ad419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:13.4.5-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:c9e51c0a96a5c1a1bc2c452ad13fe6101c9088f62e052a540afd034195bcce36
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **723.3 MB (723289453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0e2e0b1cdcc31584120fcea351dcd515d273353019d89fd3a46aeb34fcaad6c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Sat, 16 Oct 2021 00:37:47 GMT
ADD file:5d68d27cc15a80653c93d3a0b262a28112d47a46326ff5fc2dfbf7fa3b9a0ce8 in / 
# Sat, 16 Oct 2021 00:37:47 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 02:44:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 29 Nov 2021 20:21:51 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 29 Nov 2021 20:22:21 GMT
ENV JAVA_VERSION=jdk-11.0.13+8
# Mon, 29 Nov 2021 20:22:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a77013bff10a5e9c59159231dd5c4bd071fc4c24beed42bd49b82803ba9506ef';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.13_8.tar.gz';          ;;        armhf|arm)          ESUM='61ee45c4ef21a85a116a87e1bca2e2a420b3af432be8d801bd52c660ffebaa9f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_arm_linux_hotspot_11.0.13_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='82f14cda71cff99c878bf8400598a87235adb6c81b0337f7077c27e5cac1190c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.13_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='9d280d86fdf6a7d9e5cbf54dc37f1d6d09dfe676ff5c684802fdfa3932eee63e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.13_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3b1c0c34be4c894e64135a454f2d5aaa4bd10aea04ec2fa0c0efe6bb26528e30';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.13_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 29 Nov 2021 20:22:33 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Nov 2021 20:22:34 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Mon, 29 Nov 2021 20:22:34 GMT
CMD ["jshell"]
# Tue, 30 Nov 2021 01:27:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 30 Nov 2021 01:27:42 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Nov 2021 01:27:42 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 30 Nov 2021 01:27:43 GMT
WORKDIR /usr/local/tomcat
# Tue, 30 Nov 2021 01:27:43 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 30 Nov 2021 01:27:43 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 30 Nov 2021 01:40:07 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 30 Nov 2021 01:40:07 GMT
ENV TOMCAT_MAJOR=8
# Tue, 30 Nov 2021 01:40:07 GMT
ENV TOMCAT_VERSION=8.5.73
# Tue, 30 Nov 2021 01:40:07 GMT
ENV TOMCAT_SHA512=4d33760d007acc5271ba0f946d2be96f6146d4632e411c9b72d351fc49d08355e8b84b051713a2f580e0f633cbe4409b7e9bb0e62f3af8d1094c6e4b3fdb96f0
# Tue, 30 Nov 2021 01:40:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Tue, 30 Nov 2021 01:40:49 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 30 Nov 2021 01:40:50 GMT
EXPOSE 8080
# Tue, 30 Nov 2021 01:40:50 GMT
CMD ["catalina.sh" "run"]
# Tue, 30 Nov 2021 09:39:43 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Tue, 30 Nov 2021 09:42:17 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 30 Nov 2021 09:46:20 GMT
ENV XWIKI_VERSION=13.4.5
# Tue, 30 Nov 2021 09:46:20 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.4.5
# Tue, 30 Nov 2021 09:46:21 GMT
ENV XWIKI_DOWNLOAD_SHA256=4cb70d74525813e55142f3246da5218c006790b8a77f4a0784fa86e01046e6e8
# Tue, 30 Nov 2021 09:47:01 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 30 Nov 2021 09:47:02 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Tue, 30 Nov 2021 09:47:02 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Tue, 30 Nov 2021 09:47:02 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Tue, 30 Nov 2021 09:47:02 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Tue, 30 Nov 2021 09:47:03 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Tue, 30 Nov 2021 09:47:04 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Tue, 30 Nov 2021 09:47:04 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 30 Nov 2021 09:47:04 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 30 Nov 2021 09:47:05 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 30 Nov 2021 09:47:05 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 30 Nov 2021 09:47:05 GMT
VOLUME [/usr/local/xwiki]
# Tue, 30 Nov 2021 09:47:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Nov 2021 09:47:06 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:7b1a6ab2e44dbac178598dabe7cff59bd67233dba0b27e4fbd1f9d4b3c877a54`  
		Last Modified: Thu, 07 Oct 2021 23:44:23 GMT  
		Size: 28.6 MB (28567101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c122ee837fa892e5fdd4f7c857600f80a7b8fa855d2475bb325372d55eaff04`  
		Last Modified: Mon, 29 Nov 2021 20:25:31 GMT  
		Size: 24.8 MB (24814948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df03d17a1d16d4f310f47ff0900289f9beec130c2f7a84d52ba93541c6f8f048`  
		Last Modified: Mon, 29 Nov 2021 20:26:21 GMT  
		Size: 193.8 MB (193801823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05d1597bd18adb0195f9d09ada1bc1261137834d5cb3b4ad5ee2cbc4e010261a`  
		Last Modified: Mon, 29 Nov 2021 20:26:07 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:717fd106c6af49e826736948af01d427d93170e8f8f066a5ffa923f3fca9e42d`  
		Last Modified: Tue, 30 Nov 2021 01:52:44 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f8b23582a59f35340387a2a4eb8c5530b353af32264f9336493ab3dc542bd59`  
		Last Modified: Tue, 30 Nov 2021 02:02:43 GMT  
		Size: 11.7 MB (11715854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba49d9e52fa20ba48959c0c396d028f3afe2626427eb9789fa3d3807b6911a7`  
		Last Modified: Tue, 30 Nov 2021 02:02:41 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2794b6353daa0dcb188e5b766ea4a556a25f1803cc514973ac17a0ba97b87440`  
		Last Modified: Tue, 30 Nov 2021 09:49:06 GMT  
		Size: 158.7 MB (158716143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16cd02a09b667d83ac9f29a36faf83d1c2b7e215c832bd0bad1c0d210f8f13c8`  
		Last Modified: Tue, 30 Nov 2021 09:52:28 GMT  
		Size: 303.4 MB (303403958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d443002d1baed689a280fd7243f2cf305f21bf53f713a3c6c0b2d25877b2155`  
		Last Modified: Tue, 30 Nov 2021 09:52:09 GMT  
		Size: 2.3 MB (2257827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e338cb6750edd410bbd5f67307d7c3353fd9e8eb7d169c351a5fec887f67a8`  
		Last Modified: Tue, 30 Nov 2021 09:52:09 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3be79c5a4d8d4505cdec257889ddb66dec5c4116d850f263724120bc9a625f`  
		Last Modified: Tue, 30 Nov 2021 09:52:09 GMT  
		Size: 2.3 KB (2316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7912b8364e0805f6e8a57ebfc2079550975c2af2647d273c4dd4515ed54a06f`  
		Last Modified: Tue, 30 Nov 2021 09:52:09 GMT  
		Size: 5.2 KB (5172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0da0254c87f35d551efcff22597fa45f4d50a63272a8bb71509922d2d8a6b386`  
		Last Modified: Tue, 30 Nov 2021 09:52:09 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13.4.5-postgres-tomcat`

```console
$ docker pull xwiki@sha256:5e23080acc366c3f591f9b49a9b2a12b3d1f0035cb4dec430ec60fe1191f270b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:13.4.5-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:0a9e9b8187595e780f2df0d4a7c9aec45846e85e712faeb1b9288844f0f8fb2a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.6 MB (722627946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfaf1387fab202c643b0cfa7e592c28d338bdc36c6db40bdf6d4d584584964c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Sat, 16 Oct 2021 00:37:47 GMT
ADD file:5d68d27cc15a80653c93d3a0b262a28112d47a46326ff5fc2dfbf7fa3b9a0ce8 in / 
# Sat, 16 Oct 2021 00:37:47 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 02:44:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 29 Nov 2021 20:21:51 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 29 Nov 2021 20:22:21 GMT
ENV JAVA_VERSION=jdk-11.0.13+8
# Mon, 29 Nov 2021 20:22:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a77013bff10a5e9c59159231dd5c4bd071fc4c24beed42bd49b82803ba9506ef';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.13_8.tar.gz';          ;;        armhf|arm)          ESUM='61ee45c4ef21a85a116a87e1bca2e2a420b3af432be8d801bd52c660ffebaa9f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_arm_linux_hotspot_11.0.13_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='82f14cda71cff99c878bf8400598a87235adb6c81b0337f7077c27e5cac1190c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.13_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='9d280d86fdf6a7d9e5cbf54dc37f1d6d09dfe676ff5c684802fdfa3932eee63e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.13_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3b1c0c34be4c894e64135a454f2d5aaa4bd10aea04ec2fa0c0efe6bb26528e30';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.13_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 29 Nov 2021 20:22:33 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Nov 2021 20:22:34 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Mon, 29 Nov 2021 20:22:34 GMT
CMD ["jshell"]
# Tue, 30 Nov 2021 01:27:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 30 Nov 2021 01:27:42 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Nov 2021 01:27:42 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 30 Nov 2021 01:27:43 GMT
WORKDIR /usr/local/tomcat
# Tue, 30 Nov 2021 01:27:43 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 30 Nov 2021 01:27:43 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 30 Nov 2021 01:40:07 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 30 Nov 2021 01:40:07 GMT
ENV TOMCAT_MAJOR=8
# Tue, 30 Nov 2021 01:40:07 GMT
ENV TOMCAT_VERSION=8.5.73
# Tue, 30 Nov 2021 01:40:07 GMT
ENV TOMCAT_SHA512=4d33760d007acc5271ba0f946d2be96f6146d4632e411c9b72d351fc49d08355e8b84b051713a2f580e0f633cbe4409b7e9bb0e62f3af8d1094c6e4b3fdb96f0
# Tue, 30 Nov 2021 01:40:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Tue, 30 Nov 2021 01:40:49 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 30 Nov 2021 01:40:50 GMT
EXPOSE 8080
# Tue, 30 Nov 2021 01:40:50 GMT
CMD ["catalina.sh" "run"]
# Tue, 30 Nov 2021 09:39:43 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Tue, 30 Nov 2021 09:43:54 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Tue, 30 Nov 2021 09:47:09 GMT
ENV XWIKI_VERSION=13.4.5
# Tue, 30 Nov 2021 09:47:09 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.4.5
# Tue, 30 Nov 2021 09:47:09 GMT
ENV XWIKI_DOWNLOAD_SHA256=4cb70d74525813e55142f3246da5218c006790b8a77f4a0784fa86e01046e6e8
# Tue, 30 Nov 2021 09:47:48 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 30 Nov 2021 09:47:51 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Tue, 30 Nov 2021 09:47:51 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 30 Nov 2021 09:47:51 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 30 Nov 2021 09:47:52 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 30 Nov 2021 09:47:53 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 30 Nov 2021 09:47:53 GMT
VOLUME [/usr/local/xwiki]
# Tue, 30 Nov 2021 09:47:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Nov 2021 09:47:53 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:7b1a6ab2e44dbac178598dabe7cff59bd67233dba0b27e4fbd1f9d4b3c877a54`  
		Last Modified: Thu, 07 Oct 2021 23:44:23 GMT  
		Size: 28.6 MB (28567101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c122ee837fa892e5fdd4f7c857600f80a7b8fa855d2475bb325372d55eaff04`  
		Last Modified: Mon, 29 Nov 2021 20:25:31 GMT  
		Size: 24.8 MB (24814948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df03d17a1d16d4f310f47ff0900289f9beec130c2f7a84d52ba93541c6f8f048`  
		Last Modified: Mon, 29 Nov 2021 20:26:21 GMT  
		Size: 193.8 MB (193801823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05d1597bd18adb0195f9d09ada1bc1261137834d5cb3b4ad5ee2cbc4e010261a`  
		Last Modified: Mon, 29 Nov 2021 20:26:07 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:717fd106c6af49e826736948af01d427d93170e8f8f066a5ffa923f3fca9e42d`  
		Last Modified: Tue, 30 Nov 2021 01:52:44 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f8b23582a59f35340387a2a4eb8c5530b353af32264f9336493ab3dc542bd59`  
		Last Modified: Tue, 30 Nov 2021 02:02:43 GMT  
		Size: 11.7 MB (11715854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba49d9e52fa20ba48959c0c396d028f3afe2626427eb9789fa3d3807b6911a7`  
		Last Modified: Tue, 30 Nov 2021 02:02:41 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44aa2597bc2f761695888ffdfb30b757ae13010ccd9b6b5a5424fea9ff7742cb`  
		Last Modified: Tue, 30 Nov 2021 09:50:12 GMT  
		Size: 159.5 MB (159516889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bd0475c2ce00cb2a9fc26ea990302ff713a02705d4a14f05e7cffbd558aa935`  
		Last Modified: Tue, 30 Nov 2021 09:53:03 GMT  
		Size: 303.4 MB (303403961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec6ec6af8ee497dbd32a1607292aea3f6ba3a00c9950144774d52db6012b86ae`  
		Last Modified: Tue, 30 Nov 2021 09:52:45 GMT  
		Size: 795.4 KB (795418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c7aadecbe511cab8f9e76c7515f792c8e79de11590617497c54281696e9648c`  
		Last Modified: Tue, 30 Nov 2021 09:52:44 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8937ca2eac7b237e8fbb3bea023af9008d408f52f10b4d7528abcc8f897274c4`  
		Last Modified: Tue, 30 Nov 2021 09:52:44 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd96297e8f1ea791e66adea13987f72342d29dfbcb16911abd1f278d21996690`  
		Last Modified: Tue, 30 Nov 2021 09:52:44 GMT  
		Size: 5.2 KB (5172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12155b3dec676fc427f05923079ccc1b3146a7bd125d2f535409d9637013baac`  
		Last Modified: Tue, 30 Nov 2021 09:52:44 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:13.4.5-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:cce59b4ef05c7b2b63764083d74152aa059f946b4b5d7a7c9a8df42e32146104
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **713.5 MB (713457382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6429e34a1646818fbdffa2ad4d326f954155fc501000048985abbed568630184`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Sat, 16 Oct 2021 01:47:45 GMT
ADD file:ff4909f2124325dac58d43c617132325934ed48a5ab4c534d05f931fcf700a2f in / 
# Sat, 16 Oct 2021 01:47:45 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 03:25:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 29 Nov 2021 19:40:01 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 29 Nov 2021 19:40:43 GMT
ENV JAVA_VERSION=jdk-11.0.13+8
# Mon, 29 Nov 2021 19:40:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a77013bff10a5e9c59159231dd5c4bd071fc4c24beed42bd49b82803ba9506ef';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.13_8.tar.gz';          ;;        armhf|arm)          ESUM='61ee45c4ef21a85a116a87e1bca2e2a420b3af432be8d801bd52c660ffebaa9f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_arm_linux_hotspot_11.0.13_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='82f14cda71cff99c878bf8400598a87235adb6c81b0337f7077c27e5cac1190c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.13_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='9d280d86fdf6a7d9e5cbf54dc37f1d6d09dfe676ff5c684802fdfa3932eee63e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.13_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3b1c0c34be4c894e64135a454f2d5aaa4bd10aea04ec2fa0c0efe6bb26528e30';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.13_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 29 Nov 2021 19:40:54 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Nov 2021 19:40:56 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Mon, 29 Nov 2021 19:40:57 GMT
CMD ["jshell"]
# Mon, 29 Nov 2021 21:17:19 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 29 Nov 2021 21:17:19 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Nov 2021 21:17:20 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 29 Nov 2021 21:17:21 GMT
WORKDIR /usr/local/tomcat
# Mon, 29 Nov 2021 21:17:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 29 Nov 2021 21:17:23 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 29 Nov 2021 21:34:34 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Mon, 29 Nov 2021 21:34:34 GMT
ENV TOMCAT_MAJOR=8
# Mon, 29 Nov 2021 21:34:35 GMT
ENV TOMCAT_VERSION=8.5.73
# Mon, 29 Nov 2021 21:34:36 GMT
ENV TOMCAT_SHA512=4d33760d007acc5271ba0f946d2be96f6146d4632e411c9b72d351fc49d08355e8b84b051713a2f580e0f633cbe4409b7e9bb0e62f3af8d1094c6e4b3fdb96f0
# Mon, 29 Nov 2021 21:35:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Mon, 29 Nov 2021 21:35:19 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Mon, 29 Nov 2021 21:35:19 GMT
EXPOSE 8080
# Mon, 29 Nov 2021 21:35:20 GMT
CMD ["catalina.sh" "run"]
# Mon, 29 Nov 2021 22:27:59 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Mon, 29 Nov 2021 22:28:37 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Mon, 29 Nov 2021 22:32:08 GMT
ENV XWIKI_VERSION=13.4.5
# Mon, 29 Nov 2021 22:32:09 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.4.5
# Mon, 29 Nov 2021 22:32:09 GMT
ENV XWIKI_DOWNLOAD_SHA256=4cb70d74525813e55142f3246da5218c006790b8a77f4a0784fa86e01046e6e8
# Mon, 29 Nov 2021 22:33:29 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Mon, 29 Nov 2021 22:33:30 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Mon, 29 Nov 2021 22:33:31 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Mon, 29 Nov 2021 22:33:32 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Mon, 29 Nov 2021 22:33:33 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Mon, 29 Nov 2021 22:33:34 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Mon, 29 Nov 2021 22:33:34 GMT
VOLUME [/usr/local/xwiki]
# Mon, 29 Nov 2021 22:33:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Nov 2021 22:33:36 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:a39c84e173f038958d338f55a9e8ee64bb6643e8ac6ae98e08ca65146e668d86`  
		Last Modified: Sat, 09 Oct 2021 15:32:18 GMT  
		Size: 27.2 MB (27170900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa42563dc02061b51ce62bff7340de9cea06ea720e8658d2a7693902aa8f700`  
		Last Modified: Mon, 29 Nov 2021 19:44:11 GMT  
		Size: 24.8 MB (24763049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77dd3dbd51783712818d90400820b5551c26f9e95104696e464e50825f558696`  
		Last Modified: Mon, 29 Nov 2021 19:45:13 GMT  
		Size: 190.5 MB (190512910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d56062c543a893b6c3d9bcc6775756d6debb5e849c02ba88d0d340523e6716a`  
		Last Modified: Mon, 29 Nov 2021 19:44:48 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:093c7df785877b00b055e2251b5b23c8563d6b4b8c4b3aa854596360557161d2`  
		Last Modified: Mon, 29 Nov 2021 21:56:01 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd78c30d612f0efcbedc574e44a2ad22bd91511b439b9b597605925512d0f64`  
		Last Modified: Mon, 29 Nov 2021 22:07:31 GMT  
		Size: 11.5 MB (11494827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e17fa2e98d378f2b12e1473caf2bc3b7642a888a5ef3bd0b6f68334ab6e2639`  
		Last Modified: Mon, 29 Nov 2021 22:34:38 GMT  
		Size: 155.3 MB (155304821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf960b0bca1c8791867458967c1f0ee46bfe1bb8c98e2c5f08544520c59f5dd1`  
		Last Modified: Mon, 29 Nov 2021 22:36:12 GMT  
		Size: 303.4 MB (303403692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2870c756160c6e7d97499c6aac0dcfdc792ce65568eba224f58097156f2e38`  
		Last Modified: Mon, 29 Nov 2021 22:35:50 GMT  
		Size: 795.4 KB (795420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d4e71364735c47ecec7229fb4fd45e410d92f048cd63d7adf0c3b4a491b99e6`  
		Last Modified: Mon, 29 Nov 2021 22:35:49 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:234d5215f92891ba0bf18c8baf28290bd0d08fd908dddea8dd378a245740af53`  
		Last Modified: Mon, 29 Nov 2021 22:35:50 GMT  
		Size: 2.5 KB (2467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e558095c54434d508864b8a4c17bc9c55a9f0b702dd05defa2daac5a38c0f0fd`  
		Last Modified: Mon, 29 Nov 2021 22:35:49 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66782e31fb66ffa7ea507d07f3e765e04a747b3e53bcf8fbe40afef11d6cc429`  
		Last Modified: Mon, 29 Nov 2021 22:35:50 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:latest`

```console
$ docker pull xwiki@sha256:f8be6bb37b7e4385597a7186a40f6d8bcde4f9c609d13f34149ace9ac4d5fdeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:latest` - linux; amd64

```console
$ docker pull xwiki@sha256:7340a02a837d6d8a7751bb8369c2d9a97643fd4e2530e1bc0098f235933f1e3d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **830.7 MB (830657270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:696e0182c57281cf1de1eefe88fa5d95fde87e191f5464d26c10b3687b03fa51`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:07 GMT
ADD file:e777355768c63f735e5458c7e0ada7f556f27d0493b3af35dc7c34f9c4294ea9 in / 
# Thu, 02 Dec 2021 02:48:08 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:39:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Dec 2021 03:40:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:34:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:34:20 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 02 Dec 2021 11:34:22 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 02 Dec 2021 11:34:22 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 11:34:22 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 11:34:23 GMT
ENV JAVA_VERSION=11.0.13
# Thu, 02 Dec 2021 11:34:48 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_x64_linux_11.0.13_8.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_aarch64_linux_11.0.13_8.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 02 Dec 2021 11:34:49 GMT
CMD ["jshell"]
# Fri, 03 Dec 2021 14:11:49 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Dec 2021 14:11:50 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Dec 2021 14:11:50 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 03 Dec 2021 14:11:51 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Dec 2021 14:11:51 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 14:11:51 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 14:27:34 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 03 Dec 2021 14:27:34 GMT
ENV TOMCAT_MAJOR=9
# Fri, 03 Dec 2021 14:27:34 GMT
ENV TOMCAT_VERSION=9.0.55
# Fri, 03 Dec 2021 14:27:35 GMT
ENV TOMCAT_SHA512=a0c480b8bba09069bda3b57f54e658450a59d799474ad587dead0ffbf5074c16ee3f9f9c13312d0ff3227c7034589dabf25941fbd672838e9baeee9661e024dc
# Fri, 03 Dec 2021 14:28:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 03 Dec 2021 14:28:03 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 03 Dec 2021 14:28:03 GMT
EXPOSE 8080
# Fri, 03 Dec 2021 14:28:03 GMT
CMD ["catalina.sh" "run"]
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 03 Dec 2021 20:52:45 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 20:52:47 GMT
ENV XWIKI_VERSION=13.10
# Fri, 03 Dec 2021 20:52:47 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10
# Fri, 03 Dec 2021 20:52:47 GMT
ENV XWIKI_DOWNLOAD_SHA256=863455ef741ec70539ab89b9981790909f3319b626a107e62fa42c8797df032b
# Fri, 03 Dec 2021 20:53:24 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 03 Dec 2021 20:53:25 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Fri, 03 Dec 2021 20:53:25 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Fri, 03 Dec 2021 20:53:25 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Fri, 03 Dec 2021 20:53:25 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Fri, 03 Dec 2021 20:53:25 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Fri, 03 Dec 2021 20:53:26 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 03 Dec 2021 20:53:27 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 03 Dec 2021 20:53:27 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 03 Dec 2021 20:53:28 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 03 Dec 2021 20:53:28 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 03 Dec 2021 20:53:28 GMT
VOLUME [/usr/local/xwiki]
# Fri, 03 Dec 2021 20:53:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Dec 2021 20:53:29 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:5e0b432e8ba9d9029a000e627840b98ffc1ed0c5172075b7d3e869be0df0fe9b`  
		Last Modified: Thu, 02 Dec 2021 02:53:18 GMT  
		Size: 54.9 MB (54932878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84cfd68b5cea612a8343c346bfa5bd6c486769010d12f7ec86b23c74887feb2`  
		Last Modified: Thu, 02 Dec 2021 03:49:22 GMT  
		Size: 5.2 MB (5153424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b8f2315954535f1e27cd13d777e73da4a787b0aebf4241d225beff3c91cbb1`  
		Last Modified: Thu, 02 Dec 2021 03:49:23 GMT  
		Size: 10.9 MB (10871995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0598fa43a7e793a76c198e8d45d8810394e1cfc943b2673d7fcf5a6fdc4f45b3`  
		Last Modified: Thu, 02 Dec 2021 03:49:46 GMT  
		Size: 54.6 MB (54567844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d35e3be804184359e0904389b149de16f159e30436d7a8a970aef67a4d155b`  
		Last Modified: Thu, 02 Dec 2021 11:54:46 GMT  
		Size: 5.4 MB (5420076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc448a0c88bee4d3cf6a928aa2b4cf499f4cb05034093c581342d414188a566`  
		Last Modified: Thu, 02 Dec 2021 11:54:45 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbdff6e5955b8bcd2e24b1a49fa4ec593ad333133c52911832aa2a7893f542da`  
		Last Modified: Thu, 02 Dec 2021 11:55:04 GMT  
		Size: 203.1 MB (203118915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5daf3771e3d8c27aa89cbcfef659790a2218e319899d49fbccde199e1780a5ef`  
		Last Modified: Fri, 03 Dec 2021 14:54:53 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5434ab540d864811e12dac3650eb0bc67bc8f6d7a6cb1f3c832e2c078c45302c`  
		Last Modified: Fri, 03 Dec 2021 15:08:17 GMT  
		Size: 12.5 MB (12523151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f43f4b2f615c39e867b3110fbc83f1d8fa2b72e4788cdcc91ea5dd73e97102`  
		Last Modified: Fri, 03 Dec 2021 15:08:16 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb64e66bc904d2f87948ce847a95dfa536c19132b599dc7f18ee2fec72ce7a8`  
		Last Modified: Fri, 03 Dec 2021 20:57:50 GMT  
		Size: 189.4 MB (189410805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eda7eb7430a70eef3ce565f0ad28fd9afcc0377bc9ba457bf47563dcf4ca3f25`  
		Last Modified: Fri, 03 Dec 2021 20:57:41 GMT  
		Size: 292.4 MB (292388360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f5388154bcdeb77283073eb4e763658b195a0a27693e1e7c35365485f30f18`  
		Last Modified: Fri, 03 Dec 2021 20:57:22 GMT  
		Size: 2.3 MB (2257828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696eeb26f8bf39548fdbc5946f4443b479ce079f2b4ff73d95ab70f4a77cd237`  
		Last Modified: Fri, 03 Dec 2021 20:57:22 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63b2a04633d035bab8bf65756959a3f6c27236b10f2df105c97760f087d2df0`  
		Last Modified: Fri, 03 Dec 2021 20:57:22 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7ba76bd956a9b63d4559a4144316330627c7dd1ceb4a8ad858ff6462db79078`  
		Last Modified: Fri, 03 Dec 2021 20:57:22 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8cd927e7dbd6905e1a2b5bb99be19019b586b787ad91f5e988fe85277cc44e`  
		Last Modified: Fri, 03 Dec 2021 20:57:22 GMT  
		Size: 2.5 KB (2500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:lts`

```console
$ docker pull xwiki@sha256:0c452bd65de374236c5c106311276ae850620d39c3d6a8a225b5a6883d2eaf9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:lts` - linux; amd64

```console
$ docker pull xwiki@sha256:bc8aaceaa6d467495242300c981dd77491cea326c58f7385481125a224888af2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.9 MB (835934777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daf03bf371ed121b6f8890ce6bebb499d4cfa8314d1de1f32552e4f86d0582f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:07 GMT
ADD file:e777355768c63f735e5458c7e0ada7f556f27d0493b3af35dc7c34f9c4294ea9 in / 
# Thu, 02 Dec 2021 02:48:08 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:39:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Dec 2021 03:40:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:34:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:34:20 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 02 Dec 2021 11:34:22 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 02 Dec 2021 11:34:22 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 11:34:22 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 11:34:23 GMT
ENV JAVA_VERSION=11.0.13
# Thu, 02 Dec 2021 11:34:48 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_x64_linux_11.0.13_8.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_aarch64_linux_11.0.13_8.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 02 Dec 2021 11:34:49 GMT
CMD ["jshell"]
# Fri, 03 Dec 2021 14:11:49 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Dec 2021 14:11:50 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Dec 2021 14:11:50 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 03 Dec 2021 14:11:51 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Dec 2021 14:11:51 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 14:11:51 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 14:27:34 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 03 Dec 2021 14:27:34 GMT
ENV TOMCAT_MAJOR=9
# Fri, 03 Dec 2021 14:27:34 GMT
ENV TOMCAT_VERSION=9.0.55
# Fri, 03 Dec 2021 14:27:35 GMT
ENV TOMCAT_SHA512=a0c480b8bba09069bda3b57f54e658450a59d799474ad587dead0ffbf5074c16ee3f9f9c13312d0ff3227c7034589dabf25941fbd672838e9baeee9661e024dc
# Fri, 03 Dec 2021 14:28:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 03 Dec 2021 14:28:03 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 03 Dec 2021 14:28:03 GMT
EXPOSE 8080
# Fri, 03 Dec 2021 14:28:03 GMT
CMD ["catalina.sh" "run"]
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 03 Dec 2021 20:52:45 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 20:54:56 GMT
ENV XWIKI_VERSION=12.10.10
# Fri, 03 Dec 2021 20:54:56 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.10
# Fri, 03 Dec 2021 20:54:56 GMT
ENV XWIKI_DOWNLOAD_SHA256=42364fd6a3d575c78969ebb12a7d28360ccff3b478379cf30232d6611ccbe9e0
# Fri, 03 Dec 2021 20:55:45 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 03 Dec 2021 20:55:46 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Fri, 03 Dec 2021 20:55:46 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Fri, 03 Dec 2021 20:55:46 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Fri, 03 Dec 2021 20:55:46 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Fri, 03 Dec 2021 20:55:46 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Fri, 03 Dec 2021 20:55:47 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 03 Dec 2021 20:55:48 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 03 Dec 2021 20:55:48 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 03 Dec 2021 20:55:49 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 03 Dec 2021 20:55:49 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 03 Dec 2021 20:55:49 GMT
VOLUME [/usr/local/xwiki]
# Fri, 03 Dec 2021 20:55:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Dec 2021 20:55:49 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:5e0b432e8ba9d9029a000e627840b98ffc1ed0c5172075b7d3e869be0df0fe9b`  
		Last Modified: Thu, 02 Dec 2021 02:53:18 GMT  
		Size: 54.9 MB (54932878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84cfd68b5cea612a8343c346bfa5bd6c486769010d12f7ec86b23c74887feb2`  
		Last Modified: Thu, 02 Dec 2021 03:49:22 GMT  
		Size: 5.2 MB (5153424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b8f2315954535f1e27cd13d777e73da4a787b0aebf4241d225beff3c91cbb1`  
		Last Modified: Thu, 02 Dec 2021 03:49:23 GMT  
		Size: 10.9 MB (10871995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0598fa43a7e793a76c198e8d45d8810394e1cfc943b2673d7fcf5a6fdc4f45b3`  
		Last Modified: Thu, 02 Dec 2021 03:49:46 GMT  
		Size: 54.6 MB (54567844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d35e3be804184359e0904389b149de16f159e30436d7a8a970aef67a4d155b`  
		Last Modified: Thu, 02 Dec 2021 11:54:46 GMT  
		Size: 5.4 MB (5420076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc448a0c88bee4d3cf6a928aa2b4cf499f4cb05034093c581342d414188a566`  
		Last Modified: Thu, 02 Dec 2021 11:54:45 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbdff6e5955b8bcd2e24b1a49fa4ec593ad333133c52911832aa2a7893f542da`  
		Last Modified: Thu, 02 Dec 2021 11:55:04 GMT  
		Size: 203.1 MB (203118915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5daf3771e3d8c27aa89cbcfef659790a2218e319899d49fbccde199e1780a5ef`  
		Last Modified: Fri, 03 Dec 2021 14:54:53 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5434ab540d864811e12dac3650eb0bc67bc8f6d7a6cb1f3c832e2c078c45302c`  
		Last Modified: Fri, 03 Dec 2021 15:08:17 GMT  
		Size: 12.5 MB (12523151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f43f4b2f615c39e867b3110fbc83f1d8fa2b72e4788cdcc91ea5dd73e97102`  
		Last Modified: Fri, 03 Dec 2021 15:08:16 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb64e66bc904d2f87948ce847a95dfa536c19132b599dc7f18ee2fec72ce7a8`  
		Last Modified: Fri, 03 Dec 2021 20:57:50 GMT  
		Size: 189.4 MB (189410805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:322c3fa9aeb088d28eaf87bee8cc347dd2446ec513406bfcc94fe921c47ef232`  
		Last Modified: Fri, 03 Dec 2021 20:59:42 GMT  
		Size: 297.7 MB (297665996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90fcdaa3c2b3eab89db62dbbc268566389c9d3aeca137f15cbdb15b0d7eaffe9`  
		Last Modified: Fri, 03 Dec 2021 20:59:25 GMT  
		Size: 2.3 MB (2257807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d51c8a2c6527bec03b855db0bdb4b58452c4af299cc4f40fc1690573eedb2676`  
		Last Modified: Fri, 03 Dec 2021 20:59:25 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56b515d1801ae6cbeea27c7f418568eb18e5310be586bb180e59cb2ddb54b41c`  
		Last Modified: Fri, 03 Dec 2021 20:59:25 GMT  
		Size: 2.3 KB (2303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9098d697724f1d37cb1cbc0032ca0057920efbebe8ff19f8391d8b88182881b6`  
		Last Modified: Fri, 03 Dec 2021 20:59:25 GMT  
		Size: 5.2 KB (5224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00faacd3e28eae83a4d5fa60009ec43904a971ad076d496b8ba65a2cc6331f3e`  
		Last Modified: Fri, 03 Dec 2021 20:59:25 GMT  
		Size: 2.5 KB (2501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:lts-mysql`

```console
$ docker pull xwiki@sha256:0c452bd65de374236c5c106311276ae850620d39c3d6a8a225b5a6883d2eaf9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:lts-mysql` - linux; amd64

```console
$ docker pull xwiki@sha256:bc8aaceaa6d467495242300c981dd77491cea326c58f7385481125a224888af2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.9 MB (835934777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daf03bf371ed121b6f8890ce6bebb499d4cfa8314d1de1f32552e4f86d0582f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:07 GMT
ADD file:e777355768c63f735e5458c7e0ada7f556f27d0493b3af35dc7c34f9c4294ea9 in / 
# Thu, 02 Dec 2021 02:48:08 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:39:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Dec 2021 03:40:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:34:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:34:20 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 02 Dec 2021 11:34:22 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 02 Dec 2021 11:34:22 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 11:34:22 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 11:34:23 GMT
ENV JAVA_VERSION=11.0.13
# Thu, 02 Dec 2021 11:34:48 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_x64_linux_11.0.13_8.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_aarch64_linux_11.0.13_8.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 02 Dec 2021 11:34:49 GMT
CMD ["jshell"]
# Fri, 03 Dec 2021 14:11:49 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Dec 2021 14:11:50 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Dec 2021 14:11:50 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 03 Dec 2021 14:11:51 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Dec 2021 14:11:51 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 14:11:51 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 14:27:34 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 03 Dec 2021 14:27:34 GMT
ENV TOMCAT_MAJOR=9
# Fri, 03 Dec 2021 14:27:34 GMT
ENV TOMCAT_VERSION=9.0.55
# Fri, 03 Dec 2021 14:27:35 GMT
ENV TOMCAT_SHA512=a0c480b8bba09069bda3b57f54e658450a59d799474ad587dead0ffbf5074c16ee3f9f9c13312d0ff3227c7034589dabf25941fbd672838e9baeee9661e024dc
# Fri, 03 Dec 2021 14:28:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 03 Dec 2021 14:28:03 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 03 Dec 2021 14:28:03 GMT
EXPOSE 8080
# Fri, 03 Dec 2021 14:28:03 GMT
CMD ["catalina.sh" "run"]
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 03 Dec 2021 20:52:45 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 20:54:56 GMT
ENV XWIKI_VERSION=12.10.10
# Fri, 03 Dec 2021 20:54:56 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.10
# Fri, 03 Dec 2021 20:54:56 GMT
ENV XWIKI_DOWNLOAD_SHA256=42364fd6a3d575c78969ebb12a7d28360ccff3b478379cf30232d6611ccbe9e0
# Fri, 03 Dec 2021 20:55:45 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 03 Dec 2021 20:55:46 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Fri, 03 Dec 2021 20:55:46 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Fri, 03 Dec 2021 20:55:46 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Fri, 03 Dec 2021 20:55:46 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Fri, 03 Dec 2021 20:55:46 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Fri, 03 Dec 2021 20:55:47 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 03 Dec 2021 20:55:48 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 03 Dec 2021 20:55:48 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 03 Dec 2021 20:55:49 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 03 Dec 2021 20:55:49 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 03 Dec 2021 20:55:49 GMT
VOLUME [/usr/local/xwiki]
# Fri, 03 Dec 2021 20:55:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Dec 2021 20:55:49 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:5e0b432e8ba9d9029a000e627840b98ffc1ed0c5172075b7d3e869be0df0fe9b`  
		Last Modified: Thu, 02 Dec 2021 02:53:18 GMT  
		Size: 54.9 MB (54932878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84cfd68b5cea612a8343c346bfa5bd6c486769010d12f7ec86b23c74887feb2`  
		Last Modified: Thu, 02 Dec 2021 03:49:22 GMT  
		Size: 5.2 MB (5153424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b8f2315954535f1e27cd13d777e73da4a787b0aebf4241d225beff3c91cbb1`  
		Last Modified: Thu, 02 Dec 2021 03:49:23 GMT  
		Size: 10.9 MB (10871995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0598fa43a7e793a76c198e8d45d8810394e1cfc943b2673d7fcf5a6fdc4f45b3`  
		Last Modified: Thu, 02 Dec 2021 03:49:46 GMT  
		Size: 54.6 MB (54567844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d35e3be804184359e0904389b149de16f159e30436d7a8a970aef67a4d155b`  
		Last Modified: Thu, 02 Dec 2021 11:54:46 GMT  
		Size: 5.4 MB (5420076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc448a0c88bee4d3cf6a928aa2b4cf499f4cb05034093c581342d414188a566`  
		Last Modified: Thu, 02 Dec 2021 11:54:45 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbdff6e5955b8bcd2e24b1a49fa4ec593ad333133c52911832aa2a7893f542da`  
		Last Modified: Thu, 02 Dec 2021 11:55:04 GMT  
		Size: 203.1 MB (203118915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5daf3771e3d8c27aa89cbcfef659790a2218e319899d49fbccde199e1780a5ef`  
		Last Modified: Fri, 03 Dec 2021 14:54:53 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5434ab540d864811e12dac3650eb0bc67bc8f6d7a6cb1f3c832e2c078c45302c`  
		Last Modified: Fri, 03 Dec 2021 15:08:17 GMT  
		Size: 12.5 MB (12523151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f43f4b2f615c39e867b3110fbc83f1d8fa2b72e4788cdcc91ea5dd73e97102`  
		Last Modified: Fri, 03 Dec 2021 15:08:16 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb64e66bc904d2f87948ce847a95dfa536c19132b599dc7f18ee2fec72ce7a8`  
		Last Modified: Fri, 03 Dec 2021 20:57:50 GMT  
		Size: 189.4 MB (189410805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:322c3fa9aeb088d28eaf87bee8cc347dd2446ec513406bfcc94fe921c47ef232`  
		Last Modified: Fri, 03 Dec 2021 20:59:42 GMT  
		Size: 297.7 MB (297665996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90fcdaa3c2b3eab89db62dbbc268566389c9d3aeca137f15cbdb15b0d7eaffe9`  
		Last Modified: Fri, 03 Dec 2021 20:59:25 GMT  
		Size: 2.3 MB (2257807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d51c8a2c6527bec03b855db0bdb4b58452c4af299cc4f40fc1690573eedb2676`  
		Last Modified: Fri, 03 Dec 2021 20:59:25 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56b515d1801ae6cbeea27c7f418568eb18e5310be586bb180e59cb2ddb54b41c`  
		Last Modified: Fri, 03 Dec 2021 20:59:25 GMT  
		Size: 2.3 KB (2303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9098d697724f1d37cb1cbc0032ca0057920efbebe8ff19f8391d8b88182881b6`  
		Last Modified: Fri, 03 Dec 2021 20:59:25 GMT  
		Size: 5.2 KB (5224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00faacd3e28eae83a4d5fa60009ec43904a971ad076d496b8ba65a2cc6331f3e`  
		Last Modified: Fri, 03 Dec 2021 20:59:25 GMT  
		Size: 2.5 KB (2501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:lts-mysql-tomcat`

```console
$ docker pull xwiki@sha256:0c452bd65de374236c5c106311276ae850620d39c3d6a8a225b5a6883d2eaf9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:lts-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:bc8aaceaa6d467495242300c981dd77491cea326c58f7385481125a224888af2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.9 MB (835934777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daf03bf371ed121b6f8890ce6bebb499d4cfa8314d1de1f32552e4f86d0582f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:07 GMT
ADD file:e777355768c63f735e5458c7e0ada7f556f27d0493b3af35dc7c34f9c4294ea9 in / 
# Thu, 02 Dec 2021 02:48:08 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:39:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Dec 2021 03:40:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:34:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:34:20 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 02 Dec 2021 11:34:22 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 02 Dec 2021 11:34:22 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 11:34:22 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 11:34:23 GMT
ENV JAVA_VERSION=11.0.13
# Thu, 02 Dec 2021 11:34:48 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_x64_linux_11.0.13_8.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_aarch64_linux_11.0.13_8.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 02 Dec 2021 11:34:49 GMT
CMD ["jshell"]
# Fri, 03 Dec 2021 14:11:49 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Dec 2021 14:11:50 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Dec 2021 14:11:50 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 03 Dec 2021 14:11:51 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Dec 2021 14:11:51 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 14:11:51 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 14:27:34 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 03 Dec 2021 14:27:34 GMT
ENV TOMCAT_MAJOR=9
# Fri, 03 Dec 2021 14:27:34 GMT
ENV TOMCAT_VERSION=9.0.55
# Fri, 03 Dec 2021 14:27:35 GMT
ENV TOMCAT_SHA512=a0c480b8bba09069bda3b57f54e658450a59d799474ad587dead0ffbf5074c16ee3f9f9c13312d0ff3227c7034589dabf25941fbd672838e9baeee9661e024dc
# Fri, 03 Dec 2021 14:28:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 03 Dec 2021 14:28:03 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 03 Dec 2021 14:28:03 GMT
EXPOSE 8080
# Fri, 03 Dec 2021 14:28:03 GMT
CMD ["catalina.sh" "run"]
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 03 Dec 2021 20:52:45 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 20:54:56 GMT
ENV XWIKI_VERSION=12.10.10
# Fri, 03 Dec 2021 20:54:56 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.10
# Fri, 03 Dec 2021 20:54:56 GMT
ENV XWIKI_DOWNLOAD_SHA256=42364fd6a3d575c78969ebb12a7d28360ccff3b478379cf30232d6611ccbe9e0
# Fri, 03 Dec 2021 20:55:45 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 03 Dec 2021 20:55:46 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Fri, 03 Dec 2021 20:55:46 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Fri, 03 Dec 2021 20:55:46 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Fri, 03 Dec 2021 20:55:46 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Fri, 03 Dec 2021 20:55:46 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Fri, 03 Dec 2021 20:55:47 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 03 Dec 2021 20:55:48 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 03 Dec 2021 20:55:48 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 03 Dec 2021 20:55:49 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 03 Dec 2021 20:55:49 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 03 Dec 2021 20:55:49 GMT
VOLUME [/usr/local/xwiki]
# Fri, 03 Dec 2021 20:55:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Dec 2021 20:55:49 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:5e0b432e8ba9d9029a000e627840b98ffc1ed0c5172075b7d3e869be0df0fe9b`  
		Last Modified: Thu, 02 Dec 2021 02:53:18 GMT  
		Size: 54.9 MB (54932878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84cfd68b5cea612a8343c346bfa5bd6c486769010d12f7ec86b23c74887feb2`  
		Last Modified: Thu, 02 Dec 2021 03:49:22 GMT  
		Size: 5.2 MB (5153424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b8f2315954535f1e27cd13d777e73da4a787b0aebf4241d225beff3c91cbb1`  
		Last Modified: Thu, 02 Dec 2021 03:49:23 GMT  
		Size: 10.9 MB (10871995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0598fa43a7e793a76c198e8d45d8810394e1cfc943b2673d7fcf5a6fdc4f45b3`  
		Last Modified: Thu, 02 Dec 2021 03:49:46 GMT  
		Size: 54.6 MB (54567844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d35e3be804184359e0904389b149de16f159e30436d7a8a970aef67a4d155b`  
		Last Modified: Thu, 02 Dec 2021 11:54:46 GMT  
		Size: 5.4 MB (5420076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc448a0c88bee4d3cf6a928aa2b4cf499f4cb05034093c581342d414188a566`  
		Last Modified: Thu, 02 Dec 2021 11:54:45 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbdff6e5955b8bcd2e24b1a49fa4ec593ad333133c52911832aa2a7893f542da`  
		Last Modified: Thu, 02 Dec 2021 11:55:04 GMT  
		Size: 203.1 MB (203118915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5daf3771e3d8c27aa89cbcfef659790a2218e319899d49fbccde199e1780a5ef`  
		Last Modified: Fri, 03 Dec 2021 14:54:53 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5434ab540d864811e12dac3650eb0bc67bc8f6d7a6cb1f3c832e2c078c45302c`  
		Last Modified: Fri, 03 Dec 2021 15:08:17 GMT  
		Size: 12.5 MB (12523151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f43f4b2f615c39e867b3110fbc83f1d8fa2b72e4788cdcc91ea5dd73e97102`  
		Last Modified: Fri, 03 Dec 2021 15:08:16 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb64e66bc904d2f87948ce847a95dfa536c19132b599dc7f18ee2fec72ce7a8`  
		Last Modified: Fri, 03 Dec 2021 20:57:50 GMT  
		Size: 189.4 MB (189410805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:322c3fa9aeb088d28eaf87bee8cc347dd2446ec513406bfcc94fe921c47ef232`  
		Last Modified: Fri, 03 Dec 2021 20:59:42 GMT  
		Size: 297.7 MB (297665996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90fcdaa3c2b3eab89db62dbbc268566389c9d3aeca137f15cbdb15b0d7eaffe9`  
		Last Modified: Fri, 03 Dec 2021 20:59:25 GMT  
		Size: 2.3 MB (2257807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d51c8a2c6527bec03b855db0bdb4b58452c4af299cc4f40fc1690573eedb2676`  
		Last Modified: Fri, 03 Dec 2021 20:59:25 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56b515d1801ae6cbeea27c7f418568eb18e5310be586bb180e59cb2ddb54b41c`  
		Last Modified: Fri, 03 Dec 2021 20:59:25 GMT  
		Size: 2.3 KB (2303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9098d697724f1d37cb1cbc0032ca0057920efbebe8ff19f8391d8b88182881b6`  
		Last Modified: Fri, 03 Dec 2021 20:59:25 GMT  
		Size: 5.2 KB (5224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00faacd3e28eae83a4d5fa60009ec43904a971ad076d496b8ba65a2cc6331f3e`  
		Last Modified: Fri, 03 Dec 2021 20:59:25 GMT  
		Size: 2.5 KB (2501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:lts-postgres`

```console
$ docker pull xwiki@sha256:33059b78ebe52d5089e0f0d0228b20ee00e97884213ea98e79d3c23d0265a18e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:lts-postgres` - linux; amd64

```console
$ docker pull xwiki@sha256:b6da64a702495f77148d7907115512347ed792c3e13745f700877be9196acfaf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.4 MB (835398749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8000205aad7fbc2729bde9231f8618248a910cad7dc4c0f6ecc6c3f82ab0f7e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:07 GMT
ADD file:e777355768c63f735e5458c7e0ada7f556f27d0493b3af35dc7c34f9c4294ea9 in / 
# Thu, 02 Dec 2021 02:48:08 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:39:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Dec 2021 03:40:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:34:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:34:20 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 02 Dec 2021 11:34:22 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 02 Dec 2021 11:34:22 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 11:34:22 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 11:34:23 GMT
ENV JAVA_VERSION=11.0.13
# Thu, 02 Dec 2021 11:34:48 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_x64_linux_11.0.13_8.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_aarch64_linux_11.0.13_8.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 02 Dec 2021 11:34:49 GMT
CMD ["jshell"]
# Fri, 03 Dec 2021 14:11:49 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Dec 2021 14:11:50 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Dec 2021 14:11:50 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 03 Dec 2021 14:11:51 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Dec 2021 14:11:51 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 14:11:51 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 14:27:34 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 03 Dec 2021 14:27:34 GMT
ENV TOMCAT_MAJOR=9
# Fri, 03 Dec 2021 14:27:34 GMT
ENV TOMCAT_VERSION=9.0.55
# Fri, 03 Dec 2021 14:27:35 GMT
ENV TOMCAT_SHA512=a0c480b8bba09069bda3b57f54e658450a59d799474ad587dead0ffbf5074c16ee3f9f9c13312d0ff3227c7034589dabf25941fbd672838e9baeee9661e024dc
# Fri, 03 Dec 2021 14:28:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 03 Dec 2021 14:28:03 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 03 Dec 2021 14:28:03 GMT
EXPOSE 8080
# Fri, 03 Dec 2021 14:28:03 GMT
CMD ["catalina.sh" "run"]
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 03 Dec 2021 20:54:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 20:55:53 GMT
ENV XWIKI_VERSION=12.10.10
# Fri, 03 Dec 2021 20:55:53 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.10
# Fri, 03 Dec 2021 20:55:53 GMT
ENV XWIKI_DOWNLOAD_SHA256=42364fd6a3d575c78969ebb12a7d28360ccff3b478379cf30232d6611ccbe9e0
# Fri, 03 Dec 2021 20:56:32 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 03 Dec 2021 20:56:34 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 03 Dec 2021 20:56:34 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 03 Dec 2021 20:56:34 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 03 Dec 2021 20:56:35 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 03 Dec 2021 20:56:35 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 03 Dec 2021 20:56:36 GMT
VOLUME [/usr/local/xwiki]
# Fri, 03 Dec 2021 20:56:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Dec 2021 20:56:36 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:5e0b432e8ba9d9029a000e627840b98ffc1ed0c5172075b7d3e869be0df0fe9b`  
		Last Modified: Thu, 02 Dec 2021 02:53:18 GMT  
		Size: 54.9 MB (54932878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84cfd68b5cea612a8343c346bfa5bd6c486769010d12f7ec86b23c74887feb2`  
		Last Modified: Thu, 02 Dec 2021 03:49:22 GMT  
		Size: 5.2 MB (5153424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b8f2315954535f1e27cd13d777e73da4a787b0aebf4241d225beff3c91cbb1`  
		Last Modified: Thu, 02 Dec 2021 03:49:23 GMT  
		Size: 10.9 MB (10871995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0598fa43a7e793a76c198e8d45d8810394e1cfc943b2673d7fcf5a6fdc4f45b3`  
		Last Modified: Thu, 02 Dec 2021 03:49:46 GMT  
		Size: 54.6 MB (54567844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d35e3be804184359e0904389b149de16f159e30436d7a8a970aef67a4d155b`  
		Last Modified: Thu, 02 Dec 2021 11:54:46 GMT  
		Size: 5.4 MB (5420076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc448a0c88bee4d3cf6a928aa2b4cf499f4cb05034093c581342d414188a566`  
		Last Modified: Thu, 02 Dec 2021 11:54:45 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbdff6e5955b8bcd2e24b1a49fa4ec593ad333133c52911832aa2a7893f542da`  
		Last Modified: Thu, 02 Dec 2021 11:55:04 GMT  
		Size: 203.1 MB (203118915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5daf3771e3d8c27aa89cbcfef659790a2218e319899d49fbccde199e1780a5ef`  
		Last Modified: Fri, 03 Dec 2021 14:54:53 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5434ab540d864811e12dac3650eb0bc67bc8f6d7a6cb1f3c832e2c078c45302c`  
		Last Modified: Fri, 03 Dec 2021 15:08:17 GMT  
		Size: 12.5 MB (12523151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f43f4b2f615c39e867b3110fbc83f1d8fa2b72e4788cdcc91ea5dd73e97102`  
		Last Modified: Fri, 03 Dec 2021 15:08:16 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c96c2f945ecec7eda758824db2032432765e7a0128ef11d3c1841ac2dc2e5d95`  
		Last Modified: Fri, 03 Dec 2021 20:59:00 GMT  
		Size: 190.3 MB (190286185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98dd220d8d99ab2f82e0c4d98e1eda554b20e4cdd518e4863383ad47a2ede008`  
		Last Modified: Fri, 03 Dec 2021 21:00:34 GMT  
		Size: 297.7 MB (297666042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68c6a4d55d8aedc737c28c16053a45f219463db9f442fd0139d5dd559732b8dc`  
		Last Modified: Fri, 03 Dec 2021 21:00:17 GMT  
		Size: 846.2 KB (846205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68bf6e53b283f66ee03293c481736522efbf14497b1b2e32a0f7df3b5a68f310`  
		Last Modified: Fri, 03 Dec 2021 21:00:17 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5872a387705493894041a0e0d185f7b63f35ba540ce218ce8a3a93f95139b77f`  
		Last Modified: Fri, 03 Dec 2021 21:00:17 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18ed072c9481ea2501ceb7126460fd9ed5efbfc1d82a60714d95c4780535d991`  
		Last Modified: Fri, 03 Dec 2021 21:00:17 GMT  
		Size: 5.2 KB (5225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f365d0250ccd4d7fe8466796da2ba876f11c83b4daddc69875dfc1a7033a79b0`  
		Last Modified: Fri, 03 Dec 2021 21:00:17 GMT  
		Size: 2.5 KB (2503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:lts-postgres` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:c2c5faf2f199eb1abe110535577faa2262fb300d8d92907861ba0ff310dabde1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **826.0 MB (826035753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78f13512af2ef156fa16d62503f8cd4483448d6e15b959fcb2dfa4015f230659`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 02 Dec 2021 08:07:54 GMT
ADD file:998dc1c35eeeed1ddf46156aeb337fb9b8cbb4855caf994201167a1061f4ecbf in / 
# Thu, 02 Dec 2021 08:07:55 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 09:53:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 09:53:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Dec 2021 09:53:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:07:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:07:23 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 02 Dec 2021 11:07:24 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 02 Dec 2021 11:07:25 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 11:07:26 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 11:07:27 GMT
ENV JAVA_VERSION=11.0.13
# Thu, 02 Dec 2021 11:07:49 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_x64_linux_11.0.13_8.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_aarch64_linux_11.0.13_8.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 02 Dec 2021 11:07:50 GMT
CMD ["jshell"]
# Fri, 03 Dec 2021 10:33:28 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Dec 2021 10:33:28 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Dec 2021 10:33:30 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 03 Dec 2021 10:33:30 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Dec 2021 10:33:31 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 10:33:32 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 10:54:19 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 03 Dec 2021 10:54:20 GMT
ENV TOMCAT_MAJOR=9
# Fri, 03 Dec 2021 10:54:21 GMT
ENV TOMCAT_VERSION=9.0.55
# Fri, 03 Dec 2021 10:54:22 GMT
ENV TOMCAT_SHA512=a0c480b8bba09069bda3b57f54e658450a59d799474ad587dead0ffbf5074c16ee3f9f9c13312d0ff3227c7034589dabf25941fbd672838e9baeee9661e024dc
# Fri, 03 Dec 2021 10:54:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 03 Dec 2021 10:54:45 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 03 Dec 2021 10:54:45 GMT
EXPOSE 8080
# Fri, 03 Dec 2021 10:54:46 GMT
CMD ["catalina.sh" "run"]
# Fri, 03 Dec 2021 16:34:04 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 03 Dec 2021 16:34:05 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 16:34:05 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 16:34:06 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 03 Dec 2021 16:34:07 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 03 Dec 2021 16:34:08 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 03 Dec 2021 16:34:43 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 16:34:44 GMT
ENV XWIKI_VERSION=12.10.10
# Fri, 03 Dec 2021 16:34:45 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.10
# Fri, 03 Dec 2021 16:34:46 GMT
ENV XWIKI_DOWNLOAD_SHA256=42364fd6a3d575c78969ebb12a7d28360ccff3b478379cf30232d6611ccbe9e0
# Fri, 03 Dec 2021 16:36:07 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 03 Dec 2021 16:36:09 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 03 Dec 2021 16:36:10 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 03 Dec 2021 16:36:11 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 03 Dec 2021 16:36:12 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 03 Dec 2021 16:36:14 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 03 Dec 2021 16:36:15 GMT
VOLUME [/usr/local/xwiki]
# Fri, 03 Dec 2021 16:36:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Dec 2021 16:36:16 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:6476cb406b24c94f24348db05d154b814b14ee38860dea1625080e7e08295a80`  
		Last Modified: Thu, 02 Dec 2021 08:40:14 GMT  
		Size: 53.6 MB (53619027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96565d527970b1cc982493f96d6b317b1fbfdd7bf0ea6fd58d44942bb4f597c5`  
		Last Modified: Thu, 02 Dec 2021 10:02:24 GMT  
		Size: 4.9 MB (4937631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8c15f93136056df893ba8088992a38e90dc37210fd6ebb712413fd045c58de`  
		Last Modified: Thu, 02 Dec 2021 10:02:25 GMT  
		Size: 10.7 MB (10655914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee42e24e52cb2f9b50ab14328865298f5ae6ac159219db890afc6366ec641a46`  
		Last Modified: Thu, 02 Dec 2021 10:02:46 GMT  
		Size: 54.7 MB (54669690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1ddc61edfde0dfa7da5e868dfebc0df6e44b7c94700ae79892d861abc32f97`  
		Last Modified: Thu, 02 Dec 2021 11:31:06 GMT  
		Size: 5.4 MB (5420180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:804b3e7e3a2930efff5c50600a2c162b8f2af073ec54a3c44314cc36e68d1a75`  
		Last Modified: Thu, 02 Dec 2021 11:31:05 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c15c25e9529bccafc0b750eb33fb972a05d42a09303dc760b67f89ea21b0bce0`  
		Last Modified: Thu, 02 Dec 2021 11:31:26 GMT  
		Size: 200.7 MB (200712890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac1b17d7ee052527ef86a2354f093548ac170d6d3318a79fa9916fd616c2c40f`  
		Last Modified: Fri, 03 Dec 2021 11:33:43 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8926fc06c65e9a17e2a3110e422fbebb73f63463202846b0b6addc004fd06d`  
		Last Modified: Fri, 03 Dec 2021 11:49:18 GMT  
		Size: 12.3 MB (12292070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56905cdb16153e42e333c2819b26aec2f74860d5924cbe3cf1952f737953c4d`  
		Last Modified: Fri, 03 Dec 2021 16:37:29 GMT  
		Size: 185.2 MB (185204101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b630d0a06c79c04946d7044a763e8bcfa3048eba1ee5917c5d73fbfc202e1cfd`  
		Last Modified: Fri, 03 Dec 2021 16:37:26 GMT  
		Size: 297.7 MB (297666166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c967f3c4012d8a61def666f59f0bb438b973b040c024ca5c194f0bc0f9ac33d1`  
		Last Modified: Fri, 03 Dec 2021 16:37:03 GMT  
		Size: 846.2 KB (846206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e42a536c4ff68942cbe6d89a2a025d4ff95d2d9c502e704b6e3981f2165b1b41`  
		Last Modified: Fri, 03 Dec 2021 16:37:03 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75dec884c2231050cbed8f6719547b3af625afb7df02cc793a7435570a75c981`  
		Last Modified: Fri, 03 Dec 2021 16:37:03 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2481f87da9b8547832e3c87fbe6f23b1e2a9a244bb522970461f859e242e089`  
		Last Modified: Fri, 03 Dec 2021 16:37:03 GMT  
		Size: 5.2 KB (5224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fac7412501c0d3bf5e64c52bf821fbae7b3be8223bc771b9b01062f15e73f60`  
		Last Modified: Fri, 03 Dec 2021 16:37:03 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:lts-postgres-tomcat`

```console
$ docker pull xwiki@sha256:33059b78ebe52d5089e0f0d0228b20ee00e97884213ea98e79d3c23d0265a18e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:lts-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:b6da64a702495f77148d7907115512347ed792c3e13745f700877be9196acfaf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.4 MB (835398749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8000205aad7fbc2729bde9231f8618248a910cad7dc4c0f6ecc6c3f82ab0f7e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:07 GMT
ADD file:e777355768c63f735e5458c7e0ada7f556f27d0493b3af35dc7c34f9c4294ea9 in / 
# Thu, 02 Dec 2021 02:48:08 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:39:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Dec 2021 03:40:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:34:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:34:20 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 02 Dec 2021 11:34:22 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 02 Dec 2021 11:34:22 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 11:34:22 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 11:34:23 GMT
ENV JAVA_VERSION=11.0.13
# Thu, 02 Dec 2021 11:34:48 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_x64_linux_11.0.13_8.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_aarch64_linux_11.0.13_8.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 02 Dec 2021 11:34:49 GMT
CMD ["jshell"]
# Fri, 03 Dec 2021 14:11:49 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Dec 2021 14:11:50 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Dec 2021 14:11:50 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 03 Dec 2021 14:11:51 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Dec 2021 14:11:51 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 14:11:51 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 14:27:34 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 03 Dec 2021 14:27:34 GMT
ENV TOMCAT_MAJOR=9
# Fri, 03 Dec 2021 14:27:34 GMT
ENV TOMCAT_VERSION=9.0.55
# Fri, 03 Dec 2021 14:27:35 GMT
ENV TOMCAT_SHA512=a0c480b8bba09069bda3b57f54e658450a59d799474ad587dead0ffbf5074c16ee3f9f9c13312d0ff3227c7034589dabf25941fbd672838e9baeee9661e024dc
# Fri, 03 Dec 2021 14:28:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 03 Dec 2021 14:28:03 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 03 Dec 2021 14:28:03 GMT
EXPOSE 8080
# Fri, 03 Dec 2021 14:28:03 GMT
CMD ["catalina.sh" "run"]
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 03 Dec 2021 20:54:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 20:55:53 GMT
ENV XWIKI_VERSION=12.10.10
# Fri, 03 Dec 2021 20:55:53 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.10
# Fri, 03 Dec 2021 20:55:53 GMT
ENV XWIKI_DOWNLOAD_SHA256=42364fd6a3d575c78969ebb12a7d28360ccff3b478379cf30232d6611ccbe9e0
# Fri, 03 Dec 2021 20:56:32 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 03 Dec 2021 20:56:34 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 03 Dec 2021 20:56:34 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 03 Dec 2021 20:56:34 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 03 Dec 2021 20:56:35 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 03 Dec 2021 20:56:35 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 03 Dec 2021 20:56:36 GMT
VOLUME [/usr/local/xwiki]
# Fri, 03 Dec 2021 20:56:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Dec 2021 20:56:36 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:5e0b432e8ba9d9029a000e627840b98ffc1ed0c5172075b7d3e869be0df0fe9b`  
		Last Modified: Thu, 02 Dec 2021 02:53:18 GMT  
		Size: 54.9 MB (54932878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84cfd68b5cea612a8343c346bfa5bd6c486769010d12f7ec86b23c74887feb2`  
		Last Modified: Thu, 02 Dec 2021 03:49:22 GMT  
		Size: 5.2 MB (5153424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b8f2315954535f1e27cd13d777e73da4a787b0aebf4241d225beff3c91cbb1`  
		Last Modified: Thu, 02 Dec 2021 03:49:23 GMT  
		Size: 10.9 MB (10871995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0598fa43a7e793a76c198e8d45d8810394e1cfc943b2673d7fcf5a6fdc4f45b3`  
		Last Modified: Thu, 02 Dec 2021 03:49:46 GMT  
		Size: 54.6 MB (54567844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d35e3be804184359e0904389b149de16f159e30436d7a8a970aef67a4d155b`  
		Last Modified: Thu, 02 Dec 2021 11:54:46 GMT  
		Size: 5.4 MB (5420076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc448a0c88bee4d3cf6a928aa2b4cf499f4cb05034093c581342d414188a566`  
		Last Modified: Thu, 02 Dec 2021 11:54:45 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbdff6e5955b8bcd2e24b1a49fa4ec593ad333133c52911832aa2a7893f542da`  
		Last Modified: Thu, 02 Dec 2021 11:55:04 GMT  
		Size: 203.1 MB (203118915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5daf3771e3d8c27aa89cbcfef659790a2218e319899d49fbccde199e1780a5ef`  
		Last Modified: Fri, 03 Dec 2021 14:54:53 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5434ab540d864811e12dac3650eb0bc67bc8f6d7a6cb1f3c832e2c078c45302c`  
		Last Modified: Fri, 03 Dec 2021 15:08:17 GMT  
		Size: 12.5 MB (12523151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f43f4b2f615c39e867b3110fbc83f1d8fa2b72e4788cdcc91ea5dd73e97102`  
		Last Modified: Fri, 03 Dec 2021 15:08:16 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c96c2f945ecec7eda758824db2032432765e7a0128ef11d3c1841ac2dc2e5d95`  
		Last Modified: Fri, 03 Dec 2021 20:59:00 GMT  
		Size: 190.3 MB (190286185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98dd220d8d99ab2f82e0c4d98e1eda554b20e4cdd518e4863383ad47a2ede008`  
		Last Modified: Fri, 03 Dec 2021 21:00:34 GMT  
		Size: 297.7 MB (297666042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68c6a4d55d8aedc737c28c16053a45f219463db9f442fd0139d5dd559732b8dc`  
		Last Modified: Fri, 03 Dec 2021 21:00:17 GMT  
		Size: 846.2 KB (846205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68bf6e53b283f66ee03293c481736522efbf14497b1b2e32a0f7df3b5a68f310`  
		Last Modified: Fri, 03 Dec 2021 21:00:17 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5872a387705493894041a0e0d185f7b63f35ba540ce218ce8a3a93f95139b77f`  
		Last Modified: Fri, 03 Dec 2021 21:00:17 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18ed072c9481ea2501ceb7126460fd9ed5efbfc1d82a60714d95c4780535d991`  
		Last Modified: Fri, 03 Dec 2021 21:00:17 GMT  
		Size: 5.2 KB (5225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f365d0250ccd4d7fe8466796da2ba876f11c83b4daddc69875dfc1a7033a79b0`  
		Last Modified: Fri, 03 Dec 2021 21:00:17 GMT  
		Size: 2.5 KB (2503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:lts-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:c2c5faf2f199eb1abe110535577faa2262fb300d8d92907861ba0ff310dabde1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **826.0 MB (826035753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78f13512af2ef156fa16d62503f8cd4483448d6e15b959fcb2dfa4015f230659`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 02 Dec 2021 08:07:54 GMT
ADD file:998dc1c35eeeed1ddf46156aeb337fb9b8cbb4855caf994201167a1061f4ecbf in / 
# Thu, 02 Dec 2021 08:07:55 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 09:53:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 09:53:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Dec 2021 09:53:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:07:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:07:23 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 02 Dec 2021 11:07:24 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 02 Dec 2021 11:07:25 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 11:07:26 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 11:07:27 GMT
ENV JAVA_VERSION=11.0.13
# Thu, 02 Dec 2021 11:07:49 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_x64_linux_11.0.13_8.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_aarch64_linux_11.0.13_8.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 02 Dec 2021 11:07:50 GMT
CMD ["jshell"]
# Fri, 03 Dec 2021 10:33:28 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Dec 2021 10:33:28 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Dec 2021 10:33:30 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 03 Dec 2021 10:33:30 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Dec 2021 10:33:31 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 10:33:32 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 10:54:19 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 03 Dec 2021 10:54:20 GMT
ENV TOMCAT_MAJOR=9
# Fri, 03 Dec 2021 10:54:21 GMT
ENV TOMCAT_VERSION=9.0.55
# Fri, 03 Dec 2021 10:54:22 GMT
ENV TOMCAT_SHA512=a0c480b8bba09069bda3b57f54e658450a59d799474ad587dead0ffbf5074c16ee3f9f9c13312d0ff3227c7034589dabf25941fbd672838e9baeee9661e024dc
# Fri, 03 Dec 2021 10:54:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 03 Dec 2021 10:54:45 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 03 Dec 2021 10:54:45 GMT
EXPOSE 8080
# Fri, 03 Dec 2021 10:54:46 GMT
CMD ["catalina.sh" "run"]
# Fri, 03 Dec 2021 16:34:04 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 03 Dec 2021 16:34:05 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 16:34:05 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 16:34:06 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 03 Dec 2021 16:34:07 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 03 Dec 2021 16:34:08 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 03 Dec 2021 16:34:43 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 16:34:44 GMT
ENV XWIKI_VERSION=12.10.10
# Fri, 03 Dec 2021 16:34:45 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.10
# Fri, 03 Dec 2021 16:34:46 GMT
ENV XWIKI_DOWNLOAD_SHA256=42364fd6a3d575c78969ebb12a7d28360ccff3b478379cf30232d6611ccbe9e0
# Fri, 03 Dec 2021 16:36:07 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 03 Dec 2021 16:36:09 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 03 Dec 2021 16:36:10 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 03 Dec 2021 16:36:11 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 03 Dec 2021 16:36:12 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 03 Dec 2021 16:36:14 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 03 Dec 2021 16:36:15 GMT
VOLUME [/usr/local/xwiki]
# Fri, 03 Dec 2021 16:36:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Dec 2021 16:36:16 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:6476cb406b24c94f24348db05d154b814b14ee38860dea1625080e7e08295a80`  
		Last Modified: Thu, 02 Dec 2021 08:40:14 GMT  
		Size: 53.6 MB (53619027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96565d527970b1cc982493f96d6b317b1fbfdd7bf0ea6fd58d44942bb4f597c5`  
		Last Modified: Thu, 02 Dec 2021 10:02:24 GMT  
		Size: 4.9 MB (4937631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8c15f93136056df893ba8088992a38e90dc37210fd6ebb712413fd045c58de`  
		Last Modified: Thu, 02 Dec 2021 10:02:25 GMT  
		Size: 10.7 MB (10655914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee42e24e52cb2f9b50ab14328865298f5ae6ac159219db890afc6366ec641a46`  
		Last Modified: Thu, 02 Dec 2021 10:02:46 GMT  
		Size: 54.7 MB (54669690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1ddc61edfde0dfa7da5e868dfebc0df6e44b7c94700ae79892d861abc32f97`  
		Last Modified: Thu, 02 Dec 2021 11:31:06 GMT  
		Size: 5.4 MB (5420180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:804b3e7e3a2930efff5c50600a2c162b8f2af073ec54a3c44314cc36e68d1a75`  
		Last Modified: Thu, 02 Dec 2021 11:31:05 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c15c25e9529bccafc0b750eb33fb972a05d42a09303dc760b67f89ea21b0bce0`  
		Last Modified: Thu, 02 Dec 2021 11:31:26 GMT  
		Size: 200.7 MB (200712890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac1b17d7ee052527ef86a2354f093548ac170d6d3318a79fa9916fd616c2c40f`  
		Last Modified: Fri, 03 Dec 2021 11:33:43 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8926fc06c65e9a17e2a3110e422fbebb73f63463202846b0b6addc004fd06d`  
		Last Modified: Fri, 03 Dec 2021 11:49:18 GMT  
		Size: 12.3 MB (12292070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56905cdb16153e42e333c2819b26aec2f74860d5924cbe3cf1952f737953c4d`  
		Last Modified: Fri, 03 Dec 2021 16:37:29 GMT  
		Size: 185.2 MB (185204101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b630d0a06c79c04946d7044a763e8bcfa3048eba1ee5917c5d73fbfc202e1cfd`  
		Last Modified: Fri, 03 Dec 2021 16:37:26 GMT  
		Size: 297.7 MB (297666166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c967f3c4012d8a61def666f59f0bb438b973b040c024ca5c194f0bc0f9ac33d1`  
		Last Modified: Fri, 03 Dec 2021 16:37:03 GMT  
		Size: 846.2 KB (846206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e42a536c4ff68942cbe6d89a2a025d4ff95d2d9c502e704b6e3981f2165b1b41`  
		Last Modified: Fri, 03 Dec 2021 16:37:03 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75dec884c2231050cbed8f6719547b3af625afb7df02cc793a7435570a75c981`  
		Last Modified: Fri, 03 Dec 2021 16:37:03 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2481f87da9b8547832e3c87fbe6f23b1e2a9a244bb522970461f859e242e089`  
		Last Modified: Fri, 03 Dec 2021 16:37:03 GMT  
		Size: 5.2 KB (5224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fac7412501c0d3bf5e64c52bf821fbae7b3be8223bc771b9b01062f15e73f60`  
		Last Modified: Fri, 03 Dec 2021 16:37:03 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:mysql-tomcat`

```console
$ docker pull xwiki@sha256:f8be6bb37b7e4385597a7186a40f6d8bcde4f9c609d13f34149ace9ac4d5fdeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:7340a02a837d6d8a7751bb8369c2d9a97643fd4e2530e1bc0098f235933f1e3d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **830.7 MB (830657270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:696e0182c57281cf1de1eefe88fa5d95fde87e191f5464d26c10b3687b03fa51`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:07 GMT
ADD file:e777355768c63f735e5458c7e0ada7f556f27d0493b3af35dc7c34f9c4294ea9 in / 
# Thu, 02 Dec 2021 02:48:08 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:39:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Dec 2021 03:40:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:34:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:34:20 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 02 Dec 2021 11:34:22 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 02 Dec 2021 11:34:22 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 11:34:22 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 11:34:23 GMT
ENV JAVA_VERSION=11.0.13
# Thu, 02 Dec 2021 11:34:48 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_x64_linux_11.0.13_8.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_aarch64_linux_11.0.13_8.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 02 Dec 2021 11:34:49 GMT
CMD ["jshell"]
# Fri, 03 Dec 2021 14:11:49 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Dec 2021 14:11:50 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Dec 2021 14:11:50 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 03 Dec 2021 14:11:51 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Dec 2021 14:11:51 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 14:11:51 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 14:27:34 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 03 Dec 2021 14:27:34 GMT
ENV TOMCAT_MAJOR=9
# Fri, 03 Dec 2021 14:27:34 GMT
ENV TOMCAT_VERSION=9.0.55
# Fri, 03 Dec 2021 14:27:35 GMT
ENV TOMCAT_SHA512=a0c480b8bba09069bda3b57f54e658450a59d799474ad587dead0ffbf5074c16ee3f9f9c13312d0ff3227c7034589dabf25941fbd672838e9baeee9661e024dc
# Fri, 03 Dec 2021 14:28:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 03 Dec 2021 14:28:03 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 03 Dec 2021 14:28:03 GMT
EXPOSE 8080
# Fri, 03 Dec 2021 14:28:03 GMT
CMD ["catalina.sh" "run"]
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 03 Dec 2021 20:52:45 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 20:52:47 GMT
ENV XWIKI_VERSION=13.10
# Fri, 03 Dec 2021 20:52:47 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10
# Fri, 03 Dec 2021 20:52:47 GMT
ENV XWIKI_DOWNLOAD_SHA256=863455ef741ec70539ab89b9981790909f3319b626a107e62fa42c8797df032b
# Fri, 03 Dec 2021 20:53:24 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 03 Dec 2021 20:53:25 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Fri, 03 Dec 2021 20:53:25 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Fri, 03 Dec 2021 20:53:25 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Fri, 03 Dec 2021 20:53:25 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Fri, 03 Dec 2021 20:53:25 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Fri, 03 Dec 2021 20:53:26 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 03 Dec 2021 20:53:27 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 03 Dec 2021 20:53:27 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 03 Dec 2021 20:53:28 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 03 Dec 2021 20:53:28 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 03 Dec 2021 20:53:28 GMT
VOLUME [/usr/local/xwiki]
# Fri, 03 Dec 2021 20:53:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Dec 2021 20:53:29 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:5e0b432e8ba9d9029a000e627840b98ffc1ed0c5172075b7d3e869be0df0fe9b`  
		Last Modified: Thu, 02 Dec 2021 02:53:18 GMT  
		Size: 54.9 MB (54932878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84cfd68b5cea612a8343c346bfa5bd6c486769010d12f7ec86b23c74887feb2`  
		Last Modified: Thu, 02 Dec 2021 03:49:22 GMT  
		Size: 5.2 MB (5153424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b8f2315954535f1e27cd13d777e73da4a787b0aebf4241d225beff3c91cbb1`  
		Last Modified: Thu, 02 Dec 2021 03:49:23 GMT  
		Size: 10.9 MB (10871995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0598fa43a7e793a76c198e8d45d8810394e1cfc943b2673d7fcf5a6fdc4f45b3`  
		Last Modified: Thu, 02 Dec 2021 03:49:46 GMT  
		Size: 54.6 MB (54567844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d35e3be804184359e0904389b149de16f159e30436d7a8a970aef67a4d155b`  
		Last Modified: Thu, 02 Dec 2021 11:54:46 GMT  
		Size: 5.4 MB (5420076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc448a0c88bee4d3cf6a928aa2b4cf499f4cb05034093c581342d414188a566`  
		Last Modified: Thu, 02 Dec 2021 11:54:45 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbdff6e5955b8bcd2e24b1a49fa4ec593ad333133c52911832aa2a7893f542da`  
		Last Modified: Thu, 02 Dec 2021 11:55:04 GMT  
		Size: 203.1 MB (203118915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5daf3771e3d8c27aa89cbcfef659790a2218e319899d49fbccde199e1780a5ef`  
		Last Modified: Fri, 03 Dec 2021 14:54:53 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5434ab540d864811e12dac3650eb0bc67bc8f6d7a6cb1f3c832e2c078c45302c`  
		Last Modified: Fri, 03 Dec 2021 15:08:17 GMT  
		Size: 12.5 MB (12523151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f43f4b2f615c39e867b3110fbc83f1d8fa2b72e4788cdcc91ea5dd73e97102`  
		Last Modified: Fri, 03 Dec 2021 15:08:16 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb64e66bc904d2f87948ce847a95dfa536c19132b599dc7f18ee2fec72ce7a8`  
		Last Modified: Fri, 03 Dec 2021 20:57:50 GMT  
		Size: 189.4 MB (189410805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eda7eb7430a70eef3ce565f0ad28fd9afcc0377bc9ba457bf47563dcf4ca3f25`  
		Last Modified: Fri, 03 Dec 2021 20:57:41 GMT  
		Size: 292.4 MB (292388360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f5388154bcdeb77283073eb4e763658b195a0a27693e1e7c35365485f30f18`  
		Last Modified: Fri, 03 Dec 2021 20:57:22 GMT  
		Size: 2.3 MB (2257828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696eeb26f8bf39548fdbc5946f4443b479ce079f2b4ff73d95ab70f4a77cd237`  
		Last Modified: Fri, 03 Dec 2021 20:57:22 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63b2a04633d035bab8bf65756959a3f6c27236b10f2df105c97760f087d2df0`  
		Last Modified: Fri, 03 Dec 2021 20:57:22 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7ba76bd956a9b63d4559a4144316330627c7dd1ceb4a8ad858ff6462db79078`  
		Last Modified: Fri, 03 Dec 2021 20:57:22 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8cd927e7dbd6905e1a2b5bb99be19019b586b787ad91f5e988fe85277cc44e`  
		Last Modified: Fri, 03 Dec 2021 20:57:22 GMT  
		Size: 2.5 KB (2500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:postgres-tomcat`

```console
$ docker pull xwiki@sha256:d50518708792e2f5ed32a8f64476cd86137ae4114fa48cb8273da99ee32bff2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:0c3fe8d2f8b7734919c768321233164aa60eba53cceb0a4de73f20fbd761b63e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **830.1 MB (830121178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e1da45be61cdd50a06bd28b7845169b75250986f288972a8b05b50ded4a22c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:07 GMT
ADD file:e777355768c63f735e5458c7e0ada7f556f27d0493b3af35dc7c34f9c4294ea9 in / 
# Thu, 02 Dec 2021 02:48:08 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:39:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Dec 2021 03:40:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:34:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:34:20 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 02 Dec 2021 11:34:22 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 02 Dec 2021 11:34:22 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 11:34:22 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 11:34:23 GMT
ENV JAVA_VERSION=11.0.13
# Thu, 02 Dec 2021 11:34:48 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_x64_linux_11.0.13_8.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_aarch64_linux_11.0.13_8.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 02 Dec 2021 11:34:49 GMT
CMD ["jshell"]
# Fri, 03 Dec 2021 14:11:49 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Dec 2021 14:11:50 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Dec 2021 14:11:50 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 03 Dec 2021 14:11:51 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Dec 2021 14:11:51 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 14:11:51 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 14:27:34 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 03 Dec 2021 14:27:34 GMT
ENV TOMCAT_MAJOR=9
# Fri, 03 Dec 2021 14:27:34 GMT
ENV TOMCAT_VERSION=9.0.55
# Fri, 03 Dec 2021 14:27:35 GMT
ENV TOMCAT_SHA512=a0c480b8bba09069bda3b57f54e658450a59d799474ad587dead0ffbf5074c16ee3f9f9c13312d0ff3227c7034589dabf25941fbd672838e9baeee9661e024dc
# Fri, 03 Dec 2021 14:28:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 03 Dec 2021 14:28:03 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 03 Dec 2021 14:28:03 GMT
EXPOSE 8080
# Fri, 03 Dec 2021 14:28:03 GMT
CMD ["catalina.sh" "run"]
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 03 Dec 2021 20:54:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 20:54:05 GMT
ENV XWIKI_VERSION=13.10
# Fri, 03 Dec 2021 20:54:05 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10
# Fri, 03 Dec 2021 20:54:05 GMT
ENV XWIKI_DOWNLOAD_SHA256=863455ef741ec70539ab89b9981790909f3319b626a107e62fa42c8797df032b
# Fri, 03 Dec 2021 20:54:44 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 03 Dec 2021 20:54:45 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 03 Dec 2021 20:54:46 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 03 Dec 2021 20:54:46 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 03 Dec 2021 20:54:47 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 03 Dec 2021 20:54:47 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 03 Dec 2021 20:54:47 GMT
VOLUME [/usr/local/xwiki]
# Fri, 03 Dec 2021 20:54:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Dec 2021 20:54:47 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:5e0b432e8ba9d9029a000e627840b98ffc1ed0c5172075b7d3e869be0df0fe9b`  
		Last Modified: Thu, 02 Dec 2021 02:53:18 GMT  
		Size: 54.9 MB (54932878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84cfd68b5cea612a8343c346bfa5bd6c486769010d12f7ec86b23c74887feb2`  
		Last Modified: Thu, 02 Dec 2021 03:49:22 GMT  
		Size: 5.2 MB (5153424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b8f2315954535f1e27cd13d777e73da4a787b0aebf4241d225beff3c91cbb1`  
		Last Modified: Thu, 02 Dec 2021 03:49:23 GMT  
		Size: 10.9 MB (10871995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0598fa43a7e793a76c198e8d45d8810394e1cfc943b2673d7fcf5a6fdc4f45b3`  
		Last Modified: Thu, 02 Dec 2021 03:49:46 GMT  
		Size: 54.6 MB (54567844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d35e3be804184359e0904389b149de16f159e30436d7a8a970aef67a4d155b`  
		Last Modified: Thu, 02 Dec 2021 11:54:46 GMT  
		Size: 5.4 MB (5420076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc448a0c88bee4d3cf6a928aa2b4cf499f4cb05034093c581342d414188a566`  
		Last Modified: Thu, 02 Dec 2021 11:54:45 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbdff6e5955b8bcd2e24b1a49fa4ec593ad333133c52911832aa2a7893f542da`  
		Last Modified: Thu, 02 Dec 2021 11:55:04 GMT  
		Size: 203.1 MB (203118915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5daf3771e3d8c27aa89cbcfef659790a2218e319899d49fbccde199e1780a5ef`  
		Last Modified: Fri, 03 Dec 2021 14:54:53 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5434ab540d864811e12dac3650eb0bc67bc8f6d7a6cb1f3c832e2c078c45302c`  
		Last Modified: Fri, 03 Dec 2021 15:08:17 GMT  
		Size: 12.5 MB (12523151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f43f4b2f615c39e867b3110fbc83f1d8fa2b72e4788cdcc91ea5dd73e97102`  
		Last Modified: Fri, 03 Dec 2021 15:08:16 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c96c2f945ecec7eda758824db2032432765e7a0128ef11d3c1841ac2dc2e5d95`  
		Last Modified: Fri, 03 Dec 2021 20:59:00 GMT  
		Size: 190.3 MB (190286185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:955cdd39f0085f569763841337c25acef25604257a3de6773891e0bdcadb872d`  
		Last Modified: Fri, 03 Dec 2021 20:58:51 GMT  
		Size: 292.4 MB (292388346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc39c66a904202841f30554fedfe28bc6396c82f817ed5ebefbaed3429b82dd9`  
		Last Modified: Fri, 03 Dec 2021 20:58:32 GMT  
		Size: 846.2 KB (846214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e85be07558e39d22dc2b4a004d91020698ea370e5fb7cf4c99b2a31d3749f6e7`  
		Last Modified: Fri, 03 Dec 2021 20:58:31 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8586fc44e80ce8805adcde54de3c1551ca1c8f7f7e73e7b2d2cd66c38f935be`  
		Last Modified: Fri, 03 Dec 2021 20:58:31 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb2fe06d239087be98bf79090e52955d9ec293fbff5f6db1ff93dd7fee9e488`  
		Last Modified: Fri, 03 Dec 2021 20:58:31 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff38395ff2cff70633d42e627db200f34e988de4c7de698114b9c085bd6c201e`  
		Last Modified: Fri, 03 Dec 2021 20:58:31 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:9791c7dc4989df351c585fcb8eb26596e4a50fdf07313003f37c81bd58d2f84f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **820.8 MB (820758295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a04e1e74e2fd570283613fa3d4d622b67d64a5b21bd3df1e905b07839c312c74`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 02 Dec 2021 08:07:54 GMT
ADD file:998dc1c35eeeed1ddf46156aeb337fb9b8cbb4855caf994201167a1061f4ecbf in / 
# Thu, 02 Dec 2021 08:07:55 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 09:53:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 09:53:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Dec 2021 09:53:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:07:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:07:23 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 02 Dec 2021 11:07:24 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 02 Dec 2021 11:07:25 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 11:07:26 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 11:07:27 GMT
ENV JAVA_VERSION=11.0.13
# Thu, 02 Dec 2021 11:07:49 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_x64_linux_11.0.13_8.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_aarch64_linux_11.0.13_8.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 02 Dec 2021 11:07:50 GMT
CMD ["jshell"]
# Fri, 03 Dec 2021 10:33:28 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Dec 2021 10:33:28 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Dec 2021 10:33:30 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 03 Dec 2021 10:33:30 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Dec 2021 10:33:31 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 10:33:32 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 10:54:19 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 03 Dec 2021 10:54:20 GMT
ENV TOMCAT_MAJOR=9
# Fri, 03 Dec 2021 10:54:21 GMT
ENV TOMCAT_VERSION=9.0.55
# Fri, 03 Dec 2021 10:54:22 GMT
ENV TOMCAT_SHA512=a0c480b8bba09069bda3b57f54e658450a59d799474ad587dead0ffbf5074c16ee3f9f9c13312d0ff3227c7034589dabf25941fbd672838e9baeee9661e024dc
# Fri, 03 Dec 2021 10:54:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 03 Dec 2021 10:54:45 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 03 Dec 2021 10:54:45 GMT
EXPOSE 8080
# Fri, 03 Dec 2021 10:54:46 GMT
CMD ["catalina.sh" "run"]
# Fri, 03 Dec 2021 16:34:04 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 03 Dec 2021 16:34:05 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 16:34:05 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 16:34:06 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 03 Dec 2021 16:34:07 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 03 Dec 2021 16:34:08 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 03 Dec 2021 16:34:43 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 20:40:41 GMT
ENV XWIKI_VERSION=13.10
# Fri, 03 Dec 2021 20:40:42 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10
# Fri, 03 Dec 2021 20:40:43 GMT
ENV XWIKI_DOWNLOAD_SHA256=863455ef741ec70539ab89b9981790909f3319b626a107e62fa42c8797df032b
# Fri, 03 Dec 2021 20:42:05 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 03 Dec 2021 20:42:07 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 03 Dec 2021 20:42:08 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 03 Dec 2021 20:42:09 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 03 Dec 2021 20:42:10 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 03 Dec 2021 20:42:11 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 03 Dec 2021 20:42:12 GMT
VOLUME [/usr/local/xwiki]
# Fri, 03 Dec 2021 20:42:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Dec 2021 20:42:14 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:6476cb406b24c94f24348db05d154b814b14ee38860dea1625080e7e08295a80`  
		Last Modified: Thu, 02 Dec 2021 08:40:14 GMT  
		Size: 53.6 MB (53619027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96565d527970b1cc982493f96d6b317b1fbfdd7bf0ea6fd58d44942bb4f597c5`  
		Last Modified: Thu, 02 Dec 2021 10:02:24 GMT  
		Size: 4.9 MB (4937631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8c15f93136056df893ba8088992a38e90dc37210fd6ebb712413fd045c58de`  
		Last Modified: Thu, 02 Dec 2021 10:02:25 GMT  
		Size: 10.7 MB (10655914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee42e24e52cb2f9b50ab14328865298f5ae6ac159219db890afc6366ec641a46`  
		Last Modified: Thu, 02 Dec 2021 10:02:46 GMT  
		Size: 54.7 MB (54669690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1ddc61edfde0dfa7da5e868dfebc0df6e44b7c94700ae79892d861abc32f97`  
		Last Modified: Thu, 02 Dec 2021 11:31:06 GMT  
		Size: 5.4 MB (5420180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:804b3e7e3a2930efff5c50600a2c162b8f2af073ec54a3c44314cc36e68d1a75`  
		Last Modified: Thu, 02 Dec 2021 11:31:05 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c15c25e9529bccafc0b750eb33fb972a05d42a09303dc760b67f89ea21b0bce0`  
		Last Modified: Thu, 02 Dec 2021 11:31:26 GMT  
		Size: 200.7 MB (200712890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac1b17d7ee052527ef86a2354f093548ac170d6d3318a79fa9916fd616c2c40f`  
		Last Modified: Fri, 03 Dec 2021 11:33:43 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8926fc06c65e9a17e2a3110e422fbebb73f63463202846b0b6addc004fd06d`  
		Last Modified: Fri, 03 Dec 2021 11:49:18 GMT  
		Size: 12.3 MB (12292070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56905cdb16153e42e333c2819b26aec2f74860d5924cbe3cf1952f737953c4d`  
		Last Modified: Fri, 03 Dec 2021 16:37:29 GMT  
		Size: 185.2 MB (185204101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb1a3f2a620897e3ef5f866de2723c108b289d8308a9c3fea23ed2d98413c95`  
		Last Modified: Fri, 03 Dec 2021 20:43:19 GMT  
		Size: 292.4 MB (292388612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19092ac47724d18b94e705918c5687646e63dc774df241652ec6c77177eb0ad`  
		Last Modified: Fri, 03 Dec 2021 20:42:56 GMT  
		Size: 846.2 KB (846209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8959324a980da8d5711d1b493e27fea4054370769e11fe27b0341d928e7cad7b`  
		Last Modified: Fri, 03 Dec 2021 20:42:56 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3315518eeae081a901de36d667f5894a3bd974fdaa2943e8f6eff269b353b34d`  
		Last Modified: Fri, 03 Dec 2021 20:42:56 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b25a16e439c94dc4b0d402bdc659b525b4bc914799cb79e15e289e26f5eabdd7`  
		Last Modified: Fri, 03 Dec 2021 20:42:56 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0747fe5f75ab79fb9a9f111b719dec4f788fe07fcecc62412907b32ff5e2e9c`  
		Last Modified: Fri, 03 Dec 2021 20:42:56 GMT  
		Size: 2.5 KB (2500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:stable`

```console
$ docker pull xwiki@sha256:f8be6bb37b7e4385597a7186a40f6d8bcde4f9c609d13f34149ace9ac4d5fdeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:stable` - linux; amd64

```console
$ docker pull xwiki@sha256:7340a02a837d6d8a7751bb8369c2d9a97643fd4e2530e1bc0098f235933f1e3d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **830.7 MB (830657270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:696e0182c57281cf1de1eefe88fa5d95fde87e191f5464d26c10b3687b03fa51`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:07 GMT
ADD file:e777355768c63f735e5458c7e0ada7f556f27d0493b3af35dc7c34f9c4294ea9 in / 
# Thu, 02 Dec 2021 02:48:08 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:39:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Dec 2021 03:40:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:34:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:34:20 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 02 Dec 2021 11:34:22 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 02 Dec 2021 11:34:22 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 11:34:22 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 11:34:23 GMT
ENV JAVA_VERSION=11.0.13
# Thu, 02 Dec 2021 11:34:48 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_x64_linux_11.0.13_8.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_aarch64_linux_11.0.13_8.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 02 Dec 2021 11:34:49 GMT
CMD ["jshell"]
# Fri, 03 Dec 2021 14:11:49 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Dec 2021 14:11:50 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Dec 2021 14:11:50 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 03 Dec 2021 14:11:51 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Dec 2021 14:11:51 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 14:11:51 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 14:27:34 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 03 Dec 2021 14:27:34 GMT
ENV TOMCAT_MAJOR=9
# Fri, 03 Dec 2021 14:27:34 GMT
ENV TOMCAT_VERSION=9.0.55
# Fri, 03 Dec 2021 14:27:35 GMT
ENV TOMCAT_SHA512=a0c480b8bba09069bda3b57f54e658450a59d799474ad587dead0ffbf5074c16ee3f9f9c13312d0ff3227c7034589dabf25941fbd672838e9baeee9661e024dc
# Fri, 03 Dec 2021 14:28:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 03 Dec 2021 14:28:03 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 03 Dec 2021 14:28:03 GMT
EXPOSE 8080
# Fri, 03 Dec 2021 14:28:03 GMT
CMD ["catalina.sh" "run"]
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 03 Dec 2021 20:52:45 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 20:52:47 GMT
ENV XWIKI_VERSION=13.10
# Fri, 03 Dec 2021 20:52:47 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10
# Fri, 03 Dec 2021 20:52:47 GMT
ENV XWIKI_DOWNLOAD_SHA256=863455ef741ec70539ab89b9981790909f3319b626a107e62fa42c8797df032b
# Fri, 03 Dec 2021 20:53:24 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 03 Dec 2021 20:53:25 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Fri, 03 Dec 2021 20:53:25 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Fri, 03 Dec 2021 20:53:25 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Fri, 03 Dec 2021 20:53:25 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Fri, 03 Dec 2021 20:53:25 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Fri, 03 Dec 2021 20:53:26 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 03 Dec 2021 20:53:27 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 03 Dec 2021 20:53:27 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 03 Dec 2021 20:53:28 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 03 Dec 2021 20:53:28 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 03 Dec 2021 20:53:28 GMT
VOLUME [/usr/local/xwiki]
# Fri, 03 Dec 2021 20:53:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Dec 2021 20:53:29 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:5e0b432e8ba9d9029a000e627840b98ffc1ed0c5172075b7d3e869be0df0fe9b`  
		Last Modified: Thu, 02 Dec 2021 02:53:18 GMT  
		Size: 54.9 MB (54932878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84cfd68b5cea612a8343c346bfa5bd6c486769010d12f7ec86b23c74887feb2`  
		Last Modified: Thu, 02 Dec 2021 03:49:22 GMT  
		Size: 5.2 MB (5153424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b8f2315954535f1e27cd13d777e73da4a787b0aebf4241d225beff3c91cbb1`  
		Last Modified: Thu, 02 Dec 2021 03:49:23 GMT  
		Size: 10.9 MB (10871995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0598fa43a7e793a76c198e8d45d8810394e1cfc943b2673d7fcf5a6fdc4f45b3`  
		Last Modified: Thu, 02 Dec 2021 03:49:46 GMT  
		Size: 54.6 MB (54567844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d35e3be804184359e0904389b149de16f159e30436d7a8a970aef67a4d155b`  
		Last Modified: Thu, 02 Dec 2021 11:54:46 GMT  
		Size: 5.4 MB (5420076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc448a0c88bee4d3cf6a928aa2b4cf499f4cb05034093c581342d414188a566`  
		Last Modified: Thu, 02 Dec 2021 11:54:45 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbdff6e5955b8bcd2e24b1a49fa4ec593ad333133c52911832aa2a7893f542da`  
		Last Modified: Thu, 02 Dec 2021 11:55:04 GMT  
		Size: 203.1 MB (203118915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5daf3771e3d8c27aa89cbcfef659790a2218e319899d49fbccde199e1780a5ef`  
		Last Modified: Fri, 03 Dec 2021 14:54:53 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5434ab540d864811e12dac3650eb0bc67bc8f6d7a6cb1f3c832e2c078c45302c`  
		Last Modified: Fri, 03 Dec 2021 15:08:17 GMT  
		Size: 12.5 MB (12523151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f43f4b2f615c39e867b3110fbc83f1d8fa2b72e4788cdcc91ea5dd73e97102`  
		Last Modified: Fri, 03 Dec 2021 15:08:16 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb64e66bc904d2f87948ce847a95dfa536c19132b599dc7f18ee2fec72ce7a8`  
		Last Modified: Fri, 03 Dec 2021 20:57:50 GMT  
		Size: 189.4 MB (189410805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eda7eb7430a70eef3ce565f0ad28fd9afcc0377bc9ba457bf47563dcf4ca3f25`  
		Last Modified: Fri, 03 Dec 2021 20:57:41 GMT  
		Size: 292.4 MB (292388360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f5388154bcdeb77283073eb4e763658b195a0a27693e1e7c35365485f30f18`  
		Last Modified: Fri, 03 Dec 2021 20:57:22 GMT  
		Size: 2.3 MB (2257828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696eeb26f8bf39548fdbc5946f4443b479ce079f2b4ff73d95ab70f4a77cd237`  
		Last Modified: Fri, 03 Dec 2021 20:57:22 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63b2a04633d035bab8bf65756959a3f6c27236b10f2df105c97760f087d2df0`  
		Last Modified: Fri, 03 Dec 2021 20:57:22 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7ba76bd956a9b63d4559a4144316330627c7dd1ceb4a8ad858ff6462db79078`  
		Last Modified: Fri, 03 Dec 2021 20:57:22 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8cd927e7dbd6905e1a2b5bb99be19019b586b787ad91f5e988fe85277cc44e`  
		Last Modified: Fri, 03 Dec 2021 20:57:22 GMT  
		Size: 2.5 KB (2500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:stable-mysql`

```console
$ docker pull xwiki@sha256:f8be6bb37b7e4385597a7186a40f6d8bcde4f9c609d13f34149ace9ac4d5fdeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:stable-mysql` - linux; amd64

```console
$ docker pull xwiki@sha256:7340a02a837d6d8a7751bb8369c2d9a97643fd4e2530e1bc0098f235933f1e3d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **830.7 MB (830657270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:696e0182c57281cf1de1eefe88fa5d95fde87e191f5464d26c10b3687b03fa51`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:07 GMT
ADD file:e777355768c63f735e5458c7e0ada7f556f27d0493b3af35dc7c34f9c4294ea9 in / 
# Thu, 02 Dec 2021 02:48:08 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:39:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Dec 2021 03:40:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:34:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:34:20 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 02 Dec 2021 11:34:22 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 02 Dec 2021 11:34:22 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 11:34:22 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 11:34:23 GMT
ENV JAVA_VERSION=11.0.13
# Thu, 02 Dec 2021 11:34:48 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_x64_linux_11.0.13_8.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_aarch64_linux_11.0.13_8.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 02 Dec 2021 11:34:49 GMT
CMD ["jshell"]
# Fri, 03 Dec 2021 14:11:49 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Dec 2021 14:11:50 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Dec 2021 14:11:50 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 03 Dec 2021 14:11:51 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Dec 2021 14:11:51 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 14:11:51 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 14:27:34 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 03 Dec 2021 14:27:34 GMT
ENV TOMCAT_MAJOR=9
# Fri, 03 Dec 2021 14:27:34 GMT
ENV TOMCAT_VERSION=9.0.55
# Fri, 03 Dec 2021 14:27:35 GMT
ENV TOMCAT_SHA512=a0c480b8bba09069bda3b57f54e658450a59d799474ad587dead0ffbf5074c16ee3f9f9c13312d0ff3227c7034589dabf25941fbd672838e9baeee9661e024dc
# Fri, 03 Dec 2021 14:28:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 03 Dec 2021 14:28:03 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 03 Dec 2021 14:28:03 GMT
EXPOSE 8080
# Fri, 03 Dec 2021 14:28:03 GMT
CMD ["catalina.sh" "run"]
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 03 Dec 2021 20:52:45 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 20:52:47 GMT
ENV XWIKI_VERSION=13.10
# Fri, 03 Dec 2021 20:52:47 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10
# Fri, 03 Dec 2021 20:52:47 GMT
ENV XWIKI_DOWNLOAD_SHA256=863455ef741ec70539ab89b9981790909f3319b626a107e62fa42c8797df032b
# Fri, 03 Dec 2021 20:53:24 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 03 Dec 2021 20:53:25 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Fri, 03 Dec 2021 20:53:25 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Fri, 03 Dec 2021 20:53:25 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Fri, 03 Dec 2021 20:53:25 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Fri, 03 Dec 2021 20:53:25 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Fri, 03 Dec 2021 20:53:26 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 03 Dec 2021 20:53:27 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 03 Dec 2021 20:53:27 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 03 Dec 2021 20:53:28 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 03 Dec 2021 20:53:28 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 03 Dec 2021 20:53:28 GMT
VOLUME [/usr/local/xwiki]
# Fri, 03 Dec 2021 20:53:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Dec 2021 20:53:29 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:5e0b432e8ba9d9029a000e627840b98ffc1ed0c5172075b7d3e869be0df0fe9b`  
		Last Modified: Thu, 02 Dec 2021 02:53:18 GMT  
		Size: 54.9 MB (54932878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84cfd68b5cea612a8343c346bfa5bd6c486769010d12f7ec86b23c74887feb2`  
		Last Modified: Thu, 02 Dec 2021 03:49:22 GMT  
		Size: 5.2 MB (5153424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b8f2315954535f1e27cd13d777e73da4a787b0aebf4241d225beff3c91cbb1`  
		Last Modified: Thu, 02 Dec 2021 03:49:23 GMT  
		Size: 10.9 MB (10871995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0598fa43a7e793a76c198e8d45d8810394e1cfc943b2673d7fcf5a6fdc4f45b3`  
		Last Modified: Thu, 02 Dec 2021 03:49:46 GMT  
		Size: 54.6 MB (54567844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d35e3be804184359e0904389b149de16f159e30436d7a8a970aef67a4d155b`  
		Last Modified: Thu, 02 Dec 2021 11:54:46 GMT  
		Size: 5.4 MB (5420076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc448a0c88bee4d3cf6a928aa2b4cf499f4cb05034093c581342d414188a566`  
		Last Modified: Thu, 02 Dec 2021 11:54:45 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbdff6e5955b8bcd2e24b1a49fa4ec593ad333133c52911832aa2a7893f542da`  
		Last Modified: Thu, 02 Dec 2021 11:55:04 GMT  
		Size: 203.1 MB (203118915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5daf3771e3d8c27aa89cbcfef659790a2218e319899d49fbccde199e1780a5ef`  
		Last Modified: Fri, 03 Dec 2021 14:54:53 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5434ab540d864811e12dac3650eb0bc67bc8f6d7a6cb1f3c832e2c078c45302c`  
		Last Modified: Fri, 03 Dec 2021 15:08:17 GMT  
		Size: 12.5 MB (12523151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f43f4b2f615c39e867b3110fbc83f1d8fa2b72e4788cdcc91ea5dd73e97102`  
		Last Modified: Fri, 03 Dec 2021 15:08:16 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb64e66bc904d2f87948ce847a95dfa536c19132b599dc7f18ee2fec72ce7a8`  
		Last Modified: Fri, 03 Dec 2021 20:57:50 GMT  
		Size: 189.4 MB (189410805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eda7eb7430a70eef3ce565f0ad28fd9afcc0377bc9ba457bf47563dcf4ca3f25`  
		Last Modified: Fri, 03 Dec 2021 20:57:41 GMT  
		Size: 292.4 MB (292388360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f5388154bcdeb77283073eb4e763658b195a0a27693e1e7c35365485f30f18`  
		Last Modified: Fri, 03 Dec 2021 20:57:22 GMT  
		Size: 2.3 MB (2257828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696eeb26f8bf39548fdbc5946f4443b479ce079f2b4ff73d95ab70f4a77cd237`  
		Last Modified: Fri, 03 Dec 2021 20:57:22 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63b2a04633d035bab8bf65756959a3f6c27236b10f2df105c97760f087d2df0`  
		Last Modified: Fri, 03 Dec 2021 20:57:22 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7ba76bd956a9b63d4559a4144316330627c7dd1ceb4a8ad858ff6462db79078`  
		Last Modified: Fri, 03 Dec 2021 20:57:22 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8cd927e7dbd6905e1a2b5bb99be19019b586b787ad91f5e988fe85277cc44e`  
		Last Modified: Fri, 03 Dec 2021 20:57:22 GMT  
		Size: 2.5 KB (2500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:stable-mysql-tomcat`

```console
$ docker pull xwiki@sha256:f8be6bb37b7e4385597a7186a40f6d8bcde4f9c609d13f34149ace9ac4d5fdeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:stable-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:7340a02a837d6d8a7751bb8369c2d9a97643fd4e2530e1bc0098f235933f1e3d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **830.7 MB (830657270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:696e0182c57281cf1de1eefe88fa5d95fde87e191f5464d26c10b3687b03fa51`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:07 GMT
ADD file:e777355768c63f735e5458c7e0ada7f556f27d0493b3af35dc7c34f9c4294ea9 in / 
# Thu, 02 Dec 2021 02:48:08 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:39:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Dec 2021 03:40:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:34:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:34:20 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 02 Dec 2021 11:34:22 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 02 Dec 2021 11:34:22 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 11:34:22 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 11:34:23 GMT
ENV JAVA_VERSION=11.0.13
# Thu, 02 Dec 2021 11:34:48 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_x64_linux_11.0.13_8.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_aarch64_linux_11.0.13_8.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 02 Dec 2021 11:34:49 GMT
CMD ["jshell"]
# Fri, 03 Dec 2021 14:11:49 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Dec 2021 14:11:50 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Dec 2021 14:11:50 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 03 Dec 2021 14:11:51 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Dec 2021 14:11:51 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 14:11:51 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 14:27:34 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 03 Dec 2021 14:27:34 GMT
ENV TOMCAT_MAJOR=9
# Fri, 03 Dec 2021 14:27:34 GMT
ENV TOMCAT_VERSION=9.0.55
# Fri, 03 Dec 2021 14:27:35 GMT
ENV TOMCAT_SHA512=a0c480b8bba09069bda3b57f54e658450a59d799474ad587dead0ffbf5074c16ee3f9f9c13312d0ff3227c7034589dabf25941fbd672838e9baeee9661e024dc
# Fri, 03 Dec 2021 14:28:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 03 Dec 2021 14:28:03 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 03 Dec 2021 14:28:03 GMT
EXPOSE 8080
# Fri, 03 Dec 2021 14:28:03 GMT
CMD ["catalina.sh" "run"]
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 03 Dec 2021 20:52:45 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 20:52:47 GMT
ENV XWIKI_VERSION=13.10
# Fri, 03 Dec 2021 20:52:47 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10
# Fri, 03 Dec 2021 20:52:47 GMT
ENV XWIKI_DOWNLOAD_SHA256=863455ef741ec70539ab89b9981790909f3319b626a107e62fa42c8797df032b
# Fri, 03 Dec 2021 20:53:24 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 03 Dec 2021 20:53:25 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Fri, 03 Dec 2021 20:53:25 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Fri, 03 Dec 2021 20:53:25 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Fri, 03 Dec 2021 20:53:25 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Fri, 03 Dec 2021 20:53:25 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Fri, 03 Dec 2021 20:53:26 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 03 Dec 2021 20:53:27 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 03 Dec 2021 20:53:27 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 03 Dec 2021 20:53:28 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 03 Dec 2021 20:53:28 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 03 Dec 2021 20:53:28 GMT
VOLUME [/usr/local/xwiki]
# Fri, 03 Dec 2021 20:53:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Dec 2021 20:53:29 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:5e0b432e8ba9d9029a000e627840b98ffc1ed0c5172075b7d3e869be0df0fe9b`  
		Last Modified: Thu, 02 Dec 2021 02:53:18 GMT  
		Size: 54.9 MB (54932878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84cfd68b5cea612a8343c346bfa5bd6c486769010d12f7ec86b23c74887feb2`  
		Last Modified: Thu, 02 Dec 2021 03:49:22 GMT  
		Size: 5.2 MB (5153424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b8f2315954535f1e27cd13d777e73da4a787b0aebf4241d225beff3c91cbb1`  
		Last Modified: Thu, 02 Dec 2021 03:49:23 GMT  
		Size: 10.9 MB (10871995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0598fa43a7e793a76c198e8d45d8810394e1cfc943b2673d7fcf5a6fdc4f45b3`  
		Last Modified: Thu, 02 Dec 2021 03:49:46 GMT  
		Size: 54.6 MB (54567844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d35e3be804184359e0904389b149de16f159e30436d7a8a970aef67a4d155b`  
		Last Modified: Thu, 02 Dec 2021 11:54:46 GMT  
		Size: 5.4 MB (5420076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc448a0c88bee4d3cf6a928aa2b4cf499f4cb05034093c581342d414188a566`  
		Last Modified: Thu, 02 Dec 2021 11:54:45 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbdff6e5955b8bcd2e24b1a49fa4ec593ad333133c52911832aa2a7893f542da`  
		Last Modified: Thu, 02 Dec 2021 11:55:04 GMT  
		Size: 203.1 MB (203118915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5daf3771e3d8c27aa89cbcfef659790a2218e319899d49fbccde199e1780a5ef`  
		Last Modified: Fri, 03 Dec 2021 14:54:53 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5434ab540d864811e12dac3650eb0bc67bc8f6d7a6cb1f3c832e2c078c45302c`  
		Last Modified: Fri, 03 Dec 2021 15:08:17 GMT  
		Size: 12.5 MB (12523151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f43f4b2f615c39e867b3110fbc83f1d8fa2b72e4788cdcc91ea5dd73e97102`  
		Last Modified: Fri, 03 Dec 2021 15:08:16 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb64e66bc904d2f87948ce847a95dfa536c19132b599dc7f18ee2fec72ce7a8`  
		Last Modified: Fri, 03 Dec 2021 20:57:50 GMT  
		Size: 189.4 MB (189410805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eda7eb7430a70eef3ce565f0ad28fd9afcc0377bc9ba457bf47563dcf4ca3f25`  
		Last Modified: Fri, 03 Dec 2021 20:57:41 GMT  
		Size: 292.4 MB (292388360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f5388154bcdeb77283073eb4e763658b195a0a27693e1e7c35365485f30f18`  
		Last Modified: Fri, 03 Dec 2021 20:57:22 GMT  
		Size: 2.3 MB (2257828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696eeb26f8bf39548fdbc5946f4443b479ce079f2b4ff73d95ab70f4a77cd237`  
		Last Modified: Fri, 03 Dec 2021 20:57:22 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63b2a04633d035bab8bf65756959a3f6c27236b10f2df105c97760f087d2df0`  
		Last Modified: Fri, 03 Dec 2021 20:57:22 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7ba76bd956a9b63d4559a4144316330627c7dd1ceb4a8ad858ff6462db79078`  
		Last Modified: Fri, 03 Dec 2021 20:57:22 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8cd927e7dbd6905e1a2b5bb99be19019b586b787ad91f5e988fe85277cc44e`  
		Last Modified: Fri, 03 Dec 2021 20:57:22 GMT  
		Size: 2.5 KB (2500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:stable-postgres`

```console
$ docker pull xwiki@sha256:d50518708792e2f5ed32a8f64476cd86137ae4114fa48cb8273da99ee32bff2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:stable-postgres` - linux; amd64

```console
$ docker pull xwiki@sha256:0c3fe8d2f8b7734919c768321233164aa60eba53cceb0a4de73f20fbd761b63e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **830.1 MB (830121178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e1da45be61cdd50a06bd28b7845169b75250986f288972a8b05b50ded4a22c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:07 GMT
ADD file:e777355768c63f735e5458c7e0ada7f556f27d0493b3af35dc7c34f9c4294ea9 in / 
# Thu, 02 Dec 2021 02:48:08 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:39:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Dec 2021 03:40:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:34:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:34:20 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 02 Dec 2021 11:34:22 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 02 Dec 2021 11:34:22 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 11:34:22 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 11:34:23 GMT
ENV JAVA_VERSION=11.0.13
# Thu, 02 Dec 2021 11:34:48 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_x64_linux_11.0.13_8.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_aarch64_linux_11.0.13_8.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 02 Dec 2021 11:34:49 GMT
CMD ["jshell"]
# Fri, 03 Dec 2021 14:11:49 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Dec 2021 14:11:50 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Dec 2021 14:11:50 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 03 Dec 2021 14:11:51 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Dec 2021 14:11:51 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 14:11:51 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 14:27:34 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 03 Dec 2021 14:27:34 GMT
ENV TOMCAT_MAJOR=9
# Fri, 03 Dec 2021 14:27:34 GMT
ENV TOMCAT_VERSION=9.0.55
# Fri, 03 Dec 2021 14:27:35 GMT
ENV TOMCAT_SHA512=a0c480b8bba09069bda3b57f54e658450a59d799474ad587dead0ffbf5074c16ee3f9f9c13312d0ff3227c7034589dabf25941fbd672838e9baeee9661e024dc
# Fri, 03 Dec 2021 14:28:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 03 Dec 2021 14:28:03 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 03 Dec 2021 14:28:03 GMT
EXPOSE 8080
# Fri, 03 Dec 2021 14:28:03 GMT
CMD ["catalina.sh" "run"]
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 03 Dec 2021 20:54:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 20:54:05 GMT
ENV XWIKI_VERSION=13.10
# Fri, 03 Dec 2021 20:54:05 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10
# Fri, 03 Dec 2021 20:54:05 GMT
ENV XWIKI_DOWNLOAD_SHA256=863455ef741ec70539ab89b9981790909f3319b626a107e62fa42c8797df032b
# Fri, 03 Dec 2021 20:54:44 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 03 Dec 2021 20:54:45 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 03 Dec 2021 20:54:46 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 03 Dec 2021 20:54:46 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 03 Dec 2021 20:54:47 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 03 Dec 2021 20:54:47 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 03 Dec 2021 20:54:47 GMT
VOLUME [/usr/local/xwiki]
# Fri, 03 Dec 2021 20:54:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Dec 2021 20:54:47 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:5e0b432e8ba9d9029a000e627840b98ffc1ed0c5172075b7d3e869be0df0fe9b`  
		Last Modified: Thu, 02 Dec 2021 02:53:18 GMT  
		Size: 54.9 MB (54932878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84cfd68b5cea612a8343c346bfa5bd6c486769010d12f7ec86b23c74887feb2`  
		Last Modified: Thu, 02 Dec 2021 03:49:22 GMT  
		Size: 5.2 MB (5153424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b8f2315954535f1e27cd13d777e73da4a787b0aebf4241d225beff3c91cbb1`  
		Last Modified: Thu, 02 Dec 2021 03:49:23 GMT  
		Size: 10.9 MB (10871995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0598fa43a7e793a76c198e8d45d8810394e1cfc943b2673d7fcf5a6fdc4f45b3`  
		Last Modified: Thu, 02 Dec 2021 03:49:46 GMT  
		Size: 54.6 MB (54567844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d35e3be804184359e0904389b149de16f159e30436d7a8a970aef67a4d155b`  
		Last Modified: Thu, 02 Dec 2021 11:54:46 GMT  
		Size: 5.4 MB (5420076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc448a0c88bee4d3cf6a928aa2b4cf499f4cb05034093c581342d414188a566`  
		Last Modified: Thu, 02 Dec 2021 11:54:45 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbdff6e5955b8bcd2e24b1a49fa4ec593ad333133c52911832aa2a7893f542da`  
		Last Modified: Thu, 02 Dec 2021 11:55:04 GMT  
		Size: 203.1 MB (203118915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5daf3771e3d8c27aa89cbcfef659790a2218e319899d49fbccde199e1780a5ef`  
		Last Modified: Fri, 03 Dec 2021 14:54:53 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5434ab540d864811e12dac3650eb0bc67bc8f6d7a6cb1f3c832e2c078c45302c`  
		Last Modified: Fri, 03 Dec 2021 15:08:17 GMT  
		Size: 12.5 MB (12523151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f43f4b2f615c39e867b3110fbc83f1d8fa2b72e4788cdcc91ea5dd73e97102`  
		Last Modified: Fri, 03 Dec 2021 15:08:16 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c96c2f945ecec7eda758824db2032432765e7a0128ef11d3c1841ac2dc2e5d95`  
		Last Modified: Fri, 03 Dec 2021 20:59:00 GMT  
		Size: 190.3 MB (190286185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:955cdd39f0085f569763841337c25acef25604257a3de6773891e0bdcadb872d`  
		Last Modified: Fri, 03 Dec 2021 20:58:51 GMT  
		Size: 292.4 MB (292388346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc39c66a904202841f30554fedfe28bc6396c82f817ed5ebefbaed3429b82dd9`  
		Last Modified: Fri, 03 Dec 2021 20:58:32 GMT  
		Size: 846.2 KB (846214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e85be07558e39d22dc2b4a004d91020698ea370e5fb7cf4c99b2a31d3749f6e7`  
		Last Modified: Fri, 03 Dec 2021 20:58:31 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8586fc44e80ce8805adcde54de3c1551ca1c8f7f7e73e7b2d2cd66c38f935be`  
		Last Modified: Fri, 03 Dec 2021 20:58:31 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb2fe06d239087be98bf79090e52955d9ec293fbff5f6db1ff93dd7fee9e488`  
		Last Modified: Fri, 03 Dec 2021 20:58:31 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff38395ff2cff70633d42e627db200f34e988de4c7de698114b9c085bd6c201e`  
		Last Modified: Fri, 03 Dec 2021 20:58:31 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:stable-postgres` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:9791c7dc4989df351c585fcb8eb26596e4a50fdf07313003f37c81bd58d2f84f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **820.8 MB (820758295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a04e1e74e2fd570283613fa3d4d622b67d64a5b21bd3df1e905b07839c312c74`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 02 Dec 2021 08:07:54 GMT
ADD file:998dc1c35eeeed1ddf46156aeb337fb9b8cbb4855caf994201167a1061f4ecbf in / 
# Thu, 02 Dec 2021 08:07:55 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 09:53:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 09:53:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Dec 2021 09:53:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:07:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:07:23 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 02 Dec 2021 11:07:24 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 02 Dec 2021 11:07:25 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 11:07:26 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 11:07:27 GMT
ENV JAVA_VERSION=11.0.13
# Thu, 02 Dec 2021 11:07:49 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_x64_linux_11.0.13_8.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_aarch64_linux_11.0.13_8.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 02 Dec 2021 11:07:50 GMT
CMD ["jshell"]
# Fri, 03 Dec 2021 10:33:28 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Dec 2021 10:33:28 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Dec 2021 10:33:30 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 03 Dec 2021 10:33:30 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Dec 2021 10:33:31 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 10:33:32 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 10:54:19 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 03 Dec 2021 10:54:20 GMT
ENV TOMCAT_MAJOR=9
# Fri, 03 Dec 2021 10:54:21 GMT
ENV TOMCAT_VERSION=9.0.55
# Fri, 03 Dec 2021 10:54:22 GMT
ENV TOMCAT_SHA512=a0c480b8bba09069bda3b57f54e658450a59d799474ad587dead0ffbf5074c16ee3f9f9c13312d0ff3227c7034589dabf25941fbd672838e9baeee9661e024dc
# Fri, 03 Dec 2021 10:54:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 03 Dec 2021 10:54:45 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 03 Dec 2021 10:54:45 GMT
EXPOSE 8080
# Fri, 03 Dec 2021 10:54:46 GMT
CMD ["catalina.sh" "run"]
# Fri, 03 Dec 2021 16:34:04 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 03 Dec 2021 16:34:05 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 16:34:05 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 16:34:06 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 03 Dec 2021 16:34:07 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 03 Dec 2021 16:34:08 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 03 Dec 2021 16:34:43 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 20:40:41 GMT
ENV XWIKI_VERSION=13.10
# Fri, 03 Dec 2021 20:40:42 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10
# Fri, 03 Dec 2021 20:40:43 GMT
ENV XWIKI_DOWNLOAD_SHA256=863455ef741ec70539ab89b9981790909f3319b626a107e62fa42c8797df032b
# Fri, 03 Dec 2021 20:42:05 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 03 Dec 2021 20:42:07 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 03 Dec 2021 20:42:08 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 03 Dec 2021 20:42:09 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 03 Dec 2021 20:42:10 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 03 Dec 2021 20:42:11 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 03 Dec 2021 20:42:12 GMT
VOLUME [/usr/local/xwiki]
# Fri, 03 Dec 2021 20:42:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Dec 2021 20:42:14 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:6476cb406b24c94f24348db05d154b814b14ee38860dea1625080e7e08295a80`  
		Last Modified: Thu, 02 Dec 2021 08:40:14 GMT  
		Size: 53.6 MB (53619027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96565d527970b1cc982493f96d6b317b1fbfdd7bf0ea6fd58d44942bb4f597c5`  
		Last Modified: Thu, 02 Dec 2021 10:02:24 GMT  
		Size: 4.9 MB (4937631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8c15f93136056df893ba8088992a38e90dc37210fd6ebb712413fd045c58de`  
		Last Modified: Thu, 02 Dec 2021 10:02:25 GMT  
		Size: 10.7 MB (10655914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee42e24e52cb2f9b50ab14328865298f5ae6ac159219db890afc6366ec641a46`  
		Last Modified: Thu, 02 Dec 2021 10:02:46 GMT  
		Size: 54.7 MB (54669690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1ddc61edfde0dfa7da5e868dfebc0df6e44b7c94700ae79892d861abc32f97`  
		Last Modified: Thu, 02 Dec 2021 11:31:06 GMT  
		Size: 5.4 MB (5420180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:804b3e7e3a2930efff5c50600a2c162b8f2af073ec54a3c44314cc36e68d1a75`  
		Last Modified: Thu, 02 Dec 2021 11:31:05 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c15c25e9529bccafc0b750eb33fb972a05d42a09303dc760b67f89ea21b0bce0`  
		Last Modified: Thu, 02 Dec 2021 11:31:26 GMT  
		Size: 200.7 MB (200712890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac1b17d7ee052527ef86a2354f093548ac170d6d3318a79fa9916fd616c2c40f`  
		Last Modified: Fri, 03 Dec 2021 11:33:43 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8926fc06c65e9a17e2a3110e422fbebb73f63463202846b0b6addc004fd06d`  
		Last Modified: Fri, 03 Dec 2021 11:49:18 GMT  
		Size: 12.3 MB (12292070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56905cdb16153e42e333c2819b26aec2f74860d5924cbe3cf1952f737953c4d`  
		Last Modified: Fri, 03 Dec 2021 16:37:29 GMT  
		Size: 185.2 MB (185204101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb1a3f2a620897e3ef5f866de2723c108b289d8308a9c3fea23ed2d98413c95`  
		Last Modified: Fri, 03 Dec 2021 20:43:19 GMT  
		Size: 292.4 MB (292388612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19092ac47724d18b94e705918c5687646e63dc774df241652ec6c77177eb0ad`  
		Last Modified: Fri, 03 Dec 2021 20:42:56 GMT  
		Size: 846.2 KB (846209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8959324a980da8d5711d1b493e27fea4054370769e11fe27b0341d928e7cad7b`  
		Last Modified: Fri, 03 Dec 2021 20:42:56 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3315518eeae081a901de36d667f5894a3bd974fdaa2943e8f6eff269b353b34d`  
		Last Modified: Fri, 03 Dec 2021 20:42:56 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b25a16e439c94dc4b0d402bdc659b525b4bc914799cb79e15e289e26f5eabdd7`  
		Last Modified: Fri, 03 Dec 2021 20:42:56 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0747fe5f75ab79fb9a9f111b719dec4f788fe07fcecc62412907b32ff5e2e9c`  
		Last Modified: Fri, 03 Dec 2021 20:42:56 GMT  
		Size: 2.5 KB (2500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:stable-postgres-tomcat`

```console
$ docker pull xwiki@sha256:d50518708792e2f5ed32a8f64476cd86137ae4114fa48cb8273da99ee32bff2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:stable-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:0c3fe8d2f8b7734919c768321233164aa60eba53cceb0a4de73f20fbd761b63e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **830.1 MB (830121178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e1da45be61cdd50a06bd28b7845169b75250986f288972a8b05b50ded4a22c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:07 GMT
ADD file:e777355768c63f735e5458c7e0ada7f556f27d0493b3af35dc7c34f9c4294ea9 in / 
# Thu, 02 Dec 2021 02:48:08 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:39:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Dec 2021 03:40:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:34:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:34:20 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 02 Dec 2021 11:34:22 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 02 Dec 2021 11:34:22 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 11:34:22 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 11:34:23 GMT
ENV JAVA_VERSION=11.0.13
# Thu, 02 Dec 2021 11:34:48 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_x64_linux_11.0.13_8.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_aarch64_linux_11.0.13_8.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 02 Dec 2021 11:34:49 GMT
CMD ["jshell"]
# Fri, 03 Dec 2021 14:11:49 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Dec 2021 14:11:50 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Dec 2021 14:11:50 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 03 Dec 2021 14:11:51 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Dec 2021 14:11:51 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 14:11:51 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 14:27:34 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 03 Dec 2021 14:27:34 GMT
ENV TOMCAT_MAJOR=9
# Fri, 03 Dec 2021 14:27:34 GMT
ENV TOMCAT_VERSION=9.0.55
# Fri, 03 Dec 2021 14:27:35 GMT
ENV TOMCAT_SHA512=a0c480b8bba09069bda3b57f54e658450a59d799474ad587dead0ffbf5074c16ee3f9f9c13312d0ff3227c7034589dabf25941fbd672838e9baeee9661e024dc
# Fri, 03 Dec 2021 14:28:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 03 Dec 2021 14:28:03 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 03 Dec 2021 14:28:03 GMT
EXPOSE 8080
# Fri, 03 Dec 2021 14:28:03 GMT
CMD ["catalina.sh" "run"]
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 20:52:10 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 03 Dec 2021 20:52:11 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 03 Dec 2021 20:54:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 20:54:05 GMT
ENV XWIKI_VERSION=13.10
# Fri, 03 Dec 2021 20:54:05 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10
# Fri, 03 Dec 2021 20:54:05 GMT
ENV XWIKI_DOWNLOAD_SHA256=863455ef741ec70539ab89b9981790909f3319b626a107e62fa42c8797df032b
# Fri, 03 Dec 2021 20:54:44 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 03 Dec 2021 20:54:45 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 03 Dec 2021 20:54:46 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 03 Dec 2021 20:54:46 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 03 Dec 2021 20:54:47 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 03 Dec 2021 20:54:47 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 03 Dec 2021 20:54:47 GMT
VOLUME [/usr/local/xwiki]
# Fri, 03 Dec 2021 20:54:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Dec 2021 20:54:47 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:5e0b432e8ba9d9029a000e627840b98ffc1ed0c5172075b7d3e869be0df0fe9b`  
		Last Modified: Thu, 02 Dec 2021 02:53:18 GMT  
		Size: 54.9 MB (54932878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84cfd68b5cea612a8343c346bfa5bd6c486769010d12f7ec86b23c74887feb2`  
		Last Modified: Thu, 02 Dec 2021 03:49:22 GMT  
		Size: 5.2 MB (5153424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b8f2315954535f1e27cd13d777e73da4a787b0aebf4241d225beff3c91cbb1`  
		Last Modified: Thu, 02 Dec 2021 03:49:23 GMT  
		Size: 10.9 MB (10871995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0598fa43a7e793a76c198e8d45d8810394e1cfc943b2673d7fcf5a6fdc4f45b3`  
		Last Modified: Thu, 02 Dec 2021 03:49:46 GMT  
		Size: 54.6 MB (54567844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d35e3be804184359e0904389b149de16f159e30436d7a8a970aef67a4d155b`  
		Last Modified: Thu, 02 Dec 2021 11:54:46 GMT  
		Size: 5.4 MB (5420076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc448a0c88bee4d3cf6a928aa2b4cf499f4cb05034093c581342d414188a566`  
		Last Modified: Thu, 02 Dec 2021 11:54:45 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbdff6e5955b8bcd2e24b1a49fa4ec593ad333133c52911832aa2a7893f542da`  
		Last Modified: Thu, 02 Dec 2021 11:55:04 GMT  
		Size: 203.1 MB (203118915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5daf3771e3d8c27aa89cbcfef659790a2218e319899d49fbccde199e1780a5ef`  
		Last Modified: Fri, 03 Dec 2021 14:54:53 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5434ab540d864811e12dac3650eb0bc67bc8f6d7a6cb1f3c832e2c078c45302c`  
		Last Modified: Fri, 03 Dec 2021 15:08:17 GMT  
		Size: 12.5 MB (12523151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f43f4b2f615c39e867b3110fbc83f1d8fa2b72e4788cdcc91ea5dd73e97102`  
		Last Modified: Fri, 03 Dec 2021 15:08:16 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c96c2f945ecec7eda758824db2032432765e7a0128ef11d3c1841ac2dc2e5d95`  
		Last Modified: Fri, 03 Dec 2021 20:59:00 GMT  
		Size: 190.3 MB (190286185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:955cdd39f0085f569763841337c25acef25604257a3de6773891e0bdcadb872d`  
		Last Modified: Fri, 03 Dec 2021 20:58:51 GMT  
		Size: 292.4 MB (292388346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc39c66a904202841f30554fedfe28bc6396c82f817ed5ebefbaed3429b82dd9`  
		Last Modified: Fri, 03 Dec 2021 20:58:32 GMT  
		Size: 846.2 KB (846214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e85be07558e39d22dc2b4a004d91020698ea370e5fb7cf4c99b2a31d3749f6e7`  
		Last Modified: Fri, 03 Dec 2021 20:58:31 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8586fc44e80ce8805adcde54de3c1551ca1c8f7f7e73e7b2d2cd66c38f935be`  
		Last Modified: Fri, 03 Dec 2021 20:58:31 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb2fe06d239087be98bf79090e52955d9ec293fbff5f6db1ff93dd7fee9e488`  
		Last Modified: Fri, 03 Dec 2021 20:58:31 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff38395ff2cff70633d42e627db200f34e988de4c7de698114b9c085bd6c201e`  
		Last Modified: Fri, 03 Dec 2021 20:58:31 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:stable-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:9791c7dc4989df351c585fcb8eb26596e4a50fdf07313003f37c81bd58d2f84f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **820.8 MB (820758295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a04e1e74e2fd570283613fa3d4d622b67d64a5b21bd3df1e905b07839c312c74`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 02 Dec 2021 08:07:54 GMT
ADD file:998dc1c35eeeed1ddf46156aeb337fb9b8cbb4855caf994201167a1061f4ecbf in / 
# Thu, 02 Dec 2021 08:07:55 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 09:53:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 09:53:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Dec 2021 09:53:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:07:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:07:23 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 02 Dec 2021 11:07:24 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 02 Dec 2021 11:07:25 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 11:07:26 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 11:07:27 GMT
ENV JAVA_VERSION=11.0.13
# Thu, 02 Dec 2021 11:07:49 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_x64_linux_11.0.13_8.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_aarch64_linux_11.0.13_8.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 02 Dec 2021 11:07:50 GMT
CMD ["jshell"]
# Fri, 03 Dec 2021 10:33:28 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Dec 2021 10:33:28 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Dec 2021 10:33:30 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 03 Dec 2021 10:33:30 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Dec 2021 10:33:31 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 10:33:32 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Dec 2021 10:54:19 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 03 Dec 2021 10:54:20 GMT
ENV TOMCAT_MAJOR=9
# Fri, 03 Dec 2021 10:54:21 GMT
ENV TOMCAT_VERSION=9.0.55
# Fri, 03 Dec 2021 10:54:22 GMT
ENV TOMCAT_SHA512=a0c480b8bba09069bda3b57f54e658450a59d799474ad587dead0ffbf5074c16ee3f9f9c13312d0ff3227c7034589dabf25941fbd672838e9baeee9661e024dc
# Fri, 03 Dec 2021 10:54:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 03 Dec 2021 10:54:45 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 03 Dec 2021 10:54:45 GMT
EXPOSE 8080
# Fri, 03 Dec 2021 10:54:46 GMT
CMD ["catalina.sh" "run"]
# Fri, 03 Dec 2021 16:34:04 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 03 Dec 2021 16:34:05 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 16:34:05 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 03 Dec 2021 16:34:06 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 03 Dec 2021 16:34:07 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 03 Dec 2021 16:34:08 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 03 Dec 2021 16:34:43 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 20:40:41 GMT
ENV XWIKI_VERSION=13.10
# Fri, 03 Dec 2021 20:40:42 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10
# Fri, 03 Dec 2021 20:40:43 GMT
ENV XWIKI_DOWNLOAD_SHA256=863455ef741ec70539ab89b9981790909f3319b626a107e62fa42c8797df032b
# Fri, 03 Dec 2021 20:42:05 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 03 Dec 2021 20:42:07 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 03 Dec 2021 20:42:08 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 03 Dec 2021 20:42:09 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 03 Dec 2021 20:42:10 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 03 Dec 2021 20:42:11 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 03 Dec 2021 20:42:12 GMT
VOLUME [/usr/local/xwiki]
# Fri, 03 Dec 2021 20:42:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Dec 2021 20:42:14 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:6476cb406b24c94f24348db05d154b814b14ee38860dea1625080e7e08295a80`  
		Last Modified: Thu, 02 Dec 2021 08:40:14 GMT  
		Size: 53.6 MB (53619027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96565d527970b1cc982493f96d6b317b1fbfdd7bf0ea6fd58d44942bb4f597c5`  
		Last Modified: Thu, 02 Dec 2021 10:02:24 GMT  
		Size: 4.9 MB (4937631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8c15f93136056df893ba8088992a38e90dc37210fd6ebb712413fd045c58de`  
		Last Modified: Thu, 02 Dec 2021 10:02:25 GMT  
		Size: 10.7 MB (10655914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee42e24e52cb2f9b50ab14328865298f5ae6ac159219db890afc6366ec641a46`  
		Last Modified: Thu, 02 Dec 2021 10:02:46 GMT  
		Size: 54.7 MB (54669690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1ddc61edfde0dfa7da5e868dfebc0df6e44b7c94700ae79892d861abc32f97`  
		Last Modified: Thu, 02 Dec 2021 11:31:06 GMT  
		Size: 5.4 MB (5420180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:804b3e7e3a2930efff5c50600a2c162b8f2af073ec54a3c44314cc36e68d1a75`  
		Last Modified: Thu, 02 Dec 2021 11:31:05 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c15c25e9529bccafc0b750eb33fb972a05d42a09303dc760b67f89ea21b0bce0`  
		Last Modified: Thu, 02 Dec 2021 11:31:26 GMT  
		Size: 200.7 MB (200712890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac1b17d7ee052527ef86a2354f093548ac170d6d3318a79fa9916fd616c2c40f`  
		Last Modified: Fri, 03 Dec 2021 11:33:43 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8926fc06c65e9a17e2a3110e422fbebb73f63463202846b0b6addc004fd06d`  
		Last Modified: Fri, 03 Dec 2021 11:49:18 GMT  
		Size: 12.3 MB (12292070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56905cdb16153e42e333c2819b26aec2f74860d5924cbe3cf1952f737953c4d`  
		Last Modified: Fri, 03 Dec 2021 16:37:29 GMT  
		Size: 185.2 MB (185204101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb1a3f2a620897e3ef5f866de2723c108b289d8308a9c3fea23ed2d98413c95`  
		Last Modified: Fri, 03 Dec 2021 20:43:19 GMT  
		Size: 292.4 MB (292388612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19092ac47724d18b94e705918c5687646e63dc774df241652ec6c77177eb0ad`  
		Last Modified: Fri, 03 Dec 2021 20:42:56 GMT  
		Size: 846.2 KB (846209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8959324a980da8d5711d1b493e27fea4054370769e11fe27b0341d928e7cad7b`  
		Last Modified: Fri, 03 Dec 2021 20:42:56 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3315518eeae081a901de36d667f5894a3bd974fdaa2943e8f6eff269b353b34d`  
		Last Modified: Fri, 03 Dec 2021 20:42:56 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b25a16e439c94dc4b0d402bdc659b525b4bc914799cb79e15e289e26f5eabdd7`  
		Last Modified: Fri, 03 Dec 2021 20:42:56 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0747fe5f75ab79fb9a9f111b719dec4f788fe07fcecc62412907b32ff5e2e9c`  
		Last Modified: Fri, 03 Dec 2021 20:42:56 GMT  
		Size: 2.5 KB (2500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
