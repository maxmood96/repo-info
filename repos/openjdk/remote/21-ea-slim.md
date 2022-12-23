## `openjdk:21-ea-slim`

```console
$ docker pull openjdk@sha256:f902807ffe46781b6eb3f828575d08485c8e6c457bf2271aa0e05d65326f503c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:21-ea-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:52430b50b76116b82891f0378807d2b16a6e984f9331a7da1ab549f041b6b46b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232467574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:883819c7e670a022a9f27eec3b2939e10d1456b9bfee1a1cc13bbe69c33c3c69`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 12:10:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 12:10:30 GMT
ENV JAVA_HOME=/usr/local/openjdk-21
# Wed, 21 Dec 2022 12:10:31 GMT
ENV PATH=/usr/local/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 12:10:31 GMT
ENV LANG=C.UTF-8
# Fri, 23 Dec 2022 01:20:44 GMT
ENV JAVA_VERSION=21-ea+3
# Fri, 23 Dec 2022 01:20:58 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/3/GPL/openjdk-21-ea+3_linux-x64_bin.tar.gz'; 			downloadSha256='21c02c2f76e385cca3ddd75d2913d3b6e16e4a1fa934fe038c0ab3c8c1184149'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/3/GPL/openjdk-21-ea+3_linux-aarch64_bin.tar.gz'; 			downloadSha256='84936b271d7997ca809075582a686eee89f8f37ac9252f33b8292260518000dd'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 23 Dec 2022 01:20:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc03ebf496347487b6180d378e9c5769b292b90df671ddc991422926d0809fec`  
		Last Modified: Wed, 21 Dec 2022 12:17:41 GMT  
		Size: 1.6 MB (1582327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c04dd65aa08bb0a5e183b7955c5af5f4a0c61add924b3fa123d3a10af5cdd64`  
		Last Modified: Fri, 23 Dec 2022 01:28:08 GMT  
		Size: 199.5 MB (199488304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:21-ea-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:4886d3b4f0ac7605b7137c1ee1505803859f8dc0484c3269891be9c8baf54c26
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.5 MB (229545827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:584f6dfee5b59615eafd9a253431b36356e7b57ac10dd9c4e3126019e70e00b5`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:48 GMT
ADD file:3ff0cc8d111595978eb50cdba91144382ce083c400d45785d53dbb03615a4890 in / 
# Wed, 21 Dec 2022 01:39:48 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 03:53:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 03:53:33 GMT
ENV JAVA_HOME=/usr/local/openjdk-21
# Wed, 21 Dec 2022 03:53:33 GMT
ENV PATH=/usr/local/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 03:53:33 GMT
ENV LANG=C.UTF-8
# Fri, 23 Dec 2022 00:40:33 GMT
ENV JAVA_VERSION=21-ea+3
# Fri, 23 Dec 2022 00:40:45 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/3/GPL/openjdk-21-ea+3_linux-x64_bin.tar.gz'; 			downloadSha256='21c02c2f76e385cca3ddd75d2913d3b6e16e4a1fa934fe038c0ab3c8c1184149'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/3/GPL/openjdk-21-ea+3_linux-aarch64_bin.tar.gz'; 			downloadSha256='84936b271d7997ca809075582a686eee89f8f37ac9252f33b8292260518000dd'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 23 Dec 2022 00:40:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4b7f5b2a311310809ab89d92f6f71b0462722fe855d3b92c93098a528aa08791`  
		Last Modified: Wed, 21 Dec 2022 01:43:12 GMT  
		Size: 30.0 MB (30044772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d25ec39ac4d8c95008c4cae68bf15b8d0f09df7a1b2b0b0c892724ec59abbd2`  
		Last Modified: Wed, 21 Dec 2022 04:00:05 GMT  
		Size: 1.6 MB (1566279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97f2f68fdb006b865000071b7a7c8df5a8186e6b465fbd8c7e3763c5ee995729`  
		Last Modified: Fri, 23 Dec 2022 00:47:41 GMT  
		Size: 197.9 MB (197934776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
