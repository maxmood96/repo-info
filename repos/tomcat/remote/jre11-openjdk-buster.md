## `tomcat:jre11-openjdk-buster`

```console
$ docker pull tomcat@sha256:89756c148e0c312454c377713651c252a44ed5b60193a226d48c167c7be580b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:jre11-openjdk-buster` - linux; amd64

```console
$ docker pull tomcat@sha256:c599100cc527c65694ef8d8d885ea50a64208e10a31a1149bdc67050b7c5b395
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133667650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba9eabbc62924c949e4b5f217dffa6e29ad870bd711c435b7b0668466003f118`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Oct 2021 01:20:53 GMT
ADD file:98c256057b79b141aea9a806a4538cf6c3f340d7e3b0d6e8c363699333f3406b in / 
# Tue, 12 Oct 2021 01:20:53 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 15:44:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 15:44:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Oct 2021 16:35:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 16:35:05 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Tue, 12 Oct 2021 16:35:06 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Tue, 12 Oct 2021 16:35:06 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Oct 2021 16:35:06 GMT
ENV LANG=C.UTF-8
# Thu, 21 Oct 2021 23:45:51 GMT
ENV JAVA_VERSION=11.0.13
# Thu, 21 Oct 2021 23:46:00 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_x64_linux_11.0.13_8.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_aarch64_linux_11.0.13_8.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Fri, 22 Oct 2021 00:17:53 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 22 Oct 2021 00:17:53 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Oct 2021 00:17:54 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 22 Oct 2021 00:17:54 GMT
WORKDIR /usr/local/tomcat
# Fri, 22 Oct 2021 00:17:54 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 22 Oct 2021 00:17:55 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 22 Oct 2021 00:17:55 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Fri, 22 Oct 2021 00:17:55 GMT
ENV TOMCAT_MAJOR=10
# Mon, 15 Nov 2021 20:59:39 GMT
ENV TOMCAT_VERSION=10.0.13
# Mon, 15 Nov 2021 20:59:39 GMT
ENV TOMCAT_SHA512=fecfe06f38ff31e31fa43c15f2566f6fcd26bb874a9b7c0533087be81d1decd97f81eefeaca7ecb5ab2b79a3ea69ed0459adff5f9d55c05f5af45f69b0725608
# Mon, 15 Nov 2021 20:59:39 GMT
COPY dir:c23d998c1ccb86f84c48a2cce21b7a1692aa0580092f59d367cffc2c06142cb4 in /usr/local/tomcat 
# Mon, 15 Nov 2021 20:59:44 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Mon, 15 Nov 2021 20:59:46 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Mon, 15 Nov 2021 20:59:46 GMT
EXPOSE 8080
# Mon, 15 Nov 2021 20:59:46 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:07471e81507f7cf1100827f10c60c3c0422d1222430e34e527d97ec72b14a193`  
		Last Modified: Tue, 12 Oct 2021 01:26:26 GMT  
		Size: 50.4 MB (50436692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6cef1aa2170c001b320769bf8b018ed82d2c94a673e3010ea1ffe152e107419`  
		Last Modified: Tue, 12 Oct 2021 15:54:16 GMT  
		Size: 7.8 MB (7833862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a51f13be8e69cfc526b671d0bbf621b985b0932acd1523050e2995777b5926`  
		Last Modified: Tue, 12 Oct 2021 15:54:17 GMT  
		Size: 10.0 MB (9997204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:926071273d78abc57f0ee894a7c609a97b18a29335e5a856a83535ab4eab675b`  
		Last Modified: Tue, 12 Oct 2021 16:53:48 GMT  
		Size: 5.5 MB (5531169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88f1993e7e63f4b53967c6d79db2c0a1cf5e78e29c3b5a8807127dbac79c27c0`  
		Last Modified: Tue, 12 Oct 2021 16:53:47 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b792d4e2c810934988559db0729c6dc03c1d0be02215ddb1f472015bc725d5c0`  
		Last Modified: Fri, 22 Oct 2021 00:01:42 GMT  
		Size: 46.8 MB (46841716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f170ed80d3a3e4dbfcb28a08b0b79fb028d5baef75d97fd816cf411395fc46`  
		Last Modified: Fri, 22 Oct 2021 01:05:42 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e208f73b3f03ab5d7eecee0600c2a95215ba6db680883ed3cf2962dd89317bea`  
		Last Modified: Mon, 15 Nov 2021 21:29:14 GMT  
		Size: 12.6 MB (12565554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61a1384f5ba84101a30066928069812763157bd0f36737bdf404356476dbaf1b`  
		Last Modified: Mon, 15 Nov 2021 21:29:13 GMT  
		Size: 460.9 KB (460939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6ecc20529134b4073c36a9b0b59593d2234e1982282d7c0e32e20aa4af44d90`  
		Last Modified: Mon, 15 Nov 2021 21:29:13 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:jre11-openjdk-buster` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:42b21436c7c0e365b6e6320ebd15bed54f5dee10c8aaac89c6071902c6f09194
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.9 MB (130914277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d75aa7924a482c0652def484321d866a415d796e1a721da16e6ceb4dc0919c1`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:27 GMT
ADD file:c7e9e884b1494f96e33e9d9a892b51367af8943edb282c4101cc99ea78a7753f in / 
# Wed, 17 Nov 2021 02:40:28 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 13:28:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 13:28:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 17 Nov 2021 21:59:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 21:59:08 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Wed, 17 Nov 2021 21:59:09 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 17 Nov 2021 21:59:10 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 21:59:11 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 21:59:12 GMT
ENV JAVA_VERSION=11.0.13
# Wed, 17 Nov 2021 21:59:24 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_x64_linux_11.0.13_8.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_aarch64_linux_11.0.13_8.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Thu, 18 Nov 2021 06:42:55 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 18 Nov 2021 06:42:55 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Nov 2021 06:42:56 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 18 Nov 2021 06:42:57 GMT
WORKDIR /usr/local/tomcat
# Thu, 18 Nov 2021 06:42:58 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 18 Nov 2021 06:42:59 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 18 Nov 2021 06:43:00 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Thu, 18 Nov 2021 06:43:01 GMT
ENV TOMCAT_MAJOR=10
# Thu, 18 Nov 2021 06:47:34 GMT
ENV TOMCAT_VERSION=10.0.13
# Thu, 18 Nov 2021 06:47:34 GMT
ENV TOMCAT_SHA512=fecfe06f38ff31e31fa43c15f2566f6fcd26bb874a9b7c0533087be81d1decd97f81eefeaca7ecb5ab2b79a3ea69ed0459adff5f9d55c05f5af45f69b0725608
# Thu, 18 Nov 2021 06:47:36 GMT
COPY dir:67b3e5fcc587e73ac95b42d9fcb2171321c7e54a43a48f996292529f33601b69 in /usr/local/tomcat 
# Thu, 18 Nov 2021 06:47:40 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 06:47:43 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 18 Nov 2021 06:47:43 GMT
EXPOSE 8080
# Thu, 18 Nov 2021 06:47:44 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:626979e62c56e192812e818d52b82f063d9f9514b1b7bae14e534e4a7c98117a`  
		Last Modified: Wed, 17 Nov 2021 02:47:40 GMT  
		Size: 49.2 MB (49222990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:134a528370d5dcbf5b6ba2d8c20f576504448e8f2d1debb5d2a4950a38a3ff2d`  
		Last Modified: Wed, 17 Nov 2021 13:37:44 GMT  
		Size: 7.7 MB (7695161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92e12e3364b52ad043d8e79f750863ed4ca2878c4fdf45ded974508febc55fdd`  
		Last Modified: Wed, 17 Nov 2021 13:37:44 GMT  
		Size: 9.8 MB (9767133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d68bc1b9fc908d2ecc7d041954a367dcb743ea85f5b79ff3ae93ac0871355ebf`  
		Last Modified: Wed, 17 Nov 2021 22:14:57 GMT  
		Size: 5.5 MB (5505361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c11fe09bcb907bab304a512ba5c12925043d0ce5fc4179a19621464c11c95d`  
		Last Modified: Wed, 17 Nov 2021 22:14:56 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366a788467635d8deb9e3c04f134cafd3f2c0fc3668b8698c80e19c1e2c16bc3`  
		Last Modified: Wed, 17 Nov 2021 22:15:04 GMT  
		Size: 45.9 MB (45927598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c81fa85f5c793643c98e0d94b02030968a676dd14e08001d06e4da53c131faf1`  
		Last Modified: Thu, 18 Nov 2021 07:38:00 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1277413150d70ede356d2b1369e8fe5ca2845e05915b2abcc17f029da42ef64b`  
		Last Modified: Thu, 18 Nov 2021 07:42:13 GMT  
		Size: 12.6 MB (12577481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceefc634ecd728c34904549568a31c61b86101d69641aa1288fb1ac3d7909139`  
		Last Modified: Thu, 18 Nov 2021 07:42:12 GMT  
		Size: 218.2 KB (218203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
