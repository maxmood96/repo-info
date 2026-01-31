## `openjdk:27-ea-bookworm`

```console
$ docker pull openjdk@sha256:62bfa757f902b01a96a40fef200318496bd74eb11ed00643414c5ed311bf2fdc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:8c97709873cc7bd7d08a4ebd053494b9ef67acd199e6ab910a8ea641deda2488
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.2 MB (382214381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b0424f796b6b9de0291439866c9bfd3560ee57fb7c8c2fa2761b387bca54b7e`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:08:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:53:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 30 Jan 2026 23:40:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 30 Jan 2026 23:40:28 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Fri, 30 Jan 2026 23:40:28 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 Jan 2026 23:40:28 GMT
ENV LANG=C.UTF-8
# Fri, 30 Jan 2026 23:40:28 GMT
ENV JAVA_VERSION=27-ea+7
# Fri, 30 Jan 2026 23:40:28 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/7/GPL/openjdk-27-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='951349bfcc6bf08d72f89175460216f0560a6c238848d93c2e194313a78b130e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/7/GPL/openjdk-27-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='3a3b7bac8a0432795430d519edf6eb790b6a3423b00516b74c85e1b7edb053a7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 30 Jan 2026 23:40:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c1be109a62df95316ceac87ea501079f32e17f36b636865a860841b7db06100c`  
		Last Modified: Tue, 13 Jan 2026 00:41:15 GMT  
		Size: 48.5 MB (48481622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64538a062a61add8dc8b290fa69475e8902eb839c497a5f5dcd5a950422e493c`  
		Last Modified: Tue, 13 Jan 2026 02:09:00 GMT  
		Size: 24.0 MB (24036867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1872fa12cc6b1145803f1a0679ca26cc65fa1b4e0ee389bfb30267594736b6`  
		Last Modified: Tue, 13 Jan 2026 03:53:27 GMT  
		Size: 64.4 MB (64395833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dbb2004d0cab95e474c28c083423929c1eae650e0fbdd4e9fe631a4b83038df`  
		Last Modified: Fri, 30 Jan 2026 23:40:51 GMT  
		Size: 16.9 MB (16944791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac059b97c0f8fa4f664c14484cd7b9e018bc740f901d56aaf8c87738b477db1`  
		Last Modified: Fri, 30 Jan 2026 23:40:56 GMT  
		Size: 228.4 MB (228355268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:c4d8054fbb2c7d1b13c55cae186ee0066bbfeb48f2d5edcc63ec96a63e1dc11e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8686171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08d6cd77b7817d9cc6d84b30ab81615edd583da680373ff4e1a744985f139bbe`

```dockerfile
```

-	Layers:
	-	`sha256:6ad2953606e1860e3eda9378b4a3d70aad4f7955536a6bc474c844c93a29a054`  
		Last Modified: Fri, 30 Jan 2026 23:40:51 GMT  
		Size: 8.7 MB (8668250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69da19c8c9e8dbf3f13e3d8c4350864d079ca7153ad9c2e60ddfd613283e07b6`  
		Last Modified: Fri, 30 Jan 2026 23:40:51 GMT  
		Size: 17.9 KB (17921 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:d48aa1c29981c6662238c64f4f90480628ba32aa5ac06ed58ccce0c05ea3eebc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.5 MB (380472480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:321022b79bf8af1a3b42c7dceb3a47b4b0c0e2c36fe9d58e0e3a138e092e0c21`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:12:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:56:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 30 Jan 2026 23:39:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 30 Jan 2026 23:40:08 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Fri, 30 Jan 2026 23:40:08 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 Jan 2026 23:40:08 GMT
ENV LANG=C.UTF-8
# Fri, 30 Jan 2026 23:40:08 GMT
ENV JAVA_VERSION=27-ea+7
# Fri, 30 Jan 2026 23:40:08 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/7/GPL/openjdk-27-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='951349bfcc6bf08d72f89175460216f0560a6c238848d93c2e194313a78b130e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/7/GPL/openjdk-27-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='3a3b7bac8a0432795430d519edf6eb790b6a3423b00516b74c85e1b7edb053a7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 30 Jan 2026 23:40:08 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1029f5ddc0d24726f1cefbb8def7a88f8ec819a1fdc4c05ce523011b4b73c72d`  
		Last Modified: Tue, 13 Jan 2026 00:41:14 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72c713ab317dd7f302a6ff5a345af5b61cddc864fca2d96a23e6ef3c90a6657`  
		Last Modified: Tue, 13 Jan 2026 02:12:45 GMT  
		Size: 23.6 MB (23604814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687ad46596f06c934001fa6d7bea3d1508b0bb616cffb71004efd5bada56884f`  
		Last Modified: Tue, 13 Jan 2026 03:57:05 GMT  
		Size: 64.5 MB (64479462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637567d3afd3c1ee199054e74fff562e35aa3f6b5d19e9bbe03970b167ae82f4`  
		Last Modified: Fri, 30 Jan 2026 23:40:34 GMT  
		Size: 17.7 MB (17728544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac51efe63c33c953bf845b4860a33f707c19b6327141a9ecb2d7536fbbf6db31`  
		Last Modified: Fri, 30 Jan 2026 23:40:38 GMT  
		Size: 226.3 MB (226293588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:dc79406a6886b04b7f0aa31ab5dbbf1c4632939f00a3dbf945e1faf451bb4a94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8823136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a375317361db36961b0c3bb80799f811b42514a56d7ffa094fb8992854930de1`

```dockerfile
```

-	Layers:
	-	`sha256:3912beee550437a2f71eebd9f9ef9b5bedc737dfd3d44ae76077358c1df02338`  
		Last Modified: Fri, 30 Jan 2026 23:40:34 GMT  
		Size: 8.8 MB (8805095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f52fbff54e6c8c4480256446478280448a522bc2e58db3f880c93d29e05a09d8`  
		Last Modified: Fri, 30 Jan 2026 23:40:33 GMT  
		Size: 18.0 KB (18041 bytes)  
		MIME: application/vnd.in-toto+json
