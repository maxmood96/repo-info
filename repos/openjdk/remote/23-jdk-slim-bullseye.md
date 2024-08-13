## `openjdk:23-jdk-slim-bullseye`

```console
$ docker pull openjdk@sha256:1c4c0b9e75d40c7c6c1ddf64165b432a1bacba879b239e74388e13d9d9a02675
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-jdk-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:2bd08e3d2990a8775923dfb3605767ec0dbe04612c9622837b7bccaad90d3eed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 MB (244479264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:878bbcd851f656b9b53307c0a493c7153b5858a8780641f46395cca3e8d2b440`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 09 Aug 2024 18:48:11 GMT
ADD file:8b272f437a81ca538a72714301aab84c945a2ff3829fd205d401f488514d36a9 in / 
# Fri, 09 Aug 2024 18:48:11 GMT
CMD ["bash"]
# Fri, 09 Aug 2024 18:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 09 Aug 2024 18:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 09 Aug 2024 18:48:11 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Aug 2024 18:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 09 Aug 2024 18:48:11 GMT
ENV JAVA_VERSION=23
# Fri, 09 Aug 2024 18:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/36/GPL/openjdk-23_linux-x64_bin.tar.gz'; 			downloadSha256='d8d169ae7a0285e09872565bc3044ad97697d3780e678d2a5ae9f8451c207cfc'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/36/GPL/openjdk-23_linux-aarch64_bin.tar.gz'; 			downloadSha256='5cad336e22d64a4a578f59d089223c226d67455c410cbaeb91f5fa0503ce2f96'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 09 Aug 2024 18:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:82aabceedc2fbf89030cbb4ff98215b70d9ae35c780ade6c784d9b447b1109ed`  
		Last Modified: Tue, 13 Aug 2024 00:24:25 GMT  
		Size: 31.4 MB (31428287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a10665d949f89f9347cfb06c24817ee01d1f467a7076b2f9e7ea333d230492`  
		Last Modified: Tue, 13 Aug 2024 01:12:51 GMT  
		Size: 1.6 MB (1581786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d4ea508435a6c04fa30f59e3451cc8d83d397f848510867e2c2b8f1f5b5c3d`  
		Last Modified: Tue, 13 Aug 2024 01:12:57 GMT  
		Size: 211.5 MB (211469191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:95bd8ddf2feeb165a628a6ac85d2c2069e20d16f9842e240dcba4dc414cf7004
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2675244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57bdbc680c33a40da1565eda9422eddb2b8bd79bb5a9e1db619a900deead1919`

```dockerfile
```

-	Layers:
	-	`sha256:ad8fabdb05d4cfe33d355dd2257442896af1defb814dd2a50cdf283a0aa4c2b8`  
		Last Modified: Tue, 13 Aug 2024 01:12:51 GMT  
		Size: 2.7 MB (2658490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e784d7311f1d26216fff3d11258214532d034a07e60481047d1ded899ec3adb`  
		Last Modified: Tue, 13 Aug 2024 01:12:51 GMT  
		Size: 16.8 KB (16754 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-jdk-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:4b2ec903914b60d83c24f20f3ebba3fe597391c9f5ac15d5d3fa41afecdc7605
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.0 MB (240981510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54141529cd6f781589a5890a40bbdf23ccd18884c38704fdb516ab80ab30420f`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Jul 2024 04:18:06 GMT
ADD file:3727dfc046704936a0b983a317eeb319ebd0fc5e9da310be06a0ca768df723ec in / 
# Tue, 23 Jul 2024 04:18:07 GMT
CMD ["bash"]
# Fri, 09 Aug 2024 18:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 09 Aug 2024 18:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 09 Aug 2024 18:48:11 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Aug 2024 18:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 09 Aug 2024 18:48:11 GMT
ENV JAVA_VERSION=23
# Fri, 09 Aug 2024 18:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/36/GPL/openjdk-23_linux-x64_bin.tar.gz'; 			downloadSha256='d8d169ae7a0285e09872565bc3044ad97697d3780e678d2a5ae9f8451c207cfc'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/36/GPL/openjdk-23_linux-aarch64_bin.tar.gz'; 			downloadSha256='5cad336e22d64a4a578f59d089223c226d67455c410cbaeb91f5fa0503ce2f96'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 09 Aug 2024 18:48:11 GMT
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
	-	`sha256:8198a129b1f55637bf94f4181f52bd1b538be2efb087bd0428bf8b5b6aedc05d`  
		Last Modified: Mon, 12 Aug 2024 18:39:37 GMT  
		Size: 209.3 MB (209339507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:42b5b996726204c64063b8e315e61d4b96bcdc3be10b3028e1fa629a8a388ba0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2675805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d92522535dc79078e610456060c3d23b29a53da11453c93690cf1589822ce700`

```dockerfile
```

-	Layers:
	-	`sha256:37933bb0bce91aa808ddf97b00f66dce3f95545dad60b8e91012a3781c3ed78c`  
		Last Modified: Mon, 12 Aug 2024 18:39:33 GMT  
		Size: 2.7 MB (2658742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b51dc704f0fe9a9766b88514009e36188d02a8ba2c50986ebe8d2b6de4fda69`  
		Last Modified: Mon, 12 Aug 2024 18:39:32 GMT  
		Size: 17.1 KB (17063 bytes)  
		MIME: application/vnd.in-toto+json
