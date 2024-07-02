## `openjdk:23-ea-29-bookworm`

```console
$ docker pull openjdk@sha256:4f8dd8668dcd9e07cec3ff3fd2a8a2cffa914392161df88183e2ff23b22d295d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:23-ea-29-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:d795dd95069412f5931345c9a844c2ab193876b2c2a49a806a146942c14437c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.1 MB (366113241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15e0c43676baa90b29f1e350324d8b7f3a292e5522aa80de2709b7c78f68a140`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 29 Jun 2024 00:48:10 GMT
ADD file:e8aac9b1598114ead96b4038c19d915b87f662ef342291d69c7e5255c5d731fc in / 
# Sat, 29 Jun 2024 00:48:10 GMT
CMD ["bash"]
# Sat, 29 Jun 2024 00:48:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 29 Jun 2024 00:48:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 29 Jun 2024 00:48:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Jun 2024 00:48:10 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Sat, 29 Jun 2024 00:48:10 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 29 Jun 2024 00:48:10 GMT
ENV LANG=C.UTF-8
# Sat, 29 Jun 2024 00:48:10 GMT
ENV JAVA_VERSION=23-ea+29
# Sat, 29 Jun 2024 00:48:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/29/GPL/openjdk-23-ea+29_linux-x64_bin.tar.gz'; 			downloadSha256='1ecb4977a7385dde5f7155e22cfdad0bec51afb8ff4dece08a061bab64be8aaa'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/29/GPL/openjdk-23-ea+29_linux-aarch64_bin.tar.gz'; 			downloadSha256='a14bddc20e706cf85f28b8cc360e3dc2506b51cff9a0e62125f3213de6c41f00'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 29 Jun 2024 00:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e9aef93137af6e967e7242f3b3c8ecd8e6f571d1e6fdd9e72db0befeeae3cf13`  
		Last Modified: Tue, 02 Jul 2024 01:28:26 GMT  
		Size: 49.6 MB (49554064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b365fa3e8dc16e70d89fab0e91f5242feb38ae3cfeb6655e654209ea109333`  
		Last Modified: Tue, 02 Jul 2024 02:00:17 GMT  
		Size: 24.0 MB (24049794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dbed71fc5444cf6889a21b002de3e7805e810aa88f91a9ca941b4e3880246d1`  
		Last Modified: Tue, 02 Jul 2024 02:00:35 GMT  
		Size: 64.1 MB (64142928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9576ea55d465e58bfdfd398df2ee1d47cc21fbb9d150ef5d84d6052b913637`  
		Last Modified: Tue, 02 Jul 2024 03:21:26 GMT  
		Size: 16.9 MB (16943061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ba1a273e67ae0ceac6e360e4ca02222f4e857c14ef5c95b038de199f493f97`  
		Last Modified: Tue, 02 Jul 2024 03:21:29 GMT  
		Size: 211.4 MB (211423394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-29-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:955d1467a3bceb376d242767822d936627f12c20ecc93d30a4e215a15712ed37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8239621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff2f9230311969409c7021a5e40b0a1bac974327c9a334bcbe6bc8f256ea3507`

```dockerfile
```

-	Layers:
	-	`sha256:b1002383377a6e69e52daf9d5f9a0d7a0e765a2ae1277c94967b54a995cb10b5`  
		Last Modified: Tue, 02 Jul 2024 03:21:26 GMT  
		Size: 8.2 MB (8221158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78791eb0d767109edc371230a3efb72cd9c66b7a9d8bdb4ce15b6391d2795653`  
		Last Modified: Tue, 02 Jul 2024 03:21:26 GMT  
		Size: 18.5 KB (18463 bytes)  
		MIME: application/vnd.in-toto+json
