## `openjdk:25-ea-jdk-slim-bullseye`

```console
$ docker pull openjdk@sha256:21266f5cb022e11e63cfbff243ff1c2b9bb0798a2eaef2396cee0ffb3266b198
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-jdk-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:3be6485efdca749450b7d793bf0c873c36a9df175c6412cfb6b74c3dc46ec855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.6 MB (243595426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d50cdbba093d5450595a5ebed516e4821affb4427fa4655ef5f1cba40822d8db`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1742169600'
# Fri, 21 Mar 2025 00:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Mar 2025 00:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 21 Mar 2025 00:48:13 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 21 Mar 2025 00:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 00:48:13 GMT
ENV JAVA_VERSION=25-ea+15
# Fri, 21 Mar 2025 00:48:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/15/GPL/openjdk-25-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='7456a38bfdaa0d7a8a4aef20ff86803e727f250350b35aa263570c5df1dc46e5'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/15/GPL/openjdk-25-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='30fab25ab72d34be3cb4ec7b0d372c0642d7dc7f824e3370b05501141245ba7b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 21 Mar 2025 00:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:55147cbf65d4d152c070165835355b8ea7a090d48d81ba52cbeb9bbe8d629fc0`  
		Last Modified: Mon, 17 Mar 2025 22:17:31 GMT  
		Size: 30.3 MB (30253836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9251365ee22fb1bbe3a28b2764f6d2170261b905e64881a26fbc76531e5c3169`  
		Last Modified: Fri, 21 Mar 2025 17:12:53 GMT  
		Size: 1.4 MB (1377192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7cb380c16e2cd10e2ccef4e3be0ffe774eff57d6a7bdfbb1552efac03319eb6`  
		Last Modified: Fri, 21 Mar 2025 17:12:56 GMT  
		Size: 212.0 MB (211964398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:f00db66aba3430c627cf0f9a4eb7d963d8f885df3ef83958062fd1edaa4fcedb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2844863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc4315fcf54f8c95060b76823d873931a35224dc9bf10878fc53b8d4a24e4e17`

```dockerfile
```

-	Layers:
	-	`sha256:16ee007761608dd570d08f3f17640269032f96d1ec46eb2b6f1c5d2a3df498c8`  
		Last Modified: Fri, 21 Mar 2025 17:12:53 GMT  
		Size: 2.8 MB (2827293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f7a80a5f15f904f175fcda8f8a0273ae243781897e9c530477b0c2ff5281562`  
		Last Modified: Fri, 21 Mar 2025 17:12:53 GMT  
		Size: 17.6 KB (17570 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-jdk-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:a819f07e64ff446c75bc258e0eab898871ed2ea2192524d1e671594bf0aec887
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.0 MB (240035242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfac0141abcc346645d7bc13929dabe1e76d78cdab766e1a119a83572e600653`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
# Fri, 21 Mar 2025 00:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Mar 2025 00:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 21 Mar 2025 00:48:13 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 21 Mar 2025 00:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 00:48:13 GMT
ENV JAVA_VERSION=25-ea+15
# Fri, 21 Mar 2025 00:48:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/15/GPL/openjdk-25-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='7456a38bfdaa0d7a8a4aef20ff86803e727f250350b35aa263570c5df1dc46e5'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/15/GPL/openjdk-25-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='30fab25ab72d34be3cb4ec7b0d372c0642d7dc7f824e3370b05501141245ba7b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 21 Mar 2025 00:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6eba8885c82049d690776150810f32585aca6c3eba49f692753434bdaee447ec`  
		Last Modified: Mon, 17 Mar 2025 22:18:52 GMT  
		Size: 28.7 MB (28745923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5678ad60b709415e17943bc531e3f43337e0d0157061bede4b10b9f3d9786a76`  
		Last Modified: Fri, 21 Mar 2025 17:28:25 GMT  
		Size: 1.4 MB (1361285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f34b4bdba349e29b5b9a6be43e0da72d12a72309b2dced6f3cf6e147d654576`  
		Last Modified: Fri, 21 Mar 2025 17:28:30 GMT  
		Size: 209.9 MB (209928034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:0724c092ca7279a846459d5323844cc5f8c9f79d3c78ca3d53c32cfef424788e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2844656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3ce1feb8197ad762ba3b2df0aad3eadea007a923e05105377f9376f64ee8e18`

```dockerfile
```

-	Layers:
	-	`sha256:059295e27f9d82bd74bb86e6cb67e43ade84b49d01e3a31798e0dfebf53909b0`  
		Last Modified: Fri, 21 Mar 2025 17:28:25 GMT  
		Size: 2.8 MB (2826945 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f467be8cd3ad95fc9b843751b9a18d6aba4680d82cc9d42dee2a61ff16d43321`  
		Last Modified: Fri, 21 Mar 2025 17:28:25 GMT  
		Size: 17.7 KB (17711 bytes)  
		MIME: application/vnd.in-toto+json
