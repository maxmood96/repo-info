## `tomcat:10-jre11-openjdk-slim-buster`

```console
$ docker pull tomcat@sha256:f1c5d408f807cb494c940a57535d66b35a631009b7a09bc7c69f445b07cb5676
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:10-jre11-openjdk-slim-buster` - linux; amd64

```console
$ docker pull tomcat@sha256:0accb52ad0fa2e7b8bb06318958831c37aa3e21d6762de75a69d1ac7a90d2d9f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.8 MB (90838221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a622d6fb37d1feb2f3217e1589ee43376a111b1c754615a4a6e1b8c347802b1c`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 11 May 2022 01:20:37 GMT
ADD file:76b454ddb7dfe4d22afae844a7e67e7e5fb4570dae2e21bbd259a1f2e5839f33 in / 
# Wed, 11 May 2022 01:20:37 GMT
CMD ["bash"]
# Wed, 11 May 2022 05:47:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 05:50:52 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Wed, 11 May 2022 05:50:53 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 11 May 2022 05:50:53 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 May 2022 05:50:53 GMT
ENV LANG=C.UTF-8
# Wed, 11 May 2022 05:50:53 GMT
ENV JAVA_VERSION=11.0.15
# Wed, 11 May 2022 05:52:25 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_11.0.15_10.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_11.0.15_10.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Wed, 11 May 2022 23:51:59 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 11 May 2022 23:51:59 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 May 2022 23:52:00 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 11 May 2022 23:52:00 GMT
WORKDIR /usr/local/tomcat
# Wed, 11 May 2022 23:52:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 11 May 2022 23:52:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 11 May 2022 23:52:00 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 11 May 2022 23:52:00 GMT
ENV TOMCAT_MAJOR=10
# Wed, 11 May 2022 23:54:58 GMT
ENV TOMCAT_VERSION=10.0.20
# Wed, 11 May 2022 23:54:58 GMT
ENV TOMCAT_SHA512=53bfdbac2e6af5cca97dc01fffb0428380fbe21d8375f45d015c16a57017ff946fdc555ebad9e9fcbcb97b438c4f6daf3aa39d36ca79fd5a372cfc1a80b7117f
# Wed, 11 May 2022 23:54:58 GMT
COPY dir:6b6d425232a267dee2baf59d41cc4969b495fa19a792bb45e4aec8f72e23b5c5 in /usr/local/tomcat 
# Wed, 11 May 2022 23:55:02 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 23:55:03 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 11 May 2022 23:55:04 GMT
EXPOSE 8080
# Wed, 11 May 2022 23:55:04 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:c32ce6654453d35d0b3dde45d195adeee586ffba0a683006ee06748c077c01fa`  
		Last Modified: Wed, 11 May 2022 01:25:58 GMT  
		Size: 27.1 MB (27140722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a9930d1f61e9a044df90a13c9456f95b2e6b31da0c5f483757324dfe0a5fc33`  
		Last Modified: Wed, 11 May 2022 05:59:57 GMT  
		Size: 3.3 MB (3273265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e180b549d0140dd3a0f09953f26fcabcef901117b88f37992b70eac1d0b2ee3`  
		Last Modified: Wed, 11 May 2022 06:05:49 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f88a38edf3851da662417ca2a0b02b9e7ef6cb78b69b8a3fe3e937fb3cb9cca6`  
		Last Modified: Wed, 11 May 2022 06:07:34 GMT  
		Size: 47.5 MB (47481995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4e9639ae4783cefe928e59225199272771f23597f3fd8566b1d493d9beee87`  
		Last Modified: Thu, 12 May 2022 00:20:21 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba709703eb10debeeb5610d0efb6343564eaf0c80095180e1800c6132c629cfa`  
		Last Modified: Thu, 12 May 2022 00:23:59 GMT  
		Size: 12.6 MB (12554052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bde7a11a00519ae9136395648e823e2bd1239ff2831e930962b2c7634510cd4`  
		Last Modified: Thu, 12 May 2022 00:23:58 GMT  
		Size: 387.7 KB (387675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f42dba96596106f820b1e6ea4efacc09a7a285ac4ae93c9843af9d7d6a412629`  
		Last Modified: Thu, 12 May 2022 00:23:58 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:10-jre11-openjdk-slim-buster` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:67ee60902292e9c076576f8adfd4f067cf13ff1446e33ee6263fa156507e8a91
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.3 MB (88341877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a56935f8c2f3891406abe26d65e51ad8380eb9c10322a08dd0ea42405c9a603`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:36 GMT
ADD file:5de4397c1295f7249c93907be599d96efbd9cd25909340d245ec8d1c9770f444 in / 
# Wed, 20 Apr 2022 04:29:37 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 10:25:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:32:37 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Wed, 20 Apr 2022 10:32:38 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 20 Apr 2022 10:32:39 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 10:32:40 GMT
ENV LANG=C.UTF-8
# Mon, 25 Apr 2022 18:46:36 GMT
ENV JAVA_VERSION=11.0.15
# Mon, 25 Apr 2022 18:47:59 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_11.0.15_10.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_11.0.15_10.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Mon, 25 Apr 2022 23:22:19 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 25 Apr 2022 23:22:20 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 25 Apr 2022 23:22:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 25 Apr 2022 23:22:22 GMT
WORKDIR /usr/local/tomcat
# Mon, 25 Apr 2022 23:22:23 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 25 Apr 2022 23:22:24 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 25 Apr 2022 23:22:25 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Mon, 25 Apr 2022 23:22:26 GMT
ENV TOMCAT_MAJOR=10
# Mon, 25 Apr 2022 23:27:19 GMT
ENV TOMCAT_VERSION=10.0.20
# Mon, 25 Apr 2022 23:27:19 GMT
ENV TOMCAT_SHA512=53bfdbac2e6af5cca97dc01fffb0428380fbe21d8375f45d015c16a57017ff946fdc555ebad9e9fcbcb97b438c4f6daf3aa39d36ca79fd5a372cfc1a80b7117f
# Mon, 25 Apr 2022 23:27:21 GMT
COPY dir:33a786d799199e49beffce11680bd27049fbd9292e52071c582cf56d9d6fac2e in /usr/local/tomcat 
# Mon, 25 Apr 2022 23:27:24 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Mon, 25 Apr 2022 23:27:26 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Mon, 25 Apr 2022 23:27:27 GMT
EXPOSE 8080
# Mon, 25 Apr 2022 23:27:28 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6c3e5b218d6477ff77053280968d5bdeaa5dcf16a803e917d98dd0ea8b93ac82`  
		Last Modified: Wed, 20 Apr 2022 04:36:38 GMT  
		Size: 25.9 MB (25908349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef4c0391a581a54e4ae08706ac3173bf39e99722f6efe3a9094dbe8916d7bfd`  
		Last Modified: Wed, 20 Apr 2022 10:47:49 GMT  
		Size: 3.1 MB (3125683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98e615f0d4667817d0647ba9f2a1de21a29f09ac4865e1a2884ea98d5a37a97`  
		Last Modified: Wed, 20 Apr 2022 10:57:30 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8dab8e0d8e1687dff848d5de31b7847170c34cb2dec670652b60bf63bf1381`  
		Last Modified: Mon, 25 Apr 2022 19:09:24 GMT  
		Size: 46.6 MB (46566824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec38df88037f674bc63b8a35ec0ab28168fb69331947aad481b4808f956b906`  
		Last Modified: Tue, 26 Apr 2022 00:02:34 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffc4115026f116755255d08a6386bd194940706be44afc1d1b7ee2b250544036`  
		Last Modified: Tue, 26 Apr 2022 00:07:29 GMT  
		Size: 12.6 MB (12567011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f672259e3939b0777dfb4f29d6e3f75fb9136aa88cfd254342e8b1aa77d1e42`  
		Last Modified: Tue, 26 Apr 2022 00:07:28 GMT  
		Size: 173.7 KB (173661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
