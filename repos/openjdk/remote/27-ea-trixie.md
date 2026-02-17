## `openjdk:27-ea-trixie`

```console
$ docker pull openjdk@sha256:af1c8d0f1cb9a3278ded85a3a4bdb24b899d17bdc2359a0dee3c8cf445f86365
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:8140ffc87805a38cb6207e351b97e330b16a6649d6045b6de111b08b1b3c4bfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.2 MB (387248081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9c689f5c3002306d3b43c2697e1a7406d8aa4f9e5392ba73e537621461d55f6`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:42:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 03:28:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 17 Feb 2026 19:32:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 19:32:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 17 Feb 2026 19:32:13 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 19:32:13 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 19:32:13 GMT
ENV JAVA_VERSION=27-ea+9
# Tue, 17 Feb 2026 19:32:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/9/GPL/openjdk-27-ea+9_linux-x64_bin.tar.gz'; 			downloadSha256='63b3704a0d6aac8050df9534d12f1e063e64ceae89a77131e1a9f01e0d1e223b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/9/GPL/openjdk-27-ea+9_linux-aarch64_bin.tar.gz'; 			downloadSha256='58393a7f38ddf3532c68f68b614756b3cb7953bbd54e64897221be7f071ee41b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 17 Feb 2026 19:32:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ef235bf1a09a237b896b69935c8c8d917c9c6a78b538724911414afc0a96763c`  
		Last Modified: Tue, 03 Feb 2026 01:16:00 GMT  
		Size: 49.3 MB (49292952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954d6059ca7bdbb9ceb566ca2239e01ef312165659d656753d7dbace7771a591`  
		Last Modified: Tue, 03 Feb 2026 02:43:06 GMT  
		Size: 25.6 MB (25614010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e2021c4c8bd1a46b34d9608a9381afdc333600ee1ef3c94306ecf7373e1956`  
		Last Modified: Tue, 03 Feb 2026 03:29:16 GMT  
		Size: 67.8 MB (67787365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628440adeeb7b1623ac7c35363f4470cf6eb9d7766535c54a8f5518aef591c80`  
		Last Modified: Tue, 17 Feb 2026 19:32:36 GMT  
		Size: 16.1 MB (16062856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5589508c6f0676dc288d66ddbddafb43fbadfaeeecc2baf37c332f0369b4bbf0`  
		Last Modified: Tue, 17 Feb 2026 19:32:40 GMT  
		Size: 228.5 MB (228490898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:794070254d52571aca27de6eb7cc012aa274d439faa0dc580707b19aade3e101
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8528914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5455270d84f1b002df63bd2b7272cbde51494740e46954cff803cb61ce94cda`

```dockerfile
```

-	Layers:
	-	`sha256:34d6477c1aa75851d54fdcbfa318705373a188fd29edbf65d47c034567ebc841`  
		Last Modified: Tue, 17 Feb 2026 19:32:36 GMT  
		Size: 8.5 MB (8511018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42c129d2a37d724b349564713bc52b5e8370afd09e6d882d82b52bd829f74fd6`  
		Last Modified: Tue, 17 Feb 2026 19:32:35 GMT  
		Size: 17.9 KB (17896 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:6e840d6abea2ceca60cbd6cd77955ea0c27f9ff6e7c73522f337b3d40da84b9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.8 MB (384777985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2484ff4dc6b4c33e07c967881aa487cf51d79f4b74f115978077d8ef85229dba`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:46:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 03:47:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 17 Feb 2026 19:31:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 19:31:58 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 17 Feb 2026 19:31:58 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 19:31:58 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 19:31:58 GMT
ENV JAVA_VERSION=27-ea+9
# Tue, 17 Feb 2026 19:31:58 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/9/GPL/openjdk-27-ea+9_linux-x64_bin.tar.gz'; 			downloadSha256='63b3704a0d6aac8050df9534d12f1e063e64ceae89a77131e1a9f01e0d1e223b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/9/GPL/openjdk-27-ea+9_linux-aarch64_bin.tar.gz'; 			downloadSha256='58393a7f38ddf3532c68f68b614756b3cb7953bbd54e64897221be7f071ee41b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 17 Feb 2026 19:31:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1bd4defc8c5e5cda3d1685bbe52bfcd79e4448ee97883913300e5d29ca8fdb89`  
		Last Modified: Tue, 03 Feb 2026 01:15:56 GMT  
		Size: 49.7 MB (49652017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cace8fbd9245d4cb1b11d410baa101c40f315e70bee7d3ba014bb966a4da4517`  
		Last Modified: Tue, 03 Feb 2026 02:46:11 GMT  
		Size: 25.0 MB (25022688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8128ce97ccffb1094b6eafc78b5827499d0496944f3d357e222bfc29f01968`  
		Last Modified: Tue, 03 Feb 2026 03:47:30 GMT  
		Size: 67.6 MB (67593005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669f8db93526ad81c1a7339999534aefd9c7ed199209c57a7061abb2620760a1`  
		Last Modified: Tue, 17 Feb 2026 19:32:24 GMT  
		Size: 16.1 MB (16071558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5770ded5881a735a1594d4de51e63a8ec0dc22a50c6b8195effea6df43b9269`  
		Last Modified: Tue, 17 Feb 2026 19:32:28 GMT  
		Size: 226.4 MB (226438717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:c0fb28ee912b10705dd900b6d75565157e3c402b992b35cb052b4ccc40b0a9f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8723823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5c22a061ce9feed7c71b37272713ea808d7120e00d7415b14d791258735a754`

```dockerfile
```

-	Layers:
	-	`sha256:877e27b231bd6dd628d62e29b800ed960b25c43b173329ca285aad3904c94022`  
		Last Modified: Tue, 17 Feb 2026 19:32:24 GMT  
		Size: 8.7 MB (8705808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3acddd7fba51013b3c2dd95cff782d538097d900032e3c59fd4e7310b5c3404`  
		Last Modified: Tue, 17 Feb 2026 19:32:23 GMT  
		Size: 18.0 KB (18015 bytes)  
		MIME: application/vnd.in-toto+json
