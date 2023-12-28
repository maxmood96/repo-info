## `openjdk:23-ea-3-jdk-slim-bullseye`

```console
$ docker pull openjdk@sha256:54c15e268492b6a45331a6150d51140942645e795fc5d9e27e0605335af014d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-3-jdk-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:7e3df1d518bb458f2e31394058b790e838066242a6fba80c4c6669f31ec4aa4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.0 MB (235950180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e841db365d522d46f8e1ff252935c85606a1c5ccd599ae6dfc119d7e242081f1`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:50 GMT
ADD file:bb44d67b03db8efaeb0c4171474f441d14ff35f328f13add32b289fca062fa2f in / 
# Tue, 19 Dec 2023 01:20:50 GMT
CMD ["bash"]
# Fri, 22 Dec 2023 01:54:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 22 Dec 2023 01:54:02 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 22 Dec 2023 01:54:02 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Dec 2023 01:54:02 GMT
ENV LANG=C.UTF-8
# Fri, 22 Dec 2023 01:54:02 GMT
ENV JAVA_VERSION=23-ea+3
# Fri, 22 Dec 2023 01:54:02 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/3/GPL/openjdk-23-ea+3_linux-x64_bin.tar.gz'; 			downloadSha256='9dfa6ea30eef2154e14ec5e38358cc814e1c5a766b1e4f9b4eda8277086defe2'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/3/GPL/openjdk-23-ea+3_linux-aarch64_bin.tar.gz'; 			downloadSha256='52fc0b69ed616eaabc2c5d89fae1654ad188324ca52ece1dfd5f44edf6645410'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 22 Dec 2023 01:54:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b5a0d5c14ba9ece1eecd5137c468d9a123372b0af2ed2c8c4446137730c90e5b`  
		Last Modified: Tue, 19 Dec 2023 01:25:40 GMT  
		Size: 31.4 MB (31417873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe22963eaeac6b4be183890a6001134c4b64e8d460ef1527597b3d5a0f1b280`  
		Last Modified: Wed, 27 Dec 2023 21:53:42 GMT  
		Size: 1.4 MB (1378087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e4c8cf951d5d856c1a2365f25d6f92e602fdf693033456b525436ef1f9fab1`  
		Last Modified: Wed, 27 Dec 2023 21:53:46 GMT  
		Size: 203.2 MB (203154220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-3-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:57034f7e45ba35381d047391a49d8082a8898d16d42c3320ca9f675978fbad7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2207640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d5ca628eee033bcb62402d77d0490651631265b1f047624ee46e9c5bc94be20`

```dockerfile
```

-	Layers:
	-	`sha256:3a52b1a563b976e481fc8ec93b6bc1c1b255bc8930cbc1eb82aecf1ab59d8b15`  
		Last Modified: Wed, 27 Dec 2023 21:53:42 GMT  
		Size: 2.2 MB (2190181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3c7cfad61ef8263b83bd4a4ab73354aa2f392acdb25470bdb5ed14f2ff6e42c`  
		Last Modified: Wed, 27 Dec 2023 21:53:42 GMT  
		Size: 17.5 KB (17459 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-3-jdk-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:dc9da557989c6aedf46743a0a00c9bec0c9fc3ad89c7ae58b4a724ac57228bbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232483866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:569541abaad9fa8d06c0eccf51f4ae041343069b5941aeedbd7cae83ac73f4fc`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:25 GMT
ADD file:4dd1c5e17a5e57644787f37e8ad290baef6c93f4f112b976f19136480a293713 in / 
# Tue, 19 Dec 2023 01:41:25 GMT
CMD ["bash"]
# Fri, 22 Dec 2023 01:54:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 22 Dec 2023 01:54:02 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 22 Dec 2023 01:54:02 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Dec 2023 01:54:02 GMT
ENV LANG=C.UTF-8
# Fri, 22 Dec 2023 01:54:02 GMT
ENV JAVA_VERSION=23-ea+3
# Fri, 22 Dec 2023 01:54:02 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/3/GPL/openjdk-23-ea+3_linux-x64_bin.tar.gz'; 			downloadSha256='9dfa6ea30eef2154e14ec5e38358cc814e1c5a766b1e4f9b4eda8277086defe2'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/3/GPL/openjdk-23-ea+3_linux-aarch64_bin.tar.gz'; 			downloadSha256='52fc0b69ed616eaabc2c5d89fae1654ad188324ca52ece1dfd5f44edf6645410'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 22 Dec 2023 01:54:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2244706f264b35566276550fbc21ada79613ddfff850e372b8f5113110a67c93`  
		Last Modified: Tue, 19 Dec 2023 01:45:22 GMT  
		Size: 30.1 MB (30064052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc02ea368438444f96ca14e22446135689f64999554dfd8cd20ab0b7c7a2913e`  
		Last Modified: Wed, 20 Dec 2023 10:24:06 GMT  
		Size: 1.4 MB (1361921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55314f9f75e1460eef629f6e32e4be1cd4b2da451d083c026f1b7b844520920`  
		Last Modified: Thu, 28 Dec 2023 05:04:12 GMT  
		Size: 201.1 MB (201057893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-3-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:8ba55b13ceb6f7c98fb6f88360471bca4a1e14b5c24a35fd7298aa4c075f471a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2206848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e245c70e4693775f35d56e7249d66eca92e1a9150a334d08430936cc230d26ba`

```dockerfile
```

-	Layers:
	-	`sha256:7aaabd6323223bfdc17b9adb991f0b808cc34d5be7043eab53366434af7b0975`  
		Last Modified: Thu, 28 Dec 2023 05:04:07 GMT  
		Size: 2.2 MB (2189543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ad343e0c883570da3d66b2cad1dd6c90b47d4e8757223a19398723f73a2251b`  
		Last Modified: Thu, 28 Dec 2023 05:04:07 GMT  
		Size: 17.3 KB (17305 bytes)  
		MIME: application/vnd.in-toto+json
