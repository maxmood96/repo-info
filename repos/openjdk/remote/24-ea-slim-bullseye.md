## `openjdk:24-ea-slim-bullseye`

```console
$ docker pull openjdk@sha256:21cd00bd765727aa0a8730d9b79360715e1d30c932550eb37a8c561957e4021f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:3c28159e4c2aca615b8483db1ee3c89369e2f916fe13c10150c97e0c6a07b0f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.9 MB (244927494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dec7e13ba6d1e4d8c23967816ddabcf7f5c23f66466b61ddbb215325afeb112d`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Jul 2024 05:24:37 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
# Tue, 23 Jul 2024 05:24:38 GMT
CMD ["bash"]
# Sat, 10 Aug 2024 00:48:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 10 Aug 2024 00:48:15 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Sat, 10 Aug 2024 00:48:15 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 10 Aug 2024 00:48:15 GMT
ENV LANG=C.UTF-8
# Sat, 10 Aug 2024 00:48:15 GMT
ENV JAVA_VERSION=24-ea+10
# Sat, 10 Aug 2024 00:48:15 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/10/GPL/openjdk-24-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='b4c878f685a1333de0743bc33fb94a6cbd60e1ddda7e1d88068c2acc1c91012b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/10/GPL/openjdk-24-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='3640a7ecb431e631d5d23e96d0df679fb45cfed38f527a3810caeebebc44a3a5'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 10 Aug 2024 00:48:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227cafba9753648705c523f6319c8bafadf5cd14cb265de661a04076202e9953`  
		Last Modified: Mon, 12 Aug 2024 17:59:17 GMT  
		Size: 1.6 MB (1581789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42b398a4856cdb70fe4e2a281bd1a8b92e17b57bdcf933f0ed25dcfc8eca482a`  
		Last Modified: Mon, 12 Aug 2024 17:59:22 GMT  
		Size: 211.9 MB (211917375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:54f15ca785a51764d55ba00b26a06986ac8f20d4b87ba49d0f59a0b8ab4dad6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2676532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7af5782fae88acf805c966ff54c0776ef4ad79a328c364b9afe8ee7cf5a44bbe`

```dockerfile
```

-	Layers:
	-	`sha256:5ecaabe706e53c894116fab83950eb5f1efb8bcd1883953d6ad05f7d6799c2dc`  
		Last Modified: Mon, 12 Aug 2024 17:59:17 GMT  
		Size: 2.7 MB (2659174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a754988efa3096a944a43528accf360a69218f2013de7f6ef351f1045d360ee5`  
		Last Modified: Mon, 12 Aug 2024 17:59:16 GMT  
		Size: 17.4 KB (17358 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:907ccdfa51380b0ef64b3318e64708fc0800b79283a27926d82dd01b83ac4f28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.4 MB (241405041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55272f49036a810999e6a386f4a5f34bdc077393140d3389eab953cfe075b322`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Jul 2024 04:18:06 GMT
ADD file:3727dfc046704936a0b983a317eeb319ebd0fc5e9da310be06a0ca768df723ec in / 
# Tue, 23 Jul 2024 04:18:07 GMT
CMD ["bash"]
# Sat, 10 Aug 2024 00:48:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 10 Aug 2024 00:48:15 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Sat, 10 Aug 2024 00:48:15 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 10 Aug 2024 00:48:15 GMT
ENV LANG=C.UTF-8
# Sat, 10 Aug 2024 00:48:15 GMT
ENV JAVA_VERSION=24-ea+10
# Sat, 10 Aug 2024 00:48:15 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/10/GPL/openjdk-24-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='b4c878f685a1333de0743bc33fb94a6cbd60e1ddda7e1d88068c2acc1c91012b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/10/GPL/openjdk-24-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='3640a7ecb431e631d5d23e96d0df679fb45cfed38f527a3810caeebebc44a3a5'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 10 Aug 2024 00:48:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bd2a3a2ed82de858b38215fac995414b3a91eea4cfe087e5f853ec1faa989ba4`  
		Last Modified: Tue, 23 Jul 2024 04:21:02 GMT  
		Size: 30.1 MB (30076083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e3bd1e759a916e6497c78e1f9bc18301b82c1d8c089d5cd721ebc3c2f5e7f3f`  
		Last Modified: Mon, 29 Jul 2024 17:01:58 GMT  
		Size: 1.6 MB (1565920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1918cc14546bd6921f977f0988db32c9e6b3e99f7ffc4118fc883feeb90ad9ed`  
		Last Modified: Mon, 12 Aug 2024 18:34:22 GMT  
		Size: 209.8 MB (209763038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:87750bece01c2d996e54f872235178190377f42b4c11452a4ce3fdb2cb18a051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2677141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa692237e45f7aadad488d6bbf9e9004d0388a36027514cc62499510234783ee`

```dockerfile
```

-	Layers:
	-	`sha256:5b556562252402b50baa11084c2f2379eadb2bf4da1374c17dd2f1fe12dc7da7`  
		Last Modified: Mon, 12 Aug 2024 18:34:09 GMT  
		Size: 2.7 MB (2659450 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d06052c6af16988d12be3b63f9b69c0bea34f5b8b401c7c8917fdf7a431ee47d`  
		Last Modified: Mon, 12 Aug 2024 18:34:09 GMT  
		Size: 17.7 KB (17691 bytes)  
		MIME: application/vnd.in-toto+json
