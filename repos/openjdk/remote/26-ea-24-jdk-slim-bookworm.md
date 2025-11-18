## `openjdk:26-ea-24-jdk-slim-bookworm`

```console
$ docker pull openjdk@sha256:c371b094cebb389afb1a2e53cfc15eb18ed3e586042ccf1b1ee637e32253a6df
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-24-jdk-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:6da724e938afa4a4594f957f79a91959531bac51d5c6449113fc76e3390e2b48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.1 MB (260135741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d020331f6a8f309c5d4d77ecb76520e1e4a76466cc2bf4fa27eb64bb743582c0`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:32:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:32:47 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Tue, 18 Nov 2025 05:32:47 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:32:47 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 05:32:47 GMT
ENV JAVA_VERSION=26-ea+24
# Tue, 18 Nov 2025 05:32:47 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/24/GPL/openjdk-26-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='4ba2cf8ca6a66fbea892ba55048f82d8cd4fabe95d9364ac28a79b282c6207f8'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/24/GPL/openjdk-26-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='d6f947b5c9fa605b41f4890ef6e09f2c0c321215681497f2174efa10adfab326'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 18 Nov 2025 05:32:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f0fe5f078a73a03d5c00cbc1ea1adb014dd81150496073f1c2b7652ac895ac`  
		Last Modified: Tue, 18 Nov 2025 05:33:21 GMT  
		Size: 4.0 MB (4027331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd34cde4df69aaf976986f11136c593162823d3a04c1073d9422e2637483cc9d`  
		Last Modified: Tue, 18 Nov 2025 07:35:39 GMT  
		Size: 227.9 MB (227879961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-24-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:b0ea445a74a9960864234977ec9df386716c2acca7b5d83479ca6888104266a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be882acea30ed1ab0f21e5782cc6ad2f913ccc0511379c0f6f9449558a17d30b`

```dockerfile
```

-	Layers:
	-	`sha256:7148862fd0b89279e635c9501222c67cbaaf94837599c78808e9d3792de8f787`  
		Last Modified: Tue, 18 Nov 2025 07:25:14 GMT  
		Size: 2.6 MB (2649789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f4aa3af8f3dcaaba3a12344c961c7e2ce9d533cf249662a9e36b65d62c9027a`  
		Last Modified: Tue, 18 Nov 2025 07:25:14 GMT  
		Size: 16.9 KB (16871 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-24-jdk-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:39ef1855443dd26930243286f276c529beca2de5bd7322c1578ae6d654faad75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.7 MB (257690251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09c45a27392c27d7042c586e41308d7d688a2d37b7fff0e15ed4c2604b74cf83`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:08:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:08:32 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Tue, 18 Nov 2025 04:08:32 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:08:32 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 04:08:32 GMT
ENV JAVA_VERSION=26-ea+24
# Tue, 18 Nov 2025 04:08:32 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/24/GPL/openjdk-26-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='4ba2cf8ca6a66fbea892ba55048f82d8cd4fabe95d9364ac28a79b282c6207f8'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/24/GPL/openjdk-26-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='d6f947b5c9fa605b41f4890ef6e09f2c0c321215681497f2174efa10adfab326'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 18 Nov 2025 04:08:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b934c9e9abfc7be688cc1d687ae45e88ffaed5f261e089703b7561557d1488`  
		Last Modified: Tue, 18 Nov 2025 04:09:03 GMT  
		Size: 3.9 MB (3851406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd884d7345f1af58fe1d9e6e5ae0ddabda95f03bac88e8647d0b673d413ee4b7`  
		Last Modified: Tue, 18 Nov 2025 07:35:40 GMT  
		Size: 225.7 MB (225736638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-24-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:1a8607c7d2796ac502566527acdb2e9ec4b7433b5a3da1143f7baf203204cad3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f5b8c4b47e17e0bdf058d2d957f7163457a1c906d308e2b840c490d6c94da84`

```dockerfile
```

-	Layers:
	-	`sha256:7374ebc16845812e43d8b18abc7a14d285fe93d00fec64b33685ac9bc46b8a74`  
		Last Modified: Tue, 18 Nov 2025 04:25:51 GMT  
		Size: 2.6 MB (2649423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56afda93db412942f07a9bfd867634838d7ada6ab0e9a7a7b959b7db7591b841`  
		Last Modified: Tue, 18 Nov 2025 04:25:52 GMT  
		Size: 17.0 KB (16990 bytes)  
		MIME: application/vnd.in-toto+json
