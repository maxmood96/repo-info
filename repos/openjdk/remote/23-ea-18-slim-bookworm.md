## `openjdk:23-ea-18-slim-bookworm`

```console
$ docker pull openjdk@sha256:29384a4bd799cdbd82d4f8c61ab692f6ba78fdc7f5a6fe301b35f49fb742262e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-18-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:995d3b8c0fed76f33c6a5ea1c86d0a4b69bebfaa631ea962d10653c9b7e3afe5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244167733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09985ac1555a189f8cb4f7cda988bde0e3292be6d0e2bba1391378e37ce00da3`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:48 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
# Wed, 10 Apr 2024 01:50:48 GMT
CMD ["bash"]
# Fri, 12 Apr 2024 18:48:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Apr 2024 18:48:10 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 12 Apr 2024 18:48:10 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 18:48:10 GMT
ENV LANG=C.UTF-8
# Fri, 12 Apr 2024 18:48:10 GMT
ENV JAVA_VERSION=23-ea+18
# Fri, 12 Apr 2024 18:48:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/18/GPL/openjdk-23-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='618c320c28c4d2d71fd5a366876b5f9ef8cf16819e9793e7d960ecea1caf9d5d'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/18/GPL/openjdk-23-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='aecde065716b2226217e12905a714da37b06daca526e77821a55d09eab1b5489'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 12 Apr 2024 18:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d968fdf50e420e0f4ea406a31e00ee2d9e96c3f786e712b1c439357431822b`  
		Last Modified: Mon, 15 Apr 2024 17:50:44 GMT  
		Size: 4.0 MB (4015009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06cbadb3740bae5e49ad18ca5bac9284ea408598826884771cd8028207c70b4c`  
		Last Modified: Mon, 15 Apr 2024 17:50:47 GMT  
		Size: 211.0 MB (211021366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-18-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:7bf225ce1bc07a7eefc31f416bb01f729a16627a3006fcef384df2a413a21ef0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2365564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c4c0196012f63af12864a8e82e18e293dc48c06687c2d63e3aec2507409f4ed`

```dockerfile
```

-	Layers:
	-	`sha256:461c2588bbe961f0909dab4bde410c710196c40cf34654bbb7fcb03bcae75127`  
		Last Modified: Mon, 15 Apr 2024 17:50:44 GMT  
		Size: 2.3 MB (2346220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13c829a2a46c2477f55fce1b9b454b80ff865540ed879e447bc2df518433fca6`  
		Last Modified: Mon, 15 Apr 2024 17:50:44 GMT  
		Size: 19.3 KB (19344 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-18-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:17dfdd33924acd0dd47e02f084e095e178a7c22e40d8e9e9897f460a1f3c9c6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.9 MB (241890574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95da71e38d0b0b4eff61368552175ed2aed7534ca7dd4a5cd7a696ff14d81fc0`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:23 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
# Wed, 10 Apr 2024 00:40:23 GMT
CMD ["bash"]
# Fri, 12 Apr 2024 18:48:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Apr 2024 18:48:10 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 12 Apr 2024 18:48:10 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 18:48:10 GMT
ENV LANG=C.UTF-8
# Fri, 12 Apr 2024 18:48:10 GMT
ENV JAVA_VERSION=23-ea+18
# Fri, 12 Apr 2024 18:48:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/18/GPL/openjdk-23-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='618c320c28c4d2d71fd5a366876b5f9ef8cf16819e9793e7d960ecea1caf9d5d'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/18/GPL/openjdk-23-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='aecde065716b2226217e12905a714da37b06daca526e77821a55d09eab1b5489'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 12 Apr 2024 18:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:231b1ea269ca1003ddaff994cead172b326871cafa79e4d1bf87d9dda8d12bb4`  
		Last Modified: Wed, 10 Apr 2024 16:59:21 GMT  
		Size: 3.8 MB (3820125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181a3c9f92d767ab432490c0dc5fa182545b8bf6a8f82fbb5678bc5ae694feef`  
		Last Modified: Mon, 15 Apr 2024 20:22:19 GMT  
		Size: 208.9 MB (208908292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-18-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:0d89e135ace6d419e9e830a8b7d2207e10ae169129cbde87ac7aa5dcdc122572
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2364691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cd84bac3751768f56032150bd2331f1e0611bcb226246ada871422571f8e362`

```dockerfile
```

-	Layers:
	-	`sha256:cf8d7fa10b1b07fdd5608eec857cfa7a0bce8c638e35593d21610d5701ac0b82`  
		Last Modified: Mon, 15 Apr 2024 20:22:15 GMT  
		Size: 2.3 MB (2345488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65f5d5603556ab363efbfa3c34d220fe79cbdea85bf1b74b1cf6c802e8b6ab21`  
		Last Modified: Mon, 15 Apr 2024 20:22:14 GMT  
		Size: 19.2 KB (19203 bytes)  
		MIME: application/vnd.in-toto+json
