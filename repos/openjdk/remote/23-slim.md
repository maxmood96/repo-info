## `openjdk:23-slim`

```console
$ docker pull openjdk@sha256:36a3f8312057615b3f0e2cd28819b158e96321507fc00a4601fdc907f5723794
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:a3614b639bbcd2bc7929aa7f9f9b1093beb57aac3e91a1045d794aadcd4ccfbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.3 MB (236296540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ca623841096dda09a01ee5147d15dce7630cae32c30fdbf02642d4156102ea3`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:27 GMT
ADD file:ac3cd70031d35e46d86b876934946ffc8756de4de065fbc926dce642dac07ff3 in / 
# Tue, 19 Dec 2023 01:20:28 GMT
CMD ["bash"]
# Fri, 22 Dec 2023 01:54:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 22 Dec 2023 01:54:02 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 22 Dec 2023 01:54:02 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Dec 2023 01:54:02 GMT
ENV LANG=C.UTF-8
# Fri, 22 Dec 2023 01:54:02 GMT
ENV JAVA_VERSION=23-ea+3
# Fri, 22 Dec 2023 01:54:02 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/3/GPL/openjdk-23-ea+3_linux-x64_bin.tar.gz'; 			downloadSha256='9dfa6ea30eef2154e14ec5e38358cc814e1c5a766b1e4f9b4eda8277086defe2'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/3/GPL/openjdk-23-ea+3_linux-aarch64_bin.tar.gz'; 			downloadSha256='52fc0b69ed616eaabc2c5d89fae1654ad188324ca52ece1dfd5f44edf6645410'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 22 Dec 2023 01:54:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:af107e978371b6cd6339127a05502c5eacd1e6b0e9eb7b2f4aa7b6fc87e2dd81`  
		Last Modified: Tue, 19 Dec 2023 01:24:59 GMT  
		Size: 29.1 MB (29125963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0903598dc41725953f3ec2bdeb87f8c5d26034d69422a95b4d2c9ef5497d5a2`  
		Last Modified: Wed, 27 Dec 2023 21:54:03 GMT  
		Size: 4.0 MB (4014842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a09e8f406e9e99c5c5ac8c463e061d2d60d714177ad562c196e5a1fe815245db`  
		Last Modified: Wed, 27 Dec 2023 21:54:06 GMT  
		Size: 203.2 MB (203155735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:6c26f0cb9f78ece2b43f638b8def86134e1cdb28cc4c78d1b28aa74fb37ceab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2056501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89a16f5900bbe63ec682618c0c6666c8f8ad63fc408073d4968aaec2e7b6ac2c`

```dockerfile
```

-	Layers:
	-	`sha256:02462cb83de71453c826f5707cd8530997cc1e32bdfaf51ca1a1c69b0c7a0a60`  
		Last Modified: Wed, 27 Dec 2023 21:54:02 GMT  
		Size: 2.0 MB (2037175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fc51764a5975979d1c648d8d213c09e1e910e454939d91ebe303fc523a1f53d`  
		Last Modified: Wed, 27 Dec 2023 21:54:02 GMT  
		Size: 19.3 KB (19326 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:b4dc73e8aacadd11355b07043d6411508e5e862862f2b460be6feccd6a3d797b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.0 MB (234038661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fac90f6cd0ae85d22228b8b84fbf5256391145fcb9a3bac297e9819c515d77c`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:11 GMT
ADD file:262fd7bf0bc26e5d2a229fba52626e22b8a93beac29733acfc60e716c26e689d in / 
# Tue, 19 Dec 2023 01:41:11 GMT
CMD ["bash"]
# Fri, 22 Dec 2023 01:54:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 22 Dec 2023 01:54:02 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 22 Dec 2023 01:54:02 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Dec 2023 01:54:02 GMT
ENV LANG=C.UTF-8
# Fri, 22 Dec 2023 01:54:02 GMT
ENV JAVA_VERSION=23-ea+3
# Fri, 22 Dec 2023 01:54:02 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/3/GPL/openjdk-23-ea+3_linux-x64_bin.tar.gz'; 			downloadSha256='9dfa6ea30eef2154e14ec5e38358cc814e1c5a766b1e4f9b4eda8277086defe2'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/3/GPL/openjdk-23-ea+3_linux-aarch64_bin.tar.gz'; 			downloadSha256='52fc0b69ed616eaabc2c5d89fae1654ad188324ca52ece1dfd5f44edf6645410'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 22 Dec 2023 01:54:02 GMT
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
	-	`sha256:81884b8bc9c988eb08ac886da10f31394a3fe5acabf79eae6eaa920e51073102`  
		Last Modified: Thu, 28 Dec 2023 05:02:00 GMT  
		Size: 201.1 MB (201061483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:ed7c04f2122f2e73acdb4879fcaa8afd952fc199bb58c468ee3fa5dbf98b3559
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2055739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8b96b2e95c68c7d88649fb23dc11703632d7a33360380a69c4500f2a67eb59d`

```dockerfile
```

-	Layers:
	-	`sha256:27b4f35c4ef80c493d73f91eeba96c27aa199c5b6dbddd64b97287e14b9d38a7`  
		Last Modified: Thu, 28 Dec 2023 05:01:56 GMT  
		Size: 2.0 MB (2036553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a46b80bb761b3c16e6baa204738569a722f408a7e03a18ae0e58a59638dade98`  
		Last Modified: Thu, 28 Dec 2023 05:01:56 GMT  
		Size: 19.2 KB (19186 bytes)  
		MIME: application/vnd.in-toto+json
