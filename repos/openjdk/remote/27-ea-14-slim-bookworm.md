## `openjdk:27-ea-14-slim-bookworm`

```console
$ docker pull openjdk@sha256:16f2907c7d1cb2cf2cd6d33c0578ba47de4082bba83b0bba69c1cbbc2451407a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-14-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:7219c5a36b26030dabf0ede3e640349e8a6ec1daab0dbe837bc46a169f596817
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.9 MB (260902106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0142df08e322a7dbc6c7c3e939d21686961992f0cb1c0e7dd256568f6d18505f`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 23 Mar 2026 17:58:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Mar 2026 17:58:59 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Mon, 23 Mar 2026 17:58:59 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Mar 2026 17:58:59 GMT
ENV LANG=C.UTF-8
# Mon, 23 Mar 2026 17:58:59 GMT
ENV JAVA_VERSION=27-ea+14
# Mon, 23 Mar 2026 17:58:59 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/14/GPL/openjdk-27-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='64b478b9973d8d04e1680cdfaf11a8e93f8a17f962af3ddb1c61b76a62c0d699'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/14/GPL/openjdk-27-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='c99686ed0406f05a113b6467b6a57699864922c476481609a703c6dd91534f45'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 23 Mar 2026 17:58:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6cc69d65d2fe13c1a39563d3279977e14d2f168f06484eb41e209ff01d5070e`  
		Last Modified: Mon, 23 Mar 2026 17:59:19 GMT  
		Size: 4.0 MB (4029174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d1da6310801d424b77f31528eb8604a20de260035de09d1c75e671e0c043a4a`  
		Last Modified: Mon, 23 Mar 2026 17:59:24 GMT  
		Size: 228.6 MB (228636707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-14-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:f855d2010a27a1d405c5cceacf86fb65c802dd0b52517c30bd862cc06ee366e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:859cd9e47b07c3503f986cd1ff31b30549aee0485be982ef6b525ed368301284`

```dockerfile
```

-	Layers:
	-	`sha256:f125119a76366d4c7f4bcd2e7c11227138dc2f4d678ec07ae83dc78f88ebf87c`  
		Last Modified: Mon, 23 Mar 2026 17:59:19 GMT  
		Size: 2.6 MB (2649807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe407101c62b572d6ca280ed855229b2776faefcde319d0deadfa09a3f392d28`  
		Last Modified: Mon, 23 Mar 2026 17:59:18 GMT  
		Size: 16.9 KB (16871 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-14-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:97a636c4d3db4cfaf2359d090d3d805471fde18ee3fb01b3af24ffccec9259fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.6 MB (258572854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c79cd570d49c26914fd440c17f8544853ad83a5f6ef7d35ebc8b59f7dadb9e9c`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 23 Mar 2026 17:58:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Mar 2026 17:58:45 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Mon, 23 Mar 2026 17:58:45 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Mar 2026 17:58:45 GMT
ENV LANG=C.UTF-8
# Mon, 23 Mar 2026 17:58:45 GMT
ENV JAVA_VERSION=27-ea+14
# Mon, 23 Mar 2026 17:58:45 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/14/GPL/openjdk-27-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='64b478b9973d8d04e1680cdfaf11a8e93f8a17f962af3ddb1c61b76a62c0d699'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/14/GPL/openjdk-27-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='c99686ed0406f05a113b6467b6a57699864922c476481609a703c6dd91534f45'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 23 Mar 2026 17:58:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9d6ef834acf2d3c98f6dbc040a9e5bc6d3f94d9c56bf62ecb5c330c741deb2`  
		Last Modified: Mon, 23 Mar 2026 17:59:06 GMT  
		Size: 3.9 MB (3851967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9bc925628192f360837e625782df3809d80f5a447231d388f27835fb09a2f6`  
		Last Modified: Mon, 23 Mar 2026 17:59:10 GMT  
		Size: 226.6 MB (226604822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-14-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:32f0d1c4f598b91aeddd555f908758fa766ecf473fcc9a0611aaee8e613a71fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f015164e959329bc6a845621af4d9f6a6a2baecce42f7003ae913d1e73f246d`

```dockerfile
```

-	Layers:
	-	`sha256:593fd0c937567a9ebb7b59a6d95e7d8a7b1fa0fc763b376ad03b9ca01cca6c21`  
		Last Modified: Mon, 23 Mar 2026 17:59:06 GMT  
		Size: 2.6 MB (2649441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a5bbb8d2fa220c30c8415b59124d88fedf0676a6f37feb68efb9057bc6d64c3`  
		Last Modified: Mon, 23 Mar 2026 17:59:05 GMT  
		Size: 17.0 KB (16990 bytes)  
		MIME: application/vnd.in-toto+json
