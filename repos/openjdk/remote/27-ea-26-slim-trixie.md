## `openjdk:27-ea-26-slim-trixie`

```console
$ docker pull openjdk@sha256:0c9e4fae008ebdb43f2e329833617ae24c4919cf607971f8e7af3c8eb353dd5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-26-slim-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:722601ffd20488ba5efdc9424cce0ba549e927a1041778ee5f8ce35a77dedc37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.3 MB (259273319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a075a309f94524dc1140acec2e14fb8aa60ace0a4198d0f226148e4bc7e43e2`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Tue, 16 Jun 2026 23:31:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Jun 2026 23:32:05 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 16 Jun 2026 23:32:05 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:32:05 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 23:32:05 GMT
ENV JAVA_VERSION=27-ea+26
# Tue, 16 Jun 2026 23:32:05 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/26/GPL/openjdk-27-ea+26_linux-x64_bin.tar.gz'; 			downloadSha256='8b55960efe73b9eb24c424f6d7dd1dae088eb2571c81dacfa76d05a2b9e24523'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/26/GPL/openjdk-27-ea+26_linux-aarch64_bin.tar.gz'; 			downloadSha256='062f3bc3a420c426c85bac9a0051044a4ce17a8f67b382efbd3f5406cb9c184d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 16 Jun 2026 23:32:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57973141c811917ecfc6944337b574af2da52c2cf8aed58702b70d4b6236dfbc`  
		Last Modified: Tue, 16 Jun 2026 23:32:25 GMT  
		Size: 2.4 MB (2371312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d115157f6f456126c5bfa184cf0f073640220b559e4604ac5075ff4bca6276d`  
		Last Modified: Tue, 16 Jun 2026 23:32:29 GMT  
		Size: 227.1 MB (227116592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-26-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:910cb94cb4504b69b47eeae5bf283dd6ad78512e6362a7fc01c163c01e00a70a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2294493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1aa13547ff764c5b6b3d0e771064bdbf41bcce58d509c7d0d4edd41045b0377`

```dockerfile
```

-	Layers:
	-	`sha256:a36b161a33f924bd3deac1534b6b55e85beea10680ce6882451b71a4db7545d2`  
		Last Modified: Tue, 16 Jun 2026 23:32:25 GMT  
		Size: 2.3 MB (2276384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:161d78de331357ccb28921a953f6b7d3b9418297b00cba22318a1a0694848901`  
		Last Modified: Tue, 16 Jun 2026 23:32:24 GMT  
		Size: 18.1 KB (18109 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-26-slim-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:581a548586da9d7aa4ec9073eb07292fd2fb0d2a5facf904ae2c61ac7c7cb564
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.6 MB (257562681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc4eea884fd4789b2e34f8ab4244e2b41c8caa9330388c118ddaa11ea8fa9793`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Tue, 16 Jun 2026 23:31:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Jun 2026 23:31:53 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 16 Jun 2026 23:31:53 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:31:53 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 23:31:53 GMT
ENV JAVA_VERSION=27-ea+26
# Tue, 16 Jun 2026 23:31:53 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/26/GPL/openjdk-27-ea+26_linux-x64_bin.tar.gz'; 			downloadSha256='8b55960efe73b9eb24c424f6d7dd1dae088eb2571c81dacfa76d05a2b9e24523'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/26/GPL/openjdk-27-ea+26_linux-aarch64_bin.tar.gz'; 			downloadSha256='062f3bc3a420c426c85bac9a0051044a4ce17a8f67b382efbd3f5406cb9c184d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 16 Jun 2026 23:31:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9467afd1e578f05688dd1d450424acb2968aea96c1c9c694564f8826427473`  
		Last Modified: Tue, 16 Jun 2026 23:32:14 GMT  
		Size: 2.3 MB (2314591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:444ac31921adb4e6382df7250dc7e60f0374fc4a14253cec09d7e907ba4290b8`  
		Last Modified: Tue, 16 Jun 2026 23:32:18 GMT  
		Size: 225.1 MB (225099560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-26-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:715c6a5747a6108c635be5a7d26ebda76bbe6555ea2a43a14419fb9d7dd591db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2294338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e49388f82995acdc0b0b4b9145c710badd28feba0f2ee896725fb0e74be9949`

```dockerfile
```

-	Layers:
	-	`sha256:5ddcd276490bc4f47e2abb0c7ee595ccd90efd2e382d3eeebf6d39aeb1861f57`  
		Last Modified: Tue, 16 Jun 2026 23:32:14 GMT  
		Size: 2.3 MB (2276062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f43af63f24edec9dc7fc1264d6bb2ed4c7c7bc259e1bde30fe0f98ac715c992`  
		Last Modified: Tue, 16 Jun 2026 23:32:14 GMT  
		Size: 18.3 KB (18276 bytes)  
		MIME: application/vnd.in-toto+json
