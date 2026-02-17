## `openjdk:26-rc-trixie`

```console
$ docker pull openjdk@sha256:35b0385e7d62554b92b18901634be8dcc91c7e1f6d0dacf85f847a0e5d29a143
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-rc-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:4dc421d48d552b77842e110657cb1e2ed78b7148dc10607da2049a876c80d52e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.8 MB (386817312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b25b8a1fbd3a17aa5c37a60621f64c600bf0d9ac5e874430a617542320b104f0`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:42:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 03:28:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 17 Feb 2026 19:30:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 19:30:44 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Tue, 17 Feb 2026 19:30:44 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 19:30:44 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 19:30:44 GMT
ENV JAVA_VERSION=26
# Tue, 17 Feb 2026 19:30:44 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/35/GPL/openjdk-26_linux-x64_bin.tar.gz'; 			downloadSha256='83c78367f8c81257beef72aca4bbbf8e6dac8ca2b3a4546a85879a09e6e4e128'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/35/GPL/openjdk-26_linux-aarch64_bin.tar.gz'; 			downloadSha256='403ccf451e88d0be9e1dec129fcb9318de9752121e0eb92dfa9a8cf06f249007'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 17 Feb 2026 19:30:44 GMT
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
	-	`sha256:03c2dfc059ba97d87c23d3d647bc001a64e196bf1447d020c39339d40778c339`  
		Last Modified: Tue, 17 Feb 2026 19:31:08 GMT  
		Size: 16.1 MB (16062902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31dd3580a98c17059e4b108893b46fb97cc9bbb9b53f5509fa680ad988174279`  
		Last Modified: Tue, 17 Feb 2026 19:31:16 GMT  
		Size: 228.1 MB (228060083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-rc-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:2162d901392352ef7f1cdc879c65c4399fc84efbd725c776ee148bf7e1c0b776
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8528324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca124cb2ff8adb6f843a090293899beb611b456fae4c16f15c5d7c98611da8c3`

```dockerfile
```

-	Layers:
	-	`sha256:896132d728b9f58d2bb68a80a2ce981529141ac3d8f33a53f70fc745aeb5a48e`  
		Last Modified: Tue, 17 Feb 2026 19:31:08 GMT  
		Size: 8.5 MB (8510991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bb145ca5caf7e3a71da0a69f7ba3c78464e48b3c90b2a86bce8fa86aae61eec`  
		Last Modified: Tue, 17 Feb 2026 19:31:08 GMT  
		Size: 17.3 KB (17333 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-rc-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:e90a1982916749a49006bd5b4833b57cba282f8c91eec70bfbe38785bfbda678
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.3 MB (384327918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95d32583b6c87a24574be900e9748f26c6faaeccbd08c3c474e1d78fe14664b9`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:46:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 03:47:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 17 Feb 2026 19:29:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 19:30:02 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Tue, 17 Feb 2026 19:30:02 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 19:30:02 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 19:30:02 GMT
ENV JAVA_VERSION=26
# Tue, 17 Feb 2026 19:30:02 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/35/GPL/openjdk-26_linux-x64_bin.tar.gz'; 			downloadSha256='83c78367f8c81257beef72aca4bbbf8e6dac8ca2b3a4546a85879a09e6e4e128'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/35/GPL/openjdk-26_linux-aarch64_bin.tar.gz'; 			downloadSha256='403ccf451e88d0be9e1dec129fcb9318de9752121e0eb92dfa9a8cf06f249007'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 17 Feb 2026 19:30:02 GMT
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
	-	`sha256:f2eec1eb966a3e89b9eb555c7903a4858a5434ea26e2f0e8e589a225ecdab234`  
		Last Modified: Tue, 17 Feb 2026 19:30:28 GMT  
		Size: 16.1 MB (16071566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a25180e5f6621fa88680c40f2bd5c5bd73df95f4ac8d0dc1e357128e4f949f`  
		Last Modified: Tue, 17 Feb 2026 19:30:32 GMT  
		Size: 226.0 MB (225988642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-rc-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:6465d8c5757d5eaf94a46cf67ae9300250301daf6499a5e83d75bc9f9431d978
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8723184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9c666665c89146a905bf8d41f2b1f1502b6e3638c4b01f6ef5e36c6bdc58d7c`

```dockerfile
```

-	Layers:
	-	`sha256:b101eed399400a5df28b36d33205a0f3288ecd5ebc241a630791a6648f94125e`  
		Last Modified: Tue, 17 Feb 2026 19:30:28 GMT  
		Size: 8.7 MB (8705757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c3a1a0a67a34aada37a3e8a4d3935ad230d599d0de1c9b8a988624cc5c2d79b`  
		Last Modified: Tue, 17 Feb 2026 19:30:27 GMT  
		Size: 17.4 KB (17427 bytes)  
		MIME: application/vnd.in-toto+json
