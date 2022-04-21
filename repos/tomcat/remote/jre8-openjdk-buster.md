## `tomcat:jre8-openjdk-buster`

```console
$ docker pull tomcat@sha256:a6c638c733f9afa5af8c1a7eeca28ab28fda13f7c9b93b13eaf35b0103df5ead
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:jre8-openjdk-buster` - linux; amd64

```console
$ docker pull tomcat@sha256:3ebc71124ce2b6910f5fc0f48c5a2742afbb1458ab10f33d0a366408938685b0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128232451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67ec460d142db24e653af1729ab3b57a1f8df3fbdfbb5f169aee3cfa50c433dd`
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
# Wed, 20 Apr 2022 10:56:22 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 20 Apr 2022 10:56:22 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 20 Apr 2022 10:56:22 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 10:56:22 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 10:56:22 GMT
ENV JAVA_VERSION=8u322
# Wed, 20 Apr 2022 10:56:27 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_8u322b06.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 21 Apr 2022 04:33:18 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 21 Apr 2022 04:33:19 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Apr 2022 04:33:19 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 21 Apr 2022 04:33:19 GMT
WORKDIR /usr/local/tomcat
# Thu, 21 Apr 2022 04:33:19 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 21 Apr 2022 04:33:19 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 21 Apr 2022 04:33:19 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Thu, 21 Apr 2022 04:33:20 GMT
ENV TOMCAT_MAJOR=10
# Thu, 21 Apr 2022 04:33:20 GMT
ENV TOMCAT_VERSION=10.0.20
# Thu, 21 Apr 2022 04:33:20 GMT
ENV TOMCAT_SHA512=53bfdbac2e6af5cca97dc01fffb0428380fbe21d8375f45d015c16a57017ff946fdc555ebad9e9fcbcb97b438c4f6daf3aa39d36ca79fd5a372cfc1a80b7117f
# Thu, 21 Apr 2022 04:33:20 GMT
COPY dir:35bf5123ee2578db21be43cdc33a5573ef25da4a31bc0770dbee8dda0d29b5ee in /usr/local/tomcat 
# Thu, 21 Apr 2022 04:33:24 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Thu, 21 Apr 2022 04:33:26 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 21 Apr 2022 04:33:26 GMT
EXPOSE 8080
# Thu, 21 Apr 2022 04:33:26 GMT
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
	-	`sha256:7a53754fb28d2d41f1b5e59821b1d521fae12c802f79efb17560e3cc3a8c9f4d`  
		Last Modified: Wed, 20 Apr 2022 11:16:34 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c25da910c8c7162f9e8f9657fc02eac7460d4d20b2bd17402f6cdc25a56548b4`  
		Last Modified: Wed, 20 Apr 2022 11:16:39 GMT  
		Size: 41.4 MB (41395119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36e5b5df5ac7e715bf47cb9de6df05ef6cd5991d86c718ebeb6c4618f3d784d1`  
		Last Modified: Thu, 21 Apr 2022 05:11:27 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f56a72752eecfc148d25513157e37cc05371f5b07bfedc5c0c25ed273181e40b`  
		Last Modified: Thu, 21 Apr 2022 05:11:28 GMT  
		Size: 12.6 MB (12552781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab37b04badd4d43dbedd1b3dd5b0bcc08ce8a841d851b6e1b9da4ab5d8d41d1`  
		Last Modified: Thu, 21 Apr 2022 05:11:28 GMT  
		Size: 460.9 KB (460913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d74c1315a52ca73b26e618133fd2604e5b22103d760dc4b60fdf3ff6fd34954d`  
		Last Modified: Thu, 21 Apr 2022 05:11:27 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:jre8-openjdk-buster` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:542955ea0eab8e43e76b4275c67a01e3a62f09696bea65c46c935f71d8c708d5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125665730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:384a9002eaf57a4fbd4242daaeb1ccffd6941f388d663d895121f0c907ece80e`
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
# Wed, 20 Apr 2022 10:36:59 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 20 Apr 2022 10:37:00 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 20 Apr 2022 10:37:01 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 10:37:02 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 10:37:03 GMT
ENV JAVA_VERSION=8u322
# Wed, 20 Apr 2022 10:37:08 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_8u322b06.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 21 Apr 2022 06:13:04 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 21 Apr 2022 06:13:04 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Apr 2022 06:13:05 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 21 Apr 2022 06:13:06 GMT
WORKDIR /usr/local/tomcat
# Thu, 21 Apr 2022 06:13:07 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 21 Apr 2022 06:13:08 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 21 Apr 2022 06:13:09 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Thu, 21 Apr 2022 06:13:10 GMT
ENV TOMCAT_MAJOR=10
# Thu, 21 Apr 2022 06:13:11 GMT
ENV TOMCAT_VERSION=10.0.20
# Thu, 21 Apr 2022 06:13:12 GMT
ENV TOMCAT_SHA512=53bfdbac2e6af5cca97dc01fffb0428380fbe21d8375f45d015c16a57017ff946fdc555ebad9e9fcbcb97b438c4f6daf3aa39d36ca79fd5a372cfc1a80b7117f
# Thu, 21 Apr 2022 06:13:14 GMT
COPY dir:77394a75d43414d1aadac5f52bb97098285f1d80e9d4d87ad345bf2bd5556d01 in /usr/local/tomcat 
# Thu, 21 Apr 2022 06:13:17 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Thu, 21 Apr 2022 06:13:19 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 21 Apr 2022 06:13:20 GMT
EXPOSE 8080
# Thu, 21 Apr 2022 06:13:21 GMT
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
	-	`sha256:7c2b8029f074801977d682a25323a6ee36cd9fb5c5cda266d5fc860005b5e2f8`  
		Last Modified: Wed, 20 Apr 2022 11:02:52 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a77b8eeb11c11d0863039682856c214aecdaa290b1497d6a2d3bfb8d6b56616`  
		Last Modified: Wed, 20 Apr 2022 11:02:57 GMT  
		Size: 40.7 MB (40659904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2ec7086de6cd82e877ddec31736f794e31d2c4fa42b1ad94a2f36beba502c32`  
		Last Modified: Thu, 21 Apr 2022 08:50:47 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1042bd4c582bec01c34cbf293f2bb138b65ed7296a39bd634e78ecf53be3b2b1`  
		Last Modified: Thu, 21 Apr 2022 08:50:49 GMT  
		Size: 12.6 MB (12565743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b671c1ce398c0ebf7cac5df1e840ea84c40072b02ccfe84a42c6393d04fe235`  
		Last Modified: Thu, 21 Apr 2022 08:50:47 GMT  
		Size: 218.2 KB (218229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
