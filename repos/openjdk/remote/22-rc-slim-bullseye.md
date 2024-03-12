## `openjdk:22-rc-slim-bullseye`

```console
$ docker pull openjdk@sha256:f6cbd1308d32d37f6acafe9ad4876a42138e9088a1cff05fec63da8a6361f28f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:22-rc-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:fc0aad82f8d4f4be2674eec80ad957162e45bd3cc3f448107ca68ae2d2db6269
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.9 MB (235932449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1ba8146224113be7d414ba33fd53f0e0742b4d953eb1f5368b76f63cbe08fa9`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 16 Feb 2024 19:48:24 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Fri, 16 Feb 2024 19:48:24 GMT
CMD ["bash"]
# Fri, 16 Feb 2024 19:48:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Feb 2024 19:48:24 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Fri, 16 Feb 2024 19:48:24 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 19:48:24 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2024 19:48:24 GMT
ENV JAVA_VERSION=22
# Fri, 16 Feb 2024 19:48:24 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/36/GPL/openjdk-22_linux-x64_bin.tar.gz'; 			downloadSha256='4d65cc6ed28711768fd72c2043a7925f7c83f5f51bb64970bd9d52f7791fc6ac'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/36/GPL/openjdk-22_linux-aarch64_bin.tar.gz'; 			downloadSha256='b272e3228d2a3e04b126d54844d33cc6d137256490526cd08679d7023d07d4b7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 16 Feb 2024 19:48:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b448f9faf2f16dd6d689fa1be319cd01db21bcc69a89a47494f34ae1fc3c056b`  
		Last Modified: Tue, 12 Mar 2024 01:57:54 GMT  
		Size: 1.6 MB (1581783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41063888bfa022203c7aec9b58c37cdf4c65b333cfebad67bd7f68d978016e02`  
		Last Modified: Tue, 12 Mar 2024 01:57:58 GMT  
		Size: 202.9 MB (202928177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-rc-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:e52663c037fa11ac8c8dae95315bca9720bfdf0b5e62d007f14e26af5f94f35a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2654518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5a77eee97a767024dc12ddb358bb87c72f342567d53f573c992e604c8804580`

```dockerfile
```

-	Layers:
	-	`sha256:b982f3b0a8aa49fcf5eada769acbcefbd123b21cf644b86917f729afe1113efc`  
		Last Modified: Tue, 12 Mar 2024 01:57:54 GMT  
		Size: 2.6 MB (2637650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da537cf6dfda49914aa7ca1f132f13b1e1fb8d6bc92e02fa241eb8ddb7316b9c`  
		Last Modified: Tue, 12 Mar 2024 01:57:53 GMT  
		Size: 16.9 KB (16868 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:22-rc-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:c68d391148cc11ed262a75705af6f1eee9b55f979d43a7c4a0b1ee0af84056e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.6 MB (232624713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee355d605144eb8f3d774f6c468d704ce6167cf575b77691f3e0dca95eeb2c11`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Fri, 16 Feb 2024 19:48:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Feb 2024 19:48:24 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Fri, 16 Feb 2024 19:48:24 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 19:48:24 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2024 19:48:24 GMT
ENV JAVA_VERSION=22
# Fri, 16 Feb 2024 19:48:24 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/36/GPL/openjdk-22_linux-x64_bin.tar.gz'; 			downloadSha256='4d65cc6ed28711768fd72c2043a7925f7c83f5f51bb64970bd9d52f7791fc6ac'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/36/GPL/openjdk-22_linux-aarch64_bin.tar.gz'; 			downloadSha256='b272e3228d2a3e04b126d54844d33cc6d137256490526cd08679d7023d07d4b7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 16 Feb 2024 19:48:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66665e7107836c004c0e092f793e4525c11b530024a61f362798cc6f7500ab93`  
		Last Modified: Wed, 14 Feb 2024 01:18:12 GMT  
		Size: 1.6 MB (1565944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293444b493db0ece4eb96b8c54610196326e5d0319eb3bc484f32201d1c67c1a`  
		Last Modified: Sun, 18 Feb 2024 05:26:32 GMT  
		Size: 201.0 MB (200987692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-rc-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:ce5c501bfad800a636390e2489303533ef8396dbeb3ee387d8e45866896a55df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2654570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bdfb113d26b4bf3fb5e95f47538291e45a40c8602b0ca13624be2829fe59d91`

```dockerfile
```

-	Layers:
	-	`sha256:b54ce213e02dfddcb71cd93a79e3b40ad4f907450a4101afa001cdad818481a0`  
		Last Modified: Sun, 18 Feb 2024 05:26:27 GMT  
		Size: 2.6 MB (2637859 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f43c23e131c861e502ad5f6bf9f4245a4f38ba8108c9235339ed71f46e31b5a`  
		Last Modified: Sun, 18 Feb 2024 05:26:27 GMT  
		Size: 16.7 KB (16711 bytes)  
		MIME: application/vnd.in-toto+json
