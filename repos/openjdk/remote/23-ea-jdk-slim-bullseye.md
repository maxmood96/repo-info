## `openjdk:23-ea-jdk-slim-bullseye`

```console
$ docker pull openjdk@sha256:34e0aca56246b81803fdeba6fa2ec48951e04381517b471d7ae2c56ec8d809e7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-jdk-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:cda918e0b4b21a075618512b836bd851cb60e91c5d84910bb975d279472a7d47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244248546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24bb7120d6d3137d528eda5ca9ec4b1e1365af929e04d1601448f5bd71d5d8ab`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
CMD ["bash"]
# Sat, 08 Jun 2024 00:50:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Jun 2024 00:50:48 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Sat, 08 Jun 2024 00:50:48 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Jun 2024 00:50:48 GMT
ENV LANG=C.UTF-8
# Sat, 08 Jun 2024 00:50:48 GMT
ENV JAVA_VERSION=23-ea+26
# Sat, 08 Jun 2024 00:50:48 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/26/GPL/openjdk-23-ea+26_linux-x64_bin.tar.gz'; 			downloadSha256='a2a36c7b3c5fd89c6e392ba88a45a4647e482eab6b703595e2842e1b23c77ec9'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/26/GPL/openjdk-23-ea+26_linux-aarch64_bin.tar.gz'; 			downloadSha256='17a271b2853bc67590282ab01cceae8109012bc87ea2e07f7d5fefb55dd3192b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 08 Jun 2024 00:50:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3cdb2bd57855b60f1719fe33a2af4d735386d79982f02de13688f757015e763`  
		Last Modified: Mon, 10 Jun 2024 22:32:56 GMT  
		Size: 1.4 MB (1378039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc30770c1cb90d3e6001481e1ad27998cb4aa474a367b170c45b3587cdab1a4`  
		Last Modified: Mon, 10 Jun 2024 22:32:59 GMT  
		Size: 211.4 MB (211436576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:4020f8b799abf00b152297984223a28cb10ab11927dc3bec57f121b648368f58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2655852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77fe14cf062a905a77d5ead29685e5bb3221901c413077e4ba10b526da0f7463`

```dockerfile
```

-	Layers:
	-	`sha256:71bf762d8423c316bbfb75969844dc2296f230fcc5db6dc5f50433f099f05254`  
		Last Modified: Mon, 10 Jun 2024 22:32:56 GMT  
		Size: 2.6 MB (2638494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1955e3b779cd3570a90d78b69e306a2e4bb203d368529cef0663a69508d2b65d`  
		Last Modified: Mon, 10 Jun 2024 22:32:56 GMT  
		Size: 17.4 KB (17358 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-jdk-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:a20cdfdc112db3f837ecaadbe8bae567a748e623084cc0f7aaf0ab8e12611b55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.8 MB (240761135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8b10a20b2f66ba8047588e2d67433254e499420eea579059ed0685aa2ecfff0`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
CMD ["bash"]
# Sat, 08 Jun 2024 00:50:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Jun 2024 00:50:48 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Sat, 08 Jun 2024 00:50:48 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Jun 2024 00:50:48 GMT
ENV LANG=C.UTF-8
# Sat, 08 Jun 2024 00:50:48 GMT
ENV JAVA_VERSION=23-ea+26
# Sat, 08 Jun 2024 00:50:48 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/26/GPL/openjdk-23-ea+26_linux-x64_bin.tar.gz'; 			downloadSha256='a2a36c7b3c5fd89c6e392ba88a45a4647e482eab6b703595e2842e1b23c77ec9'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/26/GPL/openjdk-23-ea+26_linux-aarch64_bin.tar.gz'; 			downloadSha256='17a271b2853bc67590282ab01cceae8109012bc87ea2e07f7d5fefb55dd3192b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 08 Jun 2024 00:50:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48635aa3a72f5d9eda6c04795e37ca650ed83de84a321f1dfcf864eb7780709`  
		Last Modified: Tue, 04 Jun 2024 13:50:07 GMT  
		Size: 1.4 MB (1361913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1cccb2398efd76ae43319400f2ac1660d6e8658254d874945119fd58dcd7575`  
		Last Modified: Tue, 11 Jun 2024 03:41:05 GMT  
		Size: 209.3 MB (209312314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:ce9c79fa141a8fdc2c3676be7753c168acee369a0c4a5ffff44348260973ab52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2656459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:491f60246e4588ce63892583c263c74dc4819b26c64977e13a624505732a7143`

```dockerfile
```

-	Layers:
	-	`sha256:57f7d362d4c87105e630f80683aec4c391acc2f4fe15d6ba9315a3ce4ad2a7b6`  
		Last Modified: Tue, 11 Jun 2024 03:41:00 GMT  
		Size: 2.6 MB (2638770 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8f3a2ebbeb2f85168d2cb723c35db37842685316b6e0b4ca4b7a66f19838c37`  
		Last Modified: Tue, 11 Jun 2024 03:41:00 GMT  
		Size: 17.7 KB (17689 bytes)  
		MIME: application/vnd.in-toto+json
