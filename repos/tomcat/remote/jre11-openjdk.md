## `tomcat:jre11-openjdk`

```console
$ docker pull tomcat@sha256:3c4b3900668d16aaa7ff650d726af4df4ce65c241fd64d49668796a63d0b00c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:jre11-openjdk` - linux; amd64

```console
$ docker pull tomcat@sha256:b952101687a21864a848885a1fee195557769ac940570b5f8bd3362d73f13f72
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.4 MB (136422240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2697bd5cd09c65e606f1f52aae4f5e394c1cb0687073a033dd9035733b5bf33a`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 17 Mar 2022 04:03:47 GMT
ADD file:19873be7a1c793d8edefb5d64edb99fe05ac5b1d304d167661ac3d8f21b4bd65 in / 
# Thu, 17 Mar 2022 04:03:47 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:29:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:30:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 19 Mar 2022 10:26:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:26:49 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Sat, 19 Mar 2022 10:26:50 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 19 Mar 2022 10:26:50 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 10:26:50 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 10:26:50 GMT
ENV JAVA_VERSION=11.0.14.1
# Sat, 19 Mar 2022 10:27:16 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_x64_linux_11.0.14.1_1.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_aarch64_linux_11.0.14.1_1.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Sun, 20 Mar 2022 11:09:42 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sun, 20 Mar 2022 11:09:42 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 20 Mar 2022 11:09:42 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sun, 20 Mar 2022 11:09:42 GMT
WORKDIR /usr/local/tomcat
# Sun, 20 Mar 2022 11:09:42 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sun, 20 Mar 2022 11:09:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sun, 20 Mar 2022 11:09:42 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Sun, 20 Mar 2022 11:09:43 GMT
ENV TOMCAT_MAJOR=10
# Sun, 20 Mar 2022 11:20:53 GMT
ENV TOMCAT_VERSION=10.0.18
# Sun, 20 Mar 2022 11:20:53 GMT
ENV TOMCAT_SHA512=a9e3c516676369bd9d52e768071898b0e07659a9ff03b9dc491e53f084b9981a929bf2c74a694f06ad26dae0644fb9617cc6e364f0e1dcd953c857978a95a644
# Sun, 20 Mar 2022 11:20:54 GMT
COPY dir:c588ac144c32fc629bac607a68194e5ef7b29b236bb9c8b3ec110dd116629fe3 in /usr/local/tomcat 
# Sun, 20 Mar 2022 11:20:57 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Sun, 20 Mar 2022 11:20:58 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Sun, 20 Mar 2022 11:20:58 GMT
EXPOSE 8080
# Sun, 20 Mar 2022 11:20:59 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:5492f66d270062ddb73f28649d80eef162f2c9376d53973a3557158390af4f30`  
		Last Modified: Thu, 17 Mar 2022 04:09:37 GMT  
		Size: 54.9 MB (54922831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540ff8c0841d610e4cc2ad3b9ed4c6edcad4f5be2add8765f416515fbc2be2a8`  
		Last Modified: Fri, 18 Mar 2022 07:03:14 GMT  
		Size: 5.2 MB (5153360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bf850a0df065fb202ebf8a3527699dc18322469c34733a6cb7f412a7aaefa6`  
		Last Modified: Fri, 18 Mar 2022 07:03:15 GMT  
		Size: 10.9 MB (10871980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e0bf408c56987056d977bb11f39372d03d2f422d5860b0dcaf279163962e8a`  
		Last Modified: Sat, 19 Mar 2022 10:45:53 GMT  
		Size: 5.7 MB (5657082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:580ea8b863625e9c2cde6de370a193cb349842b0f6bea736140878a13fdbeeaf`  
		Last Modified: Sat, 19 Mar 2022 10:45:52 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f36d17e35d62a47fa9891c632a6ae8864fce56cf90341924395af0dbc7133f1`  
		Last Modified: Sat, 19 Mar 2022 10:46:00 GMT  
		Size: 46.9 MB (46879397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43cf10162fa0b1934276c143d800ae522ba3e6cfe30611688c8aa62424f73879`  
		Last Modified: Sun, 20 Mar 2022 12:07:55 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df9263a6c677d162beac0318eb6963025762260e16879ae0797e39870138d869`  
		Last Modified: Sun, 20 Mar 2022 12:13:23 GMT  
		Size: 12.5 MB (12477443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6fdeb8a54f7cbe2e13f712a95649de8d641701cff736feafb679c59a894cc54`  
		Last Modified: Sun, 20 Mar 2022 12:13:22 GMT  
		Size: 459.6 KB (459636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dfe2a05585b063e3e28262f5abd81a94637a88d1c1e4535448ce3ac3411a010`  
		Last Modified: Sun, 20 Mar 2022 12:13:21 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:jre11-openjdk` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:d3783267579614470bb7ade8daf71bf4b05d4e55c31193410de3841e50dc61e9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133537019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cec623eb872ac002085c8e809fc52b1d83df0fb62cd50210eff508cfd73ea9a9`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 17 Mar 2022 03:21:41 GMT
ADD file:5effc7e0ab7312f14a7ee81c06c71400aae31219d477ebe1a4f7a9156797c42a in / 
# Thu, 17 Mar 2022 03:21:42 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 22:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 22:11:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Mar 2022 23:32:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 23:32:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 17 Mar 2022 23:32:14 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 17 Mar 2022 23:32:15 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Mar 2022 23:32:16 GMT
ENV LANG=C.UTF-8
# Thu, 17 Mar 2022 23:32:17 GMT
ENV JAVA_VERSION=11.0.14.1
# Thu, 17 Mar 2022 23:32:26 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_x64_linux_11.0.14.1_1.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_aarch64_linux_11.0.14.1_1.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Sat, 19 Mar 2022 11:14:43 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 19 Mar 2022 11:14:44 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 11:14:45 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sat, 19 Mar 2022 11:14:46 GMT
WORKDIR /usr/local/tomcat
# Sat, 19 Mar 2022 11:14:47 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 19 Mar 2022 11:14:48 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 19 Mar 2022 11:14:49 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Sat, 19 Mar 2022 11:14:50 GMT
ENV TOMCAT_MAJOR=10
# Sat, 19 Mar 2022 11:24:44 GMT
ENV TOMCAT_VERSION=10.0.18
# Sat, 19 Mar 2022 11:24:45 GMT
ENV TOMCAT_SHA512=a9e3c516676369bd9d52e768071898b0e07659a9ff03b9dc491e53f084b9981a929bf2c74a694f06ad26dae0644fb9617cc6e364f0e1dcd953c857978a95a644
# Sat, 19 Mar 2022 11:24:47 GMT
COPY dir:abd5654768c553c1094f8f2aadb52f60770d393ba4f19033d526c1f0a96b3972 in /usr/local/tomcat 
# Sat, 19 Mar 2022 11:24:50 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 11:24:52 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Sat, 19 Mar 2022 11:24:53 GMT
EXPOSE 8080
# Sat, 19 Mar 2022 11:24:54 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:260ad8146ed2447d5587608b10fed4f80de80cdc559e619f3a235d3ba09eaf7b`  
		Last Modified: Thu, 17 Mar 2022 03:28:04 GMT  
		Size: 53.6 MB (53616308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1399f445da611be3789923cf26d158e3f4f80449b7295fa069a8eaecaaf137e6`  
		Last Modified: Thu, 17 Mar 2022 22:20:58 GMT  
		Size: 4.9 MB (4937558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd9e43777fa6c09c341f3aa922f47b5b3ace26de1d779124afd2f1d435731d9`  
		Last Modified: Thu, 17 Mar 2022 22:20:58 GMT  
		Size: 10.7 MB (10655858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd720cff0e1622b97733146cf5fd82069a1b35f159e9fb60a4c5f79811616ae9`  
		Last Modified: Thu, 17 Mar 2022 23:59:12 GMT  
		Size: 5.6 MB (5648940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f78ea60c71697144cf4c086bdd4487d84326c8357de477c1ee1dde8de8b4a4`  
		Last Modified: Thu, 17 Mar 2022 23:59:11 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7a633a28261b8c7876c88dd148362345817667ecf117d439e6989810e1d9f96`  
		Last Modified: Thu, 17 Mar 2022 23:59:19 GMT  
		Size: 46.0 MB (45972898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c86727d538dc34fc0ae2a4e11a57b7c792baf4bad0b6f700804cf9593197d518`  
		Last Modified: Sat, 19 Mar 2022 12:28:27 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d9ed2534fdfaef2dc18911c82532844fbff10c1b43fd6e60bdc047b21de6a44`  
		Last Modified: Sat, 19 Mar 2022 12:34:05 GMT  
		Size: 12.5 MB (12488074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c509a85333eee8076a9a8da2f740177e0c37f0f452916ac112190df316cdb62f`  
		Last Modified: Sat, 19 Mar 2022 12:34:04 GMT  
		Size: 217.0 KB (217035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
