## `openjdk:24-jdk-slim-bullseye`

```console
$ docker pull openjdk@sha256:27b3070e6ca4d4985a96ebb50607cbfa687f7f324dc4383f755c9fe381d3d8d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-jdk-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:e31fa3330210af5a027eeb9d5eb07e7ed4c6ae22f0f13fd594f40c921d07c261
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.9 MB (244927459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b438da8a81a1669da791c6e849024fad36b0a29354ebbbfef7bb4c1de09e9ad`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 10 Aug 2024 00:48:15 GMT
ADD file:8b272f437a81ca538a72714301aab84c945a2ff3829fd205d401f488514d36a9 in / 
# Sat, 10 Aug 2024 00:48:15 GMT
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
	-	`sha256:82aabceedc2fbf89030cbb4ff98215b70d9ae35c780ade6c784d9b447b1109ed`  
		Last Modified: Tue, 13 Aug 2024 00:24:25 GMT  
		Size: 31.4 MB (31428287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e2552edb3f71b7339b9f0b93b8aead9266c93d0f82bfc83e10a6cbfe2f62d8d`  
		Last Modified: Tue, 13 Aug 2024 01:12:26 GMT  
		Size: 1.6 MB (1581742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b9a113ca17be719eac6fe67d30e9d684a163feb061d743231b5197cc492776`  
		Last Modified: Tue, 13 Aug 2024 01:12:30 GMT  
		Size: 211.9 MB (211917430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:27cff099895fe2a6d471ef7f8af2bca9845524ce3be2d4969900f056032f0c6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2676532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66db5be95fbb4717dc49f9dff1aed9a3b4f89904eb1c3da8252abc7522c27605`

```dockerfile
```

-	Layers:
	-	`sha256:5196d111eb98390ef858365d71a626198b01776dfcbf59318b2a80167bf6b7ac`  
		Last Modified: Tue, 13 Aug 2024 01:12:26 GMT  
		Size: 2.7 MB (2659174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b4fbc729cfa22a925208cd510fc06c38f33d65448c533a072339b20616a9c00`  
		Last Modified: Tue, 13 Aug 2024 01:12:26 GMT  
		Size: 17.4 KB (17358 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-jdk-slim-bullseye` - linux; arm64 variant v8

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

### `openjdk:24-jdk-slim-bullseye` - unknown; unknown

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
