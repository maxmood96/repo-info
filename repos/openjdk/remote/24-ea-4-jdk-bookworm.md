## `openjdk:24-ea-4-jdk-bookworm`

```console
$ docker pull openjdk@sha256:1a1cfee94b46b6cf5a309859018a0f1e4e08c56f54dffaf7af37b9ef737d97a6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:24-ea-4-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:8ef71455697d8fb8942a432a62076a6a858b6b880dd40a5594777ac3f36ed5ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.1 MB (366114917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59bcff92cd5ec719be233783a6c06b0b851be69d02044e2bde170b6e3f74146b`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 29 Jun 2024 00:52:17 GMT
ADD file:e8aac9b1598114ead96b4038c19d915b87f662ef342291d69c7e5255c5d731fc in / 
# Sat, 29 Jun 2024 00:52:17 GMT
CMD ["bash"]
# Sat, 29 Jun 2024 00:52:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 29 Jun 2024 00:52:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 29 Jun 2024 00:52:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Jun 2024 00:52:17 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Sat, 29 Jun 2024 00:52:17 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 29 Jun 2024 00:52:17 GMT
ENV LANG=C.UTF-8
# Sat, 29 Jun 2024 00:52:17 GMT
ENV JAVA_VERSION=24-ea+4
# Sat, 29 Jun 2024 00:52:17 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/4/GPL/openjdk-24-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='64aa493b28493a2d223626bdad774640cb148b0d52f392b081b2776532a980a0'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/4/GPL/openjdk-24-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='3d0b65f191528ab241b4e238568e52fa7199975b4f4b7badcf58a279b1fac426'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 29 Jun 2024 00:52:17 GMT
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
	-	`sha256:c249213bdd88c87abb8ec7d6bc2d08c4a34ef6314552228171a50edb410617c6`  
		Last Modified: Tue, 02 Jul 2024 03:21:16 GMT  
		Size: 16.9 MB (16943005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c03091424074362eaf389bca7f8a45e1114232cf25663ecb21646d492475ad`  
		Last Modified: Tue, 02 Jul 2024 03:21:19 GMT  
		Size: 211.4 MB (211425126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-4-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:d1ec3515ab7693446cf17273863660141307d6a9ddadea441c4c42c2420bcb19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8239596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8819d2e97d1adef9b845b4e579c71e68920c518213b56ccaa363468a34ddf9a3`

```dockerfile
```

-	Layers:
	-	`sha256:f7e77a329d5c2b029ce96febee70a4a77e27fd14c36538f16b9c859c2d8e3aec`  
		Last Modified: Tue, 02 Jul 2024 03:21:16 GMT  
		Size: 8.2 MB (8221150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c15d62e291db53823d3ad73de348c58d05f3c87aef25154c56e2a3f6d110235d`  
		Last Modified: Tue, 02 Jul 2024 03:21:16 GMT  
		Size: 18.4 KB (18446 bytes)  
		MIME: application/vnd.in-toto+json
