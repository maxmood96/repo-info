## `tomcat:10-jdk21-openjdk-bookworm`

```console
$ docker pull tomcat@sha256:2286be38094997ec0ffd61c0a6e2faaa1c1859229b60e3c983183e4f0355395f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:10-jdk21-openjdk-bookworm` - linux; amd64

```console
$ docker pull tomcat@sha256:5b868aa970b9eac591d89faf12b556627dc815167325d57bedacfc3fefc354ad
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.2 MB (371151676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac2862cef175e0acf2e476874b996045e504ef691261013ef201ace5fb3bd41f`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 12 Jun 2023 23:20:28 GMT
ADD file:98cacc5890a8c0b29d7a2b296774428cb2268b01b4ff97a84deadcd3b513f319 in / 
# Mon, 12 Jun 2023 23:20:29 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 03:26:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 03:27:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 18:42:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 18:43:06 GMT
ENV JAVA_HOME=/usr/local/openjdk-21
# Tue, 13 Jun 2023 18:43:06 GMT
ENV PATH=/usr/local/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jun 2023 18:43:06 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jun 2023 01:14:40 GMT
ENV JAVA_VERSION=21-ea+27
# Wed, 21 Jun 2023 01:14:51 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/27/GPL/openjdk-21-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='686f2ed6faecd9b5be0306df695bafa576758f00efc51b2250a8044a31ddc9af'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/27/GPL/openjdk-21-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='f6b6f664146527de70f9dcb2d424cf91c6429a41c6e19e9b940819fdfc73aba4'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 21 Jun 2023 01:14:52 GMT
CMD ["jshell"]
# Wed, 21 Jun 2023 01:39:37 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 21 Jun 2023 01:39:37 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Jun 2023 01:39:38 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 21 Jun 2023 01:39:38 GMT
WORKDIR /usr/local/tomcat
# Wed, 21 Jun 2023 01:39:38 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 21 Jun 2023 01:39:38 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 21 Jun 2023 01:40:47 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 21 Jun 2023 01:40:47 GMT
ENV TOMCAT_MAJOR=10
# Wed, 21 Jun 2023 01:40:47 GMT
ENV TOMCAT_VERSION=10.1.10
# Wed, 21 Jun 2023 01:40:47 GMT
ENV TOMCAT_SHA512=be35edeb7f63be2d087da6b5cf3c1250eb5fbaa484ba788870780109278d1f5607bf8dfb40f718beda82352109c131fc97f7907f5521dc462bd60773b33e2c68
# Wed, 21 Jun 2023 01:41:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version
# Wed, 21 Jun 2023 01:41:07 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 21 Jun 2023 01:41:07 GMT
EXPOSE 8080
# Wed, 21 Jun 2023 01:41:08 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:bba7bb10d5baebcaad1d68ab3cbfd37390c646b2a688529b1d118a47991116f4`  
		Last Modified: Mon, 12 Jun 2023 23:25:26 GMT  
		Size: 49.6 MB (49552112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec2b820b8e87758dde67c29b25d4cbf88377601a4355cc5d556a9beebc80da00`  
		Last Modified: Tue, 13 Jun 2023 03:36:28 GMT  
		Size: 24.0 MB (24030539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:284f2345db055020282f6e80a646f1111fb2d5dfc6f7ee871f89bc50919a51bf`  
		Last Modified: Tue, 13 Jun 2023 03:36:47 GMT  
		Size: 64.1 MB (64111555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9350d4cb97cd74af4173b0a47cb308cd97cec7c6d33e7f66f37adf410f7b5d31`  
		Last Modified: Tue, 13 Jun 2023 18:44:35 GMT  
		Size: 16.9 MB (16947115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ac0e603fd06ce9c1edb7b0555cd638b7f13f4cf8a9b10d040b2babe19f711cc`  
		Last Modified: Wed, 21 Jun 2023 01:21:55 GMT  
		Size: 203.9 MB (203944467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1009f27a77633c7b9d4519642467204c35921a41bd21626349491e7582a92a7b`  
		Last Modified: Wed, 21 Jun 2023 01:49:32 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50afe0fff65b6c6efd7ebca0a0524522055c9318d05b529dde5cdd34eaeac429`  
		Last Modified: Wed, 21 Jun 2023 01:50:07 GMT  
		Size: 12.6 MB (12565588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ade99d27188aee5ce9a3e07145d43b2621a21e86b12ff493c97f6e844b8391d`  
		Last Modified: Wed, 21 Jun 2023 01:50:05 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:10-jdk21-openjdk-bookworm` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:e38d671a5c20eb75e08963bf7ef82f5189063026486a111db6e79efe6b416430
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.7 MB (369715087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cd8ad3130159b884a5b7a3a868da32ab779d3a8cfac8b8fa83e4f6b83e52d97`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 12 Jun 2023 23:39:59 GMT
ADD file:0dfaa4beac7b0a95f2b33bc35e08b104057469f46fa35df2af7193451ab3714d in / 
# Mon, 12 Jun 2023 23:40:00 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 02:58:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 02:59:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 18:27:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 18:27:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-21
# Tue, 13 Jun 2023 18:27:56 GMT
ENV PATH=/usr/local/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jun 2023 18:27:56 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jun 2023 01:15:39 GMT
ENV JAVA_VERSION=21-ea+27
# Wed, 21 Jun 2023 01:15:47 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/27/GPL/openjdk-21-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='686f2ed6faecd9b5be0306df695bafa576758f00efc51b2250a8044a31ddc9af'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/27/GPL/openjdk-21-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='f6b6f664146527de70f9dcb2d424cf91c6429a41c6e19e9b940819fdfc73aba4'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 21 Jun 2023 01:15:49 GMT
CMD ["jshell"]
# Wed, 21 Jun 2023 01:42:47 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 21 Jun 2023 01:42:47 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Jun 2023 01:42:48 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 21 Jun 2023 01:42:48 GMT
WORKDIR /usr/local/tomcat
# Wed, 21 Jun 2023 01:42:48 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 21 Jun 2023 01:42:48 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 21 Jun 2023 01:43:51 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 21 Jun 2023 01:43:51 GMT
ENV TOMCAT_MAJOR=10
# Wed, 21 Jun 2023 01:43:51 GMT
ENV TOMCAT_VERSION=10.1.10
# Wed, 21 Jun 2023 01:43:51 GMT
ENV TOMCAT_SHA512=be35edeb7f63be2d087da6b5cf3c1250eb5fbaa484ba788870780109278d1f5607bf8dfb40f718beda82352109c131fc97f7907f5521dc462bd60773b33e2c68
# Wed, 21 Jun 2023 01:44:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version
# Wed, 21 Jun 2023 01:44:08 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 21 Jun 2023 01:44:08 GMT
EXPOSE 8080
# Wed, 21 Jun 2023 01:44:08 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:a31111d070044ed920abddebc16bfa67a69fb0e0e782b703073c93ec10dedf67`  
		Last Modified: Mon, 12 Jun 2023 23:43:47 GMT  
		Size: 49.6 MB (49573162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2455b35210792787557bbd2b0b976aa27a8bd5931191be95c7291b93b9e38f6c`  
		Last Modified: Tue, 13 Jun 2023 03:07:36 GMT  
		Size: 23.6 MB (23569494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd13397d6ccd754586b475131a51ebeb69394eb49de84b647f4fb6a38703da89`  
		Last Modified: Tue, 13 Jun 2023 03:07:53 GMT  
		Size: 64.0 MB (63983834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a8c967ff35ea3c019c6a9818d32a376ba3b75b94ba824f757a0d12df5614c3`  
		Last Modified: Tue, 13 Jun 2023 18:29:20 GMT  
		Size: 17.7 MB (17728902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd47e4930b89e4bf1725c246fd20ed7b22e4420d28537cfe05687ee37babfb22`  
		Last Modified: Wed, 21 Jun 2023 01:22:21 GMT  
		Size: 202.3 MB (202291302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a113436dbb5833b7c2c36a0c90dcd0962a46b704e4c263317e779aa61a51a205`  
		Last Modified: Wed, 21 Jun 2023 01:51:39 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cffb9e0c70da4f644041793ed2d88761ad6df280622afbb91ac54f4adbe9856`  
		Last Modified: Wed, 21 Jun 2023 01:52:13 GMT  
		Size: 12.6 MB (12568094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba43eb2ed2989fe31f64e9923538301aca7790583aa607a5c6fba3316e764c9a`  
		Last Modified: Wed, 21 Jun 2023 01:52:12 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
