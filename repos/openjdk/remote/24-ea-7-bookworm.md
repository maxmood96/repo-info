## `openjdk:24-ea-7-bookworm`

```console
$ docker pull openjdk@sha256:5d3870fe3786e9f93547ec0f4c7a28f8077ca83684528ea1813a73aa9601c7f2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:24-ea-7-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:893dbdf49b263977932fe3a15c4eec6faa0b87fbdb95af12823f9df12ca79733
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.3 MB (366335479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f0e6ecfc3f1fdb2f74397702387a5367b32cb376b6aa14acb94f614dce53fbf`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Jul 2024 01:24:49 GMT
ADD file:e8aac9b1598114ead96b4038c19d915b87f662ef342291d69c7e5255c5d731fc in / 
# Tue, 02 Jul 2024 01:24:50 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:48:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:48:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 20 Jul 2024 00:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 20 Jul 2024 00:52:05 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Sat, 20 Jul 2024 00:52:05 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 20 Jul 2024 00:52:05 GMT
ENV LANG=C.UTF-8
# Sat, 20 Jul 2024 00:52:05 GMT
ENV JAVA_VERSION=24-ea+7
# Sat, 20 Jul 2024 00:52:05 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/7/GPL/openjdk-24-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='d175c4cfc7ab8306b42cf88fe0e60b2b827a2106c026ae6d2a3f2e51bbcb60d0'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/7/GPL/openjdk-24-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='5df46f7b64a38a7a34e1b283f6c37b57f8238567b81c3db0f127f348f4842977'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 20 Jul 2024 00:52:05 GMT
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
	-	`sha256:f09a21e8911d074733a6d3d9d6f2409d30d8ed5e055f06288c148b7ade1194e5`  
		Last Modified: Mon, 22 Jul 2024 21:00:00 GMT  
		Size: 16.9 MB (16943072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc4b384583752e5699d84fea2af72f4dac2a8006142dea5cd6e556edc855796`  
		Last Modified: Mon, 22 Jul 2024 21:00:03 GMT  
		Size: 211.6 MB (211645621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-7-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:2928b3c478f412871814550aa2cdd7f3af4e6e0cc623c9241418a92f795e4699
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8276432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3791606a85d3cd03f0d183a53f8b2700b9749f63608972848a39af94577c7e2b`

```dockerfile
```

-	Layers:
	-	`sha256:cb00f343088fa2ffd667e3db6e6cfb72449e8a9b29888d93cfbbf58a3100136c`  
		Last Modified: Mon, 22 Jul 2024 21:00:00 GMT  
		Size: 8.3 MB (8257986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02669fd07631a47cf1b6c988d78e8b0f1a868aa3e9bf68a20b6ac9b11a23fb6a`  
		Last Modified: Mon, 22 Jul 2024 21:00:00 GMT  
		Size: 18.4 KB (18446 bytes)  
		MIME: application/vnd.in-toto+json
