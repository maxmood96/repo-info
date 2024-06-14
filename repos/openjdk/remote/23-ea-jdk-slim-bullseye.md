## `openjdk:23-ea-jdk-slim-bullseye`

```console
$ docker pull openjdk@sha256:4b42a20ea7044496795ee23088f16050bfe633a65b10d55bf60df53ed106d255
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-jdk-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:a720848bd97d3540155017f3a40ddce5b35bfb6eb5769349e1843ac5e2762293
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244248771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22ddf299aff7a450b3b3470643ebad699b997a32b8764190615454dceccaa09d`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 08 Jun 2024 00:50:48 GMT
ADD file:574b112227f85a83f5d80d2523398640537475d2a56fa4c622397c466c0b552b in / 
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
	-	`sha256:f7b75fe1f735933f47315080637abf01f87962d47f8636a07ff4535ed7a4a133`  
		Last Modified: Thu, 13 Jun 2024 01:26:15 GMT  
		Size: 31.4 MB (31434040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39227b55982e38938694224e8bbef747f9d6e8d42dd55f764e17408704d7708d`  
		Last Modified: Thu, 13 Jun 2024 18:29:38 GMT  
		Size: 1.4 MB (1378116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb1c29d310ba7fe8f0e83ce1831abb8b306d5b0755ddaf2e3175abedefe428ac`  
		Last Modified: Thu, 13 Jun 2024 18:29:40 GMT  
		Size: 211.4 MB (211436615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:92d41ef8ceea4ab646aaffb866f684dae3cfb63de92be284e82f8521f4b57482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2655852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f955c1139d07a351f0322dc6e738704e00ce4dfc0be54f78c6b046b67a4af32`

```dockerfile
```

-	Layers:
	-	`sha256:4a8f33509916f06a81cf0a26877b4279f193b11b9fac7312e936296d8457faa5`  
		Last Modified: Thu, 13 Jun 2024 18:29:38 GMT  
		Size: 2.6 MB (2638494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85969bf6f30d8de4c5752790fbc39af86d5dfafb0308a1fcacdd4910263f555a`  
		Last Modified: Thu, 13 Jun 2024 18:29:38 GMT  
		Size: 17.4 KB (17358 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-jdk-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:04a4c53bb8e351cbf24606f0a6bce5c1c1bdead9e776c644c0348ca25c30a69f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.8 MB (240761152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e9d00705a45228aff82181b7576fc339c776b3e0017985833450b83382fabcf`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 08 Jun 2024 00:50:48 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
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
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8abb9c6653ca6c247cb904f25b084470905f4d6682db52ade7c408705b3728c`  
		Last Modified: Thu, 13 Jun 2024 19:58:27 GMT  
		Size: 1.4 MB (1361905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8722b88156a1cb1b46a062cd05c8c0e579d88a8515c3534f1d97365b6611e63d`  
		Last Modified: Thu, 13 Jun 2024 20:01:57 GMT  
		Size: 209.3 MB (209312274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:76233985c26dbd3e2f029b4ce4bd7dec048345cb6d5223711fd9671791bd02c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2656461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad0649a679bc7eaa6b34ddfbedacd5947e3c423c129320f4a965693adb0ba42a`

```dockerfile
```

-	Layers:
	-	`sha256:dc0ca33c9d53d33a0a2718c224cbba126360ff2fcffdf0440b234edc473233ff`  
		Last Modified: Thu, 13 Jun 2024 20:01:52 GMT  
		Size: 2.6 MB (2638770 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:352811093d213d621ec5f441ce3e3d7c4f809c655a9ceceefcc1920763db20a9`  
		Last Modified: Thu, 13 Jun 2024 20:01:51 GMT  
		Size: 17.7 KB (17691 bytes)  
		MIME: application/vnd.in-toto+json
