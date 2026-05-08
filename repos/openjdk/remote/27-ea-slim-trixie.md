## `openjdk:27-ea-slim-trixie`

```console
$ docker pull openjdk@sha256:ad2cec891374b56d382e4a12e8e354274ab81c852c80ca1527e01d9d8e3e8e14
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-slim-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:c7045ac30b906512cd43eca3be6a0854279451493619a8e50c30def3606ded52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.8 MB (260794178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f0df241c94e46679a9a3ea3413e5c2bc85c00778cd09caef15f15d5f35d222e`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:46:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:20 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Fri, 08 May 2026 19:46:20 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 19:46:20 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 19:46:20 GMT
ENV JAVA_VERSION=27-ea+20
# Fri, 08 May 2026 19:46:20 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/20/GPL/openjdk-27-ea+20_linux-x64_bin.tar.gz'; 			downloadSha256='a7c288898b71578ab424b0234102cb576ac5cf71c31bbdacc5d610a36be3d9cb'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/20/GPL/openjdk-27-ea+20_linux-aarch64_bin.tar.gz'; 			downloadSha256='47a8c6fedd9b292e5b5a5ad9e4cd238eecfc4d1cf098f052d48e7b6f19a0b025'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 08 May 2026 19:46:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff1c15dfd0ef9f6c00fa90586160c9f64bb6c682c5e41587a9143c7dcf3bea74`  
		Last Modified: Fri, 08 May 2026 19:46:40 GMT  
		Size: 2.4 MB (2371153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da99c021ed67a4725b4f45583329e78e155d198d4249b3eaadb012b07e51c7dd`  
		Last Modified: Fri, 08 May 2026 19:46:45 GMT  
		Size: 228.6 MB (228642799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:b2cfbbeff34b7746b641dbb5d74fe736a58990186ae16711a53f1fa3ee46fb96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2295734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8d3bb44d090083878dc17f769f4731b54273da8837b7d2e95323d8fa7c48a2b`

```dockerfile
```

-	Layers:
	-	`sha256:7ab5661a990c73e83cd9beb23730bfa34e50c30ad2cfff2210332439f1702037`  
		Last Modified: Fri, 08 May 2026 19:46:40 GMT  
		Size: 2.3 MB (2277625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a97cf8f4f724ce722a8ce3aebd34020c922c3fb9389d9486a6d91e3a4fa680fa`  
		Last Modified: Fri, 08 May 2026 19:46:39 GMT  
		Size: 18.1 KB (18109 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-slim-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:4e46a6e3051a09a50d4b6eebdbed0b4515c29169177be02a850494b14890d415
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.1 MB (259061100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a13f9cdc39e42fb3aaed0b9bcd935af4f7956901754db2b44335b9586b9677e`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:47:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:48:03 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Fri, 08 May 2026 19:48:03 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 19:48:03 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 19:48:03 GMT
ENV JAVA_VERSION=27-ea+20
# Fri, 08 May 2026 19:48:03 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/20/GPL/openjdk-27-ea+20_linux-x64_bin.tar.gz'; 			downloadSha256='a7c288898b71578ab424b0234102cb576ac5cf71c31bbdacc5d610a36be3d9cb'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/20/GPL/openjdk-27-ea+20_linux-aarch64_bin.tar.gz'; 			downloadSha256='47a8c6fedd9b292e5b5a5ad9e4cd238eecfc4d1cf098f052d48e7b6f19a0b025'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 08 May 2026 19:48:03 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6afbfe21593d47d34ab726ac45d64bb941cf5b3daa7f0d68213ffafbb9c2c52b`  
		Last Modified: Fri, 08 May 2026 19:48:24 GMT  
		Size: 2.3 MB (2314384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c3926bd113d34afa202bf08300ede75f83945f556f03f864836b274119298b`  
		Last Modified: Fri, 08 May 2026 19:48:34 GMT  
		Size: 226.6 MB (226603074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:6161695dcf007070b287a35059da5fac18d390bf26cdda06bb2e6e8329ca08b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2295586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f7a0c248e596c6a846177d816748baaf56817c5e1fc2fcda92e840f23a6c340`

```dockerfile
```

-	Layers:
	-	`sha256:91b3c5ba993cedf5d449f296dba6599c763133c63a5ea16ee43aa23afb87c2be`  
		Last Modified: Fri, 08 May 2026 19:48:24 GMT  
		Size: 2.3 MB (2277311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e661acb3e7f586fcc89204db77afb33df5b396d1734556d75d5880c764c1fb2`  
		Last Modified: Fri, 08 May 2026 19:48:24 GMT  
		Size: 18.3 KB (18275 bytes)  
		MIME: application/vnd.in-toto+json
