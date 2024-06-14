## `openjdk:24-jdk-slim-bookworm`

```console
$ docker pull openjdk@sha256:1cc29d7a402fa7eb616de87be55215a9625d998c55c7f2fb5747100078da48de
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-jdk-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:8899fdd43385aa8b3a7476f93c1c2381492f5a18ae8927ffe22bba88c054a08b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 MB (244456972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3f26a31b47eb69992fdd0c0093f52a12ca5551440003358a2b8b17a6fab1fb2`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 13 Jun 2024 01:20:56 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
# Thu, 13 Jun 2024 01:20:56 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 18:54:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Jun 2024 18:54:09 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Thu, 13 Jun 2024 18:54:09 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 18:54:09 GMT
ENV LANG=C.UTF-8
# Thu, 13 Jun 2024 18:54:09 GMT
ENV JAVA_VERSION=24-ea+2
# Thu, 13 Jun 2024 18:54:09 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/2/GPL/openjdk-24-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='5219b8df6c8c43be5dab2d1ab5251df85610360ab22789e497ee05c66fa4c7e6'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/2/GPL/openjdk-24-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='5632c71df051ca5b6640c3c2a09ca3dd2b3dd131ea632906bd0eef7033323223'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 13 Jun 2024 18:54:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867613481d7ee9948e352585c59409cbe8eb41529e8cddb424981b7ab9eb0f8e`  
		Last Modified: Fri, 14 Jun 2024 01:01:10 GMT  
		Size: 3.8 MB (3821798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b95ba62bbdb0fceb12eedb66da42f79d4bc955a47212ec7cbfb43038cee092c`  
		Last Modified: Fri, 14 Jun 2024 01:01:16 GMT  
		Size: 211.5 MB (211484744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:253f83ca709524f8cc152ea93211b3feb4fa3e7183613476642335b6c281e693
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2365517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3513b89571ae96476960c21ab80ef99def9ffa0e0bb4dec60bdb2faf388e18e3`

```dockerfile
```

-	Layers:
	-	`sha256:2e1753e18955cf2e50ba12509fc737335a4bba373d07203607383a1cbd58fecd`  
		Last Modified: Fri, 14 Jun 2024 01:01:10 GMT  
		Size: 2.3 MB (2346304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c13808f121582c7dc43d7f5651212b12681469b7d4335d7d6db47a533226e768`  
		Last Modified: Fri, 14 Jun 2024 01:01:10 GMT  
		Size: 19.2 KB (19213 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-jdk-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:61eeda5e5b62772e1fa2c90029067b2164cb882c6dc6948f067b467ecfe9bb1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.2 MB (242174188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42e27f8e37547992e4a0eaec7eed4bdad28bb45966c3d3bde8e2bc3de3ec2716`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 13 Jun 2024 00:39:50 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
# Thu, 13 Jun 2024 00:39:51 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 18:54:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Jun 2024 18:54:09 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Thu, 13 Jun 2024 18:54:09 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 18:54:09 GMT
ENV LANG=C.UTF-8
# Thu, 13 Jun 2024 18:54:09 GMT
ENV JAVA_VERSION=24-ea+2
# Thu, 13 Jun 2024 18:54:09 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/2/GPL/openjdk-24-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='5219b8df6c8c43be5dab2d1ab5251df85610360ab22789e497ee05c66fa4c7e6'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/2/GPL/openjdk-24-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='5632c71df051ca5b6640c3c2a09ca3dd2b3dd131ea632906bd0eef7033323223'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 13 Jun 2024 18:54:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb960144e9a3234b18ad0a695286d60905b47d016807f2c30ce00e0acd5b3ab5`  
		Last Modified: Thu, 13 Jun 2024 19:56:32 GMT  
		Size: 3.6 MB (3629819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92487804d9f896548f5460493303f44c112ce01b3b5ba3e42ee5cbaf170b8857`  
		Last Modified: Fri, 14 Jun 2024 04:07:02 GMT  
		Size: 209.4 MB (209364703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:6ffc78fcf59b5644c7c1b45e14148c1f73ae91454c8eccca1045d7830ff5c25d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2366276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:945a04db61ef5a16c26fd250a8e7f7b0ce07bd06b6589f30c14a0c993ea1bcdb`

```dockerfile
```

-	Layers:
	-	`sha256:5eb34afc1f6ef85a2a747f48715ce2fca3377bf2f33352fb91f2776625a723e2`  
		Last Modified: Fri, 14 Jun 2024 04:06:57 GMT  
		Size: 2.3 MB (2346658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8c393f25d5531d95536bc64dd05378da392af907d93c96e139d1681a19717f1`  
		Last Modified: Fri, 14 Jun 2024 04:06:57 GMT  
		Size: 19.6 KB (19618 bytes)  
		MIME: application/vnd.in-toto+json
