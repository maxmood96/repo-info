## `openjdk:27-ea-8-jdk-slim`

```console
$ docker pull openjdk@sha256:2186af5eac2427d742206891b17ff50b28fc469c77b433dab2f1c9bc337f9515
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-8-jdk-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:44af6a0e7bb34b532a2aa2ec5827962d1e7e27ae3727d3d2aeb31c40d3df0547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.6 MB (260635102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d69506ecdc86412abef444be7b33ce214d770e079a51cd4e60d7f5f437ab3f50`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Fri, 13 Feb 2026 00:01:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Feb 2026 00:01:17 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Fri, 13 Feb 2026 00:01:17 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Feb 2026 00:01:17 GMT
ENV LANG=C.UTF-8
# Fri, 13 Feb 2026 00:01:17 GMT
ENV JAVA_VERSION=27-ea+8
# Fri, 13 Feb 2026 00:01:17 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/8/GPL/openjdk-27-ea+8_linux-x64_bin.tar.gz'; 			downloadSha256='26424619f5fc68be80026db27b8d73d0e36e791df4b4c4e8dbee4edae1f8ffeb'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/8/GPL/openjdk-27-ea+8_linux-aarch64_bin.tar.gz'; 			downloadSha256='7ca3627abde323298007e3644968cd30d4363d289840c83bd0b8b49ccd84da51'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 13 Feb 2026 00:01:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02591fe449ca586455ec1b36ab969c447b167b263e8704b6bc36a631e31f1b4b`  
		Last Modified: Fri, 13 Feb 2026 00:01:37 GMT  
		Size: 2.4 MB (2371070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff1085c8811c1c4ffcf11c1bcf593f60c1af88b9f1c6e5d09e2b78ad4158935`  
		Last Modified: Fri, 13 Feb 2026 00:01:42 GMT  
		Size: 228.5 MB (228485436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-8-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:52b89b4dccec7eebfc8023fb5fca05055deb9d5c339793d0ffc247713da33d2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5735cc01b10f02707914c3d23fcd393ec270eeee1a605e2f8752cb7e258bf4da`

```dockerfile
```

-	Layers:
	-	`sha256:9a471e54ec501a55d30ad3fde7add2a0d2fa9de55d85ec3d7a84fe0136880e22`  
		Last Modified: Fri, 13 Feb 2026 00:01:37 GMT  
		Size: 2.3 MB (2278218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2dca6fcb7037fce02ac087310e3b2622a7b3ca9508fea2aa215386685f8fdcd3`  
		Last Modified: Fri, 13 Feb 2026 00:01:37 GMT  
		Size: 18.1 KB (18087 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-8-jdk-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:eea3f08f9cb37ce7fff21abab9b36ca53c46b149fbdc7d6f6a0a8ffe39bd2851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.9 MB (258883083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f80d28b9e31c033d2008d17886ee649bc7cdd2d1bb63711c7893449328c27cec`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Fri, 13 Feb 2026 00:02:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Feb 2026 00:02:48 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Fri, 13 Feb 2026 00:02:48 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Feb 2026 00:02:48 GMT
ENV LANG=C.UTF-8
# Fri, 13 Feb 2026 00:02:48 GMT
ENV JAVA_VERSION=27-ea+8
# Fri, 13 Feb 2026 00:02:48 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/8/GPL/openjdk-27-ea+8_linux-x64_bin.tar.gz'; 			downloadSha256='26424619f5fc68be80026db27b8d73d0e36e791df4b4c4e8dbee4edae1f8ffeb'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/8/GPL/openjdk-27-ea+8_linux-aarch64_bin.tar.gz'; 			downloadSha256='7ca3627abde323298007e3644968cd30d4363d289840c83bd0b8b49ccd84da51'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 13 Feb 2026 00:02:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52bd8f47d12537790d28124bf8fc6711b2e5b0f4aaec3a27fb1d5acfa2ccdf22`  
		Last Modified: Fri, 13 Feb 2026 00:03:10 GMT  
		Size: 2.3 MB (2314412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e415931a9f01c537959db8f1e9606691bbfe5657d1246cae9f8f6575f8936ffe`  
		Last Modified: Fri, 13 Feb 2026 00:03:15 GMT  
		Size: 226.4 MB (226428607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-8-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:6c977533106c2a66b799b8658c75c79c2f2def4636df2739dcece26d9ad698af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fe26a99a2b227fb5ee4b76dd7099acc202185827ccedfa31853a546a267a866`

```dockerfile
```

-	Layers:
	-	`sha256:4411c342a7babf161908be911b558f7ad3652b2cae9c3554836e6998455732ab`  
		Last Modified: Fri, 13 Feb 2026 00:03:10 GMT  
		Size: 2.3 MB (2277904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43eac10bcd2e3fe37fbfb55e1c98a94058f0b0210cf82fdb1a0d4cdf49de2f9b`  
		Last Modified: Fri, 13 Feb 2026 00:03:10 GMT  
		Size: 18.3 KB (18255 bytes)  
		MIME: application/vnd.in-toto+json
