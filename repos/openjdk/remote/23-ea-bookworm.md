## `openjdk:23-ea-bookworm`

```console
$ docker pull openjdk@sha256:5cb795f9ab7f0df3d21749ad9f86adc64ab05935f04d5c3acd2e0add03f32145
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:08562154caf7e3fca607568a2b0f636a9548601967763abe43c70b39381276a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.1 MB (366120474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f244cc3de6a33c23fd81a2ad69fdb99c12a69f4228d23c22237add6e240d6b83`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Jul 2024 01:24:49 GMT
ADD file:e8aac9b1598114ead96b4038c19d915b87f662ef342291d69c7e5255c5d731fc in / 
# Tue, 02 Jul 2024 01:24:50 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:48:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:48:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 06 Jul 2024 00:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Jul 2024 00:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Sat, 06 Jul 2024 00:48:12 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Jul 2024 00:48:12 GMT
ENV LANG=C.UTF-8
# Sat, 06 Jul 2024 00:48:12 GMT
ENV JAVA_VERSION=23-ea+30
# Sat, 06 Jul 2024 00:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/30/GPL/openjdk-23-ea+30_linux-x64_bin.tar.gz'; 			downloadSha256='847f053c0a1e23b388353fdfa7c43ebe7eae98f8221e43d561a0ad3a4c486681'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/30/GPL/openjdk-23-ea+30_linux-aarch64_bin.tar.gz'; 			downloadSha256='ef0255786108e95110839309fe5ed09fc730c0e3d78dd3d84d3f0f7e520a0d93'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 06 Jul 2024 00:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e9aef93137af6e967e7242f3b3c8ecd8e6f571d1e6fdd9e72db0befeeae3cf13`  
		Last Modified: Tue, 02 Jul 2024 01:28:26 GMT  
		Size: 49.6 MB (49554064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b365fa3e8dc16e70d89fab0e91f5242feb38ae3cfeb6655e654209ea109333`  
		Last Modified: Tue, 02 Jul 2024 02:00:17 GMT  
		Size: 24.0 MB (24049794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dbed71fc5444cf6889a21b002de3e7805e810aa88f91a9ca941b4e3880246d1`  
		Last Modified: Tue, 02 Jul 2024 02:00:35 GMT  
		Size: 64.1 MB (64142928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce04a4c91bce17b4cf4f759c7dcde6e8ee6a8dd1d370997a83cc58ba26fa615`  
		Last Modified: Mon, 08 Jul 2024 20:57:11 GMT  
		Size: 16.9 MB (16943071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6af227165afbe9cb7ddaed8efcbb0359925f6d2cd8e5a707ee9f92c5e0fe3d2`  
		Last Modified: Mon, 08 Jul 2024 20:57:15 GMT  
		Size: 211.4 MB (211430617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:e35a0f53a35403d42746e3f0c032bd666fd7626aa3028717ca7f94c66785d457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8239619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7285491e10775cb1754d596d95db1bafad58de291964edbcabdf78e8cd37909`

```dockerfile
```

-	Layers:
	-	`sha256:faa6ed96c658285ab3874036c7b4e2f2726145341416444f8ca5825d57bf0b4b`  
		Last Modified: Mon, 08 Jul 2024 20:57:11 GMT  
		Size: 8.2 MB (8221158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7656fc766c38f92e6e064a0527d31620c1aeadb393d044a62ba7d08394707b4`  
		Last Modified: Mon, 08 Jul 2024 20:57:10 GMT  
		Size: 18.5 KB (18461 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:1314cd96e800f7283cf6b5c72fcf8fe36eb1c0f9570e1227fe8a5a09b94bb8c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.2 MB (364190885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9f4b0ea9b880a3e64379acc2846eaa680dbf7d8b9e1a2f9d38de9c01f998883`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:29 GMT
ADD file:696648070a57689a69a184fda234045f7be4a8a9f3b2fff9031ff0a2d9914113 in / 
# Tue, 02 Jul 2024 00:39:29 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:50:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 03:51:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 06 Jul 2024 00:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Jul 2024 00:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Sat, 06 Jul 2024 00:48:12 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Jul 2024 00:48:12 GMT
ENV LANG=C.UTF-8
# Sat, 06 Jul 2024 00:48:12 GMT
ENV JAVA_VERSION=23-ea+30
# Sat, 06 Jul 2024 00:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/30/GPL/openjdk-23-ea+30_linux-x64_bin.tar.gz'; 			downloadSha256='847f053c0a1e23b388353fdfa7c43ebe7eae98f8221e43d561a0ad3a4c486681'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/30/GPL/openjdk-23-ea+30_linux-aarch64_bin.tar.gz'; 			downloadSha256='ef0255786108e95110839309fe5ed09fc730c0e3d78dd3d84d3f0f7e520a0d93'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 06 Jul 2024 00:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0bd1f8180c504ba389021ce74895ed487ccd8c70e2d9af3707934bc801ba28d8`  
		Last Modified: Tue, 02 Jul 2024 00:42:03 GMT  
		Size: 49.6 MB (49588448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b16610496e73ba3d120d519598b53fa8a2db4c80ccc097a5016ad44aedd0654b`  
		Last Modified: Tue, 02 Jul 2024 04:01:41 GMT  
		Size: 23.6 MB (23591145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a6ab51b82df5ee608db374a16686eefb99bc53834af17064184653121729b3`  
		Last Modified: Tue, 02 Jul 2024 04:01:58 GMT  
		Size: 64.0 MB (63994637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2053aae84813025bf8ab96db13380e2938f95a3609c3bda3e2d1d9b419ace555`  
		Last Modified: Mon, 08 Jul 2024 20:59:06 GMT  
		Size: 17.7 MB (17727137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f58b56a13c86bfe2553d72bdf3c893cc6e8d66ddf0f5797fc6362896c11e0e`  
		Last Modified: Mon, 08 Jul 2024 21:04:54 GMT  
		Size: 209.3 MB (209289518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:a96ea21668307fa0d9c9e15950deccdfa41ebc2f5bd9692eb88a72fe175ffdca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8377622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7e18bd9309ae0c2eaa825e712d9f3be77250d04751d397a98e6a452ed31a4ca`

```dockerfile
```

-	Layers:
	-	`sha256:baf0261c6bdc2700ae3d993b2835bcec35f311b65db40a8de6828649dd30cc49`  
		Last Modified: Mon, 08 Jul 2024 21:04:50 GMT  
		Size: 8.4 MB (8358819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09816b7151915e8492bef653f280f616cf04d9726a22916c619f51cc23aaabe0`  
		Last Modified: Mon, 08 Jul 2024 21:04:50 GMT  
		Size: 18.8 KB (18803 bytes)  
		MIME: application/vnd.in-toto+json
