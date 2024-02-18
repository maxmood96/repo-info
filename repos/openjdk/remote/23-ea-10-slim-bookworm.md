## `openjdk:23-ea-10-slim-bookworm`

```console
$ docker pull openjdk@sha256:7026d4ac9adf9fc97eac7d064cf9ab9f49f09488d1b0ebf346ede458c4a810ee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-10-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:f2d683da08743ca6ed3bc2371a2271333135173d3612929095eb958558c4e739
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.4 MB (236409995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:503ab007dc28b90a2e3d8c6fc1d71824ca775b98e7bb3faaaea582c9c5c31cd7`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:22 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Tue, 13 Feb 2024 00:37:22 GMT
CMD ["bash"]
# Fri, 16 Feb 2024 20:22:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Feb 2024 20:22:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 16 Feb 2024 20:22:31 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 20:22:31 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2024 20:22:31 GMT
ENV JAVA_VERSION=23-ea+10
# Fri, 16 Feb 2024 20:22:31 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/10/GPL/openjdk-23-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='9b583a20351ff9be1b782ba71d5e61d7f8e4731c81277e4f2566c5509db052b0'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/10/GPL/openjdk-23-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='b646bcb58d932236e066c97dbc32d6df53a9a823c78565cd22bd6bf05a0cea7d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 16 Feb 2024 20:22:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6487fd45cfee70e553c2252aa957894b32b69a269a85b8ed601ebe5781f0cd5`  
		Last Modified: Sat, 17 Feb 2024 00:53:28 GMT  
		Size: 4.0 MB (4014951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0945a7ab1cf5cbc0e19d52538e61cc42bc132dba3f2c1ae9bd6ec87947f5ad70`  
		Last Modified: Sat, 17 Feb 2024 00:53:33 GMT  
		Size: 203.3 MB (203270953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-10-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:49077cadb2092efe0792177b3c12f44c805890a885d40d5fc2c3a714e32a39fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2366846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de00f9a9c316021d920275f28e6927967864157f7ce4ad47bc3e4e7d3e0482ba`

```dockerfile
```

-	Layers:
	-	`sha256:678a649ec494679d35c677925f9357a48e2231cebdb8a1014f67b9c92789c238`  
		Last Modified: Sat, 17 Feb 2024 00:53:28 GMT  
		Size: 2.3 MB (2347502 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce78a38c1da7148b235ea0595e86b7c97784425b8ede800161befe46fcdde57a`  
		Last Modified: Sat, 17 Feb 2024 00:53:28 GMT  
		Size: 19.3 KB (19344 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-10-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:ed78e925d44564d767a093042569e33d5e5e381fccfd237935eec35d0aa21ef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.1 MB (234126545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c6f2e498d9833fcfc3b6d7a787f606efbf64619dd73a3b0c49d66c0fd65e33e`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:20 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Tue, 13 Feb 2024 00:41:20 GMT
CMD ["bash"]
# Fri, 16 Feb 2024 20:22:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Feb 2024 20:22:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 16 Feb 2024 20:22:31 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 20:22:31 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2024 20:22:31 GMT
ENV JAVA_VERSION=23-ea+10
# Fri, 16 Feb 2024 20:22:31 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/10/GPL/openjdk-23-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='9b583a20351ff9be1b782ba71d5e61d7f8e4731c81277e4f2566c5509db052b0'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/10/GPL/openjdk-23-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='b646bcb58d932236e066c97dbc32d6df53a9a823c78565cd22bd6bf05a0cea7d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 16 Feb 2024 20:22:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f546e941f15b76df3d982d56985432b05bc065e3923fb35be25a4d33d5c0f911`  
		Last Modified: Tue, 13 Feb 2024 00:44:54 GMT  
		Size: 29.2 MB (29156363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f1e9c7916a6ccf7810e822d985a2f9d022599aef32a11c6676f3590484cf2cd`  
		Last Modified: Wed, 14 Feb 2024 01:16:16 GMT  
		Size: 3.8 MB (3820100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2533d66fac038179da25106e6a7b2038d7879642fa35fa6927aba41e07f50d2b`  
		Last Modified: Sun, 18 Feb 2024 05:18:25 GMT  
		Size: 201.2 MB (201150082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-10-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:6829088de52858d9a0290c8dda85363057dfaf8d37e631def057b75a8f88aa81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2365975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9544a74853b2183373133646127f704ab64eb1d5865846597411571af4010936`

```dockerfile
```

-	Layers:
	-	`sha256:d9982c9efb7eed3287fd3e2510ecba2b00730b7b07867583fc0a9bcd9e8575e2`  
		Last Modified: Sun, 18 Feb 2024 05:18:21 GMT  
		Size: 2.3 MB (2346772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:239ded760255974dae45ef54e002cf94fb82e4208df9d26fc57147a213ea608d`  
		Last Modified: Sun, 18 Feb 2024 05:18:21 GMT  
		Size: 19.2 KB (19203 bytes)  
		MIME: application/vnd.in-toto+json
