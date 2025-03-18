## `openjdk:25-ea-14-slim-bullseye`

```console
$ docker pull openjdk@sha256:061815fd8db41048c7b9b3e777c9da4ee088414340a89ba7aa887aa4e129a341
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-14-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:efed5a4cdf485b75a0e1b33c65f9e9649760881aeb01b2c00a79ba4df6dc405f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.6 MB (243557415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f5a27c87238d1f80777d22f7eccc2052955621b81968e64c3b317bb830a111d`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 15 Mar 2025 00:48:15 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1742169600'
# Sat, 15 Mar 2025 00:48:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 15 Mar 2025 00:48:15 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Sat, 15 Mar 2025 00:48:15 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 15 Mar 2025 00:48:15 GMT
ENV LANG=C.UTF-8
# Sat, 15 Mar 2025 00:48:15 GMT
ENV JAVA_VERSION=25-ea+14
# Sat, 15 Mar 2025 00:48:15 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/14/GPL/openjdk-25-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='5fc0ecfeaad76f5acd86d6f0d28755072d9b2531d87629a245059f33b7d31c9f'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/14/GPL/openjdk-25-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='655f70de3b6c5247ab18bc41b57791463b6bbd0275845c6026201fb9a1a04032'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 15 Mar 2025 00:48:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:55147cbf65d4d152c070165835355b8ea7a090d48d81ba52cbeb9bbe8d629fc0`  
		Last Modified: Mon, 17 Mar 2025 22:17:31 GMT  
		Size: 30.3 MB (30253836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d1a35e57299a1f3427c282052f759d2ba14dd8383110e61e06b7904d282f834`  
		Last Modified: Mon, 17 Mar 2025 23:19:18 GMT  
		Size: 1.4 MB (1377253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3084d0e14d2fb6dacb5292c31ad93c252d8cc3e0dcb40fa684ed687844a59d9d`  
		Last Modified: Mon, 17 Mar 2025 23:19:24 GMT  
		Size: 211.9 MB (211926326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-14-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:e7a29dbfb77be216d6fdaf13960d6cc19275a97c7354eca9cad6cb5529d87f31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2844862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:783bd0102ab4939fa5b5591763d8c5bbbd38456f83503651f390cbbb5f201fdf`

```dockerfile
```

-	Layers:
	-	`sha256:d0dd8920577dfe1e2f52105867272344451b99ce9d76784642e3ce70f788d129`  
		Last Modified: Mon, 17 Mar 2025 23:19:18 GMT  
		Size: 2.8 MB (2827293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d4d8be92162055069a440089e918b4d1a0e0b884ebed1fdc52d1bf232f15460`  
		Last Modified: Mon, 17 Mar 2025 23:19:17 GMT  
		Size: 17.6 KB (17569 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-14-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:c4329d37d1f6f2244b3f4a46d4d2c6c9b8a7682e10eeffa25312da24ede42578
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.0 MB (239987481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf4b636993413bf66a47a43cd76085f5ceafb21d2e17f0000cb8a09660031222`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 15 Mar 2025 00:48:15 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
# Sat, 15 Mar 2025 00:48:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 15 Mar 2025 00:48:15 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Sat, 15 Mar 2025 00:48:15 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 15 Mar 2025 00:48:15 GMT
ENV LANG=C.UTF-8
# Sat, 15 Mar 2025 00:48:15 GMT
ENV JAVA_VERSION=25-ea+14
# Sat, 15 Mar 2025 00:48:15 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/14/GPL/openjdk-25-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='5fc0ecfeaad76f5acd86d6f0d28755072d9b2531d87629a245059f33b7d31c9f'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/14/GPL/openjdk-25-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='655f70de3b6c5247ab18bc41b57791463b6bbd0275845c6026201fb9a1a04032'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 15 Mar 2025 00:48:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6eba8885c82049d690776150810f32585aca6c3eba49f692753434bdaee447ec`  
		Last Modified: Mon, 17 Mar 2025 22:18:52 GMT  
		Size: 28.7 MB (28745923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b76e8dac6bda20d60bbc8e1c24d815653af8ea9c2c3c13732d813d3ae2c1f773`  
		Last Modified: Tue, 18 Mar 2025 03:01:50 GMT  
		Size: 1.4 MB (1361261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af806bdb31360264f80f932ce38ba47869a82c6ea7f5984bd163a22387bcf7c9`  
		Last Modified: Tue, 18 Mar 2025 03:02:11 GMT  
		Size: 209.9 MB (209880297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-14-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:d4a52fa0f4829bfe924a1f632229346a02605ac553280d7385fda0b166bc4a4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2844657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:504f70992a49335818344b15c422a946676801f96d1193eae6b14e2740398910`

```dockerfile
```

-	Layers:
	-	`sha256:99d5dbaf2754bdde5050c422174b10ab9d307b69e88027907dc54e5130eb4ec1`  
		Last Modified: Tue, 18 Mar 2025 03:01:50 GMT  
		Size: 2.8 MB (2826945 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:725b643cbe4ec6154ab61686209f1243eaab2e20ae0207e6ab0683c5463b49ee`  
		Last Modified: Tue, 18 Mar 2025 03:01:49 GMT  
		Size: 17.7 KB (17712 bytes)  
		MIME: application/vnd.in-toto+json
