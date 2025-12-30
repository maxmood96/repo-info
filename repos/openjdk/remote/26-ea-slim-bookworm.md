## `openjdk:26-ea-slim-bookworm`

```console
$ docker pull openjdk@sha256:d477c0a0ff3806c9eaf4585a0b243a82c19b2eefc1dd0454f9455ded0e79af3d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:8984b4659231d01beb1f7c99a5fe816e87ecd36ce24197e39b2bb37d06f0008b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.3 MB (260259846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fa0f0a08a3a86fd03e99721178d55582f7a2cb8ff593331d9311a6b889ba110`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:11:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:12:04 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Tue, 30 Dec 2025 00:12:04 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:12:04 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 00:12:04 GMT
ENV JAVA_VERSION=26-ea+29
# Tue, 30 Dec 2025 00:12:04 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/29/GPL/openjdk-26-ea+29_linux-x64_bin.tar.gz'; 			downloadSha256='14b38c0378b8fccf20824a10aed0193c3e5c9732c7933f4e14b1409027db9d5a'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/29/GPL/openjdk-26-ea+29_linux-aarch64_bin.tar.gz'; 			downloadSha256='fbf83d509c5cbc2ca19ae7e7456d277a469c94290129cb4230cfbcea05ea7edf'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 30 Dec 2025 00:12:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998fd0232716ed617e4a51b1d2fda0f16db505c6c59da1e1d980d576dfadcfc5`  
		Last Modified: Tue, 30 Dec 2025 00:12:36 GMT  
		Size: 4.0 MB (4027374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e90f99886f11abb44bbf2eca6bed19b746df68b62bf7b9cbb1f5f0533a231e`  
		Last Modified: Tue, 30 Dec 2025 00:12:47 GMT  
		Size: 228.0 MB (228004048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:49e2be090e2b207016dc151423fadca9be68042b4a97993fd99e29230200d9ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3279246453e32b11201432ed990621c8bd182758eac8b18f1db057d16404f217`

```dockerfile
```

-	Layers:
	-	`sha256:6d1aa0e71b43d3317093c80995256a943cb2027a85e0ef4ed7bd05f0acf7d7a1`  
		Last Modified: Tue, 30 Dec 2025 04:24:15 GMT  
		Size: 2.6 MB (2649789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64280ef5449213d607450ab4a27373c8bc56aed5816e9295c4ad918b26306483`  
		Last Modified: Tue, 30 Dec 2025 04:24:16 GMT  
		Size: 16.9 KB (16871 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:c94bc40951448c99f4272ff52711211bf6f6ad685e677a7116927a23c6e7482b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.9 MB (257865895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f245c98b96e076e8dee8462b85b6299cda0d9431a185caa46a05259b74215d9`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:13:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:13:17 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Tue, 30 Dec 2025 00:13:17 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:13:17 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 00:13:17 GMT
ENV JAVA_VERSION=26-ea+29
# Tue, 30 Dec 2025 00:13:17 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/29/GPL/openjdk-26-ea+29_linux-x64_bin.tar.gz'; 			downloadSha256='14b38c0378b8fccf20824a10aed0193c3e5c9732c7933f4e14b1409027db9d5a'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/29/GPL/openjdk-26-ea+29_linux-aarch64_bin.tar.gz'; 			downloadSha256='fbf83d509c5cbc2ca19ae7e7456d277a469c94290129cb4230cfbcea05ea7edf'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 30 Dec 2025 00:13:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b1efea88fbf7c88bbbdeec2e84bd4f8d0b814c210ee65763f6d4cc91c28365e8`  
		Last Modified: Mon, 29 Dec 2025 22:26:16 GMT  
		Size: 28.1 MB (28102210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad426403a266942b1bbe1b8285d4566cebfefab1dfa4ddd0cfbe89b18084627`  
		Last Modified: Tue, 30 Dec 2025 00:13:50 GMT  
		Size: 3.9 MB (3851377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5af24c4618d0d56fb24c6bdd4803631454702665b26033ae3fd1ed8c9bd1d93`  
		Last Modified: Tue, 30 Dec 2025 00:13:57 GMT  
		Size: 225.9 MB (225912308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:37c181ed4944868e0f372a70d01179c2442bde673211aa7ae78ca9c09c59e5d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:babf4a663beacc04bba4850b90ac215ce2a60a979df37cd87e28140b68a67c45`

```dockerfile
```

-	Layers:
	-	`sha256:dada07920415686f658717ae069e7ae3573d72d94e19ebc2a5b9de72394709b8`  
		Last Modified: Tue, 30 Dec 2025 04:24:19 GMT  
		Size: 2.6 MB (2649423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e04ae695472d98737a31d434f94c08078eb723dcc38ca8fb2912fd4a0c7f403`  
		Last Modified: Tue, 30 Dec 2025 04:24:21 GMT  
		Size: 17.0 KB (16990 bytes)  
		MIME: application/vnd.in-toto+json
