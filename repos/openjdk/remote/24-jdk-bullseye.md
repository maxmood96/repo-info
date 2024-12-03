## `openjdk:24-jdk-bullseye`

```console
$ docker pull openjdk@sha256:c7aa1e6b56bd417b163c2ee84ab96033b80bfac583f598c39177e936fd379054
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-jdk-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:7bfa6b10c38dad0862062a6fd94fbb80169e74cbc6ce8094639f8fc6eb8cd513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.2 MB (351151493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4fbb4af3e1e6d247b82d0b31ef7c2158af481302acbfde61dd205699b0090d7`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 22 Nov 2024 19:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 22 Nov 2024 19:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 22 Nov 2024 19:48:12 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Nov 2024 19:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 22 Nov 2024 19:48:12 GMT
ENV JAVA_VERSION=24-ea+25
# Fri, 22 Nov 2024 19:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/25/GPL/openjdk-24-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='06d2571c8af4948ac1eaad2b912ab59f320f01744bc4152f3476a65512bb3901'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/25/GPL/openjdk-24-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='022d2edea028f26d0aa8cc933429f305abac8f8a74451095a55b1354f0db7966'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 22 Nov 2024 19:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cd606f6f489eb66f1307280aec321b3af3aa998dca447ae1cc91c6b884240064`  
		Last Modified: Tue, 03 Dec 2024 01:27:20 GMT  
		Size: 53.7 MB (53739147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925257a7168ed219a5d7c2a69af3245ca4cd9e376424f7f006535d9714437bd4`  
		Last Modified: Tue, 03 Dec 2024 02:15:41 GMT  
		Size: 15.6 MB (15558387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb34ce34679cf6bc8738a0166300fb0af605abff20bb9c1c8008dbc48722061`  
		Last Modified: Tue, 03 Dec 2024 03:17:12 GMT  
		Size: 54.8 MB (54753972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f34ca586a30b667b4b36ea4c810be567681f46492ed91428397dfd91c9c5f7`  
		Last Modified: Tue, 03 Dec 2024 04:31:57 GMT  
		Size: 14.1 MB (14071379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487a00d47ad4aa67a6df38793c528a49f62d7c1e74fa885e61add969f99b2212`  
		Last Modified: Tue, 03 Dec 2024 04:32:00 GMT  
		Size: 213.0 MB (213028608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:bea447f61539223ac8e9848c12e2205aed8836fa9063e49157c7bf13b177a995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8389534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea9a961753e8efc6a2af222847517dc0e6760b1fb7b1ee53c07115ccf6a0ad1e`

```dockerfile
```

-	Layers:
	-	`sha256:6bd431c56580e27ea4e505dd59b440dbc31d329b2d23a07f13208d08f2722ec8`  
		Last Modified: Tue, 03 Dec 2024 04:31:57 GMT  
		Size: 8.4 MB (8370918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:656768068292a4ce12b97911957d6551bcfce4dd51e7a9ba78314f02d626c9f4`  
		Last Modified: Tue, 03 Dec 2024 04:31:57 GMT  
		Size: 18.6 KB (18616 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-jdk-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:15d3a860863778b8b580fa85b92e119b73d9d48f372232b6d285e51c4c6831c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.7 MB (350659865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67067592a590a4269c45d717cca74e1b7e8f146cb5c429301785a5670d4fb711`
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
# Fri, 22 Nov 2024 19:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 22 Nov 2024 19:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 22 Nov 2024 19:48:12 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Nov 2024 19:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 22 Nov 2024 19:48:12 GMT
ENV JAVA_VERSION=24-ea+25
# Fri, 22 Nov 2024 19:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/25/GPL/openjdk-24-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='06d2571c8af4948ac1eaad2b912ab59f320f01744bc4152f3476a65512bb3901'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/25/GPL/openjdk-24-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='022d2edea028f26d0aa8cc933429f305abac8f8a74451095a55b1354f0db7966'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 22 Nov 2024 19:48:12 GMT
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
	-	`sha256:1b36346f77c9f73cfa38f7bc0735ed1a9eff331a137125184bae85bda9e9f722`  
		Last Modified: Mon, 25 Nov 2024 23:29:51 GMT  
		Size: 15.5 MB (15526246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:623dbc3849adf25a226aa6b5eb5662bec74f82bbfb8bf9913f91d774ec85fab0`  
		Last Modified: Mon, 25 Nov 2024 23:29:55 GMT  
		Size: 211.0 MB (210990875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:f75ed7f53e761545cf352ab92a720dd9ddaa94e241092bfc7239fa51cc86412b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8492566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd6c5a830e4ccd766572f5b59b91f84a2b43b81106b9054721f9cc78c903fe47`

```dockerfile
```

-	Layers:
	-	`sha256:589817e2bfcdc579c789ff2b52e266ebf399575419a8e8c96b7a7380c9fcfc18`  
		Last Modified: Mon, 25 Nov 2024 23:29:51 GMT  
		Size: 8.5 MB (8473805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7762b8c84bcfab9b3a1e11191847d649492d00001041501e4d6982bdc38f028`  
		Last Modified: Mon, 25 Nov 2024 23:29:50 GMT  
		Size: 18.8 KB (18761 bytes)  
		MIME: application/vnd.in-toto+json
