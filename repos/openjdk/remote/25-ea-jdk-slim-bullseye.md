## `openjdk:25-ea-jdk-slim-bullseye`

```console
$ docker pull openjdk@sha256:2ae6d0154892de7c281759fdcac2c1553bae95e851ab797a7dfaba134ad49fb4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-jdk-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:988aed8d0fa3baac593cba1a48c1572586bbde7f3439a49def9a8cceccb375f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.4 MB (245422948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc93922b9bfc2be2833d9a8e1b133dedbeb88e1e4964a17f134074732bcc0350`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 16 May 2025 00:48:12 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Fri, 16 May 2025 00:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 May 2025 00:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 16 May 2025 00:48:12 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 May 2025 00:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 16 May 2025 00:48:12 GMT
ENV JAVA_VERSION=25-ea+23
# Fri, 16 May 2025 00:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/23/GPL/openjdk-25-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='f2d8788017e8ffb7bf559492efe8fb46d20d613df50a5eafaed7a8344a54a5bb'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/23/GPL/openjdk-25-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='5f1c62c8b60be587c98a541129878b43e854c0fe167710878aa719e7f3dbefa3'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 16 May 2025 00:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e1f16b66c2e86ad38458eba597e4ec79e4750398a28dbbc2d7819d829c4c9023`  
		Last Modified: Wed, 21 May 2025 22:28:05 GMT  
		Size: 30.3 MB (30255940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f9a49e2086f71740beadee7319546b25fa9f3815b11a7bb0b972cb13d41a01`  
		Last Modified: Wed, 21 May 2025 23:23:58 GMT  
		Size: 1.6 MB (1583497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4994c5fbb52f7810813517194156fdd02133de68e5d3452eef429e359e6c450a`  
		Last Modified: Wed, 21 May 2025 23:24:01 GMT  
		Size: 213.6 MB (213583511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:bd16410ea28401a0b47b76225ef1d400ac2e72fa04e91d4cdf9d14bc0b4a907d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2866361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6051c0047d491b8ba875d93599c9f78cae0c4794f157aba886a24d68a1fc86ac`

```dockerfile
```

-	Layers:
	-	`sha256:2183d97e1bcaa9e4f36f4dc90708645ca703b1f20b98614e4485594261f11dc0`  
		Last Modified: Wed, 21 May 2025 23:23:58 GMT  
		Size: 2.8 MB (2848791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59e1c7e6ce02d60735ed7b485c8d476e12cd59f87a169271917184f466008ae5`  
		Last Modified: Wed, 21 May 2025 23:23:58 GMT  
		Size: 17.6 KB (17570 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-jdk-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:2f1421e4e7c56de6143c73e4d73b3f2739a15aac2b80399e429aa655def203da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.7 MB (241672398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:366f3c0f339a2803863eb948de799f1380cb2982390a7e8f757eea56c167abc0`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 16 May 2025 00:48:12 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
# Fri, 16 May 2025 00:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 May 2025 00:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 16 May 2025 00:48:12 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 May 2025 00:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 16 May 2025 00:48:12 GMT
ENV JAVA_VERSION=25-ea+23
# Fri, 16 May 2025 00:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/23/GPL/openjdk-25-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='f2d8788017e8ffb7bf559492efe8fb46d20d613df50a5eafaed7a8344a54a5bb'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/23/GPL/openjdk-25-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='5f1c62c8b60be587c98a541129878b43e854c0fe167710878aa719e7f3dbefa3'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 16 May 2025 00:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:66850c8b65c1e9c3674a722b71f8887dd317a9b257148bb1063e88d85790544f`  
		Last Modified: Wed, 21 May 2025 22:28:28 GMT  
		Size: 28.7 MB (28746257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffa11c65fe0dd0f7246aa2d713287d4a2696818976b40e30107e62a132ee9e9`  
		Last Modified: Thu, 22 May 2025 03:35:17 GMT  
		Size: 1.6 MB (1567203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dbfbdd68066d0613fdb4588d83557b43c391425dcff1e71bc336c0df851bdb8`  
		Last Modified: Thu, 22 May 2025 03:35:22 GMT  
		Size: 211.4 MB (211358938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:7fb726849a3ee6570e5895fed5af8656c764d8f2cdada90cf4acffb68ac9421f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2866156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d426c29921781c6ad134971dab1de8e5d1fff2b2b201749bfab9c228e6b0c5a`

```dockerfile
```

-	Layers:
	-	`sha256:c74a1e7ad7222d26616d20de8402651506d6a7762760e39272b34c6db89a4d80`  
		Last Modified: Thu, 22 May 2025 03:35:17 GMT  
		Size: 2.8 MB (2848443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e65a1d521e588250f0effe692472f9d464491e57dee93013a055a108efd7816a`  
		Last Modified: Thu, 22 May 2025 03:35:16 GMT  
		Size: 17.7 KB (17713 bytes)  
		MIME: application/vnd.in-toto+json
