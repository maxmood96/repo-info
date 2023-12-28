## `openjdk:22-slim-bookworm`

```console
$ docker pull openjdk@sha256:dbc8a4029bbc90fc860732c5774a0b6717765f940eeee97cdb5c2f48411d5c73
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:22-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:653110737c1619d44392858b50a0ca627a6e7b33445e980f2c511eb0f44f19f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236055074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c735019c4e4427d71b3f608aa3045f4081f669618ad31ecb0098e6eb5f2e7cfd`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:27 GMT
ADD file:ac3cd70031d35e46d86b876934946ffc8756de4de065fbc926dce642dac07ff3 in / 
# Tue, 19 Dec 2023 01:20:28 GMT
CMD ["bash"]
# Fri, 22 Dec 2023 01:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 22 Dec 2023 01:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Fri, 22 Dec 2023 01:48:11 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Dec 2023 01:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 22 Dec 2023 01:48:11 GMT
ENV JAVA_VERSION=22-ea+29
# Fri, 22 Dec 2023 01:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/29/GPL/openjdk-22-ea+29_linux-x64_bin.tar.gz'; 			downloadSha256='711a8d0580fa87221146b3c7d3bf1e8fce37b921a71a72989b8396a3fffdb71a'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/29/GPL/openjdk-22-ea+29_linux-aarch64_bin.tar.gz'; 			downloadSha256='bb3edae2765a15fce07581139c8833540021c383cb07492afcd4b130a1eb4810'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 22 Dec 2023 01:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:af107e978371b6cd6339127a05502c5eacd1e6b0e9eb7b2f4aa7b6fc87e2dd81`  
		Last Modified: Tue, 19 Dec 2023 01:24:59 GMT  
		Size: 29.1 MB (29125963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:919bd3551883db178215540ef91b656b6b2c84fbb66d4f843ac664962ad75ca1`  
		Last Modified: Wed, 27 Dec 2023 21:53:40 GMT  
		Size: 4.0 MB (4014761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7760cd777399d4c807f69c44906f4a32bacc77d85e15b412efd1744808949517`  
		Last Modified: Wed, 27 Dec 2023 21:53:44 GMT  
		Size: 202.9 MB (202914350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:170fe8dad28a488c3482573308b4e92f00cd38d0ab739a80549a40fef750c04b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2056529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab0ccbcff2623dc5675f66c3e893c530732b8921958f615b91c3894208b37ff6`

```dockerfile
```

-	Layers:
	-	`sha256:d74649dfa81341f7a52bb336a721bb7874a65cb802f4aabf1e64b81a98908eb5`  
		Last Modified: Wed, 27 Dec 2023 21:53:40 GMT  
		Size: 2.0 MB (2037187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61da689cb4b47bb7cd088b627773436c0bc83c0c560f076ab5314ddec1a2f1b7`  
		Last Modified: Wed, 27 Dec 2023 21:53:40 GMT  
		Size: 19.3 KB (19342 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:22-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:fa9c14aa35fd0b9bbfe9e4dc3a14d90529ce5ee12f5b6afc463da71796def0a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233940005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23ffc27253c388272fafaf682e4b871d6250d0c7022862a55049f2c2ffdba934`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:11 GMT
ADD file:262fd7bf0bc26e5d2a229fba52626e22b8a93beac29733acfc60e716c26e689d in / 
# Tue, 19 Dec 2023 01:41:11 GMT
CMD ["bash"]
# Fri, 22 Dec 2023 01:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 22 Dec 2023 01:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Fri, 22 Dec 2023 01:48:11 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Dec 2023 01:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 22 Dec 2023 01:48:11 GMT
ENV JAVA_VERSION=22-ea+29
# Fri, 22 Dec 2023 01:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/29/GPL/openjdk-22-ea+29_linux-x64_bin.tar.gz'; 			downloadSha256='711a8d0580fa87221146b3c7d3bf1e8fce37b921a71a72989b8396a3fffdb71a'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/29/GPL/openjdk-22-ea+29_linux-aarch64_bin.tar.gz'; 			downloadSha256='bb3edae2765a15fce07581139c8833540021c383cb07492afcd4b130a1eb4810'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 22 Dec 2023 01:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:24e221e92a36ab5b0075dd156b4f2ff095532a9b0927946cf6070bb1bea208b8`  
		Last Modified: Tue, 19 Dec 2023 01:44:38 GMT  
		Size: 29.2 MB (29157269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2614bd11b588c96b15909791ce0a1d4f2faa851a036310cc2fe1b2deae203b7`  
		Last Modified: Wed, 20 Dec 2023 10:22:09 GMT  
		Size: 3.8 MB (3819909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f5fe131808f7ca03b17e49db2ecf5653c014c81691b8412940bc61bc21fdbdc`  
		Last Modified: Thu, 28 Dec 2023 05:07:36 GMT  
		Size: 201.0 MB (200962827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:18ef9f61d50b95fd3869efa814ae4cb8a3e38b804f48f3f182afccc01dc7b3ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2055762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52d45b41cfc08cb3b2ac0a90804d0917465d89bee2e8befd208c46f223bb3be8`

```dockerfile
```

-	Layers:
	-	`sha256:e0ec4672afac3111d21c43ca75e3f8925839eeb69a9f2a3635ab9735425382c4`  
		Last Modified: Thu, 28 Dec 2023 05:07:31 GMT  
		Size: 2.0 MB (2036561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2acc0ce7034038afe94504ee93a666e81734fc3fe0c3336b04eb1c7a42eeaa8d`  
		Last Modified: Thu, 28 Dec 2023 05:07:30 GMT  
		Size: 19.2 KB (19201 bytes)  
		MIME: application/vnd.in-toto+json
