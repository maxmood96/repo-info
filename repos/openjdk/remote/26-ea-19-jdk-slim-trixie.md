## `openjdk:26-ea-19-jdk-slim-trixie`

```console
$ docker pull openjdk@sha256:961d3a10a0f8b494ee616f25c9dde6bf0cc0008d52fe8d990bd78cd77a2ac7c1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-19-jdk-slim-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:8317998f3049cfd430c76d89c38fb062eb24e8f27dc31c1b4218e1ae15d7ed7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.0 MB (260972835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6bd10265c603e8a89a3cbd1baa73a29e1dbe6c3e92492063507969b7215299`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Sat, 11 Oct 2025 00:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 11 Oct 2025 00:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Sat, 11 Oct 2025 00:48:11 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 11 Oct 2025 00:48:11 GMT
ENV LANG=C.UTF-8
# Sat, 11 Oct 2025 00:48:11 GMT
ENV JAVA_VERSION=26-ea+19
# Sat, 11 Oct 2025 00:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/19/GPL/openjdk-26-ea+19_linux-x64_bin.tar.gz'; 			downloadSha256='9a89dcca644d59f40b82f6712c854e416d5b5fe80808c40868e1ba2d6d8e1e9e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/19/GPL/openjdk-26-ea+19_linux-aarch64_bin.tar.gz'; 			downloadSha256='2841b9fa0e22671fc0ee3e6ba1e87237d895446e7548021004f201a1ff5abd99'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 11 Oct 2025 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0a478a61dd4ee72e7db5650976c3447041bb726d3d8b3bb540093fc261357d`  
		Last Modified: Mon, 13 Oct 2025 21:03:09 GMT  
		Size: 5.3 MB (5330694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:932bce017639942620443fde0892ad83281ac2f0426f41d5b27bce701edfac75`  
		Last Modified: Mon, 13 Oct 2025 21:36:37 GMT  
		Size: 225.9 MB (225864375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-19-jdk-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:582bac011469ed76c3fd315455b76c6d3d6efe8a50e857c6d5de0df0ea5c54f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a557eff196a7afac79b301fc847b42c83c259ba8af1550ef6ec80feaae95fed`

```dockerfile
```

-	Layers:
	-	`sha256:e0365d863e1c3865bbd5a437b720614771658c307284a8c9cd170907b05dcb74`  
		Last Modified: Mon, 13 Oct 2025 21:24:12 GMT  
		Size: 2.3 MB (2282558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5d5551df4032aa571fe59a30789f0f2080f2e7c320984f2c1df8fd2930d728b`  
		Last Modified: Mon, 13 Oct 2025 21:24:13 GMT  
		Size: 19.4 KB (19412 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-19-jdk-slim-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:5149c6e0b2fdb062ea79d0715c0fbd54ed685a21db48a5426cdc1dae0474a38c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.5 MB (259493955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a06bb17c87c797d19eb760505d99e60adc4b15cd0c3247521c7a6c47ae2ee007`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Sat, 11 Oct 2025 00:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 11 Oct 2025 00:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Sat, 11 Oct 2025 00:48:11 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 11 Oct 2025 00:48:11 GMT
ENV LANG=C.UTF-8
# Sat, 11 Oct 2025 00:48:11 GMT
ENV JAVA_VERSION=26-ea+19
# Sat, 11 Oct 2025 00:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/19/GPL/openjdk-26-ea+19_linux-x64_bin.tar.gz'; 			downloadSha256='9a89dcca644d59f40b82f6712c854e416d5b5fe80808c40868e1ba2d6d8e1e9e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/19/GPL/openjdk-26-ea+19_linux-aarch64_bin.tar.gz'; 			downloadSha256='2841b9fa0e22671fc0ee3e6ba1e87237d895446e7548021004f201a1ff5abd99'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 11 Oct 2025 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c758be4def51008ebf92e615f7b29eb97254f5f999dc545894c366efa17498a`  
		Last Modified: Mon, 13 Oct 2025 18:21:34 GMT  
		Size: 5.6 MB (5633003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2295a25dbe91fe80b25a3821f1a90180ecdb235c2c558fba532dacdfe1152e47`  
		Last Modified: Mon, 13 Oct 2025 18:21:39 GMT  
		Size: 223.7 MB (223720110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-19-jdk-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:d56e5d4bc04021187dc10207204fa260440f39faa0cbb8a84859e1d4d06796b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df8c080a948f3b56096b59c770e42f3b7531b291c2388d1b50dc3df6a0e1008c`

```dockerfile
```

-	Layers:
	-	`sha256:8d9783d9155b5721e45e2d25350fe3343d34b18696f9be776eb944fb26f3d81e`  
		Last Modified: Mon, 13 Oct 2025 21:24:17 GMT  
		Size: 2.3 MB (2282292 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0b2e5cdbf94d48caa03106cc0c44bf3c92ac043116f21fb80dae1afd666c4b7`  
		Last Modified: Mon, 13 Oct 2025 21:24:18 GMT  
		Size: 19.6 KB (19627 bytes)  
		MIME: application/vnd.in-toto+json
