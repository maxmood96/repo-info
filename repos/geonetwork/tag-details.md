<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `geonetwork`

-	[`geonetwork:3`](#geonetwork3)
-	[`geonetwork:3.10`](#geonetwork310)
-	[`geonetwork:3.10.5`](#geonetwork3105)
-	[`geonetwork:3.10.5-postgres`](#geonetwork3105-postgres)
-	[`geonetwork:3.10-postgres`](#geonetwork310-postgres)
-	[`geonetwork:3.8`](#geonetwork38)
-	[`geonetwork:3.8.3`](#geonetwork383)
-	[`geonetwork:3.8.3-postgres`](#geonetwork383-postgres)
-	[`geonetwork:3.8-postgres`](#geonetwork38-postgres)
-	[`geonetwork:3-postgres`](#geonetwork3-postgres)
-	[`geonetwork:4`](#geonetwork4)
-	[`geonetwork:4.0`](#geonetwork40)
-	[`geonetwork:4.0.1`](#geonetwork401)
-	[`geonetwork:latest`](#geonetworklatest)
-	[`geonetwork:postgres`](#geonetworkpostgres)

## `geonetwork:3`

```console
$ docker pull geonetwork@sha256:098ee2562a602e183593356186aaab3e2a65aa036b861d7a0af97b4e47d58ef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `geonetwork:3` - linux; amd64

```console
$ docker pull geonetwork@sha256:ddc1aac1b012c4070fadb10459d8b2fa191ddf1727184d77e988a745f7f69031
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **519.0 MB (519001392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b66a1d14df62e48874015a4c511892d6a7737f117702691d781c1160bcc18c73`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 17 Nov 2020 20:20:58 GMT
ADD file:9a4fd72d749f4a791e75e0f6fc6028d0771e3381b6d84a8d0b07a4887bc7c641 in / 
# Tue, 17 Nov 2020 20:20:58 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 00:30:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 00:30:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Nov 2020 00:31:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 19 Nov 2020 03:06:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 19 Nov 2020 03:06:07 GMT
ENV LANG=C.UTF-8
# Thu, 19 Nov 2020 03:07:06 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 19 Nov 2020 03:07:06 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Nov 2020 03:07:08 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 19 Nov 2020 03:07:08 GMT
ENV JAVA_VERSION=8u275
# Thu, 19 Nov 2020 03:07:19 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u275-b01/OpenJDK8U-jdk_x64_linux_8u275b01.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 19 Nov 2020 06:13:16 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 19 Nov 2020 06:13:16 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Nov 2020 06:13:17 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 19 Nov 2020 06:13:18 GMT
WORKDIR /usr/local/tomcat
# Thu, 19 Nov 2020 06:13:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 19 Nov 2020 06:13:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 19 Nov 2020 06:21:01 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 19 Nov 2020 06:21:01 GMT
ENV TOMCAT_MAJOR=8
# Thu, 19 Nov 2020 06:21:02 GMT
ENV TOMCAT_VERSION=8.5.60
# Thu, 19 Nov 2020 06:21:02 GMT
ENV TOMCAT_SHA512=460b4d0f2d445670b69ff97d4295628b9ce444c294e301b4c0c5e4c48b42bb1a642769f075dfe105b7d7257d9aba62b75a6ea5b6fb65487891ab23d7bb3d6140
# Thu, 19 Nov 2020 06:21:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 19 Nov 2020 06:21:33 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 19 Nov 2020 06:21:33 GMT
EXPOSE 8080
# Thu, 19 Nov 2020 06:21:34 GMT
CMD ["catalina.sh" "run"]
# Thu, 19 Nov 2020 09:05:08 GMT
ENV GN_FILE=geonetwork.war
# Thu, 19 Nov 2020 09:05:08 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Thu, 19 Nov 2020 09:05:09 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Thu, 19 Nov 2020 09:05:09 GMT
ENV GN_VERSION=3.10.5
# Thu, 19 Nov 2020 09:05:09 GMT
ENV GN_DOWNLOAD_MD5=63ffc3929e486e48c56b89b62da72813
# Thu, 19 Nov 2020 09:05:09 GMT
WORKDIR /usr/local/tomcat/webapps
# Thu, 19 Nov 2020 09:11:44 GMT
RUN curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "$GN_DOWNLOAD_MD5 *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE
# Thu, 19 Nov 2020 09:11:44 GMT
COPY file:0804862fd42c05f06dfa65cb1e5dad9a956d8ac6a3ddd4d962847ba159f5cfe6 in /entrypoint.sh 
# Thu, 19 Nov 2020 09:11:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 19 Nov 2020 09:11:44 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:756975cb9c7e7933d824af9319b512dd72a50894232761d06ef3be59981df838`  
		Last Modified: Tue, 17 Nov 2020 20:27:06 GMT  
		Size: 50.4 MB (50397725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77915b4e630d47296770ce4cf481894885978072432456615172af463433cc5`  
		Last Modified: Wed, 18 Nov 2020 00:49:42 GMT  
		Size: 7.8 MB (7811717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f37a0a41b6b03489dd7de0aa2a79e369fd8b219bbc36b52f3f9790dc128e74b`  
		Last Modified: Wed, 18 Nov 2020 00:49:42 GMT  
		Size: 10.0 MB (9996233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96b2c1e36db5f5910f58da2ca4f9311b0690810c7107fb055ee1541498b5061f`  
		Last Modified: Wed, 18 Nov 2020 00:50:25 GMT  
		Size: 51.8 MB (51829318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a2d52b526e253b306ae38d6b75645b6a1716888a0b5e4b85b4dd93df8843a6`  
		Last Modified: Thu, 19 Nov 2020 03:11:37 GMT  
		Size: 5.3 MB (5284715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a36defce609c2ec5a9cc77094704955c777946a68d0f517f2d2d8223dd6420`  
		Last Modified: Thu, 19 Nov 2020 03:12:33 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e2014d79b302bdc5c3c30f767dddf39b02d21608607deb53450c893636731c1`  
		Last Modified: Thu, 19 Nov 2020 03:12:44 GMT  
		Size: 105.9 MB (105883500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528f69e563774f04c70bd19d8d09d1f758bf238b9c163dbd6ad5f2082ce0f194`  
		Last Modified: Thu, 19 Nov 2020 06:25:29 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37b94cea6fdec640e12b21ce5b846e8c7591c1bbd3f73538221374767362460`  
		Last Modified: Thu, 19 Nov 2020 06:27:39 GMT  
		Size: 11.5 MB (11500367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f96b01204efdb3b57520912607f112501248b5be77fd986c6d397f367e290d66`  
		Last Modified: Thu, 19 Nov 2020 06:27:37 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc9ae91a589697b43d9db64c38773ffd09a978edf568ac3c744a793ec93490cb`  
		Last Modified: Thu, 19 Nov 2020 09:25:48 GMT  
		Size: 276.3 MB (276297086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:375e55e6c143afbab56977401d0c13f62c15fcf1d0c5b54bf141acef29bc3c94`  
		Last Modified: Thu, 19 Nov 2020 09:25:28 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `geonetwork:3.10`

```console
$ docker pull geonetwork@sha256:098ee2562a602e183593356186aaab3e2a65aa036b861d7a0af97b4e47d58ef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `geonetwork:3.10` - linux; amd64

```console
$ docker pull geonetwork@sha256:ddc1aac1b012c4070fadb10459d8b2fa191ddf1727184d77e988a745f7f69031
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **519.0 MB (519001392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b66a1d14df62e48874015a4c511892d6a7737f117702691d781c1160bcc18c73`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 17 Nov 2020 20:20:58 GMT
ADD file:9a4fd72d749f4a791e75e0f6fc6028d0771e3381b6d84a8d0b07a4887bc7c641 in / 
# Tue, 17 Nov 2020 20:20:58 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 00:30:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 00:30:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Nov 2020 00:31:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 19 Nov 2020 03:06:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 19 Nov 2020 03:06:07 GMT
ENV LANG=C.UTF-8
# Thu, 19 Nov 2020 03:07:06 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 19 Nov 2020 03:07:06 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Nov 2020 03:07:08 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 19 Nov 2020 03:07:08 GMT
ENV JAVA_VERSION=8u275
# Thu, 19 Nov 2020 03:07:19 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u275-b01/OpenJDK8U-jdk_x64_linux_8u275b01.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 19 Nov 2020 06:13:16 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 19 Nov 2020 06:13:16 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Nov 2020 06:13:17 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 19 Nov 2020 06:13:18 GMT
WORKDIR /usr/local/tomcat
# Thu, 19 Nov 2020 06:13:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 19 Nov 2020 06:13:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 19 Nov 2020 06:21:01 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 19 Nov 2020 06:21:01 GMT
ENV TOMCAT_MAJOR=8
# Thu, 19 Nov 2020 06:21:02 GMT
ENV TOMCAT_VERSION=8.5.60
# Thu, 19 Nov 2020 06:21:02 GMT
ENV TOMCAT_SHA512=460b4d0f2d445670b69ff97d4295628b9ce444c294e301b4c0c5e4c48b42bb1a642769f075dfe105b7d7257d9aba62b75a6ea5b6fb65487891ab23d7bb3d6140
# Thu, 19 Nov 2020 06:21:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 19 Nov 2020 06:21:33 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 19 Nov 2020 06:21:33 GMT
EXPOSE 8080
# Thu, 19 Nov 2020 06:21:34 GMT
CMD ["catalina.sh" "run"]
# Thu, 19 Nov 2020 09:05:08 GMT
ENV GN_FILE=geonetwork.war
# Thu, 19 Nov 2020 09:05:08 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Thu, 19 Nov 2020 09:05:09 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Thu, 19 Nov 2020 09:05:09 GMT
ENV GN_VERSION=3.10.5
# Thu, 19 Nov 2020 09:05:09 GMT
ENV GN_DOWNLOAD_MD5=63ffc3929e486e48c56b89b62da72813
# Thu, 19 Nov 2020 09:05:09 GMT
WORKDIR /usr/local/tomcat/webapps
# Thu, 19 Nov 2020 09:11:44 GMT
RUN curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "$GN_DOWNLOAD_MD5 *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE
# Thu, 19 Nov 2020 09:11:44 GMT
COPY file:0804862fd42c05f06dfa65cb1e5dad9a956d8ac6a3ddd4d962847ba159f5cfe6 in /entrypoint.sh 
# Thu, 19 Nov 2020 09:11:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 19 Nov 2020 09:11:44 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:756975cb9c7e7933d824af9319b512dd72a50894232761d06ef3be59981df838`  
		Last Modified: Tue, 17 Nov 2020 20:27:06 GMT  
		Size: 50.4 MB (50397725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77915b4e630d47296770ce4cf481894885978072432456615172af463433cc5`  
		Last Modified: Wed, 18 Nov 2020 00:49:42 GMT  
		Size: 7.8 MB (7811717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f37a0a41b6b03489dd7de0aa2a79e369fd8b219bbc36b52f3f9790dc128e74b`  
		Last Modified: Wed, 18 Nov 2020 00:49:42 GMT  
		Size: 10.0 MB (9996233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96b2c1e36db5f5910f58da2ca4f9311b0690810c7107fb055ee1541498b5061f`  
		Last Modified: Wed, 18 Nov 2020 00:50:25 GMT  
		Size: 51.8 MB (51829318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a2d52b526e253b306ae38d6b75645b6a1716888a0b5e4b85b4dd93df8843a6`  
		Last Modified: Thu, 19 Nov 2020 03:11:37 GMT  
		Size: 5.3 MB (5284715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a36defce609c2ec5a9cc77094704955c777946a68d0f517f2d2d8223dd6420`  
		Last Modified: Thu, 19 Nov 2020 03:12:33 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e2014d79b302bdc5c3c30f767dddf39b02d21608607deb53450c893636731c1`  
		Last Modified: Thu, 19 Nov 2020 03:12:44 GMT  
		Size: 105.9 MB (105883500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528f69e563774f04c70bd19d8d09d1f758bf238b9c163dbd6ad5f2082ce0f194`  
		Last Modified: Thu, 19 Nov 2020 06:25:29 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37b94cea6fdec640e12b21ce5b846e8c7591c1bbd3f73538221374767362460`  
		Last Modified: Thu, 19 Nov 2020 06:27:39 GMT  
		Size: 11.5 MB (11500367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f96b01204efdb3b57520912607f112501248b5be77fd986c6d397f367e290d66`  
		Last Modified: Thu, 19 Nov 2020 06:27:37 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc9ae91a589697b43d9db64c38773ffd09a978edf568ac3c744a793ec93490cb`  
		Last Modified: Thu, 19 Nov 2020 09:25:48 GMT  
		Size: 276.3 MB (276297086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:375e55e6c143afbab56977401d0c13f62c15fcf1d0c5b54bf141acef29bc3c94`  
		Last Modified: Thu, 19 Nov 2020 09:25:28 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `geonetwork:3.10.5`

```console
$ docker pull geonetwork@sha256:098ee2562a602e183593356186aaab3e2a65aa036b861d7a0af97b4e47d58ef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `geonetwork:3.10.5` - linux; amd64

```console
$ docker pull geonetwork@sha256:ddc1aac1b012c4070fadb10459d8b2fa191ddf1727184d77e988a745f7f69031
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **519.0 MB (519001392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b66a1d14df62e48874015a4c511892d6a7737f117702691d781c1160bcc18c73`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 17 Nov 2020 20:20:58 GMT
ADD file:9a4fd72d749f4a791e75e0f6fc6028d0771e3381b6d84a8d0b07a4887bc7c641 in / 
# Tue, 17 Nov 2020 20:20:58 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 00:30:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 00:30:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Nov 2020 00:31:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 19 Nov 2020 03:06:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 19 Nov 2020 03:06:07 GMT
ENV LANG=C.UTF-8
# Thu, 19 Nov 2020 03:07:06 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 19 Nov 2020 03:07:06 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Nov 2020 03:07:08 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 19 Nov 2020 03:07:08 GMT
ENV JAVA_VERSION=8u275
# Thu, 19 Nov 2020 03:07:19 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u275-b01/OpenJDK8U-jdk_x64_linux_8u275b01.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 19 Nov 2020 06:13:16 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 19 Nov 2020 06:13:16 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Nov 2020 06:13:17 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 19 Nov 2020 06:13:18 GMT
WORKDIR /usr/local/tomcat
# Thu, 19 Nov 2020 06:13:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 19 Nov 2020 06:13:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 19 Nov 2020 06:21:01 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 19 Nov 2020 06:21:01 GMT
ENV TOMCAT_MAJOR=8
# Thu, 19 Nov 2020 06:21:02 GMT
ENV TOMCAT_VERSION=8.5.60
# Thu, 19 Nov 2020 06:21:02 GMT
ENV TOMCAT_SHA512=460b4d0f2d445670b69ff97d4295628b9ce444c294e301b4c0c5e4c48b42bb1a642769f075dfe105b7d7257d9aba62b75a6ea5b6fb65487891ab23d7bb3d6140
# Thu, 19 Nov 2020 06:21:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 19 Nov 2020 06:21:33 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 19 Nov 2020 06:21:33 GMT
EXPOSE 8080
# Thu, 19 Nov 2020 06:21:34 GMT
CMD ["catalina.sh" "run"]
# Thu, 19 Nov 2020 09:05:08 GMT
ENV GN_FILE=geonetwork.war
# Thu, 19 Nov 2020 09:05:08 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Thu, 19 Nov 2020 09:05:09 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Thu, 19 Nov 2020 09:05:09 GMT
ENV GN_VERSION=3.10.5
# Thu, 19 Nov 2020 09:05:09 GMT
ENV GN_DOWNLOAD_MD5=63ffc3929e486e48c56b89b62da72813
# Thu, 19 Nov 2020 09:05:09 GMT
WORKDIR /usr/local/tomcat/webapps
# Thu, 19 Nov 2020 09:11:44 GMT
RUN curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "$GN_DOWNLOAD_MD5 *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE
# Thu, 19 Nov 2020 09:11:44 GMT
COPY file:0804862fd42c05f06dfa65cb1e5dad9a956d8ac6a3ddd4d962847ba159f5cfe6 in /entrypoint.sh 
# Thu, 19 Nov 2020 09:11:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 19 Nov 2020 09:11:44 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:756975cb9c7e7933d824af9319b512dd72a50894232761d06ef3be59981df838`  
		Last Modified: Tue, 17 Nov 2020 20:27:06 GMT  
		Size: 50.4 MB (50397725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77915b4e630d47296770ce4cf481894885978072432456615172af463433cc5`  
		Last Modified: Wed, 18 Nov 2020 00:49:42 GMT  
		Size: 7.8 MB (7811717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f37a0a41b6b03489dd7de0aa2a79e369fd8b219bbc36b52f3f9790dc128e74b`  
		Last Modified: Wed, 18 Nov 2020 00:49:42 GMT  
		Size: 10.0 MB (9996233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96b2c1e36db5f5910f58da2ca4f9311b0690810c7107fb055ee1541498b5061f`  
		Last Modified: Wed, 18 Nov 2020 00:50:25 GMT  
		Size: 51.8 MB (51829318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a2d52b526e253b306ae38d6b75645b6a1716888a0b5e4b85b4dd93df8843a6`  
		Last Modified: Thu, 19 Nov 2020 03:11:37 GMT  
		Size: 5.3 MB (5284715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a36defce609c2ec5a9cc77094704955c777946a68d0f517f2d2d8223dd6420`  
		Last Modified: Thu, 19 Nov 2020 03:12:33 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e2014d79b302bdc5c3c30f767dddf39b02d21608607deb53450c893636731c1`  
		Last Modified: Thu, 19 Nov 2020 03:12:44 GMT  
		Size: 105.9 MB (105883500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528f69e563774f04c70bd19d8d09d1f758bf238b9c163dbd6ad5f2082ce0f194`  
		Last Modified: Thu, 19 Nov 2020 06:25:29 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37b94cea6fdec640e12b21ce5b846e8c7591c1bbd3f73538221374767362460`  
		Last Modified: Thu, 19 Nov 2020 06:27:39 GMT  
		Size: 11.5 MB (11500367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f96b01204efdb3b57520912607f112501248b5be77fd986c6d397f367e290d66`  
		Last Modified: Thu, 19 Nov 2020 06:27:37 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc9ae91a589697b43d9db64c38773ffd09a978edf568ac3c744a793ec93490cb`  
		Last Modified: Thu, 19 Nov 2020 09:25:48 GMT  
		Size: 276.3 MB (276297086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:375e55e6c143afbab56977401d0c13f62c15fcf1d0c5b54bf141acef29bc3c94`  
		Last Modified: Thu, 19 Nov 2020 09:25:28 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `geonetwork:3.10.5-postgres`

```console
$ docker pull geonetwork@sha256:a370092791facbc5e807f4b7b3b59996741cdce5b3a43f0d80c6fb9bf434399a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `geonetwork:3.10.5-postgres` - linux; amd64

```console
$ docker pull geonetwork@sha256:197f62a106d8cf980ccade87705c14e75ca756e51a82d40268b3f8d14bab27de
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.8 MB (530813056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8082cf9604ffc803448d1271c9277b539523e0b381fc42db9a9e91fb5b22c35b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 17 Nov 2020 20:20:58 GMT
ADD file:9a4fd72d749f4a791e75e0f6fc6028d0771e3381b6d84a8d0b07a4887bc7c641 in / 
# Tue, 17 Nov 2020 20:20:58 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 00:30:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 00:30:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Nov 2020 00:31:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 19 Nov 2020 03:06:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 19 Nov 2020 03:06:07 GMT
ENV LANG=C.UTF-8
# Thu, 19 Nov 2020 03:07:06 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 19 Nov 2020 03:07:06 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Nov 2020 03:07:08 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 19 Nov 2020 03:07:08 GMT
ENV JAVA_VERSION=8u275
# Thu, 19 Nov 2020 03:07:19 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u275-b01/OpenJDK8U-jdk_x64_linux_8u275b01.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 19 Nov 2020 06:13:16 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 19 Nov 2020 06:13:16 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Nov 2020 06:13:17 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 19 Nov 2020 06:13:18 GMT
WORKDIR /usr/local/tomcat
# Thu, 19 Nov 2020 06:13:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 19 Nov 2020 06:13:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 19 Nov 2020 06:21:01 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 19 Nov 2020 06:21:01 GMT
ENV TOMCAT_MAJOR=8
# Thu, 19 Nov 2020 06:21:02 GMT
ENV TOMCAT_VERSION=8.5.60
# Thu, 19 Nov 2020 06:21:02 GMT
ENV TOMCAT_SHA512=460b4d0f2d445670b69ff97d4295628b9ce444c294e301b4c0c5e4c48b42bb1a642769f075dfe105b7d7257d9aba62b75a6ea5b6fb65487891ab23d7bb3d6140
# Thu, 19 Nov 2020 06:21:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 19 Nov 2020 06:21:33 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 19 Nov 2020 06:21:33 GMT
EXPOSE 8080
# Thu, 19 Nov 2020 06:21:34 GMT
CMD ["catalina.sh" "run"]
# Thu, 19 Nov 2020 09:05:08 GMT
ENV GN_FILE=geonetwork.war
# Thu, 19 Nov 2020 09:05:08 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Thu, 19 Nov 2020 09:05:09 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Thu, 19 Nov 2020 09:05:09 GMT
ENV GN_VERSION=3.10.5
# Thu, 19 Nov 2020 09:05:09 GMT
ENV GN_DOWNLOAD_MD5=63ffc3929e486e48c56b89b62da72813
# Thu, 19 Nov 2020 09:05:09 GMT
WORKDIR /usr/local/tomcat/webapps
# Thu, 19 Nov 2020 09:11:44 GMT
RUN curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "$GN_DOWNLOAD_MD5 *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE
# Thu, 19 Nov 2020 09:11:44 GMT
COPY file:0804862fd42c05f06dfa65cb1e5dad9a956d8ac6a3ddd4d962847ba159f5cfe6 in /entrypoint.sh 
# Thu, 19 Nov 2020 09:11:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 19 Nov 2020 09:11:44 GMT
CMD ["catalina.sh" "run"]
# Thu, 19 Nov 2020 09:12:10 GMT
RUN apt-get update && apt-get install -y postgresql-client &&     rm -rf /var/lib/apt/lists/*
# Thu, 19 Nov 2020 09:12:11 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' $CATALINA_HOME/webapps/geonetwork/WEB-INF/config-node/srv.xml && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' $CATALINA_HOME/webapps/geonetwork/WEB-INF/config-node/srv.xml
# Thu, 19 Nov 2020 09:12:12 GMT
COPY file:83f69d2041e5fb378033b0db57e096c81ba0725102ab4da4f089685e748fcce3 in /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties 
# Thu, 19 Nov 2020 09:12:12 GMT
COPY file:c88411abba7ad9b7bb75019f08755dbfa163d2fc7fdd80676bf9350c4c56a19c in /entrypoint.sh 
# Thu, 19 Nov 2020 09:12:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 19 Nov 2020 09:12:12 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:756975cb9c7e7933d824af9319b512dd72a50894232761d06ef3be59981df838`  
		Last Modified: Tue, 17 Nov 2020 20:27:06 GMT  
		Size: 50.4 MB (50397725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77915b4e630d47296770ce4cf481894885978072432456615172af463433cc5`  
		Last Modified: Wed, 18 Nov 2020 00:49:42 GMT  
		Size: 7.8 MB (7811717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f37a0a41b6b03489dd7de0aa2a79e369fd8b219bbc36b52f3f9790dc128e74b`  
		Last Modified: Wed, 18 Nov 2020 00:49:42 GMT  
		Size: 10.0 MB (9996233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96b2c1e36db5f5910f58da2ca4f9311b0690810c7107fb055ee1541498b5061f`  
		Last Modified: Wed, 18 Nov 2020 00:50:25 GMT  
		Size: 51.8 MB (51829318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a2d52b526e253b306ae38d6b75645b6a1716888a0b5e4b85b4dd93df8843a6`  
		Last Modified: Thu, 19 Nov 2020 03:11:37 GMT  
		Size: 5.3 MB (5284715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a36defce609c2ec5a9cc77094704955c777946a68d0f517f2d2d8223dd6420`  
		Last Modified: Thu, 19 Nov 2020 03:12:33 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e2014d79b302bdc5c3c30f767dddf39b02d21608607deb53450c893636731c1`  
		Last Modified: Thu, 19 Nov 2020 03:12:44 GMT  
		Size: 105.9 MB (105883500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528f69e563774f04c70bd19d8d09d1f758bf238b9c163dbd6ad5f2082ce0f194`  
		Last Modified: Thu, 19 Nov 2020 06:25:29 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37b94cea6fdec640e12b21ce5b846e8c7591c1bbd3f73538221374767362460`  
		Last Modified: Thu, 19 Nov 2020 06:27:39 GMT  
		Size: 11.5 MB (11500367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f96b01204efdb3b57520912607f112501248b5be77fd986c6d397f367e290d66`  
		Last Modified: Thu, 19 Nov 2020 06:27:37 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc9ae91a589697b43d9db64c38773ffd09a978edf568ac3c744a793ec93490cb`  
		Last Modified: Thu, 19 Nov 2020 09:25:48 GMT  
		Size: 276.3 MB (276297086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:375e55e6c143afbab56977401d0c13f62c15fcf1d0c5b54bf141acef29bc3c94`  
		Last Modified: Thu, 19 Nov 2020 09:25:28 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de5f684135aed6842f15dc83ee246860033044ea0767a78718ef7283e8336669`  
		Last Modified: Thu, 19 Nov 2020 09:25:57 GMT  
		Size: 11.8 MB (11808303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bef6ec9d292f414f2e057c6a55cacd28f22d8b1b9ef170b9a49db40a2950e7b`  
		Last Modified: Thu, 19 Nov 2020 09:25:55 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31da2fecd2e76420600c49f08974869b84e1fd3e99a0138aa6bd7298d3d4d633`  
		Last Modified: Thu, 19 Nov 2020 09:25:55 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfad719ddee04927017bfa4fee2356d9aaa7683efc57708638a2e3c4df3b90a5`  
		Last Modified: Thu, 19 Nov 2020 09:25:55 GMT  
		Size: 974.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `geonetwork:3.10-postgres`

```console
$ docker pull geonetwork@sha256:a370092791facbc5e807f4b7b3b59996741cdce5b3a43f0d80c6fb9bf434399a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `geonetwork:3.10-postgres` - linux; amd64

```console
$ docker pull geonetwork@sha256:197f62a106d8cf980ccade87705c14e75ca756e51a82d40268b3f8d14bab27de
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.8 MB (530813056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8082cf9604ffc803448d1271c9277b539523e0b381fc42db9a9e91fb5b22c35b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 17 Nov 2020 20:20:58 GMT
ADD file:9a4fd72d749f4a791e75e0f6fc6028d0771e3381b6d84a8d0b07a4887bc7c641 in / 
# Tue, 17 Nov 2020 20:20:58 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 00:30:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 00:30:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Nov 2020 00:31:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 19 Nov 2020 03:06:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 19 Nov 2020 03:06:07 GMT
ENV LANG=C.UTF-8
# Thu, 19 Nov 2020 03:07:06 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 19 Nov 2020 03:07:06 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Nov 2020 03:07:08 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 19 Nov 2020 03:07:08 GMT
ENV JAVA_VERSION=8u275
# Thu, 19 Nov 2020 03:07:19 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u275-b01/OpenJDK8U-jdk_x64_linux_8u275b01.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 19 Nov 2020 06:13:16 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 19 Nov 2020 06:13:16 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Nov 2020 06:13:17 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 19 Nov 2020 06:13:18 GMT
WORKDIR /usr/local/tomcat
# Thu, 19 Nov 2020 06:13:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 19 Nov 2020 06:13:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 19 Nov 2020 06:21:01 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 19 Nov 2020 06:21:01 GMT
ENV TOMCAT_MAJOR=8
# Thu, 19 Nov 2020 06:21:02 GMT
ENV TOMCAT_VERSION=8.5.60
# Thu, 19 Nov 2020 06:21:02 GMT
ENV TOMCAT_SHA512=460b4d0f2d445670b69ff97d4295628b9ce444c294e301b4c0c5e4c48b42bb1a642769f075dfe105b7d7257d9aba62b75a6ea5b6fb65487891ab23d7bb3d6140
# Thu, 19 Nov 2020 06:21:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 19 Nov 2020 06:21:33 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 19 Nov 2020 06:21:33 GMT
EXPOSE 8080
# Thu, 19 Nov 2020 06:21:34 GMT
CMD ["catalina.sh" "run"]
# Thu, 19 Nov 2020 09:05:08 GMT
ENV GN_FILE=geonetwork.war
# Thu, 19 Nov 2020 09:05:08 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Thu, 19 Nov 2020 09:05:09 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Thu, 19 Nov 2020 09:05:09 GMT
ENV GN_VERSION=3.10.5
# Thu, 19 Nov 2020 09:05:09 GMT
ENV GN_DOWNLOAD_MD5=63ffc3929e486e48c56b89b62da72813
# Thu, 19 Nov 2020 09:05:09 GMT
WORKDIR /usr/local/tomcat/webapps
# Thu, 19 Nov 2020 09:11:44 GMT
RUN curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "$GN_DOWNLOAD_MD5 *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE
# Thu, 19 Nov 2020 09:11:44 GMT
COPY file:0804862fd42c05f06dfa65cb1e5dad9a956d8ac6a3ddd4d962847ba159f5cfe6 in /entrypoint.sh 
# Thu, 19 Nov 2020 09:11:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 19 Nov 2020 09:11:44 GMT
CMD ["catalina.sh" "run"]
# Thu, 19 Nov 2020 09:12:10 GMT
RUN apt-get update && apt-get install -y postgresql-client &&     rm -rf /var/lib/apt/lists/*
# Thu, 19 Nov 2020 09:12:11 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' $CATALINA_HOME/webapps/geonetwork/WEB-INF/config-node/srv.xml && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' $CATALINA_HOME/webapps/geonetwork/WEB-INF/config-node/srv.xml
# Thu, 19 Nov 2020 09:12:12 GMT
COPY file:83f69d2041e5fb378033b0db57e096c81ba0725102ab4da4f089685e748fcce3 in /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties 
# Thu, 19 Nov 2020 09:12:12 GMT
COPY file:c88411abba7ad9b7bb75019f08755dbfa163d2fc7fdd80676bf9350c4c56a19c in /entrypoint.sh 
# Thu, 19 Nov 2020 09:12:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 19 Nov 2020 09:12:12 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:756975cb9c7e7933d824af9319b512dd72a50894232761d06ef3be59981df838`  
		Last Modified: Tue, 17 Nov 2020 20:27:06 GMT  
		Size: 50.4 MB (50397725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77915b4e630d47296770ce4cf481894885978072432456615172af463433cc5`  
		Last Modified: Wed, 18 Nov 2020 00:49:42 GMT  
		Size: 7.8 MB (7811717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f37a0a41b6b03489dd7de0aa2a79e369fd8b219bbc36b52f3f9790dc128e74b`  
		Last Modified: Wed, 18 Nov 2020 00:49:42 GMT  
		Size: 10.0 MB (9996233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96b2c1e36db5f5910f58da2ca4f9311b0690810c7107fb055ee1541498b5061f`  
		Last Modified: Wed, 18 Nov 2020 00:50:25 GMT  
		Size: 51.8 MB (51829318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a2d52b526e253b306ae38d6b75645b6a1716888a0b5e4b85b4dd93df8843a6`  
		Last Modified: Thu, 19 Nov 2020 03:11:37 GMT  
		Size: 5.3 MB (5284715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a36defce609c2ec5a9cc77094704955c777946a68d0f517f2d2d8223dd6420`  
		Last Modified: Thu, 19 Nov 2020 03:12:33 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e2014d79b302bdc5c3c30f767dddf39b02d21608607deb53450c893636731c1`  
		Last Modified: Thu, 19 Nov 2020 03:12:44 GMT  
		Size: 105.9 MB (105883500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528f69e563774f04c70bd19d8d09d1f758bf238b9c163dbd6ad5f2082ce0f194`  
		Last Modified: Thu, 19 Nov 2020 06:25:29 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37b94cea6fdec640e12b21ce5b846e8c7591c1bbd3f73538221374767362460`  
		Last Modified: Thu, 19 Nov 2020 06:27:39 GMT  
		Size: 11.5 MB (11500367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f96b01204efdb3b57520912607f112501248b5be77fd986c6d397f367e290d66`  
		Last Modified: Thu, 19 Nov 2020 06:27:37 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc9ae91a589697b43d9db64c38773ffd09a978edf568ac3c744a793ec93490cb`  
		Last Modified: Thu, 19 Nov 2020 09:25:48 GMT  
		Size: 276.3 MB (276297086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:375e55e6c143afbab56977401d0c13f62c15fcf1d0c5b54bf141acef29bc3c94`  
		Last Modified: Thu, 19 Nov 2020 09:25:28 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de5f684135aed6842f15dc83ee246860033044ea0767a78718ef7283e8336669`  
		Last Modified: Thu, 19 Nov 2020 09:25:57 GMT  
		Size: 11.8 MB (11808303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bef6ec9d292f414f2e057c6a55cacd28f22d8b1b9ef170b9a49db40a2950e7b`  
		Last Modified: Thu, 19 Nov 2020 09:25:55 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31da2fecd2e76420600c49f08974869b84e1fd3e99a0138aa6bd7298d3d4d633`  
		Last Modified: Thu, 19 Nov 2020 09:25:55 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfad719ddee04927017bfa4fee2356d9aaa7683efc57708638a2e3c4df3b90a5`  
		Last Modified: Thu, 19 Nov 2020 09:25:55 GMT  
		Size: 974.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `geonetwork:3.8`

```console
$ docker pull geonetwork@sha256:ebabffc6609467d0299607bcac1d09431361cd6a8b3544af87ca72b7ec5062de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `geonetwork:3.8` - linux; amd64

```console
$ docker pull geonetwork@sha256:bc18d01d733b8515fc5621a5d5cecd88cd5cab0c49cd6c80797cf4ef2afedcf7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **448.5 MB (448452015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ffe298eaf8b99d77104dac3ea9fabb000ce3cfddb95bdf2303795a8c2cbdd3f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 17 Nov 2020 20:20:58 GMT
ADD file:9a4fd72d749f4a791e75e0f6fc6028d0771e3381b6d84a8d0b07a4887bc7c641 in / 
# Tue, 17 Nov 2020 20:20:58 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 00:30:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 00:30:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Nov 2020 00:31:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 19 Nov 2020 03:06:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 19 Nov 2020 03:06:07 GMT
ENV LANG=C.UTF-8
# Thu, 19 Nov 2020 03:07:06 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 19 Nov 2020 03:07:06 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Nov 2020 03:07:08 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 19 Nov 2020 03:07:08 GMT
ENV JAVA_VERSION=8u275
# Thu, 19 Nov 2020 03:07:19 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u275-b01/OpenJDK8U-jdk_x64_linux_8u275b01.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 19 Nov 2020 06:13:16 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 19 Nov 2020 06:13:16 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Nov 2020 06:13:17 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 19 Nov 2020 06:13:18 GMT
WORKDIR /usr/local/tomcat
# Thu, 19 Nov 2020 06:13:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 19 Nov 2020 06:13:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 19 Nov 2020 06:21:01 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 19 Nov 2020 06:21:01 GMT
ENV TOMCAT_MAJOR=8
# Thu, 19 Nov 2020 06:21:02 GMT
ENV TOMCAT_VERSION=8.5.60
# Thu, 19 Nov 2020 06:21:02 GMT
ENV TOMCAT_SHA512=460b4d0f2d445670b69ff97d4295628b9ce444c294e301b4c0c5e4c48b42bb1a642769f075dfe105b7d7257d9aba62b75a6ea5b6fb65487891ab23d7bb3d6140
# Thu, 19 Nov 2020 06:21:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 19 Nov 2020 06:21:33 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 19 Nov 2020 06:21:33 GMT
EXPOSE 8080
# Thu, 19 Nov 2020 06:21:34 GMT
CMD ["catalina.sh" "run"]
# Thu, 19 Nov 2020 09:05:08 GMT
ENV GN_FILE=geonetwork.war
# Thu, 19 Nov 2020 09:05:08 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Thu, 19 Nov 2020 09:05:09 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Thu, 19 Nov 2020 09:12:18 GMT
ENV GN_VERSION=3.8.3
# Thu, 19 Nov 2020 09:12:18 GMT
ENV GN_DOWNLOAD_MD5=0d05c65aa4ac67fea90fa74f947822d6
# Thu, 19 Nov 2020 09:12:18 GMT
WORKDIR /usr/local/tomcat/webapps
# Thu, 19 Nov 2020 09:18:10 GMT
RUN curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/geonetwork.war/download &&      echo "$GN_DOWNLOAD_MD5 *$GN_FILE" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE
# Thu, 19 Nov 2020 09:18:11 GMT
COPY file:0804862fd42c05f06dfa65cb1e5dad9a956d8ac6a3ddd4d962847ba159f5cfe6 in /entrypoint.sh 
# Thu, 19 Nov 2020 09:18:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 19 Nov 2020 09:18:11 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:756975cb9c7e7933d824af9319b512dd72a50894232761d06ef3be59981df838`  
		Last Modified: Tue, 17 Nov 2020 20:27:06 GMT  
		Size: 50.4 MB (50397725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77915b4e630d47296770ce4cf481894885978072432456615172af463433cc5`  
		Last Modified: Wed, 18 Nov 2020 00:49:42 GMT  
		Size: 7.8 MB (7811717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f37a0a41b6b03489dd7de0aa2a79e369fd8b219bbc36b52f3f9790dc128e74b`  
		Last Modified: Wed, 18 Nov 2020 00:49:42 GMT  
		Size: 10.0 MB (9996233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96b2c1e36db5f5910f58da2ca4f9311b0690810c7107fb055ee1541498b5061f`  
		Last Modified: Wed, 18 Nov 2020 00:50:25 GMT  
		Size: 51.8 MB (51829318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a2d52b526e253b306ae38d6b75645b6a1716888a0b5e4b85b4dd93df8843a6`  
		Last Modified: Thu, 19 Nov 2020 03:11:37 GMT  
		Size: 5.3 MB (5284715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a36defce609c2ec5a9cc77094704955c777946a68d0f517f2d2d8223dd6420`  
		Last Modified: Thu, 19 Nov 2020 03:12:33 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e2014d79b302bdc5c3c30f767dddf39b02d21608607deb53450c893636731c1`  
		Last Modified: Thu, 19 Nov 2020 03:12:44 GMT  
		Size: 105.9 MB (105883500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528f69e563774f04c70bd19d8d09d1f758bf238b9c163dbd6ad5f2082ce0f194`  
		Last Modified: Thu, 19 Nov 2020 06:25:29 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37b94cea6fdec640e12b21ce5b846e8c7591c1bbd3f73538221374767362460`  
		Last Modified: Thu, 19 Nov 2020 06:27:39 GMT  
		Size: 11.5 MB (11500367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f96b01204efdb3b57520912607f112501248b5be77fd986c6d397f367e290d66`  
		Last Modified: Thu, 19 Nov 2020 06:27:37 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b80525e7a940bca2495d174da60002b358857a95d4d9afe25af6c29391b73b22`  
		Last Modified: Thu, 19 Nov 2020 09:26:21 GMT  
		Size: 205.7 MB (205747709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f74ced5dd82593bcfa96166dc6cebda4fcc5a300324608f8326a1897a224b77`  
		Last Modified: Thu, 19 Nov 2020 09:26:04 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `geonetwork:3.8.3`

```console
$ docker pull geonetwork@sha256:ebabffc6609467d0299607bcac1d09431361cd6a8b3544af87ca72b7ec5062de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `geonetwork:3.8.3` - linux; amd64

```console
$ docker pull geonetwork@sha256:bc18d01d733b8515fc5621a5d5cecd88cd5cab0c49cd6c80797cf4ef2afedcf7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **448.5 MB (448452015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ffe298eaf8b99d77104dac3ea9fabb000ce3cfddb95bdf2303795a8c2cbdd3f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 17 Nov 2020 20:20:58 GMT
ADD file:9a4fd72d749f4a791e75e0f6fc6028d0771e3381b6d84a8d0b07a4887bc7c641 in / 
# Tue, 17 Nov 2020 20:20:58 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 00:30:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 00:30:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Nov 2020 00:31:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 19 Nov 2020 03:06:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 19 Nov 2020 03:06:07 GMT
ENV LANG=C.UTF-8
# Thu, 19 Nov 2020 03:07:06 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 19 Nov 2020 03:07:06 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Nov 2020 03:07:08 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 19 Nov 2020 03:07:08 GMT
ENV JAVA_VERSION=8u275
# Thu, 19 Nov 2020 03:07:19 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u275-b01/OpenJDK8U-jdk_x64_linux_8u275b01.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 19 Nov 2020 06:13:16 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 19 Nov 2020 06:13:16 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Nov 2020 06:13:17 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 19 Nov 2020 06:13:18 GMT
WORKDIR /usr/local/tomcat
# Thu, 19 Nov 2020 06:13:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 19 Nov 2020 06:13:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 19 Nov 2020 06:21:01 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 19 Nov 2020 06:21:01 GMT
ENV TOMCAT_MAJOR=8
# Thu, 19 Nov 2020 06:21:02 GMT
ENV TOMCAT_VERSION=8.5.60
# Thu, 19 Nov 2020 06:21:02 GMT
ENV TOMCAT_SHA512=460b4d0f2d445670b69ff97d4295628b9ce444c294e301b4c0c5e4c48b42bb1a642769f075dfe105b7d7257d9aba62b75a6ea5b6fb65487891ab23d7bb3d6140
# Thu, 19 Nov 2020 06:21:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 19 Nov 2020 06:21:33 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 19 Nov 2020 06:21:33 GMT
EXPOSE 8080
# Thu, 19 Nov 2020 06:21:34 GMT
CMD ["catalina.sh" "run"]
# Thu, 19 Nov 2020 09:05:08 GMT
ENV GN_FILE=geonetwork.war
# Thu, 19 Nov 2020 09:05:08 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Thu, 19 Nov 2020 09:05:09 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Thu, 19 Nov 2020 09:12:18 GMT
ENV GN_VERSION=3.8.3
# Thu, 19 Nov 2020 09:12:18 GMT
ENV GN_DOWNLOAD_MD5=0d05c65aa4ac67fea90fa74f947822d6
# Thu, 19 Nov 2020 09:12:18 GMT
WORKDIR /usr/local/tomcat/webapps
# Thu, 19 Nov 2020 09:18:10 GMT
RUN curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/geonetwork.war/download &&      echo "$GN_DOWNLOAD_MD5 *$GN_FILE" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE
# Thu, 19 Nov 2020 09:18:11 GMT
COPY file:0804862fd42c05f06dfa65cb1e5dad9a956d8ac6a3ddd4d962847ba159f5cfe6 in /entrypoint.sh 
# Thu, 19 Nov 2020 09:18:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 19 Nov 2020 09:18:11 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:756975cb9c7e7933d824af9319b512dd72a50894232761d06ef3be59981df838`  
		Last Modified: Tue, 17 Nov 2020 20:27:06 GMT  
		Size: 50.4 MB (50397725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77915b4e630d47296770ce4cf481894885978072432456615172af463433cc5`  
		Last Modified: Wed, 18 Nov 2020 00:49:42 GMT  
		Size: 7.8 MB (7811717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f37a0a41b6b03489dd7de0aa2a79e369fd8b219bbc36b52f3f9790dc128e74b`  
		Last Modified: Wed, 18 Nov 2020 00:49:42 GMT  
		Size: 10.0 MB (9996233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96b2c1e36db5f5910f58da2ca4f9311b0690810c7107fb055ee1541498b5061f`  
		Last Modified: Wed, 18 Nov 2020 00:50:25 GMT  
		Size: 51.8 MB (51829318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a2d52b526e253b306ae38d6b75645b6a1716888a0b5e4b85b4dd93df8843a6`  
		Last Modified: Thu, 19 Nov 2020 03:11:37 GMT  
		Size: 5.3 MB (5284715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a36defce609c2ec5a9cc77094704955c777946a68d0f517f2d2d8223dd6420`  
		Last Modified: Thu, 19 Nov 2020 03:12:33 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e2014d79b302bdc5c3c30f767dddf39b02d21608607deb53450c893636731c1`  
		Last Modified: Thu, 19 Nov 2020 03:12:44 GMT  
		Size: 105.9 MB (105883500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528f69e563774f04c70bd19d8d09d1f758bf238b9c163dbd6ad5f2082ce0f194`  
		Last Modified: Thu, 19 Nov 2020 06:25:29 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37b94cea6fdec640e12b21ce5b846e8c7591c1bbd3f73538221374767362460`  
		Last Modified: Thu, 19 Nov 2020 06:27:39 GMT  
		Size: 11.5 MB (11500367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f96b01204efdb3b57520912607f112501248b5be77fd986c6d397f367e290d66`  
		Last Modified: Thu, 19 Nov 2020 06:27:37 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b80525e7a940bca2495d174da60002b358857a95d4d9afe25af6c29391b73b22`  
		Last Modified: Thu, 19 Nov 2020 09:26:21 GMT  
		Size: 205.7 MB (205747709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f74ced5dd82593bcfa96166dc6cebda4fcc5a300324608f8326a1897a224b77`  
		Last Modified: Thu, 19 Nov 2020 09:26:04 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `geonetwork:3.8.3-postgres`

```console
$ docker pull geonetwork@sha256:e9a113ac97edd29540c853ea6703eff6009737959c072165b51e4f9110f04843
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `geonetwork:3.8.3-postgres` - linux; amd64

```console
$ docker pull geonetwork@sha256:e73057c51db7c29c0299966206e1cb1f36ff7dfe3b7b75848a00012d614a2fea
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **460.3 MB (460263090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb1ac9ed7c6a0529fadaa802a24e719c5d91a1311de34a51e2147998eccc4c9e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 17 Nov 2020 20:20:58 GMT
ADD file:9a4fd72d749f4a791e75e0f6fc6028d0771e3381b6d84a8d0b07a4887bc7c641 in / 
# Tue, 17 Nov 2020 20:20:58 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 00:30:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 00:30:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Nov 2020 00:31:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 19 Nov 2020 03:06:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 19 Nov 2020 03:06:07 GMT
ENV LANG=C.UTF-8
# Thu, 19 Nov 2020 03:07:06 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 19 Nov 2020 03:07:06 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Nov 2020 03:07:08 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 19 Nov 2020 03:07:08 GMT
ENV JAVA_VERSION=8u275
# Thu, 19 Nov 2020 03:07:19 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u275-b01/OpenJDK8U-jdk_x64_linux_8u275b01.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 19 Nov 2020 06:13:16 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 19 Nov 2020 06:13:16 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Nov 2020 06:13:17 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 19 Nov 2020 06:13:18 GMT
WORKDIR /usr/local/tomcat
# Thu, 19 Nov 2020 06:13:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 19 Nov 2020 06:13:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 19 Nov 2020 06:21:01 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 19 Nov 2020 06:21:01 GMT
ENV TOMCAT_MAJOR=8
# Thu, 19 Nov 2020 06:21:02 GMT
ENV TOMCAT_VERSION=8.5.60
# Thu, 19 Nov 2020 06:21:02 GMT
ENV TOMCAT_SHA512=460b4d0f2d445670b69ff97d4295628b9ce444c294e301b4c0c5e4c48b42bb1a642769f075dfe105b7d7257d9aba62b75a6ea5b6fb65487891ab23d7bb3d6140
# Thu, 19 Nov 2020 06:21:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 19 Nov 2020 06:21:33 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 19 Nov 2020 06:21:33 GMT
EXPOSE 8080
# Thu, 19 Nov 2020 06:21:34 GMT
CMD ["catalina.sh" "run"]
# Thu, 19 Nov 2020 09:05:08 GMT
ENV GN_FILE=geonetwork.war
# Thu, 19 Nov 2020 09:05:08 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Thu, 19 Nov 2020 09:05:09 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Thu, 19 Nov 2020 09:12:18 GMT
ENV GN_VERSION=3.8.3
# Thu, 19 Nov 2020 09:12:18 GMT
ENV GN_DOWNLOAD_MD5=0d05c65aa4ac67fea90fa74f947822d6
# Thu, 19 Nov 2020 09:12:18 GMT
WORKDIR /usr/local/tomcat/webapps
# Thu, 19 Nov 2020 09:18:10 GMT
RUN curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/geonetwork.war/download &&      echo "$GN_DOWNLOAD_MD5 *$GN_FILE" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE
# Thu, 19 Nov 2020 09:18:11 GMT
COPY file:0804862fd42c05f06dfa65cb1e5dad9a956d8ac6a3ddd4d962847ba159f5cfe6 in /entrypoint.sh 
# Thu, 19 Nov 2020 09:18:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 19 Nov 2020 09:18:11 GMT
CMD ["catalina.sh" "run"]
# Thu, 19 Nov 2020 09:18:35 GMT
RUN apt-get update && apt-get install -y postgresql-client &&     rm -rf /var/lib/apt/lists/*
# Thu, 19 Nov 2020 09:18:36 GMT
RUN sed -i -e 's#<import resource="../config-db/h2.xml"/>#<!--<import resource="../config-db/h2.xml"/> -->#g' $CATALINA_HOME/webapps/geonetwork/WEB-INF/config-node/srv.xml && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' $CATALINA_HOME/webapps/geonetwork/WEB-INF/config-node/srv.xml
# Thu, 19 Nov 2020 09:18:36 GMT
COPY file:2dedfd940a86106b2ae284c537f14d365881c03a01b212f81b49177bb22c8d7a in /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties 
# Thu, 19 Nov 2020 09:18:36 GMT
COPY file:c88411abba7ad9b7bb75019f08755dbfa163d2fc7fdd80676bf9350c4c56a19c in /entrypoint.sh 
# Thu, 19 Nov 2020 09:18:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 19 Nov 2020 09:18:36 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:756975cb9c7e7933d824af9319b512dd72a50894232761d06ef3be59981df838`  
		Last Modified: Tue, 17 Nov 2020 20:27:06 GMT  
		Size: 50.4 MB (50397725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77915b4e630d47296770ce4cf481894885978072432456615172af463433cc5`  
		Last Modified: Wed, 18 Nov 2020 00:49:42 GMT  
		Size: 7.8 MB (7811717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f37a0a41b6b03489dd7de0aa2a79e369fd8b219bbc36b52f3f9790dc128e74b`  
		Last Modified: Wed, 18 Nov 2020 00:49:42 GMT  
		Size: 10.0 MB (9996233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96b2c1e36db5f5910f58da2ca4f9311b0690810c7107fb055ee1541498b5061f`  
		Last Modified: Wed, 18 Nov 2020 00:50:25 GMT  
		Size: 51.8 MB (51829318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a2d52b526e253b306ae38d6b75645b6a1716888a0b5e4b85b4dd93df8843a6`  
		Last Modified: Thu, 19 Nov 2020 03:11:37 GMT  
		Size: 5.3 MB (5284715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a36defce609c2ec5a9cc77094704955c777946a68d0f517f2d2d8223dd6420`  
		Last Modified: Thu, 19 Nov 2020 03:12:33 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e2014d79b302bdc5c3c30f767dddf39b02d21608607deb53450c893636731c1`  
		Last Modified: Thu, 19 Nov 2020 03:12:44 GMT  
		Size: 105.9 MB (105883500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528f69e563774f04c70bd19d8d09d1f758bf238b9c163dbd6ad5f2082ce0f194`  
		Last Modified: Thu, 19 Nov 2020 06:25:29 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37b94cea6fdec640e12b21ce5b846e8c7591c1bbd3f73538221374767362460`  
		Last Modified: Thu, 19 Nov 2020 06:27:39 GMT  
		Size: 11.5 MB (11500367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f96b01204efdb3b57520912607f112501248b5be77fd986c6d397f367e290d66`  
		Last Modified: Thu, 19 Nov 2020 06:27:37 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b80525e7a940bca2495d174da60002b358857a95d4d9afe25af6c29391b73b22`  
		Last Modified: Thu, 19 Nov 2020 09:26:21 GMT  
		Size: 205.7 MB (205747709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f74ced5dd82593bcfa96166dc6cebda4fcc5a300324608f8326a1897a224b77`  
		Last Modified: Thu, 19 Nov 2020 09:26:04 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:428c9851436d7c7d7e03fc5692d33747406a167aa5e6b8ec14137752ed3089be`  
		Last Modified: Thu, 19 Nov 2020 09:26:29 GMT  
		Size: 11.8 MB (11808301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90147430dad2ba5c5801a58d10e91999d0220cb5c56e69b4bc0754aba7d2323d`  
		Last Modified: Thu, 19 Nov 2020 09:26:27 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:955da5f1a930decb2d0eddee117104cf50dca2f0cec528ae80f0ad96653a4cbe`  
		Last Modified: Thu, 19 Nov 2020 09:26:27 GMT  
		Size: 536.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cfa39b87b0b498def9001db63285077b471a48ce0298b98ec9d7b2a765c0cbc`  
		Last Modified: Thu, 19 Nov 2020 09:26:27 GMT  
		Size: 974.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `geonetwork:3.8-postgres`

```console
$ docker pull geonetwork@sha256:e9a113ac97edd29540c853ea6703eff6009737959c072165b51e4f9110f04843
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `geonetwork:3.8-postgres` - linux; amd64

```console
$ docker pull geonetwork@sha256:e73057c51db7c29c0299966206e1cb1f36ff7dfe3b7b75848a00012d614a2fea
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **460.3 MB (460263090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb1ac9ed7c6a0529fadaa802a24e719c5d91a1311de34a51e2147998eccc4c9e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 17 Nov 2020 20:20:58 GMT
ADD file:9a4fd72d749f4a791e75e0f6fc6028d0771e3381b6d84a8d0b07a4887bc7c641 in / 
# Tue, 17 Nov 2020 20:20:58 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 00:30:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 00:30:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Nov 2020 00:31:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 19 Nov 2020 03:06:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 19 Nov 2020 03:06:07 GMT
ENV LANG=C.UTF-8
# Thu, 19 Nov 2020 03:07:06 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 19 Nov 2020 03:07:06 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Nov 2020 03:07:08 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 19 Nov 2020 03:07:08 GMT
ENV JAVA_VERSION=8u275
# Thu, 19 Nov 2020 03:07:19 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u275-b01/OpenJDK8U-jdk_x64_linux_8u275b01.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 19 Nov 2020 06:13:16 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 19 Nov 2020 06:13:16 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Nov 2020 06:13:17 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 19 Nov 2020 06:13:18 GMT
WORKDIR /usr/local/tomcat
# Thu, 19 Nov 2020 06:13:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 19 Nov 2020 06:13:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 19 Nov 2020 06:21:01 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 19 Nov 2020 06:21:01 GMT
ENV TOMCAT_MAJOR=8
# Thu, 19 Nov 2020 06:21:02 GMT
ENV TOMCAT_VERSION=8.5.60
# Thu, 19 Nov 2020 06:21:02 GMT
ENV TOMCAT_SHA512=460b4d0f2d445670b69ff97d4295628b9ce444c294e301b4c0c5e4c48b42bb1a642769f075dfe105b7d7257d9aba62b75a6ea5b6fb65487891ab23d7bb3d6140
# Thu, 19 Nov 2020 06:21:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 19 Nov 2020 06:21:33 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 19 Nov 2020 06:21:33 GMT
EXPOSE 8080
# Thu, 19 Nov 2020 06:21:34 GMT
CMD ["catalina.sh" "run"]
# Thu, 19 Nov 2020 09:05:08 GMT
ENV GN_FILE=geonetwork.war
# Thu, 19 Nov 2020 09:05:08 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Thu, 19 Nov 2020 09:05:09 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Thu, 19 Nov 2020 09:12:18 GMT
ENV GN_VERSION=3.8.3
# Thu, 19 Nov 2020 09:12:18 GMT
ENV GN_DOWNLOAD_MD5=0d05c65aa4ac67fea90fa74f947822d6
# Thu, 19 Nov 2020 09:12:18 GMT
WORKDIR /usr/local/tomcat/webapps
# Thu, 19 Nov 2020 09:18:10 GMT
RUN curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/geonetwork.war/download &&      echo "$GN_DOWNLOAD_MD5 *$GN_FILE" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE
# Thu, 19 Nov 2020 09:18:11 GMT
COPY file:0804862fd42c05f06dfa65cb1e5dad9a956d8ac6a3ddd4d962847ba159f5cfe6 in /entrypoint.sh 
# Thu, 19 Nov 2020 09:18:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 19 Nov 2020 09:18:11 GMT
CMD ["catalina.sh" "run"]
# Thu, 19 Nov 2020 09:18:35 GMT
RUN apt-get update && apt-get install -y postgresql-client &&     rm -rf /var/lib/apt/lists/*
# Thu, 19 Nov 2020 09:18:36 GMT
RUN sed -i -e 's#<import resource="../config-db/h2.xml"/>#<!--<import resource="../config-db/h2.xml"/> -->#g' $CATALINA_HOME/webapps/geonetwork/WEB-INF/config-node/srv.xml && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' $CATALINA_HOME/webapps/geonetwork/WEB-INF/config-node/srv.xml
# Thu, 19 Nov 2020 09:18:36 GMT
COPY file:2dedfd940a86106b2ae284c537f14d365881c03a01b212f81b49177bb22c8d7a in /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties 
# Thu, 19 Nov 2020 09:18:36 GMT
COPY file:c88411abba7ad9b7bb75019f08755dbfa163d2fc7fdd80676bf9350c4c56a19c in /entrypoint.sh 
# Thu, 19 Nov 2020 09:18:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 19 Nov 2020 09:18:36 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:756975cb9c7e7933d824af9319b512dd72a50894232761d06ef3be59981df838`  
		Last Modified: Tue, 17 Nov 2020 20:27:06 GMT  
		Size: 50.4 MB (50397725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77915b4e630d47296770ce4cf481894885978072432456615172af463433cc5`  
		Last Modified: Wed, 18 Nov 2020 00:49:42 GMT  
		Size: 7.8 MB (7811717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f37a0a41b6b03489dd7de0aa2a79e369fd8b219bbc36b52f3f9790dc128e74b`  
		Last Modified: Wed, 18 Nov 2020 00:49:42 GMT  
		Size: 10.0 MB (9996233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96b2c1e36db5f5910f58da2ca4f9311b0690810c7107fb055ee1541498b5061f`  
		Last Modified: Wed, 18 Nov 2020 00:50:25 GMT  
		Size: 51.8 MB (51829318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a2d52b526e253b306ae38d6b75645b6a1716888a0b5e4b85b4dd93df8843a6`  
		Last Modified: Thu, 19 Nov 2020 03:11:37 GMT  
		Size: 5.3 MB (5284715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a36defce609c2ec5a9cc77094704955c777946a68d0f517f2d2d8223dd6420`  
		Last Modified: Thu, 19 Nov 2020 03:12:33 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e2014d79b302bdc5c3c30f767dddf39b02d21608607deb53450c893636731c1`  
		Last Modified: Thu, 19 Nov 2020 03:12:44 GMT  
		Size: 105.9 MB (105883500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528f69e563774f04c70bd19d8d09d1f758bf238b9c163dbd6ad5f2082ce0f194`  
		Last Modified: Thu, 19 Nov 2020 06:25:29 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37b94cea6fdec640e12b21ce5b846e8c7591c1bbd3f73538221374767362460`  
		Last Modified: Thu, 19 Nov 2020 06:27:39 GMT  
		Size: 11.5 MB (11500367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f96b01204efdb3b57520912607f112501248b5be77fd986c6d397f367e290d66`  
		Last Modified: Thu, 19 Nov 2020 06:27:37 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b80525e7a940bca2495d174da60002b358857a95d4d9afe25af6c29391b73b22`  
		Last Modified: Thu, 19 Nov 2020 09:26:21 GMT  
		Size: 205.7 MB (205747709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f74ced5dd82593bcfa96166dc6cebda4fcc5a300324608f8326a1897a224b77`  
		Last Modified: Thu, 19 Nov 2020 09:26:04 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:428c9851436d7c7d7e03fc5692d33747406a167aa5e6b8ec14137752ed3089be`  
		Last Modified: Thu, 19 Nov 2020 09:26:29 GMT  
		Size: 11.8 MB (11808301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90147430dad2ba5c5801a58d10e91999d0220cb5c56e69b4bc0754aba7d2323d`  
		Last Modified: Thu, 19 Nov 2020 09:26:27 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:955da5f1a930decb2d0eddee117104cf50dca2f0cec528ae80f0ad96653a4cbe`  
		Last Modified: Thu, 19 Nov 2020 09:26:27 GMT  
		Size: 536.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cfa39b87b0b498def9001db63285077b471a48ce0298b98ec9d7b2a765c0cbc`  
		Last Modified: Thu, 19 Nov 2020 09:26:27 GMT  
		Size: 974.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `geonetwork:3-postgres`

```console
$ docker pull geonetwork@sha256:a370092791facbc5e807f4b7b3b59996741cdce5b3a43f0d80c6fb9bf434399a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `geonetwork:3-postgres` - linux; amd64

```console
$ docker pull geonetwork@sha256:197f62a106d8cf980ccade87705c14e75ca756e51a82d40268b3f8d14bab27de
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.8 MB (530813056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8082cf9604ffc803448d1271c9277b539523e0b381fc42db9a9e91fb5b22c35b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 17 Nov 2020 20:20:58 GMT
ADD file:9a4fd72d749f4a791e75e0f6fc6028d0771e3381b6d84a8d0b07a4887bc7c641 in / 
# Tue, 17 Nov 2020 20:20:58 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 00:30:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 00:30:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Nov 2020 00:31:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 19 Nov 2020 03:06:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 19 Nov 2020 03:06:07 GMT
ENV LANG=C.UTF-8
# Thu, 19 Nov 2020 03:07:06 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 19 Nov 2020 03:07:06 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Nov 2020 03:07:08 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 19 Nov 2020 03:07:08 GMT
ENV JAVA_VERSION=8u275
# Thu, 19 Nov 2020 03:07:19 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u275-b01/OpenJDK8U-jdk_x64_linux_8u275b01.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 19 Nov 2020 06:13:16 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 19 Nov 2020 06:13:16 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Nov 2020 06:13:17 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 19 Nov 2020 06:13:18 GMT
WORKDIR /usr/local/tomcat
# Thu, 19 Nov 2020 06:13:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 19 Nov 2020 06:13:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 19 Nov 2020 06:21:01 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 19 Nov 2020 06:21:01 GMT
ENV TOMCAT_MAJOR=8
# Thu, 19 Nov 2020 06:21:02 GMT
ENV TOMCAT_VERSION=8.5.60
# Thu, 19 Nov 2020 06:21:02 GMT
ENV TOMCAT_SHA512=460b4d0f2d445670b69ff97d4295628b9ce444c294e301b4c0c5e4c48b42bb1a642769f075dfe105b7d7257d9aba62b75a6ea5b6fb65487891ab23d7bb3d6140
# Thu, 19 Nov 2020 06:21:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 19 Nov 2020 06:21:33 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 19 Nov 2020 06:21:33 GMT
EXPOSE 8080
# Thu, 19 Nov 2020 06:21:34 GMT
CMD ["catalina.sh" "run"]
# Thu, 19 Nov 2020 09:05:08 GMT
ENV GN_FILE=geonetwork.war
# Thu, 19 Nov 2020 09:05:08 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Thu, 19 Nov 2020 09:05:09 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Thu, 19 Nov 2020 09:05:09 GMT
ENV GN_VERSION=3.10.5
# Thu, 19 Nov 2020 09:05:09 GMT
ENV GN_DOWNLOAD_MD5=63ffc3929e486e48c56b89b62da72813
# Thu, 19 Nov 2020 09:05:09 GMT
WORKDIR /usr/local/tomcat/webapps
# Thu, 19 Nov 2020 09:11:44 GMT
RUN curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "$GN_DOWNLOAD_MD5 *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE
# Thu, 19 Nov 2020 09:11:44 GMT
COPY file:0804862fd42c05f06dfa65cb1e5dad9a956d8ac6a3ddd4d962847ba159f5cfe6 in /entrypoint.sh 
# Thu, 19 Nov 2020 09:11:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 19 Nov 2020 09:11:44 GMT
CMD ["catalina.sh" "run"]
# Thu, 19 Nov 2020 09:12:10 GMT
RUN apt-get update && apt-get install -y postgresql-client &&     rm -rf /var/lib/apt/lists/*
# Thu, 19 Nov 2020 09:12:11 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' $CATALINA_HOME/webapps/geonetwork/WEB-INF/config-node/srv.xml && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' $CATALINA_HOME/webapps/geonetwork/WEB-INF/config-node/srv.xml
# Thu, 19 Nov 2020 09:12:12 GMT
COPY file:83f69d2041e5fb378033b0db57e096c81ba0725102ab4da4f089685e748fcce3 in /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties 
# Thu, 19 Nov 2020 09:12:12 GMT
COPY file:c88411abba7ad9b7bb75019f08755dbfa163d2fc7fdd80676bf9350c4c56a19c in /entrypoint.sh 
# Thu, 19 Nov 2020 09:12:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 19 Nov 2020 09:12:12 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:756975cb9c7e7933d824af9319b512dd72a50894232761d06ef3be59981df838`  
		Last Modified: Tue, 17 Nov 2020 20:27:06 GMT  
		Size: 50.4 MB (50397725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77915b4e630d47296770ce4cf481894885978072432456615172af463433cc5`  
		Last Modified: Wed, 18 Nov 2020 00:49:42 GMT  
		Size: 7.8 MB (7811717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f37a0a41b6b03489dd7de0aa2a79e369fd8b219bbc36b52f3f9790dc128e74b`  
		Last Modified: Wed, 18 Nov 2020 00:49:42 GMT  
		Size: 10.0 MB (9996233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96b2c1e36db5f5910f58da2ca4f9311b0690810c7107fb055ee1541498b5061f`  
		Last Modified: Wed, 18 Nov 2020 00:50:25 GMT  
		Size: 51.8 MB (51829318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a2d52b526e253b306ae38d6b75645b6a1716888a0b5e4b85b4dd93df8843a6`  
		Last Modified: Thu, 19 Nov 2020 03:11:37 GMT  
		Size: 5.3 MB (5284715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a36defce609c2ec5a9cc77094704955c777946a68d0f517f2d2d8223dd6420`  
		Last Modified: Thu, 19 Nov 2020 03:12:33 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e2014d79b302bdc5c3c30f767dddf39b02d21608607deb53450c893636731c1`  
		Last Modified: Thu, 19 Nov 2020 03:12:44 GMT  
		Size: 105.9 MB (105883500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528f69e563774f04c70bd19d8d09d1f758bf238b9c163dbd6ad5f2082ce0f194`  
		Last Modified: Thu, 19 Nov 2020 06:25:29 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37b94cea6fdec640e12b21ce5b846e8c7591c1bbd3f73538221374767362460`  
		Last Modified: Thu, 19 Nov 2020 06:27:39 GMT  
		Size: 11.5 MB (11500367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f96b01204efdb3b57520912607f112501248b5be77fd986c6d397f367e290d66`  
		Last Modified: Thu, 19 Nov 2020 06:27:37 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc9ae91a589697b43d9db64c38773ffd09a978edf568ac3c744a793ec93490cb`  
		Last Modified: Thu, 19 Nov 2020 09:25:48 GMT  
		Size: 276.3 MB (276297086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:375e55e6c143afbab56977401d0c13f62c15fcf1d0c5b54bf141acef29bc3c94`  
		Last Modified: Thu, 19 Nov 2020 09:25:28 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de5f684135aed6842f15dc83ee246860033044ea0767a78718ef7283e8336669`  
		Last Modified: Thu, 19 Nov 2020 09:25:57 GMT  
		Size: 11.8 MB (11808303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bef6ec9d292f414f2e057c6a55cacd28f22d8b1b9ef170b9a49db40a2950e7b`  
		Last Modified: Thu, 19 Nov 2020 09:25:55 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31da2fecd2e76420600c49f08974869b84e1fd3e99a0138aa6bd7298d3d4d633`  
		Last Modified: Thu, 19 Nov 2020 09:25:55 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfad719ddee04927017bfa4fee2356d9aaa7683efc57708638a2e3c4df3b90a5`  
		Last Modified: Thu, 19 Nov 2020 09:25:55 GMT  
		Size: 974.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `geonetwork:4`

```console
$ docker pull geonetwork@sha256:415c652d5a4623888973c0c57bf3c7be7476b838fb61ea75cf798d365df999d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `geonetwork:4` - linux; amd64

```console
$ docker pull geonetwork@sha256:d941c9f58436cc5c29aa15078b0ce1430992b3d276c04d47076c535855dc389b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **416.2 MB (416166939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3867e0339e7768d88d73b9a96f618540991fcc24ed516f3a0329a30b2c16463`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 17 Nov 2020 20:20:58 GMT
ADD file:9a4fd72d749f4a791e75e0f6fc6028d0771e3381b6d84a8d0b07a4887bc7c641 in / 
# Tue, 17 Nov 2020 20:20:58 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 00:30:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 00:30:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 19 Nov 2020 03:06:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 19 Nov 2020 03:06:45 GMT
ENV LANG=C.UTF-8
# Thu, 19 Nov 2020 03:07:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 19 Nov 2020 03:07:31 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Nov 2020 03:07:32 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 19 Nov 2020 03:07:32 GMT
ENV JAVA_VERSION=8u275
# Thu, 19 Nov 2020 03:07:38 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u275-b01/OpenJDK8U-jre_x64_linux_8u275b01.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 19 Nov 2020 08:10:48 GMT
ENV JETTY_VERSION=9.4.34.v20201102
# Thu, 19 Nov 2020 08:10:49 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 19 Nov 2020 08:10:49 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 19 Nov 2020 08:10:49 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 19 Nov 2020 08:10:49 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Nov 2020 08:10:49 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.34.v20201102/jetty-home-9.4.34.v20201102.tar.gz
# Thu, 19 Nov 2020 08:10:50 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E 	F254B35617DC255D9344BCFA873A8E86B4372146
# Thu, 19 Nov 2020 08:10:53 GMT
RUN set -xe ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		for server in 			ha.pool.sks-keyservers.net 			p80.pool.sks-keyservers.net:80 			ipv4.pool.sks-keyservers.net 			pgp.mit.edu ; 		do 			if gpg --batch --keyserver "$server" --recv-keys "$key"; then 				break; 			fi; 		done; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	mkdir -p "$TMPDIR" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Thu, 19 Nov 2020 08:10:53 GMT
WORKDIR /var/lib/jetty
# Thu, 19 Nov 2020 08:10:53 GMT
COPY multi:aa77a0f6aef2add1a97bf742e5d8ca9322cda3f66ea7673ea49c33da7e5b0889 in / 
# Thu, 19 Nov 2020 08:10:54 GMT
USER jetty
# Thu, 19 Nov 2020 08:10:54 GMT
EXPOSE 8080
# Thu, 19 Nov 2020 08:10:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 19 Nov 2020 08:10:54 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Thu, 19 Nov 2020 09:18:42 GMT
ENV DATA_DIR=/catalogue-data
# Thu, 19 Nov 2020 09:18:43 GMT
ENV JAVA_OPTS=-Dorg.eclipse.jetty.annotations.AnnotationParser.LEVEL=OFF         -Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC         -Dgeonetwork.resources.dir=/catalogue-data/resources         -Dgeonetwork.data.dir=/catalogue-data         -Dgeonetwork.codeList.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/codelist         -Dgeonetwork.schema.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/schema_plugins
# Thu, 19 Nov 2020 09:18:43 GMT
USER root
# Thu, 19 Nov 2020 09:18:47 GMT
RUN apt-get -y update &&     apt-get -y install curl &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p /${DATA_DIR} &&     chown -R jetty:jetty ${DATA_DIR} &&     mkdir -p /var/lib/jetty/webapps/geonetwork &&     chown -R jetty:jetty /var/lib/jetty/webapps/geonetwork
# Thu, 19 Nov 2020 09:18:48 GMT
USER jetty
# Thu, 19 Nov 2020 09:18:48 GMT
ENV GN_FILE=GeoNetwork-4.0.1-0.war
# Thu, 19 Nov 2020 09:18:48 GMT
ENV GN_VERSION=4.0.1
# Thu, 19 Nov 2020 09:18:48 GMT
ENV GN_DOWNLOAD_MD5=e9c885de19644856d855c0ea78052b12
# Thu, 19 Nov 2020 09:25:09 GMT
RUN cd /var/lib/jetty/webapps/geonetwork/ &&     curl -fSL -o geonetwork.war      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c &&      unzip -q geonetwork.war &&      rm geonetwork.war
# Thu, 19 Nov 2020 09:25:09 GMT
COPY file:ca46ab251df3dfc253cb04cf962e7266e42428fab31ad2f583a7c86b06d5f778 in /geonetwork-entrypoint.sh 
# Thu, 19 Nov 2020 09:25:09 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Thu, 19 Nov 2020 09:25:10 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Thu, 19 Nov 2020 09:25:10 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:756975cb9c7e7933d824af9319b512dd72a50894232761d06ef3be59981df838`  
		Last Modified: Tue, 17 Nov 2020 20:27:06 GMT  
		Size: 50.4 MB (50397725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77915b4e630d47296770ce4cf481894885978072432456615172af463433cc5`  
		Last Modified: Wed, 18 Nov 2020 00:49:42 GMT  
		Size: 7.8 MB (7811717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f37a0a41b6b03489dd7de0aa2a79e369fd8b219bbc36b52f3f9790dc128e74b`  
		Last Modified: Wed, 18 Nov 2020 00:49:42 GMT  
		Size: 10.0 MB (9996233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:713f7746108e0e07f616eec5ac22de7d9981c7e5087a3d63d92193b71d3e98e3`  
		Last Modified: Thu, 19 Nov 2020 03:12:18 GMT  
		Size: 5.5 MB (5529433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba38f0ad15ed007b8974fb97b174e2f3e0418a49a03c215e237812c058006714`  
		Last Modified: Thu, 19 Nov 2020 03:12:53 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aef0ecdbb4512b269e1df4a3a65f0ff50bbfbdbfe16779256f3f3954f36eb61b`  
		Last Modified: Thu, 19 Nov 2020 03:12:58 GMT  
		Size: 41.3 MB (41301352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c767072a31fb49fa5ec3f5d0f4b2ca6d3e04b4ef754b9b7fd71d0fa5447a441`  
		Last Modified: Thu, 19 Nov 2020 08:13:07 GMT  
		Size: 9.8 MB (9769134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c78e45ba22d7119a5b75d071e6ef1f9b80b2dfd6417e93a735629b5dab0fb706`  
		Last Modified: Thu, 19 Nov 2020 08:13:05 GMT  
		Size: 1.4 KB (1450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:533b056ffb8af9013fc3139e24823323cb094906b2806c0d2c44bf2b0fd287ad`  
		Last Modified: Thu, 19 Nov 2020 09:26:34 GMT  
		Size: 466.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:795a6fe00ffbb6dbafddade9a45c8e68a7dea98e2ba0827d8b80b2ba70ed8fe3`  
		Last Modified: Thu, 19 Nov 2020 09:26:54 GMT  
		Size: 291.4 MB (291358257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be1be42981519abedd791e8c2637ac927ba30a0b879356ed0840bcee2c37e7b0`  
		Last Modified: Thu, 19 Nov 2020 09:26:35 GMT  
		Size: 959.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `geonetwork:4.0`

```console
$ docker pull geonetwork@sha256:415c652d5a4623888973c0c57bf3c7be7476b838fb61ea75cf798d365df999d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `geonetwork:4.0` - linux; amd64

```console
$ docker pull geonetwork@sha256:d941c9f58436cc5c29aa15078b0ce1430992b3d276c04d47076c535855dc389b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **416.2 MB (416166939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3867e0339e7768d88d73b9a96f618540991fcc24ed516f3a0329a30b2c16463`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 17 Nov 2020 20:20:58 GMT
ADD file:9a4fd72d749f4a791e75e0f6fc6028d0771e3381b6d84a8d0b07a4887bc7c641 in / 
# Tue, 17 Nov 2020 20:20:58 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 00:30:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 00:30:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 19 Nov 2020 03:06:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 19 Nov 2020 03:06:45 GMT
ENV LANG=C.UTF-8
# Thu, 19 Nov 2020 03:07:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 19 Nov 2020 03:07:31 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Nov 2020 03:07:32 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 19 Nov 2020 03:07:32 GMT
ENV JAVA_VERSION=8u275
# Thu, 19 Nov 2020 03:07:38 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u275-b01/OpenJDK8U-jre_x64_linux_8u275b01.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 19 Nov 2020 08:10:48 GMT
ENV JETTY_VERSION=9.4.34.v20201102
# Thu, 19 Nov 2020 08:10:49 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 19 Nov 2020 08:10:49 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 19 Nov 2020 08:10:49 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 19 Nov 2020 08:10:49 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Nov 2020 08:10:49 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.34.v20201102/jetty-home-9.4.34.v20201102.tar.gz
# Thu, 19 Nov 2020 08:10:50 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E 	F254B35617DC255D9344BCFA873A8E86B4372146
# Thu, 19 Nov 2020 08:10:53 GMT
RUN set -xe ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		for server in 			ha.pool.sks-keyservers.net 			p80.pool.sks-keyservers.net:80 			ipv4.pool.sks-keyservers.net 			pgp.mit.edu ; 		do 			if gpg --batch --keyserver "$server" --recv-keys "$key"; then 				break; 			fi; 		done; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	mkdir -p "$TMPDIR" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Thu, 19 Nov 2020 08:10:53 GMT
WORKDIR /var/lib/jetty
# Thu, 19 Nov 2020 08:10:53 GMT
COPY multi:aa77a0f6aef2add1a97bf742e5d8ca9322cda3f66ea7673ea49c33da7e5b0889 in / 
# Thu, 19 Nov 2020 08:10:54 GMT
USER jetty
# Thu, 19 Nov 2020 08:10:54 GMT
EXPOSE 8080
# Thu, 19 Nov 2020 08:10:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 19 Nov 2020 08:10:54 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Thu, 19 Nov 2020 09:18:42 GMT
ENV DATA_DIR=/catalogue-data
# Thu, 19 Nov 2020 09:18:43 GMT
ENV JAVA_OPTS=-Dorg.eclipse.jetty.annotations.AnnotationParser.LEVEL=OFF         -Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC         -Dgeonetwork.resources.dir=/catalogue-data/resources         -Dgeonetwork.data.dir=/catalogue-data         -Dgeonetwork.codeList.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/codelist         -Dgeonetwork.schema.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/schema_plugins
# Thu, 19 Nov 2020 09:18:43 GMT
USER root
# Thu, 19 Nov 2020 09:18:47 GMT
RUN apt-get -y update &&     apt-get -y install curl &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p /${DATA_DIR} &&     chown -R jetty:jetty ${DATA_DIR} &&     mkdir -p /var/lib/jetty/webapps/geonetwork &&     chown -R jetty:jetty /var/lib/jetty/webapps/geonetwork
# Thu, 19 Nov 2020 09:18:48 GMT
USER jetty
# Thu, 19 Nov 2020 09:18:48 GMT
ENV GN_FILE=GeoNetwork-4.0.1-0.war
# Thu, 19 Nov 2020 09:18:48 GMT
ENV GN_VERSION=4.0.1
# Thu, 19 Nov 2020 09:18:48 GMT
ENV GN_DOWNLOAD_MD5=e9c885de19644856d855c0ea78052b12
# Thu, 19 Nov 2020 09:25:09 GMT
RUN cd /var/lib/jetty/webapps/geonetwork/ &&     curl -fSL -o geonetwork.war      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c &&      unzip -q geonetwork.war &&      rm geonetwork.war
# Thu, 19 Nov 2020 09:25:09 GMT
COPY file:ca46ab251df3dfc253cb04cf962e7266e42428fab31ad2f583a7c86b06d5f778 in /geonetwork-entrypoint.sh 
# Thu, 19 Nov 2020 09:25:09 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Thu, 19 Nov 2020 09:25:10 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Thu, 19 Nov 2020 09:25:10 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:756975cb9c7e7933d824af9319b512dd72a50894232761d06ef3be59981df838`  
		Last Modified: Tue, 17 Nov 2020 20:27:06 GMT  
		Size: 50.4 MB (50397725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77915b4e630d47296770ce4cf481894885978072432456615172af463433cc5`  
		Last Modified: Wed, 18 Nov 2020 00:49:42 GMT  
		Size: 7.8 MB (7811717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f37a0a41b6b03489dd7de0aa2a79e369fd8b219bbc36b52f3f9790dc128e74b`  
		Last Modified: Wed, 18 Nov 2020 00:49:42 GMT  
		Size: 10.0 MB (9996233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:713f7746108e0e07f616eec5ac22de7d9981c7e5087a3d63d92193b71d3e98e3`  
		Last Modified: Thu, 19 Nov 2020 03:12:18 GMT  
		Size: 5.5 MB (5529433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba38f0ad15ed007b8974fb97b174e2f3e0418a49a03c215e237812c058006714`  
		Last Modified: Thu, 19 Nov 2020 03:12:53 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aef0ecdbb4512b269e1df4a3a65f0ff50bbfbdbfe16779256f3f3954f36eb61b`  
		Last Modified: Thu, 19 Nov 2020 03:12:58 GMT  
		Size: 41.3 MB (41301352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c767072a31fb49fa5ec3f5d0f4b2ca6d3e04b4ef754b9b7fd71d0fa5447a441`  
		Last Modified: Thu, 19 Nov 2020 08:13:07 GMT  
		Size: 9.8 MB (9769134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c78e45ba22d7119a5b75d071e6ef1f9b80b2dfd6417e93a735629b5dab0fb706`  
		Last Modified: Thu, 19 Nov 2020 08:13:05 GMT  
		Size: 1.4 KB (1450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:533b056ffb8af9013fc3139e24823323cb094906b2806c0d2c44bf2b0fd287ad`  
		Last Modified: Thu, 19 Nov 2020 09:26:34 GMT  
		Size: 466.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:795a6fe00ffbb6dbafddade9a45c8e68a7dea98e2ba0827d8b80b2ba70ed8fe3`  
		Last Modified: Thu, 19 Nov 2020 09:26:54 GMT  
		Size: 291.4 MB (291358257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be1be42981519abedd791e8c2637ac927ba30a0b879356ed0840bcee2c37e7b0`  
		Last Modified: Thu, 19 Nov 2020 09:26:35 GMT  
		Size: 959.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `geonetwork:4.0.1`

```console
$ docker pull geonetwork@sha256:415c652d5a4623888973c0c57bf3c7be7476b838fb61ea75cf798d365df999d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `geonetwork:4.0.1` - linux; amd64

```console
$ docker pull geonetwork@sha256:d941c9f58436cc5c29aa15078b0ce1430992b3d276c04d47076c535855dc389b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **416.2 MB (416166939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3867e0339e7768d88d73b9a96f618540991fcc24ed516f3a0329a30b2c16463`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 17 Nov 2020 20:20:58 GMT
ADD file:9a4fd72d749f4a791e75e0f6fc6028d0771e3381b6d84a8d0b07a4887bc7c641 in / 
# Tue, 17 Nov 2020 20:20:58 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 00:30:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 00:30:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 19 Nov 2020 03:06:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 19 Nov 2020 03:06:45 GMT
ENV LANG=C.UTF-8
# Thu, 19 Nov 2020 03:07:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 19 Nov 2020 03:07:31 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Nov 2020 03:07:32 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 19 Nov 2020 03:07:32 GMT
ENV JAVA_VERSION=8u275
# Thu, 19 Nov 2020 03:07:38 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u275-b01/OpenJDK8U-jre_x64_linux_8u275b01.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 19 Nov 2020 08:10:48 GMT
ENV JETTY_VERSION=9.4.34.v20201102
# Thu, 19 Nov 2020 08:10:49 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 19 Nov 2020 08:10:49 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 19 Nov 2020 08:10:49 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 19 Nov 2020 08:10:49 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Nov 2020 08:10:49 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.34.v20201102/jetty-home-9.4.34.v20201102.tar.gz
# Thu, 19 Nov 2020 08:10:50 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E 	F254B35617DC255D9344BCFA873A8E86B4372146
# Thu, 19 Nov 2020 08:10:53 GMT
RUN set -xe ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		for server in 			ha.pool.sks-keyservers.net 			p80.pool.sks-keyservers.net:80 			ipv4.pool.sks-keyservers.net 			pgp.mit.edu ; 		do 			if gpg --batch --keyserver "$server" --recv-keys "$key"; then 				break; 			fi; 		done; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	mkdir -p "$TMPDIR" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Thu, 19 Nov 2020 08:10:53 GMT
WORKDIR /var/lib/jetty
# Thu, 19 Nov 2020 08:10:53 GMT
COPY multi:aa77a0f6aef2add1a97bf742e5d8ca9322cda3f66ea7673ea49c33da7e5b0889 in / 
# Thu, 19 Nov 2020 08:10:54 GMT
USER jetty
# Thu, 19 Nov 2020 08:10:54 GMT
EXPOSE 8080
# Thu, 19 Nov 2020 08:10:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 19 Nov 2020 08:10:54 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Thu, 19 Nov 2020 09:18:42 GMT
ENV DATA_DIR=/catalogue-data
# Thu, 19 Nov 2020 09:18:43 GMT
ENV JAVA_OPTS=-Dorg.eclipse.jetty.annotations.AnnotationParser.LEVEL=OFF         -Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC         -Dgeonetwork.resources.dir=/catalogue-data/resources         -Dgeonetwork.data.dir=/catalogue-data         -Dgeonetwork.codeList.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/codelist         -Dgeonetwork.schema.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/schema_plugins
# Thu, 19 Nov 2020 09:18:43 GMT
USER root
# Thu, 19 Nov 2020 09:18:47 GMT
RUN apt-get -y update &&     apt-get -y install curl &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p /${DATA_DIR} &&     chown -R jetty:jetty ${DATA_DIR} &&     mkdir -p /var/lib/jetty/webapps/geonetwork &&     chown -R jetty:jetty /var/lib/jetty/webapps/geonetwork
# Thu, 19 Nov 2020 09:18:48 GMT
USER jetty
# Thu, 19 Nov 2020 09:18:48 GMT
ENV GN_FILE=GeoNetwork-4.0.1-0.war
# Thu, 19 Nov 2020 09:18:48 GMT
ENV GN_VERSION=4.0.1
# Thu, 19 Nov 2020 09:18:48 GMT
ENV GN_DOWNLOAD_MD5=e9c885de19644856d855c0ea78052b12
# Thu, 19 Nov 2020 09:25:09 GMT
RUN cd /var/lib/jetty/webapps/geonetwork/ &&     curl -fSL -o geonetwork.war      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c &&      unzip -q geonetwork.war &&      rm geonetwork.war
# Thu, 19 Nov 2020 09:25:09 GMT
COPY file:ca46ab251df3dfc253cb04cf962e7266e42428fab31ad2f583a7c86b06d5f778 in /geonetwork-entrypoint.sh 
# Thu, 19 Nov 2020 09:25:09 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Thu, 19 Nov 2020 09:25:10 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Thu, 19 Nov 2020 09:25:10 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:756975cb9c7e7933d824af9319b512dd72a50894232761d06ef3be59981df838`  
		Last Modified: Tue, 17 Nov 2020 20:27:06 GMT  
		Size: 50.4 MB (50397725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77915b4e630d47296770ce4cf481894885978072432456615172af463433cc5`  
		Last Modified: Wed, 18 Nov 2020 00:49:42 GMT  
		Size: 7.8 MB (7811717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f37a0a41b6b03489dd7de0aa2a79e369fd8b219bbc36b52f3f9790dc128e74b`  
		Last Modified: Wed, 18 Nov 2020 00:49:42 GMT  
		Size: 10.0 MB (9996233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:713f7746108e0e07f616eec5ac22de7d9981c7e5087a3d63d92193b71d3e98e3`  
		Last Modified: Thu, 19 Nov 2020 03:12:18 GMT  
		Size: 5.5 MB (5529433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba38f0ad15ed007b8974fb97b174e2f3e0418a49a03c215e237812c058006714`  
		Last Modified: Thu, 19 Nov 2020 03:12:53 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aef0ecdbb4512b269e1df4a3a65f0ff50bbfbdbfe16779256f3f3954f36eb61b`  
		Last Modified: Thu, 19 Nov 2020 03:12:58 GMT  
		Size: 41.3 MB (41301352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c767072a31fb49fa5ec3f5d0f4b2ca6d3e04b4ef754b9b7fd71d0fa5447a441`  
		Last Modified: Thu, 19 Nov 2020 08:13:07 GMT  
		Size: 9.8 MB (9769134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c78e45ba22d7119a5b75d071e6ef1f9b80b2dfd6417e93a735629b5dab0fb706`  
		Last Modified: Thu, 19 Nov 2020 08:13:05 GMT  
		Size: 1.4 KB (1450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:533b056ffb8af9013fc3139e24823323cb094906b2806c0d2c44bf2b0fd287ad`  
		Last Modified: Thu, 19 Nov 2020 09:26:34 GMT  
		Size: 466.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:795a6fe00ffbb6dbafddade9a45c8e68a7dea98e2ba0827d8b80b2ba70ed8fe3`  
		Last Modified: Thu, 19 Nov 2020 09:26:54 GMT  
		Size: 291.4 MB (291358257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be1be42981519abedd791e8c2637ac927ba30a0b879356ed0840bcee2c37e7b0`  
		Last Modified: Thu, 19 Nov 2020 09:26:35 GMT  
		Size: 959.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `geonetwork:latest`

```console
$ docker pull geonetwork@sha256:098ee2562a602e183593356186aaab3e2a65aa036b861d7a0af97b4e47d58ef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `geonetwork:latest` - linux; amd64

```console
$ docker pull geonetwork@sha256:ddc1aac1b012c4070fadb10459d8b2fa191ddf1727184d77e988a745f7f69031
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **519.0 MB (519001392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b66a1d14df62e48874015a4c511892d6a7737f117702691d781c1160bcc18c73`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 17 Nov 2020 20:20:58 GMT
ADD file:9a4fd72d749f4a791e75e0f6fc6028d0771e3381b6d84a8d0b07a4887bc7c641 in / 
# Tue, 17 Nov 2020 20:20:58 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 00:30:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 00:30:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Nov 2020 00:31:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 19 Nov 2020 03:06:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 19 Nov 2020 03:06:07 GMT
ENV LANG=C.UTF-8
# Thu, 19 Nov 2020 03:07:06 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 19 Nov 2020 03:07:06 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Nov 2020 03:07:08 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 19 Nov 2020 03:07:08 GMT
ENV JAVA_VERSION=8u275
# Thu, 19 Nov 2020 03:07:19 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u275-b01/OpenJDK8U-jdk_x64_linux_8u275b01.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 19 Nov 2020 06:13:16 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 19 Nov 2020 06:13:16 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Nov 2020 06:13:17 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 19 Nov 2020 06:13:18 GMT
WORKDIR /usr/local/tomcat
# Thu, 19 Nov 2020 06:13:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 19 Nov 2020 06:13:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 19 Nov 2020 06:21:01 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 19 Nov 2020 06:21:01 GMT
ENV TOMCAT_MAJOR=8
# Thu, 19 Nov 2020 06:21:02 GMT
ENV TOMCAT_VERSION=8.5.60
# Thu, 19 Nov 2020 06:21:02 GMT
ENV TOMCAT_SHA512=460b4d0f2d445670b69ff97d4295628b9ce444c294e301b4c0c5e4c48b42bb1a642769f075dfe105b7d7257d9aba62b75a6ea5b6fb65487891ab23d7bb3d6140
# Thu, 19 Nov 2020 06:21:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 19 Nov 2020 06:21:33 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 19 Nov 2020 06:21:33 GMT
EXPOSE 8080
# Thu, 19 Nov 2020 06:21:34 GMT
CMD ["catalina.sh" "run"]
# Thu, 19 Nov 2020 09:05:08 GMT
ENV GN_FILE=geonetwork.war
# Thu, 19 Nov 2020 09:05:08 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Thu, 19 Nov 2020 09:05:09 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Thu, 19 Nov 2020 09:05:09 GMT
ENV GN_VERSION=3.10.5
# Thu, 19 Nov 2020 09:05:09 GMT
ENV GN_DOWNLOAD_MD5=63ffc3929e486e48c56b89b62da72813
# Thu, 19 Nov 2020 09:05:09 GMT
WORKDIR /usr/local/tomcat/webapps
# Thu, 19 Nov 2020 09:11:44 GMT
RUN curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "$GN_DOWNLOAD_MD5 *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE
# Thu, 19 Nov 2020 09:11:44 GMT
COPY file:0804862fd42c05f06dfa65cb1e5dad9a956d8ac6a3ddd4d962847ba159f5cfe6 in /entrypoint.sh 
# Thu, 19 Nov 2020 09:11:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 19 Nov 2020 09:11:44 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:756975cb9c7e7933d824af9319b512dd72a50894232761d06ef3be59981df838`  
		Last Modified: Tue, 17 Nov 2020 20:27:06 GMT  
		Size: 50.4 MB (50397725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77915b4e630d47296770ce4cf481894885978072432456615172af463433cc5`  
		Last Modified: Wed, 18 Nov 2020 00:49:42 GMT  
		Size: 7.8 MB (7811717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f37a0a41b6b03489dd7de0aa2a79e369fd8b219bbc36b52f3f9790dc128e74b`  
		Last Modified: Wed, 18 Nov 2020 00:49:42 GMT  
		Size: 10.0 MB (9996233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96b2c1e36db5f5910f58da2ca4f9311b0690810c7107fb055ee1541498b5061f`  
		Last Modified: Wed, 18 Nov 2020 00:50:25 GMT  
		Size: 51.8 MB (51829318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a2d52b526e253b306ae38d6b75645b6a1716888a0b5e4b85b4dd93df8843a6`  
		Last Modified: Thu, 19 Nov 2020 03:11:37 GMT  
		Size: 5.3 MB (5284715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a36defce609c2ec5a9cc77094704955c777946a68d0f517f2d2d8223dd6420`  
		Last Modified: Thu, 19 Nov 2020 03:12:33 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e2014d79b302bdc5c3c30f767dddf39b02d21608607deb53450c893636731c1`  
		Last Modified: Thu, 19 Nov 2020 03:12:44 GMT  
		Size: 105.9 MB (105883500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528f69e563774f04c70bd19d8d09d1f758bf238b9c163dbd6ad5f2082ce0f194`  
		Last Modified: Thu, 19 Nov 2020 06:25:29 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37b94cea6fdec640e12b21ce5b846e8c7591c1bbd3f73538221374767362460`  
		Last Modified: Thu, 19 Nov 2020 06:27:39 GMT  
		Size: 11.5 MB (11500367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f96b01204efdb3b57520912607f112501248b5be77fd986c6d397f367e290d66`  
		Last Modified: Thu, 19 Nov 2020 06:27:37 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc9ae91a589697b43d9db64c38773ffd09a978edf568ac3c744a793ec93490cb`  
		Last Modified: Thu, 19 Nov 2020 09:25:48 GMT  
		Size: 276.3 MB (276297086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:375e55e6c143afbab56977401d0c13f62c15fcf1d0c5b54bf141acef29bc3c94`  
		Last Modified: Thu, 19 Nov 2020 09:25:28 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `geonetwork:postgres`

```console
$ docker pull geonetwork@sha256:a370092791facbc5e807f4b7b3b59996741cdce5b3a43f0d80c6fb9bf434399a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `geonetwork:postgres` - linux; amd64

```console
$ docker pull geonetwork@sha256:197f62a106d8cf980ccade87705c14e75ca756e51a82d40268b3f8d14bab27de
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.8 MB (530813056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8082cf9604ffc803448d1271c9277b539523e0b381fc42db9a9e91fb5b22c35b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 17 Nov 2020 20:20:58 GMT
ADD file:9a4fd72d749f4a791e75e0f6fc6028d0771e3381b6d84a8d0b07a4887bc7c641 in / 
# Tue, 17 Nov 2020 20:20:58 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 00:30:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 00:30:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Nov 2020 00:31:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 19 Nov 2020 03:06:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 19 Nov 2020 03:06:07 GMT
ENV LANG=C.UTF-8
# Thu, 19 Nov 2020 03:07:06 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 19 Nov 2020 03:07:06 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Nov 2020 03:07:08 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 19 Nov 2020 03:07:08 GMT
ENV JAVA_VERSION=8u275
# Thu, 19 Nov 2020 03:07:19 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u275-b01/OpenJDK8U-jdk_x64_linux_8u275b01.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 19 Nov 2020 06:13:16 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 19 Nov 2020 06:13:16 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Nov 2020 06:13:17 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 19 Nov 2020 06:13:18 GMT
WORKDIR /usr/local/tomcat
# Thu, 19 Nov 2020 06:13:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 19 Nov 2020 06:13:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 19 Nov 2020 06:21:01 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 19 Nov 2020 06:21:01 GMT
ENV TOMCAT_MAJOR=8
# Thu, 19 Nov 2020 06:21:02 GMT
ENV TOMCAT_VERSION=8.5.60
# Thu, 19 Nov 2020 06:21:02 GMT
ENV TOMCAT_SHA512=460b4d0f2d445670b69ff97d4295628b9ce444c294e301b4c0c5e4c48b42bb1a642769f075dfe105b7d7257d9aba62b75a6ea5b6fb65487891ab23d7bb3d6140
# Thu, 19 Nov 2020 06:21:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 19 Nov 2020 06:21:33 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 19 Nov 2020 06:21:33 GMT
EXPOSE 8080
# Thu, 19 Nov 2020 06:21:34 GMT
CMD ["catalina.sh" "run"]
# Thu, 19 Nov 2020 09:05:08 GMT
ENV GN_FILE=geonetwork.war
# Thu, 19 Nov 2020 09:05:08 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Thu, 19 Nov 2020 09:05:09 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Thu, 19 Nov 2020 09:05:09 GMT
ENV GN_VERSION=3.10.5
# Thu, 19 Nov 2020 09:05:09 GMT
ENV GN_DOWNLOAD_MD5=63ffc3929e486e48c56b89b62da72813
# Thu, 19 Nov 2020 09:05:09 GMT
WORKDIR /usr/local/tomcat/webapps
# Thu, 19 Nov 2020 09:11:44 GMT
RUN curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "$GN_DOWNLOAD_MD5 *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE
# Thu, 19 Nov 2020 09:11:44 GMT
COPY file:0804862fd42c05f06dfa65cb1e5dad9a956d8ac6a3ddd4d962847ba159f5cfe6 in /entrypoint.sh 
# Thu, 19 Nov 2020 09:11:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 19 Nov 2020 09:11:44 GMT
CMD ["catalina.sh" "run"]
# Thu, 19 Nov 2020 09:12:10 GMT
RUN apt-get update && apt-get install -y postgresql-client &&     rm -rf /var/lib/apt/lists/*
# Thu, 19 Nov 2020 09:12:11 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' $CATALINA_HOME/webapps/geonetwork/WEB-INF/config-node/srv.xml && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' $CATALINA_HOME/webapps/geonetwork/WEB-INF/config-node/srv.xml
# Thu, 19 Nov 2020 09:12:12 GMT
COPY file:83f69d2041e5fb378033b0db57e096c81ba0725102ab4da4f089685e748fcce3 in /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties 
# Thu, 19 Nov 2020 09:12:12 GMT
COPY file:c88411abba7ad9b7bb75019f08755dbfa163d2fc7fdd80676bf9350c4c56a19c in /entrypoint.sh 
# Thu, 19 Nov 2020 09:12:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 19 Nov 2020 09:12:12 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:756975cb9c7e7933d824af9319b512dd72a50894232761d06ef3be59981df838`  
		Last Modified: Tue, 17 Nov 2020 20:27:06 GMT  
		Size: 50.4 MB (50397725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77915b4e630d47296770ce4cf481894885978072432456615172af463433cc5`  
		Last Modified: Wed, 18 Nov 2020 00:49:42 GMT  
		Size: 7.8 MB (7811717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f37a0a41b6b03489dd7de0aa2a79e369fd8b219bbc36b52f3f9790dc128e74b`  
		Last Modified: Wed, 18 Nov 2020 00:49:42 GMT  
		Size: 10.0 MB (9996233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96b2c1e36db5f5910f58da2ca4f9311b0690810c7107fb055ee1541498b5061f`  
		Last Modified: Wed, 18 Nov 2020 00:50:25 GMT  
		Size: 51.8 MB (51829318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a2d52b526e253b306ae38d6b75645b6a1716888a0b5e4b85b4dd93df8843a6`  
		Last Modified: Thu, 19 Nov 2020 03:11:37 GMT  
		Size: 5.3 MB (5284715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a36defce609c2ec5a9cc77094704955c777946a68d0f517f2d2d8223dd6420`  
		Last Modified: Thu, 19 Nov 2020 03:12:33 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e2014d79b302bdc5c3c30f767dddf39b02d21608607deb53450c893636731c1`  
		Last Modified: Thu, 19 Nov 2020 03:12:44 GMT  
		Size: 105.9 MB (105883500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528f69e563774f04c70bd19d8d09d1f758bf238b9c163dbd6ad5f2082ce0f194`  
		Last Modified: Thu, 19 Nov 2020 06:25:29 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37b94cea6fdec640e12b21ce5b846e8c7591c1bbd3f73538221374767362460`  
		Last Modified: Thu, 19 Nov 2020 06:27:39 GMT  
		Size: 11.5 MB (11500367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f96b01204efdb3b57520912607f112501248b5be77fd986c6d397f367e290d66`  
		Last Modified: Thu, 19 Nov 2020 06:27:37 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc9ae91a589697b43d9db64c38773ffd09a978edf568ac3c744a793ec93490cb`  
		Last Modified: Thu, 19 Nov 2020 09:25:48 GMT  
		Size: 276.3 MB (276297086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:375e55e6c143afbab56977401d0c13f62c15fcf1d0c5b54bf141acef29bc3c94`  
		Last Modified: Thu, 19 Nov 2020 09:25:28 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de5f684135aed6842f15dc83ee246860033044ea0767a78718ef7283e8336669`  
		Last Modified: Thu, 19 Nov 2020 09:25:57 GMT  
		Size: 11.8 MB (11808303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bef6ec9d292f414f2e057c6a55cacd28f22d8b1b9ef170b9a49db40a2950e7b`  
		Last Modified: Thu, 19 Nov 2020 09:25:55 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31da2fecd2e76420600c49f08974869b84e1fd3e99a0138aa6bd7298d3d4d633`  
		Last Modified: Thu, 19 Nov 2020 09:25:55 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfad719ddee04927017bfa4fee2356d9aaa7683efc57708638a2e3c4df3b90a5`  
		Last Modified: Thu, 19 Nov 2020 09:25:55 GMT  
		Size: 974.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
