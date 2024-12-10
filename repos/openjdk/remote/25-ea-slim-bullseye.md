## `openjdk:25-ea-slim-bullseye`

```console
$ docker pull openjdk@sha256:ca40be70d8d8a64027efd327583dfb14004fe40e1770b29156bf948aedc6148a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:a817cb8482469591134cac1613b86004240e53b5972f6ddaf557c9dcc6ab730d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.7 MB (244650927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24750ff6f077bfa345d89691ededf31a05f318f8bdf6811f8502f2df9d8549ae`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Mon, 09 Dec 2024 05:52:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 05:52:24 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Mon, 09 Dec 2024 05:52:24 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 05:52:24 GMT
ENV LANG=C.UTF-8
# Mon, 09 Dec 2024 05:52:24 GMT
ENV JAVA_VERSION=25-ea+1
# Mon, 09 Dec 2024 05:52:24 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/1/GPL/openjdk-25-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='b2c1c3716a21ae204e31e0f37782552ffef0f6e0d9850ba16fb57cd0fa98d84c'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/1/GPL/openjdk-25-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='76761c3ad2bebc865c5ed4ce08a7c5f89eb4f51d3f471d76f650e0556d79daa3'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 09 Dec 2024 05:52:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057068157e352cf32e8ed257353c687267e924f6243a7d36498c3e0dc361b0db`  
		Last Modified: Mon, 09 Dec 2024 23:30:36 GMT  
		Size: 1.4 MB (1377271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e3d832b59088f74304cc137fb8a2f5484ba54bbe4ef67c8c2181be1de0160a`  
		Last Modified: Mon, 09 Dec 2024 23:30:40 GMT  
		Size: 213.0 MB (213021012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:ba36f09dac0c1439d7f739aa45c51a0d0ac08ff331f4fb3da2dc0ccb35afba94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2848424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eb225ae009033884474726d2d8a2dee0dfdc84d85a820f290107ee7af0bb587`

```dockerfile
```

-	Layers:
	-	`sha256:ec3f0fc8b60425cd0e37ad324c063094b7daecdb78f189bda7b44360167cf89c`  
		Last Modified: Mon, 09 Dec 2024 23:30:36 GMT  
		Size: 2.8 MB (2830867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76b281050c744be473a5895aa2c4fca9c364e5cf6bea038ade843f2901889e22`  
		Last Modified: Mon, 09 Dec 2024 23:30:36 GMT  
		Size: 17.6 KB (17557 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:78807d194d61f0ff9558ae7535af7f322c66938a053faaa134a98ce4fb8cc3d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.1 MB (241071888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a428fcc7754420a052d9f0068fc1e125e0197159d85f1b878ec5b14843d3aec`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Mon, 09 Dec 2024 05:52:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 05:52:24 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Mon, 09 Dec 2024 05:52:24 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 05:52:24 GMT
ENV LANG=C.UTF-8
# Mon, 09 Dec 2024 05:52:24 GMT
ENV JAVA_VERSION=25-ea+1
# Mon, 09 Dec 2024 05:52:24 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/1/GPL/openjdk-25-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='b2c1c3716a21ae204e31e0f37782552ffef0f6e0d9850ba16fb57cd0fa98d84c'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/1/GPL/openjdk-25-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='76761c3ad2bebc865c5ed4ce08a7c5f89eb4f51d3f471d76f650e0556d79daa3'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 09 Dec 2024 05:52:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4f7ad6e84f249b4b319e4c8cf12e7929732105f68e6f8a67945acfd605733bd`  
		Last Modified: Tue, 10 Dec 2024 01:31:31 GMT  
		Size: 1.4 MB (1361283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:486069ad9324d6eebf03ccb16d29c65d696c810acc895f96c8c836c484ab9aa8`  
		Last Modified: Tue, 10 Dec 2024 01:31:36 GMT  
		Size: 211.0 MB (210965682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:5287adb426713e2ec5e4c7fd906e4b34892493162c0824b351b5efaa6d74e4fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2848217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69bc15740f33dcd61839a86244ca2e635f63d9640815ee91297f0c7e7510dce8`

```dockerfile
```

-	Layers:
	-	`sha256:86eb66de2748ff9f89dd3261fdb25a9cd546a5ea28b75a9e2a965e40ca62dca0`  
		Last Modified: Tue, 10 Dec 2024 01:31:31 GMT  
		Size: 2.8 MB (2830517 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44a2681e6edbd4d0a3fb06d78f3f5f30c74bfa06b950148cd904a8bda3b60a0c`  
		Last Modified: Tue, 10 Dec 2024 01:31:31 GMT  
		Size: 17.7 KB (17700 bytes)  
		MIME: application/vnd.in-toto+json
