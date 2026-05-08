## `openjdk:27-ea-slim-bookworm`

```console
$ docker pull openjdk@sha256:45857c5e2741e9c8d60ba081ea6eec29b5b8c2da99ad15e810d3d617ec731aa4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:5ffb7b87467dc1668349006dda39ae30e38eacdc40aab9145561ce2cae26caf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.9 MB (260905918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87eb7378fe51d359a27a10404fd50d8b8b18497e56bd0da96a9ad36cfc04615c`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:46:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:34 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Fri, 08 May 2026 19:46:34 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 19:46:34 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 19:46:34 GMT
ENV JAVA_VERSION=27-ea+20
# Fri, 08 May 2026 19:46:34 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/20/GPL/openjdk-27-ea+20_linux-x64_bin.tar.gz'; 			downloadSha256='a7c288898b71578ab424b0234102cb576ac5cf71c31bbdacc5d610a36be3d9cb'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/20/GPL/openjdk-27-ea+20_linux-aarch64_bin.tar.gz'; 			downloadSha256='47a8c6fedd9b292e5b5a5ad9e4cd238eecfc4d1cf098f052d48e7b6f19a0b025'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 08 May 2026 19:46:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9484cfffe805b8b853ac3013c286321ebe960f3af4203cf068f06561605987`  
		Last Modified: Fri, 08 May 2026 19:46:53 GMT  
		Size: 4.0 MB (4030650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32fedcec34946e122f60eb7c356a90614970c1d3ce1e6608991bca30b31e753d`  
		Last Modified: Fri, 08 May 2026 19:47:00 GMT  
		Size: 228.6 MB (228638986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:558b89761142b071dc987383b15f3b3ecd509aa448dbb547bc018833895ca3a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2665407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19c6ff0387fe1dda255cd58464969c862ec943d5106d61b1fcb7710a10845e66`

```dockerfile
```

-	Layers:
	-	`sha256:dfde61c9dfdfd0c20e52031250ae2359b0921bd5d9df9cf4f965d7d880dfeda4`  
		Last Modified: Fri, 08 May 2026 19:46:53 GMT  
		Size: 2.6 MB (2648537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:658962d4a62facaae090c27f7f516e05f9405d07a15771d909ccfcd4ef29eae1`  
		Last Modified: Fri, 08 May 2026 19:46:53 GMT  
		Size: 16.9 KB (16870 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:00758e86e15ba4c7b92e2c06b8fa37762c68cc3a412fbf085ccf934cd321e941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.6 MB (258574158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5935fdd877fad939411a5cb604a759a6b6d9286f5d977bc9d4b1e61d7e0af10b`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:47:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:48:07 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Fri, 08 May 2026 19:48:07 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 19:48:07 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 19:48:07 GMT
ENV JAVA_VERSION=27-ea+20
# Fri, 08 May 2026 19:48:07 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/20/GPL/openjdk-27-ea+20_linux-x64_bin.tar.gz'; 			downloadSha256='a7c288898b71578ab424b0234102cb576ac5cf71c31bbdacc5d610a36be3d9cb'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/20/GPL/openjdk-27-ea+20_linux-aarch64_bin.tar.gz'; 			downloadSha256='47a8c6fedd9b292e5b5a5ad9e4cd238eecfc4d1cf098f052d48e7b6f19a0b025'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 08 May 2026 19:48:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94dc2129f396d617ddad27ca4acd2e85bb6516b7fa03a1a14dc5dbf310391a0f`  
		Last Modified: Fri, 08 May 2026 19:48:28 GMT  
		Size: 3.9 MB (3852244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f96c6d3629e0ffb49febbab4e27551bd17177bee8ae80c8663533a8a568f3bff`  
		Last Modified: Fri, 08 May 2026 19:48:38 GMT  
		Size: 226.6 MB (226605749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:4e2875ccbd072619c7e6a7fdcbfe46a170a941b5c232310d0e6b321dc38e1922
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2665161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3ab565efb93e000301c50926761e9ff12bcae96b45ebcbae46f6f91698990d1`

```dockerfile
```

-	Layers:
	-	`sha256:dc8b1b12b6d9eff6aa512dfd978d0d8af43f891c8b6bef49884784011afd6ea0`  
		Last Modified: Fri, 08 May 2026 19:48:28 GMT  
		Size: 2.6 MB (2648171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bee7cc2feb5928ed0bf38226cf1ca547f80b13d898b16a37d7cb37494bb7974`  
		Last Modified: Fri, 08 May 2026 19:48:28 GMT  
		Size: 17.0 KB (16990 bytes)  
		MIME: application/vnd.in-toto+json
