## `openjdk:27-ea-19-jdk-trixie`

```console
$ docker pull openjdk@sha256:8b34b5ee953c202e2d8be6a7e1f0632ec52c3693e13b1141886312a3fb132b21
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-19-jdk-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:d9ae465b0f7405df44898cbc27a7c801b8175f0878e486e707e43ecc1633ee1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.3 MB (387326560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:520e6e18d2b77520e7e799ad807f909e01138da1dee1b8da8435847b2941b293`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:45:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 28 Apr 2026 23:34:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Apr 2026 23:34:43 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 28 Apr 2026 23:34:43 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Apr 2026 23:34:43 GMT
ENV LANG=C.UTF-8
# Tue, 28 Apr 2026 23:34:43 GMT
ENV JAVA_VERSION=27-ea+19
# Tue, 28 Apr 2026 23:34:43 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/19/GPL/openjdk-27-ea+19_linux-x64_bin.tar.gz'; 			downloadSha256='97a3527cdc677e8205e755bd56b8931a8e3461c1bdd7fdd564da9b7842bcea0b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/19/GPL/openjdk-27-ea+19_linux-aarch64_bin.tar.gz'; 			downloadSha256='5d6876749a41cfecbcda3332da94d88a9e3097292f0eeafdb6d7fd41f66265c8'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 28 Apr 2026 23:34:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3b32e3bb7338c216b077e95920ae53332d81bd57f4a7393bc324432d5a3f88a2`  
		Last Modified: Wed, 22 Apr 2026 00:16:56 GMT  
		Size: 49.3 MB (49302102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5467f93954cfe1451f4333422086d00bd066cf33f42112b531804ffe06f0a929`  
		Last Modified: Wed, 22 Apr 2026 01:39:50 GMT  
		Size: 25.6 MB (25622443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20d12c8f3f3fbb5bd2b8369adf3213e09d6b33f975462543ddfece85b2fe85e5`  
		Last Modified: Wed, 22 Apr 2026 04:45:50 GMT  
		Size: 67.8 MB (67790089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db950563f79bf97925d4c9c4d06d9c7fe5a65e55d6bc75199278b07e869feac`  
		Last Modified: Tue, 28 Apr 2026 23:35:07 GMT  
		Size: 16.1 MB (16064953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b14a418bfddc794e21a9d54976715c8cd0e1071444bef6e66c11f386993c867c`  
		Last Modified: Tue, 28 Apr 2026 23:35:12 GMT  
		Size: 228.5 MB (228546973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-19-jdk-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:372fc773a77fb9d92f4b0534b816eaf0548bbedb24315d6bec84cd554ad72755
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8527833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2368b50b7b8c3f4e4c88792f294d05f17459be7414f31472896d252067a0be00`

```dockerfile
```

-	Layers:
	-	`sha256:d0285505ae955b1fa684d490dcba8b78169a24ebb3a4318f7f96de79becdcb9f`  
		Last Modified: Tue, 28 Apr 2026 23:35:07 GMT  
		Size: 8.5 MB (8509920 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88da580639f554f50f4f8be9edab3c14b8145fc4764edbd4cf9d80fff4f4bd33`  
		Last Modified: Tue, 28 Apr 2026 23:35:07 GMT  
		Size: 17.9 KB (17913 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-19-jdk-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:f500fca652ec167db3cf5107978c98250d3b29000f5a0b007a8a76fa6e071f77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.9 MB (384853128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84cab4187ebe8c59068fdaf6cb680f8ea10fa0bc18d32333839bc717a33410d5`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:43:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 02:32:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 28 Apr 2026 23:35:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Apr 2026 23:35:41 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 28 Apr 2026 23:35:41 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Apr 2026 23:35:41 GMT
ENV LANG=C.UTF-8
# Tue, 28 Apr 2026 23:35:41 GMT
ENV JAVA_VERSION=27-ea+19
# Tue, 28 Apr 2026 23:35:41 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/19/GPL/openjdk-27-ea+19_linux-x64_bin.tar.gz'; 			downloadSha256='97a3527cdc677e8205e755bd56b8931a8e3461c1bdd7fdd564da9b7842bcea0b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/19/GPL/openjdk-27-ea+19_linux-aarch64_bin.tar.gz'; 			downloadSha256='5d6876749a41cfecbcda3332da94d88a9e3097292f0eeafdb6d7fd41f66265c8'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 28 Apr 2026 23:35:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6e7932d5cb5573d1bff4fb8801baad19fc72d2ae741bb046333573653944f5a5`  
		Last Modified: Wed, 22 Apr 2026 00:16:45 GMT  
		Size: 49.7 MB (49669245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705f67984ab3d0b84dba0bf1b9e75bc42547713ab962aa5b392bacb0e61fa68b`  
		Last Modified: Wed, 22 Apr 2026 01:43:34 GMT  
		Size: 25.0 MB (25023409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c17e454c787ef19107fbea0250c33a4b6ca95fe0319ad68539a7bae9d9cad57`  
		Last Modified: Wed, 22 Apr 2026 02:32:52 GMT  
		Size: 67.6 MB (67584735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61907f74ae6bbe2e7d326e5928ae94a7685b685ee111a39c6aa8370365d4a79b`  
		Last Modified: Tue, 28 Apr 2026 23:36:07 GMT  
		Size: 16.1 MB (16071256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:368a1be73ed789d7f5e93f30490b49526379ee4bfd0223d503c60bc43224025f`  
		Last Modified: Tue, 28 Apr 2026 23:36:11 GMT  
		Size: 226.5 MB (226504483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-19-jdk-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:89f1f5fbe601d888ce10671e5942ea1d9b0c7d929f1d1bcb452cf0fcd4533517
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8722742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbcd132193e94f7f1e925555e7e7bb084aadcdf23e8c3dc2b1d75bbec77d1bec`

```dockerfile
```

-	Layers:
	-	`sha256:845a08265a28e69a6a4702d53dbb30c4d37e36e762d82ffe127f7981bca3d0c5`  
		Last Modified: Tue, 28 Apr 2026 23:36:07 GMT  
		Size: 8.7 MB (8704710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec0449d5606267d7e6599248d79793d8e7456bb0c49a61bded2cd4cb200a72ff`  
		Last Modified: Tue, 28 Apr 2026 23:36:06 GMT  
		Size: 18.0 KB (18032 bytes)  
		MIME: application/vnd.in-toto+json
