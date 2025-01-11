## `openjdk:25-ea-slim-bullseye`

```console
$ docker pull openjdk@sha256:de5fb88dd83f7fccf95abe0b3b0f34aa6f70379a3950f2d0135be81a6f3309d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:fd3bfc1fa74c3c104506e66c25922384e06e4fa2ef09eee02ce7765599794828
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.7 MB (244703521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a59a25d6a5aff4054ff720ec5471fb7bb6ab61945f110913bdcc6ffffa4f314`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
# Fri, 10 Jan 2025 07:52:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 07:52:09 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 10 Jan 2025 07:52:09 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Jan 2025 07:52:09 GMT
ENV LANG=C.UTF-8
# Fri, 10 Jan 2025 07:52:09 GMT
ENV JAVA_VERSION=25-ea+5
# Fri, 10 Jan 2025 07:52:09 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/5/GPL/openjdk-25-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='b4ee63f91536c06f46e6f0d9c45e820bc2cb552046df27aa5c77d0bacc35aa21'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/5/GPL/openjdk-25-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='43d1f9c863580d839b21121bc0c09ef0525d80ce1a3fbe26ea22fe2d77eadf7a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 10 Jan 2025 07:52:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6c87eefc1f428634061bcdc9ec95ccceecd7c7475d35a777479af83f64ee6915`  
		Last Modified: Tue, 24 Dec 2024 21:32:32 GMT  
		Size: 30.3 MB (30252643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94354cfed018203e2a865b914ec931b6fc62a2341364a2bfb889bbb4b4745772`  
		Last Modified: Sat, 11 Jan 2025 02:29:51 GMT  
		Size: 1.4 MB (1377261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4f61dfc8c2a77e0acd4a2834bd041f48a1fe3c4517dc787bcf4374717cc9485`  
		Last Modified: Sat, 11 Jan 2025 02:29:54 GMT  
		Size: 213.1 MB (213073617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:453de71f9f195210593e301769571ca356ca7e3c68e3b7c501f90d28a0816db9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2845471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d847d45450c5753bba895bf3b59ab2795fdbaeafa794e6c3dc1d7d70d0069b2`

```dockerfile
```

-	Layers:
	-	`sha256:0caf7b6b0579aecb0e843f876564bcacb11d1d5c2c56fc489f3b8437f68afa9a`  
		Last Modified: Sat, 11 Jan 2025 02:29:51 GMT  
		Size: 2.8 MB (2827914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01da7185b799fa295cac35dec4e209b1390474334ac3b46bacb22f8b40d7aee7`  
		Last Modified: Sat, 11 Jan 2025 02:29:51 GMT  
		Size: 17.6 KB (17557 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:dbd6aaa30eee2baa4486f9e8278ab6885d6a1dfaa0ed2abdb77087634bc8b2a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.1 MB (241141770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3740cbdbdeaf3f3e32c9a0d23e5787db42b98ee4cb2d4ae1ede752b123f9cd0b`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
# Fri, 10 Jan 2025 07:52:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 07:52:09 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 10 Jan 2025 07:52:09 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Jan 2025 07:52:09 GMT
ENV LANG=C.UTF-8
# Fri, 10 Jan 2025 07:52:09 GMT
ENV JAVA_VERSION=25-ea+5
# Fri, 10 Jan 2025 07:52:09 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/5/GPL/openjdk-25-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='b4ee63f91536c06f46e6f0d9c45e820bc2cb552046df27aa5c77d0bacc35aa21'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/5/GPL/openjdk-25-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='43d1f9c863580d839b21121bc0c09ef0525d80ce1a3fbe26ea22fe2d77eadf7a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 10 Jan 2025 07:52:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:879a6187682fc52c69294a2f450abdb54e257a50e8133ec6e89cb140345be6ce`  
		Last Modified: Tue, 24 Dec 2024 21:34:50 GMT  
		Size: 28.7 MB (28744853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca5c8f0fb84ba0a041b6e177e7fb8753ae3d2ea2da20fd79be83781ec01d2ac`  
		Last Modified: Sat, 11 Jan 2025 03:19:47 GMT  
		Size: 1.4 MB (1361268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0f1dd1baa1fe9bc44bd900d2893cece1cc732601d4c56a9f2b95e4bc57a535`  
		Last Modified: Sat, 11 Jan 2025 03:19:51 GMT  
		Size: 211.0 MB (211035649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:5e8b690d510ba1aa4ad019975c1edde15c5b2ca3d7505df51c240581af39053c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2845266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:debd18e9324fda1c7f55c1dc4f2cdd322ca49b2534ed17538259de5f49c2a48b`

```dockerfile
```

-	Layers:
	-	`sha256:d867085e32d1f73ee23d5da133645bc46351e46f18fb646ef43f6c7ce0d98b5c`  
		Last Modified: Sat, 11 Jan 2025 03:19:47 GMT  
		Size: 2.8 MB (2827566 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eeb841d110b1be96d831f199de822173db99e637aa897a232e21b53adfdd5fbc`  
		Last Modified: Sat, 11 Jan 2025 03:19:47 GMT  
		Size: 17.7 KB (17700 bytes)  
		MIME: application/vnd.in-toto+json
