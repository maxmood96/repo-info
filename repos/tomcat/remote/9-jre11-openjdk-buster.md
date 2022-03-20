## `tomcat:9-jre11-openjdk-buster`

```console
$ docker pull tomcat@sha256:e7f61e313e9190b538d87e0d5bc90c1618dbb8313dea5fa93f065dfe3b9525b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:9-jre11-openjdk-buster` - linux; amd64

```console
$ docker pull tomcat@sha256:d4af7e5330513597d96cbcbdcb6cd982238e68453032296e16a3b75ff22b766a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.3 MB (133326499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4bba7e8ce34662a8f6900f0dca0e2c2d051becc76d01594fd55f22555e22cf5`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 17 Mar 2022 04:04:10 GMT
ADD file:28eba36c2d43c343d9dfd5ace80db0043e1f92aa3afb4aa95d6cbb54d7e6efef in / 
# Thu, 17 Mar 2022 04:04:11 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:31:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:32:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 19 Mar 2022 10:27:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:27:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Sat, 19 Mar 2022 10:27:31 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 19 Mar 2022 10:27:31 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 10:27:32 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 10:27:32 GMT
ENV JAVA_VERSION=11.0.14.1
# Sat, 19 Mar 2022 10:27:55 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_x64_linux_11.0.14.1_1.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_aarch64_linux_11.0.14.1_1.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Sun, 20 Mar 2022 11:10:50 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sun, 20 Mar 2022 11:10:50 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 20 Mar 2022 11:10:51 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sun, 20 Mar 2022 11:10:51 GMT
WORKDIR /usr/local/tomcat
# Sun, 20 Mar 2022 11:10:51 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sun, 20 Mar 2022 11:10:51 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sun, 20 Mar 2022 11:36:45 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Sun, 20 Mar 2022 11:36:45 GMT
ENV TOMCAT_MAJOR=9
# Sun, 20 Mar 2022 11:36:45 GMT
ENV TOMCAT_VERSION=9.0.60
# Sun, 20 Mar 2022 11:36:45 GMT
ENV TOMCAT_SHA512=a4d43ac45f76e29d3dea23a2712c7570a11419aad7a1af2d1533454709c020b59666c7f9e063a77120224e0cbd4020cac06ca596dda7057cacb9a8a7e6d73eea
# Sun, 20 Mar 2022 11:36:46 GMT
COPY dir:ea92026b7eb5e7e1db20efd6e69784597117bb5c5ab2ba7cb74c2d119d536c02 in /usr/local/tomcat 
# Sun, 20 Mar 2022 11:36:49 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Sun, 20 Mar 2022 11:36:51 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Sun, 20 Mar 2022 11:36:51 GMT
EXPOSE 8080
# Sun, 20 Mar 2022 11:36:51 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:7d66b83ec869a899bc8364af9c9eb0f1a5ba6907f699ef52f3182e19e2598924`  
		Last Modified: Thu, 17 Mar 2022 04:10:29 GMT  
		Size: 50.4 MB (50437294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d88439e7b50a5f3923f67f432b6863c1e11adf4e45bf9740515d2cc01fd8e155`  
		Last Modified: Fri, 18 Mar 2022 07:04:47 GMT  
		Size: 7.8 MB (7834140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22360a9558f73f04bb5e4dbe6dbe1584cb913040ae66388a8db66fc2ed131002`  
		Last Modified: Fri, 18 Mar 2022 07:04:47 GMT  
		Size: 10.0 MB (9997260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64eaf79a044669ac4a77db074212e085e5f13aec085e1f08050790cb04aad920`  
		Last Modified: Sat, 19 Mar 2022 10:46:20 GMT  
		Size: 5.5 MB (5532255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e469609e9ec2676caa5d062ead7d0f994058374f53b23c6a33a8a20d86e34d0a`  
		Last Modified: Sat, 19 Mar 2022 10:46:20 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c688f20bd440c61c0446aa66f3570f9c2175adf6dd85c64b7c1d47e749d8573`  
		Last Modified: Sat, 19 Mar 2022 10:46:26 GMT  
		Size: 46.9 MB (46879453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf9f66fba5c7f4cd14206513da6ef0b7e51d1fbee94128ba83c1c0fe4e1cd471`  
		Last Modified: Sun, 20 Mar 2022 12:08:38 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f7ad0eaaa307ebb83b080c74e8be21a601400826d0c096c9b0aca390b05ac37`  
		Last Modified: Sun, 20 Mar 2022 12:22:43 GMT  
		Size: 12.2 MB (12184675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b324e2edfec95dff4cd4afbdaae70ccfef498e9b111f7ad3155d1b2605426e0`  
		Last Modified: Sun, 20 Mar 2022 12:22:42 GMT  
		Size: 460.9 KB (460910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d8124a5e5a64f2abe62af5741efc3d43083aaac813e7b7af9d84d885459a612`  
		Last Modified: Sun, 20 Mar 2022 12:22:41 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre11-openjdk-buster` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:7ccf6ae100dcac6534f3cd1d63134125daad709ce0a37235a1cb8b32bd8b7709
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130590467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02e47dd5500459e44043b8e0339f22f0cc918bb4b73efbca7639c10681d6d16f`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 17 Mar 2022 03:22:08 GMT
ADD file:37cabd1fec04269c22fc158f62ce5bc655934f2e58fb1ff3a1e366a33ba9bc18 in / 
# Thu, 17 Mar 2022 03:22:09 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 22:12:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 22:12:25 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Mar 2022 23:33:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 23:33:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 17 Mar 2022 23:33:12 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 17 Mar 2022 23:33:13 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Mar 2022 23:33:14 GMT
ENV LANG=C.UTF-8
# Thu, 17 Mar 2022 23:33:15 GMT
ENV JAVA_VERSION=11.0.14.1
# Thu, 17 Mar 2022 23:33:24 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_x64_linux_11.0.14.1_1.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_aarch64_linux_11.0.14.1_1.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Sat, 19 Mar 2022 11:16:23 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 19 Mar 2022 11:16:24 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 11:16:25 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sat, 19 Mar 2022 11:16:26 GMT
WORKDIR /usr/local/tomcat
# Sat, 19 Mar 2022 11:16:27 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 19 Mar 2022 11:16:28 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 19 Mar 2022 11:41:28 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Sat, 19 Mar 2022 11:41:28 GMT
ENV TOMCAT_MAJOR=9
# Sat, 19 Mar 2022 11:41:29 GMT
ENV TOMCAT_VERSION=9.0.60
# Sat, 19 Mar 2022 11:41:30 GMT
ENV TOMCAT_SHA512=a4d43ac45f76e29d3dea23a2712c7570a11419aad7a1af2d1533454709c020b59666c7f9e063a77120224e0cbd4020cac06ca596dda7057cacb9a8a7e6d73eea
# Sat, 19 Mar 2022 11:41:32 GMT
COPY dir:9182be0c258b1c0572c237e42a64c01cbe10d02e7a1ebf64346310107593689e in /usr/local/tomcat 
# Sat, 19 Mar 2022 11:41:35 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 11:41:37 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Sat, 19 Mar 2022 11:41:38 GMT
EXPOSE 8080
# Sat, 19 Mar 2022 11:41:39 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:3996f04b7c6c17d8b25c04c7287353b896b4a0b10ab440f47d00573a7d5c3e17`  
		Last Modified: Thu, 17 Mar 2022 03:28:59 GMT  
		Size: 49.2 MB (49222993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80907b498681187ef4aa817ec6f39ba351e376afbb4fcf4415841ab9015cfc59`  
		Last Modified: Thu, 17 Mar 2022 22:22:15 GMT  
		Size: 7.7 MB (7695349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8327dc7899c1a628cf11f95bb594fca3c86e45d1f4f0eb73d2ba9058eba5927`  
		Last Modified: Thu, 17 Mar 2022 22:22:15 GMT  
		Size: 9.8 MB (9767203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c8cde2d5e9d31d1b6eddddf3ae8e11b9d09f2a5a27bf2a825be248088e76a3`  
		Last Modified: Fri, 18 Mar 2022 00:00:18 GMT  
		Size: 5.5 MB (5506222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6dfd2091f9b4b415fa8718e6baac650787b57b27b3acf0a43627f6b740bbca`  
		Last Modified: Fri, 18 Mar 2022 00:00:17 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b2d9793db2e600ff10402845afdf80f6b71070db85594a1aee9f083abf6794`  
		Last Modified: Fri, 18 Mar 2022 00:00:24 GMT  
		Size: 46.0 MB (45983055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:955dae82cc2f9fc58037fba8f031809ca7707f4ca328cfa15c74bbcb5d95e948`  
		Last Modified: Sat, 19 Mar 2022 12:29:17 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:424f9197799e392b7eb624d9b998bbdc4fdefa87bfe139e12cac4b65658ce212`  
		Last Modified: Sat, 19 Mar 2022 12:44:35 GMT  
		Size: 12.2 MB (12197049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:916e2ae03241c5d70570a0502924a81affd0a0e64993c32acb2e20ee371b7c0a`  
		Last Modified: Sat, 19 Mar 2022 12:44:34 GMT  
		Size: 218.2 KB (218249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
