## `openjdk:24-bullseye`

```console
$ docker pull openjdk@sha256:2bcb491b85ac409e5dedb30ae361a1773e6f5e50540b5e75e06ab9a2b5dd0070
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:4bf458edfa34ce83aa37325a5703b3be8fc407da355c1df0d144824ab8645dbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.0 MB (350965908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87fa949c9b0acc3a9217ac573d1b98a8bb1b359181dfedba64a95e8601ad3036`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Dec 2024 01:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Dec 2024 01:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Sat, 07 Dec 2024 01:48:13 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Dec 2024 01:48:13 GMT
ENV LANG=C.UTF-8
# Sat, 07 Dec 2024 01:48:13 GMT
ENV JAVA_VERSION=24-ea+27
# Sat, 07 Dec 2024 01:48:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/27/GPL/openjdk-24-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='99196f78561dace922e06c52af4d33157ded8ae02a8009f35ea2fb7075dda452'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/27/GPL/openjdk-24-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='e78b5c2b599fd835fb88bfe9155b27e16dfcab3e0488bb63051c073acabd5cba'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 07 Dec 2024 01:48:13 GMT
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
	-	`sha256:ba51e6df45f82201ea5f2097edaabefe20afd99bedd7a623cf36de7af5af405e`  
		Last Modified: Mon, 09 Dec 2024 23:30:37 GMT  
		Size: 14.1 MB (14071361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b078d43b55a82a26db885a1d5e01e0d19365a962e12706519f9c0421ec8949c`  
		Last Modified: Mon, 09 Dec 2024 23:30:39 GMT  
		Size: 212.8 MB (212843041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:e374f858bc51b292a0d122cca265d4ce2a363e389d9c59f371b06221aabdc5ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8394623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c666f3dac30b06ea7e03f908a449a4af2010a9521bfc8750826de425ef3164d5`

```dockerfile
```

-	Layers:
	-	`sha256:900761699df14ab66ecc72f588667e18c65757318b58e22f31cc81e613c5546f`  
		Last Modified: Mon, 09 Dec 2024 23:30:37 GMT  
		Size: 8.4 MB (8376005 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b28bce4665823dfd059c9c2051843c9bb84e0b3b6681738e639fdb06e6f20a2`  
		Last Modified: Mon, 09 Dec 2024 23:30:37 GMT  
		Size: 18.6 KB (18618 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:1bffb06879699de1066ad317dcc8abec8dd323f388d7dc4c3e5a06d691a26450
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.0 MB (348964433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a76968e58c8a7886cb0aa8b06e37244252e2fa15bf328a9f2b4f18c806a34a79`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Dec 2024 01:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Dec 2024 01:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Sat, 07 Dec 2024 01:48:13 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Dec 2024 01:48:13 GMT
ENV LANG=C.UTF-8
# Sat, 07 Dec 2024 01:48:13 GMT
ENV JAVA_VERSION=24-ea+27
# Sat, 07 Dec 2024 01:48:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/27/GPL/openjdk-24-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='99196f78561dace922e06c52af4d33157ded8ae02a8009f35ea2fb7075dda452'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/27/GPL/openjdk-24-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='e78b5c2b599fd835fb88bfe9155b27e16dfcab3e0488bb63051c073acabd5cba'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 07 Dec 2024 01:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e357e1f94476a03fde298261e8c007d487d3cfade45a9eef064eba724a5c5e2e`  
		Last Modified: Tue, 03 Dec 2024 01:30:26 GMT  
		Size: 52.2 MB (52245994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b2279cee7374c65ae079e8ccdceeeb8b20c07ffc727e5b7cd595285b44a3a0`  
		Last Modified: Tue, 03 Dec 2024 05:39:10 GMT  
		Size: 15.5 MB (15544048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2749caeb5baae1b5e6316a6f02e57835aa548497fba6792be844c743a57c72a2`  
		Last Modified: Tue, 03 Dec 2024 11:51:00 GMT  
		Size: 54.9 MB (54852316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72075f2e4bb2192408955026a169695446c09e734ec8d71fd14ded7b9b67ab5c`  
		Last Modified: Tue, 10 Dec 2024 01:30:44 GMT  
		Size: 15.5 MB (15526199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24bdf4134f25ae02a478118d0974a37b75faf4bbcc0e6d7ea24a7f02540ac6e3`  
		Last Modified: Tue, 10 Dec 2024 01:35:34 GMT  
		Size: 210.8 MB (210795876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:9ed807771791d342586bebfd39d119d560ccca935fb4566f359894d3a40dbae2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8495850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b00772296f0b8cb0810387d2d4c5e1145d6b8ca8e63454a4d7ac0e7528cc511`

```dockerfile
```

-	Layers:
	-	`sha256:da9daf312e2f43fbd6bde0ceac5fb54580dc21d2fdb0f943b7768afd85d09dff`  
		Last Modified: Tue, 10 Dec 2024 01:35:29 GMT  
		Size: 8.5 MB (8477089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9f68d97cdad33202a4f3b968357af98306c6e50536ef6bc37f6389857f200b0`  
		Last Modified: Tue, 10 Dec 2024 01:35:28 GMT  
		Size: 18.8 KB (18761 bytes)  
		MIME: application/vnd.in-toto+json
