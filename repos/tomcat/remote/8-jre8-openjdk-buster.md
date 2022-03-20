## `tomcat:8-jre8-openjdk-buster`

```console
$ docker pull tomcat@sha256:540766086b0a050d2da38eeead34f08aa8001e896620c580848981d470fa4c04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:8-jre8-openjdk-buster` - linux; amd64

```console
$ docker pull tomcat@sha256:480b8d58d4655e1fa8b4d44cfa748146f61192a0252fe47c815e92bf7e3cfcc6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.9 MB (126852723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54f916dae862ffa969d79169834360b109601547ea681f5243587009e35fdc04`
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
# Sat, 19 Mar 2022 10:30:08 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 19 Mar 2022 10:30:09 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 19 Mar 2022 10:30:09 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 10:30:09 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 10:30:09 GMT
ENV JAVA_VERSION=8u322
# Sat, 19 Mar 2022 10:30:15 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_8u322b06.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Sun, 20 Mar 2022 11:26:35 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sun, 20 Mar 2022 11:26:35 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 20 Mar 2022 11:26:36 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sun, 20 Mar 2022 11:26:36 GMT
WORKDIR /usr/local/tomcat
# Sun, 20 Mar 2022 11:26:36 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sun, 20 Mar 2022 11:26:36 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sun, 20 Mar 2022 11:54:39 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Sun, 20 Mar 2022 11:54:39 GMT
ENV TOMCAT_MAJOR=8
# Sun, 20 Mar 2022 11:54:39 GMT
ENV TOMCAT_VERSION=8.5.76
# Sun, 20 Mar 2022 11:54:40 GMT
ENV TOMCAT_SHA512=7b84a311b2ba3b6c92eea5739275b45686ed893bc000c16ead0a3cfe7c166b12d42485e9eb9c40fe279d207a293c4de65db3107602794f2b8e6071bc4d2b53ed
# Sun, 20 Mar 2022 11:54:40 GMT
COPY dir:ac44181fdc85828dea834481f0fa29d596c42e44981d051c8c9efb4bab9eea0e in /usr/local/tomcat 
# Sun, 20 Mar 2022 11:54:43 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Sun, 20 Mar 2022 11:54:45 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Sun, 20 Mar 2022 11:54:45 GMT
EXPOSE 8080
# Sun, 20 Mar 2022 11:54:45 GMT
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
	-	`sha256:961b2b1ebb1dc930fa5954e4bf790035c372c34f69b5aaa9e484c981cc9b8105`  
		Last Modified: Sat, 19 Mar 2022 10:49:04 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f945d937f010be456d4f4e06aba96eff5c3520c5b2c85116c31a9bb2bcc60be`  
		Last Modified: Sat, 19 Mar 2022 10:49:11 GMT  
		Size: 41.4 MB (41395069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:093eb01f1b677e9aebc8f4c93fe4d8c21cfcd72a6942851be8dfa4b95cba49da`  
		Last Modified: Sun, 20 Mar 2022 12:17:28 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b8a0d9651314cc51807827164a2bee9732fd05895d5b604d00a245f9a206244`  
		Last Modified: Sun, 20 Mar 2022 14:12:38 GMT  
		Size: 11.2 MB (11195317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf35b624994a3c6b218d8ec61c2077c08a5cf61652c73e0863998f95a8f0022f`  
		Last Modified: Sun, 20 Mar 2022 14:12:37 GMT  
		Size: 460.9 KB (460878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3111f7c4ee3a75506c2e7e5d315cd3e425d749ac5f080e6a0dc78d92e90087a`  
		Last Modified: Sun, 20 Mar 2022 14:12:36 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:8-jre8-openjdk-buster` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:bf6ccb5e70fa0cdfecd1066955f9a45c0c37d8c5156df91c527c9696931b192a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124280089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c0bc65ddbce4fc623fad5583ba830d40f072b9f4bc1bae507309e8e9899c252`
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
# Thu, 17 Mar 2022 23:37:41 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 17 Mar 2022 23:37:41 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 17 Mar 2022 23:37:42 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Mar 2022 23:37:43 GMT
ENV LANG=C.UTF-8
# Thu, 17 Mar 2022 23:37:44 GMT
ENV JAVA_VERSION=8u322
# Thu, 17 Mar 2022 23:37:57 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_8u322b06.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Sat, 19 Mar 2022 11:31:17 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 19 Mar 2022 11:31:18 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 11:31:19 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sat, 19 Mar 2022 11:31:20 GMT
WORKDIR /usr/local/tomcat
# Sat, 19 Mar 2022 11:31:21 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 19 Mar 2022 11:31:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 19 Mar 2022 12:05:13 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Sat, 19 Mar 2022 12:05:14 GMT
ENV TOMCAT_MAJOR=8
# Sat, 19 Mar 2022 12:05:15 GMT
ENV TOMCAT_VERSION=8.5.76
# Sat, 19 Mar 2022 12:05:16 GMT
ENV TOMCAT_SHA512=7b84a311b2ba3b6c92eea5739275b45686ed893bc000c16ead0a3cfe7c166b12d42485e9eb9c40fe279d207a293c4de65db3107602794f2b8e6071bc4d2b53ed
# Sat, 19 Mar 2022 12:05:18 GMT
COPY dir:d619de0ff550cf5c2b54d63f98d85e0d22ca7f1ecd3588b6f38387fd67f17898 in /usr/local/tomcat 
# Sat, 19 Mar 2022 12:05:21 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 12:05:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Sat, 19 Mar 2022 12:05:24 GMT
EXPOSE 8080
# Sat, 19 Mar 2022 12:05:25 GMT
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
	-	`sha256:c28b1a3c630183836ef1838d016b5f0f97e467700194e16f84cc4ba76a1934fc`  
		Last Modified: Fri, 18 Mar 2022 00:03:52 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a668d7a2d60b4d80e69ef05b92584aea9a6ae49ebb919f2126c4f4b0a496fc85`  
		Last Modified: Fri, 18 Mar 2022 00:03:57 GMT  
		Size: 40.7 MB (40659858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3d7ec91ac8a38fc6d36356fd0da7cfc5a06a4752dcfcb3dbfe10c809e93774`  
		Last Modified: Sat, 19 Mar 2022 12:39:08 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ad63f1bd03ca881f9a7183b8fc25262f4c39aa44592045211ea64db508a82cb`  
		Last Modified: Sat, 19 Mar 2022 14:36:12 GMT  
		Size: 11.2 MB (11209920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e67d86fb41c96a3e48791df0ff97eab0a19658a5c1a06b9af134664ced22765b`  
		Last Modified: Sat, 19 Mar 2022 14:36:10 GMT  
		Size: 218.2 KB (218196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
