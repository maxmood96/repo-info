## `openjdk:24-ea-slim-bullseye`

```console
$ docker pull openjdk@sha256:9f795b48e8ce950dbd62ae84c7a4ab2e8fbde27d937f032da4bca36662909b7a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:3395593ba140e3e5b214ac54f19a668d34ea4f4bb04c0d39ed376f383cfc727f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244608452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a755cece51572dad87d0855cd715e18b570be71079d9f01debe58ff3c182156d`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 31 Jan 2025 01:48:14 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Fri, 31 Jan 2025 01:48:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 01:48:14 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 31 Jan 2025 01:48:14 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jan 2025 01:48:14 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 01:48:14 GMT
ENV JAVA_VERSION=24-ea+34
# Fri, 31 Jan 2025 01:48:14 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/34/GPL/openjdk-24-ea+34_linux-x64_bin.tar.gz'; 			downloadSha256='d49c0df93307a9bd06c9ca7b35ce6d068246a0938d0802933910b42574c173d3'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/34/GPL/openjdk-24-ea+34_linux-aarch64_bin.tar.gz'; 			downloadSha256='ffab3ade32683a348fbb81aef96107b38545d1df7daa4e7ca81fe0f6775002ea'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 31 Jan 2025 01:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 01:36:33 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfadbd98377229634a83a66d6e049a8c579577190b638fdc0a9449f4af6f81cf`  
		Last Modified: Tue, 04 Feb 2025 04:44:49 GMT  
		Size: 1.4 MB (1377265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30fbe782cbf74835b69e04470b6e30dc5eece062dd75f7ed040b215ef4fcae7a`  
		Last Modified: Tue, 04 Feb 2025 04:44:52 GMT  
		Size: 213.0 MB (212978599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:a498f98b61927e2a094db0a42f94831eb94d6dae81763c835a53360683fea0ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2845491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2df8971eef138c63a090c49b7f793cd96a1c08c4bb78f54cfae6824995e0d16`

```dockerfile
```

-	Layers:
	-	`sha256:07189cb1838ae4200650857315eb8461001afb759dbac99a75dd41d7d9d2c38a`  
		Last Modified: Tue, 04 Feb 2025 04:44:49 GMT  
		Size: 2.8 MB (2827922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9c0aee14f6cb9207c45a84e3dd123182107bd6061154e0508f77c1f67b4756d`  
		Last Modified: Tue, 04 Feb 2025 04:44:49 GMT  
		Size: 17.6 KB (17569 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:ae7e9e9bd3018fcb0886f4fe023f4c15b2510199d7a6613ef84a90e9523d8e80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.0 MB (241034819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c772adcb4fe0fa1abe4f24e718f5eb355f71bf0ba53b9ce6bf75fa5cf88fbaf`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Fri, 31 Jan 2025 01:48:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 01:48:14 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 31 Jan 2025 01:48:14 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jan 2025 01:48:14 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 01:48:14 GMT
ENV JAVA_VERSION=24-ea+34
# Fri, 31 Jan 2025 01:48:14 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/34/GPL/openjdk-24-ea+34_linux-x64_bin.tar.gz'; 			downloadSha256='d49c0df93307a9bd06c9ca7b35ce6d068246a0938d0802933910b42574c173d3'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/34/GPL/openjdk-24-ea+34_linux-aarch64_bin.tar.gz'; 			downloadSha256='ffab3ade32683a348fbb81aef96107b38545d1df7daa4e7ca81fe0f6775002ea'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 31 Jan 2025 01:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696461101c67cc9af64403e8b92081fe283008fa12948c4ddab16982e126d03f`  
		Last Modified: Wed, 22 Jan 2025 02:34:05 GMT  
		Size: 1.4 MB (1361278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80d05c11aaf104a1397c734dc0e748900fcd1b71ce9556a74459f1f43d20d09b`  
		Last Modified: Fri, 31 Jan 2025 22:36:15 GMT  
		Size: 210.9 MB (210928628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:3649640edd5b435781a41a78cd61caf9bc97102af5b6ea9947566969b9fdc305
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2845287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e71499522a859ec3bcd6028940373afc1165e258d16ad89554a9cfae926f6ed`

```dockerfile
```

-	Layers:
	-	`sha256:5140c262ce4142d19b47136486652c66518c31bf9742d9d1080c9b9ffbe198fd`  
		Last Modified: Fri, 31 Jan 2025 22:36:10 GMT  
		Size: 2.8 MB (2827574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2a724b3668cdad7b56ca8d2247ed1351a5bd88268dafd15e001a9ac23e752e6`  
		Last Modified: Fri, 31 Jan 2025 22:36:10 GMT  
		Size: 17.7 KB (17713 bytes)  
		MIME: application/vnd.in-toto+json
