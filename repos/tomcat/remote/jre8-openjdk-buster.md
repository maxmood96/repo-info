## `tomcat:jre8-openjdk-buster`

```console
$ docker pull tomcat@sha256:4104e558fa90b499c4d1fa6083f6a020132bd4881c1cb98674ba24dbd195ff76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:jre8-openjdk-buster` - linux; amd64

```console
$ docker pull tomcat@sha256:22081e4babdc026b19b743b83803631f5e6ccd63b1058d77910cfc821c63bbb8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128202976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6081ec25f98ade5453638ae93f3f2c42df7001bdc86309806bd0e6e3d0752d60`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:47 GMT
ADD file:a290acee3581e1e9c42c0a37b53086a8f070cb0730179be81a6ba24a620b6ee4 in / 
# Wed, 26 Jan 2022 01:40:47 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:13:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:13:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Jan 2022 09:29:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:33:48 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 26 Jan 2022 09:33:49 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 26 Jan 2022 09:33:49 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 09:33:50 GMT
ENV LANG=C.UTF-8
# Thu, 03 Feb 2022 20:50:09 GMT
ENV JAVA_VERSION=8u322
# Thu, 03 Feb 2022 20:50:23 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_8u322b06.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 04 Feb 2022 01:43:12 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 04 Feb 2022 01:43:12 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Feb 2022 01:43:13 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 04 Feb 2022 01:43:13 GMT
WORKDIR /usr/local/tomcat
# Fri, 04 Feb 2022 01:43:14 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 04 Feb 2022 01:43:14 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 04 Feb 2022 01:43:14 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Fri, 04 Feb 2022 01:43:14 GMT
ENV TOMCAT_MAJOR=10
# Fri, 04 Feb 2022 01:43:15 GMT
ENV TOMCAT_VERSION=10.0.16
# Fri, 04 Feb 2022 01:43:15 GMT
ENV TOMCAT_SHA512=9b70f4db2c7b2efb5453cd581322b1137df7b6443acd6a8e278eaaf97de89c9ad0c7c7996a2d545ef1e4d965aca43c40d2b2c7d5e46b021695f87093143fbba2
# Fri, 04 Feb 2022 01:43:15 GMT
COPY dir:7709eb780787438bc663d44fc49743ab514d510784413769848ff8f86231e8aa in /usr/local/tomcat 
# Fri, 04 Feb 2022 01:43:20 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 04 Feb 2022 01:43:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 04 Feb 2022 01:43:23 GMT
EXPOSE 8080
# Fri, 04 Feb 2022 01:43:23 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:a024302f8a017855dd20a107ace079dd543c4bdfa8e7c11472771babbe298d2b`  
		Last Modified: Wed, 26 Jan 2022 01:47:01 GMT  
		Size: 50.4 MB (50437057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:289773030fdc98afe6cc53bdd0c05332ea8ff21ad836afa1d3042388953c43f8`  
		Last Modified: Wed, 26 Jan 2022 02:23:32 GMT  
		Size: 7.8 MB (7833856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81bb8b3399fe8dd0b83bd5e32a97e5183ab235d6fb4cc0b5dfabb20e6653e715`  
		Last Modified: Wed, 26 Jan 2022 02:23:32 GMT  
		Size: 10.0 MB (9997205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8c4cd1777c2ad6fc91f6816c9487e7b60fa8737eb08fdedd368869db4c6dcad`  
		Last Modified: Wed, 26 Jan 2022 09:54:54 GMT  
		Size: 5.5 MB (5531148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5b2343e0bc6241190b190e921fb66f3dbd6fe422af4a88bb9ef0ae9bece9b39`  
		Last Modified: Wed, 26 Jan 2022 09:58:35 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64618cd75e529e5d0e280df0519a827c990dca118cf99708dfd80b9d40cb597b`  
		Last Modified: Thu, 03 Feb 2022 21:05:20 GMT  
		Size: 41.4 MB (41395113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcaf928fa8f068e2481ffb0905ac05a5e3cf5fb4d337a78e27c39365a220cabc`  
		Last Modified: Fri, 04 Feb 2022 02:25:35 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b26d7d8707d99c4582ef3205d4df6e7768d8c90b6400ff3c12f74bf465945e95`  
		Last Modified: Fri, 04 Feb 2022 02:25:36 GMT  
		Size: 12.5 MB (12547145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:078ce7f0ac3ada193a103834459faa473b01e1a69d95b676a5c4f996f877231f`  
		Last Modified: Fri, 04 Feb 2022 02:25:35 GMT  
		Size: 460.9 KB (460936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a1ff9c831a447dbfdfad00549dc8a92245b8955bc48d8e7db1a809412bd2a0`  
		Last Modified: Fri, 04 Feb 2022 02:25:35 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:jre8-openjdk-buster` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:b4dd528c3fa0250ed1188fcf249bf0e91a82c3b288f6697750bc1319359b6bd5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.6 MB (125629557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6214921989f00d40dd1cc3720c6ff5d8ab0a82d28e1c3547bbfd4656f5f5fa26`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 26 Jan 2022 01:42:41 GMT
ADD file:98a75269e438ff15cee16ad2763fe2698fb436bc4770c0ca27c059f66b65e56a in / 
# Wed, 26 Jan 2022 01:42:42 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:14:31 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Jan 2022 06:00:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 06:03:37 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 26 Jan 2022 06:03:38 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 26 Jan 2022 06:03:39 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 06:03:40 GMT
ENV LANG=C.UTF-8
# Thu, 03 Feb 2022 20:59:52 GMT
ENV JAVA_VERSION=8u322
# Thu, 03 Feb 2022 21:00:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_8u322b06.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 04 Feb 2022 00:57:15 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 04 Feb 2022 00:57:16 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Feb 2022 00:57:17 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 04 Feb 2022 00:57:18 GMT
WORKDIR /usr/local/tomcat
# Fri, 04 Feb 2022 00:57:19 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 04 Feb 2022 00:57:20 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 04 Feb 2022 00:57:21 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Fri, 04 Feb 2022 00:57:22 GMT
ENV TOMCAT_MAJOR=10
# Fri, 04 Feb 2022 00:57:23 GMT
ENV TOMCAT_VERSION=10.0.16
# Fri, 04 Feb 2022 00:57:24 GMT
ENV TOMCAT_SHA512=9b70f4db2c7b2efb5453cd581322b1137df7b6443acd6a8e278eaaf97de89c9ad0c7c7996a2d545ef1e4d965aca43c40d2b2c7d5e46b021695f87093143fbba2
# Fri, 04 Feb 2022 00:57:26 GMT
COPY dir:1e6ea146571fe047d85ac567e1a596ef0d05a577815ef6a9435b3ef47a8b2366 in /usr/local/tomcat 
# Fri, 04 Feb 2022 00:57:29 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 04 Feb 2022 00:57:31 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 04 Feb 2022 00:57:32 GMT
EXPOSE 8080
# Fri, 04 Feb 2022 00:57:33 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:ccd458f933f7966e412773ee1551aaf2433a5bf9adaae519e2ac7c9c3f8b5f89`  
		Last Modified: Wed, 26 Jan 2022 01:49:28 GMT  
		Size: 49.2 MB (49223041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3524e6d2c855bef1f32da73e00738b2e5e91e6a346d19f8b33e8e8117c82748`  
		Last Modified: Wed, 26 Jan 2022 02:25:05 GMT  
		Size: 7.7 MB (7695112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14cc9cf00cd9023559aeda43668c7d9d621318631bab103ae03b8a3787260048`  
		Last Modified: Wed, 26 Jan 2022 02:25:05 GMT  
		Size: 9.8 MB (9767300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32bb47824c903cca25cdc9a24eb3596e18ae0d673921bb6c79164a4ce0317c77`  
		Last Modified: Wed, 26 Jan 2022 06:27:25 GMT  
		Size: 5.5 MB (5505341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12dc49bec552e2f75fee5bc90dc9f53f90322354e3f0ad8852c42a9948fe9ade`  
		Last Modified: Wed, 26 Jan 2022 06:31:00 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43a566472d4770f395b054d6aab83196980d606d38a3011b3f3cb33018668ef`  
		Last Modified: Thu, 03 Feb 2022 21:20:54 GMT  
		Size: 40.7 MB (40659894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c69389b562a93be0c7b03e7346b20d7d914b891b12f764db72e19220cfe5416`  
		Last Modified: Fri, 04 Feb 2022 01:55:13 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e4f325e21f0023bc202a5697cd28f97cf5837d23e5aedf6f7afe2dc3423dee`  
		Last Modified: Fri, 04 Feb 2022 01:55:15 GMT  
		Size: 12.6 MB (12560312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf7e5810d13c6aba2546b8f2fe771ef6bb7eeb71c0e277e000b860be561e2673`  
		Last Modified: Fri, 04 Feb 2022 01:55:14 GMT  
		Size: 218.2 KB (218207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
