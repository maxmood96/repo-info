## `openjdk:27-ea-3-bookworm`

```console
$ docker pull openjdk@sha256:7278a5f6cedc82bca64ed098c9b957152b21d9b8d60ee0a9eb4b70acc7227b02
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-3-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:639fbec1edbb2c9cbed460d90b9de824b5eae81baf91222431abd94b06f4c34f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.9 MB (381905361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6bec33d80ee77f17efd26b02e77c51e9348acb26dd7da75e10161a81ad21f67`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:06:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:05:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Dec 2025 05:20:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Dec 2025 05:20:33 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Wed, 24 Dec 2025 05:20:33 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Dec 2025 05:20:33 GMT
ENV LANG=C.UTF-8
# Wed, 24 Dec 2025 05:20:33 GMT
ENV JAVA_VERSION=27-ea+3
# Wed, 24 Dec 2025 05:20:33 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/3/GPL/openjdk-27-ea+3_linux-x64_bin.tar.gz'; 			downloadSha256='aaaea47c6d93cbeb444a08dfa58105ee17a15ab5c6d07b98c71952d8c12ead80'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/3/GPL/openjdk-27-ea+3_linux-aarch64_bin.tar.gz'; 			downloadSha256='b90b89ea9b49abf85ab7ae4323ddb7ef028ab69054d08d43e72b1f6e0b8860f6'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 24 Dec 2025 05:20:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c8443a297fa42e27cb10653777dd5a53f82a65fbc8b2d33f82b8722199f941d3`  
		Last Modified: Mon, 08 Dec 2025 22:16:25 GMT  
		Size: 48.5 MB (48480736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae8659f7a8d357662281a0f87eb293725bb75ffa6c7356c38567f557d8a1f11`  
		Last Modified: Mon, 08 Dec 2025 23:07:04 GMT  
		Size: 24.0 MB (24029335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c237534654fe7a5c118fcee78652af952e57a4a07cc322c0ae3c367839bb0ccc`  
		Last Modified: Tue, 09 Dec 2025 00:06:16 GMT  
		Size: 64.4 MB (64396522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f90ee0e42c4165e836caa4644a92acb323cf99df012ee595c8d71dfacaef75a`  
		Last Modified: Wed, 24 Dec 2025 05:21:08 GMT  
		Size: 16.9 MB (16944816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42837a7be1e12de93ec4beb9e99727e99a98cd7a13fc71c1b968d5c7529dcdc0`  
		Last Modified: Wed, 24 Dec 2025 05:21:24 GMT  
		Size: 228.1 MB (228053952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-3-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:40d0029363a85ebbd483c44c41e9ba0be9079caf504164ef24c1d08f414859c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8686150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb0ddaa6e85965b1c2269627db2f24fd293d42424de0229fc5aa58dfe52026e5`

```dockerfile
```

-	Layers:
	-	`sha256:2e5b961c26eac16879506d236d1839cba01c8e6c4386e6a873f8814b8b75ca87`  
		Last Modified: Wed, 24 Dec 2025 07:26:16 GMT  
		Size: 8.7 MB (8668228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:050cde64975f3ca41fb26e8b8db0cfcda1441043c8c79771e73556fbbe8c1b12`  
		Last Modified: Wed, 24 Dec 2025 07:26:17 GMT  
		Size: 17.9 KB (17922 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-3-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:177f2ab377725885ebd4a14ea466f36455e6057ba9dd95ce88b5f75061405c4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.0 MB (380021899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05a00d19b4b890376e920e377f52ed5d08b8182c8c8040dc59e092dc9832fe02`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:10:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:10:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Dec 2025 05:22:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Dec 2025 05:22:25 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Wed, 24 Dec 2025 05:22:25 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Dec 2025 05:22:25 GMT
ENV LANG=C.UTF-8
# Wed, 24 Dec 2025 05:22:25 GMT
ENV JAVA_VERSION=27-ea+3
# Wed, 24 Dec 2025 05:22:25 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/3/GPL/openjdk-27-ea+3_linux-x64_bin.tar.gz'; 			downloadSha256='aaaea47c6d93cbeb444a08dfa58105ee17a15ab5c6d07b98c71952d8c12ead80'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/3/GPL/openjdk-27-ea+3_linux-aarch64_bin.tar.gz'; 			downloadSha256='b90b89ea9b49abf85ab7ae4323ddb7ef028ab69054d08d43e72b1f6e0b8860f6'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 24 Dec 2025 05:22:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7f2b9668af76f73927725e2d1fb5d7224604d8c4c42cb8cdecb502257d9101c4`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 48.4 MB (48359071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0da1fc24a51c3ab23b5143a2c67b43348114c11a8029b3483be57ab9fe54eb6`  
		Last Modified: Mon, 08 Dec 2025 23:10:26 GMT  
		Size: 23.6 MB (23598247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a266a3916e0f2e8ff6996b219222479419b3dca87b3e3dfc3bd0108f509071`  
		Last Modified: Tue, 09 Dec 2025 00:11:40 GMT  
		Size: 64.4 MB (64371489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1bb8a817566887fdac1188f485d2ed5d5d81b6bbb1f34330cbcbb373c4294c8`  
		Last Modified: Wed, 24 Dec 2025 05:23:03 GMT  
		Size: 17.7 MB (17728533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9f842b7b9b2ff87487f628a6bb1975d63475db7e9894908b1237c76d7613f4`  
		Last Modified: Wed, 24 Dec 2025 05:25:19 GMT  
		Size: 226.0 MB (225964559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-3-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:75e3adefbc8fecb1b0428b0011967955d15b3d1d0856062852055c4bda743677
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8823114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32ae004119c4974791df2c4c528884f0fb942921ad9fe3f7ee56e2fda96d4238`

```dockerfile
```

-	Layers:
	-	`sha256:0679bea27cf8312b2b4626860c6b8e4354a67986835e1d569b1e1f9f952aafcd`  
		Last Modified: Wed, 24 Dec 2025 07:26:25 GMT  
		Size: 8.8 MB (8805073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9e7e26945bd79db76b5e420112ac34d18b575d2802cea1c5ec22f4754d20a5d`  
		Last Modified: Wed, 24 Dec 2025 07:26:26 GMT  
		Size: 18.0 KB (18041 bytes)  
		MIME: application/vnd.in-toto+json
