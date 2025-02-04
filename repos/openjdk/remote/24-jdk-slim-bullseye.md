## `openjdk:24-jdk-slim-bullseye`

```console
$ docker pull openjdk@sha256:08ea153bc8a563fd3061339b9bee569dca91bea8ea65b697f92848d935f27713
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-jdk-slim-bullseye` - linux; amd64

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

### `openjdk:24-jdk-slim-bullseye` - unknown; unknown

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

### `openjdk:24-jdk-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:2397e7d22c5c00b23b3a4ce0299e73f1a258c9bd4bf49fd1ebeb5fa7e7f178b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.0 MB (241034747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b403160ce640315220cfb9cef6d8e3996fa60787d9f57bb386391218db96f50`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 31 Jan 2025 01:48:14 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1738540800'
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
	-	`sha256:9225a2a808e874449ee822a282882a3c331aad2f5093c1062e16494d8bce3e9a`  
		Last Modified: Tue, 04 Feb 2025 01:38:25 GMT  
		Size: 28.7 MB (28744810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19ab3d281e75349c8d7e523dfe331e05eef1e55328ca9cf23395949e954a9cf4`  
		Last Modified: Tue, 04 Feb 2025 10:45:02 GMT  
		Size: 1.4 MB (1361266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb01018a325a85f5afc361927a7752d4e07de40901b27c09004e65508e0c751`  
		Last Modified: Tue, 04 Feb 2025 10:46:45 GMT  
		Size: 210.9 MB (210928671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:2236633385287c2ff41d2f571dd7f983a5a9a0917fbea88fb699c8204eaff8bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2845287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f31cd26af175289bebe9252fdc95e9287c7b41a198c1f4e815dd04b624f4d32`

```dockerfile
```

-	Layers:
	-	`sha256:3028fbde20dc7b3bf7a9401f3ea5fc458075568dd1b7d767b60a1deb1310c6b3`  
		Last Modified: Tue, 04 Feb 2025 10:46:41 GMT  
		Size: 2.8 MB (2827574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:432845dcb2ef06fdb669ea0243f8efbd4e4fa249e9a39fe1a726d29397206e60`  
		Last Modified: Tue, 04 Feb 2025 10:46:41 GMT  
		Size: 17.7 KB (17713 bytes)  
		MIME: application/vnd.in-toto+json
