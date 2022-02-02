<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `geonetwork`

-	[`geonetwork:3`](#geonetwork3)
-	[`geonetwork:3-postgres`](#geonetwork3-postgres)
-	[`geonetwork:3.10`](#geonetwork310)
-	[`geonetwork:3.10-postgres`](#geonetwork310-postgres)
-	[`geonetwork:3.10.10`](#geonetwork31010)
-	[`geonetwork:3.10.10-postgres`](#geonetwork31010-postgres)
-	[`geonetwork:3.12`](#geonetwork312)
-	[`geonetwork:3.12-postgres`](#geonetwork312-postgres)
-	[`geonetwork:3.12.3`](#geonetwork3123)
-	[`geonetwork:3.12.3-postgres`](#geonetwork3123-postgres)
-	[`geonetwork:4`](#geonetwork4)
-	[`geonetwork:4.0`](#geonetwork40)
-	[`geonetwork:4.0.6`](#geonetwork406)
-	[`geonetwork:latest`](#geonetworklatest)

## `geonetwork:3`

```console
$ docker pull geonetwork@sha256:37d5c95e4202a9b96f76622a28784e15ec7063bb7f3ccf42562f244319dd5c6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `geonetwork:3` - linux; amd64

```console
$ docker pull geonetwork@sha256:df817d01621765865a644f5556aab1e0210d3df49567e02d572833f1a9eefacd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **475.7 MB (475732709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c3a7abfc682cdda276a0be019a8b0880fcd6dd65fec545d5a523c9058e0e841`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:22 GMT
ADD file:9cca7f8e4abcd8309501cad216ff33a28932386ded66461a7591c0fdf2c859d3 in / 
# Wed, 26 Jan 2022 01:40:23 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:11:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:12:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Jan 2022 02:12:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:24:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:29:49 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 26 Jan 2022 09:29:50 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 26 Jan 2022 09:29:50 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 09:29:50 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jan 2022 09:29:50 GMT
ENV JAVA_VERSION=8u312
# Wed, 26 Jan 2022 09:30:47 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_x64_linux_8u312b07.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_aarch64_linux_8u312b07.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 27 Jan 2022 17:58:51 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 27 Jan 2022 17:58:51 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Jan 2022 17:58:52 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 27 Jan 2022 17:58:52 GMT
WORKDIR /usr/local/tomcat
# Thu, 27 Jan 2022 17:58:52 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 27 Jan 2022 17:58:52 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 27 Jan 2022 18:40:21 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 27 Jan 2022 18:40:22 GMT
ENV TOMCAT_MAJOR=8
# Thu, 27 Jan 2022 18:40:22 GMT
ENV TOMCAT_VERSION=8.5.75
# Thu, 27 Jan 2022 18:40:22 GMT
ENV TOMCAT_SHA512=b86d191506f8a647e3f4505bb7cc095068abb26bb4283562924913606514ce15930a467bd5d20c09b11d785827bf1914ed869b48dfb1c95e9f826e4c8b4e8aaa
# Thu, 27 Jan 2022 18:41:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 27 Jan 2022 18:41:49 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 27 Jan 2022 18:41:49 GMT
EXPOSE 8080
# Thu, 27 Jan 2022 18:41:49 GMT
CMD ["catalina.sh" "run"]
# Fri, 28 Jan 2022 00:29:11 GMT
ENV GN_FILE=geonetwork.war
# Fri, 28 Jan 2022 00:29:11 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Fri, 28 Jan 2022 00:29:11 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Fri, 28 Jan 2022 00:30:29 GMT
ENV GN_VERSION=3.12.3
# Fri, 28 Jan 2022 00:30:29 GMT
ENV GN_DOWNLOAD_MD5=ecbbff832c8a6edf22e06aa1870dddab
# Fri, 28 Jan 2022 00:30:29 GMT
WORKDIR /usr/local/tomcat/webapps
# Fri, 28 Jan 2022 01:14:38 GMT
RUN curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE
# Fri, 28 Jan 2022 01:14:39 GMT
COPY file:0804862fd42c05f06dfa65cb1e5dad9a956d8ac6a3ddd4d962847ba159f5cfe6 in /entrypoint.sh 
# Fri, 28 Jan 2022 01:14:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 28 Jan 2022 01:14:39 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:0c6b8ff8c37e92eb1ca65ed8917e818927d5bf318b6f18896049b5d9afc28343`  
		Last Modified: Wed, 26 Jan 2022 01:46:07 GMT  
		Size: 54.9 MB (54917164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:412caad352a3ecbb29c080379407ae0761e7b9b454f7239cbfd1d1da25e06b29`  
		Last Modified: Wed, 26 Jan 2022 02:22:09 GMT  
		Size: 5.2 MB (5152685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6d3e61f7a504fa66d7275123969e9917570188650eb84b2280a726b996040f6`  
		Last Modified: Wed, 26 Jan 2022 02:22:09 GMT  
		Size: 10.9 MB (10871783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:461bb1d8c517c7f9fc0f1df66c9dc34c85a23421c1e1c540b2e28cbb258e75f5`  
		Last Modified: Wed, 26 Jan 2022 02:22:32 GMT  
		Size: 54.6 MB (54567492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e442ee9d8dd9896a5b3b67117060f2af4ae8e997af7297009e7d0ea4b6595163`  
		Last Modified: Wed, 26 Jan 2022 09:50:58 GMT  
		Size: 5.4 MB (5420014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b5bcea956cbbcc7e16356354d5eb4b5b3834a43d708ca6c3fd048f33ddc579`  
		Last Modified: Wed, 26 Jan 2022 09:55:46 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3879cb950b1f93eff09fbecc9c1d4ed3760d3f81df96b99f8090e3955578b57`  
		Last Modified: Wed, 26 Jan 2022 09:55:59 GMT  
		Size: 106.0 MB (105999002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49e3fbddb891d992809b3882c1be86760359a997fbf71f9d2d67e30abc94e65`  
		Last Modified: Thu, 27 Jan 2022 19:16:46 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7bfbc34820025e3023401808fdd9dafc703b563ec8ade714a62eaa3395acad5`  
		Last Modified: Thu, 27 Jan 2022 19:35:44 GMT  
		Size: 11.5 MB (11531982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79726cf7f4f515d435cfde8dfaa18fedb5bdfe4edc28d01da89154106b32d77`  
		Last Modified: Thu, 27 Jan 2022 19:35:43 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e535218eecde23bcc1cc7329cf505d83f2e401ff1edefc5bbc05e0d1a5d04b39`  
		Last Modified: Fri, 28 Jan 2022 01:16:11 GMT  
		Size: 227.3 MB (227271824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a1e69ef5f77af477dee27b039a9b6c5d65be2230110d76e5d501e5d9318bbf2`  
		Last Modified: Fri, 28 Jan 2022 01:15:58 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `geonetwork:3` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:d6b77812dd3c63935ac94786f3fde7a2625d9d19774b8f4b4947899183500165
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **473.1 MB (473081985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5d62bdccd0d9f540879a1f4effa87b0d183092355a9b20c7e386f5c45920af0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 26 Jan 2022 01:42:15 GMT
ADD file:b6338a9c3c2f8d7ba1a23dcb7a1389c7d0eab75a7489ef66f21c773be56aa9ed in / 
# Wed, 26 Jan 2022 01:42:16 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:13:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:13:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Jan 2022 02:13:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 05:56:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 06:00:46 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 26 Jan 2022 06:00:48 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 26 Jan 2022 06:00:48 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 06:00:49 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jan 2022 06:00:50 GMT
ENV JAVA_VERSION=8u312
# Wed, 26 Jan 2022 06:01:01 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_x64_linux_8u312b07.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_aarch64_linux_8u312b07.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Wed, 26 Jan 2022 23:58:42 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 26 Jan 2022 23:58:43 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 23:58:44 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 26 Jan 2022 23:58:45 GMT
WORKDIR /usr/local/tomcat
# Wed, 26 Jan 2022 23:58:46 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 26 Jan 2022 23:58:47 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 27 Jan 2022 00:24:40 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 27 Jan 2022 00:24:41 GMT
ENV TOMCAT_MAJOR=8
# Thu, 27 Jan 2022 00:24:42 GMT
ENV TOMCAT_VERSION=8.5.75
# Thu, 27 Jan 2022 00:24:43 GMT
ENV TOMCAT_SHA512=b86d191506f8a647e3f4505bb7cc095068abb26bb4283562924913606514ce15930a467bd5d20c09b11d785827bf1914ed869b48dfb1c95e9f826e4c8b4e8aaa
# Thu, 27 Jan 2022 00:25:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 27 Jan 2022 00:25:48 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 27 Jan 2022 00:25:49 GMT
EXPOSE 8080
# Thu, 27 Jan 2022 00:25:50 GMT
CMD ["catalina.sh" "run"]
# Thu, 27 Jan 2022 05:09:51 GMT
ENV GN_FILE=geonetwork.war
# Thu, 27 Jan 2022 05:09:52 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Thu, 27 Jan 2022 05:09:52 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Thu, 27 Jan 2022 05:12:18 GMT
ENV GN_VERSION=3.12.3
# Thu, 27 Jan 2022 05:12:18 GMT
ENV GN_DOWNLOAD_MD5=ecbbff832c8a6edf22e06aa1870dddab
# Thu, 27 Jan 2022 05:12:19 GMT
WORKDIR /usr/local/tomcat/webapps
# Thu, 27 Jan 2022 05:15:06 GMT
RUN curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE
# Thu, 27 Jan 2022 05:15:08 GMT
COPY file:0804862fd42c05f06dfa65cb1e5dad9a956d8ac6a3ddd4d962847ba159f5cfe6 in /entrypoint.sh 
# Thu, 27 Jan 2022 05:15:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Jan 2022 05:15:09 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:39ab78bc09e79a21f719ced771689354d1948f4afd57e86afed8dac6ffb47826`  
		Last Modified: Wed, 26 Jan 2022 01:48:34 GMT  
		Size: 53.6 MB (53608848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cf88d09fc28807e643d4f619b2e0c559aaeddc7d7b8176e1144b065d63fa160`  
		Last Modified: Wed, 26 Jan 2022 02:23:47 GMT  
		Size: 5.1 MB (5141567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e019dd0368ba992803442a16cc7792c1bd5a3d06c3a1ae6fae17cb838822fb4c`  
		Last Modified: Wed, 26 Jan 2022 02:23:48 GMT  
		Size: 10.7 MB (10655902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9f1769d50d3693321e1b48f527d9c920830ad24d931b642c116bf7823bed6a`  
		Last Modified: Wed, 26 Jan 2022 02:24:10 GMT  
		Size: 54.7 MB (54669460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5cb8edd8beada37ea034ed391c47dfd106ff9cc9fac852e0f52db0b063374f`  
		Last Modified: Wed, 26 Jan 2022 06:23:05 GMT  
		Size: 5.4 MB (5420184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3973acc73ccb4db4685136c67eb73dd02f02b1518d5381cf376d82710758caa`  
		Last Modified: Wed, 26 Jan 2022 06:28:15 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:568c3474f69d85e6c2c507e089aacb5f23548845e35e993a3df6640ca80a6a61`  
		Last Modified: Wed, 26 Jan 2022 06:28:29 GMT  
		Size: 105.0 MB (105010960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c750153dc133d7b7832882e2a1e214d7e796cd23f1e59adc71cca58bd106ca1`  
		Last Modified: Thu, 27 Jan 2022 00:58:36 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd36e2060fcb58cd13a8f07504a330d6a61dbcfed5e64d211f76c6d93998d54`  
		Last Modified: Thu, 27 Jan 2022 01:16:23 GMT  
		Size: 11.3 MB (11303628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b87cb97d3e30d47e944ad2b3e55d72ef881c77a8599f906591dd8c2fcc45f56`  
		Last Modified: Thu, 27 Jan 2022 05:20:11 GMT  
		Size: 227.3 MB (227270838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:881aba0954a8e117ca330b1e1b047aa39075276fc7db40142388ccbfb0ec034f`  
		Last Modified: Thu, 27 Jan 2022 05:19:53 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `geonetwork:3-postgres`

```console
$ docker pull geonetwork@sha256:7f7959c4395c6853a248dad867133f75a1df647c527f901f61d92eebf419c040
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `geonetwork:3-postgres` - linux; amd64

```console
$ docker pull geonetwork@sha256:28be89ec28ce4bde3902d00a2cf87ec13a81bef5c6fcbeecf49ec2ae60e2103c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **479.2 MB (479239897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfc2f03558b5ccdb22ee9812d1022b2532fbf6177e6b3c87b57a8157601faf30`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:22 GMT
ADD file:9cca7f8e4abcd8309501cad216ff33a28932386ded66461a7591c0fdf2c859d3 in / 
# Wed, 26 Jan 2022 01:40:23 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:11:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:12:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Jan 2022 02:12:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:24:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:29:49 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 26 Jan 2022 09:29:50 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 26 Jan 2022 09:29:50 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 09:29:50 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jan 2022 09:29:50 GMT
ENV JAVA_VERSION=8u312
# Wed, 26 Jan 2022 09:30:47 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_x64_linux_8u312b07.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_aarch64_linux_8u312b07.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 27 Jan 2022 17:58:51 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 27 Jan 2022 17:58:51 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Jan 2022 17:58:52 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 27 Jan 2022 17:58:52 GMT
WORKDIR /usr/local/tomcat
# Thu, 27 Jan 2022 17:58:52 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 27 Jan 2022 17:58:52 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 27 Jan 2022 18:40:21 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 27 Jan 2022 18:40:22 GMT
ENV TOMCAT_MAJOR=8
# Thu, 27 Jan 2022 18:40:22 GMT
ENV TOMCAT_VERSION=8.5.75
# Thu, 27 Jan 2022 18:40:22 GMT
ENV TOMCAT_SHA512=b86d191506f8a647e3f4505bb7cc095068abb26bb4283562924913606514ce15930a467bd5d20c09b11d785827bf1914ed869b48dfb1c95e9f826e4c8b4e8aaa
# Thu, 27 Jan 2022 18:41:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 27 Jan 2022 18:41:49 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 27 Jan 2022 18:41:49 GMT
EXPOSE 8080
# Thu, 27 Jan 2022 18:41:49 GMT
CMD ["catalina.sh" "run"]
# Fri, 28 Jan 2022 00:29:11 GMT
ENV GN_FILE=geonetwork.war
# Fri, 28 Jan 2022 00:29:11 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Fri, 28 Jan 2022 00:29:11 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Fri, 28 Jan 2022 00:30:29 GMT
ENV GN_VERSION=3.12.3
# Fri, 28 Jan 2022 00:30:29 GMT
ENV GN_DOWNLOAD_MD5=ecbbff832c8a6edf22e06aa1870dddab
# Fri, 28 Jan 2022 00:30:29 GMT
WORKDIR /usr/local/tomcat/webapps
# Fri, 28 Jan 2022 01:14:38 GMT
RUN curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE
# Fri, 28 Jan 2022 01:14:39 GMT
COPY file:0804862fd42c05f06dfa65cb1e5dad9a956d8ac6a3ddd4d962847ba159f5cfe6 in /entrypoint.sh 
# Fri, 28 Jan 2022 01:14:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 28 Jan 2022 01:14:39 GMT
CMD ["catalina.sh" "run"]
# Fri, 28 Jan 2022 01:14:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jan 2022 01:14:56 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml"
# Fri, 28 Jan 2022 01:14:56 GMT
COPY file:83f69d2041e5fb378033b0db57e096c81ba0725102ab4da4f089685e748fcce3 in /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties 
# Fri, 28 Jan 2022 01:14:56 GMT
COPY file:c88411abba7ad9b7bb75019f08755dbfa163d2fc7fdd80676bf9350c4c56a19c in /entrypoint.sh 
# Fri, 28 Jan 2022 01:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 28 Jan 2022 01:14:57 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:0c6b8ff8c37e92eb1ca65ed8917e818927d5bf318b6f18896049b5d9afc28343`  
		Last Modified: Wed, 26 Jan 2022 01:46:07 GMT  
		Size: 54.9 MB (54917164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:412caad352a3ecbb29c080379407ae0761e7b9b454f7239cbfd1d1da25e06b29`  
		Last Modified: Wed, 26 Jan 2022 02:22:09 GMT  
		Size: 5.2 MB (5152685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6d3e61f7a504fa66d7275123969e9917570188650eb84b2280a726b996040f6`  
		Last Modified: Wed, 26 Jan 2022 02:22:09 GMT  
		Size: 10.9 MB (10871783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:461bb1d8c517c7f9fc0f1df66c9dc34c85a23421c1e1c540b2e28cbb258e75f5`  
		Last Modified: Wed, 26 Jan 2022 02:22:32 GMT  
		Size: 54.6 MB (54567492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e442ee9d8dd9896a5b3b67117060f2af4ae8e997af7297009e7d0ea4b6595163`  
		Last Modified: Wed, 26 Jan 2022 09:50:58 GMT  
		Size: 5.4 MB (5420014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b5bcea956cbbcc7e16356354d5eb4b5b3834a43d708ca6c3fd048f33ddc579`  
		Last Modified: Wed, 26 Jan 2022 09:55:46 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3879cb950b1f93eff09fbecc9c1d4ed3760d3f81df96b99f8090e3955578b57`  
		Last Modified: Wed, 26 Jan 2022 09:55:59 GMT  
		Size: 106.0 MB (105999002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49e3fbddb891d992809b3882c1be86760359a997fbf71f9d2d67e30abc94e65`  
		Last Modified: Thu, 27 Jan 2022 19:16:46 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7bfbc34820025e3023401808fdd9dafc703b563ec8ade714a62eaa3395acad5`  
		Last Modified: Thu, 27 Jan 2022 19:35:44 GMT  
		Size: 11.5 MB (11531982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79726cf7f4f515d435cfde8dfaa18fedb5bdfe4edc28d01da89154106b32d77`  
		Last Modified: Thu, 27 Jan 2022 19:35:43 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e535218eecde23bcc1cc7329cf505d83f2e401ff1edefc5bbc05e0d1a5d04b39`  
		Last Modified: Fri, 28 Jan 2022 01:16:11 GMT  
		Size: 227.3 MB (227271824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a1e69ef5f77af477dee27b039a9b6c5d65be2230110d76e5d501e5d9318bbf2`  
		Last Modified: Fri, 28 Jan 2022 01:15:58 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b62dadb210a914e3c38a325041dafe9c739465a9130cee94db462e7fd20a3f8`  
		Last Modified: Fri, 28 Jan 2022 01:16:27 GMT  
		Size: 3.5 MB (3503818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21d351266fb7a1d8cbf106d8b6aefece074dc5f0bff29d700ff4fe8cd5c4763d`  
		Last Modified: Fri, 28 Jan 2022 01:16:26 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48204bc4304fc8a091cd9be6d452b8e809475445582bcc3927c10d8a0c71472e`  
		Last Modified: Fri, 28 Jan 2022 01:16:26 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bea59ddb2568c53835bd9791ed31bc78fc5f3eac0c70888f1112c9791b34f4b`  
		Last Modified: Fri, 28 Jan 2022 01:16:26 GMT  
		Size: 973.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `geonetwork:3-postgres` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:f2773d655f2b71114be11fa5322a3af0776258caa1ef8f6da4957bc51674c471
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **476.3 MB (476346385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a381731898665b1e6e70b5c772c4364f76dc81a32043fb93ab4f908de0dc288e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 26 Jan 2022 01:42:15 GMT
ADD file:b6338a9c3c2f8d7ba1a23dcb7a1389c7d0eab75a7489ef66f21c773be56aa9ed in / 
# Wed, 26 Jan 2022 01:42:16 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:13:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:13:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Jan 2022 02:13:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 05:56:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 06:00:46 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 26 Jan 2022 06:00:48 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 26 Jan 2022 06:00:48 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 06:00:49 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jan 2022 06:00:50 GMT
ENV JAVA_VERSION=8u312
# Wed, 26 Jan 2022 06:01:01 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_x64_linux_8u312b07.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_aarch64_linux_8u312b07.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Wed, 26 Jan 2022 23:58:42 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 26 Jan 2022 23:58:43 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 23:58:44 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 26 Jan 2022 23:58:45 GMT
WORKDIR /usr/local/tomcat
# Wed, 26 Jan 2022 23:58:46 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 26 Jan 2022 23:58:47 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 27 Jan 2022 00:24:40 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 27 Jan 2022 00:24:41 GMT
ENV TOMCAT_MAJOR=8
# Thu, 27 Jan 2022 00:24:42 GMT
ENV TOMCAT_VERSION=8.5.75
# Thu, 27 Jan 2022 00:24:43 GMT
ENV TOMCAT_SHA512=b86d191506f8a647e3f4505bb7cc095068abb26bb4283562924913606514ce15930a467bd5d20c09b11d785827bf1914ed869b48dfb1c95e9f826e4c8b4e8aaa
# Thu, 27 Jan 2022 00:25:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 27 Jan 2022 00:25:48 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 27 Jan 2022 00:25:49 GMT
EXPOSE 8080
# Thu, 27 Jan 2022 00:25:50 GMT
CMD ["catalina.sh" "run"]
# Thu, 27 Jan 2022 05:09:51 GMT
ENV GN_FILE=geonetwork.war
# Thu, 27 Jan 2022 05:09:52 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Thu, 27 Jan 2022 05:09:52 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Thu, 27 Jan 2022 05:12:18 GMT
ENV GN_VERSION=3.12.3
# Thu, 27 Jan 2022 05:12:18 GMT
ENV GN_DOWNLOAD_MD5=ecbbff832c8a6edf22e06aa1870dddab
# Thu, 27 Jan 2022 05:12:19 GMT
WORKDIR /usr/local/tomcat/webapps
# Thu, 27 Jan 2022 05:15:06 GMT
RUN curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE
# Thu, 27 Jan 2022 05:15:08 GMT
COPY file:0804862fd42c05f06dfa65cb1e5dad9a956d8ac6a3ddd4d962847ba159f5cfe6 in /entrypoint.sh 
# Thu, 27 Jan 2022 05:15:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Jan 2022 05:15:09 GMT
CMD ["catalina.sh" "run"]
# Thu, 27 Jan 2022 05:15:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/*
# Thu, 27 Jan 2022 05:15:21 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml"
# Thu, 27 Jan 2022 05:15:22 GMT
COPY file:83f69d2041e5fb378033b0db57e096c81ba0725102ab4da4f089685e748fcce3 in /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties 
# Thu, 27 Jan 2022 05:15:23 GMT
COPY file:c88411abba7ad9b7bb75019f08755dbfa163d2fc7fdd80676bf9350c4c56a19c in /entrypoint.sh 
# Thu, 27 Jan 2022 05:15:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Jan 2022 05:15:24 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:39ab78bc09e79a21f719ced771689354d1948f4afd57e86afed8dac6ffb47826`  
		Last Modified: Wed, 26 Jan 2022 01:48:34 GMT  
		Size: 53.6 MB (53608848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cf88d09fc28807e643d4f619b2e0c559aaeddc7d7b8176e1144b065d63fa160`  
		Last Modified: Wed, 26 Jan 2022 02:23:47 GMT  
		Size: 5.1 MB (5141567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e019dd0368ba992803442a16cc7792c1bd5a3d06c3a1ae6fae17cb838822fb4c`  
		Last Modified: Wed, 26 Jan 2022 02:23:48 GMT  
		Size: 10.7 MB (10655902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9f1769d50d3693321e1b48f527d9c920830ad24d931b642c116bf7823bed6a`  
		Last Modified: Wed, 26 Jan 2022 02:24:10 GMT  
		Size: 54.7 MB (54669460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5cb8edd8beada37ea034ed391c47dfd106ff9cc9fac852e0f52db0b063374f`  
		Last Modified: Wed, 26 Jan 2022 06:23:05 GMT  
		Size: 5.4 MB (5420184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3973acc73ccb4db4685136c67eb73dd02f02b1518d5381cf376d82710758caa`  
		Last Modified: Wed, 26 Jan 2022 06:28:15 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:568c3474f69d85e6c2c507e089aacb5f23548845e35e993a3df6640ca80a6a61`  
		Last Modified: Wed, 26 Jan 2022 06:28:29 GMT  
		Size: 105.0 MB (105010960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c750153dc133d7b7832882e2a1e214d7e796cd23f1e59adc71cca58bd106ca1`  
		Last Modified: Thu, 27 Jan 2022 00:58:36 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd36e2060fcb58cd13a8f07504a330d6a61dbcfed5e64d211f76c6d93998d54`  
		Last Modified: Thu, 27 Jan 2022 01:16:23 GMT  
		Size: 11.3 MB (11303628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b87cb97d3e30d47e944ad2b3e55d72ef881c77a8599f906591dd8c2fcc45f56`  
		Last Modified: Thu, 27 Jan 2022 05:20:11 GMT  
		Size: 227.3 MB (227270838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:881aba0954a8e117ca330b1e1b047aa39075276fc7db40142388ccbfb0ec034f`  
		Last Modified: Thu, 27 Jan 2022 05:19:53 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9acebe6860978760636fd588bac693eb4beee3543ef67ef8f25cd67f7a7457f2`  
		Last Modified: Thu, 27 Jan 2022 05:20:27 GMT  
		Size: 3.3 MB (3261038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4baea3b1d826a8a216f0f9797bd95394e946a085b38d7f33b924ac3baccb4210`  
		Last Modified: Thu, 27 Jan 2022 05:20:26 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb94c323bdb05fb1ee7b2dd60cf963d12b24caca02794520d8cc92ccebf402b4`  
		Last Modified: Thu, 27 Jan 2022 05:20:26 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b8e950e474e503d01784c3b407aa7e628e6ac77eef70c7b4d1d9ca995cd497e`  
		Last Modified: Thu, 27 Jan 2022 05:20:26 GMT  
		Size: 974.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `geonetwork:3.10`

```console
$ docker pull geonetwork@sha256:960974844d964fbed7a55526bcd1019f9c5548a0a8553df1c4360adc2815645b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `geonetwork:3.10` - linux; amd64

```console
$ docker pull geonetwork@sha256:93dae0c04627f6fcfbe20c325d2b402192d2107f0964a7668810bfe565639a72
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **444.1 MB (444117967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1dbf4b8bb6da4961e42973cb5105fca642a9bdfd3a3aedbe6727959fb415673`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:22 GMT
ADD file:9cca7f8e4abcd8309501cad216ff33a28932386ded66461a7591c0fdf2c859d3 in / 
# Wed, 26 Jan 2022 01:40:23 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:11:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:12:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Jan 2022 02:12:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:24:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:29:49 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 26 Jan 2022 09:29:50 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 26 Jan 2022 09:29:50 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 09:29:50 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jan 2022 09:29:50 GMT
ENV JAVA_VERSION=8u312
# Wed, 26 Jan 2022 09:30:47 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_x64_linux_8u312b07.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_aarch64_linux_8u312b07.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 27 Jan 2022 17:58:51 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 27 Jan 2022 17:58:51 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Jan 2022 17:58:52 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 27 Jan 2022 17:58:52 GMT
WORKDIR /usr/local/tomcat
# Thu, 27 Jan 2022 17:58:52 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 27 Jan 2022 17:58:52 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 27 Jan 2022 18:40:21 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 27 Jan 2022 18:40:22 GMT
ENV TOMCAT_MAJOR=8
# Thu, 27 Jan 2022 18:40:22 GMT
ENV TOMCAT_VERSION=8.5.75
# Thu, 27 Jan 2022 18:40:22 GMT
ENV TOMCAT_SHA512=b86d191506f8a647e3f4505bb7cc095068abb26bb4283562924913606514ce15930a467bd5d20c09b11d785827bf1914ed869b48dfb1c95e9f826e4c8b4e8aaa
# Thu, 27 Jan 2022 18:41:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 27 Jan 2022 18:41:49 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 27 Jan 2022 18:41:49 GMT
EXPOSE 8080
# Thu, 27 Jan 2022 18:41:49 GMT
CMD ["catalina.sh" "run"]
# Fri, 28 Jan 2022 00:29:11 GMT
ENV GN_FILE=geonetwork.war
# Fri, 28 Jan 2022 00:29:11 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Fri, 28 Jan 2022 00:29:11 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Fri, 28 Jan 2022 00:29:12 GMT
ENV GN_VERSION=3.10.10
# Fri, 28 Jan 2022 00:29:12 GMT
ENV GN_DOWNLOAD_MD5=de09ba1a43d6f3a224ad5ff02b4c4fb3
# Fri, 28 Jan 2022 00:29:12 GMT
ENV LOG4J_VERSION=2.17.1
# Fri, 28 Jan 2022 00:29:12 GMT
ENV LOG4J_SHA512=b7e948df6c6f57d903d990de2cc0270c1537b711285e9b6b91280db6ace38418fced713785b2c20512dd9a4238c2d1d0ceb414d9936df2ca110ff14993ae04dc
# Fri, 28 Jan 2022 00:29:13 GMT
WORKDIR /usr/local/tomcat/webapps
# Fri, 28 Jan 2022 01:13:36 GMT
RUN curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "$GN_DOWNLOAD_MD5 *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE &&      rm geonetwork/WEB-INF/lib/log4j-core-* &&      rm geonetwork/WEB-INF/lib/log4j-api* &&      curl -fSL -o apache-log4j-${LOG4J_VERSION}-bin.tar.gz "https://dlcdn.apache.org/logging/log4j/${LOG4J_VERSION}/apache-log4j-${LOG4J_VERSION}-bin.tar.gz" &&      echo "${LOG4J_SHA512} apache-log4j-${LOG4J_VERSION}-bin.tar.gz" | sha512sum -c &&      tar -xvzf apache-log4j-${LOG4J_VERSION}-bin.tar.gz &&      cp apache-log4j-${LOG4J_VERSION}-bin/log4j-core-${LOG4J_VERSION}.jar "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/lib/" &&      cp apache-log4j-${LOG4J_VERSION}-bin/log4j-api-${LOG4J_VERSION}.jar "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/lib/" &&      rm -rf apache-log4j-${LOG4J_VERSION}-bin*
# Fri, 28 Jan 2022 01:13:37 GMT
COPY file:0804862fd42c05f06dfa65cb1e5dad9a956d8ac6a3ddd4d962847ba159f5cfe6 in /entrypoint.sh 
# Fri, 28 Jan 2022 01:13:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 28 Jan 2022 01:13:37 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:0c6b8ff8c37e92eb1ca65ed8917e818927d5bf318b6f18896049b5d9afc28343`  
		Last Modified: Wed, 26 Jan 2022 01:46:07 GMT  
		Size: 54.9 MB (54917164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:412caad352a3ecbb29c080379407ae0761e7b9b454f7239cbfd1d1da25e06b29`  
		Last Modified: Wed, 26 Jan 2022 02:22:09 GMT  
		Size: 5.2 MB (5152685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6d3e61f7a504fa66d7275123969e9917570188650eb84b2280a726b996040f6`  
		Last Modified: Wed, 26 Jan 2022 02:22:09 GMT  
		Size: 10.9 MB (10871783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:461bb1d8c517c7f9fc0f1df66c9dc34c85a23421c1e1c540b2e28cbb258e75f5`  
		Last Modified: Wed, 26 Jan 2022 02:22:32 GMT  
		Size: 54.6 MB (54567492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e442ee9d8dd9896a5b3b67117060f2af4ae8e997af7297009e7d0ea4b6595163`  
		Last Modified: Wed, 26 Jan 2022 09:50:58 GMT  
		Size: 5.4 MB (5420014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b5bcea956cbbcc7e16356354d5eb4b5b3834a43d708ca6c3fd048f33ddc579`  
		Last Modified: Wed, 26 Jan 2022 09:55:46 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3879cb950b1f93eff09fbecc9c1d4ed3760d3f81df96b99f8090e3955578b57`  
		Last Modified: Wed, 26 Jan 2022 09:55:59 GMT  
		Size: 106.0 MB (105999002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49e3fbddb891d992809b3882c1be86760359a997fbf71f9d2d67e30abc94e65`  
		Last Modified: Thu, 27 Jan 2022 19:16:46 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7bfbc34820025e3023401808fdd9dafc703b563ec8ade714a62eaa3395acad5`  
		Last Modified: Thu, 27 Jan 2022 19:35:44 GMT  
		Size: 11.5 MB (11531982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79726cf7f4f515d435cfde8dfaa18fedb5bdfe4edc28d01da89154106b32d77`  
		Last Modified: Thu, 27 Jan 2022 19:35:43 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99ce8840adc65146127fda27ccbe7b20867b9d89c9967a0e10520d2ee11f09fe`  
		Last Modified: Fri, 28 Jan 2022 01:15:33 GMT  
		Size: 195.7 MB (195657080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e1b367fe97a69251f113c267a16902892314fe37e6377bc84d49df3e83f5ad4`  
		Last Modified: Fri, 28 Jan 2022 01:15:21 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `geonetwork:3.10` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:9dc0ac2a5ec22c89c7e93955fc0b732473660270a0ac394dd9150877b7ba38c8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **441.5 MB (441469744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cb48ed4757fd1ced823701f6a3625db32a7670b4cc6b796217cb9e81cc2a994`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 26 Jan 2022 01:42:15 GMT
ADD file:b6338a9c3c2f8d7ba1a23dcb7a1389c7d0eab75a7489ef66f21c773be56aa9ed in / 
# Wed, 26 Jan 2022 01:42:16 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:13:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:13:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Jan 2022 02:13:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 05:56:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 06:00:46 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 26 Jan 2022 06:00:48 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 26 Jan 2022 06:00:48 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 06:00:49 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jan 2022 06:00:50 GMT
ENV JAVA_VERSION=8u312
# Wed, 26 Jan 2022 06:01:01 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_x64_linux_8u312b07.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_aarch64_linux_8u312b07.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Wed, 26 Jan 2022 23:58:42 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 26 Jan 2022 23:58:43 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 23:58:44 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 26 Jan 2022 23:58:45 GMT
WORKDIR /usr/local/tomcat
# Wed, 26 Jan 2022 23:58:46 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 26 Jan 2022 23:58:47 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 27 Jan 2022 00:24:40 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 27 Jan 2022 00:24:41 GMT
ENV TOMCAT_MAJOR=8
# Thu, 27 Jan 2022 00:24:42 GMT
ENV TOMCAT_VERSION=8.5.75
# Thu, 27 Jan 2022 00:24:43 GMT
ENV TOMCAT_SHA512=b86d191506f8a647e3f4505bb7cc095068abb26bb4283562924913606514ce15930a467bd5d20c09b11d785827bf1914ed869b48dfb1c95e9f826e4c8b4e8aaa
# Thu, 27 Jan 2022 00:25:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 27 Jan 2022 00:25:48 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 27 Jan 2022 00:25:49 GMT
EXPOSE 8080
# Thu, 27 Jan 2022 00:25:50 GMT
CMD ["catalina.sh" "run"]
# Thu, 27 Jan 2022 05:09:51 GMT
ENV GN_FILE=geonetwork.war
# Thu, 27 Jan 2022 05:09:52 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Thu, 27 Jan 2022 05:09:52 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Thu, 27 Jan 2022 05:09:53 GMT
ENV GN_VERSION=3.10.10
# Thu, 27 Jan 2022 05:09:54 GMT
ENV GN_DOWNLOAD_MD5=de09ba1a43d6f3a224ad5ff02b4c4fb3
# Thu, 27 Jan 2022 05:09:55 GMT
ENV LOG4J_VERSION=2.17.1
# Thu, 27 Jan 2022 05:09:56 GMT
ENV LOG4J_SHA512=b7e948df6c6f57d903d990de2cc0270c1537b711285e9b6b91280db6ace38418fced713785b2c20512dd9a4238c2d1d0ceb414d9936df2ca110ff14993ae04dc
# Thu, 27 Jan 2022 05:09:57 GMT
WORKDIR /usr/local/tomcat/webapps
# Thu, 27 Jan 2022 05:11:44 GMT
RUN curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "$GN_DOWNLOAD_MD5 *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE &&      rm geonetwork/WEB-INF/lib/log4j-core-* &&      rm geonetwork/WEB-INF/lib/log4j-api* &&      curl -fSL -o apache-log4j-${LOG4J_VERSION}-bin.tar.gz "https://dlcdn.apache.org/logging/log4j/${LOG4J_VERSION}/apache-log4j-${LOG4J_VERSION}-bin.tar.gz" &&      echo "${LOG4J_SHA512} apache-log4j-${LOG4J_VERSION}-bin.tar.gz" | sha512sum -c &&      tar -xvzf apache-log4j-${LOG4J_VERSION}-bin.tar.gz &&      cp apache-log4j-${LOG4J_VERSION}-bin/log4j-core-${LOG4J_VERSION}.jar "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/lib/" &&      cp apache-log4j-${LOG4J_VERSION}-bin/log4j-api-${LOG4J_VERSION}.jar "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/lib/" &&      rm -rf apache-log4j-${LOG4J_VERSION}-bin*
# Thu, 27 Jan 2022 05:11:45 GMT
COPY file:0804862fd42c05f06dfa65cb1e5dad9a956d8ac6a3ddd4d962847ba159f5cfe6 in /entrypoint.sh 
# Thu, 27 Jan 2022 05:11:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Jan 2022 05:11:47 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:39ab78bc09e79a21f719ced771689354d1948f4afd57e86afed8dac6ffb47826`  
		Last Modified: Wed, 26 Jan 2022 01:48:34 GMT  
		Size: 53.6 MB (53608848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cf88d09fc28807e643d4f619b2e0c559aaeddc7d7b8176e1144b065d63fa160`  
		Last Modified: Wed, 26 Jan 2022 02:23:47 GMT  
		Size: 5.1 MB (5141567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e019dd0368ba992803442a16cc7792c1bd5a3d06c3a1ae6fae17cb838822fb4c`  
		Last Modified: Wed, 26 Jan 2022 02:23:48 GMT  
		Size: 10.7 MB (10655902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9f1769d50d3693321e1b48f527d9c920830ad24d931b642c116bf7823bed6a`  
		Last Modified: Wed, 26 Jan 2022 02:24:10 GMT  
		Size: 54.7 MB (54669460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5cb8edd8beada37ea034ed391c47dfd106ff9cc9fac852e0f52db0b063374f`  
		Last Modified: Wed, 26 Jan 2022 06:23:05 GMT  
		Size: 5.4 MB (5420184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3973acc73ccb4db4685136c67eb73dd02f02b1518d5381cf376d82710758caa`  
		Last Modified: Wed, 26 Jan 2022 06:28:15 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:568c3474f69d85e6c2c507e089aacb5f23548845e35e993a3df6640ca80a6a61`  
		Last Modified: Wed, 26 Jan 2022 06:28:29 GMT  
		Size: 105.0 MB (105010960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c750153dc133d7b7832882e2a1e214d7e796cd23f1e59adc71cca58bd106ca1`  
		Last Modified: Thu, 27 Jan 2022 00:58:36 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd36e2060fcb58cd13a8f07504a330d6a61dbcfed5e64d211f76c6d93998d54`  
		Last Modified: Thu, 27 Jan 2022 01:16:23 GMT  
		Size: 11.3 MB (11303628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1be15c1e58fe9530aae8d99555bb240e60ceafbd8c41fc14e13b9ff17894be7c`  
		Last Modified: Thu, 27 Jan 2022 05:19:29 GMT  
		Size: 195.7 MB (195658597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cdc01c6f942f2a1582083f5d361b03f10b6261e0e41b03804528aa3c66a74e2`  
		Last Modified: Thu, 27 Jan 2022 05:19:13 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `geonetwork:3.10-postgres`

```console
$ docker pull geonetwork@sha256:b1b8c32b61673c3d8a6915216f8af34d12a8e43157225dcd708eb4e666110a14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `geonetwork:3.10-postgres` - linux; amd64

```console
$ docker pull geonetwork@sha256:0c771d4dd89ac51d0541c04da4c74e288dcf24effc03bfd59242f89be13c5c82
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **447.6 MB (447625160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7699902282d7e6be3707b318659206ea2c2479efc0ded72aa9c5fe77c262452`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:22 GMT
ADD file:9cca7f8e4abcd8309501cad216ff33a28932386ded66461a7591c0fdf2c859d3 in / 
# Wed, 26 Jan 2022 01:40:23 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:11:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:12:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Jan 2022 02:12:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:24:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:29:49 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 26 Jan 2022 09:29:50 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 26 Jan 2022 09:29:50 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 09:29:50 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jan 2022 09:29:50 GMT
ENV JAVA_VERSION=8u312
# Wed, 26 Jan 2022 09:30:47 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_x64_linux_8u312b07.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_aarch64_linux_8u312b07.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 27 Jan 2022 17:58:51 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 27 Jan 2022 17:58:51 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Jan 2022 17:58:52 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 27 Jan 2022 17:58:52 GMT
WORKDIR /usr/local/tomcat
# Thu, 27 Jan 2022 17:58:52 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 27 Jan 2022 17:58:52 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 27 Jan 2022 18:40:21 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 27 Jan 2022 18:40:22 GMT
ENV TOMCAT_MAJOR=8
# Thu, 27 Jan 2022 18:40:22 GMT
ENV TOMCAT_VERSION=8.5.75
# Thu, 27 Jan 2022 18:40:22 GMT
ENV TOMCAT_SHA512=b86d191506f8a647e3f4505bb7cc095068abb26bb4283562924913606514ce15930a467bd5d20c09b11d785827bf1914ed869b48dfb1c95e9f826e4c8b4e8aaa
# Thu, 27 Jan 2022 18:41:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 27 Jan 2022 18:41:49 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 27 Jan 2022 18:41:49 GMT
EXPOSE 8080
# Thu, 27 Jan 2022 18:41:49 GMT
CMD ["catalina.sh" "run"]
# Fri, 28 Jan 2022 00:29:11 GMT
ENV GN_FILE=geonetwork.war
# Fri, 28 Jan 2022 00:29:11 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Fri, 28 Jan 2022 00:29:11 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Fri, 28 Jan 2022 00:29:12 GMT
ENV GN_VERSION=3.10.10
# Fri, 28 Jan 2022 00:29:12 GMT
ENV GN_DOWNLOAD_MD5=de09ba1a43d6f3a224ad5ff02b4c4fb3
# Fri, 28 Jan 2022 00:29:12 GMT
ENV LOG4J_VERSION=2.17.1
# Fri, 28 Jan 2022 00:29:12 GMT
ENV LOG4J_SHA512=b7e948df6c6f57d903d990de2cc0270c1537b711285e9b6b91280db6ace38418fced713785b2c20512dd9a4238c2d1d0ceb414d9936df2ca110ff14993ae04dc
# Fri, 28 Jan 2022 00:29:13 GMT
WORKDIR /usr/local/tomcat/webapps
# Fri, 28 Jan 2022 01:13:36 GMT
RUN curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "$GN_DOWNLOAD_MD5 *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE &&      rm geonetwork/WEB-INF/lib/log4j-core-* &&      rm geonetwork/WEB-INF/lib/log4j-api* &&      curl -fSL -o apache-log4j-${LOG4J_VERSION}-bin.tar.gz "https://dlcdn.apache.org/logging/log4j/${LOG4J_VERSION}/apache-log4j-${LOG4J_VERSION}-bin.tar.gz" &&      echo "${LOG4J_SHA512} apache-log4j-${LOG4J_VERSION}-bin.tar.gz" | sha512sum -c &&      tar -xvzf apache-log4j-${LOG4J_VERSION}-bin.tar.gz &&      cp apache-log4j-${LOG4J_VERSION}-bin/log4j-core-${LOG4J_VERSION}.jar "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/lib/" &&      cp apache-log4j-${LOG4J_VERSION}-bin/log4j-api-${LOG4J_VERSION}.jar "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/lib/" &&      rm -rf apache-log4j-${LOG4J_VERSION}-bin*
# Fri, 28 Jan 2022 01:13:37 GMT
COPY file:0804862fd42c05f06dfa65cb1e5dad9a956d8ac6a3ddd4d962847ba159f5cfe6 in /entrypoint.sh 
# Fri, 28 Jan 2022 01:13:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 28 Jan 2022 01:13:37 GMT
CMD ["catalina.sh" "run"]
# Fri, 28 Jan 2022 01:13:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jan 2022 01:13:49 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml"
# Fri, 28 Jan 2022 01:13:49 GMT
COPY file:83f69d2041e5fb378033b0db57e096c81ba0725102ab4da4f089685e748fcce3 in /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties 
# Fri, 28 Jan 2022 01:13:49 GMT
COPY file:c88411abba7ad9b7bb75019f08755dbfa163d2fc7fdd80676bf9350c4c56a19c in /entrypoint.sh 
# Fri, 28 Jan 2022 01:13:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 28 Jan 2022 01:13:50 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:0c6b8ff8c37e92eb1ca65ed8917e818927d5bf318b6f18896049b5d9afc28343`  
		Last Modified: Wed, 26 Jan 2022 01:46:07 GMT  
		Size: 54.9 MB (54917164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:412caad352a3ecbb29c080379407ae0761e7b9b454f7239cbfd1d1da25e06b29`  
		Last Modified: Wed, 26 Jan 2022 02:22:09 GMT  
		Size: 5.2 MB (5152685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6d3e61f7a504fa66d7275123969e9917570188650eb84b2280a726b996040f6`  
		Last Modified: Wed, 26 Jan 2022 02:22:09 GMT  
		Size: 10.9 MB (10871783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:461bb1d8c517c7f9fc0f1df66c9dc34c85a23421c1e1c540b2e28cbb258e75f5`  
		Last Modified: Wed, 26 Jan 2022 02:22:32 GMT  
		Size: 54.6 MB (54567492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e442ee9d8dd9896a5b3b67117060f2af4ae8e997af7297009e7d0ea4b6595163`  
		Last Modified: Wed, 26 Jan 2022 09:50:58 GMT  
		Size: 5.4 MB (5420014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b5bcea956cbbcc7e16356354d5eb4b5b3834a43d708ca6c3fd048f33ddc579`  
		Last Modified: Wed, 26 Jan 2022 09:55:46 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3879cb950b1f93eff09fbecc9c1d4ed3760d3f81df96b99f8090e3955578b57`  
		Last Modified: Wed, 26 Jan 2022 09:55:59 GMT  
		Size: 106.0 MB (105999002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49e3fbddb891d992809b3882c1be86760359a997fbf71f9d2d67e30abc94e65`  
		Last Modified: Thu, 27 Jan 2022 19:16:46 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7bfbc34820025e3023401808fdd9dafc703b563ec8ade714a62eaa3395acad5`  
		Last Modified: Thu, 27 Jan 2022 19:35:44 GMT  
		Size: 11.5 MB (11531982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79726cf7f4f515d435cfde8dfaa18fedb5bdfe4edc28d01da89154106b32d77`  
		Last Modified: Thu, 27 Jan 2022 19:35:43 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99ce8840adc65146127fda27ccbe7b20867b9d89c9967a0e10520d2ee11f09fe`  
		Last Modified: Fri, 28 Jan 2022 01:15:33 GMT  
		Size: 195.7 MB (195657080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e1b367fe97a69251f113c267a16902892314fe37e6377bc84d49df3e83f5ad4`  
		Last Modified: Fri, 28 Jan 2022 01:15:21 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d1bbbe799cc6f61d2e000c52fc1908f0047528f417be6555eb37d15444ee757`  
		Last Modified: Fri, 28 Jan 2022 01:15:46 GMT  
		Size: 3.5 MB (3503825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed733596b47210740bc32e2e51aa393ece16e09b10787eb216ecde9cb037b2bb`  
		Last Modified: Fri, 28 Jan 2022 01:15:46 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db80ffabf1db0652d73eecfdf0aa932566eb0ce279f95fc1e2cb12076e7c403d`  
		Last Modified: Fri, 28 Jan 2022 01:15:45 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d137fbf18a9dfe666c5e4653432b1d3d8c34e196b1df0865f7f896949904450`  
		Last Modified: Fri, 28 Jan 2022 01:15:45 GMT  
		Size: 973.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `geonetwork:3.10-postgres` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:e5b4f6cb75293ba0de2192b9dd04e17612df2196236ab9e2a0f09f2c4f7acc1b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **444.7 MB (444734096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5442994d3c9366ed518b8caa34abb403871f0765f03cefa7084a01fb0b970a6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 26 Jan 2022 01:42:15 GMT
ADD file:b6338a9c3c2f8d7ba1a23dcb7a1389c7d0eab75a7489ef66f21c773be56aa9ed in / 
# Wed, 26 Jan 2022 01:42:16 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:13:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:13:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Jan 2022 02:13:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 05:56:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 06:00:46 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 26 Jan 2022 06:00:48 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 26 Jan 2022 06:00:48 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 06:00:49 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jan 2022 06:00:50 GMT
ENV JAVA_VERSION=8u312
# Wed, 26 Jan 2022 06:01:01 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_x64_linux_8u312b07.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_aarch64_linux_8u312b07.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Wed, 26 Jan 2022 23:58:42 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 26 Jan 2022 23:58:43 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 23:58:44 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 26 Jan 2022 23:58:45 GMT
WORKDIR /usr/local/tomcat
# Wed, 26 Jan 2022 23:58:46 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 26 Jan 2022 23:58:47 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 27 Jan 2022 00:24:40 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 27 Jan 2022 00:24:41 GMT
ENV TOMCAT_MAJOR=8
# Thu, 27 Jan 2022 00:24:42 GMT
ENV TOMCAT_VERSION=8.5.75
# Thu, 27 Jan 2022 00:24:43 GMT
ENV TOMCAT_SHA512=b86d191506f8a647e3f4505bb7cc095068abb26bb4283562924913606514ce15930a467bd5d20c09b11d785827bf1914ed869b48dfb1c95e9f826e4c8b4e8aaa
# Thu, 27 Jan 2022 00:25:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 27 Jan 2022 00:25:48 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 27 Jan 2022 00:25:49 GMT
EXPOSE 8080
# Thu, 27 Jan 2022 00:25:50 GMT
CMD ["catalina.sh" "run"]
# Thu, 27 Jan 2022 05:09:51 GMT
ENV GN_FILE=geonetwork.war
# Thu, 27 Jan 2022 05:09:52 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Thu, 27 Jan 2022 05:09:52 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Thu, 27 Jan 2022 05:09:53 GMT
ENV GN_VERSION=3.10.10
# Thu, 27 Jan 2022 05:09:54 GMT
ENV GN_DOWNLOAD_MD5=de09ba1a43d6f3a224ad5ff02b4c4fb3
# Thu, 27 Jan 2022 05:09:55 GMT
ENV LOG4J_VERSION=2.17.1
# Thu, 27 Jan 2022 05:09:56 GMT
ENV LOG4J_SHA512=b7e948df6c6f57d903d990de2cc0270c1537b711285e9b6b91280db6ace38418fced713785b2c20512dd9a4238c2d1d0ceb414d9936df2ca110ff14993ae04dc
# Thu, 27 Jan 2022 05:09:57 GMT
WORKDIR /usr/local/tomcat/webapps
# Thu, 27 Jan 2022 05:11:44 GMT
RUN curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "$GN_DOWNLOAD_MD5 *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE &&      rm geonetwork/WEB-INF/lib/log4j-core-* &&      rm geonetwork/WEB-INF/lib/log4j-api* &&      curl -fSL -o apache-log4j-${LOG4J_VERSION}-bin.tar.gz "https://dlcdn.apache.org/logging/log4j/${LOG4J_VERSION}/apache-log4j-${LOG4J_VERSION}-bin.tar.gz" &&      echo "${LOG4J_SHA512} apache-log4j-${LOG4J_VERSION}-bin.tar.gz" | sha512sum -c &&      tar -xvzf apache-log4j-${LOG4J_VERSION}-bin.tar.gz &&      cp apache-log4j-${LOG4J_VERSION}-bin/log4j-core-${LOG4J_VERSION}.jar "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/lib/" &&      cp apache-log4j-${LOG4J_VERSION}-bin/log4j-api-${LOG4J_VERSION}.jar "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/lib/" &&      rm -rf apache-log4j-${LOG4J_VERSION}-bin*
# Thu, 27 Jan 2022 05:11:45 GMT
COPY file:0804862fd42c05f06dfa65cb1e5dad9a956d8ac6a3ddd4d962847ba159f5cfe6 in /entrypoint.sh 
# Thu, 27 Jan 2022 05:11:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Jan 2022 05:11:47 GMT
CMD ["catalina.sh" "run"]
# Thu, 27 Jan 2022 05:12:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/*
# Thu, 27 Jan 2022 05:12:09 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml"
# Thu, 27 Jan 2022 05:12:10 GMT
COPY file:83f69d2041e5fb378033b0db57e096c81ba0725102ab4da4f089685e748fcce3 in /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties 
# Thu, 27 Jan 2022 05:12:11 GMT
COPY file:c88411abba7ad9b7bb75019f08755dbfa163d2fc7fdd80676bf9350c4c56a19c in /entrypoint.sh 
# Thu, 27 Jan 2022 05:12:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Jan 2022 05:12:12 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:39ab78bc09e79a21f719ced771689354d1948f4afd57e86afed8dac6ffb47826`  
		Last Modified: Wed, 26 Jan 2022 01:48:34 GMT  
		Size: 53.6 MB (53608848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cf88d09fc28807e643d4f619b2e0c559aaeddc7d7b8176e1144b065d63fa160`  
		Last Modified: Wed, 26 Jan 2022 02:23:47 GMT  
		Size: 5.1 MB (5141567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e019dd0368ba992803442a16cc7792c1bd5a3d06c3a1ae6fae17cb838822fb4c`  
		Last Modified: Wed, 26 Jan 2022 02:23:48 GMT  
		Size: 10.7 MB (10655902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9f1769d50d3693321e1b48f527d9c920830ad24d931b642c116bf7823bed6a`  
		Last Modified: Wed, 26 Jan 2022 02:24:10 GMT  
		Size: 54.7 MB (54669460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5cb8edd8beada37ea034ed391c47dfd106ff9cc9fac852e0f52db0b063374f`  
		Last Modified: Wed, 26 Jan 2022 06:23:05 GMT  
		Size: 5.4 MB (5420184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3973acc73ccb4db4685136c67eb73dd02f02b1518d5381cf376d82710758caa`  
		Last Modified: Wed, 26 Jan 2022 06:28:15 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:568c3474f69d85e6c2c507e089aacb5f23548845e35e993a3df6640ca80a6a61`  
		Last Modified: Wed, 26 Jan 2022 06:28:29 GMT  
		Size: 105.0 MB (105010960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c750153dc133d7b7832882e2a1e214d7e796cd23f1e59adc71cca58bd106ca1`  
		Last Modified: Thu, 27 Jan 2022 00:58:36 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd36e2060fcb58cd13a8f07504a330d6a61dbcfed5e64d211f76c6d93998d54`  
		Last Modified: Thu, 27 Jan 2022 01:16:23 GMT  
		Size: 11.3 MB (11303628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1be15c1e58fe9530aae8d99555bb240e60ceafbd8c41fc14e13b9ff17894be7c`  
		Last Modified: Thu, 27 Jan 2022 05:19:29 GMT  
		Size: 195.7 MB (195658597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cdc01c6f942f2a1582083f5d361b03f10b6261e0e41b03804528aa3c66a74e2`  
		Last Modified: Thu, 27 Jan 2022 05:19:13 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba5757904131d07ee2dd8aa0efaac54ae74eabe4acae773ef79d5070390884f`  
		Last Modified: Thu, 27 Jan 2022 05:19:42 GMT  
		Size: 3.3 MB (3260983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f22c64a8cd1dfcadf29016415ede58e852732d52486444385d5116773f6f2d8`  
		Last Modified: Thu, 27 Jan 2022 05:19:42 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de67ae6e8a50f9014765bbc631096fd8d36e2f672a24ee3684248889684442e`  
		Last Modified: Thu, 27 Jan 2022 05:19:41 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5326143d47f5727b41f1dedc4c564f5a93f87842a9add39739bf921eb119ed8d`  
		Last Modified: Thu, 27 Jan 2022 05:19:41 GMT  
		Size: 973.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `geonetwork:3.10.10`

```console
$ docker pull geonetwork@sha256:960974844d964fbed7a55526bcd1019f9c5548a0a8553df1c4360adc2815645b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `geonetwork:3.10.10` - linux; amd64

```console
$ docker pull geonetwork@sha256:93dae0c04627f6fcfbe20c325d2b402192d2107f0964a7668810bfe565639a72
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **444.1 MB (444117967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1dbf4b8bb6da4961e42973cb5105fca642a9bdfd3a3aedbe6727959fb415673`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:22 GMT
ADD file:9cca7f8e4abcd8309501cad216ff33a28932386ded66461a7591c0fdf2c859d3 in / 
# Wed, 26 Jan 2022 01:40:23 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:11:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:12:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Jan 2022 02:12:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:24:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:29:49 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 26 Jan 2022 09:29:50 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 26 Jan 2022 09:29:50 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 09:29:50 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jan 2022 09:29:50 GMT
ENV JAVA_VERSION=8u312
# Wed, 26 Jan 2022 09:30:47 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_x64_linux_8u312b07.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_aarch64_linux_8u312b07.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 27 Jan 2022 17:58:51 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 27 Jan 2022 17:58:51 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Jan 2022 17:58:52 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 27 Jan 2022 17:58:52 GMT
WORKDIR /usr/local/tomcat
# Thu, 27 Jan 2022 17:58:52 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 27 Jan 2022 17:58:52 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 27 Jan 2022 18:40:21 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 27 Jan 2022 18:40:22 GMT
ENV TOMCAT_MAJOR=8
# Thu, 27 Jan 2022 18:40:22 GMT
ENV TOMCAT_VERSION=8.5.75
# Thu, 27 Jan 2022 18:40:22 GMT
ENV TOMCAT_SHA512=b86d191506f8a647e3f4505bb7cc095068abb26bb4283562924913606514ce15930a467bd5d20c09b11d785827bf1914ed869b48dfb1c95e9f826e4c8b4e8aaa
# Thu, 27 Jan 2022 18:41:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 27 Jan 2022 18:41:49 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 27 Jan 2022 18:41:49 GMT
EXPOSE 8080
# Thu, 27 Jan 2022 18:41:49 GMT
CMD ["catalina.sh" "run"]
# Fri, 28 Jan 2022 00:29:11 GMT
ENV GN_FILE=geonetwork.war
# Fri, 28 Jan 2022 00:29:11 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Fri, 28 Jan 2022 00:29:11 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Fri, 28 Jan 2022 00:29:12 GMT
ENV GN_VERSION=3.10.10
# Fri, 28 Jan 2022 00:29:12 GMT
ENV GN_DOWNLOAD_MD5=de09ba1a43d6f3a224ad5ff02b4c4fb3
# Fri, 28 Jan 2022 00:29:12 GMT
ENV LOG4J_VERSION=2.17.1
# Fri, 28 Jan 2022 00:29:12 GMT
ENV LOG4J_SHA512=b7e948df6c6f57d903d990de2cc0270c1537b711285e9b6b91280db6ace38418fced713785b2c20512dd9a4238c2d1d0ceb414d9936df2ca110ff14993ae04dc
# Fri, 28 Jan 2022 00:29:13 GMT
WORKDIR /usr/local/tomcat/webapps
# Fri, 28 Jan 2022 01:13:36 GMT
RUN curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "$GN_DOWNLOAD_MD5 *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE &&      rm geonetwork/WEB-INF/lib/log4j-core-* &&      rm geonetwork/WEB-INF/lib/log4j-api* &&      curl -fSL -o apache-log4j-${LOG4J_VERSION}-bin.tar.gz "https://dlcdn.apache.org/logging/log4j/${LOG4J_VERSION}/apache-log4j-${LOG4J_VERSION}-bin.tar.gz" &&      echo "${LOG4J_SHA512} apache-log4j-${LOG4J_VERSION}-bin.tar.gz" | sha512sum -c &&      tar -xvzf apache-log4j-${LOG4J_VERSION}-bin.tar.gz &&      cp apache-log4j-${LOG4J_VERSION}-bin/log4j-core-${LOG4J_VERSION}.jar "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/lib/" &&      cp apache-log4j-${LOG4J_VERSION}-bin/log4j-api-${LOG4J_VERSION}.jar "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/lib/" &&      rm -rf apache-log4j-${LOG4J_VERSION}-bin*
# Fri, 28 Jan 2022 01:13:37 GMT
COPY file:0804862fd42c05f06dfa65cb1e5dad9a956d8ac6a3ddd4d962847ba159f5cfe6 in /entrypoint.sh 
# Fri, 28 Jan 2022 01:13:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 28 Jan 2022 01:13:37 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:0c6b8ff8c37e92eb1ca65ed8917e818927d5bf318b6f18896049b5d9afc28343`  
		Last Modified: Wed, 26 Jan 2022 01:46:07 GMT  
		Size: 54.9 MB (54917164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:412caad352a3ecbb29c080379407ae0761e7b9b454f7239cbfd1d1da25e06b29`  
		Last Modified: Wed, 26 Jan 2022 02:22:09 GMT  
		Size: 5.2 MB (5152685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6d3e61f7a504fa66d7275123969e9917570188650eb84b2280a726b996040f6`  
		Last Modified: Wed, 26 Jan 2022 02:22:09 GMT  
		Size: 10.9 MB (10871783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:461bb1d8c517c7f9fc0f1df66c9dc34c85a23421c1e1c540b2e28cbb258e75f5`  
		Last Modified: Wed, 26 Jan 2022 02:22:32 GMT  
		Size: 54.6 MB (54567492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e442ee9d8dd9896a5b3b67117060f2af4ae8e997af7297009e7d0ea4b6595163`  
		Last Modified: Wed, 26 Jan 2022 09:50:58 GMT  
		Size: 5.4 MB (5420014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b5bcea956cbbcc7e16356354d5eb4b5b3834a43d708ca6c3fd048f33ddc579`  
		Last Modified: Wed, 26 Jan 2022 09:55:46 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3879cb950b1f93eff09fbecc9c1d4ed3760d3f81df96b99f8090e3955578b57`  
		Last Modified: Wed, 26 Jan 2022 09:55:59 GMT  
		Size: 106.0 MB (105999002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49e3fbddb891d992809b3882c1be86760359a997fbf71f9d2d67e30abc94e65`  
		Last Modified: Thu, 27 Jan 2022 19:16:46 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7bfbc34820025e3023401808fdd9dafc703b563ec8ade714a62eaa3395acad5`  
		Last Modified: Thu, 27 Jan 2022 19:35:44 GMT  
		Size: 11.5 MB (11531982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79726cf7f4f515d435cfde8dfaa18fedb5bdfe4edc28d01da89154106b32d77`  
		Last Modified: Thu, 27 Jan 2022 19:35:43 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99ce8840adc65146127fda27ccbe7b20867b9d89c9967a0e10520d2ee11f09fe`  
		Last Modified: Fri, 28 Jan 2022 01:15:33 GMT  
		Size: 195.7 MB (195657080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e1b367fe97a69251f113c267a16902892314fe37e6377bc84d49df3e83f5ad4`  
		Last Modified: Fri, 28 Jan 2022 01:15:21 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `geonetwork:3.10.10` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:9dc0ac2a5ec22c89c7e93955fc0b732473660270a0ac394dd9150877b7ba38c8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **441.5 MB (441469744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cb48ed4757fd1ced823701f6a3625db32a7670b4cc6b796217cb9e81cc2a994`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 26 Jan 2022 01:42:15 GMT
ADD file:b6338a9c3c2f8d7ba1a23dcb7a1389c7d0eab75a7489ef66f21c773be56aa9ed in / 
# Wed, 26 Jan 2022 01:42:16 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:13:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:13:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Jan 2022 02:13:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 05:56:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 06:00:46 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 26 Jan 2022 06:00:48 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 26 Jan 2022 06:00:48 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 06:00:49 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jan 2022 06:00:50 GMT
ENV JAVA_VERSION=8u312
# Wed, 26 Jan 2022 06:01:01 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_x64_linux_8u312b07.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_aarch64_linux_8u312b07.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Wed, 26 Jan 2022 23:58:42 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 26 Jan 2022 23:58:43 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 23:58:44 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 26 Jan 2022 23:58:45 GMT
WORKDIR /usr/local/tomcat
# Wed, 26 Jan 2022 23:58:46 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 26 Jan 2022 23:58:47 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 27 Jan 2022 00:24:40 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 27 Jan 2022 00:24:41 GMT
ENV TOMCAT_MAJOR=8
# Thu, 27 Jan 2022 00:24:42 GMT
ENV TOMCAT_VERSION=8.5.75
# Thu, 27 Jan 2022 00:24:43 GMT
ENV TOMCAT_SHA512=b86d191506f8a647e3f4505bb7cc095068abb26bb4283562924913606514ce15930a467bd5d20c09b11d785827bf1914ed869b48dfb1c95e9f826e4c8b4e8aaa
# Thu, 27 Jan 2022 00:25:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 27 Jan 2022 00:25:48 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 27 Jan 2022 00:25:49 GMT
EXPOSE 8080
# Thu, 27 Jan 2022 00:25:50 GMT
CMD ["catalina.sh" "run"]
# Thu, 27 Jan 2022 05:09:51 GMT
ENV GN_FILE=geonetwork.war
# Thu, 27 Jan 2022 05:09:52 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Thu, 27 Jan 2022 05:09:52 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Thu, 27 Jan 2022 05:09:53 GMT
ENV GN_VERSION=3.10.10
# Thu, 27 Jan 2022 05:09:54 GMT
ENV GN_DOWNLOAD_MD5=de09ba1a43d6f3a224ad5ff02b4c4fb3
# Thu, 27 Jan 2022 05:09:55 GMT
ENV LOG4J_VERSION=2.17.1
# Thu, 27 Jan 2022 05:09:56 GMT
ENV LOG4J_SHA512=b7e948df6c6f57d903d990de2cc0270c1537b711285e9b6b91280db6ace38418fced713785b2c20512dd9a4238c2d1d0ceb414d9936df2ca110ff14993ae04dc
# Thu, 27 Jan 2022 05:09:57 GMT
WORKDIR /usr/local/tomcat/webapps
# Thu, 27 Jan 2022 05:11:44 GMT
RUN curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "$GN_DOWNLOAD_MD5 *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE &&      rm geonetwork/WEB-INF/lib/log4j-core-* &&      rm geonetwork/WEB-INF/lib/log4j-api* &&      curl -fSL -o apache-log4j-${LOG4J_VERSION}-bin.tar.gz "https://dlcdn.apache.org/logging/log4j/${LOG4J_VERSION}/apache-log4j-${LOG4J_VERSION}-bin.tar.gz" &&      echo "${LOG4J_SHA512} apache-log4j-${LOG4J_VERSION}-bin.tar.gz" | sha512sum -c &&      tar -xvzf apache-log4j-${LOG4J_VERSION}-bin.tar.gz &&      cp apache-log4j-${LOG4J_VERSION}-bin/log4j-core-${LOG4J_VERSION}.jar "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/lib/" &&      cp apache-log4j-${LOG4J_VERSION}-bin/log4j-api-${LOG4J_VERSION}.jar "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/lib/" &&      rm -rf apache-log4j-${LOG4J_VERSION}-bin*
# Thu, 27 Jan 2022 05:11:45 GMT
COPY file:0804862fd42c05f06dfa65cb1e5dad9a956d8ac6a3ddd4d962847ba159f5cfe6 in /entrypoint.sh 
# Thu, 27 Jan 2022 05:11:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Jan 2022 05:11:47 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:39ab78bc09e79a21f719ced771689354d1948f4afd57e86afed8dac6ffb47826`  
		Last Modified: Wed, 26 Jan 2022 01:48:34 GMT  
		Size: 53.6 MB (53608848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cf88d09fc28807e643d4f619b2e0c559aaeddc7d7b8176e1144b065d63fa160`  
		Last Modified: Wed, 26 Jan 2022 02:23:47 GMT  
		Size: 5.1 MB (5141567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e019dd0368ba992803442a16cc7792c1bd5a3d06c3a1ae6fae17cb838822fb4c`  
		Last Modified: Wed, 26 Jan 2022 02:23:48 GMT  
		Size: 10.7 MB (10655902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9f1769d50d3693321e1b48f527d9c920830ad24d931b642c116bf7823bed6a`  
		Last Modified: Wed, 26 Jan 2022 02:24:10 GMT  
		Size: 54.7 MB (54669460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5cb8edd8beada37ea034ed391c47dfd106ff9cc9fac852e0f52db0b063374f`  
		Last Modified: Wed, 26 Jan 2022 06:23:05 GMT  
		Size: 5.4 MB (5420184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3973acc73ccb4db4685136c67eb73dd02f02b1518d5381cf376d82710758caa`  
		Last Modified: Wed, 26 Jan 2022 06:28:15 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:568c3474f69d85e6c2c507e089aacb5f23548845e35e993a3df6640ca80a6a61`  
		Last Modified: Wed, 26 Jan 2022 06:28:29 GMT  
		Size: 105.0 MB (105010960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c750153dc133d7b7832882e2a1e214d7e796cd23f1e59adc71cca58bd106ca1`  
		Last Modified: Thu, 27 Jan 2022 00:58:36 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd36e2060fcb58cd13a8f07504a330d6a61dbcfed5e64d211f76c6d93998d54`  
		Last Modified: Thu, 27 Jan 2022 01:16:23 GMT  
		Size: 11.3 MB (11303628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1be15c1e58fe9530aae8d99555bb240e60ceafbd8c41fc14e13b9ff17894be7c`  
		Last Modified: Thu, 27 Jan 2022 05:19:29 GMT  
		Size: 195.7 MB (195658597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cdc01c6f942f2a1582083f5d361b03f10b6261e0e41b03804528aa3c66a74e2`  
		Last Modified: Thu, 27 Jan 2022 05:19:13 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `geonetwork:3.10.10-postgres`

```console
$ docker pull geonetwork@sha256:b1b8c32b61673c3d8a6915216f8af34d12a8e43157225dcd708eb4e666110a14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `geonetwork:3.10.10-postgres` - linux; amd64

```console
$ docker pull geonetwork@sha256:0c771d4dd89ac51d0541c04da4c74e288dcf24effc03bfd59242f89be13c5c82
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **447.6 MB (447625160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7699902282d7e6be3707b318659206ea2c2479efc0ded72aa9c5fe77c262452`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:22 GMT
ADD file:9cca7f8e4abcd8309501cad216ff33a28932386ded66461a7591c0fdf2c859d3 in / 
# Wed, 26 Jan 2022 01:40:23 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:11:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:12:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Jan 2022 02:12:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:24:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:29:49 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 26 Jan 2022 09:29:50 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 26 Jan 2022 09:29:50 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 09:29:50 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jan 2022 09:29:50 GMT
ENV JAVA_VERSION=8u312
# Wed, 26 Jan 2022 09:30:47 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_x64_linux_8u312b07.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_aarch64_linux_8u312b07.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 27 Jan 2022 17:58:51 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 27 Jan 2022 17:58:51 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Jan 2022 17:58:52 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 27 Jan 2022 17:58:52 GMT
WORKDIR /usr/local/tomcat
# Thu, 27 Jan 2022 17:58:52 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 27 Jan 2022 17:58:52 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 27 Jan 2022 18:40:21 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 27 Jan 2022 18:40:22 GMT
ENV TOMCAT_MAJOR=8
# Thu, 27 Jan 2022 18:40:22 GMT
ENV TOMCAT_VERSION=8.5.75
# Thu, 27 Jan 2022 18:40:22 GMT
ENV TOMCAT_SHA512=b86d191506f8a647e3f4505bb7cc095068abb26bb4283562924913606514ce15930a467bd5d20c09b11d785827bf1914ed869b48dfb1c95e9f826e4c8b4e8aaa
# Thu, 27 Jan 2022 18:41:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 27 Jan 2022 18:41:49 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 27 Jan 2022 18:41:49 GMT
EXPOSE 8080
# Thu, 27 Jan 2022 18:41:49 GMT
CMD ["catalina.sh" "run"]
# Fri, 28 Jan 2022 00:29:11 GMT
ENV GN_FILE=geonetwork.war
# Fri, 28 Jan 2022 00:29:11 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Fri, 28 Jan 2022 00:29:11 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Fri, 28 Jan 2022 00:29:12 GMT
ENV GN_VERSION=3.10.10
# Fri, 28 Jan 2022 00:29:12 GMT
ENV GN_DOWNLOAD_MD5=de09ba1a43d6f3a224ad5ff02b4c4fb3
# Fri, 28 Jan 2022 00:29:12 GMT
ENV LOG4J_VERSION=2.17.1
# Fri, 28 Jan 2022 00:29:12 GMT
ENV LOG4J_SHA512=b7e948df6c6f57d903d990de2cc0270c1537b711285e9b6b91280db6ace38418fced713785b2c20512dd9a4238c2d1d0ceb414d9936df2ca110ff14993ae04dc
# Fri, 28 Jan 2022 00:29:13 GMT
WORKDIR /usr/local/tomcat/webapps
# Fri, 28 Jan 2022 01:13:36 GMT
RUN curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "$GN_DOWNLOAD_MD5 *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE &&      rm geonetwork/WEB-INF/lib/log4j-core-* &&      rm geonetwork/WEB-INF/lib/log4j-api* &&      curl -fSL -o apache-log4j-${LOG4J_VERSION}-bin.tar.gz "https://dlcdn.apache.org/logging/log4j/${LOG4J_VERSION}/apache-log4j-${LOG4J_VERSION}-bin.tar.gz" &&      echo "${LOG4J_SHA512} apache-log4j-${LOG4J_VERSION}-bin.tar.gz" | sha512sum -c &&      tar -xvzf apache-log4j-${LOG4J_VERSION}-bin.tar.gz &&      cp apache-log4j-${LOG4J_VERSION}-bin/log4j-core-${LOG4J_VERSION}.jar "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/lib/" &&      cp apache-log4j-${LOG4J_VERSION}-bin/log4j-api-${LOG4J_VERSION}.jar "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/lib/" &&      rm -rf apache-log4j-${LOG4J_VERSION}-bin*
# Fri, 28 Jan 2022 01:13:37 GMT
COPY file:0804862fd42c05f06dfa65cb1e5dad9a956d8ac6a3ddd4d962847ba159f5cfe6 in /entrypoint.sh 
# Fri, 28 Jan 2022 01:13:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 28 Jan 2022 01:13:37 GMT
CMD ["catalina.sh" "run"]
# Fri, 28 Jan 2022 01:13:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jan 2022 01:13:49 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml"
# Fri, 28 Jan 2022 01:13:49 GMT
COPY file:83f69d2041e5fb378033b0db57e096c81ba0725102ab4da4f089685e748fcce3 in /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties 
# Fri, 28 Jan 2022 01:13:49 GMT
COPY file:c88411abba7ad9b7bb75019f08755dbfa163d2fc7fdd80676bf9350c4c56a19c in /entrypoint.sh 
# Fri, 28 Jan 2022 01:13:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 28 Jan 2022 01:13:50 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:0c6b8ff8c37e92eb1ca65ed8917e818927d5bf318b6f18896049b5d9afc28343`  
		Last Modified: Wed, 26 Jan 2022 01:46:07 GMT  
		Size: 54.9 MB (54917164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:412caad352a3ecbb29c080379407ae0761e7b9b454f7239cbfd1d1da25e06b29`  
		Last Modified: Wed, 26 Jan 2022 02:22:09 GMT  
		Size: 5.2 MB (5152685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6d3e61f7a504fa66d7275123969e9917570188650eb84b2280a726b996040f6`  
		Last Modified: Wed, 26 Jan 2022 02:22:09 GMT  
		Size: 10.9 MB (10871783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:461bb1d8c517c7f9fc0f1df66c9dc34c85a23421c1e1c540b2e28cbb258e75f5`  
		Last Modified: Wed, 26 Jan 2022 02:22:32 GMT  
		Size: 54.6 MB (54567492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e442ee9d8dd9896a5b3b67117060f2af4ae8e997af7297009e7d0ea4b6595163`  
		Last Modified: Wed, 26 Jan 2022 09:50:58 GMT  
		Size: 5.4 MB (5420014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b5bcea956cbbcc7e16356354d5eb4b5b3834a43d708ca6c3fd048f33ddc579`  
		Last Modified: Wed, 26 Jan 2022 09:55:46 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3879cb950b1f93eff09fbecc9c1d4ed3760d3f81df96b99f8090e3955578b57`  
		Last Modified: Wed, 26 Jan 2022 09:55:59 GMT  
		Size: 106.0 MB (105999002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49e3fbddb891d992809b3882c1be86760359a997fbf71f9d2d67e30abc94e65`  
		Last Modified: Thu, 27 Jan 2022 19:16:46 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7bfbc34820025e3023401808fdd9dafc703b563ec8ade714a62eaa3395acad5`  
		Last Modified: Thu, 27 Jan 2022 19:35:44 GMT  
		Size: 11.5 MB (11531982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79726cf7f4f515d435cfde8dfaa18fedb5bdfe4edc28d01da89154106b32d77`  
		Last Modified: Thu, 27 Jan 2022 19:35:43 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99ce8840adc65146127fda27ccbe7b20867b9d89c9967a0e10520d2ee11f09fe`  
		Last Modified: Fri, 28 Jan 2022 01:15:33 GMT  
		Size: 195.7 MB (195657080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e1b367fe97a69251f113c267a16902892314fe37e6377bc84d49df3e83f5ad4`  
		Last Modified: Fri, 28 Jan 2022 01:15:21 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d1bbbe799cc6f61d2e000c52fc1908f0047528f417be6555eb37d15444ee757`  
		Last Modified: Fri, 28 Jan 2022 01:15:46 GMT  
		Size: 3.5 MB (3503825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed733596b47210740bc32e2e51aa393ece16e09b10787eb216ecde9cb037b2bb`  
		Last Modified: Fri, 28 Jan 2022 01:15:46 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db80ffabf1db0652d73eecfdf0aa932566eb0ce279f95fc1e2cb12076e7c403d`  
		Last Modified: Fri, 28 Jan 2022 01:15:45 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d137fbf18a9dfe666c5e4653432b1d3d8c34e196b1df0865f7f896949904450`  
		Last Modified: Fri, 28 Jan 2022 01:15:45 GMT  
		Size: 973.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `geonetwork:3.10.10-postgres` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:e5b4f6cb75293ba0de2192b9dd04e17612df2196236ab9e2a0f09f2c4f7acc1b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **444.7 MB (444734096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5442994d3c9366ed518b8caa34abb403871f0765f03cefa7084a01fb0b970a6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 26 Jan 2022 01:42:15 GMT
ADD file:b6338a9c3c2f8d7ba1a23dcb7a1389c7d0eab75a7489ef66f21c773be56aa9ed in / 
# Wed, 26 Jan 2022 01:42:16 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:13:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:13:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Jan 2022 02:13:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 05:56:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 06:00:46 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 26 Jan 2022 06:00:48 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 26 Jan 2022 06:00:48 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 06:00:49 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jan 2022 06:00:50 GMT
ENV JAVA_VERSION=8u312
# Wed, 26 Jan 2022 06:01:01 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_x64_linux_8u312b07.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_aarch64_linux_8u312b07.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Wed, 26 Jan 2022 23:58:42 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 26 Jan 2022 23:58:43 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 23:58:44 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 26 Jan 2022 23:58:45 GMT
WORKDIR /usr/local/tomcat
# Wed, 26 Jan 2022 23:58:46 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 26 Jan 2022 23:58:47 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 27 Jan 2022 00:24:40 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 27 Jan 2022 00:24:41 GMT
ENV TOMCAT_MAJOR=8
# Thu, 27 Jan 2022 00:24:42 GMT
ENV TOMCAT_VERSION=8.5.75
# Thu, 27 Jan 2022 00:24:43 GMT
ENV TOMCAT_SHA512=b86d191506f8a647e3f4505bb7cc095068abb26bb4283562924913606514ce15930a467bd5d20c09b11d785827bf1914ed869b48dfb1c95e9f826e4c8b4e8aaa
# Thu, 27 Jan 2022 00:25:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 27 Jan 2022 00:25:48 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 27 Jan 2022 00:25:49 GMT
EXPOSE 8080
# Thu, 27 Jan 2022 00:25:50 GMT
CMD ["catalina.sh" "run"]
# Thu, 27 Jan 2022 05:09:51 GMT
ENV GN_FILE=geonetwork.war
# Thu, 27 Jan 2022 05:09:52 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Thu, 27 Jan 2022 05:09:52 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Thu, 27 Jan 2022 05:09:53 GMT
ENV GN_VERSION=3.10.10
# Thu, 27 Jan 2022 05:09:54 GMT
ENV GN_DOWNLOAD_MD5=de09ba1a43d6f3a224ad5ff02b4c4fb3
# Thu, 27 Jan 2022 05:09:55 GMT
ENV LOG4J_VERSION=2.17.1
# Thu, 27 Jan 2022 05:09:56 GMT
ENV LOG4J_SHA512=b7e948df6c6f57d903d990de2cc0270c1537b711285e9b6b91280db6ace38418fced713785b2c20512dd9a4238c2d1d0ceb414d9936df2ca110ff14993ae04dc
# Thu, 27 Jan 2022 05:09:57 GMT
WORKDIR /usr/local/tomcat/webapps
# Thu, 27 Jan 2022 05:11:44 GMT
RUN curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "$GN_DOWNLOAD_MD5 *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE &&      rm geonetwork/WEB-INF/lib/log4j-core-* &&      rm geonetwork/WEB-INF/lib/log4j-api* &&      curl -fSL -o apache-log4j-${LOG4J_VERSION}-bin.tar.gz "https://dlcdn.apache.org/logging/log4j/${LOG4J_VERSION}/apache-log4j-${LOG4J_VERSION}-bin.tar.gz" &&      echo "${LOG4J_SHA512} apache-log4j-${LOG4J_VERSION}-bin.tar.gz" | sha512sum -c &&      tar -xvzf apache-log4j-${LOG4J_VERSION}-bin.tar.gz &&      cp apache-log4j-${LOG4J_VERSION}-bin/log4j-core-${LOG4J_VERSION}.jar "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/lib/" &&      cp apache-log4j-${LOG4J_VERSION}-bin/log4j-api-${LOG4J_VERSION}.jar "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/lib/" &&      rm -rf apache-log4j-${LOG4J_VERSION}-bin*
# Thu, 27 Jan 2022 05:11:45 GMT
COPY file:0804862fd42c05f06dfa65cb1e5dad9a956d8ac6a3ddd4d962847ba159f5cfe6 in /entrypoint.sh 
# Thu, 27 Jan 2022 05:11:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Jan 2022 05:11:47 GMT
CMD ["catalina.sh" "run"]
# Thu, 27 Jan 2022 05:12:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/*
# Thu, 27 Jan 2022 05:12:09 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml"
# Thu, 27 Jan 2022 05:12:10 GMT
COPY file:83f69d2041e5fb378033b0db57e096c81ba0725102ab4da4f089685e748fcce3 in /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties 
# Thu, 27 Jan 2022 05:12:11 GMT
COPY file:c88411abba7ad9b7bb75019f08755dbfa163d2fc7fdd80676bf9350c4c56a19c in /entrypoint.sh 
# Thu, 27 Jan 2022 05:12:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Jan 2022 05:12:12 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:39ab78bc09e79a21f719ced771689354d1948f4afd57e86afed8dac6ffb47826`  
		Last Modified: Wed, 26 Jan 2022 01:48:34 GMT  
		Size: 53.6 MB (53608848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cf88d09fc28807e643d4f619b2e0c559aaeddc7d7b8176e1144b065d63fa160`  
		Last Modified: Wed, 26 Jan 2022 02:23:47 GMT  
		Size: 5.1 MB (5141567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e019dd0368ba992803442a16cc7792c1bd5a3d06c3a1ae6fae17cb838822fb4c`  
		Last Modified: Wed, 26 Jan 2022 02:23:48 GMT  
		Size: 10.7 MB (10655902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9f1769d50d3693321e1b48f527d9c920830ad24d931b642c116bf7823bed6a`  
		Last Modified: Wed, 26 Jan 2022 02:24:10 GMT  
		Size: 54.7 MB (54669460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5cb8edd8beada37ea034ed391c47dfd106ff9cc9fac852e0f52db0b063374f`  
		Last Modified: Wed, 26 Jan 2022 06:23:05 GMT  
		Size: 5.4 MB (5420184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3973acc73ccb4db4685136c67eb73dd02f02b1518d5381cf376d82710758caa`  
		Last Modified: Wed, 26 Jan 2022 06:28:15 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:568c3474f69d85e6c2c507e089aacb5f23548845e35e993a3df6640ca80a6a61`  
		Last Modified: Wed, 26 Jan 2022 06:28:29 GMT  
		Size: 105.0 MB (105010960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c750153dc133d7b7832882e2a1e214d7e796cd23f1e59adc71cca58bd106ca1`  
		Last Modified: Thu, 27 Jan 2022 00:58:36 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd36e2060fcb58cd13a8f07504a330d6a61dbcfed5e64d211f76c6d93998d54`  
		Last Modified: Thu, 27 Jan 2022 01:16:23 GMT  
		Size: 11.3 MB (11303628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1be15c1e58fe9530aae8d99555bb240e60ceafbd8c41fc14e13b9ff17894be7c`  
		Last Modified: Thu, 27 Jan 2022 05:19:29 GMT  
		Size: 195.7 MB (195658597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cdc01c6f942f2a1582083f5d361b03f10b6261e0e41b03804528aa3c66a74e2`  
		Last Modified: Thu, 27 Jan 2022 05:19:13 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba5757904131d07ee2dd8aa0efaac54ae74eabe4acae773ef79d5070390884f`  
		Last Modified: Thu, 27 Jan 2022 05:19:42 GMT  
		Size: 3.3 MB (3260983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f22c64a8cd1dfcadf29016415ede58e852732d52486444385d5116773f6f2d8`  
		Last Modified: Thu, 27 Jan 2022 05:19:42 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de67ae6e8a50f9014765bbc631096fd8d36e2f672a24ee3684248889684442e`  
		Last Modified: Thu, 27 Jan 2022 05:19:41 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5326143d47f5727b41f1dedc4c564f5a93f87842a9add39739bf921eb119ed8d`  
		Last Modified: Thu, 27 Jan 2022 05:19:41 GMT  
		Size: 973.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `geonetwork:3.12`

```console
$ docker pull geonetwork@sha256:37d5c95e4202a9b96f76622a28784e15ec7063bb7f3ccf42562f244319dd5c6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `geonetwork:3.12` - linux; amd64

```console
$ docker pull geonetwork@sha256:df817d01621765865a644f5556aab1e0210d3df49567e02d572833f1a9eefacd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **475.7 MB (475732709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c3a7abfc682cdda276a0be019a8b0880fcd6dd65fec545d5a523c9058e0e841`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:22 GMT
ADD file:9cca7f8e4abcd8309501cad216ff33a28932386ded66461a7591c0fdf2c859d3 in / 
# Wed, 26 Jan 2022 01:40:23 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:11:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:12:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Jan 2022 02:12:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:24:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:29:49 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 26 Jan 2022 09:29:50 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 26 Jan 2022 09:29:50 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 09:29:50 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jan 2022 09:29:50 GMT
ENV JAVA_VERSION=8u312
# Wed, 26 Jan 2022 09:30:47 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_x64_linux_8u312b07.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_aarch64_linux_8u312b07.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 27 Jan 2022 17:58:51 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 27 Jan 2022 17:58:51 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Jan 2022 17:58:52 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 27 Jan 2022 17:58:52 GMT
WORKDIR /usr/local/tomcat
# Thu, 27 Jan 2022 17:58:52 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 27 Jan 2022 17:58:52 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 27 Jan 2022 18:40:21 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 27 Jan 2022 18:40:22 GMT
ENV TOMCAT_MAJOR=8
# Thu, 27 Jan 2022 18:40:22 GMT
ENV TOMCAT_VERSION=8.5.75
# Thu, 27 Jan 2022 18:40:22 GMT
ENV TOMCAT_SHA512=b86d191506f8a647e3f4505bb7cc095068abb26bb4283562924913606514ce15930a467bd5d20c09b11d785827bf1914ed869b48dfb1c95e9f826e4c8b4e8aaa
# Thu, 27 Jan 2022 18:41:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 27 Jan 2022 18:41:49 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 27 Jan 2022 18:41:49 GMT
EXPOSE 8080
# Thu, 27 Jan 2022 18:41:49 GMT
CMD ["catalina.sh" "run"]
# Fri, 28 Jan 2022 00:29:11 GMT
ENV GN_FILE=geonetwork.war
# Fri, 28 Jan 2022 00:29:11 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Fri, 28 Jan 2022 00:29:11 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Fri, 28 Jan 2022 00:30:29 GMT
ENV GN_VERSION=3.12.3
# Fri, 28 Jan 2022 00:30:29 GMT
ENV GN_DOWNLOAD_MD5=ecbbff832c8a6edf22e06aa1870dddab
# Fri, 28 Jan 2022 00:30:29 GMT
WORKDIR /usr/local/tomcat/webapps
# Fri, 28 Jan 2022 01:14:38 GMT
RUN curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE
# Fri, 28 Jan 2022 01:14:39 GMT
COPY file:0804862fd42c05f06dfa65cb1e5dad9a956d8ac6a3ddd4d962847ba159f5cfe6 in /entrypoint.sh 
# Fri, 28 Jan 2022 01:14:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 28 Jan 2022 01:14:39 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:0c6b8ff8c37e92eb1ca65ed8917e818927d5bf318b6f18896049b5d9afc28343`  
		Last Modified: Wed, 26 Jan 2022 01:46:07 GMT  
		Size: 54.9 MB (54917164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:412caad352a3ecbb29c080379407ae0761e7b9b454f7239cbfd1d1da25e06b29`  
		Last Modified: Wed, 26 Jan 2022 02:22:09 GMT  
		Size: 5.2 MB (5152685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6d3e61f7a504fa66d7275123969e9917570188650eb84b2280a726b996040f6`  
		Last Modified: Wed, 26 Jan 2022 02:22:09 GMT  
		Size: 10.9 MB (10871783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:461bb1d8c517c7f9fc0f1df66c9dc34c85a23421c1e1c540b2e28cbb258e75f5`  
		Last Modified: Wed, 26 Jan 2022 02:22:32 GMT  
		Size: 54.6 MB (54567492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e442ee9d8dd9896a5b3b67117060f2af4ae8e997af7297009e7d0ea4b6595163`  
		Last Modified: Wed, 26 Jan 2022 09:50:58 GMT  
		Size: 5.4 MB (5420014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b5bcea956cbbcc7e16356354d5eb4b5b3834a43d708ca6c3fd048f33ddc579`  
		Last Modified: Wed, 26 Jan 2022 09:55:46 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3879cb950b1f93eff09fbecc9c1d4ed3760d3f81df96b99f8090e3955578b57`  
		Last Modified: Wed, 26 Jan 2022 09:55:59 GMT  
		Size: 106.0 MB (105999002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49e3fbddb891d992809b3882c1be86760359a997fbf71f9d2d67e30abc94e65`  
		Last Modified: Thu, 27 Jan 2022 19:16:46 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7bfbc34820025e3023401808fdd9dafc703b563ec8ade714a62eaa3395acad5`  
		Last Modified: Thu, 27 Jan 2022 19:35:44 GMT  
		Size: 11.5 MB (11531982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79726cf7f4f515d435cfde8dfaa18fedb5bdfe4edc28d01da89154106b32d77`  
		Last Modified: Thu, 27 Jan 2022 19:35:43 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e535218eecde23bcc1cc7329cf505d83f2e401ff1edefc5bbc05e0d1a5d04b39`  
		Last Modified: Fri, 28 Jan 2022 01:16:11 GMT  
		Size: 227.3 MB (227271824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a1e69ef5f77af477dee27b039a9b6c5d65be2230110d76e5d501e5d9318bbf2`  
		Last Modified: Fri, 28 Jan 2022 01:15:58 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `geonetwork:3.12` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:d6b77812dd3c63935ac94786f3fde7a2625d9d19774b8f4b4947899183500165
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **473.1 MB (473081985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5d62bdccd0d9f540879a1f4effa87b0d183092355a9b20c7e386f5c45920af0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 26 Jan 2022 01:42:15 GMT
ADD file:b6338a9c3c2f8d7ba1a23dcb7a1389c7d0eab75a7489ef66f21c773be56aa9ed in / 
# Wed, 26 Jan 2022 01:42:16 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:13:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:13:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Jan 2022 02:13:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 05:56:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 06:00:46 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 26 Jan 2022 06:00:48 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 26 Jan 2022 06:00:48 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 06:00:49 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jan 2022 06:00:50 GMT
ENV JAVA_VERSION=8u312
# Wed, 26 Jan 2022 06:01:01 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_x64_linux_8u312b07.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_aarch64_linux_8u312b07.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Wed, 26 Jan 2022 23:58:42 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 26 Jan 2022 23:58:43 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 23:58:44 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 26 Jan 2022 23:58:45 GMT
WORKDIR /usr/local/tomcat
# Wed, 26 Jan 2022 23:58:46 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 26 Jan 2022 23:58:47 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 27 Jan 2022 00:24:40 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 27 Jan 2022 00:24:41 GMT
ENV TOMCAT_MAJOR=8
# Thu, 27 Jan 2022 00:24:42 GMT
ENV TOMCAT_VERSION=8.5.75
# Thu, 27 Jan 2022 00:24:43 GMT
ENV TOMCAT_SHA512=b86d191506f8a647e3f4505bb7cc095068abb26bb4283562924913606514ce15930a467bd5d20c09b11d785827bf1914ed869b48dfb1c95e9f826e4c8b4e8aaa
# Thu, 27 Jan 2022 00:25:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 27 Jan 2022 00:25:48 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 27 Jan 2022 00:25:49 GMT
EXPOSE 8080
# Thu, 27 Jan 2022 00:25:50 GMT
CMD ["catalina.sh" "run"]
# Thu, 27 Jan 2022 05:09:51 GMT
ENV GN_FILE=geonetwork.war
# Thu, 27 Jan 2022 05:09:52 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Thu, 27 Jan 2022 05:09:52 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Thu, 27 Jan 2022 05:12:18 GMT
ENV GN_VERSION=3.12.3
# Thu, 27 Jan 2022 05:12:18 GMT
ENV GN_DOWNLOAD_MD5=ecbbff832c8a6edf22e06aa1870dddab
# Thu, 27 Jan 2022 05:12:19 GMT
WORKDIR /usr/local/tomcat/webapps
# Thu, 27 Jan 2022 05:15:06 GMT
RUN curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE
# Thu, 27 Jan 2022 05:15:08 GMT
COPY file:0804862fd42c05f06dfa65cb1e5dad9a956d8ac6a3ddd4d962847ba159f5cfe6 in /entrypoint.sh 
# Thu, 27 Jan 2022 05:15:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Jan 2022 05:15:09 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:39ab78bc09e79a21f719ced771689354d1948f4afd57e86afed8dac6ffb47826`  
		Last Modified: Wed, 26 Jan 2022 01:48:34 GMT  
		Size: 53.6 MB (53608848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cf88d09fc28807e643d4f619b2e0c559aaeddc7d7b8176e1144b065d63fa160`  
		Last Modified: Wed, 26 Jan 2022 02:23:47 GMT  
		Size: 5.1 MB (5141567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e019dd0368ba992803442a16cc7792c1bd5a3d06c3a1ae6fae17cb838822fb4c`  
		Last Modified: Wed, 26 Jan 2022 02:23:48 GMT  
		Size: 10.7 MB (10655902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9f1769d50d3693321e1b48f527d9c920830ad24d931b642c116bf7823bed6a`  
		Last Modified: Wed, 26 Jan 2022 02:24:10 GMT  
		Size: 54.7 MB (54669460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5cb8edd8beada37ea034ed391c47dfd106ff9cc9fac852e0f52db0b063374f`  
		Last Modified: Wed, 26 Jan 2022 06:23:05 GMT  
		Size: 5.4 MB (5420184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3973acc73ccb4db4685136c67eb73dd02f02b1518d5381cf376d82710758caa`  
		Last Modified: Wed, 26 Jan 2022 06:28:15 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:568c3474f69d85e6c2c507e089aacb5f23548845e35e993a3df6640ca80a6a61`  
		Last Modified: Wed, 26 Jan 2022 06:28:29 GMT  
		Size: 105.0 MB (105010960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c750153dc133d7b7832882e2a1e214d7e796cd23f1e59adc71cca58bd106ca1`  
		Last Modified: Thu, 27 Jan 2022 00:58:36 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd36e2060fcb58cd13a8f07504a330d6a61dbcfed5e64d211f76c6d93998d54`  
		Last Modified: Thu, 27 Jan 2022 01:16:23 GMT  
		Size: 11.3 MB (11303628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b87cb97d3e30d47e944ad2b3e55d72ef881c77a8599f906591dd8c2fcc45f56`  
		Last Modified: Thu, 27 Jan 2022 05:20:11 GMT  
		Size: 227.3 MB (227270838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:881aba0954a8e117ca330b1e1b047aa39075276fc7db40142388ccbfb0ec034f`  
		Last Modified: Thu, 27 Jan 2022 05:19:53 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `geonetwork:3.12-postgres`

```console
$ docker pull geonetwork@sha256:7f7959c4395c6853a248dad867133f75a1df647c527f901f61d92eebf419c040
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `geonetwork:3.12-postgres` - linux; amd64

```console
$ docker pull geonetwork@sha256:28be89ec28ce4bde3902d00a2cf87ec13a81bef5c6fcbeecf49ec2ae60e2103c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **479.2 MB (479239897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfc2f03558b5ccdb22ee9812d1022b2532fbf6177e6b3c87b57a8157601faf30`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:22 GMT
ADD file:9cca7f8e4abcd8309501cad216ff33a28932386ded66461a7591c0fdf2c859d3 in / 
# Wed, 26 Jan 2022 01:40:23 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:11:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:12:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Jan 2022 02:12:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:24:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:29:49 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 26 Jan 2022 09:29:50 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 26 Jan 2022 09:29:50 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 09:29:50 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jan 2022 09:29:50 GMT
ENV JAVA_VERSION=8u312
# Wed, 26 Jan 2022 09:30:47 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_x64_linux_8u312b07.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_aarch64_linux_8u312b07.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 27 Jan 2022 17:58:51 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 27 Jan 2022 17:58:51 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Jan 2022 17:58:52 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 27 Jan 2022 17:58:52 GMT
WORKDIR /usr/local/tomcat
# Thu, 27 Jan 2022 17:58:52 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 27 Jan 2022 17:58:52 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 27 Jan 2022 18:40:21 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 27 Jan 2022 18:40:22 GMT
ENV TOMCAT_MAJOR=8
# Thu, 27 Jan 2022 18:40:22 GMT
ENV TOMCAT_VERSION=8.5.75
# Thu, 27 Jan 2022 18:40:22 GMT
ENV TOMCAT_SHA512=b86d191506f8a647e3f4505bb7cc095068abb26bb4283562924913606514ce15930a467bd5d20c09b11d785827bf1914ed869b48dfb1c95e9f826e4c8b4e8aaa
# Thu, 27 Jan 2022 18:41:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 27 Jan 2022 18:41:49 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 27 Jan 2022 18:41:49 GMT
EXPOSE 8080
# Thu, 27 Jan 2022 18:41:49 GMT
CMD ["catalina.sh" "run"]
# Fri, 28 Jan 2022 00:29:11 GMT
ENV GN_FILE=geonetwork.war
# Fri, 28 Jan 2022 00:29:11 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Fri, 28 Jan 2022 00:29:11 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Fri, 28 Jan 2022 00:30:29 GMT
ENV GN_VERSION=3.12.3
# Fri, 28 Jan 2022 00:30:29 GMT
ENV GN_DOWNLOAD_MD5=ecbbff832c8a6edf22e06aa1870dddab
# Fri, 28 Jan 2022 00:30:29 GMT
WORKDIR /usr/local/tomcat/webapps
# Fri, 28 Jan 2022 01:14:38 GMT
RUN curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE
# Fri, 28 Jan 2022 01:14:39 GMT
COPY file:0804862fd42c05f06dfa65cb1e5dad9a956d8ac6a3ddd4d962847ba159f5cfe6 in /entrypoint.sh 
# Fri, 28 Jan 2022 01:14:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 28 Jan 2022 01:14:39 GMT
CMD ["catalina.sh" "run"]
# Fri, 28 Jan 2022 01:14:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jan 2022 01:14:56 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml"
# Fri, 28 Jan 2022 01:14:56 GMT
COPY file:83f69d2041e5fb378033b0db57e096c81ba0725102ab4da4f089685e748fcce3 in /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties 
# Fri, 28 Jan 2022 01:14:56 GMT
COPY file:c88411abba7ad9b7bb75019f08755dbfa163d2fc7fdd80676bf9350c4c56a19c in /entrypoint.sh 
# Fri, 28 Jan 2022 01:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 28 Jan 2022 01:14:57 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:0c6b8ff8c37e92eb1ca65ed8917e818927d5bf318b6f18896049b5d9afc28343`  
		Last Modified: Wed, 26 Jan 2022 01:46:07 GMT  
		Size: 54.9 MB (54917164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:412caad352a3ecbb29c080379407ae0761e7b9b454f7239cbfd1d1da25e06b29`  
		Last Modified: Wed, 26 Jan 2022 02:22:09 GMT  
		Size: 5.2 MB (5152685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6d3e61f7a504fa66d7275123969e9917570188650eb84b2280a726b996040f6`  
		Last Modified: Wed, 26 Jan 2022 02:22:09 GMT  
		Size: 10.9 MB (10871783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:461bb1d8c517c7f9fc0f1df66c9dc34c85a23421c1e1c540b2e28cbb258e75f5`  
		Last Modified: Wed, 26 Jan 2022 02:22:32 GMT  
		Size: 54.6 MB (54567492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e442ee9d8dd9896a5b3b67117060f2af4ae8e997af7297009e7d0ea4b6595163`  
		Last Modified: Wed, 26 Jan 2022 09:50:58 GMT  
		Size: 5.4 MB (5420014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b5bcea956cbbcc7e16356354d5eb4b5b3834a43d708ca6c3fd048f33ddc579`  
		Last Modified: Wed, 26 Jan 2022 09:55:46 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3879cb950b1f93eff09fbecc9c1d4ed3760d3f81df96b99f8090e3955578b57`  
		Last Modified: Wed, 26 Jan 2022 09:55:59 GMT  
		Size: 106.0 MB (105999002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49e3fbddb891d992809b3882c1be86760359a997fbf71f9d2d67e30abc94e65`  
		Last Modified: Thu, 27 Jan 2022 19:16:46 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7bfbc34820025e3023401808fdd9dafc703b563ec8ade714a62eaa3395acad5`  
		Last Modified: Thu, 27 Jan 2022 19:35:44 GMT  
		Size: 11.5 MB (11531982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79726cf7f4f515d435cfde8dfaa18fedb5bdfe4edc28d01da89154106b32d77`  
		Last Modified: Thu, 27 Jan 2022 19:35:43 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e535218eecde23bcc1cc7329cf505d83f2e401ff1edefc5bbc05e0d1a5d04b39`  
		Last Modified: Fri, 28 Jan 2022 01:16:11 GMT  
		Size: 227.3 MB (227271824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a1e69ef5f77af477dee27b039a9b6c5d65be2230110d76e5d501e5d9318bbf2`  
		Last Modified: Fri, 28 Jan 2022 01:15:58 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b62dadb210a914e3c38a325041dafe9c739465a9130cee94db462e7fd20a3f8`  
		Last Modified: Fri, 28 Jan 2022 01:16:27 GMT  
		Size: 3.5 MB (3503818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21d351266fb7a1d8cbf106d8b6aefece074dc5f0bff29d700ff4fe8cd5c4763d`  
		Last Modified: Fri, 28 Jan 2022 01:16:26 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48204bc4304fc8a091cd9be6d452b8e809475445582bcc3927c10d8a0c71472e`  
		Last Modified: Fri, 28 Jan 2022 01:16:26 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bea59ddb2568c53835bd9791ed31bc78fc5f3eac0c70888f1112c9791b34f4b`  
		Last Modified: Fri, 28 Jan 2022 01:16:26 GMT  
		Size: 973.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `geonetwork:3.12-postgres` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:f2773d655f2b71114be11fa5322a3af0776258caa1ef8f6da4957bc51674c471
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **476.3 MB (476346385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a381731898665b1e6e70b5c772c4364f76dc81a32043fb93ab4f908de0dc288e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 26 Jan 2022 01:42:15 GMT
ADD file:b6338a9c3c2f8d7ba1a23dcb7a1389c7d0eab75a7489ef66f21c773be56aa9ed in / 
# Wed, 26 Jan 2022 01:42:16 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:13:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:13:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Jan 2022 02:13:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 05:56:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 06:00:46 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 26 Jan 2022 06:00:48 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 26 Jan 2022 06:00:48 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 06:00:49 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jan 2022 06:00:50 GMT
ENV JAVA_VERSION=8u312
# Wed, 26 Jan 2022 06:01:01 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_x64_linux_8u312b07.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_aarch64_linux_8u312b07.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Wed, 26 Jan 2022 23:58:42 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 26 Jan 2022 23:58:43 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 23:58:44 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 26 Jan 2022 23:58:45 GMT
WORKDIR /usr/local/tomcat
# Wed, 26 Jan 2022 23:58:46 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 26 Jan 2022 23:58:47 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 27 Jan 2022 00:24:40 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 27 Jan 2022 00:24:41 GMT
ENV TOMCAT_MAJOR=8
# Thu, 27 Jan 2022 00:24:42 GMT
ENV TOMCAT_VERSION=8.5.75
# Thu, 27 Jan 2022 00:24:43 GMT
ENV TOMCAT_SHA512=b86d191506f8a647e3f4505bb7cc095068abb26bb4283562924913606514ce15930a467bd5d20c09b11d785827bf1914ed869b48dfb1c95e9f826e4c8b4e8aaa
# Thu, 27 Jan 2022 00:25:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 27 Jan 2022 00:25:48 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 27 Jan 2022 00:25:49 GMT
EXPOSE 8080
# Thu, 27 Jan 2022 00:25:50 GMT
CMD ["catalina.sh" "run"]
# Thu, 27 Jan 2022 05:09:51 GMT
ENV GN_FILE=geonetwork.war
# Thu, 27 Jan 2022 05:09:52 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Thu, 27 Jan 2022 05:09:52 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Thu, 27 Jan 2022 05:12:18 GMT
ENV GN_VERSION=3.12.3
# Thu, 27 Jan 2022 05:12:18 GMT
ENV GN_DOWNLOAD_MD5=ecbbff832c8a6edf22e06aa1870dddab
# Thu, 27 Jan 2022 05:12:19 GMT
WORKDIR /usr/local/tomcat/webapps
# Thu, 27 Jan 2022 05:15:06 GMT
RUN curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE
# Thu, 27 Jan 2022 05:15:08 GMT
COPY file:0804862fd42c05f06dfa65cb1e5dad9a956d8ac6a3ddd4d962847ba159f5cfe6 in /entrypoint.sh 
# Thu, 27 Jan 2022 05:15:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Jan 2022 05:15:09 GMT
CMD ["catalina.sh" "run"]
# Thu, 27 Jan 2022 05:15:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/*
# Thu, 27 Jan 2022 05:15:21 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml"
# Thu, 27 Jan 2022 05:15:22 GMT
COPY file:83f69d2041e5fb378033b0db57e096c81ba0725102ab4da4f089685e748fcce3 in /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties 
# Thu, 27 Jan 2022 05:15:23 GMT
COPY file:c88411abba7ad9b7bb75019f08755dbfa163d2fc7fdd80676bf9350c4c56a19c in /entrypoint.sh 
# Thu, 27 Jan 2022 05:15:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Jan 2022 05:15:24 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:39ab78bc09e79a21f719ced771689354d1948f4afd57e86afed8dac6ffb47826`  
		Last Modified: Wed, 26 Jan 2022 01:48:34 GMT  
		Size: 53.6 MB (53608848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cf88d09fc28807e643d4f619b2e0c559aaeddc7d7b8176e1144b065d63fa160`  
		Last Modified: Wed, 26 Jan 2022 02:23:47 GMT  
		Size: 5.1 MB (5141567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e019dd0368ba992803442a16cc7792c1bd5a3d06c3a1ae6fae17cb838822fb4c`  
		Last Modified: Wed, 26 Jan 2022 02:23:48 GMT  
		Size: 10.7 MB (10655902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9f1769d50d3693321e1b48f527d9c920830ad24d931b642c116bf7823bed6a`  
		Last Modified: Wed, 26 Jan 2022 02:24:10 GMT  
		Size: 54.7 MB (54669460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5cb8edd8beada37ea034ed391c47dfd106ff9cc9fac852e0f52db0b063374f`  
		Last Modified: Wed, 26 Jan 2022 06:23:05 GMT  
		Size: 5.4 MB (5420184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3973acc73ccb4db4685136c67eb73dd02f02b1518d5381cf376d82710758caa`  
		Last Modified: Wed, 26 Jan 2022 06:28:15 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:568c3474f69d85e6c2c507e089aacb5f23548845e35e993a3df6640ca80a6a61`  
		Last Modified: Wed, 26 Jan 2022 06:28:29 GMT  
		Size: 105.0 MB (105010960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c750153dc133d7b7832882e2a1e214d7e796cd23f1e59adc71cca58bd106ca1`  
		Last Modified: Thu, 27 Jan 2022 00:58:36 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd36e2060fcb58cd13a8f07504a330d6a61dbcfed5e64d211f76c6d93998d54`  
		Last Modified: Thu, 27 Jan 2022 01:16:23 GMT  
		Size: 11.3 MB (11303628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b87cb97d3e30d47e944ad2b3e55d72ef881c77a8599f906591dd8c2fcc45f56`  
		Last Modified: Thu, 27 Jan 2022 05:20:11 GMT  
		Size: 227.3 MB (227270838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:881aba0954a8e117ca330b1e1b047aa39075276fc7db40142388ccbfb0ec034f`  
		Last Modified: Thu, 27 Jan 2022 05:19:53 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9acebe6860978760636fd588bac693eb4beee3543ef67ef8f25cd67f7a7457f2`  
		Last Modified: Thu, 27 Jan 2022 05:20:27 GMT  
		Size: 3.3 MB (3261038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4baea3b1d826a8a216f0f9797bd95394e946a085b38d7f33b924ac3baccb4210`  
		Last Modified: Thu, 27 Jan 2022 05:20:26 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb94c323bdb05fb1ee7b2dd60cf963d12b24caca02794520d8cc92ccebf402b4`  
		Last Modified: Thu, 27 Jan 2022 05:20:26 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b8e950e474e503d01784c3b407aa7e628e6ac77eef70c7b4d1d9ca995cd497e`  
		Last Modified: Thu, 27 Jan 2022 05:20:26 GMT  
		Size: 974.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `geonetwork:3.12.3`

```console
$ docker pull geonetwork@sha256:37d5c95e4202a9b96f76622a28784e15ec7063bb7f3ccf42562f244319dd5c6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `geonetwork:3.12.3` - linux; amd64

```console
$ docker pull geonetwork@sha256:df817d01621765865a644f5556aab1e0210d3df49567e02d572833f1a9eefacd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **475.7 MB (475732709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c3a7abfc682cdda276a0be019a8b0880fcd6dd65fec545d5a523c9058e0e841`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:22 GMT
ADD file:9cca7f8e4abcd8309501cad216ff33a28932386ded66461a7591c0fdf2c859d3 in / 
# Wed, 26 Jan 2022 01:40:23 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:11:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:12:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Jan 2022 02:12:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:24:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:29:49 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 26 Jan 2022 09:29:50 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 26 Jan 2022 09:29:50 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 09:29:50 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jan 2022 09:29:50 GMT
ENV JAVA_VERSION=8u312
# Wed, 26 Jan 2022 09:30:47 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_x64_linux_8u312b07.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_aarch64_linux_8u312b07.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 27 Jan 2022 17:58:51 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 27 Jan 2022 17:58:51 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Jan 2022 17:58:52 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 27 Jan 2022 17:58:52 GMT
WORKDIR /usr/local/tomcat
# Thu, 27 Jan 2022 17:58:52 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 27 Jan 2022 17:58:52 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 27 Jan 2022 18:40:21 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 27 Jan 2022 18:40:22 GMT
ENV TOMCAT_MAJOR=8
# Thu, 27 Jan 2022 18:40:22 GMT
ENV TOMCAT_VERSION=8.5.75
# Thu, 27 Jan 2022 18:40:22 GMT
ENV TOMCAT_SHA512=b86d191506f8a647e3f4505bb7cc095068abb26bb4283562924913606514ce15930a467bd5d20c09b11d785827bf1914ed869b48dfb1c95e9f826e4c8b4e8aaa
# Thu, 27 Jan 2022 18:41:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 27 Jan 2022 18:41:49 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 27 Jan 2022 18:41:49 GMT
EXPOSE 8080
# Thu, 27 Jan 2022 18:41:49 GMT
CMD ["catalina.sh" "run"]
# Fri, 28 Jan 2022 00:29:11 GMT
ENV GN_FILE=geonetwork.war
# Fri, 28 Jan 2022 00:29:11 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Fri, 28 Jan 2022 00:29:11 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Fri, 28 Jan 2022 00:30:29 GMT
ENV GN_VERSION=3.12.3
# Fri, 28 Jan 2022 00:30:29 GMT
ENV GN_DOWNLOAD_MD5=ecbbff832c8a6edf22e06aa1870dddab
# Fri, 28 Jan 2022 00:30:29 GMT
WORKDIR /usr/local/tomcat/webapps
# Fri, 28 Jan 2022 01:14:38 GMT
RUN curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE
# Fri, 28 Jan 2022 01:14:39 GMT
COPY file:0804862fd42c05f06dfa65cb1e5dad9a956d8ac6a3ddd4d962847ba159f5cfe6 in /entrypoint.sh 
# Fri, 28 Jan 2022 01:14:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 28 Jan 2022 01:14:39 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:0c6b8ff8c37e92eb1ca65ed8917e818927d5bf318b6f18896049b5d9afc28343`  
		Last Modified: Wed, 26 Jan 2022 01:46:07 GMT  
		Size: 54.9 MB (54917164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:412caad352a3ecbb29c080379407ae0761e7b9b454f7239cbfd1d1da25e06b29`  
		Last Modified: Wed, 26 Jan 2022 02:22:09 GMT  
		Size: 5.2 MB (5152685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6d3e61f7a504fa66d7275123969e9917570188650eb84b2280a726b996040f6`  
		Last Modified: Wed, 26 Jan 2022 02:22:09 GMT  
		Size: 10.9 MB (10871783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:461bb1d8c517c7f9fc0f1df66c9dc34c85a23421c1e1c540b2e28cbb258e75f5`  
		Last Modified: Wed, 26 Jan 2022 02:22:32 GMT  
		Size: 54.6 MB (54567492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e442ee9d8dd9896a5b3b67117060f2af4ae8e997af7297009e7d0ea4b6595163`  
		Last Modified: Wed, 26 Jan 2022 09:50:58 GMT  
		Size: 5.4 MB (5420014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b5bcea956cbbcc7e16356354d5eb4b5b3834a43d708ca6c3fd048f33ddc579`  
		Last Modified: Wed, 26 Jan 2022 09:55:46 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3879cb950b1f93eff09fbecc9c1d4ed3760d3f81df96b99f8090e3955578b57`  
		Last Modified: Wed, 26 Jan 2022 09:55:59 GMT  
		Size: 106.0 MB (105999002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49e3fbddb891d992809b3882c1be86760359a997fbf71f9d2d67e30abc94e65`  
		Last Modified: Thu, 27 Jan 2022 19:16:46 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7bfbc34820025e3023401808fdd9dafc703b563ec8ade714a62eaa3395acad5`  
		Last Modified: Thu, 27 Jan 2022 19:35:44 GMT  
		Size: 11.5 MB (11531982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79726cf7f4f515d435cfde8dfaa18fedb5bdfe4edc28d01da89154106b32d77`  
		Last Modified: Thu, 27 Jan 2022 19:35:43 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e535218eecde23bcc1cc7329cf505d83f2e401ff1edefc5bbc05e0d1a5d04b39`  
		Last Modified: Fri, 28 Jan 2022 01:16:11 GMT  
		Size: 227.3 MB (227271824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a1e69ef5f77af477dee27b039a9b6c5d65be2230110d76e5d501e5d9318bbf2`  
		Last Modified: Fri, 28 Jan 2022 01:15:58 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `geonetwork:3.12.3` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:d6b77812dd3c63935ac94786f3fde7a2625d9d19774b8f4b4947899183500165
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **473.1 MB (473081985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5d62bdccd0d9f540879a1f4effa87b0d183092355a9b20c7e386f5c45920af0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 26 Jan 2022 01:42:15 GMT
ADD file:b6338a9c3c2f8d7ba1a23dcb7a1389c7d0eab75a7489ef66f21c773be56aa9ed in / 
# Wed, 26 Jan 2022 01:42:16 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:13:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:13:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Jan 2022 02:13:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 05:56:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 06:00:46 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 26 Jan 2022 06:00:48 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 26 Jan 2022 06:00:48 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 06:00:49 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jan 2022 06:00:50 GMT
ENV JAVA_VERSION=8u312
# Wed, 26 Jan 2022 06:01:01 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_x64_linux_8u312b07.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_aarch64_linux_8u312b07.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Wed, 26 Jan 2022 23:58:42 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 26 Jan 2022 23:58:43 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 23:58:44 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 26 Jan 2022 23:58:45 GMT
WORKDIR /usr/local/tomcat
# Wed, 26 Jan 2022 23:58:46 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 26 Jan 2022 23:58:47 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 27 Jan 2022 00:24:40 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 27 Jan 2022 00:24:41 GMT
ENV TOMCAT_MAJOR=8
# Thu, 27 Jan 2022 00:24:42 GMT
ENV TOMCAT_VERSION=8.5.75
# Thu, 27 Jan 2022 00:24:43 GMT
ENV TOMCAT_SHA512=b86d191506f8a647e3f4505bb7cc095068abb26bb4283562924913606514ce15930a467bd5d20c09b11d785827bf1914ed869b48dfb1c95e9f826e4c8b4e8aaa
# Thu, 27 Jan 2022 00:25:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 27 Jan 2022 00:25:48 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 27 Jan 2022 00:25:49 GMT
EXPOSE 8080
# Thu, 27 Jan 2022 00:25:50 GMT
CMD ["catalina.sh" "run"]
# Thu, 27 Jan 2022 05:09:51 GMT
ENV GN_FILE=geonetwork.war
# Thu, 27 Jan 2022 05:09:52 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Thu, 27 Jan 2022 05:09:52 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Thu, 27 Jan 2022 05:12:18 GMT
ENV GN_VERSION=3.12.3
# Thu, 27 Jan 2022 05:12:18 GMT
ENV GN_DOWNLOAD_MD5=ecbbff832c8a6edf22e06aa1870dddab
# Thu, 27 Jan 2022 05:12:19 GMT
WORKDIR /usr/local/tomcat/webapps
# Thu, 27 Jan 2022 05:15:06 GMT
RUN curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE
# Thu, 27 Jan 2022 05:15:08 GMT
COPY file:0804862fd42c05f06dfa65cb1e5dad9a956d8ac6a3ddd4d962847ba159f5cfe6 in /entrypoint.sh 
# Thu, 27 Jan 2022 05:15:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Jan 2022 05:15:09 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:39ab78bc09e79a21f719ced771689354d1948f4afd57e86afed8dac6ffb47826`  
		Last Modified: Wed, 26 Jan 2022 01:48:34 GMT  
		Size: 53.6 MB (53608848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cf88d09fc28807e643d4f619b2e0c559aaeddc7d7b8176e1144b065d63fa160`  
		Last Modified: Wed, 26 Jan 2022 02:23:47 GMT  
		Size: 5.1 MB (5141567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e019dd0368ba992803442a16cc7792c1bd5a3d06c3a1ae6fae17cb838822fb4c`  
		Last Modified: Wed, 26 Jan 2022 02:23:48 GMT  
		Size: 10.7 MB (10655902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9f1769d50d3693321e1b48f527d9c920830ad24d931b642c116bf7823bed6a`  
		Last Modified: Wed, 26 Jan 2022 02:24:10 GMT  
		Size: 54.7 MB (54669460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5cb8edd8beada37ea034ed391c47dfd106ff9cc9fac852e0f52db0b063374f`  
		Last Modified: Wed, 26 Jan 2022 06:23:05 GMT  
		Size: 5.4 MB (5420184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3973acc73ccb4db4685136c67eb73dd02f02b1518d5381cf376d82710758caa`  
		Last Modified: Wed, 26 Jan 2022 06:28:15 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:568c3474f69d85e6c2c507e089aacb5f23548845e35e993a3df6640ca80a6a61`  
		Last Modified: Wed, 26 Jan 2022 06:28:29 GMT  
		Size: 105.0 MB (105010960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c750153dc133d7b7832882e2a1e214d7e796cd23f1e59adc71cca58bd106ca1`  
		Last Modified: Thu, 27 Jan 2022 00:58:36 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd36e2060fcb58cd13a8f07504a330d6a61dbcfed5e64d211f76c6d93998d54`  
		Last Modified: Thu, 27 Jan 2022 01:16:23 GMT  
		Size: 11.3 MB (11303628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b87cb97d3e30d47e944ad2b3e55d72ef881c77a8599f906591dd8c2fcc45f56`  
		Last Modified: Thu, 27 Jan 2022 05:20:11 GMT  
		Size: 227.3 MB (227270838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:881aba0954a8e117ca330b1e1b047aa39075276fc7db40142388ccbfb0ec034f`  
		Last Modified: Thu, 27 Jan 2022 05:19:53 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `geonetwork:3.12.3-postgres`

```console
$ docker pull geonetwork@sha256:7f7959c4395c6853a248dad867133f75a1df647c527f901f61d92eebf419c040
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `geonetwork:3.12.3-postgres` - linux; amd64

```console
$ docker pull geonetwork@sha256:28be89ec28ce4bde3902d00a2cf87ec13a81bef5c6fcbeecf49ec2ae60e2103c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **479.2 MB (479239897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfc2f03558b5ccdb22ee9812d1022b2532fbf6177e6b3c87b57a8157601faf30`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:22 GMT
ADD file:9cca7f8e4abcd8309501cad216ff33a28932386ded66461a7591c0fdf2c859d3 in / 
# Wed, 26 Jan 2022 01:40:23 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:11:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:12:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Jan 2022 02:12:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:24:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:29:49 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 26 Jan 2022 09:29:50 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 26 Jan 2022 09:29:50 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 09:29:50 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jan 2022 09:29:50 GMT
ENV JAVA_VERSION=8u312
# Wed, 26 Jan 2022 09:30:47 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_x64_linux_8u312b07.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_aarch64_linux_8u312b07.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 27 Jan 2022 17:58:51 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 27 Jan 2022 17:58:51 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Jan 2022 17:58:52 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 27 Jan 2022 17:58:52 GMT
WORKDIR /usr/local/tomcat
# Thu, 27 Jan 2022 17:58:52 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 27 Jan 2022 17:58:52 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 27 Jan 2022 18:40:21 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 27 Jan 2022 18:40:22 GMT
ENV TOMCAT_MAJOR=8
# Thu, 27 Jan 2022 18:40:22 GMT
ENV TOMCAT_VERSION=8.5.75
# Thu, 27 Jan 2022 18:40:22 GMT
ENV TOMCAT_SHA512=b86d191506f8a647e3f4505bb7cc095068abb26bb4283562924913606514ce15930a467bd5d20c09b11d785827bf1914ed869b48dfb1c95e9f826e4c8b4e8aaa
# Thu, 27 Jan 2022 18:41:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 27 Jan 2022 18:41:49 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 27 Jan 2022 18:41:49 GMT
EXPOSE 8080
# Thu, 27 Jan 2022 18:41:49 GMT
CMD ["catalina.sh" "run"]
# Fri, 28 Jan 2022 00:29:11 GMT
ENV GN_FILE=geonetwork.war
# Fri, 28 Jan 2022 00:29:11 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Fri, 28 Jan 2022 00:29:11 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Fri, 28 Jan 2022 00:30:29 GMT
ENV GN_VERSION=3.12.3
# Fri, 28 Jan 2022 00:30:29 GMT
ENV GN_DOWNLOAD_MD5=ecbbff832c8a6edf22e06aa1870dddab
# Fri, 28 Jan 2022 00:30:29 GMT
WORKDIR /usr/local/tomcat/webapps
# Fri, 28 Jan 2022 01:14:38 GMT
RUN curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE
# Fri, 28 Jan 2022 01:14:39 GMT
COPY file:0804862fd42c05f06dfa65cb1e5dad9a956d8ac6a3ddd4d962847ba159f5cfe6 in /entrypoint.sh 
# Fri, 28 Jan 2022 01:14:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 28 Jan 2022 01:14:39 GMT
CMD ["catalina.sh" "run"]
# Fri, 28 Jan 2022 01:14:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jan 2022 01:14:56 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml"
# Fri, 28 Jan 2022 01:14:56 GMT
COPY file:83f69d2041e5fb378033b0db57e096c81ba0725102ab4da4f089685e748fcce3 in /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties 
# Fri, 28 Jan 2022 01:14:56 GMT
COPY file:c88411abba7ad9b7bb75019f08755dbfa163d2fc7fdd80676bf9350c4c56a19c in /entrypoint.sh 
# Fri, 28 Jan 2022 01:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 28 Jan 2022 01:14:57 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:0c6b8ff8c37e92eb1ca65ed8917e818927d5bf318b6f18896049b5d9afc28343`  
		Last Modified: Wed, 26 Jan 2022 01:46:07 GMT  
		Size: 54.9 MB (54917164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:412caad352a3ecbb29c080379407ae0761e7b9b454f7239cbfd1d1da25e06b29`  
		Last Modified: Wed, 26 Jan 2022 02:22:09 GMT  
		Size: 5.2 MB (5152685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6d3e61f7a504fa66d7275123969e9917570188650eb84b2280a726b996040f6`  
		Last Modified: Wed, 26 Jan 2022 02:22:09 GMT  
		Size: 10.9 MB (10871783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:461bb1d8c517c7f9fc0f1df66c9dc34c85a23421c1e1c540b2e28cbb258e75f5`  
		Last Modified: Wed, 26 Jan 2022 02:22:32 GMT  
		Size: 54.6 MB (54567492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e442ee9d8dd9896a5b3b67117060f2af4ae8e997af7297009e7d0ea4b6595163`  
		Last Modified: Wed, 26 Jan 2022 09:50:58 GMT  
		Size: 5.4 MB (5420014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b5bcea956cbbcc7e16356354d5eb4b5b3834a43d708ca6c3fd048f33ddc579`  
		Last Modified: Wed, 26 Jan 2022 09:55:46 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3879cb950b1f93eff09fbecc9c1d4ed3760d3f81df96b99f8090e3955578b57`  
		Last Modified: Wed, 26 Jan 2022 09:55:59 GMT  
		Size: 106.0 MB (105999002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49e3fbddb891d992809b3882c1be86760359a997fbf71f9d2d67e30abc94e65`  
		Last Modified: Thu, 27 Jan 2022 19:16:46 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7bfbc34820025e3023401808fdd9dafc703b563ec8ade714a62eaa3395acad5`  
		Last Modified: Thu, 27 Jan 2022 19:35:44 GMT  
		Size: 11.5 MB (11531982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79726cf7f4f515d435cfde8dfaa18fedb5bdfe4edc28d01da89154106b32d77`  
		Last Modified: Thu, 27 Jan 2022 19:35:43 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e535218eecde23bcc1cc7329cf505d83f2e401ff1edefc5bbc05e0d1a5d04b39`  
		Last Modified: Fri, 28 Jan 2022 01:16:11 GMT  
		Size: 227.3 MB (227271824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a1e69ef5f77af477dee27b039a9b6c5d65be2230110d76e5d501e5d9318bbf2`  
		Last Modified: Fri, 28 Jan 2022 01:15:58 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b62dadb210a914e3c38a325041dafe9c739465a9130cee94db462e7fd20a3f8`  
		Last Modified: Fri, 28 Jan 2022 01:16:27 GMT  
		Size: 3.5 MB (3503818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21d351266fb7a1d8cbf106d8b6aefece074dc5f0bff29d700ff4fe8cd5c4763d`  
		Last Modified: Fri, 28 Jan 2022 01:16:26 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48204bc4304fc8a091cd9be6d452b8e809475445582bcc3927c10d8a0c71472e`  
		Last Modified: Fri, 28 Jan 2022 01:16:26 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bea59ddb2568c53835bd9791ed31bc78fc5f3eac0c70888f1112c9791b34f4b`  
		Last Modified: Fri, 28 Jan 2022 01:16:26 GMT  
		Size: 973.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `geonetwork:3.12.3-postgres` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:f2773d655f2b71114be11fa5322a3af0776258caa1ef8f6da4957bc51674c471
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **476.3 MB (476346385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a381731898665b1e6e70b5c772c4364f76dc81a32043fb93ab4f908de0dc288e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 26 Jan 2022 01:42:15 GMT
ADD file:b6338a9c3c2f8d7ba1a23dcb7a1389c7d0eab75a7489ef66f21c773be56aa9ed in / 
# Wed, 26 Jan 2022 01:42:16 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:13:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:13:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Jan 2022 02:13:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 05:56:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 06:00:46 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 26 Jan 2022 06:00:48 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 26 Jan 2022 06:00:48 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 06:00:49 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jan 2022 06:00:50 GMT
ENV JAVA_VERSION=8u312
# Wed, 26 Jan 2022 06:01:01 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_x64_linux_8u312b07.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_aarch64_linux_8u312b07.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Wed, 26 Jan 2022 23:58:42 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 26 Jan 2022 23:58:43 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 23:58:44 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 26 Jan 2022 23:58:45 GMT
WORKDIR /usr/local/tomcat
# Wed, 26 Jan 2022 23:58:46 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 26 Jan 2022 23:58:47 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 27 Jan 2022 00:24:40 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 27 Jan 2022 00:24:41 GMT
ENV TOMCAT_MAJOR=8
# Thu, 27 Jan 2022 00:24:42 GMT
ENV TOMCAT_VERSION=8.5.75
# Thu, 27 Jan 2022 00:24:43 GMT
ENV TOMCAT_SHA512=b86d191506f8a647e3f4505bb7cc095068abb26bb4283562924913606514ce15930a467bd5d20c09b11d785827bf1914ed869b48dfb1c95e9f826e4c8b4e8aaa
# Thu, 27 Jan 2022 00:25:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 27 Jan 2022 00:25:48 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 27 Jan 2022 00:25:49 GMT
EXPOSE 8080
# Thu, 27 Jan 2022 00:25:50 GMT
CMD ["catalina.sh" "run"]
# Thu, 27 Jan 2022 05:09:51 GMT
ENV GN_FILE=geonetwork.war
# Thu, 27 Jan 2022 05:09:52 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Thu, 27 Jan 2022 05:09:52 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Thu, 27 Jan 2022 05:12:18 GMT
ENV GN_VERSION=3.12.3
# Thu, 27 Jan 2022 05:12:18 GMT
ENV GN_DOWNLOAD_MD5=ecbbff832c8a6edf22e06aa1870dddab
# Thu, 27 Jan 2022 05:12:19 GMT
WORKDIR /usr/local/tomcat/webapps
# Thu, 27 Jan 2022 05:15:06 GMT
RUN curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE
# Thu, 27 Jan 2022 05:15:08 GMT
COPY file:0804862fd42c05f06dfa65cb1e5dad9a956d8ac6a3ddd4d962847ba159f5cfe6 in /entrypoint.sh 
# Thu, 27 Jan 2022 05:15:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Jan 2022 05:15:09 GMT
CMD ["catalina.sh" "run"]
# Thu, 27 Jan 2022 05:15:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/*
# Thu, 27 Jan 2022 05:15:21 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml"
# Thu, 27 Jan 2022 05:15:22 GMT
COPY file:83f69d2041e5fb378033b0db57e096c81ba0725102ab4da4f089685e748fcce3 in /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties 
# Thu, 27 Jan 2022 05:15:23 GMT
COPY file:c88411abba7ad9b7bb75019f08755dbfa163d2fc7fdd80676bf9350c4c56a19c in /entrypoint.sh 
# Thu, 27 Jan 2022 05:15:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Jan 2022 05:15:24 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:39ab78bc09e79a21f719ced771689354d1948f4afd57e86afed8dac6ffb47826`  
		Last Modified: Wed, 26 Jan 2022 01:48:34 GMT  
		Size: 53.6 MB (53608848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cf88d09fc28807e643d4f619b2e0c559aaeddc7d7b8176e1144b065d63fa160`  
		Last Modified: Wed, 26 Jan 2022 02:23:47 GMT  
		Size: 5.1 MB (5141567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e019dd0368ba992803442a16cc7792c1bd5a3d06c3a1ae6fae17cb838822fb4c`  
		Last Modified: Wed, 26 Jan 2022 02:23:48 GMT  
		Size: 10.7 MB (10655902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9f1769d50d3693321e1b48f527d9c920830ad24d931b642c116bf7823bed6a`  
		Last Modified: Wed, 26 Jan 2022 02:24:10 GMT  
		Size: 54.7 MB (54669460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5cb8edd8beada37ea034ed391c47dfd106ff9cc9fac852e0f52db0b063374f`  
		Last Modified: Wed, 26 Jan 2022 06:23:05 GMT  
		Size: 5.4 MB (5420184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3973acc73ccb4db4685136c67eb73dd02f02b1518d5381cf376d82710758caa`  
		Last Modified: Wed, 26 Jan 2022 06:28:15 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:568c3474f69d85e6c2c507e089aacb5f23548845e35e993a3df6640ca80a6a61`  
		Last Modified: Wed, 26 Jan 2022 06:28:29 GMT  
		Size: 105.0 MB (105010960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c750153dc133d7b7832882e2a1e214d7e796cd23f1e59adc71cca58bd106ca1`  
		Last Modified: Thu, 27 Jan 2022 00:58:36 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd36e2060fcb58cd13a8f07504a330d6a61dbcfed5e64d211f76c6d93998d54`  
		Last Modified: Thu, 27 Jan 2022 01:16:23 GMT  
		Size: 11.3 MB (11303628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b87cb97d3e30d47e944ad2b3e55d72ef881c77a8599f906591dd8c2fcc45f56`  
		Last Modified: Thu, 27 Jan 2022 05:20:11 GMT  
		Size: 227.3 MB (227270838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:881aba0954a8e117ca330b1e1b047aa39075276fc7db40142388ccbfb0ec034f`  
		Last Modified: Thu, 27 Jan 2022 05:19:53 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9acebe6860978760636fd588bac693eb4beee3543ef67ef8f25cd67f7a7457f2`  
		Last Modified: Thu, 27 Jan 2022 05:20:27 GMT  
		Size: 3.3 MB (3261038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4baea3b1d826a8a216f0f9797bd95394e946a085b38d7f33b924ac3baccb4210`  
		Last Modified: Thu, 27 Jan 2022 05:20:26 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb94c323bdb05fb1ee7b2dd60cf963d12b24caca02794520d8cc92ccebf402b4`  
		Last Modified: Thu, 27 Jan 2022 05:20:26 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b8e950e474e503d01784c3b407aa7e628e6ac77eef70c7b4d1d9ca995cd497e`  
		Last Modified: Thu, 27 Jan 2022 05:20:26 GMT  
		Size: 974.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `geonetwork:4`

```console
$ docker pull geonetwork@sha256:ee2db1934b8dec0804ccb49a9ea4ac716d541c56c50a7a1fb9991d754615d2fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `geonetwork:4` - linux; amd64

```console
$ docker pull geonetwork@sha256:7661b86c13bac377b9944e240437e0ffdd66ebbfd7dd5d8ebc2f4b8ef6ef8048
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.9 MB (430865409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05d7e16621792197d8c421b9038f423057507e29834e4be72827e20c1132c5b8`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:22 GMT
ADD file:9cca7f8e4abcd8309501cad216ff33a28932386ded66461a7591c0fdf2c859d3 in / 
# Wed, 26 Jan 2022 01:40:23 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:11:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:12:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Jan 2022 09:28:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:33:06 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 26 Jan 2022 09:33:07 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 26 Jan 2022 09:33:07 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 09:33:07 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jan 2022 09:33:08 GMT
ENV JAVA_VERSION=8u312
# Wed, 26 Jan 2022 09:33:19 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jre_x64_linux_8u312b07.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jre_aarch64_linux_8u312b07.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 27 Jan 2022 16:29:37 GMT
ENV JETTY_VERSION=9.4.44.v20210927
# Thu, 27 Jan 2022 16:29:38 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 27 Jan 2022 16:29:38 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 27 Jan 2022 16:29:38 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 27 Jan 2022 16:29:38 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Jan 2022 16:29:38 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.44.v20210927/jetty-home-9.4.44.v20210927.tar.gz
# Thu, 27 Jan 2022 16:29:39 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E 	F254B35617DC255D9344BCFA873A8E86B4372146
# Thu, 27 Jan 2022 16:29:48 GMT
RUN set -xe ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		for server in 			ha.pool.sks-keyservers.net 			pgp.mit.edu 			hkp://p80.pool.sks-keyservers.net:80 			hkp://keyserver.ubuntu.com:80 			keyserver.pgp.com 			ipv4.pool.sks-keyservers.net ; 		do 			if gpg --batch --keyserver "$server" --recv-keys "$key"; then 				break; 			fi; 		done; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	mkdir -p "$TMPDIR" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Thu, 27 Jan 2022 16:29:48 GMT
WORKDIR /var/lib/jetty
# Thu, 27 Jan 2022 16:29:48 GMT
COPY multi:a6bf79f83e3ff0c7dc5946cd61ca0413cd3191ce9671725a647923d97a115fae in / 
# Thu, 27 Jan 2022 16:29:49 GMT
USER jetty
# Thu, 27 Jan 2022 16:29:49 GMT
EXPOSE 8080
# Thu, 27 Jan 2022 16:29:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 27 Jan 2022 16:29:49 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Fri, 28 Jan 2022 00:30:59 GMT
ENV DATA_DIR=/catalogue-data
# Fri, 28 Jan 2022 00:30:59 GMT
ENV JAVA_OPTS=-Dorg.eclipse.jetty.annotations.AnnotationParser.LEVEL=OFF         -Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC         -Dgeonetwork.resources.dir=/catalogue-data/resources         -Dgeonetwork.data.dir=/catalogue-data         -Dgeonetwork.codeList.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/codelist         -Dgeonetwork.schema.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/schema_plugins
# Fri, 28 Jan 2022 00:31:00 GMT
USER root
# Fri, 28 Jan 2022 00:31:03 GMT
RUN apt-get -y update &&     apt-get -y install curl &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p /${DATA_DIR} &&     chown -R jetty:jetty ${DATA_DIR} &&     mkdir -p /var/lib/jetty/webapps/geonetwork &&     chown -R jetty:jetty /var/lib/jetty/webapps/geonetwork
# Fri, 28 Jan 2022 00:31:03 GMT
USER jetty
# Fri, 28 Jan 2022 00:31:04 GMT
ENV GN_FILE=GeoNetwork-4.0.5-0.war
# Fri, 28 Jan 2022 00:31:04 GMT
ENV GN_VERSION=4.0.5
# Fri, 28 Jan 2022 00:31:04 GMT
ENV GN_DOWNLOAD_MD5=7dfcfdffc66b9a97f0d24b0769e9c3b7
# Fri, 28 Jan 2022 00:31:04 GMT
ENV LOG4J_VERSION=2.17.1
# Fri, 28 Jan 2022 00:31:04 GMT
ENV LOG4J_SHA512=b7e948df6c6f57d903d990de2cc0270c1537b711285e9b6b91280db6ace38418fced713785b2c20512dd9a4238c2d1d0ceb414d9936df2ca110ff14993ae04dc
# Fri, 28 Jan 2022 00:33:12 GMT
RUN cd /var/lib/jetty/webapps/geonetwork/ &&      curl -fSL -o geonetwork.war      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c &&      unzip -q geonetwork.war &&      rm geonetwork.war &&      rm /var/lib/jetty/webapps/geonetwork/WEB-INF/lib/log4j-core-* &&      rm /var/lib/jetty/webapps/geonetwork/WEB-INF/lib/log4j-api* &&      curl -fSL -o apache-log4j-${LOG4J_VERSION}-bin.tar.gz "https://dlcdn.apache.org/logging/log4j/${LOG4J_VERSION}/apache-log4j-${LOG4J_VERSION}-bin.tar.gz" &&      echo "${LOG4J_SHA512} apache-log4j-${LOG4J_VERSION}-bin.tar.gz" | sha512sum -c &&      tar -xvzf apache-log4j-${LOG4J_VERSION}-bin.tar.gz &&      cp apache-log4j-${LOG4J_VERSION}-bin/log4j-core-${LOG4J_VERSION}.jar /var/lib/jetty/webapps/geonetwork/WEB-INF/lib/ &&      cp apache-log4j-${LOG4J_VERSION}-bin/log4j-api-${LOG4J_VERSION}.jar /var/lib/jetty/webapps/geonetwork/WEB-INF/lib/ &&      rm -rf apache-log4j-${LOG4J_VERSION}-bin*
# Fri, 28 Jan 2022 00:33:13 GMT
COPY file:ca46ab251df3dfc253cb04cf962e7266e42428fab31ad2f583a7c86b06d5f778 in /geonetwork-entrypoint.sh 
# Fri, 28 Jan 2022 00:33:14 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Fri, 28 Jan 2022 00:33:14 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Fri, 28 Jan 2022 00:33:14 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:0c6b8ff8c37e92eb1ca65ed8917e818927d5bf318b6f18896049b5d9afc28343`  
		Last Modified: Wed, 26 Jan 2022 01:46:07 GMT  
		Size: 54.9 MB (54917164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:412caad352a3ecbb29c080379407ae0761e7b9b454f7239cbfd1d1da25e06b29`  
		Last Modified: Wed, 26 Jan 2022 02:22:09 GMT  
		Size: 5.2 MB (5152685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6d3e61f7a504fa66d7275123969e9917570188650eb84b2280a726b996040f6`  
		Last Modified: Wed, 26 Jan 2022 02:22:09 GMT  
		Size: 10.9 MB (10871783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd32ce0efa70eec9871a7cd5114ec448a2e5a97856007ca63d35543654aaa644`  
		Last Modified: Wed, 26 Jan 2022 09:54:06 GMT  
		Size: 5.7 MB (5653867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2fdf6e75af9ac9832398a018b4a214bcbd1348b7fae7f8a8525dc3b242a89a0`  
		Last Modified: Wed, 26 Jan 2022 09:57:44 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81350f39ccf12fb4beebcfb3269a90795d4408acb65eaa236d0e644a1c23de92`  
		Last Modified: Wed, 26 Jan 2022 09:57:50 GMT  
		Size: 41.4 MB (41372008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebcf5f5925571a5c7a0919e47229fbc03e77b2247b90225028d32665e5d92de3`  
		Last Modified: Thu, 27 Jan 2022 16:38:50 GMT  
		Size: 9.9 MB (9878284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56ac505b394c592a4a66ddc8d5b33c03c45356d2e9ba6efb1c3257209eb3d06`  
		Last Modified: Thu, 27 Jan 2022 16:38:50 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e36ffd507754e49f21c59a070fafa26475a6030fe479324d79772da9038ac69e`  
		Last Modified: Fri, 28 Jan 2022 00:33:30 GMT  
		Size: 511.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c87373d400033c1a0a6e08a034754357b60ec766496a1b6db966b3068d717fc`  
		Last Modified: Fri, 28 Jan 2022 00:33:47 GMT  
		Size: 303.0 MB (303016496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7685c9c3c532a1e150024afc46947cc42eb31e360bf33e06cdc7c881886ebf9d`  
		Last Modified: Fri, 28 Jan 2022 00:33:30 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `geonetwork:4` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:9ad82c890235b36b003b6ea5db7c2e6c0583b2a8ad6b73d73bcf5870d95c27c8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.6 MB (428577027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c3746fee759ee0ea16239192cf3491c7ea1f909b23b65bf4fe68dcce9d99278`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 26 Jan 2022 01:42:15 GMT
ADD file:b6338a9c3c2f8d7ba1a23dcb7a1389c7d0eab75a7489ef66f21c773be56aa9ed in / 
# Wed, 26 Jan 2022 01:42:16 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:13:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:13:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Jan 2022 05:59:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 06:03:05 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 26 Jan 2022 06:03:05 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 26 Jan 2022 06:03:06 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 06:03:07 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jan 2022 06:03:08 GMT
ENV JAVA_VERSION=8u312
# Wed, 26 Jan 2022 06:03:15 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jre_x64_linux_8u312b07.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jre_aarch64_linux_8u312b07.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Wed, 26 Jan 2022 22:18:21 GMT
ENV JETTY_VERSION=9.4.44.v20210927
# Wed, 26 Jan 2022 22:18:22 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 26 Jan 2022 22:18:23 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 26 Jan 2022 22:18:24 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 26 Jan 2022 22:18:25 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 22:18:26 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.44.v20210927/jetty-home-9.4.44.v20210927.tar.gz
# Wed, 26 Jan 2022 22:18:27 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E 	F254B35617DC255D9344BCFA873A8E86B4372146
# Wed, 26 Jan 2022 22:19:04 GMT
RUN set -xe ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		for server in 			ha.pool.sks-keyservers.net 			pgp.mit.edu 			hkp://p80.pool.sks-keyservers.net:80 			hkp://keyserver.ubuntu.com:80 			keyserver.pgp.com 			ipv4.pool.sks-keyservers.net ; 		do 			if gpg --batch --keyserver "$server" --recv-keys "$key"; then 				break; 			fi; 		done; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	mkdir -p "$TMPDIR" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Wed, 26 Jan 2022 22:19:05 GMT
WORKDIR /var/lib/jetty
# Wed, 26 Jan 2022 22:19:07 GMT
COPY multi:a6bf79f83e3ff0c7dc5946cd61ca0413cd3191ce9671725a647923d97a115fae in / 
# Wed, 26 Jan 2022 22:19:07 GMT
USER jetty
# Wed, 26 Jan 2022 22:19:08 GMT
EXPOSE 8080
# Wed, 26 Jan 2022 22:19:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 26 Jan 2022 22:19:10 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Thu, 27 Jan 2022 05:15:30 GMT
ENV DATA_DIR=/catalogue-data
# Thu, 27 Jan 2022 05:15:31 GMT
ENV JAVA_OPTS=-Dorg.eclipse.jetty.annotations.AnnotationParser.LEVEL=OFF         -Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC         -Dgeonetwork.resources.dir=/catalogue-data/resources         -Dgeonetwork.data.dir=/catalogue-data         -Dgeonetwork.codeList.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/codelist         -Dgeonetwork.schema.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/schema_plugins
# Thu, 27 Jan 2022 05:15:32 GMT
USER root
# Thu, 27 Jan 2022 05:15:36 GMT
RUN apt-get -y update &&     apt-get -y install curl &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p /${DATA_DIR} &&     chown -R jetty:jetty ${DATA_DIR} &&     mkdir -p /var/lib/jetty/webapps/geonetwork &&     chown -R jetty:jetty /var/lib/jetty/webapps/geonetwork
# Thu, 27 Jan 2022 05:15:36 GMT
USER jetty
# Thu, 27 Jan 2022 05:15:37 GMT
ENV GN_FILE=GeoNetwork-4.0.5-0.war
# Thu, 27 Jan 2022 05:15:38 GMT
ENV GN_VERSION=4.0.5
# Thu, 27 Jan 2022 05:15:39 GMT
ENV GN_DOWNLOAD_MD5=7dfcfdffc66b9a97f0d24b0769e9c3b7
# Thu, 27 Jan 2022 05:15:40 GMT
ENV LOG4J_VERSION=2.17.1
# Thu, 27 Jan 2022 05:15:41 GMT
ENV LOG4J_SHA512=b7e948df6c6f57d903d990de2cc0270c1537b711285e9b6b91280db6ace38418fced713785b2c20512dd9a4238c2d1d0ceb414d9936df2ca110ff14993ae04dc
# Thu, 27 Jan 2022 05:18:24 GMT
RUN cd /var/lib/jetty/webapps/geonetwork/ &&      curl -fSL -o geonetwork.war      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c &&      unzip -q geonetwork.war &&      rm geonetwork.war &&      rm /var/lib/jetty/webapps/geonetwork/WEB-INF/lib/log4j-core-* &&      rm /var/lib/jetty/webapps/geonetwork/WEB-INF/lib/log4j-api* &&      curl -fSL -o apache-log4j-${LOG4J_VERSION}-bin.tar.gz "https://dlcdn.apache.org/logging/log4j/${LOG4J_VERSION}/apache-log4j-${LOG4J_VERSION}-bin.tar.gz" &&      echo "${LOG4J_SHA512} apache-log4j-${LOG4J_VERSION}-bin.tar.gz" | sha512sum -c &&      tar -xvzf apache-log4j-${LOG4J_VERSION}-bin.tar.gz &&      cp apache-log4j-${LOG4J_VERSION}-bin/log4j-core-${LOG4J_VERSION}.jar /var/lib/jetty/webapps/geonetwork/WEB-INF/lib/ &&      cp apache-log4j-${LOG4J_VERSION}-bin/log4j-api-${LOG4J_VERSION}.jar /var/lib/jetty/webapps/geonetwork/WEB-INF/lib/ &&      rm -rf apache-log4j-${LOG4J_VERSION}-bin*
# Thu, 27 Jan 2022 05:18:25 GMT
COPY file:ca46ab251df3dfc253cb04cf962e7266e42428fab31ad2f583a7c86b06d5f778 in /geonetwork-entrypoint.sh 
# Thu, 27 Jan 2022 05:18:25 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Thu, 27 Jan 2022 05:18:26 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Thu, 27 Jan 2022 05:18:27 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:39ab78bc09e79a21f719ced771689354d1948f4afd57e86afed8dac6ffb47826`  
		Last Modified: Wed, 26 Jan 2022 01:48:34 GMT  
		Size: 53.6 MB (53608848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cf88d09fc28807e643d4f619b2e0c559aaeddc7d7b8176e1144b065d63fa160`  
		Last Modified: Wed, 26 Jan 2022 02:23:47 GMT  
		Size: 5.1 MB (5141567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e019dd0368ba992803442a16cc7792c1bd5a3d06c3a1ae6fae17cb838822fb4c`  
		Last Modified: Wed, 26 Jan 2022 02:23:48 GMT  
		Size: 10.7 MB (10655902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b269ee9fd3f44b0f3ecdfc14a0700e33d5979b928afd56bb96d2be690a462a6c`  
		Last Modified: Wed, 26 Jan 2022 06:26:28 GMT  
		Size: 5.6 MB (5647129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061e60dae85d85f58889066155c694663e45b4a7b85bd631802b1c53e9524fd1`  
		Last Modified: Wed, 26 Jan 2022 06:30:22 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:264ac66becd5a5f624a9c04509bb2bf08e63fa805185620694ea5e35c744ba43`  
		Last Modified: Wed, 26 Jan 2022 06:30:27 GMT  
		Size: 40.6 MB (40625393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9327a58db87bb92d4d77ef5ceeb6af898b0057da74e29c0dc5594d21b5775e9`  
		Last Modified: Wed, 26 Jan 2022 22:29:22 GMT  
		Size: 9.9 MB (9877990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52d18fca085ac0b9f79c0a24d561bcaadf22dc320997db62d05273cef072c426`  
		Last Modified: Wed, 26 Jan 2022 22:29:21 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a930eb72d6ae846bbbe1931a2636c5b0997de498d21fbfceda8e32a4d26fc032`  
		Last Modified: Thu, 27 Jan 2022 05:20:43 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f427190f16bfc83388f7c8bf25bba56613407943306f3eccfb5272ad09a16d0d`  
		Last Modified: Thu, 27 Jan 2022 05:21:05 GMT  
		Size: 303.0 MB (303017367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f301c78ad85e0dba03764e80e3b496e1a3e93745341a83d80949f5a4e313578e`  
		Last Modified: Thu, 27 Jan 2022 05:20:42 GMT  
		Size: 959.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `geonetwork:4.0`

```console
$ docker pull geonetwork@sha256:ee2db1934b8dec0804ccb49a9ea4ac716d541c56c50a7a1fb9991d754615d2fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `geonetwork:4.0` - linux; amd64

```console
$ docker pull geonetwork@sha256:7661b86c13bac377b9944e240437e0ffdd66ebbfd7dd5d8ebc2f4b8ef6ef8048
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.9 MB (430865409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05d7e16621792197d8c421b9038f423057507e29834e4be72827e20c1132c5b8`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:22 GMT
ADD file:9cca7f8e4abcd8309501cad216ff33a28932386ded66461a7591c0fdf2c859d3 in / 
# Wed, 26 Jan 2022 01:40:23 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:11:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:12:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Jan 2022 09:28:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:33:06 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 26 Jan 2022 09:33:07 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 26 Jan 2022 09:33:07 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 09:33:07 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jan 2022 09:33:08 GMT
ENV JAVA_VERSION=8u312
# Wed, 26 Jan 2022 09:33:19 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jre_x64_linux_8u312b07.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jre_aarch64_linux_8u312b07.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 27 Jan 2022 16:29:37 GMT
ENV JETTY_VERSION=9.4.44.v20210927
# Thu, 27 Jan 2022 16:29:38 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 27 Jan 2022 16:29:38 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 27 Jan 2022 16:29:38 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 27 Jan 2022 16:29:38 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Jan 2022 16:29:38 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.44.v20210927/jetty-home-9.4.44.v20210927.tar.gz
# Thu, 27 Jan 2022 16:29:39 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E 	F254B35617DC255D9344BCFA873A8E86B4372146
# Thu, 27 Jan 2022 16:29:48 GMT
RUN set -xe ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		for server in 			ha.pool.sks-keyservers.net 			pgp.mit.edu 			hkp://p80.pool.sks-keyservers.net:80 			hkp://keyserver.ubuntu.com:80 			keyserver.pgp.com 			ipv4.pool.sks-keyservers.net ; 		do 			if gpg --batch --keyserver "$server" --recv-keys "$key"; then 				break; 			fi; 		done; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	mkdir -p "$TMPDIR" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Thu, 27 Jan 2022 16:29:48 GMT
WORKDIR /var/lib/jetty
# Thu, 27 Jan 2022 16:29:48 GMT
COPY multi:a6bf79f83e3ff0c7dc5946cd61ca0413cd3191ce9671725a647923d97a115fae in / 
# Thu, 27 Jan 2022 16:29:49 GMT
USER jetty
# Thu, 27 Jan 2022 16:29:49 GMT
EXPOSE 8080
# Thu, 27 Jan 2022 16:29:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 27 Jan 2022 16:29:49 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Fri, 28 Jan 2022 00:30:59 GMT
ENV DATA_DIR=/catalogue-data
# Fri, 28 Jan 2022 00:30:59 GMT
ENV JAVA_OPTS=-Dorg.eclipse.jetty.annotations.AnnotationParser.LEVEL=OFF         -Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC         -Dgeonetwork.resources.dir=/catalogue-data/resources         -Dgeonetwork.data.dir=/catalogue-data         -Dgeonetwork.codeList.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/codelist         -Dgeonetwork.schema.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/schema_plugins
# Fri, 28 Jan 2022 00:31:00 GMT
USER root
# Fri, 28 Jan 2022 00:31:03 GMT
RUN apt-get -y update &&     apt-get -y install curl &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p /${DATA_DIR} &&     chown -R jetty:jetty ${DATA_DIR} &&     mkdir -p /var/lib/jetty/webapps/geonetwork &&     chown -R jetty:jetty /var/lib/jetty/webapps/geonetwork
# Fri, 28 Jan 2022 00:31:03 GMT
USER jetty
# Fri, 28 Jan 2022 00:31:04 GMT
ENV GN_FILE=GeoNetwork-4.0.5-0.war
# Fri, 28 Jan 2022 00:31:04 GMT
ENV GN_VERSION=4.0.5
# Fri, 28 Jan 2022 00:31:04 GMT
ENV GN_DOWNLOAD_MD5=7dfcfdffc66b9a97f0d24b0769e9c3b7
# Fri, 28 Jan 2022 00:31:04 GMT
ENV LOG4J_VERSION=2.17.1
# Fri, 28 Jan 2022 00:31:04 GMT
ENV LOG4J_SHA512=b7e948df6c6f57d903d990de2cc0270c1537b711285e9b6b91280db6ace38418fced713785b2c20512dd9a4238c2d1d0ceb414d9936df2ca110ff14993ae04dc
# Fri, 28 Jan 2022 00:33:12 GMT
RUN cd /var/lib/jetty/webapps/geonetwork/ &&      curl -fSL -o geonetwork.war      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c &&      unzip -q geonetwork.war &&      rm geonetwork.war &&      rm /var/lib/jetty/webapps/geonetwork/WEB-INF/lib/log4j-core-* &&      rm /var/lib/jetty/webapps/geonetwork/WEB-INF/lib/log4j-api* &&      curl -fSL -o apache-log4j-${LOG4J_VERSION}-bin.tar.gz "https://dlcdn.apache.org/logging/log4j/${LOG4J_VERSION}/apache-log4j-${LOG4J_VERSION}-bin.tar.gz" &&      echo "${LOG4J_SHA512} apache-log4j-${LOG4J_VERSION}-bin.tar.gz" | sha512sum -c &&      tar -xvzf apache-log4j-${LOG4J_VERSION}-bin.tar.gz &&      cp apache-log4j-${LOG4J_VERSION}-bin/log4j-core-${LOG4J_VERSION}.jar /var/lib/jetty/webapps/geonetwork/WEB-INF/lib/ &&      cp apache-log4j-${LOG4J_VERSION}-bin/log4j-api-${LOG4J_VERSION}.jar /var/lib/jetty/webapps/geonetwork/WEB-INF/lib/ &&      rm -rf apache-log4j-${LOG4J_VERSION}-bin*
# Fri, 28 Jan 2022 00:33:13 GMT
COPY file:ca46ab251df3dfc253cb04cf962e7266e42428fab31ad2f583a7c86b06d5f778 in /geonetwork-entrypoint.sh 
# Fri, 28 Jan 2022 00:33:14 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Fri, 28 Jan 2022 00:33:14 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Fri, 28 Jan 2022 00:33:14 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:0c6b8ff8c37e92eb1ca65ed8917e818927d5bf318b6f18896049b5d9afc28343`  
		Last Modified: Wed, 26 Jan 2022 01:46:07 GMT  
		Size: 54.9 MB (54917164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:412caad352a3ecbb29c080379407ae0761e7b9b454f7239cbfd1d1da25e06b29`  
		Last Modified: Wed, 26 Jan 2022 02:22:09 GMT  
		Size: 5.2 MB (5152685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6d3e61f7a504fa66d7275123969e9917570188650eb84b2280a726b996040f6`  
		Last Modified: Wed, 26 Jan 2022 02:22:09 GMT  
		Size: 10.9 MB (10871783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd32ce0efa70eec9871a7cd5114ec448a2e5a97856007ca63d35543654aaa644`  
		Last Modified: Wed, 26 Jan 2022 09:54:06 GMT  
		Size: 5.7 MB (5653867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2fdf6e75af9ac9832398a018b4a214bcbd1348b7fae7f8a8525dc3b242a89a0`  
		Last Modified: Wed, 26 Jan 2022 09:57:44 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81350f39ccf12fb4beebcfb3269a90795d4408acb65eaa236d0e644a1c23de92`  
		Last Modified: Wed, 26 Jan 2022 09:57:50 GMT  
		Size: 41.4 MB (41372008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebcf5f5925571a5c7a0919e47229fbc03e77b2247b90225028d32665e5d92de3`  
		Last Modified: Thu, 27 Jan 2022 16:38:50 GMT  
		Size: 9.9 MB (9878284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56ac505b394c592a4a66ddc8d5b33c03c45356d2e9ba6efb1c3257209eb3d06`  
		Last Modified: Thu, 27 Jan 2022 16:38:50 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e36ffd507754e49f21c59a070fafa26475a6030fe479324d79772da9038ac69e`  
		Last Modified: Fri, 28 Jan 2022 00:33:30 GMT  
		Size: 511.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c87373d400033c1a0a6e08a034754357b60ec766496a1b6db966b3068d717fc`  
		Last Modified: Fri, 28 Jan 2022 00:33:47 GMT  
		Size: 303.0 MB (303016496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7685c9c3c532a1e150024afc46947cc42eb31e360bf33e06cdc7c881886ebf9d`  
		Last Modified: Fri, 28 Jan 2022 00:33:30 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `geonetwork:4.0` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:9ad82c890235b36b003b6ea5db7c2e6c0583b2a8ad6b73d73bcf5870d95c27c8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.6 MB (428577027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c3746fee759ee0ea16239192cf3491c7ea1f909b23b65bf4fe68dcce9d99278`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 26 Jan 2022 01:42:15 GMT
ADD file:b6338a9c3c2f8d7ba1a23dcb7a1389c7d0eab75a7489ef66f21c773be56aa9ed in / 
# Wed, 26 Jan 2022 01:42:16 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:13:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:13:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Jan 2022 05:59:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 06:03:05 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 26 Jan 2022 06:03:05 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 26 Jan 2022 06:03:06 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 06:03:07 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jan 2022 06:03:08 GMT
ENV JAVA_VERSION=8u312
# Wed, 26 Jan 2022 06:03:15 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jre_x64_linux_8u312b07.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jre_aarch64_linux_8u312b07.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Wed, 26 Jan 2022 22:18:21 GMT
ENV JETTY_VERSION=9.4.44.v20210927
# Wed, 26 Jan 2022 22:18:22 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 26 Jan 2022 22:18:23 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 26 Jan 2022 22:18:24 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 26 Jan 2022 22:18:25 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 22:18:26 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.44.v20210927/jetty-home-9.4.44.v20210927.tar.gz
# Wed, 26 Jan 2022 22:18:27 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E 	F254B35617DC255D9344BCFA873A8E86B4372146
# Wed, 26 Jan 2022 22:19:04 GMT
RUN set -xe ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		for server in 			ha.pool.sks-keyservers.net 			pgp.mit.edu 			hkp://p80.pool.sks-keyservers.net:80 			hkp://keyserver.ubuntu.com:80 			keyserver.pgp.com 			ipv4.pool.sks-keyservers.net ; 		do 			if gpg --batch --keyserver "$server" --recv-keys "$key"; then 				break; 			fi; 		done; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	mkdir -p "$TMPDIR" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Wed, 26 Jan 2022 22:19:05 GMT
WORKDIR /var/lib/jetty
# Wed, 26 Jan 2022 22:19:07 GMT
COPY multi:a6bf79f83e3ff0c7dc5946cd61ca0413cd3191ce9671725a647923d97a115fae in / 
# Wed, 26 Jan 2022 22:19:07 GMT
USER jetty
# Wed, 26 Jan 2022 22:19:08 GMT
EXPOSE 8080
# Wed, 26 Jan 2022 22:19:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 26 Jan 2022 22:19:10 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Thu, 27 Jan 2022 05:15:30 GMT
ENV DATA_DIR=/catalogue-data
# Thu, 27 Jan 2022 05:15:31 GMT
ENV JAVA_OPTS=-Dorg.eclipse.jetty.annotations.AnnotationParser.LEVEL=OFF         -Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC         -Dgeonetwork.resources.dir=/catalogue-data/resources         -Dgeonetwork.data.dir=/catalogue-data         -Dgeonetwork.codeList.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/codelist         -Dgeonetwork.schema.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/schema_plugins
# Thu, 27 Jan 2022 05:15:32 GMT
USER root
# Thu, 27 Jan 2022 05:15:36 GMT
RUN apt-get -y update &&     apt-get -y install curl &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p /${DATA_DIR} &&     chown -R jetty:jetty ${DATA_DIR} &&     mkdir -p /var/lib/jetty/webapps/geonetwork &&     chown -R jetty:jetty /var/lib/jetty/webapps/geonetwork
# Thu, 27 Jan 2022 05:15:36 GMT
USER jetty
# Thu, 27 Jan 2022 05:15:37 GMT
ENV GN_FILE=GeoNetwork-4.0.5-0.war
# Thu, 27 Jan 2022 05:15:38 GMT
ENV GN_VERSION=4.0.5
# Thu, 27 Jan 2022 05:15:39 GMT
ENV GN_DOWNLOAD_MD5=7dfcfdffc66b9a97f0d24b0769e9c3b7
# Thu, 27 Jan 2022 05:15:40 GMT
ENV LOG4J_VERSION=2.17.1
# Thu, 27 Jan 2022 05:15:41 GMT
ENV LOG4J_SHA512=b7e948df6c6f57d903d990de2cc0270c1537b711285e9b6b91280db6ace38418fced713785b2c20512dd9a4238c2d1d0ceb414d9936df2ca110ff14993ae04dc
# Thu, 27 Jan 2022 05:18:24 GMT
RUN cd /var/lib/jetty/webapps/geonetwork/ &&      curl -fSL -o geonetwork.war      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c &&      unzip -q geonetwork.war &&      rm geonetwork.war &&      rm /var/lib/jetty/webapps/geonetwork/WEB-INF/lib/log4j-core-* &&      rm /var/lib/jetty/webapps/geonetwork/WEB-INF/lib/log4j-api* &&      curl -fSL -o apache-log4j-${LOG4J_VERSION}-bin.tar.gz "https://dlcdn.apache.org/logging/log4j/${LOG4J_VERSION}/apache-log4j-${LOG4J_VERSION}-bin.tar.gz" &&      echo "${LOG4J_SHA512} apache-log4j-${LOG4J_VERSION}-bin.tar.gz" | sha512sum -c &&      tar -xvzf apache-log4j-${LOG4J_VERSION}-bin.tar.gz &&      cp apache-log4j-${LOG4J_VERSION}-bin/log4j-core-${LOG4J_VERSION}.jar /var/lib/jetty/webapps/geonetwork/WEB-INF/lib/ &&      cp apache-log4j-${LOG4J_VERSION}-bin/log4j-api-${LOG4J_VERSION}.jar /var/lib/jetty/webapps/geonetwork/WEB-INF/lib/ &&      rm -rf apache-log4j-${LOG4J_VERSION}-bin*
# Thu, 27 Jan 2022 05:18:25 GMT
COPY file:ca46ab251df3dfc253cb04cf962e7266e42428fab31ad2f583a7c86b06d5f778 in /geonetwork-entrypoint.sh 
# Thu, 27 Jan 2022 05:18:25 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Thu, 27 Jan 2022 05:18:26 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Thu, 27 Jan 2022 05:18:27 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:39ab78bc09e79a21f719ced771689354d1948f4afd57e86afed8dac6ffb47826`  
		Last Modified: Wed, 26 Jan 2022 01:48:34 GMT  
		Size: 53.6 MB (53608848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cf88d09fc28807e643d4f619b2e0c559aaeddc7d7b8176e1144b065d63fa160`  
		Last Modified: Wed, 26 Jan 2022 02:23:47 GMT  
		Size: 5.1 MB (5141567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e019dd0368ba992803442a16cc7792c1bd5a3d06c3a1ae6fae17cb838822fb4c`  
		Last Modified: Wed, 26 Jan 2022 02:23:48 GMT  
		Size: 10.7 MB (10655902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b269ee9fd3f44b0f3ecdfc14a0700e33d5979b928afd56bb96d2be690a462a6c`  
		Last Modified: Wed, 26 Jan 2022 06:26:28 GMT  
		Size: 5.6 MB (5647129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061e60dae85d85f58889066155c694663e45b4a7b85bd631802b1c53e9524fd1`  
		Last Modified: Wed, 26 Jan 2022 06:30:22 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:264ac66becd5a5f624a9c04509bb2bf08e63fa805185620694ea5e35c744ba43`  
		Last Modified: Wed, 26 Jan 2022 06:30:27 GMT  
		Size: 40.6 MB (40625393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9327a58db87bb92d4d77ef5ceeb6af898b0057da74e29c0dc5594d21b5775e9`  
		Last Modified: Wed, 26 Jan 2022 22:29:22 GMT  
		Size: 9.9 MB (9877990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52d18fca085ac0b9f79c0a24d561bcaadf22dc320997db62d05273cef072c426`  
		Last Modified: Wed, 26 Jan 2022 22:29:21 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a930eb72d6ae846bbbe1931a2636c5b0997de498d21fbfceda8e32a4d26fc032`  
		Last Modified: Thu, 27 Jan 2022 05:20:43 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f427190f16bfc83388f7c8bf25bba56613407943306f3eccfb5272ad09a16d0d`  
		Last Modified: Thu, 27 Jan 2022 05:21:05 GMT  
		Size: 303.0 MB (303017367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f301c78ad85e0dba03764e80e3b496e1a3e93745341a83d80949f5a4e313578e`  
		Last Modified: Thu, 27 Jan 2022 05:20:42 GMT  
		Size: 959.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `geonetwork:4.0.6`

```console
$ docker pull geonetwork@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 0

## `geonetwork:latest`

```console
$ docker pull geonetwork@sha256:ee2db1934b8dec0804ccb49a9ea4ac716d541c56c50a7a1fb9991d754615d2fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `geonetwork:latest` - linux; amd64

```console
$ docker pull geonetwork@sha256:7661b86c13bac377b9944e240437e0ffdd66ebbfd7dd5d8ebc2f4b8ef6ef8048
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.9 MB (430865409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05d7e16621792197d8c421b9038f423057507e29834e4be72827e20c1132c5b8`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:22 GMT
ADD file:9cca7f8e4abcd8309501cad216ff33a28932386ded66461a7591c0fdf2c859d3 in / 
# Wed, 26 Jan 2022 01:40:23 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:11:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:12:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Jan 2022 09:28:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:33:06 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 26 Jan 2022 09:33:07 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 26 Jan 2022 09:33:07 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 09:33:07 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jan 2022 09:33:08 GMT
ENV JAVA_VERSION=8u312
# Wed, 26 Jan 2022 09:33:19 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jre_x64_linux_8u312b07.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jre_aarch64_linux_8u312b07.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 27 Jan 2022 16:29:37 GMT
ENV JETTY_VERSION=9.4.44.v20210927
# Thu, 27 Jan 2022 16:29:38 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 27 Jan 2022 16:29:38 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 27 Jan 2022 16:29:38 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 27 Jan 2022 16:29:38 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Jan 2022 16:29:38 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.44.v20210927/jetty-home-9.4.44.v20210927.tar.gz
# Thu, 27 Jan 2022 16:29:39 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E 	F254B35617DC255D9344BCFA873A8E86B4372146
# Thu, 27 Jan 2022 16:29:48 GMT
RUN set -xe ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		for server in 			ha.pool.sks-keyservers.net 			pgp.mit.edu 			hkp://p80.pool.sks-keyservers.net:80 			hkp://keyserver.ubuntu.com:80 			keyserver.pgp.com 			ipv4.pool.sks-keyservers.net ; 		do 			if gpg --batch --keyserver "$server" --recv-keys "$key"; then 				break; 			fi; 		done; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	mkdir -p "$TMPDIR" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Thu, 27 Jan 2022 16:29:48 GMT
WORKDIR /var/lib/jetty
# Thu, 27 Jan 2022 16:29:48 GMT
COPY multi:a6bf79f83e3ff0c7dc5946cd61ca0413cd3191ce9671725a647923d97a115fae in / 
# Thu, 27 Jan 2022 16:29:49 GMT
USER jetty
# Thu, 27 Jan 2022 16:29:49 GMT
EXPOSE 8080
# Thu, 27 Jan 2022 16:29:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 27 Jan 2022 16:29:49 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Fri, 28 Jan 2022 00:30:59 GMT
ENV DATA_DIR=/catalogue-data
# Fri, 28 Jan 2022 00:30:59 GMT
ENV JAVA_OPTS=-Dorg.eclipse.jetty.annotations.AnnotationParser.LEVEL=OFF         -Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC         -Dgeonetwork.resources.dir=/catalogue-data/resources         -Dgeonetwork.data.dir=/catalogue-data         -Dgeonetwork.codeList.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/codelist         -Dgeonetwork.schema.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/schema_plugins
# Fri, 28 Jan 2022 00:31:00 GMT
USER root
# Fri, 28 Jan 2022 00:31:03 GMT
RUN apt-get -y update &&     apt-get -y install curl &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p /${DATA_DIR} &&     chown -R jetty:jetty ${DATA_DIR} &&     mkdir -p /var/lib/jetty/webapps/geonetwork &&     chown -R jetty:jetty /var/lib/jetty/webapps/geonetwork
# Fri, 28 Jan 2022 00:31:03 GMT
USER jetty
# Fri, 28 Jan 2022 00:31:04 GMT
ENV GN_FILE=GeoNetwork-4.0.5-0.war
# Fri, 28 Jan 2022 00:31:04 GMT
ENV GN_VERSION=4.0.5
# Fri, 28 Jan 2022 00:31:04 GMT
ENV GN_DOWNLOAD_MD5=7dfcfdffc66b9a97f0d24b0769e9c3b7
# Fri, 28 Jan 2022 00:31:04 GMT
ENV LOG4J_VERSION=2.17.1
# Fri, 28 Jan 2022 00:31:04 GMT
ENV LOG4J_SHA512=b7e948df6c6f57d903d990de2cc0270c1537b711285e9b6b91280db6ace38418fced713785b2c20512dd9a4238c2d1d0ceb414d9936df2ca110ff14993ae04dc
# Fri, 28 Jan 2022 00:33:12 GMT
RUN cd /var/lib/jetty/webapps/geonetwork/ &&      curl -fSL -o geonetwork.war      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c &&      unzip -q geonetwork.war &&      rm geonetwork.war &&      rm /var/lib/jetty/webapps/geonetwork/WEB-INF/lib/log4j-core-* &&      rm /var/lib/jetty/webapps/geonetwork/WEB-INF/lib/log4j-api* &&      curl -fSL -o apache-log4j-${LOG4J_VERSION}-bin.tar.gz "https://dlcdn.apache.org/logging/log4j/${LOG4J_VERSION}/apache-log4j-${LOG4J_VERSION}-bin.tar.gz" &&      echo "${LOG4J_SHA512} apache-log4j-${LOG4J_VERSION}-bin.tar.gz" | sha512sum -c &&      tar -xvzf apache-log4j-${LOG4J_VERSION}-bin.tar.gz &&      cp apache-log4j-${LOG4J_VERSION}-bin/log4j-core-${LOG4J_VERSION}.jar /var/lib/jetty/webapps/geonetwork/WEB-INF/lib/ &&      cp apache-log4j-${LOG4J_VERSION}-bin/log4j-api-${LOG4J_VERSION}.jar /var/lib/jetty/webapps/geonetwork/WEB-INF/lib/ &&      rm -rf apache-log4j-${LOG4J_VERSION}-bin*
# Fri, 28 Jan 2022 00:33:13 GMT
COPY file:ca46ab251df3dfc253cb04cf962e7266e42428fab31ad2f583a7c86b06d5f778 in /geonetwork-entrypoint.sh 
# Fri, 28 Jan 2022 00:33:14 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Fri, 28 Jan 2022 00:33:14 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Fri, 28 Jan 2022 00:33:14 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:0c6b8ff8c37e92eb1ca65ed8917e818927d5bf318b6f18896049b5d9afc28343`  
		Last Modified: Wed, 26 Jan 2022 01:46:07 GMT  
		Size: 54.9 MB (54917164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:412caad352a3ecbb29c080379407ae0761e7b9b454f7239cbfd1d1da25e06b29`  
		Last Modified: Wed, 26 Jan 2022 02:22:09 GMT  
		Size: 5.2 MB (5152685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6d3e61f7a504fa66d7275123969e9917570188650eb84b2280a726b996040f6`  
		Last Modified: Wed, 26 Jan 2022 02:22:09 GMT  
		Size: 10.9 MB (10871783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd32ce0efa70eec9871a7cd5114ec448a2e5a97856007ca63d35543654aaa644`  
		Last Modified: Wed, 26 Jan 2022 09:54:06 GMT  
		Size: 5.7 MB (5653867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2fdf6e75af9ac9832398a018b4a214bcbd1348b7fae7f8a8525dc3b242a89a0`  
		Last Modified: Wed, 26 Jan 2022 09:57:44 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81350f39ccf12fb4beebcfb3269a90795d4408acb65eaa236d0e644a1c23de92`  
		Last Modified: Wed, 26 Jan 2022 09:57:50 GMT  
		Size: 41.4 MB (41372008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebcf5f5925571a5c7a0919e47229fbc03e77b2247b90225028d32665e5d92de3`  
		Last Modified: Thu, 27 Jan 2022 16:38:50 GMT  
		Size: 9.9 MB (9878284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56ac505b394c592a4a66ddc8d5b33c03c45356d2e9ba6efb1c3257209eb3d06`  
		Last Modified: Thu, 27 Jan 2022 16:38:50 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e36ffd507754e49f21c59a070fafa26475a6030fe479324d79772da9038ac69e`  
		Last Modified: Fri, 28 Jan 2022 00:33:30 GMT  
		Size: 511.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c87373d400033c1a0a6e08a034754357b60ec766496a1b6db966b3068d717fc`  
		Last Modified: Fri, 28 Jan 2022 00:33:47 GMT  
		Size: 303.0 MB (303016496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7685c9c3c532a1e150024afc46947cc42eb31e360bf33e06cdc7c881886ebf9d`  
		Last Modified: Fri, 28 Jan 2022 00:33:30 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `geonetwork:latest` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:9ad82c890235b36b003b6ea5db7c2e6c0583b2a8ad6b73d73bcf5870d95c27c8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.6 MB (428577027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c3746fee759ee0ea16239192cf3491c7ea1f909b23b65bf4fe68dcce9d99278`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 26 Jan 2022 01:42:15 GMT
ADD file:b6338a9c3c2f8d7ba1a23dcb7a1389c7d0eab75a7489ef66f21c773be56aa9ed in / 
# Wed, 26 Jan 2022 01:42:16 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:13:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:13:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Jan 2022 05:59:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 06:03:05 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 26 Jan 2022 06:03:05 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 26 Jan 2022 06:03:06 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 06:03:07 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jan 2022 06:03:08 GMT
ENV JAVA_VERSION=8u312
# Wed, 26 Jan 2022 06:03:15 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jre_x64_linux_8u312b07.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jre_aarch64_linux_8u312b07.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Wed, 26 Jan 2022 22:18:21 GMT
ENV JETTY_VERSION=9.4.44.v20210927
# Wed, 26 Jan 2022 22:18:22 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 26 Jan 2022 22:18:23 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 26 Jan 2022 22:18:24 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 26 Jan 2022 22:18:25 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 22:18:26 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.44.v20210927/jetty-home-9.4.44.v20210927.tar.gz
# Wed, 26 Jan 2022 22:18:27 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E 	F254B35617DC255D9344BCFA873A8E86B4372146
# Wed, 26 Jan 2022 22:19:04 GMT
RUN set -xe ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		for server in 			ha.pool.sks-keyservers.net 			pgp.mit.edu 			hkp://p80.pool.sks-keyservers.net:80 			hkp://keyserver.ubuntu.com:80 			keyserver.pgp.com 			ipv4.pool.sks-keyservers.net ; 		do 			if gpg --batch --keyserver "$server" --recv-keys "$key"; then 				break; 			fi; 		done; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	mkdir -p "$TMPDIR" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Wed, 26 Jan 2022 22:19:05 GMT
WORKDIR /var/lib/jetty
# Wed, 26 Jan 2022 22:19:07 GMT
COPY multi:a6bf79f83e3ff0c7dc5946cd61ca0413cd3191ce9671725a647923d97a115fae in / 
# Wed, 26 Jan 2022 22:19:07 GMT
USER jetty
# Wed, 26 Jan 2022 22:19:08 GMT
EXPOSE 8080
# Wed, 26 Jan 2022 22:19:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 26 Jan 2022 22:19:10 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Thu, 27 Jan 2022 05:15:30 GMT
ENV DATA_DIR=/catalogue-data
# Thu, 27 Jan 2022 05:15:31 GMT
ENV JAVA_OPTS=-Dorg.eclipse.jetty.annotations.AnnotationParser.LEVEL=OFF         -Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC         -Dgeonetwork.resources.dir=/catalogue-data/resources         -Dgeonetwork.data.dir=/catalogue-data         -Dgeonetwork.codeList.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/codelist         -Dgeonetwork.schema.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/schema_plugins
# Thu, 27 Jan 2022 05:15:32 GMT
USER root
# Thu, 27 Jan 2022 05:15:36 GMT
RUN apt-get -y update &&     apt-get -y install curl &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p /${DATA_DIR} &&     chown -R jetty:jetty ${DATA_DIR} &&     mkdir -p /var/lib/jetty/webapps/geonetwork &&     chown -R jetty:jetty /var/lib/jetty/webapps/geonetwork
# Thu, 27 Jan 2022 05:15:36 GMT
USER jetty
# Thu, 27 Jan 2022 05:15:37 GMT
ENV GN_FILE=GeoNetwork-4.0.5-0.war
# Thu, 27 Jan 2022 05:15:38 GMT
ENV GN_VERSION=4.0.5
# Thu, 27 Jan 2022 05:15:39 GMT
ENV GN_DOWNLOAD_MD5=7dfcfdffc66b9a97f0d24b0769e9c3b7
# Thu, 27 Jan 2022 05:15:40 GMT
ENV LOG4J_VERSION=2.17.1
# Thu, 27 Jan 2022 05:15:41 GMT
ENV LOG4J_SHA512=b7e948df6c6f57d903d990de2cc0270c1537b711285e9b6b91280db6ace38418fced713785b2c20512dd9a4238c2d1d0ceb414d9936df2ca110ff14993ae04dc
# Thu, 27 Jan 2022 05:18:24 GMT
RUN cd /var/lib/jetty/webapps/geonetwork/ &&      curl -fSL -o geonetwork.war      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c &&      unzip -q geonetwork.war &&      rm geonetwork.war &&      rm /var/lib/jetty/webapps/geonetwork/WEB-INF/lib/log4j-core-* &&      rm /var/lib/jetty/webapps/geonetwork/WEB-INF/lib/log4j-api* &&      curl -fSL -o apache-log4j-${LOG4J_VERSION}-bin.tar.gz "https://dlcdn.apache.org/logging/log4j/${LOG4J_VERSION}/apache-log4j-${LOG4J_VERSION}-bin.tar.gz" &&      echo "${LOG4J_SHA512} apache-log4j-${LOG4J_VERSION}-bin.tar.gz" | sha512sum -c &&      tar -xvzf apache-log4j-${LOG4J_VERSION}-bin.tar.gz &&      cp apache-log4j-${LOG4J_VERSION}-bin/log4j-core-${LOG4J_VERSION}.jar /var/lib/jetty/webapps/geonetwork/WEB-INF/lib/ &&      cp apache-log4j-${LOG4J_VERSION}-bin/log4j-api-${LOG4J_VERSION}.jar /var/lib/jetty/webapps/geonetwork/WEB-INF/lib/ &&      rm -rf apache-log4j-${LOG4J_VERSION}-bin*
# Thu, 27 Jan 2022 05:18:25 GMT
COPY file:ca46ab251df3dfc253cb04cf962e7266e42428fab31ad2f583a7c86b06d5f778 in /geonetwork-entrypoint.sh 
# Thu, 27 Jan 2022 05:18:25 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Thu, 27 Jan 2022 05:18:26 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Thu, 27 Jan 2022 05:18:27 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:39ab78bc09e79a21f719ced771689354d1948f4afd57e86afed8dac6ffb47826`  
		Last Modified: Wed, 26 Jan 2022 01:48:34 GMT  
		Size: 53.6 MB (53608848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cf88d09fc28807e643d4f619b2e0c559aaeddc7d7b8176e1144b065d63fa160`  
		Last Modified: Wed, 26 Jan 2022 02:23:47 GMT  
		Size: 5.1 MB (5141567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e019dd0368ba992803442a16cc7792c1bd5a3d06c3a1ae6fae17cb838822fb4c`  
		Last Modified: Wed, 26 Jan 2022 02:23:48 GMT  
		Size: 10.7 MB (10655902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b269ee9fd3f44b0f3ecdfc14a0700e33d5979b928afd56bb96d2be690a462a6c`  
		Last Modified: Wed, 26 Jan 2022 06:26:28 GMT  
		Size: 5.6 MB (5647129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061e60dae85d85f58889066155c694663e45b4a7b85bd631802b1c53e9524fd1`  
		Last Modified: Wed, 26 Jan 2022 06:30:22 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:264ac66becd5a5f624a9c04509bb2bf08e63fa805185620694ea5e35c744ba43`  
		Last Modified: Wed, 26 Jan 2022 06:30:27 GMT  
		Size: 40.6 MB (40625393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9327a58db87bb92d4d77ef5ceeb6af898b0057da74e29c0dc5594d21b5775e9`  
		Last Modified: Wed, 26 Jan 2022 22:29:22 GMT  
		Size: 9.9 MB (9877990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52d18fca085ac0b9f79c0a24d561bcaadf22dc320997db62d05273cef072c426`  
		Last Modified: Wed, 26 Jan 2022 22:29:21 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a930eb72d6ae846bbbe1931a2636c5b0997de498d21fbfceda8e32a4d26fc032`  
		Last Modified: Thu, 27 Jan 2022 05:20:43 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f427190f16bfc83388f7c8bf25bba56613407943306f3eccfb5272ad09a16d0d`  
		Last Modified: Thu, 27 Jan 2022 05:21:05 GMT  
		Size: 303.0 MB (303017367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f301c78ad85e0dba03764e80e3b496e1a3e93745341a83d80949f5a4e313578e`  
		Last Modified: Thu, 27 Jan 2022 05:20:42 GMT  
		Size: 959.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
