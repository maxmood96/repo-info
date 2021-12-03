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
