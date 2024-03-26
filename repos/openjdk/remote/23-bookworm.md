## `openjdk:23-bookworm`

```console
$ docker pull openjdk@sha256:ee3ed6fd94376731e735d92445fdcef95dbdecca04962189e5b21b57b574c1fb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:bb319a6a9a2c3e699d73b7d8065875ee3c2114c456863b27cbb588cd4f5456b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.5 MB (357517604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd83d7d07e37f2e08de128ddd4ae0674ed9b3a43f776078207b0d3e2c84a0957`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 Mar 2024 01:20:46 GMT
ADD file:b18b4c32dd8042f45097997c732dc29b3917fd7d5f337f9e772eee5875fbe6f1 in / 
# Tue, 12 Mar 2024 01:20:46 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 05:53:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 05:53:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Mar 2024 18:48:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 22 Mar 2024 18:48:16 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 22 Mar 2024 18:48:16 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Mar 2024 18:48:16 GMT
ENV LANG=C.UTF-8
# Fri, 22 Mar 2024 18:48:16 GMT
ENV JAVA_VERSION=23-ea+15
# Fri, 22 Mar 2024 18:48:16 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/15/GPL/openjdk-23-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='c17995b5c67b845af47704e2a664f5b6ab540f968cfae06972a7562144b7634a'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/15/GPL/openjdk-23-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='804a15db8c406a0d70ad5a2da125339de3ff66759107fdd75bc6323d6d0cc5d4'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 22 Mar 2024 18:48:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:71215d55680cf0ab2dcc0e1dd65ed76414e3fb0c294249b5b9319a8fa7c398e4`  
		Last Modified: Tue, 12 Mar 2024 01:25:15 GMT  
		Size: 49.6 MB (49552196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb8f9c23302e175d87a827f0a1c376bd59b1f6949bd3bc24ab8da0d669cdfa0`  
		Last Modified: Tue, 12 Mar 2024 06:02:24 GMT  
		Size: 24.0 MB (24046734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f899db30843f8330d5a40d1acb26bb00e93a9f21bff253f31c20562fa264767`  
		Last Modified: Tue, 12 Mar 2024 06:02:43 GMT  
		Size: 64.1 MB (64140360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f76f3fcb9ca20f206f95ea68ab40dd2e473611e2e71a362e083251505ac4ecd`  
		Last Modified: Mon, 25 Mar 2024 19:12:51 GMT  
		Size: 16.9 MB (16945824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:647b239177eb2253477b30ca050f955582d1fadf5401141dae17145abcc0fad0`  
		Last Modified: Mon, 25 Mar 2024 19:12:55 GMT  
		Size: 202.8 MB (202832490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:2a2d05f411963e17c46587715c4b71c73a542390ca2fa607bc6c9729721e2576
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8248110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5917c62681aadf202002b02d1f123eb984dec448a099af62e2edc53d086a0ddc`

```dockerfile
```

-	Layers:
	-	`sha256:425066c94a8761dbba4bc16ae396f524ef11341356e141d9abaa3020159797ee`  
		Last Modified: Mon, 25 Mar 2024 19:12:50 GMT  
		Size: 8.2 MB (8229203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ca2f6d60930dd2d9f36fc3eccfae503352a108bf7e2d7b01c5bd5f21041902e`  
		Last Modified: Mon, 25 Mar 2024 19:12:50 GMT  
		Size: 18.9 KB (18907 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:fda6398209f5c68bdc50d27e53b79436220fa05e0914ede25e7bfb8ae8b6a366
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.6 MB (355618087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6774a25dc9ead5b8ffd677659ef1b3ac3180e69cc3f9f97070fb7c9c4d77b0ff`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:26 GMT
ADD file:9b51ed214f9332acf3126d841440c24eed0beac4062487fb360b288f628454dc in / 
# Tue, 12 Mar 2024 00:45:27 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:24:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:24:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Mar 2024 18:48:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 22 Mar 2024 18:48:16 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 22 Mar 2024 18:48:16 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Mar 2024 18:48:16 GMT
ENV LANG=C.UTF-8
# Fri, 22 Mar 2024 18:48:16 GMT
ENV JAVA_VERSION=23-ea+15
# Fri, 22 Mar 2024 18:48:16 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/15/GPL/openjdk-23-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='c17995b5c67b845af47704e2a664f5b6ab540f968cfae06972a7562144b7634a'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/15/GPL/openjdk-23-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='804a15db8c406a0d70ad5a2da125339de3ff66759107fdd75bc6323d6d0cc5d4'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 22 Mar 2024 18:48:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6ee0baa58a3d368515336c1b5c1cade29c975e1b49a832f19e22f4c46f4a23a7`  
		Last Modified: Tue, 12 Mar 2024 00:48:33 GMT  
		Size: 49.6 MB (49590984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992a857ef57584af4efb4c62d68456f1e8513c95d6248fd796a9ea7f45da4d79`  
		Last Modified: Tue, 12 Mar 2024 01:34:28 GMT  
		Size: 23.6 MB (23582876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3861a6536e4e911503e7d2fc8f93228491ba45d1e5def0d2f3723e32e03d7466`  
		Last Modified: Tue, 12 Mar 2024 01:34:50 GMT  
		Size: 64.0 MB (63990914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17436a1bcc9ca1dbdb0bc455f606f09462af1bdc6826599ce5bce2e7ab9f1a93`  
		Last Modified: Sat, 16 Mar 2024 15:53:20 GMT  
		Size: 17.7 MB (17728967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d40b176de3f8c8b0b772d4224482dad5779298f52a28abbf5ed1e12a1e687aef`  
		Last Modified: Mon, 25 Mar 2024 19:56:45 GMT  
		Size: 200.7 MB (200724346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:8cfd678d3fcf6c6770ba32a63d6fe736e454a5cd163e756d1f01ace70ea522d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8384259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39859a4ad01e6bc8fb0e15269e04e494ea568e42d76dfdb4f0a4c3cc555d5a79`

```dockerfile
```

-	Layers:
	-	`sha256:debe4fed9952871ae920ac6fdd417115adfeaf67745648004444e336c6bf963b`  
		Last Modified: Mon, 25 Mar 2024 19:56:40 GMT  
		Size: 8.4 MB (8365838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17cd3d37016cd502abdacbfdd243d0de4e594b638daf849fae8798bed0af9765`  
		Last Modified: Mon, 25 Mar 2024 19:56:39 GMT  
		Size: 18.4 KB (18421 bytes)  
		MIME: application/vnd.in-toto+json
