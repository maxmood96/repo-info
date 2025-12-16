## `openjdk:26-ea-jdk-slim-bookworm`

```console
$ docker pull openjdk@sha256:4486f5773d5379f0e58e9dff8b50beac266d10ab9372e01779f0a75b4f200fb4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-jdk-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:d27a02921f59ba9119c4234b0761b4cc3c2acb656c3fae7c4085a8fcdd8352bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.2 MB (260244572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ebb2ee3217b67ac7392c567db7ae197cdc90f17a05616ad7420b251fc658791`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Tue, 16 Dec 2025 00:03:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Dec 2025 00:03:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Tue, 16 Dec 2025 00:03:56 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Dec 2025 00:03:56 GMT
ENV LANG=C.UTF-8
# Tue, 16 Dec 2025 00:03:56 GMT
ENV JAVA_VERSION=26-ea+28
# Tue, 16 Dec 2025 00:03:56 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/28/GPL/openjdk-26-ea+28_linux-x64_bin.tar.gz'; 			downloadSha256='a18910b0bdceb12a4f78147a1feebee50cc621ad8114c07a1ab071e58c17b09d'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/28/GPL/openjdk-26-ea+28_linux-aarch64_bin.tar.gz'; 			downloadSha256='d330a706e3fc611f4b39f6768f104e47d0a755ffabda31e3299dbc2e791f4f18'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 16 Dec 2025 00:03:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa4e5850b8acab36d407020ab698b132d91e71ab153dba13e043c739ec625acc`  
		Last Modified: Tue, 16 Dec 2025 00:04:31 GMT  
		Size: 4.0 MB (4027350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7edcecb8c3f9f445d8c784f94368e949cf6cb3e44ebcb9a63315478ce07a122f`  
		Last Modified: Tue, 16 Dec 2025 00:04:42 GMT  
		Size: 228.0 MB (227988804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:4b2269f12cb2114136b2a31214a1acf3ecc48f9ba277e93b97bbee76a3be3ee9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7635eecc594d78c1a74428e5b3d12c608a9ffcd9d0ed18c2aecf4b337d5b3d6`

```dockerfile
```

-	Layers:
	-	`sha256:3dc609b67654e00c6cdca8a2479d5cff1e9f46c815dc645195b9670c8380ff2a`  
		Last Modified: Tue, 16 Dec 2025 01:24:11 GMT  
		Size: 2.6 MB (2649789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12e60bc335e77547078ed89493d66f73740380701bbeb1adabf49e009c6f3ead`  
		Last Modified: Tue, 16 Dec 2025 01:24:12 GMT  
		Size: 16.9 KB (16871 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-jdk-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:543e53fee9ae254a860021b364441e9806cf75c93361474db0f1416e9e72f460
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.9 MB (257856343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c6c5f83914b5b078594629dfcc246a964fcb649c19606f7b45ac25baf280a2b`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Tue, 16 Dec 2025 00:03:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Dec 2025 00:03:48 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Tue, 16 Dec 2025 00:03:48 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Dec 2025 00:03:48 GMT
ENV LANG=C.UTF-8
# Tue, 16 Dec 2025 00:03:48 GMT
ENV JAVA_VERSION=26-ea+28
# Tue, 16 Dec 2025 00:03:48 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/28/GPL/openjdk-26-ea+28_linux-x64_bin.tar.gz'; 			downloadSha256='a18910b0bdceb12a4f78147a1feebee50cc621ad8114c07a1ab071e58c17b09d'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/28/GPL/openjdk-26-ea+28_linux-aarch64_bin.tar.gz'; 			downloadSha256='d330a706e3fc611f4b39f6768f104e47d0a755ffabda31e3299dbc2e791f4f18'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 16 Dec 2025 00:03:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8a4a7306158c2bef7a131de3110e384f4822829cbcce20bc6b4ba32dd82a1d87`  
		Last Modified: Mon, 08 Dec 2025 22:16:51 GMT  
		Size: 28.1 MB (28102229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38db6a2de04abbfae12dac07ddb2f136eb29541ac60c488e5151c3f0e347db86`  
		Last Modified: Tue, 16 Dec 2025 00:04:21 GMT  
		Size: 3.9 MB (3851367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6d351e70198e606998c8d1e87cc78a07c6c721fe3a200abad0eecf11f297c3a`  
		Last Modified: Tue, 16 Dec 2025 00:04:26 GMT  
		Size: 225.9 MB (225902747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:f400fc2c16bf4f881829880a24be482cc01985c8b50779b211281b689c38d7ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1111aad0413f3cdde07682c2fc4ab2649f8d4e3414cc2b9072007b2e503b911`

```dockerfile
```

-	Layers:
	-	`sha256:14226f55dd1d96890472e175b09180c088fde259537a5794b35d8dca7397e1c7`  
		Last Modified: Tue, 16 Dec 2025 01:24:16 GMT  
		Size: 2.6 MB (2649423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8856df672398c828cdf9ecb202be52f8da35f41a5b40801b5c874d2445a07606`  
		Last Modified: Tue, 16 Dec 2025 01:24:17 GMT  
		Size: 17.0 KB (16989 bytes)  
		MIME: application/vnd.in-toto+json
