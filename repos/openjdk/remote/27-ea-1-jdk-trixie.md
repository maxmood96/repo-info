## `openjdk:27-ea-1-jdk-trixie`

```console
$ docker pull openjdk@sha256:a0bba5ed5299c2292e3231474f767329863733feff79144937da7ec7c7918887
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-1-jdk-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:b46049b7b61fcacab22e929736c3f3472b9b88edbc2a3d21679c5f9a043110db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.8 MB (386750368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a59bd62c8511ff3478114f29bf20f464203b80940f99254be1578eea616796ed`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:07:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:06:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:50:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:50:32 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 09 Dec 2025 00:50:32 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 00:50:32 GMT
ENV LANG=C.UTF-8
# Tue, 09 Dec 2025 00:50:32 GMT
ENV JAVA_VERSION=27-ea+1
# Tue, 09 Dec 2025 00:50:32 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/1/GPL/openjdk-27-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='1aa364bd43fc19955536763cfbf4ed9019a9766283b6b00c7813301c229ac2ff'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/1/GPL/openjdk-27-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='48552e3ba3f4c8a08d0078fe9af2c25a1145a36e3cccdc56f61aa90786cade22'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 09 Dec 2025 00:50:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2981f7e8980b9f4b6605026e1c5f99b4971ebba15f626e46904554de09f324f4`  
		Last Modified: Mon, 08 Dec 2025 22:17:46 GMT  
		Size: 49.3 MB (49289520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22766554d6bfa95c7325b00ee002f2705a7b8605908c3eb43dbe729c412422c`  
		Last Modified: Mon, 08 Dec 2025 23:07:43 GMT  
		Size: 25.6 MB (25613863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f2d358b447d091790c5ef0943550bbcf57bac46c4b8bfcfc3e6dacf4cb7969`  
		Last Modified: Tue, 09 Dec 2025 00:06:46 GMT  
		Size: 67.8 MB (67778647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce48627f74b3faad525bf9cd30aff81a2840985e1dd59a0f97b9f32ac97119f`  
		Last Modified: Tue, 09 Dec 2025 00:51:10 GMT  
		Size: 16.1 MB (16061615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:569ee15c4a0f3741e6b90ab9c186d479bbe1adaae6887e63865d80a1f4fb3ab0`  
		Last Modified: Tue, 09 Dec 2025 00:51:15 GMT  
		Size: 228.0 MB (228006723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-1-jdk-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:f7cbaf32ccaba1876bfe891a46fa630f6f4e13230262530c9d14e6995c78625e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8527826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a3726855efd7f8d1e7ca9497c85c5fa32b9f776f559bcbca3dab68c9277ea31`

```dockerfile
```

-	Layers:
	-	`sha256:32df660e04ac45afc5d5c793232dce377d275d7ffb87a7dc87dc249671819f8e`  
		Last Modified: Tue, 09 Dec 2025 04:25:28 GMT  
		Size: 8.5 MB (8509931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1c38ec1973cd1e902271bb471d1a1228a648d778e4fa504a921a14a105eac9e`  
		Last Modified: Tue, 09 Dec 2025 04:25:29 GMT  
		Size: 17.9 KB (17895 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-1-jdk-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:bdac592957945332475be217c7390a4ad2777fd9e8ea331f2f2b3a2a88a1fce2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.2 MB (384244506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a686bec30b3b4184ed2efc72585595e4b46ac14732616ae1d276db7afda8c223`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:11:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 01:20:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 01:21:20 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 09 Dec 2025 01:21:20 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 01:21:20 GMT
ENV LANG=C.UTF-8
# Tue, 09 Dec 2025 01:21:20 GMT
ENV JAVA_VERSION=27-ea+1
# Tue, 09 Dec 2025 01:21:20 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/1/GPL/openjdk-27-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='1aa364bd43fc19955536763cfbf4ed9019a9766283b6b00c7813301c229ac2ff'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/1/GPL/openjdk-27-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='48552e3ba3f4c8a08d0078fe9af2c25a1145a36e3cccdc56f61aa90786cade22'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 09 Dec 2025 01:21:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6a828f739420ec96bad6123094a07f3f234998f6cf772e34e0ba733aa8e2b347`  
		Last Modified: Mon, 08 Dec 2025 22:17:28 GMT  
		Size: 49.7 MB (49650226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f097d536d3c26abbb49039062f8d8e471b0c97bdfcc2ecfcfcf56545161524fb`  
		Last Modified: Mon, 08 Dec 2025 23:11:17 GMT  
		Size: 25.0 MB (25020941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb13e64d383cee6a152ac57ad29b9b1116554b1c9daab0e94464d674f3804db`  
		Last Modified: Tue, 09 Dec 2025 00:12:25 GMT  
		Size: 67.6 MB (67585014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434bd3384a6a16d5d525f8ea16daf8aa562f543a55f20636371d0e4d2a24c085`  
		Last Modified: Tue, 09 Dec 2025 01:21:06 GMT  
		Size: 16.1 MB (16070723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7634fb0dfa670dee031397131f4626d3662209969c2f8f87cde1b6018f087fe`  
		Last Modified: Tue, 09 Dec 2025 01:22:22 GMT  
		Size: 225.9 MB (225917602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-1-jdk-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:715493ba2c84f882cdcad8411a7831e0b714c37616effc7aed877562b8ed4b63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8722736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d314e250a01bf04d95679994528d2334c705e2c4f7b7c760f86d6ee217a6443f`

```dockerfile
```

-	Layers:
	-	`sha256:0ceddde9cd9a8aa03e1caaad2d629b58cabedf2c09f885a20c1b2bfcc6dec327`  
		Last Modified: Tue, 09 Dec 2025 04:25:35 GMT  
		Size: 8.7 MB (8704721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8922da8da13cbfaea7b31478e2264083fbb6339f15afacb0696a9d2e53d437f7`  
		Last Modified: Tue, 09 Dec 2025 04:25:36 GMT  
		Size: 18.0 KB (18015 bytes)  
		MIME: application/vnd.in-toto+json
