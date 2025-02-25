## `openjdk:25-ea-11-bullseye`

```console
$ docker pull openjdk@sha256:f8a92413f5d2ec2e24ac5ab7c6c4e55a19a1dcf26fdf9471fe604d3b5b356fc5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-11-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:fbb693a3b94b803162792b581bed105e0913895c81c1d67c361fc9e8f95c8909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.1 MB (350053014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c784854ff1bc909406126cacde51540626f23370177e81b0299589258102631a`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:48:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:48:17 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 21 Feb 2025 01:48:17 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 21 Feb 2025 01:48:17 GMT
ENV LANG=C.UTF-8
# Fri, 21 Feb 2025 01:48:17 GMT
ENV JAVA_VERSION=25-ea+11
# Fri, 21 Feb 2025 01:48:17 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/11/GPL/openjdk-25-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='48a39baf57099268625cdafd903613bf54229d97dfd800d01733e036770a89f7'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/11/GPL/openjdk-25-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='fbbf2112e28aede77dc8f42dd8e27e6bcdd34cb862b5dfbb3b1c15c709fedf19'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 21 Feb 2025 01:48:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4ff5a3a54264ee833e4a09583363bbe779e881f15449fe4f4a6a662885dd37fb`  
		Last Modified: Tue, 25 Feb 2025 01:29:47 GMT  
		Size: 53.7 MB (53741401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6bcbc2151ce4be9aa40b26468719dafd6528d7d11d6f6cb60e3a58a3447305`  
		Last Modified: Tue, 25 Feb 2025 02:12:52 GMT  
		Size: 15.6 MB (15558424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e36295709cc3855d0f98f8a6b939053cc43efcf3092756703c1fc518d73fe77`  
		Last Modified: Tue, 25 Feb 2025 03:13:48 GMT  
		Size: 54.8 MB (54752085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f12991f0c8ee9420e43f153656cbd75ee28bbefca253969f6f0f3a02ab96556a`  
		Last Modified: Tue, 25 Feb 2025 04:17:45 GMT  
		Size: 14.1 MB (14071404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2e8d1fba2381e9a10bee849c122e5b5595ff0eccc9fb643438b95ae5637b63`  
		Last Modified: Tue, 25 Feb 2025 04:17:49 GMT  
		Size: 211.9 MB (211929700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-11-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:e3012a1c814aa08646e63e8ab49419ca65360924ee3616bd9e5035ddb1dea359
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8386552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e342449874640b9a6fbca77493db6904f2f0d2476b29e5b7a69a0f04f7a17313`

```dockerfile
```

-	Layers:
	-	`sha256:c468f7b80312eb2d7edc4e0b5875ab8c9e99d0952f6220711100dbedb216540e`  
		Last Modified: Tue, 25 Feb 2025 04:17:45 GMT  
		Size: 8.4 MB (8367934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7754d135eaa05a28f0a18752ffa31f9a512d4468c1ca28b0661dcf8503ce88cc`  
		Last Modified: Tue, 25 Feb 2025 04:17:45 GMT  
		Size: 18.6 KB (18618 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-11-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:370d985109b1adefb47e34eed3e9ddb31ad9651a527212bca32f7e129ac8bb8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.0 MB (348042330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc13e5e308aee3ef315b3db27c07fff9873f96e8708b17a40b3aea6a78dd62af`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1738540800'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:48:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:48:17 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 21 Feb 2025 01:48:17 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 21 Feb 2025 01:48:17 GMT
ENV LANG=C.UTF-8
# Fri, 21 Feb 2025 01:48:17 GMT
ENV JAVA_VERSION=25-ea+11
# Fri, 21 Feb 2025 01:48:17 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/11/GPL/openjdk-25-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='48a39baf57099268625cdafd903613bf54229d97dfd800d01733e036770a89f7'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/11/GPL/openjdk-25-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='fbbf2112e28aede77dc8f42dd8e27e6bcdd34cb862b5dfbb3b1c15c709fedf19'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 21 Feb 2025 01:48:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0038ef039a89ede34c57806e684dc9d9be7dcd22d3c08b90deb36bb22a2c7122`  
		Last Modified: Tue, 04 Feb 2025 01:38:11 GMT  
		Size: 52.2 MB (52245695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c7afb1aa0f9672a06c4c7eaa6b7c7e111a91a8d45272dce1e361ac0b0ed79a`  
		Last Modified: Tue, 04 Feb 2025 09:00:33 GMT  
		Size: 15.5 MB (15544055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8e2f45c7ddf8cc116eeb2ac1ef8be70e3639a883c6d9e5eaf1f2dd702dbf92`  
		Last Modified: Tue, 04 Feb 2025 19:02:31 GMT  
		Size: 54.9 MB (54852696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f71935bf5380fa38f69ff91bf754433c2b1c7b3cdf382c0dfc5a5374d331e545`  
		Last Modified: Wed, 05 Feb 2025 02:55:07 GMT  
		Size: 15.5 MB (15526198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:000f08fd5f9574fbb28ef7f19cd76b48462c9fe64307642806bd556284b07580`  
		Last Modified: Sat, 22 Feb 2025 02:38:22 GMT  
		Size: 209.9 MB (209873686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-11-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:37cc2e4b3ba002476e0370d223c17adbdfda2306ce0244732075d8d5b1de0c83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8487657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52bf9494adb186e3bd35483c01d4fc0d98aceb642427b3c33c63f3612704150c`

```dockerfile
```

-	Layers:
	-	`sha256:a9d22ac7ac77404e8a061b57ebaec3722632b0bbc658bfd01a3f4cb5ebc6806e`  
		Last Modified: Sat, 22 Feb 2025 02:38:11 GMT  
		Size: 8.5 MB (8468896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec1f38d4f1984835ed9921794cfd07222bf60e150859de70b7069abafa23a97c`  
		Last Modified: Sat, 22 Feb 2025 02:38:11 GMT  
		Size: 18.8 KB (18761 bytes)  
		MIME: application/vnd.in-toto+json
