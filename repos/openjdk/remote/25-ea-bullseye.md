## `openjdk:25-ea-bullseye`

```console
$ docker pull openjdk@sha256:c2554962fe7e924749565337c45af9353f6eb6a229fea021d150d973158e8052
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:91343d767ab527ed55ea4e2068ffe2b8a05e173df989f24c2a69c4d7f2710f07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.1 MB (351143133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:904374175b1c0b6c2c0afa9049b14afe9a9275ec78281dabc0601ded69e00987`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 07:52:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 07:52:09 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 10 Jan 2025 07:52:09 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Jan 2025 07:52:09 GMT
ENV LANG=C.UTF-8
# Fri, 10 Jan 2025 07:52:09 GMT
ENV JAVA_VERSION=25-ea+5
# Fri, 10 Jan 2025 07:52:09 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/5/GPL/openjdk-25-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='b4ee63f91536c06f46e6f0d9c45e820bc2cb552046df27aa5c77d0bacc35aa21'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/5/GPL/openjdk-25-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='43d1f9c863580d839b21121bc0c09ef0525d80ce1a3fbe26ea22fe2d77eadf7a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 10 Jan 2025 07:52:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5d6e107a26c2ffb6e234f04132358dea70a691a64c1152f984d2f2ba0e218c58`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 53.7 MB (53738957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2377065f3b700cf1b5e391d26c572c8b91892dd44acd75deebdab5e403b23175`  
		Last Modified: Tue, 24 Dec 2024 22:15:26 GMT  
		Size: 15.6 MB (15558293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee26b7a209f9a26720207792b237af3e19c0efeed8695e1e630fcd0feef9230`  
		Last Modified: Tue, 24 Dec 2024 23:16:05 GMT  
		Size: 54.8 MB (54753708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b4a93182829d4e6647d8e143c089d1aa6b16fff441336316ccf1b339b9b62db`  
		Last Modified: Sat, 11 Jan 2025 02:29:48 GMT  
		Size: 14.1 MB (14071607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d84df14d87bf1f527b677ee13b08d4b1f45f35c914f0197439a8490c06883f`  
		Last Modified: Sat, 11 Jan 2025 02:29:51 GMT  
		Size: 213.0 MB (213020568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:1aa588c6c19e75e9ed9e1fc8e93fe9289db95e694e02ddc444504a7ea9b372cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8383378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ec451dc8172a30d634b338fb4ae2cf55d47060d0d90c1254e857fe2856a47c6`

```dockerfile
```

-	Layers:
	-	`sha256:ddb963e1e6475232fae16dab77e0a81e36c84da920cfaa8bf9fb212b9045aa1f`  
		Last Modified: Sat, 11 Jan 2025 02:29:48 GMT  
		Size: 8.4 MB (8364777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1b500e24f686d32cf9791065dc900fca631aabfdda348693d5397f225a7299f`  
		Last Modified: Sat, 11 Jan 2025 02:29:48 GMT  
		Size: 18.6 KB (18601 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:a8f2777b307c6dcaf30d9776939a6db69a63ea6808a5d582dd0179eee65d743d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.2 MB (349150591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3120fcc6019d89d971a6a98743952df5817f3c0f4e5ce2bfad4e7fc6c8041e0`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 07:52:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 07:52:09 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 10 Jan 2025 07:52:09 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Jan 2025 07:52:09 GMT
ENV LANG=C.UTF-8
# Fri, 10 Jan 2025 07:52:09 GMT
ENV JAVA_VERSION=25-ea+5
# Fri, 10 Jan 2025 07:52:09 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/5/GPL/openjdk-25-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='b4ee63f91536c06f46e6f0d9c45e820bc2cb552046df27aa5c77d0bacc35aa21'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/5/GPL/openjdk-25-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='43d1f9c863580d839b21121bc0c09ef0525d80ce1a3fbe26ea22fe2d77eadf7a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 10 Jan 2025 07:52:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:447d428f9ffe60c6c8cc59e00901cd865a36737372ba05710598d7eaf0a1144d`  
		Last Modified: Tue, 24 Dec 2024 21:34:37 GMT  
		Size: 52.2 MB (52245698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eceb2e49ad0ea75b24fca7d94b98a8202f70828ce20fd23846a542d8dca2667d`  
		Last Modified: Wed, 25 Dec 2024 01:49:44 GMT  
		Size: 15.5 MB (15544017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f980dd00d0ffb99c81471a2f1d6dbe4936d0d24b2e81f9be4ad52c0cc28b66`  
		Last Modified: Wed, 25 Dec 2024 08:12:36 GMT  
		Size: 54.9 MB (54852432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b76479c78354ea5a5c0b1b7532f5adca25103a796405e3d01dfeeb0e9af4b21e`  
		Last Modified: Sat, 11 Jan 2025 03:18:56 GMT  
		Size: 15.5 MB (15526432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d1e1fdf123e445b229c3f4ef59ec02a8512284879a40e977b09972ea778d105`  
		Last Modified: Sat, 11 Jan 2025 03:19:02 GMT  
		Size: 211.0 MB (210982012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:18d09dc4b2c45251524f45311878a94c413ad751f5e39c9e22ac1e257f5be18e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8484483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50a066843eb6d0dfd0083e8548b96ef10236ce8984125d3b0f38146c998216ec`

```dockerfile
```

-	Layers:
	-	`sha256:7724d116ae95f8a94ef441d16e89f8a331a82b56df7e89d24dc6fda5c5a15853`  
		Last Modified: Sat, 11 Jan 2025 03:18:56 GMT  
		Size: 8.5 MB (8465739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ed022a630692b5514955439f421308d990c0daf0ca4ff37bd63beb4f247869d`  
		Last Modified: Sat, 11 Jan 2025 03:18:56 GMT  
		Size: 18.7 KB (18744 bytes)  
		MIME: application/vnd.in-toto+json
