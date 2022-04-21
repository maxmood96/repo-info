## `tomcat:10-jre11-openjdk-buster`

```console
$ docker pull tomcat@sha256:f493dcb61ad0ff635b7c5427af05409e3b34874436b5d9e87e4977f7fcf0ff2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:10-jre11-openjdk-buster` - linux; amd64

```console
$ docker pull tomcat@sha256:046054331df1794fa62faa6f8f16c6760342c2799ad4dccd1293a41f4caef02b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133716547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f1c50d22bb8a9a9acd5faaa84554f0f7707d8b27dd8f10db5c7d04b362f8b51`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:37 GMT
ADD file:7c5789fb822bda2652d7addee832c5a3d71733f0f94f97d89b0c5570c0840829 in / 
# Wed, 20 Apr 2022 04:43:37 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 06:59:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 06:59:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 20 Apr 2022 10:54:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:54:32 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Wed, 20 Apr 2022 10:54:32 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 20 Apr 2022 10:54:33 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 10:54:33 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 10:54:33 GMT
ENV JAVA_VERSION=11.0.14.1
# Wed, 20 Apr 2022 10:54:38 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_x64_linux_11.0.14.1_1.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_aarch64_linux_11.0.14.1_1.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Thu, 21 Apr 2022 04:25:38 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 21 Apr 2022 04:25:38 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Apr 2022 04:25:39 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 21 Apr 2022 04:25:39 GMT
WORKDIR /usr/local/tomcat
# Thu, 21 Apr 2022 04:25:39 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 21 Apr 2022 04:25:39 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 21 Apr 2022 04:25:39 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Thu, 21 Apr 2022 04:25:39 GMT
ENV TOMCAT_MAJOR=10
# Thu, 21 Apr 2022 04:30:30 GMT
ENV TOMCAT_VERSION=10.0.20
# Thu, 21 Apr 2022 04:30:30 GMT
ENV TOMCAT_SHA512=53bfdbac2e6af5cca97dc01fffb0428380fbe21d8375f45d015c16a57017ff946fdc555ebad9e9fcbcb97b438c4f6daf3aa39d36ca79fd5a372cfc1a80b7117f
# Thu, 21 Apr 2022 04:30:30 GMT
COPY dir:011793c09361f657325cadf76f0913227332e5bb583b24d70d3d27fe59e9e2ab in /usr/local/tomcat 
# Thu, 21 Apr 2022 04:30:34 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Thu, 21 Apr 2022 04:30:36 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 21 Apr 2022 04:30:36 GMT
EXPOSE 8080
# Thu, 21 Apr 2022 04:30:36 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:85bed84afb9a834cf090b55d2e584abd55b4792d93b750db896f486680638344`  
		Last Modified: Wed, 20 Apr 2022 04:48:49 GMT  
		Size: 50.4 MB (50436985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fdd409f4b2bf3771fac1cbc2df46d1cbb4b800b154cfc33e8e0cd23e67ab3e0`  
		Last Modified: Wed, 20 Apr 2022 07:06:56 GMT  
		Size: 7.9 MB (7856378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3069e6cecf9d5e43ace0a925b53849b2fd189ef41883d45d8f2e12213c2c06`  
		Last Modified: Wed, 20 Apr 2022 07:06:56 GMT  
		Size: 10.0 MB (9997231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61f81393f382611cf77dfb7e0e958aff2c06386dab286300b237441df9a07ef6`  
		Last Modified: Wed, 20 Apr 2022 11:13:16 GMT  
		Size: 5.5 MB (5532533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:192269fb9373f1afda71a29c7259978e5d08dbe0a6c229bf07dee546f1955de2`  
		Last Modified: Wed, 20 Apr 2022 11:13:15 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:001353c6c1de1c9ffcf214f8625e59d021def69d4088ea794a3e2528e6f1a3f4`  
		Last Modified: Wed, 20 Apr 2022 11:13:22 GMT  
		Size: 46.9 MB (46877986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7b0ca06cd883fe5772590137084a7dcd405a3f47f393918353b3ccfa8c81a8`  
		Last Modified: Thu, 21 Apr 2022 05:02:43 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7afe6443090e07b47b83d9edd6177f02507fdba7994eb932831ba0abd6b801`  
		Last Modified: Thu, 21 Apr 2022 05:07:56 GMT  
		Size: 12.6 MB (12553980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16fbc55b260e7793bba1a4a2620c9a253178b865357642009c073807c8713ca`  
		Last Modified: Thu, 21 Apr 2022 05:07:55 GMT  
		Size: 460.9 KB (460942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8b70acce40be6e0e998dee97a5521950d4b90a0256e6a75ca59f1453c29c27`  
		Last Modified: Thu, 21 Apr 2022 05:07:55 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:10-jre11-openjdk-buster` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:163eca822a6c0536984d09307728f719419335fe4d533c79ddc5715a09eab31a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.0 MB (130990122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e51a2239a71fb96b67e5f90d9a981b9fd6516ce11cd8792fb1c82c25e270f646`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:22 GMT
ADD file:5286ff5db23c42ac6a437e8f2f9ef01b6ee6e523d7866c752428d54f177c7108 in / 
# Wed, 20 Apr 2022 04:29:22 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 06:45:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 06:45:34 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 20 Apr 2022 10:34:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:34:06 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Wed, 20 Apr 2022 10:34:07 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 20 Apr 2022 10:34:08 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 10:34:09 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 10:34:10 GMT
ENV JAVA_VERSION=11.0.14.1
# Wed, 20 Apr 2022 10:34:16 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_x64_linux_11.0.14.1_1.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_aarch64_linux_11.0.14.1_1.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Thu, 21 Apr 2022 06:01:36 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 21 Apr 2022 06:01:37 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Apr 2022 06:01:38 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 21 Apr 2022 06:01:39 GMT
WORKDIR /usr/local/tomcat
# Thu, 21 Apr 2022 06:01:40 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 21 Apr 2022 06:01:41 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 21 Apr 2022 06:01:42 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Thu, 21 Apr 2022 06:01:43 GMT
ENV TOMCAT_MAJOR=10
# Thu, 21 Apr 2022 06:08:45 GMT
ENV TOMCAT_VERSION=10.0.20
# Thu, 21 Apr 2022 06:08:46 GMT
ENV TOMCAT_SHA512=53bfdbac2e6af5cca97dc01fffb0428380fbe21d8375f45d015c16a57017ff946fdc555ebad9e9fcbcb97b438c4f6daf3aa39d36ca79fd5a372cfc1a80b7117f
# Thu, 21 Apr 2022 06:08:48 GMT
COPY dir:0432af8658df7e430f4dac0ee086b1ef6149b8ee7e757754a04a406cfccb11a3 in /usr/local/tomcat 
# Thu, 21 Apr 2022 06:08:51 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Thu, 21 Apr 2022 06:08:53 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 21 Apr 2022 06:08:54 GMT
EXPOSE 8080
# Thu, 21 Apr 2022 06:08:55 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b9f330b3a7e234282d632d95bd19a655cf0e06c1a76a51d0f73b9581be8f851b`  
		Last Modified: Wed, 20 Apr 2022 04:36:12 GMT  
		Size: 49.2 MB (49227738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a80651adb7e52d8ecd27d43b9e69ada9ca277071ea09607121d0076de36480b`  
		Last Modified: Wed, 20 Apr 2022 06:55:25 GMT  
		Size: 7.7 MB (7719745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b38ee622cbfb492ebc3bc598771624fba7ef1830b4e0f9737f2bbf4b6ec0ea`  
		Last Modified: Wed, 20 Apr 2022 06:55:26 GMT  
		Size: 9.8 MB (9767312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bd9ef6cd611a3f644d8e2dbd9072cca066d10483bb06b4db05027567e857821`  
		Last Modified: Wed, 20 Apr 2022 10:59:18 GMT  
		Size: 5.5 MB (5506710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3704f2012740c33707d24455d28f47a9dd627f6816fad38fd788048aaf8195f5`  
		Last Modified: Wed, 20 Apr 2022 10:59:17 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29dc65b39393e19b911e7a4a7969b5b5c32bd8a101ff35bbda71bde1a977a732`  
		Last Modified: Wed, 20 Apr 2022 10:59:24 GMT  
		Size: 46.0 MB (45983062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ac3d70b0f13a18574dcf6fe01632e6d6be28cc8a8be114a580b1235b777e44f`  
		Last Modified: Thu, 21 Apr 2022 08:40:40 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5fffd559814275454c08e10ef0d121add33bab417cf558de5d54172c9746bb8`  
		Last Modified: Thu, 21 Apr 2022 08:46:44 GMT  
		Size: 12.6 MB (12566933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3947a73641a616b0b8be8c65fc6a8554576b310000eece6eab1ffaa99d21506f`  
		Last Modified: Thu, 21 Apr 2022 08:46:42 GMT  
		Size: 218.3 KB (218273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
