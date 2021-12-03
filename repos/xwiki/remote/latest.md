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
