## `openjdk:25-ea-9-slim-bullseye`

```console
$ docker pull openjdk@sha256:5db339d9884ce9cca038471e19464ff414023432a3685c4a9c6a7e1fd5332956
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-9-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:9cc23d3543ac53e1f660c28def84ccc3f909e4fff2ccf3fcf763e41ec31c4b98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.6 MB (243605526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0642f5b94472dd8f16f5072245c5272eb1017a73ee919d365c53a573ef3b5000`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Fri, 07 Feb 2025 01:53:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Feb 2025 01:53:06 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 07 Feb 2025 01:53:06 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Feb 2025 01:53:06 GMT
ENV LANG=C.UTF-8
# Fri, 07 Feb 2025 01:53:06 GMT
ENV JAVA_VERSION=25-ea+9
# Fri, 07 Feb 2025 01:53:06 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/9/GPL/openjdk-25-ea+9_linux-x64_bin.tar.gz'; 			downloadSha256='7c57d59eebec0a42a9bca9611b79759eaaeee24f115a9503f4977e5f089eca90'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/9/GPL/openjdk-25-ea+9_linux-aarch64_bin.tar.gz'; 			downloadSha256='7297335988877649a1eebd21261a54e3d96e4f82038766b1a8dfae4fc177ea02'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 07 Feb 2025 01:53:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 01:36:33 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a518575e14cacb01e995f1c96fbe39d340c68954cdd13032d73befb8f2a389ae`  
		Last Modified: Tue, 11 Feb 2025 00:27:58 GMT  
		Size: 1.4 MB (1377186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddbdfecd8642b0346b9d2051af81c367a8112ad0e44cc5845bd61aed66dfe578`  
		Last Modified: Tue, 11 Feb 2025 00:28:02 GMT  
		Size: 212.0 MB (211975752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-9-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:eba70910f7062e7a2b10230042797e3e4e0e72a7f8c8400fada4c3175882a96d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2848602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eb5c9a5355df9e41d2f0c97642cae041bcadca0ce61cbb71cbea62ef4d913ab`

```dockerfile
```

-	Layers:
	-	`sha256:09e733ee70a7cb29efd9bf17db97fc42ae426883ced519a98838fb026f6597ff`  
		Last Modified: Tue, 11 Feb 2025 00:27:58 GMT  
		Size: 2.8 MB (2831045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3831ea8a6846531f78ea7f54f596de152cab11b10bdecc6387b98d498e18374f`  
		Last Modified: Tue, 11 Feb 2025 00:27:58 GMT  
		Size: 17.6 KB (17557 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-9-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:873d380832c4403ceafd510afb0605a987f1e7618e7850b93303c8b5e33f6863
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.1 MB (240050286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ed05d91bf15070e02a034f33809dc664f40ee582471dca36e04cb3d3313ef5e`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1738540800'
# Fri, 07 Feb 2025 01:53:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Feb 2025 01:53:06 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 07 Feb 2025 01:53:06 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Feb 2025 01:53:06 GMT
ENV LANG=C.UTF-8
# Fri, 07 Feb 2025 01:53:06 GMT
ENV JAVA_VERSION=25-ea+9
# Fri, 07 Feb 2025 01:53:06 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/9/GPL/openjdk-25-ea+9_linux-x64_bin.tar.gz'; 			downloadSha256='7c57d59eebec0a42a9bca9611b79759eaaeee24f115a9503f4977e5f089eca90'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/9/GPL/openjdk-25-ea+9_linux-aarch64_bin.tar.gz'; 			downloadSha256='7297335988877649a1eebd21261a54e3d96e4f82038766b1a8dfae4fc177ea02'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 07 Feb 2025 01:53:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9225a2a808e874449ee822a282882a3c331aad2f5093c1062e16494d8bce3e9a`  
		Last Modified: Tue, 04 Feb 2025 01:38:25 GMT  
		Size: 28.7 MB (28744810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0b8342410f5de7992f24293c7ba6dfbca7729223103def73b5319fa46cc62b`  
		Last Modified: Wed, 05 Feb 2025 03:02:01 GMT  
		Size: 1.4 MB (1361282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64a2802eeb58ca588d7b4b4643e676b64f0c8789d36a91d2a69c8df5c079edc`  
		Last Modified: Tue, 11 Feb 2025 00:37:32 GMT  
		Size: 209.9 MB (209944194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-9-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:7de224826cc8548a2ebd0a72a67724d33a21ad5f28044b6945a18b5d4980c4ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2848397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd5ac7184dad2482579e9fcd5670521ee37937423ade702c3c4335a49c30bd15`

```dockerfile
```

-	Layers:
	-	`sha256:1776e50d4d7524cb6ed2d37816657a7db71adbd4c46d85b9ca5604e90f5f2b15`  
		Last Modified: Tue, 11 Feb 2025 00:37:27 GMT  
		Size: 2.8 MB (2830697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e912f6ebab01b669411c43f5a36901ebcd71e286fc6e22625c1e7b400afc78a`  
		Last Modified: Tue, 11 Feb 2025 00:37:26 GMT  
		Size: 17.7 KB (17700 bytes)  
		MIME: application/vnd.in-toto+json
