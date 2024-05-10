## `openjdk:23-ea-22-jdk-slim-bullseye`

```console
$ docker pull openjdk@sha256:3e5ff117ceedda209afe2f852f0de976c19db4caa12df31b7fcfb491242f336e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-22-jdk-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:3f4f37dc3fced56d68ee9a74fbfbf626cff3e95bfd20e03c16ce84a251098a9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.9 MB (242877233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec99b7d28739e179042894e890c9b72a572c0b4ade31b7ea41315abcd3e2cb6b`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
CMD ["bash"]
# Thu, 09 May 2024 18:48:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:48:15 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Thu, 09 May 2024 18:48:15 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 May 2024 18:48:15 GMT
ENV LANG=C.UTF-8
# Thu, 09 May 2024 18:48:15 GMT
ENV JAVA_VERSION=23-ea+22
# Thu, 09 May 2024 18:48:15 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/22/GPL/openjdk-23-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='ccc93940dc68c8a0c9bc01591e72321cd694bfb7c70384ed377f0a615cac323b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/22/GPL/openjdk-23-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='9dd3ec5e765c2eaabfc53e02589d00865053269474c8b2c939d8ce00e5f9ad15'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 09 May 2024 18:48:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88b0923b841880c01622c4bbb80792b7c5cc7cadad13a2a747e9e41f618044a2`  
		Last Modified: Fri, 10 May 2024 00:51:44 GMT  
		Size: 1.4 MB (1378077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1500a342a21ac92b6d5fa0c8e450ac2f6b59b24f94fd6c0b68aabaaadeb305b0`  
		Last Modified: Fri, 10 May 2024 00:51:46 GMT  
		Size: 210.1 MB (210064893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-22-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:cbd6d3065ae2953e04262f06e1049d859d157ca2b090a19d24cadb1b19a8b926
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2655965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7551908a2eb529ae8f2ba10394e8c66fafa4f44a0193f31315944ed293e2851c`

```dockerfile
```

-	Layers:
	-	`sha256:fdf6abfa12aabf9c8d7b738561049bf2332f5a401bf97f963a5bd4116dbb8347`  
		Last Modified: Fri, 10 May 2024 00:51:44 GMT  
		Size: 2.6 MB (2638489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80e0e58446eb524da13de4832c781eeda3e3b0f2a4cd34f8e12aed0fb9cdbc93`  
		Last Modified: Fri, 10 May 2024 00:51:44 GMT  
		Size: 17.5 KB (17476 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-22-jdk-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:536cf65aba6e8994cae26c55f32f3b6fcc4728d4d4d48cb1d7c5cb303b8dc1b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.4 MB (239402101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fdb6a9d9ef8d66a4de305040d333610cca8fa500ebe3277d1cfda02cd7ed70a`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:54 GMT
ADD file:e8990741de71fcc1884f30fcd1b6c5ea411bfa752419a82e9748fcd378ca100a in / 
# Wed, 24 Apr 2024 04:10:54 GMT
CMD ["bash"]
# Thu, 09 May 2024 18:48:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:48:15 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Thu, 09 May 2024 18:48:15 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 May 2024 18:48:15 GMT
ENV LANG=C.UTF-8
# Thu, 09 May 2024 18:48:15 GMT
ENV JAVA_VERSION=23-ea+22
# Thu, 09 May 2024 18:48:15 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/22/GPL/openjdk-23-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='ccc93940dc68c8a0c9bc01591e72321cd694bfb7c70384ed377f0a615cac323b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/22/GPL/openjdk-23-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='9dd3ec5e765c2eaabfc53e02589d00865053269474c8b2c939d8ce00e5f9ad15'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 09 May 2024 18:48:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:40a322c395ab3df43e27d8be65cc48139c091588ac868643a02567ca247d0c73`  
		Last Modified: Wed, 24 Apr 2024 04:14:48 GMT  
		Size: 30.1 MB (30087336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de0e1ff5972418c28862eebf600ebc7f9f20a7a6d5c18d60f7e1147fadcb3547`  
		Last Modified: Tue, 07 May 2024 00:23:12 GMT  
		Size: 1.4 MB (1361947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:546478ad633bf7fa5f43aa5bfc334ee96cb34133a938bbcf1435629990b02860`  
		Last Modified: Fri, 10 May 2024 01:18:04 GMT  
		Size: 208.0 MB (207952818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-22-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:7b4bed3ad5e7c2b53af65b764bc8760b74adc6495a9bd7ade5aa02da00dfc9b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2656023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:072574b2662708e79fa9a6a268dd68070044ad8b5f8d492a97a00beccecdcac9`

```dockerfile
```

-	Layers:
	-	`sha256:36e3edcaf27797be6544d371160ac3c4548211c4d3d0d9d6a73d53536ba0ad3e`  
		Last Modified: Fri, 10 May 2024 01:17:59 GMT  
		Size: 2.6 MB (2638700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0922f1e76ff30634de7dcdfbbd4c8bfcecad7add20bec52b61014eaedda424ec`  
		Last Modified: Fri, 10 May 2024 01:17:59 GMT  
		Size: 17.3 KB (17323 bytes)  
		MIME: application/vnd.in-toto+json
