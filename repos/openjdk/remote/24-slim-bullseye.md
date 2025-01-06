## `openjdk:24-slim-bullseye`

```console
$ docker pull openjdk@sha256:e511f740bac12f0aab37fc5e9482f9fab0a0ccfdfa3dbe55ab02c279e328e251
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:a56988ada7347c92acaf76c4fc2a81c26421be299626c12fb9c8196db6998008
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 MB (244535186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c031b10fb02082d4c1173a9aec1ef15e638bbbc603d498b4f76a7122f744d589`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 13 Dec 2024 19:48:13 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
# Fri, 13 Dec 2024 19:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Dec 2024 19:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 13 Dec 2024 19:48:13 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Dec 2024 19:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 19:48:13 GMT
ENV JAVA_VERSION=24-ea+28
# Fri, 13 Dec 2024 19:48:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/28/GPL/openjdk-24-ea+28_linux-x64_bin.tar.gz'; 			downloadSha256='3d1038a0c6dfc0821d81a3995a1ce7225c5c1c97413c38e3ba76aba3562b4192'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/28/GPL/openjdk-24-ea+28_linux-aarch64_bin.tar.gz'; 			downloadSha256='bfc242be61e5de4a8b5a38551bb2d0e17e3308b9e260583cc4db5a54f6c91938'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 13 Dec 2024 19:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6c87eefc1f428634061bcdc9ec95ccceecd7c7475d35a777479af83f64ee6915`  
		Last Modified: Tue, 24 Dec 2024 21:32:32 GMT  
		Size: 30.3 MB (30252643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fae3e01fe4823c5606c9a5f504959356edd990a39e151387a1ece2c86c950fe`  
		Size: 1.4 MB (1377232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8516f2b1ece682a14e91f06745cb4916f315adad7e622aad970830826648ddad`  
		Last Modified: Tue, 24 Dec 2024 22:31:03 GMT  
		Size: 212.9 MB (212905311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:a3e1d7d85095854efffe05a457ab3542e11cc7065ecf18b7b3f40093d2f1bccc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2845492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33779c56a9cd53e03e6e726d322a7c299a6d3986f90f643e95fe75b73eebe528`

```dockerfile
```

-	Layers:
	-	`sha256:a47549d1fa200f3bec56e1d3c90f507208f82ed8a181aa00191ec2a33320dfad`  
		Last Modified: Tue, 24 Dec 2024 22:31:00 GMT  
		Size: 2.8 MB (2827922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c40fac61e7c1e4c66e3c49a7fe709f84bfe6153826839ad1e50ccb0a6ff57213`  
		Last Modified: Tue, 24 Dec 2024 22:31:00 GMT  
		Size: 17.6 KB (17570 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:fd6a84afef6bad4c2688fadd02303bc158f23d16ec53cf17c495bf24a91bad9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.0 MB (240974303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b6772e954578aed3da40f85bca35e80fd7b4168f1d3227701b48b015c7d005b`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 13 Dec 2024 19:48:13 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
# Fri, 13 Dec 2024 19:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Dec 2024 19:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 13 Dec 2024 19:48:13 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Dec 2024 19:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 19:48:13 GMT
ENV JAVA_VERSION=24-ea+28
# Fri, 13 Dec 2024 19:48:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/28/GPL/openjdk-24-ea+28_linux-x64_bin.tar.gz'; 			downloadSha256='3d1038a0c6dfc0821d81a3995a1ce7225c5c1c97413c38e3ba76aba3562b4192'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/28/GPL/openjdk-24-ea+28_linux-aarch64_bin.tar.gz'; 			downloadSha256='bfc242be61e5de4a8b5a38551bb2d0e17e3308b9e260583cc4db5a54f6c91938'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 13 Dec 2024 19:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:879a6187682fc52c69294a2f450abdb54e257a50e8133ec6e89cb140345be6ce`  
		Last Modified: Tue, 24 Dec 2024 21:34:50 GMT  
		Size: 28.7 MB (28744853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:802af25e15e1605893bc7f616bdceb6df54d42569f2584718a22b15a94ff45a7`  
		Last Modified: Wed, 25 Dec 2024 02:34:25 GMT  
		Size: 1.4 MB (1361263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2cb0ec8e06fd92619f4c4215de6f187ec8a9921ac2cc58f12864b880985eeb1`  
		Last Modified: Wed, 25 Dec 2024 02:36:12 GMT  
		Size: 210.9 MB (210868187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:9afa58c26a589d5c459781718c78931bdcb36dd5516311be4958d0c906afc323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2845287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4271fec51d4fdc2b753b07573ca66a82b2dde6033373bcbc2e1259bd0d21519c`

```dockerfile
```

-	Layers:
	-	`sha256:4d60474b41372d12cd564d9fbc7b6ab8c4c5b5472b5da0deb52f3b1b727248fb`  
		Last Modified: Wed, 25 Dec 2024 02:36:07 GMT  
		Size: 2.8 MB (2827574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f13aecbe3181762e5bb360b71bdb9570bd582aadb4c52ab9b43fae484a97343`  
		Last Modified: Wed, 25 Dec 2024 02:36:06 GMT  
		Size: 17.7 KB (17713 bytes)  
		MIME: application/vnd.in-toto+json
