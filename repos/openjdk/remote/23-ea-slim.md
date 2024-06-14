## `openjdk:23-ea-slim`

```console
$ docker pull openjdk@sha256:b16d0155cd52d0da066934a9f2deb353303910e458effccfcbbc396647306d82
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:e13b48530567e19e0ccccfbd09fa15c7388e950805042c523c821b66cf489044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.4 MB (244410458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afe9cb757d070c5449463b0705e8f2499d2ba0d82e46e8422100316c01bf5138`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 08 Jun 2024 00:50:48 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
# Sat, 08 Jun 2024 00:50:48 GMT
CMD ["bash"]
# Sat, 08 Jun 2024 00:50:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Jun 2024 00:50:48 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Sat, 08 Jun 2024 00:50:48 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Jun 2024 00:50:48 GMT
ENV LANG=C.UTF-8
# Sat, 08 Jun 2024 00:50:48 GMT
ENV JAVA_VERSION=23-ea+26
# Sat, 08 Jun 2024 00:50:48 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/26/GPL/openjdk-23-ea+26_linux-x64_bin.tar.gz'; 			downloadSha256='a2a36c7b3c5fd89c6e392ba88a45a4647e482eab6b703595e2842e1b23c77ec9'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/26/GPL/openjdk-23-ea+26_linux-aarch64_bin.tar.gz'; 			downloadSha256='17a271b2853bc67590282ab01cceae8109012bc87ea2e07f7d5fefb55dd3192b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 08 Jun 2024 00:50:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4729de2f67f294238729f5ec73db83ce3bdb8ccf6cfab3ee99a2eee3a5e752`  
		Last Modified: Thu, 13 Jun 2024 18:29:45 GMT  
		Size: 3.8 MB (3821795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32fddb0b301ace12a79d1a5260eb118ace3304c09e49d4a23cbdd550e3223201`  
		Last Modified: Thu, 13 Jun 2024 18:29:50 GMT  
		Size: 211.4 MB (211438233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:a85004bbaf6d630862efdd0f37eba0423b3337fd1a5039db3feec19a7d185d49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2365546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4b08292988811233792866d4c7a5d6629783b73147f56e564dd465833d0b0ad`

```dockerfile
```

-	Layers:
	-	`sha256:a53573861d042899c280546efd34e9e603e2e1dc366a586ac3123952b0d81a5d`  
		Last Modified: Thu, 13 Jun 2024 18:29:45 GMT  
		Size: 2.3 MB (2346316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f88bbfd206b562823a6c3111509f714a0b492fe53f8c69b659ecf5cc9fd773a`  
		Last Modified: Thu, 13 Jun 2024 18:29:44 GMT  
		Size: 19.2 KB (19230 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:3be9887c8940800125ed7ce318e897942d163a3f10538d153b6b0cb7b4d69a3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.1 MB (242124241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e324c1182bf94fc00e6627fc65d648a68c3beda4e54fb94b773257533bde793`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 08 Jun 2024 00:50:48 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
# Sat, 08 Jun 2024 00:50:48 GMT
CMD ["bash"]
# Sat, 08 Jun 2024 00:50:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Jun 2024 00:50:48 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Sat, 08 Jun 2024 00:50:48 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Jun 2024 00:50:48 GMT
ENV LANG=C.UTF-8
# Sat, 08 Jun 2024 00:50:48 GMT
ENV JAVA_VERSION=23-ea+26
# Sat, 08 Jun 2024 00:50:48 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/26/GPL/openjdk-23-ea+26_linux-x64_bin.tar.gz'; 			downloadSha256='a2a36c7b3c5fd89c6e392ba88a45a4647e482eab6b703595e2842e1b23c77ec9'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/26/GPL/openjdk-23-ea+26_linux-aarch64_bin.tar.gz'; 			downloadSha256='17a271b2853bc67590282ab01cceae8109012bc87ea2e07f7d5fefb55dd3192b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 08 Jun 2024 00:50:48 GMT
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
	-	`sha256:cd292dabc17bcee1dda4f1e8963f3ced3322489d7a5be255e3634e42305b0aba`  
		Last Modified: Thu, 13 Jun 2024 20:00:13 GMT  
		Size: 209.3 MB (209314756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:1b21449da95f990a13587d6585b3387fc0b054fd5c14108753d0792dc7942541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2366303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adb86c3abf19df55e5d09900e81a7b2035e56ed26a83493b3e5cf25ffd0b93d2`

```dockerfile
```

-	Layers:
	-	`sha256:b5cefa25f977eca07b3269d328239d35268ea47276bbe48cd632532bd38ccdd7`  
		Last Modified: Thu, 13 Jun 2024 20:00:08 GMT  
		Size: 2.3 MB (2346670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a2eb476fe2f2c2e978a970b28885dd7ca0508738f6cb0fb6d3f172c0d8a58d6`  
		Last Modified: Thu, 13 Jun 2024 20:00:07 GMT  
		Size: 19.6 KB (19633 bytes)  
		MIME: application/vnd.in-toto+json
