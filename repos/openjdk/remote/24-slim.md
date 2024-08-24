## `openjdk:24-slim`

```console
$ docker pull openjdk@sha256:5e2eeaf47c73778ee1e1f7c2243f2e81a174d4c309d401a8754589bb63a76cf2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:8297cb9e51e5a037c5f65d6cf73c791da7d9117898c231bd5d7b24615edbb9c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.2 MB (245155673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8013c4b2ba5e3469d18c1dd150c63fba4a6da740481f6aac4da30a814c40e470`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Aug 2024 00:20:20 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
# Tue, 13 Aug 2024 00:20:20 GMT
CMD ["bash"]
# Fri, 23 Aug 2024 00:48:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 Aug 2024 00:48:14 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 23 Aug 2024 00:48:14 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Aug 2024 00:48:14 GMT
ENV LANG=C.UTF-8
# Fri, 23 Aug 2024 00:48:14 GMT
ENV JAVA_VERSION=24-ea+12
# Fri, 23 Aug 2024 00:48:14 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/12/GPL/openjdk-24-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='9a859e4f3840e3f0890051a26b06413cd18dc8a1b7d68b221f47b38ba2f5add4'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/12/GPL/openjdk-24-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='4631ab62c58dbecfc00983df819c9a669b3d4fb681d7f6c3d95af11b7aacf087'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 23 Aug 2024 00:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebc01a8a24ab45e6ef244279faa015459b82143178ec25ecffe38f09b45b1be6`  
		Last Modified: Fri, 23 Aug 2024 21:11:06 GMT  
		Size: 4.0 MB (4016745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d25b10ed3e30ca5b6ef91171f1cac51efd4979d74eb73585694712476624b98`  
		Last Modified: Fri, 23 Aug 2024 21:11:11 GMT  
		Size: 212.0 MB (212012696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:9234dbb41dd5d977c7db090447ed0eff1aa1e6235bd4638f882af74065e516b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad43b1c9a085bcff0bc927d724df3df4f71eb6022b069f525deef7ed14097cbf`

```dockerfile
```

-	Layers:
	-	`sha256:cbe70ee73d2e785aa35233400de20163a111b773ece0a724d2b656fccd895fd9`  
		Last Modified: Fri, 23 Aug 2024 21:11:06 GMT  
		Size: 2.4 MB (2365306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66622538937198937517679123923517adb3286128ebabab3cd0d6a61e9ba8c2`  
		Last Modified: Fri, 23 Aug 2024 21:11:05 GMT  
		Size: 19.2 KB (19229 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:7f4082a79d00330d04bf5ba8fd478e3e3d5b6ca500ec0f69542e41e2a33f5d7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.8 MB (242761951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d97adf27c7c707d0bf7eef8e1b960a93b7bdb7a7852ab7590d0e068570561c1e`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Aug 2024 00:39:51 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
# Tue, 13 Aug 2024 00:39:51 GMT
CMD ["bash"]
# Fri, 16 Aug 2024 18:48:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Aug 2024 18:48:14 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 16 Aug 2024 18:48:14 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Aug 2024 18:48:14 GMT
ENV LANG=C.UTF-8
# Fri, 16 Aug 2024 18:48:14 GMT
ENV JAVA_VERSION=24-ea+11
# Fri, 16 Aug 2024 18:48:14 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/11/GPL/openjdk-24-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='c8cc4f7709c86eca1eb249323b8502416afffc54ddffc85278182dc222b1dcd8'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/11/GPL/openjdk-24-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='cd79e2e9877e5f8efa2324bc78851af99fbd9dc936c41c7c07ba928efd889c21'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 16 Aug 2024 18:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043d4d1b1fc77f5b08a9240bc3e33d2d018f4c45dee42461a423875aecade4e7`  
		Last Modified: Sat, 17 Aug 2024 00:35:10 GMT  
		Size: 3.8 MB (3829915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ef19d9323d3d9d3c6364e4dbb0a9ae5b15ab83d7e4c610db202783ac3e6de9`  
		Last Modified: Sat, 17 Aug 2024 00:35:14 GMT  
		Size: 209.8 MB (209775508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:fd4acd6268d8dab7f81ec46638f347c325dbc9eb372dc4837dadf24ab0f76c2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ee944821063c82f507ad116ebf7506768eb6b79f629191601ac5e9740eee69e`

```dockerfile
```

-	Layers:
	-	`sha256:8b8c25e88378f390bea816dccca91cb8de8b336b8542e6122c8314f587fbf27a`  
		Last Modified: Sat, 17 Aug 2024 00:35:10 GMT  
		Size: 2.4 MB (2365660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be86d020c3121d1c44e955fd5c0823d8aa8ba3eb27ec56e7dc11d24061053027`  
		Last Modified: Sat, 17 Aug 2024 00:35:09 GMT  
		Size: 19.6 KB (19634 bytes)  
		MIME: application/vnd.in-toto+json
