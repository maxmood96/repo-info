## `openjdk:24-jdk-bullseye`

```console
$ docker pull openjdk@sha256:7cba719a08d4b0dfaf15b307e0c3ab602f592225f06cbaa159a3adb6cca6b7bc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-jdk-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:b5f2fca0cf7d9aea1df968ac4090546cdb14c0158d2e683993498e006ec24d20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.7 MB (361681611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5271ad564618d80a347a69ed80de39c9277259909002957d78da0d2c564405e4`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 Nov 2024 01:48:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 Nov 2024 01:48:14 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 15 Nov 2024 01:48:14 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Nov 2024 01:48:14 GMT
ENV LANG=C.UTF-8
# Fri, 15 Nov 2024 01:48:14 GMT
ENV JAVA_VERSION=24-ea+24
# Fri, 15 Nov 2024 01:48:14 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/24/GPL/openjdk-24-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='d6aa1bee11c9e9b14603f88fa1620ae6572d81194cf50a6d8da876ba2ff3ec40'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/24/GPL/openjdk-24-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='1097eb5c1379e64a06ab8ba8a1af84a0802ab573823a7b8c792a5df8c1cc2509'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 15 Nov 2024 01:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c2056d933cd629f55ac55802dda223f122286bf60ec42a24f0d0f6ae2615315c`  
		Last Modified: Tue, 12 Nov 2024 00:55:16 GMT  
		Size: 55.1 MB (55108780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f895247ac53f8ccaff2388685ac5288e243187f243654f4af6205a31f8b693`  
		Last Modified: Tue, 12 Nov 2024 02:37:53 GMT  
		Size: 15.6 MB (15557923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d199724b11b5ccb55a34503a046bfe20064837b3f7beb547b9a3eab1cb57e0`  
		Last Modified: Tue, 12 Nov 2024 03:14:06 GMT  
		Size: 54.7 MB (54735758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2742eb54aca1ccebb8473d2197e7ba620b441b96322847f04d6a1baabe3da81c`  
		Last Modified: Fri, 15 Nov 2024 23:04:50 GMT  
		Size: 14.1 MB (14071437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a500890031aec52001479f357137da10de871389b4240b0badfe955d5b17aea`  
		Last Modified: Fri, 15 Nov 2024 23:04:53 GMT  
		Size: 222.2 MB (222207713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:534090d35ffa139a732c9cd91c559310be4276ece02846cee77a65eb164ff757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8392615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb182bed3fdfb918433af12ba5580ea3e9188eed1e250623ffebe720975d19a1`

```dockerfile
```

-	Layers:
	-	`sha256:265869260963f0ecacb075f50d518d058ab22b45647f4fc551a71960768198da`  
		Last Modified: Fri, 15 Nov 2024 23:04:50 GMT  
		Size: 8.4 MB (8373997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef6d090031dd21faccf70e3bd91fb744295e4950c90da9fca017798ebbd7fa09`  
		Last Modified: Fri, 15 Nov 2024 23:04:50 GMT  
		Size: 18.6 KB (18618 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-jdk-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:8b68621ffed7b1fcb71814a723eefd34cc9b36418f55c3e8e8a6c92c676a7724
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.8 MB (359829298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2346e7d1ebb36e642ba42187c3057884c8defd2761dc78d4177bfbff5178fcb1`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 Nov 2024 01:48:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 Nov 2024 01:48:14 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 15 Nov 2024 01:48:14 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Nov 2024 01:48:14 GMT
ENV LANG=C.UTF-8
# Fri, 15 Nov 2024 01:48:14 GMT
ENV JAVA_VERSION=24-ea+24
# Fri, 15 Nov 2024 01:48:14 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/24/GPL/openjdk-24-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='d6aa1bee11c9e9b14603f88fa1620ae6572d81194cf50a6d8da876ba2ff3ec40'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/24/GPL/openjdk-24-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='1097eb5c1379e64a06ab8ba8a1af84a0802ab573823a7b8c792a5df8c1cc2509'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 15 Nov 2024 01:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a839664fe62f615da74af799f94ccbc890a15d0f78470aac54302c2fd5475615`  
		Last Modified: Tue, 12 Nov 2024 00:57:41 GMT  
		Size: 53.8 MB (53757072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca9e545ff305fe56558a94b064a901c16b373a3501daf5519f82ec19db6a3655`  
		Last Modified: Tue, 12 Nov 2024 11:16:34 GMT  
		Size: 15.5 MB (15543588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d952be101e4ab063ff4eafa1d2809245e9ac9e713c342da9f201d2280d4a6c9b`  
		Last Modified: Wed, 13 Nov 2024 02:42:41 GMT  
		Size: 54.8 MB (54842084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c623f874b16f14c4d69bec05c9b83214f158dbfa8442708dd1556a399d617a03`  
		Last Modified: Wed, 13 Nov 2024 09:13:06 GMT  
		Size: 15.5 MB (15526044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91fedfadcfb2942ec5f1eef33a0de45e9d157d707b90ca6d263547ecced616c4`  
		Last Modified: Fri, 15 Nov 2024 23:13:05 GMT  
		Size: 220.2 MB (220160510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:f884e3765c4f176795d9df1c03d426a9d59689aa85421473889f16ff9c5939ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8493842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dda8567d8b3765afac93592869d15952e83408845f4d8b89460820e9359e2f7d`

```dockerfile
```

-	Layers:
	-	`sha256:1219fec24a882fb3f7326e520561423e684023bf286ee072ad6cb56b39d6b067`  
		Last Modified: Fri, 15 Nov 2024 23:13:01 GMT  
		Size: 8.5 MB (8475081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef5fa58505f904fae71016c5c93a6ccf291f3c1a7c3cf78a1951cfdcbe77bf2b`  
		Last Modified: Fri, 15 Nov 2024 23:13:00 GMT  
		Size: 18.8 KB (18761 bytes)  
		MIME: application/vnd.in-toto+json
