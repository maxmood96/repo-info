## `openjdk:24-ea-15-bullseye`

```console
$ docker pull openjdk@sha256:1090f0e85268a8dc5822acafc2a1946468e095bca80b02112ce1f12639640511
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-15-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:b0b554cdcf2de55003610423a08cdedfd311bb86ebd50d78dc882e7deee916e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.7 MB (349652824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdd09e4ce32ae3210da9e350d8e60c0e5944041cd6113166d501a235ea171b7d`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:59 GMT
ADD file:aad8b86b3a958bc07504985acedcc819faa4f1ed12ca8b46d8d94c4d564cbdfa in / 
# Wed, 04 Sep 2024 21:40:00 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:03:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:03:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 14 Sep 2024 06:48:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 14 Sep 2024 06:48:15 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Sat, 14 Sep 2024 06:48:15 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 14 Sep 2024 06:48:15 GMT
ENV LANG=C.UTF-8
# Sat, 14 Sep 2024 06:48:15 GMT
ENV JAVA_VERSION=24-ea+15
# Sat, 14 Sep 2024 06:48:15 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/15/GPL/openjdk-24-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='b41d4867c348d7f1991085d8bcc8797eaf032d9dfaa3419bc9db15eaea75e91e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/15/GPL/openjdk-24-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='165b7c19403e9708ca261cdfe4c385e837df683049203e33ad2bf76228054a25'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 14 Sep 2024 06:48:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d82c4492ee91810a42e0c53e955a661e9a092364bc474c9db559ea5b24b7047f`  
		Last Modified: Wed, 04 Sep 2024 21:42:52 GMT  
		Size: 53.7 MB (53731619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf248fd698830ce7c74f07fb7ca6adac7bea55a16521e9e1f2afe06219e00f6`  
		Last Modified: Wed, 04 Sep 2024 22:08:56 GMT  
		Size: 15.7 MB (15749712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b216df41d3eb392b55b4bb8c654fe024d7c3d00404a7e105f494ef43990fad`  
		Last Modified: Wed, 04 Sep 2024 22:09:10 GMT  
		Size: 54.8 MB (54833449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47b2b01e7ce009af5fa97c531d3c10731cde5c693d8574b0416f64f36c47e6a`  
		Last Modified: Mon, 16 Sep 2024 19:24:34 GMT  
		Size: 15.5 MB (15526332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c63a410e1d96040d168ccc5818be85fb02c3835f77676b2e16b4a527f99e5e5`  
		Last Modified: Mon, 16 Sep 2024 19:24:39 GMT  
		Size: 209.8 MB (209811712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-15-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:bb43322b2a11139a2fcb19f9cf8aa11a7bf342c07f6e1294c4b85456e3f45a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8314422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72a68d7d0c933735571efce519a747206ed6e5639fcf6665dad0bda9fd8bc17f`

```dockerfile
```

-	Layers:
	-	`sha256:2415db0e91e4c82bb4e61e9675e16c2236f57cc2191f521880e3582b3fc8463d`  
		Last Modified: Mon, 16 Sep 2024 19:24:34 GMT  
		Size: 8.3 MB (8295620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbcc3476cc224366373ca9ad25e73ec037c13ef7a8e71da5b255ccbd1996e4cb`  
		Last Modified: Mon, 16 Sep 2024 19:24:34 GMT  
		Size: 18.8 KB (18802 bytes)  
		MIME: application/vnd.in-toto+json
