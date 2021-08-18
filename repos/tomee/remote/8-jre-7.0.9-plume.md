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
