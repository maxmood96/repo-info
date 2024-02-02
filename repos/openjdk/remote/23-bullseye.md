## `openjdk:23-bullseye`

```console
$ docker pull openjdk@sha256:dd946ef6ea1d139c52277ae83939a8a961f140ca57dcb436e806bda940435397
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:a6473b06989d388b45d3cbfbfac06aea900af35b616e09917bca48782703b991
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.7 MB (342725712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a7be47dfbcbe84fbb2efff6f67342ba3d3612f91ad20a49872cd029c2ff326a`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 26 Jan 2024 01:56:28 GMT
ADD file:4fa73c8d113df02c8656b74ab87563432215332f3de78446a02e5ab7d6e2ab7a in / 
# Fri, 26 Jan 2024 01:56:28 GMT
CMD ["bash"]
# Fri, 26 Jan 2024 01:56:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Jan 2024 01:56:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Jan 2024 01:56:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jan 2024 01:56:28 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 26 Jan 2024 01:56:28 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jan 2024 01:56:28 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jan 2024 01:56:28 GMT
ENV JAVA_VERSION=23-ea+7
# Fri, 26 Jan 2024 01:56:28 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/7/GPL/openjdk-23-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='b10ac9dc80cf8dd508c44072989f1327a05a95dfcbf0af1fc65571ac2de613a7'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/7/GPL/openjdk-23-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='b21ca578927851a80700167439bbb9cd75c7d60152d51240bac49be8dd548e7a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Jan 2024 01:56:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7faaa42ac0c18c9baf539c97a5c8f042d02a77b05380cb57759e4407385710dc`  
		Last Modified: Wed, 31 Jan 2024 22:40:15 GMT  
		Size: 55.1 MB (55056963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1efd1e766326156b6d61b11d929f560cb73024ca0ff2a896b23e8bc6e0044244`  
		Last Modified: Wed, 31 Jan 2024 23:33:27 GMT  
		Size: 15.8 MB (15765028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f124d049a72aebbe5ef2fd589921f51fde08aa5b66cfa8cf81748411af8874dc`  
		Last Modified: Wed, 31 Jan 2024 23:33:44 GMT  
		Size: 54.6 MB (54601507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e7a3a778281d50e43a05fbbfebe5c293bf2bc7bbfa485e2d9c0df6e57609368`  
		Last Modified: Wed, 31 Jan 2024 23:57:30 GMT  
		Size: 14.1 MB (14073085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9c91cf51a6a7329ba86c70b99a7e05a648da0893e2b36418990d4a86455555`  
		Last Modified: Wed, 31 Jan 2024 23:57:33 GMT  
		Size: 203.2 MB (203229129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:b91a652feec353b18c442c957f77680ea04cc5a86f3cae410ba8351293260a33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6974965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc5b233294697140bcc62669bbc95cc4d698a63f90c064bdfbbfbcb6b66c0eee`

```dockerfile
```

-	Layers:
	-	`sha256:5252c2c5c111ded49f4343da3c9e5c02c44b5329720f1d4c52af736692aafef8`  
		Last Modified: Wed, 31 Jan 2024 23:57:30 GMT  
		Size: 7.0 MB (6956076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:012d72cddedbc1b5ba6602f712309a35f8fcff1c478ad4c1c6f1ca7af8761f24`  
		Last Modified: Wed, 31 Jan 2024 23:57:30 GMT  
		Size: 18.9 KB (18889 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:2779269262c57cf61df51b16c8415476f617806340946bee31832026d36db49f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.8 MB (340818986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1947ab08df99adcbe8608ae914084a43cad9bc7728693353f4243e7305d9ea22`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 26 Jan 2024 01:56:28 GMT
ADD file:81cb49e646b9feb1ddeddea1cb6dbafa672a250f1553cc28eae09c955607236d in / 
# Fri, 26 Jan 2024 01:56:28 GMT
CMD ["bash"]
# Fri, 26 Jan 2024 01:56:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Jan 2024 01:56:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Jan 2024 01:56:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jan 2024 01:56:28 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 26 Jan 2024 01:56:28 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jan 2024 01:56:28 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jan 2024 01:56:28 GMT
ENV JAVA_VERSION=23-ea+7
# Fri, 26 Jan 2024 01:56:28 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/7/GPL/openjdk-23-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='b10ac9dc80cf8dd508c44072989f1327a05a95dfcbf0af1fc65571ac2de613a7'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/7/GPL/openjdk-23-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='b21ca578927851a80700167439bbb9cd75c7d60152d51240bac49be8dd548e7a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Jan 2024 01:56:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4b6eb2d0256d18652f84fd30c1db34ce9462e535a2d96fbf2f9044db000b13f5`  
		Last Modified: Wed, 31 Jan 2024 22:48:27 GMT  
		Size: 53.7 MB (53708267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a36799ce495b4202a2dd0034c9955834237665bad54a5154faf464f20da7eb84`  
		Last Modified: Wed, 31 Jan 2024 23:53:07 GMT  
		Size: 15.8 MB (15750615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da2c043d162bc242dc65d025ae4775153d19e07ae75f2d759ab1f51bdefb529`  
		Last Modified: Wed, 31 Jan 2024 23:53:22 GMT  
		Size: 54.7 MB (54699941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e361934ac48c39bb74079449b2f9bbddf18b39b92133150271ba85b2d8782bc`  
		Last Modified: Fri, 02 Feb 2024 14:13:35 GMT  
		Size: 15.5 MB (15527406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bedf5668b67827f75045d309ccb26e073e38435dc02a1f5a3078b43c6ad05c01`  
		Last Modified: Fri, 02 Feb 2024 14:13:39 GMT  
		Size: 201.1 MB (201132757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:69e1db239373dd658cfe21bb7b365f862cb233072e3b1ef3b0e2df8ac70cff90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7062632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23ad65a7470b9695cf23cbcd9ad90bd7ce226179757d750193dc6404b3a74a15`

```dockerfile
```

-	Layers:
	-	`sha256:48b4bc50ff83a4ca068cdf73dce2fb413e97d35754ef14d65e34c26b30ab6986`  
		Last Modified: Fri, 02 Feb 2024 14:13:34 GMT  
		Size: 7.0 MB (7043728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:364ca929a6988b4cec705bbda7a1ed350c5a2af2ae52f51f1312aa0a724f2e72`  
		Last Modified: Fri, 02 Feb 2024 14:13:34 GMT  
		Size: 18.9 KB (18904 bytes)  
		MIME: application/vnd.in-toto+json
