## `openjdk:22-ea-jdk-slim`

```console
$ docker pull openjdk@sha256:c2b383c1588fa190dfa53fbe97d6abe6528373f940ee65b72d5b34a92d6c0ef5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:22-ea-jdk-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:1de7908b93af72268c891a0a6018c47a4ef8ea567e71b50c5265c601af21925c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236057676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bf8e4a18aca1a0acbf51268f70ea8a94628133183e66534474bf28202f8a81d`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 06 Jan 2024 01:48:12 GMT
ADD file:9deb26e1dbc258df47629e6f8fbcea4e4b54e7673537cc925db16af858d9cc8d in / 
# Sat, 06 Jan 2024 01:48:12 GMT
CMD ["bash"]
# Sat, 06 Jan 2024 01:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Jan 2024 01:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Sat, 06 Jan 2024 01:48:12 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Jan 2024 01:48:12 GMT
ENV LANG=C.UTF-8
# Sat, 06 Jan 2024 01:48:12 GMT
ENV JAVA_VERSION=22-ea+30
# Sat, 06 Jan 2024 01:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/30/GPL/openjdk-22-ea+30_linux-x64_bin.tar.gz'; 			downloadSha256='b0bc58519b965bba6505b882e5666c273ca5d2c192c44ecd5daba5efd3716ae9'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/30/GPL/openjdk-22-ea+30_linux-aarch64_bin.tar.gz'; 			downloadSha256='3e4c06460b2bf71e6f50fe574073f25d071bbde07323e02521fe6bcd7b9a4517'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 06 Jan 2024 01:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2f44b7a888fa005d07c031d3cfad2a1c0344207def2ab9dbb97712425ff812c1`  
		Last Modified: Thu, 11 Jan 2024 02:42:28 GMT  
		Size: 29.1 MB (29125921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c594d23b16a63ce60f88fdd121b163bd5c1e47a4a4bb2c1c7d1b19ad0abeb8`  
		Last Modified: Fri, 12 Jan 2024 00:22:27 GMT  
		Size: 4.0 MB (4014786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70e84015963a0145301e3330b6c705866533f8e990e09d3e3f6c0cd486b218a6`  
		Last Modified: Fri, 12 Jan 2024 00:22:31 GMT  
		Size: 202.9 MB (202916969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-ea-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:a484a9f9ae4b52fcd8bad006bc1ea7977f49b7d4eae836c1b49988acbe6a849c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2056530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cdd869fb2ea285f95e21bffc65797e74eac84392f3c9e6cfa340e94f58b7477`

```dockerfile
```

-	Layers:
	-	`sha256:76aac0daf808a8097e62c7cd3979a96b61eb08d1c235f23ccd275be8ac61c2d7`  
		Last Modified: Fri, 12 Jan 2024 00:22:26 GMT  
		Size: 2.0 MB (2037187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d5d6a31f205f31f68fa3e73fba03a27ce2c89dc4eff63dfde4cbfe6e1d73673`  
		Last Modified: Fri, 12 Jan 2024 00:22:25 GMT  
		Size: 19.3 KB (19343 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:22-ea-jdk-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:40ccf6d43397695924aeba572723ee8797d6cea126769a3f4f2deef813ca2157
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233942617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:038b0b8700668d6c105c70e6a7cf313430a7e3a4977785b7451a78c1b14884f8`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:11 GMT
ADD file:262fd7bf0bc26e5d2a229fba52626e22b8a93beac29733acfc60e716c26e689d in / 
# Tue, 19 Dec 2023 01:41:11 GMT
CMD ["bash"]
# Sat, 06 Jan 2024 01:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Jan 2024 01:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Sat, 06 Jan 2024 01:48:12 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Jan 2024 01:48:12 GMT
ENV LANG=C.UTF-8
# Sat, 06 Jan 2024 01:48:12 GMT
ENV JAVA_VERSION=22-ea+30
# Sat, 06 Jan 2024 01:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/30/GPL/openjdk-22-ea+30_linux-x64_bin.tar.gz'; 			downloadSha256='b0bc58519b965bba6505b882e5666c273ca5d2c192c44ecd5daba5efd3716ae9'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/30/GPL/openjdk-22-ea+30_linux-aarch64_bin.tar.gz'; 			downloadSha256='3e4c06460b2bf71e6f50fe574073f25d071bbde07323e02521fe6bcd7b9a4517'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 06 Jan 2024 01:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:24e221e92a36ab5b0075dd156b4f2ff095532a9b0927946cf6070bb1bea208b8`  
		Last Modified: Tue, 19 Dec 2023 01:44:38 GMT  
		Size: 29.2 MB (29157269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2614bd11b588c96b15909791ce0a1d4f2faa851a036310cc2fe1b2deae203b7`  
		Last Modified: Wed, 20 Dec 2023 10:22:09 GMT  
		Size: 3.8 MB (3819909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce8212ec78910395dfd24f1372506dfd695148128296327216f60f02b533d2e5`  
		Last Modified: Tue, 09 Jan 2024 02:26:36 GMT  
		Size: 201.0 MB (200965439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-ea-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:1b0c7192b681d290f9e505b1719bdc0d75e6b58d2f5ad98caa5387a4c67a64fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2055764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a38b4d8ca994cf484d5e6d834b5e258e439c926fe18a70a87abb540fcc44ec5a`

```dockerfile
```

-	Layers:
	-	`sha256:67ae54acf2b57d7dcb9289399bb986eac6d59d93b31ca7341c641f0757a18684`  
		Last Modified: Tue, 09 Jan 2024 02:26:31 GMT  
		Size: 2.0 MB (2036561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e71775542c0bf7c49863bd7ae360eb805c761d5e7343c1d9420943ff40cd694f`  
		Last Modified: Tue, 09 Jan 2024 02:26:31 GMT  
		Size: 19.2 KB (19203 bytes)  
		MIME: application/vnd.in-toto+json
