## `tomcat:9-jre11-openjdk-buster`

```console
$ docker pull tomcat@sha256:c00e2777ba029d0b1937afd9d9077472245bf2b0a993ece573e012048ba630b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:9-jre11-openjdk-buster` - linux; amd64

```console
$ docker pull tomcat@sha256:4d980669918d2ed82785b4b04ab10ac4eb6720fd3ac0f01163c0c8bfee6bfb8a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.3 MB (133323095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc5eb08298f059e6587963b5a839b1f7aeaab0642d3ed2684d855dab20e388fe`
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
# Fri, 22 Oct 2021 00:34:25 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 22 Oct 2021 00:34:25 GMT
ENV TOMCAT_MAJOR=9
# Tue, 16 Nov 2021 00:29:09 GMT
ENV TOMCAT_VERSION=9.0.55
# Tue, 16 Nov 2021 00:29:09 GMT
ENV TOMCAT_SHA512=a0c480b8bba09069bda3b57f54e658450a59d799474ad587dead0ffbf5074c16ee3f9f9c13312d0ff3227c7034589dabf25941fbd672838e9baeee9661e024dc
# Tue, 16 Nov 2021 00:29:09 GMT
COPY dir:178b68f356851a80ada1ff57ff873d0200f497449e73baabcbf1ff40b1a6a85d in /usr/local/tomcat 
# Tue, 16 Nov 2021 00:29:14 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Nov 2021 00:29:16 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 16 Nov 2021 00:29:16 GMT
EXPOSE 8080
# Tue, 16 Nov 2021 00:29:16 GMT
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
	-	`sha256:6027f978ac415502bf757d6fe1291af14c3f5695f8c6e5f47e55b8afd3c1761b`  
		Last Modified: Tue, 16 Nov 2021 00:52:37 GMT  
		Size: 12.2 MB (12221002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:191b925a4a57b0615c3014187dc69249c2ef3b299618cfc24c73cd38940c0e4b`  
		Last Modified: Tue, 16 Nov 2021 00:52:36 GMT  
		Size: 460.9 KB (460937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f17df60f7a1fa5493b429fa1e0027ecede661c68f8d710cca7548f74689c6748`  
		Last Modified: Tue, 16 Nov 2021 00:52:36 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre11-openjdk-buster` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:e001a59d173d122511071478888d7554793cc4795df01e893d40e4dfe44add1f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130569853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b334d602731d737fc398df56fcc63dd10eae2b122cafea49fe13eaf93657da40`
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
# Thu, 18 Nov 2021 06:55:45 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 18 Nov 2021 06:55:46 GMT
ENV TOMCAT_MAJOR=9
# Thu, 18 Nov 2021 06:55:47 GMT
ENV TOMCAT_VERSION=9.0.55
# Thu, 18 Nov 2021 06:55:48 GMT
ENV TOMCAT_SHA512=a0c480b8bba09069bda3b57f54e658450a59d799474ad587dead0ffbf5074c16ee3f9f9c13312d0ff3227c7034589dabf25941fbd672838e9baeee9661e024dc
# Thu, 18 Nov 2021 06:55:50 GMT
COPY dir:69ec86406f83d8e5cf272084ee758abeb99faf9d2a26c1b3c8a788c7df2d22ed in /usr/local/tomcat 
# Thu, 18 Nov 2021 06:55:54 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 06:55:56 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 18 Nov 2021 06:55:56 GMT
EXPOSE 8080
# Thu, 18 Nov 2021 06:55:57 GMT
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
	-	`sha256:c4f62bf936497f61fb133aa21382fbedc472ea96fe27ccef762298efc5fb7830`  
		Last Modified: Thu, 18 Nov 2021 07:48:20 GMT  
		Size: 12.2 MB (12233061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c716ddc30f89a6130bdefd855ffef0d836a0bd43673ed227ce3d9cf52024f4ff`  
		Last Modified: Thu, 18 Nov 2021 07:48:19 GMT  
		Size: 218.2 KB (218199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
