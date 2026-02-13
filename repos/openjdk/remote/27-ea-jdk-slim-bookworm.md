## `openjdk:27-ea-jdk-slim-bookworm`

```console
$ docker pull openjdk@sha256:f6d1062cf4b44b15811b7c3c197e5f07be8b24ba5e3e567037f63e870f10dde2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-jdk-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:77273d2cb77dd93fc82ffa2798777a29c95e5773fc4d0267c6cdbda0e26042d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.7 MB (260745732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:805617f5fc5867e31c52d5172783d7d1b20caa2f3fb53d1235d726115dff7eb6`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Fri, 13 Feb 2026 00:00:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Feb 2026 00:00:50 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Fri, 13 Feb 2026 00:00:50 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Feb 2026 00:00:50 GMT
ENV LANG=C.UTF-8
# Fri, 13 Feb 2026 00:00:50 GMT
ENV JAVA_VERSION=27-ea+8
# Fri, 13 Feb 2026 00:00:50 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/8/GPL/openjdk-27-ea+8_linux-x64_bin.tar.gz'; 			downloadSha256='26424619f5fc68be80026db27b8d73d0e36e791df4b4c4e8dbee4edae1f8ffeb'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/8/GPL/openjdk-27-ea+8_linux-aarch64_bin.tar.gz'; 			downloadSha256='7ca3627abde323298007e3644968cd30d4363d289840c83bd0b8b49ccd84da51'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 13 Feb 2026 00:00:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc684763e0bd80cef48364928ffdacdecfaf1ed1e42fa72a204125ab392eed7`  
		Last Modified: Fri, 13 Feb 2026 00:01:10 GMT  
		Size: 4.0 MB (4029248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:961bc6e89736e85d5312c671cc26cd2d9cb080f8d63587860c36c87ed8e8411f`  
		Last Modified: Fri, 13 Feb 2026 00:01:15 GMT  
		Size: 228.5 MB (228487997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:d1a0643984e475ae6be8c792fa07130860d30ecfb38ed7a9a9b7d279937d2d3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94512e6ad1da0b38829155b846a6d45eef780659d9cfba64a68158f07d9c39e3`

```dockerfile
```

-	Layers:
	-	`sha256:e4a848a7882a765e8028157c03aae5bb87196c2395b8e6e0cdcb6930125bf94d`  
		Last Modified: Fri, 13 Feb 2026 00:01:10 GMT  
		Size: 2.6 MB (2649170 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fc0da46e8241f36f9475829f54b2d5d1d22967e8997efd08c7ee76fb650dc26`  
		Last Modified: Fri, 13 Feb 2026 00:01:10 GMT  
		Size: 16.9 KB (16858 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-jdk-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:069647927d8ede51039290d938ee2f521bf1ab0daf0b0bba10f6f171b1318f98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.4 MB (258382673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:750ff533bca2d09b9e6a5ea40a34aae2e1abd02bd07b0bea0fe2bb5b1bb10cfd`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Fri, 13 Feb 2026 00:02:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Feb 2026 00:02:54 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Fri, 13 Feb 2026 00:02:54 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Feb 2026 00:02:54 GMT
ENV LANG=C.UTF-8
# Fri, 13 Feb 2026 00:02:54 GMT
ENV JAVA_VERSION=27-ea+8
# Fri, 13 Feb 2026 00:02:54 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/8/GPL/openjdk-27-ea+8_linux-x64_bin.tar.gz'; 			downloadSha256='26424619f5fc68be80026db27b8d73d0e36e791df4b4c4e8dbee4edae1f8ffeb'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/8/GPL/openjdk-27-ea+8_linux-aarch64_bin.tar.gz'; 			downloadSha256='7ca3627abde323298007e3644968cd30d4363d289840c83bd0b8b49ccd84da51'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 13 Feb 2026 00:02:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896064c42d184f04e69fb2eb0fa9edb3516fe6f22f5e84e5e724c4461b0f7c10`  
		Last Modified: Fri, 13 Feb 2026 00:03:16 GMT  
		Size: 3.9 MB (3851972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a907b6736ca434bccbf98188fb6a9c039ed9a4a722a04d9edd414bfabe01f49e`  
		Last Modified: Fri, 13 Feb 2026 00:03:20 GMT  
		Size: 226.4 MB (226422878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:243007d728b82b513a57bff5aa06ba8d1ab30f33ef587ffc9314d577685de9d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2665781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebac3e0ff4c0b91ef71ad738eca67672239da828b658415188d86cd1a4388070`

```dockerfile
```

-	Layers:
	-	`sha256:927d9273dd1632acd99048fec4675a830e0e0e2bb9ec904f0c832241274d47db`  
		Last Modified: Fri, 13 Feb 2026 00:03:16 GMT  
		Size: 2.6 MB (2648804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ccf17e994781d75dccf14fb3cccea5177c4551269c4043f29728c660a80ca7a`  
		Last Modified: Fri, 13 Feb 2026 00:03:16 GMT  
		Size: 17.0 KB (16977 bytes)  
		MIME: application/vnd.in-toto+json
