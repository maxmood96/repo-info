## `openjdk:23-slim-bullseye`

```console
$ docker pull openjdk@sha256:3eb0001a663a50bb67534e10021e81e552e7e1a5adbaed9f910e98136e74456f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:753a162e7a63eb6c691202d6c8f2a4ef9415cc0c8c57f94863e0829b6043525b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.0 MB (236020947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a11da753fac94a04191ad51f3113d5f9adff4d243e41ccadf30d9a1d4cd6be35`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Tue, 23 Jan 2024 20:18:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jan 2024 20:18:23 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Tue, 23 Jan 2024 20:18:23 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Jan 2024 20:18:23 GMT
ENV LANG=C.UTF-8
# Tue, 23 Jan 2024 20:18:23 GMT
ENV JAVA_VERSION=23-ea+6
# Tue, 23 Jan 2024 20:18:23 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/6/GPL/openjdk-23-ea+6_linux-x64_bin.tar.gz'; 			downloadSha256='5163a8a077bfb1cb60e6b4ade06959b0ecba73399a509a5e83f8f9df5cebd140'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/6/GPL/openjdk-23-ea+6_linux-aarch64_bin.tar.gz'; 			downloadSha256='aa7e954bb29a17c5d0095c4ce94275bfe53383cb8aa7f14894d352e9c00110c8'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 23 Jan 2024 20:18:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dc7f2c1c12751383df0f6d1e863ad3a69c2d4ed93417d267323f489e94745a9`  
		Last Modified: Wed, 24 Jan 2024 20:50:03 GMT  
		Size: 1.4 MB (1378089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ddce7a46c0c97389847567d695ddcf21458122ee13c6d6c6f5b2e0306a1dd11`  
		Last Modified: Wed, 24 Jan 2024 20:50:06 GMT  
		Size: 203.2 MB (203224903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:c31f9d1dd6c36db08e913bbe1657e3399081216a57281a363df0ca34e0926d59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2207640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:737ee7a1fdc7626171ab880261d0279044f0787b0a52bc1edbac95b0ff012c1d`

```dockerfile
```

-	Layers:
	-	`sha256:1d32353bf81273187539635c8750acce5362863db46378f24f9ed340c4302b34`  
		Last Modified: Wed, 24 Jan 2024 20:50:03 GMT  
		Size: 2.2 MB (2190181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:184ebbe28f02edbbff6346c96d1f8bae01ff7505e2246d4beec25968c8b57fa7`  
		Last Modified: Wed, 24 Jan 2024 20:50:03 GMT  
		Size: 17.5 KB (17459 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:8f624149f08b396273599bb3d6cbea05270e7ca5aaab75269a1de45c9f28d0bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.6 MB (232562084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:315749fcd4825441c506304938b981005980953b6005e2542df3398d83d7f8d2`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 02:00:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jan 2024 02:00:35 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 12 Jan 2024 02:00:35 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jan 2024 02:00:35 GMT
ENV LANG=C.UTF-8
# Fri, 12 Jan 2024 02:00:35 GMT
ENV JAVA_VERSION=23-ea+5
# Fri, 12 Jan 2024 02:00:35 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/5/GPL/openjdk-23-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='ccf927cccbf0ae655b04e2da009aa13811e971f214fee242acd46ca2b5d9ed63'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/5/GPL/openjdk-23-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='acfc5986d442c5c3c3d622e774e0bc9cce3763f485a9a3b71a46a93a3f703d81'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 12 Jan 2024 02:00:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864f90b8981b087545e440102e5efeb70861aaadc2193e6caa6a685b8ddd18f2`  
		Last Modified: Fri, 12 Jan 2024 09:23:32 GMT  
		Size: 1.4 MB (1361926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03023fe357acfd34ca07adc3d484eb7cc7706653c080aacc1c28b76b2d231fcf`  
		Last Modified: Sat, 13 Jan 2024 01:42:27 GMT  
		Size: 201.1 MB (201136148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:387e6be50ac74121b0f340a37e499cdbd6d51639df400b35dd88c59dfd8b977b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2206848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeccc99f970e83ca29c7e14d6d0af7ba1f30b4e3db5088fde3264d6f11810d50`

```dockerfile
```

-	Layers:
	-	`sha256:d5d1defb763f4e6ff14cec6696031bb74806a7d91f12b1d233ec37210c24594e`  
		Last Modified: Sat, 13 Jan 2024 01:42:22 GMT  
		Size: 2.2 MB (2189543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c47d202583613633621e7a0c034effd391afb740c0da5f8dd29d0c490a6b3ebb`  
		Last Modified: Sat, 13 Jan 2024 01:42:22 GMT  
		Size: 17.3 KB (17305 bytes)  
		MIME: application/vnd.in-toto+json
