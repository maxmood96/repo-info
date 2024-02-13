## `openjdk:22-bookworm`

```console
$ docker pull openjdk@sha256:15103cdc21cc7e48a9b6fba4ac67fefa15b3f394e2e132c3903e009cad9d3d54
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:22-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:47dd77d6bb4d2fda7094444aba9fc7082bcea915039fc8cd756477538a975518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.6 MB (357564085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:161e071053e88b6fd1bb0a592f29f7aa685798fa8529f3dbe76c3e7cce4147ef`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 09 Feb 2024 19:48:12 GMT
ADD file:333b899a197a48b3333115a3b59efed559494808873943f606a9bc2b6e242c49 in / 
# Fri, 09 Feb 2024 19:48:12 GMT
CMD ["bash"]
# Fri, 09 Feb 2024 19:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 09 Feb 2024 19:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 09 Feb 2024 19:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 09 Feb 2024 19:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Fri, 09 Feb 2024 19:48:12 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Feb 2024 19:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 09 Feb 2024 19:48:12 GMT
ENV JAVA_VERSION=22
# Fri, 09 Feb 2024 19:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/35/GPL/openjdk-22_linux-x64_bin.tar.gz'; 			downloadSha256='37b0e1d93e9b6478824c21753f2e8445c8caad885a2245f393b35658be1695b3'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/35/GPL/openjdk-22_linux-aarch64_bin.tar.gz'; 			downloadSha256='5bc8c3ea634bf3be8a275c789dabbaa3e68eb639ee920b6fbce1b2236082086d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 09 Feb 2024 19:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7bb465c2914923b08ae03b7fc67b92a1ef9b09c4c1eb9d6711b22ee6bbb46a00`  
		Last Modified: Tue, 13 Feb 2024 00:41:39 GMT  
		Size: 49.6 MB (49552605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9b41aaa3c52ab268b47da303015b94ced04a1eb02e58860e58b283404974f4`  
		Last Modified: Tue, 13 Feb 2024 01:30:39 GMT  
		Size: 24.0 MB (24046577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49b40be4436eff6fe463f6977159dc727df37cabe65ade75c75c1caa3cb0a234`  
		Last Modified: Tue, 13 Feb 2024 01:30:58 GMT  
		Size: 64.1 MB (64140328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e1ca1e8689db4396f2ddb220565fd09f527b91a2a6364baa39669d6c679a6e1`  
		Last Modified: Tue, 13 Feb 2024 02:58:13 GMT  
		Size: 16.9 MB (16945618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e505d4e94bdd3c1ed5913cdbdfc8d21e42e7c41568e230c2f073a2e08af2c51`  
		Last Modified: Tue, 13 Feb 2024 02:58:17 GMT  
		Size: 202.9 MB (202878957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:bf094f96363af524399e20a3b3f0621eba6f9ac50ded859c83a9d64965745789
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7134070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53efc460b08bc283af44fdf32ba4bd3cad2ec05dcd80b5356ab3ec9f8c25cae2`

```dockerfile
```

-	Layers:
	-	`sha256:39aca2a6cc387a552629a6cd9d6e642a3b3a226922f524141194b07cf892567b`  
		Last Modified: Tue, 13 Feb 2024 02:58:13 GMT  
		Size: 7.1 MB (7115751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92cf0615029cce762ca678bf766790986a6fca87bc835b98fe2bd01af9ca37c8`  
		Last Modified: Tue, 13 Feb 2024 02:58:13 GMT  
		Size: 18.3 KB (18319 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:22-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:3defc9a71978968491345254ce6e3a30f628f6ffe7b37aba15734cc9277c3de5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.9 MB (355862158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6920dc9076720f4021bed56ac3e4507ab71b7078eca4ecdc9b708a4f03e017f`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:15 GMT
ADD file:8bc7f537dd3dc4b92ec9006080fd563cc79205ee1ec3f456d03e869125a5bc21 in / 
# Wed, 31 Jan 2024 22:44:15 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:42:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:43:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 09 Feb 2024 19:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 09 Feb 2024 19:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Fri, 09 Feb 2024 19:48:12 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Feb 2024 19:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 09 Feb 2024 19:48:12 GMT
ENV JAVA_VERSION=22
# Fri, 09 Feb 2024 19:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/35/GPL/openjdk-22_linux-x64_bin.tar.gz'; 			downloadSha256='37b0e1d93e9b6478824c21753f2e8445c8caad885a2245f393b35658be1695b3'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/35/GPL/openjdk-22_linux-aarch64_bin.tar.gz'; 			downloadSha256='5bc8c3ea634bf3be8a275c789dabbaa3e68eb639ee920b6fbce1b2236082086d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 09 Feb 2024 19:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:66932e2b787d33a94ee3eb8b489be6e6838b29f5c1d732262da306da9b1f2eed`  
		Last Modified: Wed, 31 Jan 2024 22:47:40 GMT  
		Size: 49.6 MB (49615296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4afa7e263db1a3a05a9f31906dee83c0ef41151669759a3362e724b2765fd66f`  
		Last Modified: Wed, 31 Jan 2024 23:52:05 GMT  
		Size: 23.6 MB (23586448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c812910e5e62436c8483e793d1956d1c70bcf42d20d5f0885ddafbe0ba124459`  
		Last Modified: Wed, 31 Jan 2024 23:52:23 GMT  
		Size: 64.0 MB (63994808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a5985ce67cc9b5be13bbd1d05bdaef8d5b3eef2c56ba38018645982e475f95a`  
		Last Modified: Fri, 02 Feb 2024 14:12:30 GMT  
		Size: 17.7 MB (17732244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77275f958b63d96bb4e1cabb335c1c02c1ae60dd5c1faf4e58d1081dbd5e0f8`  
		Last Modified: Tue, 13 Feb 2024 00:32:46 GMT  
		Size: 200.9 MB (200933362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:102aa6fef1148b4da96a23d01ef8e1c5eb1842b7494e50a3a0ccf2fa8dff3190
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7253319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da035957f96ab9e8b5bdda356de96ae0f4842ee9358ab824175fd3cd01390197`

```dockerfile
```

-	Layers:
	-	`sha256:476343cd045c8601f9898b65eeec59ba8216e209318a01ce01b54dbfeae6928d`  
		Last Modified: Tue, 13 Feb 2024 00:32:41 GMT  
		Size: 7.2 MB (7235487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09bd38fd38b6f428207300db30d2b3a990126f6d133a8d61c20e49acc2281a0f`  
		Last Modified: Tue, 13 Feb 2024 00:32:41 GMT  
		Size: 17.8 KB (17832 bytes)  
		MIME: application/vnd.in-toto+json
