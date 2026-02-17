## `openjdk:26-rc-bookworm`

```console
$ docker pull openjdk@sha256:e1af5dfa6e6b414336404cda11ecf294d80a5744d3342d018ab7933e2d272610
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-rc-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:d0261a0b4a6d4ba24edd23579ce4ebc662fce330b4f5d73f2344de3b5cf510d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.9 MB (381915571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bdbeb6a4477bf48c83cb9f84cc900669713fc2e6e661e3097e5f29249a24c8f`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:41:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:28:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 19:31:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 19:31:42 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Tue, 17 Feb 2026 19:31:42 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 19:31:42 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 19:31:42 GMT
ENV JAVA_VERSION=26
# Tue, 17 Feb 2026 19:31:42 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/35/GPL/openjdk-26_linux-x64_bin.tar.gz'; 			downloadSha256='83c78367f8c81257beef72aca4bbbf8e6dac8ca2b3a4546a85879a09e6e4e128'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/35/GPL/openjdk-26_linux-aarch64_bin.tar.gz'; 			downloadSha256='403ccf451e88d0be9e1dec129fcb9318de9752121e0eb92dfa9a8cf06f249007'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 17 Feb 2026 19:31:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89edcaae7ec479668d9bf0891145726173a305c809a8c4165723ceaf15b5a05f`  
		Last Modified: Tue, 03 Feb 2026 02:41:49 GMT  
		Size: 24.0 MB (24038446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbceb003542957cee7df7b79249eaf0a71d21c5203d086969b565fb6dec85d86`  
		Last Modified: Tue, 03 Feb 2026 03:28:33 GMT  
		Size: 64.4 MB (64395971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d7af76ca79cb036a4fee2b9f2a48a51554ae1e8b0650fea2366495788db1f3`  
		Last Modified: Tue, 17 Feb 2026 19:32:05 GMT  
		Size: 16.9 MB (16944785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71675179bb72b3947b0ebffec8bbe89e8c62998b8ea61c9dcfacff4968256f95`  
		Last Modified: Tue, 17 Feb 2026 19:32:10 GMT  
		Size: 228.1 MB (228054886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-rc-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:968e41583207508f72858c721137277d58e982fead3f53df7901e5c1e3036e55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8686195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fe9aa9e351f90e6788235b9e3c8c2e090963db0d5c6ab6076abc97de0b4ff9c`

```dockerfile
```

-	Layers:
	-	`sha256:8fcc5dd34be1104c8b2766c57927cd95e9bed0c0d74f4b1e8e0ba753c72a2be8`  
		Last Modified: Tue, 17 Feb 2026 19:32:05 GMT  
		Size: 8.7 MB (8668844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4de2cb8c2b1f61024ab63058a49c4de2d6d73c1472c22e993056c013f33f8c1`  
		Last Modified: Tue, 17 Feb 2026 19:32:04 GMT  
		Size: 17.4 KB (17351 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-rc-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:6d9ee95cdcb8f80750c79e87eb0ce5dae46f8e5113b3d2520a8fdcbfafd904b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.2 MB (380159500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:888e4172dbae1df3cffdc9b1c6ff95acc7c48808ff0ddc87cf854a35dab28cba`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:44:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:46:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 19:30:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 19:31:02 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Tue, 17 Feb 2026 19:31:02 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 19:31:02 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 19:31:02 GMT
ENV JAVA_VERSION=26
# Tue, 17 Feb 2026 19:31:02 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/35/GPL/openjdk-26_linux-x64_bin.tar.gz'; 			downloadSha256='83c78367f8c81257beef72aca4bbbf8e6dac8ca2b3a4546a85879a09e6e4e128'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/35/GPL/openjdk-26_linux-aarch64_bin.tar.gz'; 			downloadSha256='403ccf451e88d0be9e1dec129fcb9318de9752121e0eb92dfa9a8cf06f249007'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 17 Feb 2026 19:31:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:64e8f4c09e7ac936ecc3deb0e61613f653224c28b2e35fa9d8e6e11cbdb5f911`  
		Last Modified: Tue, 03 Feb 2026 01:13:22 GMT  
		Size: 48.4 MB (48365956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:404413e6e45accf116074dace885c7ccf2917479ae04f2f46c046b6ae1909254`  
		Last Modified: Tue, 03 Feb 2026 02:44:54 GMT  
		Size: 23.6 MB (23604842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e9aa4982c2a67e202ea283fc3760e94d8d8b16966c616e01ad0238abbaac82`  
		Last Modified: Tue, 03 Feb 2026 03:46:50 GMT  
		Size: 64.5 MB (64479687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e75f74f450c7a955e93bf0efdd08056ae7261f63f5d37c7ca32bb97cc6c0692`  
		Last Modified: Tue, 17 Feb 2026 19:31:27 GMT  
		Size: 17.7 MB (17728528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f78a8e8e8613836b6ba2c61f293ed3ac29154bde62ae9d606905c8dc00801ac5`  
		Last Modified: Tue, 17 Feb 2026 19:31:32 GMT  
		Size: 226.0 MB (225980487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-rc-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:afacec7807846f88ce5974128f4a22e3b965b1e304184ca8369a8a0fc5b14176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8823111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf0cfe69f5b22859f06f7d60457d2e0cf456db0b322451fb517f898d9b80ea94`

```dockerfile
```

-	Layers:
	-	`sha256:527e81dad13ac9e89b1f7798db08e79efdda376f0d44f4940fd66194791b4672`  
		Last Modified: Tue, 17 Feb 2026 19:31:27 GMT  
		Size: 8.8 MB (8805665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00d6617412cdc9e1921707d1690f80cb3e53ae07a6c6832d8926025f177ea2a8`  
		Last Modified: Tue, 17 Feb 2026 19:31:26 GMT  
		Size: 17.4 KB (17446 bytes)  
		MIME: application/vnd.in-toto+json
