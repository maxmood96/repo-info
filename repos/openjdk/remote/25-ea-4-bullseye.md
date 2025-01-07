## `openjdk:25-ea-4-bullseye`

```console
$ docker pull openjdk@sha256:16b74437dcbec9527d5bcbaab00ed3ece2eab053324eb2fdbdc74a703296ffcd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-4-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:99bb35b2fabdb826229e515cd8d2e2953f2b78a24c165370fba86376e62707b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.1 MB (351145389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e8aca19780699ea37597e5554f51aa390b5de80f226bd94814e8adf06ad8fd`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Jan 2025 19:53:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Jan 2025 19:53:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 03 Jan 2025 19:53:11 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Jan 2025 19:53:11 GMT
ENV LANG=C.UTF-8
# Fri, 03 Jan 2025 19:53:11 GMT
ENV JAVA_VERSION=25-ea+4
# Fri, 03 Jan 2025 19:53:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/4/GPL/openjdk-25-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='57eb4b2610608286fb271949bd4f1acb9ce6d550325d0797f445c1bd0587de50'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/4/GPL/openjdk-25-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='2ebebc0344b40c03cd47ecd8936fe2aee3f0624e5e2463340054d7174b3f4e1d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 03 Jan 2025 19:53:11 GMT
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
	-	`sha256:a92ebd6fdca8e79056c390ee3e0cbe772ed9ef8633a874a2a2fb2a90d52d1809`  
		Last Modified: Mon, 06 Jan 2025 20:28:16 GMT  
		Size: 14.1 MB (14071383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eede2ca9e4fc4048ef81383c0662d85ee4ad729d47ad8f579969d64333eb25d4`  
		Last Modified: Mon, 06 Jan 2025 20:28:22 GMT  
		Size: 213.0 MB (213023048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-4-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:943d17832e9897988c01a978dee021e33fb9369b255e953375d572c7e7be3f0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8383378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:765b71954b1d643e3d0509286376c236666034e35cfbdfe2573b2dcf2023cf40`

```dockerfile
```

-	Layers:
	-	`sha256:c9bc37a72d3ead894efab542629d286f10bc5b78ccb32e160d1c5cbca6f4f9fb`  
		Last Modified: Mon, 06 Jan 2025 20:28:16 GMT  
		Size: 8.4 MB (8364777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8eb264b8249290e734c037bfa6f0758c399299d0cacb5a1d8b2488d77f230c97`  
		Last Modified: Mon, 06 Jan 2025 20:28:16 GMT  
		Size: 18.6 KB (18601 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-4-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:b02b7969a0340db195ca6add9a2b4c051400d3407c8ab2fed6bb5131f92350a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.1 MB (349141161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:803b7ebbe24a78325d1a1056b6a637d3df5d720b8db754734f3cd4f085eb26cf`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Jan 2025 19:53:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Jan 2025 19:53:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 03 Jan 2025 19:53:11 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Jan 2025 19:53:11 GMT
ENV LANG=C.UTF-8
# Fri, 03 Jan 2025 19:53:11 GMT
ENV JAVA_VERSION=25-ea+4
# Fri, 03 Jan 2025 19:53:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/4/GPL/openjdk-25-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='57eb4b2610608286fb271949bd4f1acb9ce6d550325d0797f445c1bd0587de50'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/4/GPL/openjdk-25-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='2ebebc0344b40c03cd47ecd8936fe2aee3f0624e5e2463340054d7174b3f4e1d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 03 Jan 2025 19:53:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:447d428f9ffe60c6c8cc59e00901cd865a36737372ba05710598d7eaf0a1144d`  
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
	-	`sha256:c43843d4db248bd55b162c50c092e0af24e1906957688ece77c8fd78e7c62441`  
		Last Modified: Wed, 25 Dec 2024 11:59:36 GMT  
		Size: 15.5 MB (15525945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b01853d9f42a9432294f9d5d2d6c78e544b22d4d665daa4d70c71ae83672f3f`  
		Last Modified: Mon, 06 Jan 2025 20:31:57 GMT  
		Size: 211.0 MB (210973069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-4-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:d4b270079ad89206594694612a330e525681f14166791a470ad8c8f1eaf77079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8484483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a94dc27980848b002f28fb72a89b40d2b4e9ee180e73a6a1b93dc391f77d06f9`

```dockerfile
```

-	Layers:
	-	`sha256:4b268ed83f5ca417c1c268b44d257b9f32ce1a6b9e291ec67d1b38f330d0dc59`  
		Size: 8.5 MB (8465739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d58c43f14e2b3ff61619b404906fff49c6de1411dfd0e357ae60c3e05fb6f047`  
		Last Modified: Mon, 06 Jan 2025 20:31:52 GMT  
		Size: 18.7 KB (18744 bytes)  
		MIME: application/vnd.in-toto+json
