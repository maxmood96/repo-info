## `openjdk:26-ea-jdk-slim-trixie`

```console
$ docker pull openjdk@sha256:d5118cb01935a447715a1be945c1dd722ea0861e5b0e96b1b3c459d36aff4fa3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-jdk-slim-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:f0c3ee8b8082d4d883e74831f54dd06936a5212fab9c5cd0d0bbb5d109c0fd43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.1 MB (260140862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f708ed0bfa4fbd475ae69a48dd26780a4b7685dc95e2140e84e76495cfca8e2`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Tue, 16 Dec 2025 00:03:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Dec 2025 00:03:32 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Tue, 16 Dec 2025 00:03:32 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Dec 2025 00:03:32 GMT
ENV LANG=C.UTF-8
# Tue, 16 Dec 2025 00:03:32 GMT
ENV JAVA_VERSION=26-ea+28
# Tue, 16 Dec 2025 00:03:32 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/28/GPL/openjdk-26-ea+28_linux-x64_bin.tar.gz'; 			downloadSha256='a18910b0bdceb12a4f78147a1feebee50cc621ad8114c07a1ab071e58c17b09d'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/28/GPL/openjdk-26-ea+28_linux-aarch64_bin.tar.gz'; 			downloadSha256='d330a706e3fc611f4b39f6768f104e47d0a755ffabda31e3299dbc2e791f4f18'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 16 Dec 2025 00:03:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:525132f6c18e6f9ec7ae9f8e2af4dbd2d685b5a3473c1aec10c2df3aae3e1af6`  
		Last Modified: Tue, 16 Dec 2025 00:04:03 GMT  
		Size: 2.4 MB (2370967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89b77c4c2eb491a0c521ca494d0394fb5328822361b93b29fa5ed9326613811`  
		Last Modified: Tue, 16 Dec 2025 00:06:05 GMT  
		Size: 228.0 MB (227993399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:e34a7883bc0b9b19a718daeae322435a35fccbfd2b2099e80de9994b415e9d63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10e18ad584a342071f4c9b4ae08a053586044502c9e2d739f83cc42ca5508ab0`

```dockerfile
```

-	Layers:
	-	`sha256:cf5c13fc7fc1cc7dbe5e094923772fd053f42bfe93474dd4d0e1ece602672885`  
		Last Modified: Tue, 16 Dec 2025 01:24:02 GMT  
		Size: 2.3 MB (2278789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab2d633bcf44bbec2a60a40df6c1e7e80eedb34140cbc3e2205f47fd320f9c01`  
		Last Modified: Tue, 16 Dec 2025 01:24:02 GMT  
		Size: 18.1 KB (18109 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-jdk-slim-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:c9e91a2b60f63c1940f5e803d4959d24007b921ae1d1c4a21e5db1bfd2f50531
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.4 MB (258354554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40a7fc5427e58923e22a17e0857df0b4c0ba350f26cb665474cf3c57fc2cf53d`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Tue, 16 Dec 2025 00:02:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Dec 2025 00:03:01 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Tue, 16 Dec 2025 00:03:01 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Dec 2025 00:03:01 GMT
ENV LANG=C.UTF-8
# Tue, 16 Dec 2025 00:03:01 GMT
ENV JAVA_VERSION=26-ea+28
# Tue, 16 Dec 2025 00:03:01 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/28/GPL/openjdk-26-ea+28_linux-x64_bin.tar.gz'; 			downloadSha256='a18910b0bdceb12a4f78147a1feebee50cc621ad8114c07a1ab071e58c17b09d'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/28/GPL/openjdk-26-ea+28_linux-aarch64_bin.tar.gz'; 			downloadSha256='d330a706e3fc611f4b39f6768f104e47d0a755ffabda31e3299dbc2e791f4f18'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 16 Dec 2025 00:03:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d94b927dd0e7a46ba1fec2f736ebfb23cba290af85c36164bca1578df4d634e`  
		Last Modified: Tue, 16 Dec 2025 00:03:33 GMT  
		Size: 2.3 MB (2314069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8d8f16affa6fce015c6a10de5a7517e0b3a99dbeb64afca5de0f4a89ddc4e5`  
		Last Modified: Tue, 16 Dec 2025 00:03:39 GMT  
		Size: 225.9 MB (225901857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:b2d9995ef03271146dee74c5bfd427851af935c660f370c0a807e849aadad4a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25c3e8fc5269696ce20d4eea16397d6c44579bac982b84ec13aa06a3ff851cae`

```dockerfile
```

-	Layers:
	-	`sha256:189d84dcb4d07be79218c2638e52a196df48680fd8dc82136f23fcf942b9990f`  
		Last Modified: Tue, 16 Dec 2025 01:24:07 GMT  
		Size: 2.3 MB (2278475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44345ef75d52b5e5e02f42980c4041a2f945ba9dcedbb6f917e5c77770d1f132`  
		Last Modified: Tue, 16 Dec 2025 01:24:07 GMT  
		Size: 18.3 KB (18276 bytes)  
		MIME: application/vnd.in-toto+json
