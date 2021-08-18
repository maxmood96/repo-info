<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `tomee`

-	[`tomee:11-jre-8.0.6-microprofile`](#tomee11-jre-806-microprofile)
-	[`tomee:11-jre-8.0.6-plume`](#tomee11-jre-806-plume)
-	[`tomee:11-jre-8.0.6-plus`](#tomee11-jre-806-plus)
-	[`tomee:11-jre-8.0.6-webprofile`](#tomee11-jre-806-webprofile)
-	[`tomee:7`](#tomee7)
-	[`tomee:7.0`](#tomee70)
-	[`tomee:7.0.9-plume`](#tomee709-plume)
-	[`tomee:7.0.9-plus`](#tomee709-plus)
-	[`tomee:7.1`](#tomee71)
-	[`tomee:7.1.4-microprofile`](#tomee714-microprofile)
-	[`tomee:7.1.4-plume`](#tomee714-plume)
-	[`tomee:7.1.4-plus`](#tomee714-plus)
-	[`tomee:7.1.4-webprofile`](#tomee714-webprofile)
-	[`tomee:8`](#tomee8)
-	[`tomee:8-jre-7.0.9-plume`](#tomee8-jre-709-plume)
-	[`tomee:8-jre-7.0.9-plus`](#tomee8-jre-709-plus)
-	[`tomee:8-jre-7.0.9-webprofile`](#tomee8-jre-709-webprofile)
-	[`tomee:8-jre-7.1.4-microprofile`](#tomee8-jre-714-microprofile)
-	[`tomee:8-jre-7.1.4-plume`](#tomee8-jre-714-plume)
-	[`tomee:8-jre-7.1.4-plus`](#tomee8-jre-714-plus)
-	[`tomee:8-jre-7.1.4-webprofile`](#tomee8-jre-714-webprofile)
-	[`tomee:8-jre-8.0.6-microprofile`](#tomee8-jre-806-microprofile)
-	[`tomee:8-jre-8.0.6-plume`](#tomee8-jre-806-plume)
-	[`tomee:8-jre-8.0.6-plus`](#tomee8-jre-806-plus)
-	[`tomee:8-jre-8.0.6-webprofile`](#tomee8-jre-806-webprofile)
-	[`tomee:8.0.6-microprofile`](#tomee806-microprofile)
-	[`tomee:8.0.6-plume`](#tomee806-plume)
-	[`tomee:8.0.6-plus`](#tomee806-plus)
-	[`tomee:8.0.6-webprofile`](#tomee806-webprofile)
-	[`tomee:latest`](#tomeelatest)

## `tomee:11-jre-8.0.6-microprofile`

```console
$ docker pull tomee@sha256:5a78751cb7d3f58f8040f139ae208cbcef4672a2271e46d4e8ff13f5e3733d1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `tomee:11-jre-8.0.6-microprofile` - linux; amd64

```console
$ docker pull tomee@sha256:525060bbb4f91ca72a3f5a82608191548b91535345f674e5f1bd4e6b68bec3a7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.1 MB (183127940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdfe4d955f75ce8b798076b95e67583da634731da28fbd2a2db92813f1bd28b1`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 17 Aug 2021 01:23:52 GMT
ADD file:b9e6354f7b545096b6cb6072a50de0dffa2232f22d1972a4679f46a7e6394cae in / 
# Tue, 17 Aug 2021 01:23:53 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 09:20:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 09:20:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Aug 2021 07:05:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 18 Aug 2021 07:05:20 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Wed, 18 Aug 2021 07:05:21 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 18 Aug 2021 07:05:21 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Aug 2021 07:05:21 GMT
ENV LANG=C.UTF-8
# Wed, 18 Aug 2021 07:05:22 GMT
ENV JAVA_VERSION=11.0.12
# Wed, 18 Aug 2021 07:05:28 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jre_x64_linux_11.0.12_7.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jre_aarch64_linux_11.0.12_7.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Wed, 18 Aug 2021 21:03:33 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Aug 2021 21:03:34 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 18 Aug 2021 21:03:34 GMT
WORKDIR /usr/local/tomee
# Wed, 18 Aug 2021 21:03:35 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Wed, 18 Aug 2021 21:03:41 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Wed, 18 Aug 2021 21:03:42 GMT
ENV TOMEE_VER=8.0.6
# Wed, 18 Aug 2021 21:04:06 GMT
ENV TOMEE_BUILD=microprofile
# Wed, 18 Aug 2021 21:04:13 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm bin/*.exe 	&& rm tomee.tar.gz*
# Wed, 18 Aug 2021 21:04:13 GMT
EXPOSE 8080
# Wed, 18 Aug 2021 21:04:13 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:1cfaf5c6f756207bc4607d40ddd440bd2bfa7ab455b2c3015ccf56d85cd1377b`  
		Last Modified: Tue, 17 Aug 2021 01:29:55 GMT  
		Size: 50.4 MB (50436201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4099a935a96edef1e9378de34e314d07fb3aea1b7205774055a1fa44a3819f4`  
		Last Modified: Tue, 17 Aug 2021 09:30:37 GMT  
		Size: 7.8 MB (7833079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e2960d83651b1494b4da6c97686e79cc760aa90a75948eed56786726f86928`  
		Last Modified: Tue, 17 Aug 2021 09:30:38 GMT  
		Size: 10.0 MB (9997209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02210be58959d874de759b34af368e884f52b8ac7643bd3cfaefe6b847bf92dd`  
		Last Modified: Wed, 18 Aug 2021 07:12:01 GMT  
		Size: 5.5 MB (5531118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99137bab1caf27aee8d1f5f962699a054178b8bc48ef8f5d17648337e8579837`  
		Last Modified: Wed, 18 Aug 2021 07:12:00 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38621337f17c0f871f3675b78bd321096624cd617666be70bc9a259788e93041`  
		Last Modified: Wed, 18 Aug 2021 07:12:07 GMT  
		Size: 46.9 MB (46863974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0238d73f652115c041086e00940b503df0976e22ba3f9f5b2a8d9a7b609d7173`  
		Last Modified: Wed, 18 Aug 2021 21:07:31 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abea88b63ce675e6fd5e791cdca5a2a54dd1baa53825c2c8f5bdc7cc0b073134`  
		Last Modified: Wed, 18 Aug 2021 21:07:31 GMT  
		Size: 21.0 KB (21021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f9797dfac064d2e34cae4a482084df62277a997efd6b382a2ef65a3735fe2d`  
		Last Modified: Wed, 18 Aug 2021 21:08:04 GMT  
		Size: 62.4 MB (62444954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:11-jre-8.0.6-plume`

```console
$ docker pull tomee@sha256:f3d2ff3de9277db837ab1041d6c177a36d03216eb0f984eda87a9cfd7b6b216a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `tomee:11-jre-8.0.6-plume` - linux; amd64

```console
$ docker pull tomee@sha256:e3794e0fcc3b7883c5265388d0ea382a3dc86fc958eb8e23042ecde22f8246cd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.3 MB (195303083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceb62bbf4720148af49aaa7f8578ffe94d9372986dd0544172aed3ae774b2bbd`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 17 Aug 2021 01:23:52 GMT
ADD file:b9e6354f7b545096b6cb6072a50de0dffa2232f22d1972a4679f46a7e6394cae in / 
# Tue, 17 Aug 2021 01:23:53 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 09:20:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 09:20:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Aug 2021 07:05:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 18 Aug 2021 07:05:20 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Wed, 18 Aug 2021 07:05:21 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 18 Aug 2021 07:05:21 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Aug 2021 07:05:21 GMT
ENV LANG=C.UTF-8
# Wed, 18 Aug 2021 07:05:22 GMT
ENV JAVA_VERSION=11.0.12
# Wed, 18 Aug 2021 07:05:28 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jre_x64_linux_11.0.12_7.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jre_aarch64_linux_11.0.12_7.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Wed, 18 Aug 2021 21:03:33 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Aug 2021 21:03:34 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 18 Aug 2021 21:03:34 GMT
WORKDIR /usr/local/tomee
# Wed, 18 Aug 2021 21:03:35 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Wed, 18 Aug 2021 21:03:41 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Wed, 18 Aug 2021 21:03:42 GMT
ENV TOMEE_VER=8.0.6
# Wed, 18 Aug 2021 21:03:42 GMT
ENV TOMEE_BUILD=plume
# Wed, 18 Aug 2021 21:03:49 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm bin/*.exe 	&& rm tomee.tar.gz*
# Wed, 18 Aug 2021 21:03:49 GMT
EXPOSE 8080
# Wed, 18 Aug 2021 21:03:49 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:1cfaf5c6f756207bc4607d40ddd440bd2bfa7ab455b2c3015ccf56d85cd1377b`  
		Last Modified: Tue, 17 Aug 2021 01:29:55 GMT  
		Size: 50.4 MB (50436201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4099a935a96edef1e9378de34e314d07fb3aea1b7205774055a1fa44a3819f4`  
		Last Modified: Tue, 17 Aug 2021 09:30:37 GMT  
		Size: 7.8 MB (7833079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e2960d83651b1494b4da6c97686e79cc760aa90a75948eed56786726f86928`  
		Last Modified: Tue, 17 Aug 2021 09:30:38 GMT  
		Size: 10.0 MB (9997209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02210be58959d874de759b34af368e884f52b8ac7643bd3cfaefe6b847bf92dd`  
		Last Modified: Wed, 18 Aug 2021 07:12:01 GMT  
		Size: 5.5 MB (5531118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99137bab1caf27aee8d1f5f962699a054178b8bc48ef8f5d17648337e8579837`  
		Last Modified: Wed, 18 Aug 2021 07:12:00 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38621337f17c0f871f3675b78bd321096624cd617666be70bc9a259788e93041`  
		Last Modified: Wed, 18 Aug 2021 07:12:07 GMT  
		Size: 46.9 MB (46863974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0238d73f652115c041086e00940b503df0976e22ba3f9f5b2a8d9a7b609d7173`  
		Last Modified: Wed, 18 Aug 2021 21:07:31 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abea88b63ce675e6fd5e791cdca5a2a54dd1baa53825c2c8f5bdc7cc0b073134`  
		Last Modified: Wed, 18 Aug 2021 21:07:31 GMT  
		Size: 21.0 KB (21021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b07bd22572328a7631757bdde85198dcb3ea2658462a2d5b4bf2be7939a76fb9`  
		Last Modified: Wed, 18 Aug 2021 21:07:35 GMT  
		Size: 74.6 MB (74620097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:11-jre-8.0.6-plus`

```console
$ docker pull tomee@sha256:44147e49e1f8c6a5a62b672566627d3e05326d8b5c70f2219077f043bd79ddc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `tomee:11-jre-8.0.6-plus` - linux; amd64

```console
$ docker pull tomee@sha256:06bb64a6a9c5a04a2eb85e581f6b250d2a96cc58f22d84c61a991d27c1a5e4b5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.0 MB (188022199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc33323e0f6f16700746f84a32bb0779f8ec13ede112eeb99e4cb24c9e3a1d31`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 17 Aug 2021 01:23:52 GMT
ADD file:b9e6354f7b545096b6cb6072a50de0dffa2232f22d1972a4679f46a7e6394cae in / 
# Tue, 17 Aug 2021 01:23:53 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 09:20:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 09:20:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Aug 2021 07:05:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 18 Aug 2021 07:05:20 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Wed, 18 Aug 2021 07:05:21 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 18 Aug 2021 07:05:21 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Aug 2021 07:05:21 GMT
ENV LANG=C.UTF-8
# Wed, 18 Aug 2021 07:05:22 GMT
ENV JAVA_VERSION=11.0.12
# Wed, 18 Aug 2021 07:05:28 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jre_x64_linux_11.0.12_7.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jre_aarch64_linux_11.0.12_7.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Wed, 18 Aug 2021 21:03:33 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Aug 2021 21:03:34 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 18 Aug 2021 21:03:34 GMT
WORKDIR /usr/local/tomee
# Wed, 18 Aug 2021 21:03:35 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Wed, 18 Aug 2021 21:03:41 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Wed, 18 Aug 2021 21:03:42 GMT
ENV TOMEE_VER=8.0.6
# Wed, 18 Aug 2021 21:03:55 GMT
ENV TOMEE_BUILD=plus
# Wed, 18 Aug 2021 21:04:02 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm bin/*.exe 	&& rm tomee.tar.gz*
# Wed, 18 Aug 2021 21:04:02 GMT
EXPOSE 8080
# Wed, 18 Aug 2021 21:04:02 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:1cfaf5c6f756207bc4607d40ddd440bd2bfa7ab455b2c3015ccf56d85cd1377b`  
		Last Modified: Tue, 17 Aug 2021 01:29:55 GMT  
		Size: 50.4 MB (50436201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4099a935a96edef1e9378de34e314d07fb3aea1b7205774055a1fa44a3819f4`  
		Last Modified: Tue, 17 Aug 2021 09:30:37 GMT  
		Size: 7.8 MB (7833079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e2960d83651b1494b4da6c97686e79cc760aa90a75948eed56786726f86928`  
		Last Modified: Tue, 17 Aug 2021 09:30:38 GMT  
		Size: 10.0 MB (9997209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02210be58959d874de759b34af368e884f52b8ac7643bd3cfaefe6b847bf92dd`  
		Last Modified: Wed, 18 Aug 2021 07:12:01 GMT  
		Size: 5.5 MB (5531118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99137bab1caf27aee8d1f5f962699a054178b8bc48ef8f5d17648337e8579837`  
		Last Modified: Wed, 18 Aug 2021 07:12:00 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38621337f17c0f871f3675b78bd321096624cd617666be70bc9a259788e93041`  
		Last Modified: Wed, 18 Aug 2021 07:12:07 GMT  
		Size: 46.9 MB (46863974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0238d73f652115c041086e00940b503df0976e22ba3f9f5b2a8d9a7b609d7173`  
		Last Modified: Wed, 18 Aug 2021 21:07:31 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abea88b63ce675e6fd5e791cdca5a2a54dd1baa53825c2c8f5bdc7cc0b073134`  
		Last Modified: Wed, 18 Aug 2021 21:07:31 GMT  
		Size: 21.0 KB (21021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab8bc65a5133c12b559131b73f78d03a5b11057495b2da409de06a0d2c55a19d`  
		Last Modified: Wed, 18 Aug 2021 21:07:50 GMT  
		Size: 67.3 MB (67339213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:11-jre-8.0.6-webprofile`

```console
$ docker pull tomee@sha256:756706fa209e96a1fcfaa6d44902df08d72d1ae98ed33bb7f837770eec6b96b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `tomee:11-jre-8.0.6-webprofile` - linux; amd64

```console
$ docker pull tomee@sha256:947e86961e6e952a8a1481e597db5e69d068b1487801c477e2777d4dd90458e2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.7 MB (167666075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c351eb6566105c3d7b95afc4d89da3efd5cf37902af3d65a40e82d527679563`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 17 Aug 2021 01:23:52 GMT
ADD file:b9e6354f7b545096b6cb6072a50de0dffa2232f22d1972a4679f46a7e6394cae in / 
# Tue, 17 Aug 2021 01:23:53 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 09:20:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 09:20:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Aug 2021 07:05:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 18 Aug 2021 07:05:20 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Wed, 18 Aug 2021 07:05:21 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 18 Aug 2021 07:05:21 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Aug 2021 07:05:21 GMT
ENV LANG=C.UTF-8
# Wed, 18 Aug 2021 07:05:22 GMT
ENV JAVA_VERSION=11.0.12
# Wed, 18 Aug 2021 07:05:28 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jre_x64_linux_11.0.12_7.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jre_aarch64_linux_11.0.12_7.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Wed, 18 Aug 2021 21:03:33 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Aug 2021 21:03:34 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 18 Aug 2021 21:03:34 GMT
WORKDIR /usr/local/tomee
# Wed, 18 Aug 2021 21:03:35 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Wed, 18 Aug 2021 21:03:41 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Wed, 18 Aug 2021 21:03:42 GMT
ENV TOMEE_VER=8.0.6
# Wed, 18 Aug 2021 21:04:16 GMT
ENV TOMEE_BUILD=webprofile
# Wed, 18 Aug 2021 21:04:21 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm bin/*.exe 	&& rm tomee.tar.gz*
# Wed, 18 Aug 2021 21:04:21 GMT
EXPOSE 8080
# Wed, 18 Aug 2021 21:04:22 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:1cfaf5c6f756207bc4607d40ddd440bd2bfa7ab455b2c3015ccf56d85cd1377b`  
		Last Modified: Tue, 17 Aug 2021 01:29:55 GMT  
		Size: 50.4 MB (50436201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4099a935a96edef1e9378de34e314d07fb3aea1b7205774055a1fa44a3819f4`  
		Last Modified: Tue, 17 Aug 2021 09:30:37 GMT  
		Size: 7.8 MB (7833079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e2960d83651b1494b4da6c97686e79cc760aa90a75948eed56786726f86928`  
		Last Modified: Tue, 17 Aug 2021 09:30:38 GMT  
		Size: 10.0 MB (9997209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02210be58959d874de759b34af368e884f52b8ac7643bd3cfaefe6b847bf92dd`  
		Last Modified: Wed, 18 Aug 2021 07:12:01 GMT  
		Size: 5.5 MB (5531118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99137bab1caf27aee8d1f5f962699a054178b8bc48ef8f5d17648337e8579837`  
		Last Modified: Wed, 18 Aug 2021 07:12:00 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38621337f17c0f871f3675b78bd321096624cd617666be70bc9a259788e93041`  
		Last Modified: Wed, 18 Aug 2021 07:12:07 GMT  
		Size: 46.9 MB (46863974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0238d73f652115c041086e00940b503df0976e22ba3f9f5b2a8d9a7b609d7173`  
		Last Modified: Wed, 18 Aug 2021 21:07:31 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abea88b63ce675e6fd5e791cdca5a2a54dd1baa53825c2c8f5bdc7cc0b073134`  
		Last Modified: Wed, 18 Aug 2021 21:07:31 GMT  
		Size: 21.0 KB (21021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7bd68da3315025fb523b0d63d54be4e8fb29ee0ffe220f66e4925b760ff3b19`  
		Last Modified: Wed, 18 Aug 2021 21:08:18 GMT  
		Size: 47.0 MB (46983089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:7`

```console
$ docker pull tomee@sha256:1e202f62302770b1cfe8bfc29f38cdde52e17679eac3409e3f5cc761ab3586d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `tomee:7` - linux; amd64

```console
$ docker pull tomee@sha256:b8ca8557dc06de3737f9e200dddca3748992c62b25019b18c232fd4cc3431d39
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.7 MB (155706600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8938236c786a5a114e41623631b45a116ee1f54ce54c46f9138c9a8e2f8630`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 17 Aug 2021 01:23:52 GMT
ADD file:b9e6354f7b545096b6cb6072a50de0dffa2232f22d1972a4679f46a7e6394cae in / 
# Tue, 17 Aug 2021 01:23:53 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 09:20:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 09:20:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Aug 2021 07:05:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 18 Aug 2021 07:06:03 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 18 Aug 2021 07:06:04 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 18 Aug 2021 07:06:04 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Aug 2021 07:06:04 GMT
ENV LANG=C.UTF-8
# Wed, 18 Aug 2021 07:06:05 GMT
ENV JAVA_VERSION=8u302
# Wed, 18 Aug 2021 07:06:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_x64_linux_8u302b08.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_aarch64_linux_8u302b08.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Wed, 18 Aug 2021 21:01:37 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Aug 2021 21:01:38 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 18 Aug 2021 21:01:38 GMT
WORKDIR /usr/local/tomee
# Wed, 18 Aug 2021 21:01:38 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Wed, 18 Aug 2021 21:01:49 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Wed, 18 Aug 2021 21:02:17 GMT
ENV TOMEE_VER=7.1.4
# Wed, 18 Aug 2021 21:02:45 GMT
ENV TOMEE_BUILD=webprofile
# Wed, 18 Aug 2021 21:02:50 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Wed, 18 Aug 2021 21:02:51 GMT
EXPOSE 8080
# Wed, 18 Aug 2021 21:02:51 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:1cfaf5c6f756207bc4607d40ddd440bd2bfa7ab455b2c3015ccf56d85cd1377b`  
		Last Modified: Tue, 17 Aug 2021 01:29:55 GMT  
		Size: 50.4 MB (50436201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4099a935a96edef1e9378de34e314d07fb3aea1b7205774055a1fa44a3819f4`  
		Last Modified: Tue, 17 Aug 2021 09:30:37 GMT  
		Size: 7.8 MB (7833079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e2960d83651b1494b4da6c97686e79cc760aa90a75948eed56786726f86928`  
		Last Modified: Tue, 17 Aug 2021 09:30:38 GMT  
		Size: 10.0 MB (9997209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02210be58959d874de759b34af368e884f52b8ac7643bd3cfaefe6b847bf92dd`  
		Last Modified: Wed, 18 Aug 2021 07:12:01 GMT  
		Size: 5.5 MB (5531118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5e6eb5c7de7d87b3d4bad5c7ac2da2c2943b073dd07ffec22cd79082839eec`  
		Last Modified: Wed, 18 Aug 2021 07:12:57 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa71fb980438da57be6fdbd979262a55138aaab7b0acb4ac8b6b04578854660`  
		Last Modified: Wed, 18 Aug 2021 07:13:01 GMT  
		Size: 41.4 MB (41367106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22b65d65f44a9befc0e14b90d8d92b02546463c854c0ced84d707c164dc5e39`  
		Last Modified: Wed, 18 Aug 2021 21:05:00 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf51b27dd69b75ab79c0f91e0edc4957eda7aa2f51ce1ca1bae1c8d4683bd5e`  
		Last Modified: Wed, 18 Aug 2021 21:05:00 GMT  
		Size: 21.0 KB (21047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97c93c5dda9d26265a04b6f1e8170adf46d494ab0b32d4c81735a4e3ddf3f3c5`  
		Last Modified: Wed, 18 Aug 2021 21:06:28 GMT  
		Size: 40.5 MB (40520456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:7.0`

```console
$ docker pull tomee@sha256:2bd542f939693d3812b9942b1625236121b6e4a631aaa003c3c11bc18bb98853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `tomee:7.0` - linux; amd64

```console
$ docker pull tomee@sha256:12675c26a4fb8bfe773056123cb250996c5c680584cfbfdd4a3d6c8662edcfb4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.6 MB (153592617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c92eabfce57332c0bd646ac24137cbf58b05c707b546e2111515c15dc44a8e`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 17 Aug 2021 01:23:52 GMT
ADD file:b9e6354f7b545096b6cb6072a50de0dffa2232f22d1972a4679f46a7e6394cae in / 
# Tue, 17 Aug 2021 01:23:53 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 09:20:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 09:20:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Aug 2021 07:05:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 18 Aug 2021 07:06:03 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 18 Aug 2021 07:06:04 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 18 Aug 2021 07:06:04 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Aug 2021 07:06:04 GMT
ENV LANG=C.UTF-8
# Wed, 18 Aug 2021 07:06:05 GMT
ENV JAVA_VERSION=8u302
# Wed, 18 Aug 2021 07:06:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_x64_linux_8u302b08.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_aarch64_linux_8u302b08.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Wed, 18 Aug 2021 21:01:37 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Aug 2021 21:01:38 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 18 Aug 2021 21:01:38 GMT
WORKDIR /usr/local/tomee
# Wed, 18 Aug 2021 21:01:38 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Wed, 18 Aug 2021 21:01:49 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Wed, 18 Aug 2021 21:01:49 GMT
ENV TOMEE_VER=7.0.9
# Wed, 18 Aug 2021 21:02:09 GMT
ENV TOMEE_BUILD=webprofile
# Wed, 18 Aug 2021 21:02:13 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Wed, 18 Aug 2021 21:02:14 GMT
EXPOSE 8080
# Wed, 18 Aug 2021 21:02:14 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:1cfaf5c6f756207bc4607d40ddd440bd2bfa7ab455b2c3015ccf56d85cd1377b`  
		Last Modified: Tue, 17 Aug 2021 01:29:55 GMT  
		Size: 50.4 MB (50436201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4099a935a96edef1e9378de34e314d07fb3aea1b7205774055a1fa44a3819f4`  
		Last Modified: Tue, 17 Aug 2021 09:30:37 GMT  
		Size: 7.8 MB (7833079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e2960d83651b1494b4da6c97686e79cc760aa90a75948eed56786726f86928`  
		Last Modified: Tue, 17 Aug 2021 09:30:38 GMT  
		Size: 10.0 MB (9997209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02210be58959d874de759b34af368e884f52b8ac7643bd3cfaefe6b847bf92dd`  
		Last Modified: Wed, 18 Aug 2021 07:12:01 GMT  
		Size: 5.5 MB (5531118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5e6eb5c7de7d87b3d4bad5c7ac2da2c2943b073dd07ffec22cd79082839eec`  
		Last Modified: Wed, 18 Aug 2021 07:12:57 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa71fb980438da57be6fdbd979262a55138aaab7b0acb4ac8b6b04578854660`  
		Last Modified: Wed, 18 Aug 2021 07:13:01 GMT  
		Size: 41.4 MB (41367106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22b65d65f44a9befc0e14b90d8d92b02546463c854c0ced84d707c164dc5e39`  
		Last Modified: Wed, 18 Aug 2021 21:05:00 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf51b27dd69b75ab79c0f91e0edc4957eda7aa2f51ce1ca1bae1c8d4683bd5e`  
		Last Modified: Wed, 18 Aug 2021 21:05:00 GMT  
		Size: 21.0 KB (21047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14d0f1db2a8b22eefa91988cba85c83f8d5fb86dc6734429ee9f3afe1396f328`  
		Last Modified: Wed, 18 Aug 2021 21:05:32 GMT  
		Size: 38.4 MB (38406473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:7.0.9-plume`

```console
$ docker pull tomee@sha256:400a42d3b5bf887176e3953c6d2364ce9916b4e92c88a585fd92df897a5b82f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `tomee:7.0.9-plume` - linux; amd64

```console
$ docker pull tomee@sha256:473c41a8bde6e542dc29dc4a218bc9da122118cfd59be673ee8fa82e688043c1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.3 MB (178318592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a7dc755cc16f8f47e9fc9129580433815211a865a6c6f391d451e8eb558dc58`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 17 Aug 2021 01:23:52 GMT
ADD file:b9e6354f7b545096b6cb6072a50de0dffa2232f22d1972a4679f46a7e6394cae in / 
# Tue, 17 Aug 2021 01:23:53 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 09:20:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 09:20:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Aug 2021 07:05:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 18 Aug 2021 07:06:03 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 18 Aug 2021 07:06:04 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 18 Aug 2021 07:06:04 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Aug 2021 07:06:04 GMT
ENV LANG=C.UTF-8
# Wed, 18 Aug 2021 07:06:05 GMT
ENV JAVA_VERSION=8u302
# Wed, 18 Aug 2021 07:06:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_x64_linux_8u302b08.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_aarch64_linux_8u302b08.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Wed, 18 Aug 2021 21:01:37 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Aug 2021 21:01:38 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 18 Aug 2021 21:01:38 GMT
WORKDIR /usr/local/tomee
# Wed, 18 Aug 2021 21:01:38 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Wed, 18 Aug 2021 21:01:49 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Wed, 18 Aug 2021 21:01:49 GMT
ENV TOMEE_VER=7.0.9
# Wed, 18 Aug 2021 21:01:49 GMT
ENV TOMEE_BUILD=plume
# Wed, 18 Aug 2021 21:01:56 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Wed, 18 Aug 2021 21:01:56 GMT
EXPOSE 8080
# Wed, 18 Aug 2021 21:01:56 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:1cfaf5c6f756207bc4607d40ddd440bd2bfa7ab455b2c3015ccf56d85cd1377b`  
		Last Modified: Tue, 17 Aug 2021 01:29:55 GMT  
		Size: 50.4 MB (50436201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4099a935a96edef1e9378de34e314d07fb3aea1b7205774055a1fa44a3819f4`  
		Last Modified: Tue, 17 Aug 2021 09:30:37 GMT  
		Size: 7.8 MB (7833079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e2960d83651b1494b4da6c97686e79cc760aa90a75948eed56786726f86928`  
		Last Modified: Tue, 17 Aug 2021 09:30:38 GMT  
		Size: 10.0 MB (9997209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02210be58959d874de759b34af368e884f52b8ac7643bd3cfaefe6b847bf92dd`  
		Last Modified: Wed, 18 Aug 2021 07:12:01 GMT  
		Size: 5.5 MB (5531118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5e6eb5c7de7d87b3d4bad5c7ac2da2c2943b073dd07ffec22cd79082839eec`  
		Last Modified: Wed, 18 Aug 2021 07:12:57 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa71fb980438da57be6fdbd979262a55138aaab7b0acb4ac8b6b04578854660`  
		Last Modified: Wed, 18 Aug 2021 07:13:01 GMT  
		Size: 41.4 MB (41367106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22b65d65f44a9befc0e14b90d8d92b02546463c854c0ced84d707c164dc5e39`  
		Last Modified: Wed, 18 Aug 2021 21:05:00 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf51b27dd69b75ab79c0f91e0edc4957eda7aa2f51ce1ca1bae1c8d4683bd5e`  
		Last Modified: Wed, 18 Aug 2021 21:05:00 GMT  
		Size: 21.0 KB (21047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aaba43d0e2b04a695df01f8c37c39454f6a3877eceac3eb2edfc63740767112`  
		Last Modified: Wed, 18 Aug 2021 21:05:05 GMT  
		Size: 63.1 MB (63132448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:7.0.9-plus`

```console
$ docker pull tomee@sha256:d9deff0350b1ad7eaf33f28262e4486683bf594ba17dbdbab58900f6cba51517
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `tomee:7.0.9-plus` - linux; amd64

```console
$ docker pull tomee@sha256:9cc2ea48e81d74b4e544f91145a5380768d89c025191147a7c3c0e1e5b41167f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.2 MB (171246643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad1c15025cd29c02c278456d8d9d23cc4adc22e079be1118530892e851f93713`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 17 Aug 2021 01:23:52 GMT
ADD file:b9e6354f7b545096b6cb6072a50de0dffa2232f22d1972a4679f46a7e6394cae in / 
# Tue, 17 Aug 2021 01:23:53 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 09:20:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 09:20:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Aug 2021 07:05:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 18 Aug 2021 07:06:03 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 18 Aug 2021 07:06:04 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 18 Aug 2021 07:06:04 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Aug 2021 07:06:04 GMT
ENV LANG=C.UTF-8
# Wed, 18 Aug 2021 07:06:05 GMT
ENV JAVA_VERSION=8u302
# Wed, 18 Aug 2021 07:06:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_x64_linux_8u302b08.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_aarch64_linux_8u302b08.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Wed, 18 Aug 2021 21:01:37 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Aug 2021 21:01:38 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 18 Aug 2021 21:01:38 GMT
WORKDIR /usr/local/tomee
# Wed, 18 Aug 2021 21:01:38 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Wed, 18 Aug 2021 21:01:49 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Wed, 18 Aug 2021 21:01:49 GMT
ENV TOMEE_VER=7.0.9
# Wed, 18 Aug 2021 21:01:59 GMT
ENV TOMEE_BUILD=plus
# Wed, 18 Aug 2021 21:02:05 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Wed, 18 Aug 2021 21:02:05 GMT
EXPOSE 8080
# Wed, 18 Aug 2021 21:02:06 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:1cfaf5c6f756207bc4607d40ddd440bd2bfa7ab455b2c3015ccf56d85cd1377b`  
		Last Modified: Tue, 17 Aug 2021 01:29:55 GMT  
		Size: 50.4 MB (50436201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4099a935a96edef1e9378de34e314d07fb3aea1b7205774055a1fa44a3819f4`  
		Last Modified: Tue, 17 Aug 2021 09:30:37 GMT  
		Size: 7.8 MB (7833079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e2960d83651b1494b4da6c97686e79cc760aa90a75948eed56786726f86928`  
		Last Modified: Tue, 17 Aug 2021 09:30:38 GMT  
		Size: 10.0 MB (9997209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02210be58959d874de759b34af368e884f52b8ac7643bd3cfaefe6b847bf92dd`  
		Last Modified: Wed, 18 Aug 2021 07:12:01 GMT  
		Size: 5.5 MB (5531118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5e6eb5c7de7d87b3d4bad5c7ac2da2c2943b073dd07ffec22cd79082839eec`  
		Last Modified: Wed, 18 Aug 2021 07:12:57 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa71fb980438da57be6fdbd979262a55138aaab7b0acb4ac8b6b04578854660`  
		Last Modified: Wed, 18 Aug 2021 07:13:01 GMT  
		Size: 41.4 MB (41367106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22b65d65f44a9befc0e14b90d8d92b02546463c854c0ced84d707c164dc5e39`  
		Last Modified: Wed, 18 Aug 2021 21:05:00 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf51b27dd69b75ab79c0f91e0edc4957eda7aa2f51ce1ca1bae1c8d4683bd5e`  
		Last Modified: Wed, 18 Aug 2021 21:05:00 GMT  
		Size: 21.0 KB (21047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03f7343a9c33b7ba0f30921eda95bfb7c01da118e353702693ac46e1733991ae`  
		Last Modified: Wed, 18 Aug 2021 21:05:19 GMT  
		Size: 56.1 MB (56060499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:7.1`

```console
$ docker pull tomee@sha256:1e202f62302770b1cfe8bfc29f38cdde52e17679eac3409e3f5cc761ab3586d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `tomee:7.1` - linux; amd64

```console
$ docker pull tomee@sha256:b8ca8557dc06de3737f9e200dddca3748992c62b25019b18c232fd4cc3431d39
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.7 MB (155706600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8938236c786a5a114e41623631b45a116ee1f54ce54c46f9138c9a8e2f8630`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 17 Aug 2021 01:23:52 GMT
ADD file:b9e6354f7b545096b6cb6072a50de0dffa2232f22d1972a4679f46a7e6394cae in / 
# Tue, 17 Aug 2021 01:23:53 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 09:20:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 09:20:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Aug 2021 07:05:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 18 Aug 2021 07:06:03 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 18 Aug 2021 07:06:04 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 18 Aug 2021 07:06:04 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Aug 2021 07:06:04 GMT
ENV LANG=C.UTF-8
# Wed, 18 Aug 2021 07:06:05 GMT
ENV JAVA_VERSION=8u302
# Wed, 18 Aug 2021 07:06:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_x64_linux_8u302b08.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_aarch64_linux_8u302b08.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Wed, 18 Aug 2021 21:01:37 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Aug 2021 21:01:38 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 18 Aug 2021 21:01:38 GMT
WORKDIR /usr/local/tomee
# Wed, 18 Aug 2021 21:01:38 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Wed, 18 Aug 2021 21:01:49 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Wed, 18 Aug 2021 21:02:17 GMT
ENV TOMEE_VER=7.1.4
# Wed, 18 Aug 2021 21:02:45 GMT
ENV TOMEE_BUILD=webprofile
# Wed, 18 Aug 2021 21:02:50 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Wed, 18 Aug 2021 21:02:51 GMT
EXPOSE 8080
# Wed, 18 Aug 2021 21:02:51 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:1cfaf5c6f756207bc4607d40ddd440bd2bfa7ab455b2c3015ccf56d85cd1377b`  
		Last Modified: Tue, 17 Aug 2021 01:29:55 GMT  
		Size: 50.4 MB (50436201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4099a935a96edef1e9378de34e314d07fb3aea1b7205774055a1fa44a3819f4`  
		Last Modified: Tue, 17 Aug 2021 09:30:37 GMT  
		Size: 7.8 MB (7833079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e2960d83651b1494b4da6c97686e79cc760aa90a75948eed56786726f86928`  
		Last Modified: Tue, 17 Aug 2021 09:30:38 GMT  
		Size: 10.0 MB (9997209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02210be58959d874de759b34af368e884f52b8ac7643bd3cfaefe6b847bf92dd`  
		Last Modified: Wed, 18 Aug 2021 07:12:01 GMT  
		Size: 5.5 MB (5531118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5e6eb5c7de7d87b3d4bad5c7ac2da2c2943b073dd07ffec22cd79082839eec`  
		Last Modified: Wed, 18 Aug 2021 07:12:57 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa71fb980438da57be6fdbd979262a55138aaab7b0acb4ac8b6b04578854660`  
		Last Modified: Wed, 18 Aug 2021 07:13:01 GMT  
		Size: 41.4 MB (41367106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22b65d65f44a9befc0e14b90d8d92b02546463c854c0ced84d707c164dc5e39`  
		Last Modified: Wed, 18 Aug 2021 21:05:00 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf51b27dd69b75ab79c0f91e0edc4957eda7aa2f51ce1ca1bae1c8d4683bd5e`  
		Last Modified: Wed, 18 Aug 2021 21:05:00 GMT  
		Size: 21.0 KB (21047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97c93c5dda9d26265a04b6f1e8170adf46d494ab0b32d4c81735a4e3ddf3f3c5`  
		Last Modified: Wed, 18 Aug 2021 21:06:28 GMT  
		Size: 40.5 MB (40520456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:7.1.4-microprofile`

```console
$ docker pull tomee@sha256:d39f4c61b0611511e60aa6fd45a17e5296634acc218315e9e83692d19e1cf4dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `tomee:7.1.4-microprofile` - linux; amd64

```console
$ docker pull tomee@sha256:dd4d73e9b11f34fecf5f34c15012d7286bc43108925cc25d8115b5e965aab088
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.2 MB (156218675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33ce6895ef87052ff83439fa55041575139eb96a4d2b5bad79da476fc34cd1c2`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 17 Aug 2021 01:23:52 GMT
ADD file:b9e6354f7b545096b6cb6072a50de0dffa2232f22d1972a4679f46a7e6394cae in / 
# Tue, 17 Aug 2021 01:23:53 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 09:20:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 09:20:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Aug 2021 07:05:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 18 Aug 2021 07:06:03 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 18 Aug 2021 07:06:04 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 18 Aug 2021 07:06:04 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Aug 2021 07:06:04 GMT
ENV LANG=C.UTF-8
# Wed, 18 Aug 2021 07:06:05 GMT
ENV JAVA_VERSION=8u302
# Wed, 18 Aug 2021 07:06:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_x64_linux_8u302b08.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_aarch64_linux_8u302b08.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Wed, 18 Aug 2021 21:01:37 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Aug 2021 21:01:38 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 18 Aug 2021 21:01:38 GMT
WORKDIR /usr/local/tomee
# Wed, 18 Aug 2021 21:01:38 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Wed, 18 Aug 2021 21:01:49 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Wed, 18 Aug 2021 21:02:17 GMT
ENV TOMEE_VER=7.1.4
# Wed, 18 Aug 2021 21:02:37 GMT
ENV TOMEE_BUILD=microprofile
# Wed, 18 Aug 2021 21:02:42 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Wed, 18 Aug 2021 21:02:42 GMT
EXPOSE 8080
# Wed, 18 Aug 2021 21:02:42 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:1cfaf5c6f756207bc4607d40ddd440bd2bfa7ab455b2c3015ccf56d85cd1377b`  
		Last Modified: Tue, 17 Aug 2021 01:29:55 GMT  
		Size: 50.4 MB (50436201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4099a935a96edef1e9378de34e314d07fb3aea1b7205774055a1fa44a3819f4`  
		Last Modified: Tue, 17 Aug 2021 09:30:37 GMT  
		Size: 7.8 MB (7833079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e2960d83651b1494b4da6c97686e79cc760aa90a75948eed56786726f86928`  
		Last Modified: Tue, 17 Aug 2021 09:30:38 GMT  
		Size: 10.0 MB (9997209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02210be58959d874de759b34af368e884f52b8ac7643bd3cfaefe6b847bf92dd`  
		Last Modified: Wed, 18 Aug 2021 07:12:01 GMT  
		Size: 5.5 MB (5531118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5e6eb5c7de7d87b3d4bad5c7ac2da2c2943b073dd07ffec22cd79082839eec`  
		Last Modified: Wed, 18 Aug 2021 07:12:57 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa71fb980438da57be6fdbd979262a55138aaab7b0acb4ac8b6b04578854660`  
		Last Modified: Wed, 18 Aug 2021 07:13:01 GMT  
		Size: 41.4 MB (41367106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22b65d65f44a9befc0e14b90d8d92b02546463c854c0ced84d707c164dc5e39`  
		Last Modified: Wed, 18 Aug 2021 21:05:00 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf51b27dd69b75ab79c0f91e0edc4957eda7aa2f51ce1ca1bae1c8d4683bd5e`  
		Last Modified: Wed, 18 Aug 2021 21:05:00 GMT  
		Size: 21.0 KB (21047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:634914726b550e9362e158cb288d158cbb532db7f13eb1d26abd8f041184747d`  
		Last Modified: Wed, 18 Aug 2021 21:06:15 GMT  
		Size: 41.0 MB (41032531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:7.1.4-plume`

```console
$ docker pull tomee@sha256:419910ff5842b910eb31d72aa45aa66696d50322589b532bc24f58bb1db2d7d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `tomee:7.1.4-plume` - linux; amd64

```console
$ docker pull tomee@sha256:16d99668e2b5e23c27b2c6bd77a24d98949466ef9d66ada0a4badae4b4888ffc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.4 MB (180363095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d75820c117713a21e15501847d349328b716d3c425e257a6ec9ab3836814d1c7`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 17 Aug 2021 01:23:52 GMT
ADD file:b9e6354f7b545096b6cb6072a50de0dffa2232f22d1972a4679f46a7e6394cae in / 
# Tue, 17 Aug 2021 01:23:53 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 09:20:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 09:20:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Aug 2021 07:05:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 18 Aug 2021 07:06:03 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 18 Aug 2021 07:06:04 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 18 Aug 2021 07:06:04 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Aug 2021 07:06:04 GMT
ENV LANG=C.UTF-8
# Wed, 18 Aug 2021 07:06:05 GMT
ENV JAVA_VERSION=8u302
# Wed, 18 Aug 2021 07:06:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_x64_linux_8u302b08.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_aarch64_linux_8u302b08.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Wed, 18 Aug 2021 21:01:37 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Aug 2021 21:01:38 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 18 Aug 2021 21:01:38 GMT
WORKDIR /usr/local/tomee
# Wed, 18 Aug 2021 21:01:38 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Wed, 18 Aug 2021 21:01:49 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Wed, 18 Aug 2021 21:02:17 GMT
ENV TOMEE_VER=7.1.4
# Wed, 18 Aug 2021 21:02:17 GMT
ENV TOMEE_BUILD=plume
# Wed, 18 Aug 2021 21:02:24 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Wed, 18 Aug 2021 21:02:24 GMT
EXPOSE 8080
# Wed, 18 Aug 2021 21:02:24 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:1cfaf5c6f756207bc4607d40ddd440bd2bfa7ab455b2c3015ccf56d85cd1377b`  
		Last Modified: Tue, 17 Aug 2021 01:29:55 GMT  
		Size: 50.4 MB (50436201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4099a935a96edef1e9378de34e314d07fb3aea1b7205774055a1fa44a3819f4`  
		Last Modified: Tue, 17 Aug 2021 09:30:37 GMT  
		Size: 7.8 MB (7833079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e2960d83651b1494b4da6c97686e79cc760aa90a75948eed56786726f86928`  
		Last Modified: Tue, 17 Aug 2021 09:30:38 GMT  
		Size: 10.0 MB (9997209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02210be58959d874de759b34af368e884f52b8ac7643bd3cfaefe6b847bf92dd`  
		Last Modified: Wed, 18 Aug 2021 07:12:01 GMT  
		Size: 5.5 MB (5531118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5e6eb5c7de7d87b3d4bad5c7ac2da2c2943b073dd07ffec22cd79082839eec`  
		Last Modified: Wed, 18 Aug 2021 07:12:57 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa71fb980438da57be6fdbd979262a55138aaab7b0acb4ac8b6b04578854660`  
		Last Modified: Wed, 18 Aug 2021 07:13:01 GMT  
		Size: 41.4 MB (41367106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22b65d65f44a9befc0e14b90d8d92b02546463c854c0ced84d707c164dc5e39`  
		Last Modified: Wed, 18 Aug 2021 21:05:00 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf51b27dd69b75ab79c0f91e0edc4957eda7aa2f51ce1ca1bae1c8d4683bd5e`  
		Last Modified: Wed, 18 Aug 2021 21:05:00 GMT  
		Size: 21.0 KB (21047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa56a58011a10f1ecb220a318ccd5824dd226ee3ba5c82d01ac74fa9520dfcb`  
		Last Modified: Wed, 18 Aug 2021 21:05:47 GMT  
		Size: 65.2 MB (65176951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:7.1.4-plus`

```console
$ docker pull tomee@sha256:51a120ee808849fb75beae20dc2c08d7f16818de6ea8743ae141c647c98abd5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `tomee:7.1.4-plus` - linux; amd64

```console
$ docker pull tomee@sha256:7a209e86ab26037e3f6d124a92eb6919c1c1ea72c55fc7b52a126a73bd7f05d1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.3 MB (173328288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08e865023cff79e0b66ad4426a5928f8278857f2564cf85d885fde54cb18f765`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 17 Aug 2021 01:23:52 GMT
ADD file:b9e6354f7b545096b6cb6072a50de0dffa2232f22d1972a4679f46a7e6394cae in / 
# Tue, 17 Aug 2021 01:23:53 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 09:20:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 09:20:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Aug 2021 07:05:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 18 Aug 2021 07:06:03 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 18 Aug 2021 07:06:04 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 18 Aug 2021 07:06:04 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Aug 2021 07:06:04 GMT
ENV LANG=C.UTF-8
# Wed, 18 Aug 2021 07:06:05 GMT
ENV JAVA_VERSION=8u302
# Wed, 18 Aug 2021 07:06:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_x64_linux_8u302b08.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_aarch64_linux_8u302b08.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Wed, 18 Aug 2021 21:01:37 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Aug 2021 21:01:38 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 18 Aug 2021 21:01:38 GMT
WORKDIR /usr/local/tomee
# Wed, 18 Aug 2021 21:01:38 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Wed, 18 Aug 2021 21:01:49 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Wed, 18 Aug 2021 21:02:17 GMT
ENV TOMEE_VER=7.1.4
# Wed, 18 Aug 2021 21:02:27 GMT
ENV TOMEE_BUILD=plus
# Wed, 18 Aug 2021 21:02:33 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Wed, 18 Aug 2021 21:02:34 GMT
EXPOSE 8080
# Wed, 18 Aug 2021 21:02:34 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:1cfaf5c6f756207bc4607d40ddd440bd2bfa7ab455b2c3015ccf56d85cd1377b`  
		Last Modified: Tue, 17 Aug 2021 01:29:55 GMT  
		Size: 50.4 MB (50436201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4099a935a96edef1e9378de34e314d07fb3aea1b7205774055a1fa44a3819f4`  
		Last Modified: Tue, 17 Aug 2021 09:30:37 GMT  
		Size: 7.8 MB (7833079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e2960d83651b1494b4da6c97686e79cc760aa90a75948eed56786726f86928`  
		Last Modified: Tue, 17 Aug 2021 09:30:38 GMT  
		Size: 10.0 MB (9997209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02210be58959d874de759b34af368e884f52b8ac7643bd3cfaefe6b847bf92dd`  
		Last Modified: Wed, 18 Aug 2021 07:12:01 GMT  
		Size: 5.5 MB (5531118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5e6eb5c7de7d87b3d4bad5c7ac2da2c2943b073dd07ffec22cd79082839eec`  
		Last Modified: Wed, 18 Aug 2021 07:12:57 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa71fb980438da57be6fdbd979262a55138aaab7b0acb4ac8b6b04578854660`  
		Last Modified: Wed, 18 Aug 2021 07:13:01 GMT  
		Size: 41.4 MB (41367106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22b65d65f44a9befc0e14b90d8d92b02546463c854c0ced84d707c164dc5e39`  
		Last Modified: Wed, 18 Aug 2021 21:05:00 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf51b27dd69b75ab79c0f91e0edc4957eda7aa2f51ce1ca1bae1c8d4683bd5e`  
		Last Modified: Wed, 18 Aug 2021 21:05:00 GMT  
		Size: 21.0 KB (21047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c8b1026094527f96e0b3573e632ace6788a405b85b55867c0358b4a9e47ccf`  
		Last Modified: Wed, 18 Aug 2021 21:06:02 GMT  
		Size: 58.1 MB (58142144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:7.1.4-webprofile`

```console
$ docker pull tomee@sha256:1e202f62302770b1cfe8bfc29f38cdde52e17679eac3409e3f5cc761ab3586d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `tomee:7.1.4-webprofile` - linux; amd64

```console
$ docker pull tomee@sha256:b8ca8557dc06de3737f9e200dddca3748992c62b25019b18c232fd4cc3431d39
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.7 MB (155706600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8938236c786a5a114e41623631b45a116ee1f54ce54c46f9138c9a8e2f8630`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 17 Aug 2021 01:23:52 GMT
ADD file:b9e6354f7b545096b6cb6072a50de0dffa2232f22d1972a4679f46a7e6394cae in / 
# Tue, 17 Aug 2021 01:23:53 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 09:20:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 09:20:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Aug 2021 07:05:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 18 Aug 2021 07:06:03 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 18 Aug 2021 07:06:04 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 18 Aug 2021 07:06:04 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Aug 2021 07:06:04 GMT
ENV LANG=C.UTF-8
# Wed, 18 Aug 2021 07:06:05 GMT
ENV JAVA_VERSION=8u302
# Wed, 18 Aug 2021 07:06:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_x64_linux_8u302b08.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_aarch64_linux_8u302b08.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Wed, 18 Aug 2021 21:01:37 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Aug 2021 21:01:38 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 18 Aug 2021 21:01:38 GMT
WORKDIR /usr/local/tomee
# Wed, 18 Aug 2021 21:01:38 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Wed, 18 Aug 2021 21:01:49 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Wed, 18 Aug 2021 21:02:17 GMT
ENV TOMEE_VER=7.1.4
# Wed, 18 Aug 2021 21:02:45 GMT
ENV TOMEE_BUILD=webprofile
# Wed, 18 Aug 2021 21:02:50 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Wed, 18 Aug 2021 21:02:51 GMT
EXPOSE 8080
# Wed, 18 Aug 2021 21:02:51 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:1cfaf5c6f756207bc4607d40ddd440bd2bfa7ab455b2c3015ccf56d85cd1377b`  
		Last Modified: Tue, 17 Aug 2021 01:29:55 GMT  
		Size: 50.4 MB (50436201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4099a935a96edef1e9378de34e314d07fb3aea1b7205774055a1fa44a3819f4`  
		Last Modified: Tue, 17 Aug 2021 09:30:37 GMT  
		Size: 7.8 MB (7833079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e2960d83651b1494b4da6c97686e79cc760aa90a75948eed56786726f86928`  
		Last Modified: Tue, 17 Aug 2021 09:30:38 GMT  
		Size: 10.0 MB (9997209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02210be58959d874de759b34af368e884f52b8ac7643bd3cfaefe6b847bf92dd`  
		Last Modified: Wed, 18 Aug 2021 07:12:01 GMT  
		Size: 5.5 MB (5531118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5e6eb5c7de7d87b3d4bad5c7ac2da2c2943b073dd07ffec22cd79082839eec`  
		Last Modified: Wed, 18 Aug 2021 07:12:57 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa71fb980438da57be6fdbd979262a55138aaab7b0acb4ac8b6b04578854660`  
		Last Modified: Wed, 18 Aug 2021 07:13:01 GMT  
		Size: 41.4 MB (41367106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22b65d65f44a9befc0e14b90d8d92b02546463c854c0ced84d707c164dc5e39`  
		Last Modified: Wed, 18 Aug 2021 21:05:00 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf51b27dd69b75ab79c0f91e0edc4957eda7aa2f51ce1ca1bae1c8d4683bd5e`  
		Last Modified: Wed, 18 Aug 2021 21:05:00 GMT  
		Size: 21.0 KB (21047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97c93c5dda9d26265a04b6f1e8170adf46d494ab0b32d4c81735a4e3ddf3f3c5`  
		Last Modified: Wed, 18 Aug 2021 21:06:28 GMT  
		Size: 40.5 MB (40520456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:8`

```console
$ docker pull tomee@sha256:756706fa209e96a1fcfaa6d44902df08d72d1ae98ed33bb7f837770eec6b96b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `tomee:8` - linux; amd64

```console
$ docker pull tomee@sha256:947e86961e6e952a8a1481e597db5e69d068b1487801c477e2777d4dd90458e2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.7 MB (167666075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c351eb6566105c3d7b95afc4d89da3efd5cf37902af3d65a40e82d527679563`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 17 Aug 2021 01:23:52 GMT
ADD file:b9e6354f7b545096b6cb6072a50de0dffa2232f22d1972a4679f46a7e6394cae in / 
# Tue, 17 Aug 2021 01:23:53 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 09:20:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 09:20:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Aug 2021 07:05:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 18 Aug 2021 07:05:20 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Wed, 18 Aug 2021 07:05:21 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 18 Aug 2021 07:05:21 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Aug 2021 07:05:21 GMT
ENV LANG=C.UTF-8
# Wed, 18 Aug 2021 07:05:22 GMT
ENV JAVA_VERSION=11.0.12
# Wed, 18 Aug 2021 07:05:28 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jre_x64_linux_11.0.12_7.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jre_aarch64_linux_11.0.12_7.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Wed, 18 Aug 2021 21:03:33 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Aug 2021 21:03:34 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 18 Aug 2021 21:03:34 GMT
WORKDIR /usr/local/tomee
# Wed, 18 Aug 2021 21:03:35 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Wed, 18 Aug 2021 21:03:41 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Wed, 18 Aug 2021 21:03:42 GMT
ENV TOMEE_VER=8.0.6
# Wed, 18 Aug 2021 21:04:16 GMT
ENV TOMEE_BUILD=webprofile
# Wed, 18 Aug 2021 21:04:21 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm bin/*.exe 	&& rm tomee.tar.gz*
# Wed, 18 Aug 2021 21:04:21 GMT
EXPOSE 8080
# Wed, 18 Aug 2021 21:04:22 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:1cfaf5c6f756207bc4607d40ddd440bd2bfa7ab455b2c3015ccf56d85cd1377b`  
		Last Modified: Tue, 17 Aug 2021 01:29:55 GMT  
		Size: 50.4 MB (50436201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4099a935a96edef1e9378de34e314d07fb3aea1b7205774055a1fa44a3819f4`  
		Last Modified: Tue, 17 Aug 2021 09:30:37 GMT  
		Size: 7.8 MB (7833079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e2960d83651b1494b4da6c97686e79cc760aa90a75948eed56786726f86928`  
		Last Modified: Tue, 17 Aug 2021 09:30:38 GMT  
		Size: 10.0 MB (9997209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02210be58959d874de759b34af368e884f52b8ac7643bd3cfaefe6b847bf92dd`  
		Last Modified: Wed, 18 Aug 2021 07:12:01 GMT  
		Size: 5.5 MB (5531118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99137bab1caf27aee8d1f5f962699a054178b8bc48ef8f5d17648337e8579837`  
		Last Modified: Wed, 18 Aug 2021 07:12:00 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38621337f17c0f871f3675b78bd321096624cd617666be70bc9a259788e93041`  
		Last Modified: Wed, 18 Aug 2021 07:12:07 GMT  
		Size: 46.9 MB (46863974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0238d73f652115c041086e00940b503df0976e22ba3f9f5b2a8d9a7b609d7173`  
		Last Modified: Wed, 18 Aug 2021 21:07:31 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abea88b63ce675e6fd5e791cdca5a2a54dd1baa53825c2c8f5bdc7cc0b073134`  
		Last Modified: Wed, 18 Aug 2021 21:07:31 GMT  
		Size: 21.0 KB (21021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7bd68da3315025fb523b0d63d54be4e8fb29ee0ffe220f66e4925b760ff3b19`  
		Last Modified: Wed, 18 Aug 2021 21:08:18 GMT  
		Size: 47.0 MB (46983089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:8-jre-7.0.9-plume`

```console
$ docker pull tomee@sha256:400a42d3b5bf887176e3953c6d2364ce9916b4e92c88a585fd92df897a5b82f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `tomee:8-jre-7.0.9-plume` - linux; amd64

```console
$ docker pull tomee@sha256:473c41a8bde6e542dc29dc4a218bc9da122118cfd59be673ee8fa82e688043c1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.3 MB (178318592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a7dc755cc16f8f47e9fc9129580433815211a865a6c6f391d451e8eb558dc58`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 17 Aug 2021 01:23:52 GMT
ADD file:b9e6354f7b545096b6cb6072a50de0dffa2232f22d1972a4679f46a7e6394cae in / 
# Tue, 17 Aug 2021 01:23:53 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 09:20:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 09:20:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Aug 2021 07:05:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 18 Aug 2021 07:06:03 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 18 Aug 2021 07:06:04 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 18 Aug 2021 07:06:04 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Aug 2021 07:06:04 GMT
ENV LANG=C.UTF-8
# Wed, 18 Aug 2021 07:06:05 GMT
ENV JAVA_VERSION=8u302
# Wed, 18 Aug 2021 07:06:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_x64_linux_8u302b08.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_aarch64_linux_8u302b08.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Wed, 18 Aug 2021 21:01:37 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Aug 2021 21:01:38 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 18 Aug 2021 21:01:38 GMT
WORKDIR /usr/local/tomee
# Wed, 18 Aug 2021 21:01:38 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Wed, 18 Aug 2021 21:01:49 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Wed, 18 Aug 2021 21:01:49 GMT
ENV TOMEE_VER=7.0.9
# Wed, 18 Aug 2021 21:01:49 GMT
ENV TOMEE_BUILD=plume
# Wed, 18 Aug 2021 21:01:56 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Wed, 18 Aug 2021 21:01:56 GMT
EXPOSE 8080
# Wed, 18 Aug 2021 21:01:56 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:1cfaf5c6f756207bc4607d40ddd440bd2bfa7ab455b2c3015ccf56d85cd1377b`  
		Last Modified: Tue, 17 Aug 2021 01:29:55 GMT  
		Size: 50.4 MB (50436201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4099a935a96edef1e9378de34e314d07fb3aea1b7205774055a1fa44a3819f4`  
		Last Modified: Tue, 17 Aug 2021 09:30:37 GMT  
		Size: 7.8 MB (7833079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e2960d83651b1494b4da6c97686e79cc760aa90a75948eed56786726f86928`  
		Last Modified: Tue, 17 Aug 2021 09:30:38 GMT  
		Size: 10.0 MB (9997209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02210be58959d874de759b34af368e884f52b8ac7643bd3cfaefe6b847bf92dd`  
		Last Modified: Wed, 18 Aug 2021 07:12:01 GMT  
		Size: 5.5 MB (5531118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5e6eb5c7de7d87b3d4bad5c7ac2da2c2943b073dd07ffec22cd79082839eec`  
		Last Modified: Wed, 18 Aug 2021 07:12:57 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa71fb980438da57be6fdbd979262a55138aaab7b0acb4ac8b6b04578854660`  
		Last Modified: Wed, 18 Aug 2021 07:13:01 GMT  
		Size: 41.4 MB (41367106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22b65d65f44a9befc0e14b90d8d92b02546463c854c0ced84d707c164dc5e39`  
		Last Modified: Wed, 18 Aug 2021 21:05:00 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf51b27dd69b75ab79c0f91e0edc4957eda7aa2f51ce1ca1bae1c8d4683bd5e`  
		Last Modified: Wed, 18 Aug 2021 21:05:00 GMT  
		Size: 21.0 KB (21047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aaba43d0e2b04a695df01f8c37c39454f6a3877eceac3eb2edfc63740767112`  
		Last Modified: Wed, 18 Aug 2021 21:05:05 GMT  
		Size: 63.1 MB (63132448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:8-jre-7.0.9-plus`

```console
$ docker pull tomee@sha256:d9deff0350b1ad7eaf33f28262e4486683bf594ba17dbdbab58900f6cba51517
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `tomee:8-jre-7.0.9-plus` - linux; amd64

```console
$ docker pull tomee@sha256:9cc2ea48e81d74b4e544f91145a5380768d89c025191147a7c3c0e1e5b41167f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.2 MB (171246643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad1c15025cd29c02c278456d8d9d23cc4adc22e079be1118530892e851f93713`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 17 Aug 2021 01:23:52 GMT
ADD file:b9e6354f7b545096b6cb6072a50de0dffa2232f22d1972a4679f46a7e6394cae in / 
# Tue, 17 Aug 2021 01:23:53 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 09:20:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 09:20:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Aug 2021 07:05:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 18 Aug 2021 07:06:03 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 18 Aug 2021 07:06:04 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 18 Aug 2021 07:06:04 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Aug 2021 07:06:04 GMT
ENV LANG=C.UTF-8
# Wed, 18 Aug 2021 07:06:05 GMT
ENV JAVA_VERSION=8u302
# Wed, 18 Aug 2021 07:06:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_x64_linux_8u302b08.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_aarch64_linux_8u302b08.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Wed, 18 Aug 2021 21:01:37 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Aug 2021 21:01:38 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 18 Aug 2021 21:01:38 GMT
WORKDIR /usr/local/tomee
# Wed, 18 Aug 2021 21:01:38 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Wed, 18 Aug 2021 21:01:49 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Wed, 18 Aug 2021 21:01:49 GMT
ENV TOMEE_VER=7.0.9
# Wed, 18 Aug 2021 21:01:59 GMT
ENV TOMEE_BUILD=plus
# Wed, 18 Aug 2021 21:02:05 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Wed, 18 Aug 2021 21:02:05 GMT
EXPOSE 8080
# Wed, 18 Aug 2021 21:02:06 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:1cfaf5c6f756207bc4607d40ddd440bd2bfa7ab455b2c3015ccf56d85cd1377b`  
		Last Modified: Tue, 17 Aug 2021 01:29:55 GMT  
		Size: 50.4 MB (50436201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4099a935a96edef1e9378de34e314d07fb3aea1b7205774055a1fa44a3819f4`  
		Last Modified: Tue, 17 Aug 2021 09:30:37 GMT  
		Size: 7.8 MB (7833079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e2960d83651b1494b4da6c97686e79cc760aa90a75948eed56786726f86928`  
		Last Modified: Tue, 17 Aug 2021 09:30:38 GMT  
		Size: 10.0 MB (9997209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02210be58959d874de759b34af368e884f52b8ac7643bd3cfaefe6b847bf92dd`  
		Last Modified: Wed, 18 Aug 2021 07:12:01 GMT  
		Size: 5.5 MB (5531118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5e6eb5c7de7d87b3d4bad5c7ac2da2c2943b073dd07ffec22cd79082839eec`  
		Last Modified: Wed, 18 Aug 2021 07:12:57 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa71fb980438da57be6fdbd979262a55138aaab7b0acb4ac8b6b04578854660`  
		Last Modified: Wed, 18 Aug 2021 07:13:01 GMT  
		Size: 41.4 MB (41367106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22b65d65f44a9befc0e14b90d8d92b02546463c854c0ced84d707c164dc5e39`  
		Last Modified: Wed, 18 Aug 2021 21:05:00 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf51b27dd69b75ab79c0f91e0edc4957eda7aa2f51ce1ca1bae1c8d4683bd5e`  
		Last Modified: Wed, 18 Aug 2021 21:05:00 GMT  
		Size: 21.0 KB (21047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03f7343a9c33b7ba0f30921eda95bfb7c01da118e353702693ac46e1733991ae`  
		Last Modified: Wed, 18 Aug 2021 21:05:19 GMT  
		Size: 56.1 MB (56060499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:8-jre-7.0.9-webprofile`

```console
$ docker pull tomee@sha256:2bd542f939693d3812b9942b1625236121b6e4a631aaa003c3c11bc18bb98853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `tomee:8-jre-7.0.9-webprofile` - linux; amd64

```console
$ docker pull tomee@sha256:12675c26a4fb8bfe773056123cb250996c5c680584cfbfdd4a3d6c8662edcfb4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.6 MB (153592617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c92eabfce57332c0bd646ac24137cbf58b05c707b546e2111515c15dc44a8e`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 17 Aug 2021 01:23:52 GMT
ADD file:b9e6354f7b545096b6cb6072a50de0dffa2232f22d1972a4679f46a7e6394cae in / 
# Tue, 17 Aug 2021 01:23:53 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 09:20:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 09:20:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Aug 2021 07:05:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 18 Aug 2021 07:06:03 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 18 Aug 2021 07:06:04 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 18 Aug 2021 07:06:04 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Aug 2021 07:06:04 GMT
ENV LANG=C.UTF-8
# Wed, 18 Aug 2021 07:06:05 GMT
ENV JAVA_VERSION=8u302
# Wed, 18 Aug 2021 07:06:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_x64_linux_8u302b08.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_aarch64_linux_8u302b08.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Wed, 18 Aug 2021 21:01:37 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Aug 2021 21:01:38 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 18 Aug 2021 21:01:38 GMT
WORKDIR /usr/local/tomee
# Wed, 18 Aug 2021 21:01:38 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Wed, 18 Aug 2021 21:01:49 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Wed, 18 Aug 2021 21:01:49 GMT
ENV TOMEE_VER=7.0.9
# Wed, 18 Aug 2021 21:02:09 GMT
ENV TOMEE_BUILD=webprofile
# Wed, 18 Aug 2021 21:02:13 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Wed, 18 Aug 2021 21:02:14 GMT
EXPOSE 8080
# Wed, 18 Aug 2021 21:02:14 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:1cfaf5c6f756207bc4607d40ddd440bd2bfa7ab455b2c3015ccf56d85cd1377b`  
		Last Modified: Tue, 17 Aug 2021 01:29:55 GMT  
		Size: 50.4 MB (50436201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4099a935a96edef1e9378de34e314d07fb3aea1b7205774055a1fa44a3819f4`  
		Last Modified: Tue, 17 Aug 2021 09:30:37 GMT  
		Size: 7.8 MB (7833079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e2960d83651b1494b4da6c97686e79cc760aa90a75948eed56786726f86928`  
		Last Modified: Tue, 17 Aug 2021 09:30:38 GMT  
		Size: 10.0 MB (9997209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02210be58959d874de759b34af368e884f52b8ac7643bd3cfaefe6b847bf92dd`  
		Last Modified: Wed, 18 Aug 2021 07:12:01 GMT  
		Size: 5.5 MB (5531118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5e6eb5c7de7d87b3d4bad5c7ac2da2c2943b073dd07ffec22cd79082839eec`  
		Last Modified: Wed, 18 Aug 2021 07:12:57 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa71fb980438da57be6fdbd979262a55138aaab7b0acb4ac8b6b04578854660`  
		Last Modified: Wed, 18 Aug 2021 07:13:01 GMT  
		Size: 41.4 MB (41367106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22b65d65f44a9befc0e14b90d8d92b02546463c854c0ced84d707c164dc5e39`  
		Last Modified: Wed, 18 Aug 2021 21:05:00 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf51b27dd69b75ab79c0f91e0edc4957eda7aa2f51ce1ca1bae1c8d4683bd5e`  
		Last Modified: Wed, 18 Aug 2021 21:05:00 GMT  
		Size: 21.0 KB (21047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14d0f1db2a8b22eefa91988cba85c83f8d5fb86dc6734429ee9f3afe1396f328`  
		Last Modified: Wed, 18 Aug 2021 21:05:32 GMT  
		Size: 38.4 MB (38406473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:8-jre-7.1.4-microprofile`

```console
$ docker pull tomee@sha256:d39f4c61b0611511e60aa6fd45a17e5296634acc218315e9e83692d19e1cf4dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `tomee:8-jre-7.1.4-microprofile` - linux; amd64

```console
$ docker pull tomee@sha256:dd4d73e9b11f34fecf5f34c15012d7286bc43108925cc25d8115b5e965aab088
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.2 MB (156218675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33ce6895ef87052ff83439fa55041575139eb96a4d2b5bad79da476fc34cd1c2`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 17 Aug 2021 01:23:52 GMT
ADD file:b9e6354f7b545096b6cb6072a50de0dffa2232f22d1972a4679f46a7e6394cae in / 
# Tue, 17 Aug 2021 01:23:53 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 09:20:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 09:20:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Aug 2021 07:05:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 18 Aug 2021 07:06:03 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 18 Aug 2021 07:06:04 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 18 Aug 2021 07:06:04 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Aug 2021 07:06:04 GMT
ENV LANG=C.UTF-8
# Wed, 18 Aug 2021 07:06:05 GMT
ENV JAVA_VERSION=8u302
# Wed, 18 Aug 2021 07:06:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_x64_linux_8u302b08.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_aarch64_linux_8u302b08.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Wed, 18 Aug 2021 21:01:37 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Aug 2021 21:01:38 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 18 Aug 2021 21:01:38 GMT
WORKDIR /usr/local/tomee
# Wed, 18 Aug 2021 21:01:38 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Wed, 18 Aug 2021 21:01:49 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Wed, 18 Aug 2021 21:02:17 GMT
ENV TOMEE_VER=7.1.4
# Wed, 18 Aug 2021 21:02:37 GMT
ENV TOMEE_BUILD=microprofile
# Wed, 18 Aug 2021 21:02:42 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Wed, 18 Aug 2021 21:02:42 GMT
EXPOSE 8080
# Wed, 18 Aug 2021 21:02:42 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:1cfaf5c6f756207bc4607d40ddd440bd2bfa7ab455b2c3015ccf56d85cd1377b`  
		Last Modified: Tue, 17 Aug 2021 01:29:55 GMT  
		Size: 50.4 MB (50436201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4099a935a96edef1e9378de34e314d07fb3aea1b7205774055a1fa44a3819f4`  
		Last Modified: Tue, 17 Aug 2021 09:30:37 GMT  
		Size: 7.8 MB (7833079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e2960d83651b1494b4da6c97686e79cc760aa90a75948eed56786726f86928`  
		Last Modified: Tue, 17 Aug 2021 09:30:38 GMT  
		Size: 10.0 MB (9997209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02210be58959d874de759b34af368e884f52b8ac7643bd3cfaefe6b847bf92dd`  
		Last Modified: Wed, 18 Aug 2021 07:12:01 GMT  
		Size: 5.5 MB (5531118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5e6eb5c7de7d87b3d4bad5c7ac2da2c2943b073dd07ffec22cd79082839eec`  
		Last Modified: Wed, 18 Aug 2021 07:12:57 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa71fb980438da57be6fdbd979262a55138aaab7b0acb4ac8b6b04578854660`  
		Last Modified: Wed, 18 Aug 2021 07:13:01 GMT  
		Size: 41.4 MB (41367106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22b65d65f44a9befc0e14b90d8d92b02546463c854c0ced84d707c164dc5e39`  
		Last Modified: Wed, 18 Aug 2021 21:05:00 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf51b27dd69b75ab79c0f91e0edc4957eda7aa2f51ce1ca1bae1c8d4683bd5e`  
		Last Modified: Wed, 18 Aug 2021 21:05:00 GMT  
		Size: 21.0 KB (21047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:634914726b550e9362e158cb288d158cbb532db7f13eb1d26abd8f041184747d`  
		Last Modified: Wed, 18 Aug 2021 21:06:15 GMT  
		Size: 41.0 MB (41032531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:8-jre-7.1.4-plume`

```console
$ docker pull tomee@sha256:419910ff5842b910eb31d72aa45aa66696d50322589b532bc24f58bb1db2d7d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `tomee:8-jre-7.1.4-plume` - linux; amd64

```console
$ docker pull tomee@sha256:16d99668e2b5e23c27b2c6bd77a24d98949466ef9d66ada0a4badae4b4888ffc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.4 MB (180363095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d75820c117713a21e15501847d349328b716d3c425e257a6ec9ab3836814d1c7`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 17 Aug 2021 01:23:52 GMT
ADD file:b9e6354f7b545096b6cb6072a50de0dffa2232f22d1972a4679f46a7e6394cae in / 
# Tue, 17 Aug 2021 01:23:53 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 09:20:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 09:20:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Aug 2021 07:05:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 18 Aug 2021 07:06:03 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 18 Aug 2021 07:06:04 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 18 Aug 2021 07:06:04 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Aug 2021 07:06:04 GMT
ENV LANG=C.UTF-8
# Wed, 18 Aug 2021 07:06:05 GMT
ENV JAVA_VERSION=8u302
# Wed, 18 Aug 2021 07:06:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_x64_linux_8u302b08.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_aarch64_linux_8u302b08.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Wed, 18 Aug 2021 21:01:37 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Aug 2021 21:01:38 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 18 Aug 2021 21:01:38 GMT
WORKDIR /usr/local/tomee
# Wed, 18 Aug 2021 21:01:38 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Wed, 18 Aug 2021 21:01:49 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Wed, 18 Aug 2021 21:02:17 GMT
ENV TOMEE_VER=7.1.4
# Wed, 18 Aug 2021 21:02:17 GMT
ENV TOMEE_BUILD=plume
# Wed, 18 Aug 2021 21:02:24 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Wed, 18 Aug 2021 21:02:24 GMT
EXPOSE 8080
# Wed, 18 Aug 2021 21:02:24 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:1cfaf5c6f756207bc4607d40ddd440bd2bfa7ab455b2c3015ccf56d85cd1377b`  
		Last Modified: Tue, 17 Aug 2021 01:29:55 GMT  
		Size: 50.4 MB (50436201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4099a935a96edef1e9378de34e314d07fb3aea1b7205774055a1fa44a3819f4`  
		Last Modified: Tue, 17 Aug 2021 09:30:37 GMT  
		Size: 7.8 MB (7833079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e2960d83651b1494b4da6c97686e79cc760aa90a75948eed56786726f86928`  
		Last Modified: Tue, 17 Aug 2021 09:30:38 GMT  
		Size: 10.0 MB (9997209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02210be58959d874de759b34af368e884f52b8ac7643bd3cfaefe6b847bf92dd`  
		Last Modified: Wed, 18 Aug 2021 07:12:01 GMT  
		Size: 5.5 MB (5531118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5e6eb5c7de7d87b3d4bad5c7ac2da2c2943b073dd07ffec22cd79082839eec`  
		Last Modified: Wed, 18 Aug 2021 07:12:57 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa71fb980438da57be6fdbd979262a55138aaab7b0acb4ac8b6b04578854660`  
		Last Modified: Wed, 18 Aug 2021 07:13:01 GMT  
		Size: 41.4 MB (41367106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22b65d65f44a9befc0e14b90d8d92b02546463c854c0ced84d707c164dc5e39`  
		Last Modified: Wed, 18 Aug 2021 21:05:00 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf51b27dd69b75ab79c0f91e0edc4957eda7aa2f51ce1ca1bae1c8d4683bd5e`  
		Last Modified: Wed, 18 Aug 2021 21:05:00 GMT  
		Size: 21.0 KB (21047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa56a58011a10f1ecb220a318ccd5824dd226ee3ba5c82d01ac74fa9520dfcb`  
		Last Modified: Wed, 18 Aug 2021 21:05:47 GMT  
		Size: 65.2 MB (65176951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:8-jre-7.1.4-plus`

```console
$ docker pull tomee@sha256:51a120ee808849fb75beae20dc2c08d7f16818de6ea8743ae141c647c98abd5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `tomee:8-jre-7.1.4-plus` - linux; amd64

```console
$ docker pull tomee@sha256:7a209e86ab26037e3f6d124a92eb6919c1c1ea72c55fc7b52a126a73bd7f05d1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.3 MB (173328288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08e865023cff79e0b66ad4426a5928f8278857f2564cf85d885fde54cb18f765`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 17 Aug 2021 01:23:52 GMT
ADD file:b9e6354f7b545096b6cb6072a50de0dffa2232f22d1972a4679f46a7e6394cae in / 
# Tue, 17 Aug 2021 01:23:53 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 09:20:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 09:20:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Aug 2021 07:05:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 18 Aug 2021 07:06:03 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 18 Aug 2021 07:06:04 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 18 Aug 2021 07:06:04 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Aug 2021 07:06:04 GMT
ENV LANG=C.UTF-8
# Wed, 18 Aug 2021 07:06:05 GMT
ENV JAVA_VERSION=8u302
# Wed, 18 Aug 2021 07:06:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_x64_linux_8u302b08.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_aarch64_linux_8u302b08.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Wed, 18 Aug 2021 21:01:37 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Aug 2021 21:01:38 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 18 Aug 2021 21:01:38 GMT
WORKDIR /usr/local/tomee
# Wed, 18 Aug 2021 21:01:38 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Wed, 18 Aug 2021 21:01:49 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Wed, 18 Aug 2021 21:02:17 GMT
ENV TOMEE_VER=7.1.4
# Wed, 18 Aug 2021 21:02:27 GMT
ENV TOMEE_BUILD=plus
# Wed, 18 Aug 2021 21:02:33 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Wed, 18 Aug 2021 21:02:34 GMT
EXPOSE 8080
# Wed, 18 Aug 2021 21:02:34 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:1cfaf5c6f756207bc4607d40ddd440bd2bfa7ab455b2c3015ccf56d85cd1377b`  
		Last Modified: Tue, 17 Aug 2021 01:29:55 GMT  
		Size: 50.4 MB (50436201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4099a935a96edef1e9378de34e314d07fb3aea1b7205774055a1fa44a3819f4`  
		Last Modified: Tue, 17 Aug 2021 09:30:37 GMT  
		Size: 7.8 MB (7833079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e2960d83651b1494b4da6c97686e79cc760aa90a75948eed56786726f86928`  
		Last Modified: Tue, 17 Aug 2021 09:30:38 GMT  
		Size: 10.0 MB (9997209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02210be58959d874de759b34af368e884f52b8ac7643bd3cfaefe6b847bf92dd`  
		Last Modified: Wed, 18 Aug 2021 07:12:01 GMT  
		Size: 5.5 MB (5531118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5e6eb5c7de7d87b3d4bad5c7ac2da2c2943b073dd07ffec22cd79082839eec`  
		Last Modified: Wed, 18 Aug 2021 07:12:57 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa71fb980438da57be6fdbd979262a55138aaab7b0acb4ac8b6b04578854660`  
		Last Modified: Wed, 18 Aug 2021 07:13:01 GMT  
		Size: 41.4 MB (41367106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22b65d65f44a9befc0e14b90d8d92b02546463c854c0ced84d707c164dc5e39`  
		Last Modified: Wed, 18 Aug 2021 21:05:00 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf51b27dd69b75ab79c0f91e0edc4957eda7aa2f51ce1ca1bae1c8d4683bd5e`  
		Last Modified: Wed, 18 Aug 2021 21:05:00 GMT  
		Size: 21.0 KB (21047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c8b1026094527f96e0b3573e632ace6788a405b85b55867c0358b4a9e47ccf`  
		Last Modified: Wed, 18 Aug 2021 21:06:02 GMT  
		Size: 58.1 MB (58142144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:8-jre-7.1.4-webprofile`

```console
$ docker pull tomee@sha256:1e202f62302770b1cfe8bfc29f38cdde52e17679eac3409e3f5cc761ab3586d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `tomee:8-jre-7.1.4-webprofile` - linux; amd64

```console
$ docker pull tomee@sha256:b8ca8557dc06de3737f9e200dddca3748992c62b25019b18c232fd4cc3431d39
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.7 MB (155706600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8938236c786a5a114e41623631b45a116ee1f54ce54c46f9138c9a8e2f8630`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 17 Aug 2021 01:23:52 GMT
ADD file:b9e6354f7b545096b6cb6072a50de0dffa2232f22d1972a4679f46a7e6394cae in / 
# Tue, 17 Aug 2021 01:23:53 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 09:20:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 09:20:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Aug 2021 07:05:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 18 Aug 2021 07:06:03 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 18 Aug 2021 07:06:04 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 18 Aug 2021 07:06:04 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Aug 2021 07:06:04 GMT
ENV LANG=C.UTF-8
# Wed, 18 Aug 2021 07:06:05 GMT
ENV JAVA_VERSION=8u302
# Wed, 18 Aug 2021 07:06:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_x64_linux_8u302b08.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_aarch64_linux_8u302b08.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Wed, 18 Aug 2021 21:01:37 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Aug 2021 21:01:38 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 18 Aug 2021 21:01:38 GMT
WORKDIR /usr/local/tomee
# Wed, 18 Aug 2021 21:01:38 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Wed, 18 Aug 2021 21:01:49 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Wed, 18 Aug 2021 21:02:17 GMT
ENV TOMEE_VER=7.1.4
# Wed, 18 Aug 2021 21:02:45 GMT
ENV TOMEE_BUILD=webprofile
# Wed, 18 Aug 2021 21:02:50 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Wed, 18 Aug 2021 21:02:51 GMT
EXPOSE 8080
# Wed, 18 Aug 2021 21:02:51 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:1cfaf5c6f756207bc4607d40ddd440bd2bfa7ab455b2c3015ccf56d85cd1377b`  
		Last Modified: Tue, 17 Aug 2021 01:29:55 GMT  
		Size: 50.4 MB (50436201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4099a935a96edef1e9378de34e314d07fb3aea1b7205774055a1fa44a3819f4`  
		Last Modified: Tue, 17 Aug 2021 09:30:37 GMT  
		Size: 7.8 MB (7833079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e2960d83651b1494b4da6c97686e79cc760aa90a75948eed56786726f86928`  
		Last Modified: Tue, 17 Aug 2021 09:30:38 GMT  
		Size: 10.0 MB (9997209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02210be58959d874de759b34af368e884f52b8ac7643bd3cfaefe6b847bf92dd`  
		Last Modified: Wed, 18 Aug 2021 07:12:01 GMT  
		Size: 5.5 MB (5531118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5e6eb5c7de7d87b3d4bad5c7ac2da2c2943b073dd07ffec22cd79082839eec`  
		Last Modified: Wed, 18 Aug 2021 07:12:57 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa71fb980438da57be6fdbd979262a55138aaab7b0acb4ac8b6b04578854660`  
		Last Modified: Wed, 18 Aug 2021 07:13:01 GMT  
		Size: 41.4 MB (41367106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22b65d65f44a9befc0e14b90d8d92b02546463c854c0ced84d707c164dc5e39`  
		Last Modified: Wed, 18 Aug 2021 21:05:00 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf51b27dd69b75ab79c0f91e0edc4957eda7aa2f51ce1ca1bae1c8d4683bd5e`  
		Last Modified: Wed, 18 Aug 2021 21:05:00 GMT  
		Size: 21.0 KB (21047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97c93c5dda9d26265a04b6f1e8170adf46d494ab0b32d4c81735a4e3ddf3f3c5`  
		Last Modified: Wed, 18 Aug 2021 21:06:28 GMT  
		Size: 40.5 MB (40520456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:8-jre-8.0.6-microprofile`

```console
$ docker pull tomee@sha256:eecb825bc34e861bfe71749a39c284062b1404739f1a2068c5e15ace0c02acb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `tomee:8-jre-8.0.6-microprofile` - linux; amd64

```console
$ docker pull tomee@sha256:adbd0645332133a062b224ba3f971563511b496b3b24433eac91c840e1ed4d94
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.6 MB (177631107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c593c2cf2d310fa31fac5edf1218f4b102d73b4a5472c81ce553674ff4334ab`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 17 Aug 2021 01:23:52 GMT
ADD file:b9e6354f7b545096b6cb6072a50de0dffa2232f22d1972a4679f46a7e6394cae in / 
# Tue, 17 Aug 2021 01:23:53 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 09:20:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 09:20:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Aug 2021 07:05:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 18 Aug 2021 07:06:03 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 18 Aug 2021 07:06:04 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 18 Aug 2021 07:06:04 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Aug 2021 07:06:04 GMT
ENV LANG=C.UTF-8
# Wed, 18 Aug 2021 07:06:05 GMT
ENV JAVA_VERSION=8u302
# Wed, 18 Aug 2021 07:06:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_x64_linux_8u302b08.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_aarch64_linux_8u302b08.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Wed, 18 Aug 2021 21:01:37 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Aug 2021 21:01:38 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 18 Aug 2021 21:01:38 GMT
WORKDIR /usr/local/tomee
# Wed, 18 Aug 2021 21:01:38 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Wed, 18 Aug 2021 21:01:49 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Wed, 18 Aug 2021 21:02:54 GMT
ENV TOMEE_VER=8.0.6
# Wed, 18 Aug 2021 21:03:15 GMT
ENV TOMEE_BUILD=microprofile
# Wed, 18 Aug 2021 21:03:22 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm bin/*.exe 	&& rm tomee.tar.gz*
# Wed, 18 Aug 2021 21:03:22 GMT
EXPOSE 8080
# Wed, 18 Aug 2021 21:03:22 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:1cfaf5c6f756207bc4607d40ddd440bd2bfa7ab455b2c3015ccf56d85cd1377b`  
		Last Modified: Tue, 17 Aug 2021 01:29:55 GMT  
		Size: 50.4 MB (50436201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4099a935a96edef1e9378de34e314d07fb3aea1b7205774055a1fa44a3819f4`  
		Last Modified: Tue, 17 Aug 2021 09:30:37 GMT  
		Size: 7.8 MB (7833079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e2960d83651b1494b4da6c97686e79cc760aa90a75948eed56786726f86928`  
		Last Modified: Tue, 17 Aug 2021 09:30:38 GMT  
		Size: 10.0 MB (9997209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02210be58959d874de759b34af368e884f52b8ac7643bd3cfaefe6b847bf92dd`  
		Last Modified: Wed, 18 Aug 2021 07:12:01 GMT  
		Size: 5.5 MB (5531118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5e6eb5c7de7d87b3d4bad5c7ac2da2c2943b073dd07ffec22cd79082839eec`  
		Last Modified: Wed, 18 Aug 2021 07:12:57 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa71fb980438da57be6fdbd979262a55138aaab7b0acb4ac8b6b04578854660`  
		Last Modified: Wed, 18 Aug 2021 07:13:01 GMT  
		Size: 41.4 MB (41367106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22b65d65f44a9befc0e14b90d8d92b02546463c854c0ced84d707c164dc5e39`  
		Last Modified: Wed, 18 Aug 2021 21:05:00 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf51b27dd69b75ab79c0f91e0edc4957eda7aa2f51ce1ca1bae1c8d4683bd5e`  
		Last Modified: Wed, 18 Aug 2021 21:05:00 GMT  
		Size: 21.0 KB (21047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff1d350de64674a1117c87ecaa5114128017aee0103daffd9951017bc1a2559c`  
		Last Modified: Wed, 18 Aug 2021 21:07:12 GMT  
		Size: 62.4 MB (62444963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:8-jre-8.0.6-plume`

```console
$ docker pull tomee@sha256:dbdbce7e31716bd837fcb56a3963d6c8cc89f81b132ebd6862f7e854f30c74c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `tomee:8-jre-8.0.6-plume` - linux; amd64

```console
$ docker pull tomee@sha256:fe3c44c38acae03a46f9ed3db516e01b839168ebac628f3e91f215977cf6c234
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.8 MB (189806242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93f4562eadba8d9604747a46b95ea7711f47b39b19de30a81e74f18744aacfb7`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 17 Aug 2021 01:23:52 GMT
ADD file:b9e6354f7b545096b6cb6072a50de0dffa2232f22d1972a4679f46a7e6394cae in / 
# Tue, 17 Aug 2021 01:23:53 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 09:20:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 09:20:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Aug 2021 07:05:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 18 Aug 2021 07:06:03 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 18 Aug 2021 07:06:04 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 18 Aug 2021 07:06:04 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Aug 2021 07:06:04 GMT
ENV LANG=C.UTF-8
# Wed, 18 Aug 2021 07:06:05 GMT
ENV JAVA_VERSION=8u302
# Wed, 18 Aug 2021 07:06:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_x64_linux_8u302b08.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_aarch64_linux_8u302b08.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Wed, 18 Aug 2021 21:01:37 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Aug 2021 21:01:38 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 18 Aug 2021 21:01:38 GMT
WORKDIR /usr/local/tomee
# Wed, 18 Aug 2021 21:01:38 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Wed, 18 Aug 2021 21:01:49 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Wed, 18 Aug 2021 21:02:54 GMT
ENV TOMEE_VER=8.0.6
# Wed, 18 Aug 2021 21:02:54 GMT
ENV TOMEE_BUILD=plume
# Wed, 18 Aug 2021 21:03:02 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm bin/*.exe 	&& rm tomee.tar.gz*
# Wed, 18 Aug 2021 21:03:02 GMT
EXPOSE 8080
# Wed, 18 Aug 2021 21:03:02 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:1cfaf5c6f756207bc4607d40ddd440bd2bfa7ab455b2c3015ccf56d85cd1377b`  
		Last Modified: Tue, 17 Aug 2021 01:29:55 GMT  
		Size: 50.4 MB (50436201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4099a935a96edef1e9378de34e314d07fb3aea1b7205774055a1fa44a3819f4`  
		Last Modified: Tue, 17 Aug 2021 09:30:37 GMT  
		Size: 7.8 MB (7833079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e2960d83651b1494b4da6c97686e79cc760aa90a75948eed56786726f86928`  
		Last Modified: Tue, 17 Aug 2021 09:30:38 GMT  
		Size: 10.0 MB (9997209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02210be58959d874de759b34af368e884f52b8ac7643bd3cfaefe6b847bf92dd`  
		Last Modified: Wed, 18 Aug 2021 07:12:01 GMT  
		Size: 5.5 MB (5531118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5e6eb5c7de7d87b3d4bad5c7ac2da2c2943b073dd07ffec22cd79082839eec`  
		Last Modified: Wed, 18 Aug 2021 07:12:57 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa71fb980438da57be6fdbd979262a55138aaab7b0acb4ac8b6b04578854660`  
		Last Modified: Wed, 18 Aug 2021 07:13:01 GMT  
		Size: 41.4 MB (41367106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22b65d65f44a9befc0e14b90d8d92b02546463c854c0ced84d707c164dc5e39`  
		Last Modified: Wed, 18 Aug 2021 21:05:00 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf51b27dd69b75ab79c0f91e0edc4957eda7aa2f51ce1ca1bae1c8d4683bd5e`  
		Last Modified: Wed, 18 Aug 2021 21:05:00 GMT  
		Size: 21.0 KB (21047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7db5b15ee7e0d51fb2db7e9301f80037b602edab3985533ec6e14f343dd2b200`  
		Last Modified: Wed, 18 Aug 2021 21:06:48 GMT  
		Size: 74.6 MB (74620098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:8-jre-8.0.6-plus`

```console
$ docker pull tomee@sha256:9d411b30774d3fecdc861456013f45550fd792fb36eaed9e034dad809c89ac26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `tomee:8-jre-8.0.6-plus` - linux; amd64

```console
$ docker pull tomee@sha256:a579efa9c71de656d51446725e68fef8f23376954af497def90fec7ea847d5be
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.5 MB (182525499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5af0d365e7f1ea1ee717279d98c9bd07252bc72c63928ee49e2d802eddcc6e7`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 17 Aug 2021 01:23:52 GMT
ADD file:b9e6354f7b545096b6cb6072a50de0dffa2232f22d1972a4679f46a7e6394cae in / 
# Tue, 17 Aug 2021 01:23:53 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 09:20:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 09:20:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Aug 2021 07:05:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 18 Aug 2021 07:06:03 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 18 Aug 2021 07:06:04 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 18 Aug 2021 07:06:04 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Aug 2021 07:06:04 GMT
ENV LANG=C.UTF-8
# Wed, 18 Aug 2021 07:06:05 GMT
ENV JAVA_VERSION=8u302
# Wed, 18 Aug 2021 07:06:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_x64_linux_8u302b08.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_aarch64_linux_8u302b08.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Wed, 18 Aug 2021 21:01:37 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Aug 2021 21:01:38 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 18 Aug 2021 21:01:38 GMT
WORKDIR /usr/local/tomee
# Wed, 18 Aug 2021 21:01:38 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Wed, 18 Aug 2021 21:01:49 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Wed, 18 Aug 2021 21:02:54 GMT
ENV TOMEE_VER=8.0.6
# Wed, 18 Aug 2021 21:03:05 GMT
ENV TOMEE_BUILD=plus
# Wed, 18 Aug 2021 21:03:12 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm bin/*.exe 	&& rm tomee.tar.gz*
# Wed, 18 Aug 2021 21:03:12 GMT
EXPOSE 8080
# Wed, 18 Aug 2021 21:03:13 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:1cfaf5c6f756207bc4607d40ddd440bd2bfa7ab455b2c3015ccf56d85cd1377b`  
		Last Modified: Tue, 17 Aug 2021 01:29:55 GMT  
		Size: 50.4 MB (50436201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4099a935a96edef1e9378de34e314d07fb3aea1b7205774055a1fa44a3819f4`  
		Last Modified: Tue, 17 Aug 2021 09:30:37 GMT  
		Size: 7.8 MB (7833079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e2960d83651b1494b4da6c97686e79cc760aa90a75948eed56786726f86928`  
		Last Modified: Tue, 17 Aug 2021 09:30:38 GMT  
		Size: 10.0 MB (9997209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02210be58959d874de759b34af368e884f52b8ac7643bd3cfaefe6b847bf92dd`  
		Last Modified: Wed, 18 Aug 2021 07:12:01 GMT  
		Size: 5.5 MB (5531118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5e6eb5c7de7d87b3d4bad5c7ac2da2c2943b073dd07ffec22cd79082839eec`  
		Last Modified: Wed, 18 Aug 2021 07:12:57 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa71fb980438da57be6fdbd979262a55138aaab7b0acb4ac8b6b04578854660`  
		Last Modified: Wed, 18 Aug 2021 07:13:01 GMT  
		Size: 41.4 MB (41367106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22b65d65f44a9befc0e14b90d8d92b02546463c854c0ced84d707c164dc5e39`  
		Last Modified: Wed, 18 Aug 2021 21:05:00 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf51b27dd69b75ab79c0f91e0edc4957eda7aa2f51ce1ca1bae1c8d4683bd5e`  
		Last Modified: Wed, 18 Aug 2021 21:05:00 GMT  
		Size: 21.0 KB (21047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac13c1d086319809aab9e8db143cf610a37c4128393e152ef308e6eb5c36ade9`  
		Last Modified: Wed, 18 Aug 2021 21:07:01 GMT  
		Size: 67.3 MB (67339355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:8-jre-8.0.6-webprofile`

```console
$ docker pull tomee@sha256:0c473310eeb8a1074b432d4f6fe68b73214b777abc0f8076327f87f6696c236e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `tomee:8-jre-8.0.6-webprofile` - linux; amd64

```console
$ docker pull tomee@sha256:6789025210248710ee88c9cd47a10002944e0caf92288f2caed5ff08b7ca6777
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.2 MB (162169305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8056a6b36495d985dcb907b022cdb7498e473cc388293495da234b3b4850be7`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 17 Aug 2021 01:23:52 GMT
ADD file:b9e6354f7b545096b6cb6072a50de0dffa2232f22d1972a4679f46a7e6394cae in / 
# Tue, 17 Aug 2021 01:23:53 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 09:20:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 09:20:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Aug 2021 07:05:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 18 Aug 2021 07:06:03 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 18 Aug 2021 07:06:04 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 18 Aug 2021 07:06:04 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Aug 2021 07:06:04 GMT
ENV LANG=C.UTF-8
# Wed, 18 Aug 2021 07:06:05 GMT
ENV JAVA_VERSION=8u302
# Wed, 18 Aug 2021 07:06:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_x64_linux_8u302b08.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_aarch64_linux_8u302b08.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Wed, 18 Aug 2021 21:01:37 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Aug 2021 21:01:38 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 18 Aug 2021 21:01:38 GMT
WORKDIR /usr/local/tomee
# Wed, 18 Aug 2021 21:01:38 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Wed, 18 Aug 2021 21:01:49 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Wed, 18 Aug 2021 21:02:54 GMT
ENV TOMEE_VER=8.0.6
# Wed, 18 Aug 2021 21:03:25 GMT
ENV TOMEE_BUILD=webprofile
# Wed, 18 Aug 2021 21:03:30 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm bin/*.exe 	&& rm tomee.tar.gz*
# Wed, 18 Aug 2021 21:03:30 GMT
EXPOSE 8080
# Wed, 18 Aug 2021 21:03:31 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:1cfaf5c6f756207bc4607d40ddd440bd2bfa7ab455b2c3015ccf56d85cd1377b`  
		Last Modified: Tue, 17 Aug 2021 01:29:55 GMT  
		Size: 50.4 MB (50436201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4099a935a96edef1e9378de34e314d07fb3aea1b7205774055a1fa44a3819f4`  
		Last Modified: Tue, 17 Aug 2021 09:30:37 GMT  
		Size: 7.8 MB (7833079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e2960d83651b1494b4da6c97686e79cc760aa90a75948eed56786726f86928`  
		Last Modified: Tue, 17 Aug 2021 09:30:38 GMT  
		Size: 10.0 MB (9997209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02210be58959d874de759b34af368e884f52b8ac7643bd3cfaefe6b847bf92dd`  
		Last Modified: Wed, 18 Aug 2021 07:12:01 GMT  
		Size: 5.5 MB (5531118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5e6eb5c7de7d87b3d4bad5c7ac2da2c2943b073dd07ffec22cd79082839eec`  
		Last Modified: Wed, 18 Aug 2021 07:12:57 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa71fb980438da57be6fdbd979262a55138aaab7b0acb4ac8b6b04578854660`  
		Last Modified: Wed, 18 Aug 2021 07:13:01 GMT  
		Size: 41.4 MB (41367106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22b65d65f44a9befc0e14b90d8d92b02546463c854c0ced84d707c164dc5e39`  
		Last Modified: Wed, 18 Aug 2021 21:05:00 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf51b27dd69b75ab79c0f91e0edc4957eda7aa2f51ce1ca1bae1c8d4683bd5e`  
		Last Modified: Wed, 18 Aug 2021 21:05:00 GMT  
		Size: 21.0 KB (21047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6babb2c1355ba0138424c69dd8e745090289bddc9d6734d56f1fba2d5593389d`  
		Last Modified: Wed, 18 Aug 2021 21:07:23 GMT  
		Size: 47.0 MB (46983161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:8.0.6-microprofile`

```console
$ docker pull tomee@sha256:5a78751cb7d3f58f8040f139ae208cbcef4672a2271e46d4e8ff13f5e3733d1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `tomee:8.0.6-microprofile` - linux; amd64

```console
$ docker pull tomee@sha256:525060bbb4f91ca72a3f5a82608191548b91535345f674e5f1bd4e6b68bec3a7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.1 MB (183127940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdfe4d955f75ce8b798076b95e67583da634731da28fbd2a2db92813f1bd28b1`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 17 Aug 2021 01:23:52 GMT
ADD file:b9e6354f7b545096b6cb6072a50de0dffa2232f22d1972a4679f46a7e6394cae in / 
# Tue, 17 Aug 2021 01:23:53 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 09:20:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 09:20:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Aug 2021 07:05:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 18 Aug 2021 07:05:20 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Wed, 18 Aug 2021 07:05:21 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 18 Aug 2021 07:05:21 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Aug 2021 07:05:21 GMT
ENV LANG=C.UTF-8
# Wed, 18 Aug 2021 07:05:22 GMT
ENV JAVA_VERSION=11.0.12
# Wed, 18 Aug 2021 07:05:28 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jre_x64_linux_11.0.12_7.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jre_aarch64_linux_11.0.12_7.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Wed, 18 Aug 2021 21:03:33 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Aug 2021 21:03:34 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 18 Aug 2021 21:03:34 GMT
WORKDIR /usr/local/tomee
# Wed, 18 Aug 2021 21:03:35 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Wed, 18 Aug 2021 21:03:41 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Wed, 18 Aug 2021 21:03:42 GMT
ENV TOMEE_VER=8.0.6
# Wed, 18 Aug 2021 21:04:06 GMT
ENV TOMEE_BUILD=microprofile
# Wed, 18 Aug 2021 21:04:13 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm bin/*.exe 	&& rm tomee.tar.gz*
# Wed, 18 Aug 2021 21:04:13 GMT
EXPOSE 8080
# Wed, 18 Aug 2021 21:04:13 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:1cfaf5c6f756207bc4607d40ddd440bd2bfa7ab455b2c3015ccf56d85cd1377b`  
		Last Modified: Tue, 17 Aug 2021 01:29:55 GMT  
		Size: 50.4 MB (50436201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4099a935a96edef1e9378de34e314d07fb3aea1b7205774055a1fa44a3819f4`  
		Last Modified: Tue, 17 Aug 2021 09:30:37 GMT  
		Size: 7.8 MB (7833079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e2960d83651b1494b4da6c97686e79cc760aa90a75948eed56786726f86928`  
		Last Modified: Tue, 17 Aug 2021 09:30:38 GMT  
		Size: 10.0 MB (9997209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02210be58959d874de759b34af368e884f52b8ac7643bd3cfaefe6b847bf92dd`  
		Last Modified: Wed, 18 Aug 2021 07:12:01 GMT  
		Size: 5.5 MB (5531118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99137bab1caf27aee8d1f5f962699a054178b8bc48ef8f5d17648337e8579837`  
		Last Modified: Wed, 18 Aug 2021 07:12:00 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38621337f17c0f871f3675b78bd321096624cd617666be70bc9a259788e93041`  
		Last Modified: Wed, 18 Aug 2021 07:12:07 GMT  
		Size: 46.9 MB (46863974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0238d73f652115c041086e00940b503df0976e22ba3f9f5b2a8d9a7b609d7173`  
		Last Modified: Wed, 18 Aug 2021 21:07:31 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abea88b63ce675e6fd5e791cdca5a2a54dd1baa53825c2c8f5bdc7cc0b073134`  
		Last Modified: Wed, 18 Aug 2021 21:07:31 GMT  
		Size: 21.0 KB (21021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f9797dfac064d2e34cae4a482084df62277a997efd6b382a2ef65a3735fe2d`  
		Last Modified: Wed, 18 Aug 2021 21:08:04 GMT  
		Size: 62.4 MB (62444954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:8.0.6-plume`

```console
$ docker pull tomee@sha256:f3d2ff3de9277db837ab1041d6c177a36d03216eb0f984eda87a9cfd7b6b216a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `tomee:8.0.6-plume` - linux; amd64

```console
$ docker pull tomee@sha256:e3794e0fcc3b7883c5265388d0ea382a3dc86fc958eb8e23042ecde22f8246cd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.3 MB (195303083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceb62bbf4720148af49aaa7f8578ffe94d9372986dd0544172aed3ae774b2bbd`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 17 Aug 2021 01:23:52 GMT
ADD file:b9e6354f7b545096b6cb6072a50de0dffa2232f22d1972a4679f46a7e6394cae in / 
# Tue, 17 Aug 2021 01:23:53 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 09:20:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 09:20:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Aug 2021 07:05:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 18 Aug 2021 07:05:20 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Wed, 18 Aug 2021 07:05:21 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 18 Aug 2021 07:05:21 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Aug 2021 07:05:21 GMT
ENV LANG=C.UTF-8
# Wed, 18 Aug 2021 07:05:22 GMT
ENV JAVA_VERSION=11.0.12
# Wed, 18 Aug 2021 07:05:28 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jre_x64_linux_11.0.12_7.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jre_aarch64_linux_11.0.12_7.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Wed, 18 Aug 2021 21:03:33 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Aug 2021 21:03:34 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 18 Aug 2021 21:03:34 GMT
WORKDIR /usr/local/tomee
# Wed, 18 Aug 2021 21:03:35 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Wed, 18 Aug 2021 21:03:41 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Wed, 18 Aug 2021 21:03:42 GMT
ENV TOMEE_VER=8.0.6
# Wed, 18 Aug 2021 21:03:42 GMT
ENV TOMEE_BUILD=plume
# Wed, 18 Aug 2021 21:03:49 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm bin/*.exe 	&& rm tomee.tar.gz*
# Wed, 18 Aug 2021 21:03:49 GMT
EXPOSE 8080
# Wed, 18 Aug 2021 21:03:49 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:1cfaf5c6f756207bc4607d40ddd440bd2bfa7ab455b2c3015ccf56d85cd1377b`  
		Last Modified: Tue, 17 Aug 2021 01:29:55 GMT  
		Size: 50.4 MB (50436201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4099a935a96edef1e9378de34e314d07fb3aea1b7205774055a1fa44a3819f4`  
		Last Modified: Tue, 17 Aug 2021 09:30:37 GMT  
		Size: 7.8 MB (7833079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e2960d83651b1494b4da6c97686e79cc760aa90a75948eed56786726f86928`  
		Last Modified: Tue, 17 Aug 2021 09:30:38 GMT  
		Size: 10.0 MB (9997209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02210be58959d874de759b34af368e884f52b8ac7643bd3cfaefe6b847bf92dd`  
		Last Modified: Wed, 18 Aug 2021 07:12:01 GMT  
		Size: 5.5 MB (5531118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99137bab1caf27aee8d1f5f962699a054178b8bc48ef8f5d17648337e8579837`  
		Last Modified: Wed, 18 Aug 2021 07:12:00 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38621337f17c0f871f3675b78bd321096624cd617666be70bc9a259788e93041`  
		Last Modified: Wed, 18 Aug 2021 07:12:07 GMT  
		Size: 46.9 MB (46863974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0238d73f652115c041086e00940b503df0976e22ba3f9f5b2a8d9a7b609d7173`  
		Last Modified: Wed, 18 Aug 2021 21:07:31 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abea88b63ce675e6fd5e791cdca5a2a54dd1baa53825c2c8f5bdc7cc0b073134`  
		Last Modified: Wed, 18 Aug 2021 21:07:31 GMT  
		Size: 21.0 KB (21021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b07bd22572328a7631757bdde85198dcb3ea2658462a2d5b4bf2be7939a76fb9`  
		Last Modified: Wed, 18 Aug 2021 21:07:35 GMT  
		Size: 74.6 MB (74620097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:8.0.6-plus`

```console
$ docker pull tomee@sha256:44147e49e1f8c6a5a62b672566627d3e05326d8b5c70f2219077f043bd79ddc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `tomee:8.0.6-plus` - linux; amd64

```console
$ docker pull tomee@sha256:06bb64a6a9c5a04a2eb85e581f6b250d2a96cc58f22d84c61a991d27c1a5e4b5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.0 MB (188022199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc33323e0f6f16700746f84a32bb0779f8ec13ede112eeb99e4cb24c9e3a1d31`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 17 Aug 2021 01:23:52 GMT
ADD file:b9e6354f7b545096b6cb6072a50de0dffa2232f22d1972a4679f46a7e6394cae in / 
# Tue, 17 Aug 2021 01:23:53 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 09:20:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 09:20:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Aug 2021 07:05:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 18 Aug 2021 07:05:20 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Wed, 18 Aug 2021 07:05:21 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 18 Aug 2021 07:05:21 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Aug 2021 07:05:21 GMT
ENV LANG=C.UTF-8
# Wed, 18 Aug 2021 07:05:22 GMT
ENV JAVA_VERSION=11.0.12
# Wed, 18 Aug 2021 07:05:28 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jre_x64_linux_11.0.12_7.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jre_aarch64_linux_11.0.12_7.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Wed, 18 Aug 2021 21:03:33 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Aug 2021 21:03:34 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 18 Aug 2021 21:03:34 GMT
WORKDIR /usr/local/tomee
# Wed, 18 Aug 2021 21:03:35 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Wed, 18 Aug 2021 21:03:41 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Wed, 18 Aug 2021 21:03:42 GMT
ENV TOMEE_VER=8.0.6
# Wed, 18 Aug 2021 21:03:55 GMT
ENV TOMEE_BUILD=plus
# Wed, 18 Aug 2021 21:04:02 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm bin/*.exe 	&& rm tomee.tar.gz*
# Wed, 18 Aug 2021 21:04:02 GMT
EXPOSE 8080
# Wed, 18 Aug 2021 21:04:02 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:1cfaf5c6f756207bc4607d40ddd440bd2bfa7ab455b2c3015ccf56d85cd1377b`  
		Last Modified: Tue, 17 Aug 2021 01:29:55 GMT  
		Size: 50.4 MB (50436201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4099a935a96edef1e9378de34e314d07fb3aea1b7205774055a1fa44a3819f4`  
		Last Modified: Tue, 17 Aug 2021 09:30:37 GMT  
		Size: 7.8 MB (7833079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e2960d83651b1494b4da6c97686e79cc760aa90a75948eed56786726f86928`  
		Last Modified: Tue, 17 Aug 2021 09:30:38 GMT  
		Size: 10.0 MB (9997209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02210be58959d874de759b34af368e884f52b8ac7643bd3cfaefe6b847bf92dd`  
		Last Modified: Wed, 18 Aug 2021 07:12:01 GMT  
		Size: 5.5 MB (5531118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99137bab1caf27aee8d1f5f962699a054178b8bc48ef8f5d17648337e8579837`  
		Last Modified: Wed, 18 Aug 2021 07:12:00 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38621337f17c0f871f3675b78bd321096624cd617666be70bc9a259788e93041`  
		Last Modified: Wed, 18 Aug 2021 07:12:07 GMT  
		Size: 46.9 MB (46863974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0238d73f652115c041086e00940b503df0976e22ba3f9f5b2a8d9a7b609d7173`  
		Last Modified: Wed, 18 Aug 2021 21:07:31 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abea88b63ce675e6fd5e791cdca5a2a54dd1baa53825c2c8f5bdc7cc0b073134`  
		Last Modified: Wed, 18 Aug 2021 21:07:31 GMT  
		Size: 21.0 KB (21021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab8bc65a5133c12b559131b73f78d03a5b11057495b2da409de06a0d2c55a19d`  
		Last Modified: Wed, 18 Aug 2021 21:07:50 GMT  
		Size: 67.3 MB (67339213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:8.0.6-webprofile`

```console
$ docker pull tomee@sha256:756706fa209e96a1fcfaa6d44902df08d72d1ae98ed33bb7f837770eec6b96b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `tomee:8.0.6-webprofile` - linux; amd64

```console
$ docker pull tomee@sha256:947e86961e6e952a8a1481e597db5e69d068b1487801c477e2777d4dd90458e2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.7 MB (167666075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c351eb6566105c3d7b95afc4d89da3efd5cf37902af3d65a40e82d527679563`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 17 Aug 2021 01:23:52 GMT
ADD file:b9e6354f7b545096b6cb6072a50de0dffa2232f22d1972a4679f46a7e6394cae in / 
# Tue, 17 Aug 2021 01:23:53 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 09:20:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 09:20:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Aug 2021 07:05:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 18 Aug 2021 07:05:20 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Wed, 18 Aug 2021 07:05:21 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 18 Aug 2021 07:05:21 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Aug 2021 07:05:21 GMT
ENV LANG=C.UTF-8
# Wed, 18 Aug 2021 07:05:22 GMT
ENV JAVA_VERSION=11.0.12
# Wed, 18 Aug 2021 07:05:28 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jre_x64_linux_11.0.12_7.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jre_aarch64_linux_11.0.12_7.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Wed, 18 Aug 2021 21:03:33 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Aug 2021 21:03:34 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 18 Aug 2021 21:03:34 GMT
WORKDIR /usr/local/tomee
# Wed, 18 Aug 2021 21:03:35 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Wed, 18 Aug 2021 21:03:41 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Wed, 18 Aug 2021 21:03:42 GMT
ENV TOMEE_VER=8.0.6
# Wed, 18 Aug 2021 21:04:16 GMT
ENV TOMEE_BUILD=webprofile
# Wed, 18 Aug 2021 21:04:21 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm bin/*.exe 	&& rm tomee.tar.gz*
# Wed, 18 Aug 2021 21:04:21 GMT
EXPOSE 8080
# Wed, 18 Aug 2021 21:04:22 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:1cfaf5c6f756207bc4607d40ddd440bd2bfa7ab455b2c3015ccf56d85cd1377b`  
		Last Modified: Tue, 17 Aug 2021 01:29:55 GMT  
		Size: 50.4 MB (50436201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4099a935a96edef1e9378de34e314d07fb3aea1b7205774055a1fa44a3819f4`  
		Last Modified: Tue, 17 Aug 2021 09:30:37 GMT  
		Size: 7.8 MB (7833079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e2960d83651b1494b4da6c97686e79cc760aa90a75948eed56786726f86928`  
		Last Modified: Tue, 17 Aug 2021 09:30:38 GMT  
		Size: 10.0 MB (9997209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02210be58959d874de759b34af368e884f52b8ac7643bd3cfaefe6b847bf92dd`  
		Last Modified: Wed, 18 Aug 2021 07:12:01 GMT  
		Size: 5.5 MB (5531118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99137bab1caf27aee8d1f5f962699a054178b8bc48ef8f5d17648337e8579837`  
		Last Modified: Wed, 18 Aug 2021 07:12:00 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38621337f17c0f871f3675b78bd321096624cd617666be70bc9a259788e93041`  
		Last Modified: Wed, 18 Aug 2021 07:12:07 GMT  
		Size: 46.9 MB (46863974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0238d73f652115c041086e00940b503df0976e22ba3f9f5b2a8d9a7b609d7173`  
		Last Modified: Wed, 18 Aug 2021 21:07:31 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abea88b63ce675e6fd5e791cdca5a2a54dd1baa53825c2c8f5bdc7cc0b073134`  
		Last Modified: Wed, 18 Aug 2021 21:07:31 GMT  
		Size: 21.0 KB (21021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7bd68da3315025fb523b0d63d54be4e8fb29ee0ffe220f66e4925b760ff3b19`  
		Last Modified: Wed, 18 Aug 2021 21:08:18 GMT  
		Size: 47.0 MB (46983089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:latest`

```console
$ docker pull tomee@sha256:756706fa209e96a1fcfaa6d44902df08d72d1ae98ed33bb7f837770eec6b96b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `tomee:latest` - linux; amd64

```console
$ docker pull tomee@sha256:947e86961e6e952a8a1481e597db5e69d068b1487801c477e2777d4dd90458e2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.7 MB (167666075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c351eb6566105c3d7b95afc4d89da3efd5cf37902af3d65a40e82d527679563`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 17 Aug 2021 01:23:52 GMT
ADD file:b9e6354f7b545096b6cb6072a50de0dffa2232f22d1972a4679f46a7e6394cae in / 
# Tue, 17 Aug 2021 01:23:53 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 09:20:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 09:20:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Aug 2021 07:05:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 18 Aug 2021 07:05:20 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Wed, 18 Aug 2021 07:05:21 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 18 Aug 2021 07:05:21 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Aug 2021 07:05:21 GMT
ENV LANG=C.UTF-8
# Wed, 18 Aug 2021 07:05:22 GMT
ENV JAVA_VERSION=11.0.12
# Wed, 18 Aug 2021 07:05:28 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jre_x64_linux_11.0.12_7.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jre_aarch64_linux_11.0.12_7.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Wed, 18 Aug 2021 21:03:33 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Aug 2021 21:03:34 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 18 Aug 2021 21:03:34 GMT
WORKDIR /usr/local/tomee
# Wed, 18 Aug 2021 21:03:35 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Wed, 18 Aug 2021 21:03:41 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Wed, 18 Aug 2021 21:03:42 GMT
ENV TOMEE_VER=8.0.6
# Wed, 18 Aug 2021 21:04:16 GMT
ENV TOMEE_BUILD=webprofile
# Wed, 18 Aug 2021 21:04:21 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm bin/*.exe 	&& rm tomee.tar.gz*
# Wed, 18 Aug 2021 21:04:21 GMT
EXPOSE 8080
# Wed, 18 Aug 2021 21:04:22 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:1cfaf5c6f756207bc4607d40ddd440bd2bfa7ab455b2c3015ccf56d85cd1377b`  
		Last Modified: Tue, 17 Aug 2021 01:29:55 GMT  
		Size: 50.4 MB (50436201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4099a935a96edef1e9378de34e314d07fb3aea1b7205774055a1fa44a3819f4`  
		Last Modified: Tue, 17 Aug 2021 09:30:37 GMT  
		Size: 7.8 MB (7833079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e2960d83651b1494b4da6c97686e79cc760aa90a75948eed56786726f86928`  
		Last Modified: Tue, 17 Aug 2021 09:30:38 GMT  
		Size: 10.0 MB (9997209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02210be58959d874de759b34af368e884f52b8ac7643bd3cfaefe6b847bf92dd`  
		Last Modified: Wed, 18 Aug 2021 07:12:01 GMT  
		Size: 5.5 MB (5531118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99137bab1caf27aee8d1f5f962699a054178b8bc48ef8f5d17648337e8579837`  
		Last Modified: Wed, 18 Aug 2021 07:12:00 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38621337f17c0f871f3675b78bd321096624cd617666be70bc9a259788e93041`  
		Last Modified: Wed, 18 Aug 2021 07:12:07 GMT  
		Size: 46.9 MB (46863974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0238d73f652115c041086e00940b503df0976e22ba3f9f5b2a8d9a7b609d7173`  
		Last Modified: Wed, 18 Aug 2021 21:07:31 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abea88b63ce675e6fd5e791cdca5a2a54dd1baa53825c2c8f5bdc7cc0b073134`  
		Last Modified: Wed, 18 Aug 2021 21:07:31 GMT  
		Size: 21.0 KB (21021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7bd68da3315025fb523b0d63d54be4e8fb29ee0ffe220f66e4925b760ff3b19`  
		Last Modified: Wed, 18 Aug 2021 21:08:18 GMT  
		Size: 47.0 MB (46983089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
