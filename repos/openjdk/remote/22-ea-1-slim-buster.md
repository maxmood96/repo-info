## `openjdk:22-ea-1-slim-buster`

```console
$ docker pull openjdk@sha256:dd6368de8e533facaf9309913b9cc0d3359d1b22e336a98ae3b0b2cc7288a245
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:22-ea-1-slim-buster` - linux; amd64

```console
$ docker pull openjdk@sha256:a82d34d8d5a68ad547f4dc8ab311ec744e62bcb7abec1008bc337f0648cf6fbb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.5 MB (235520406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93857e83dc927d60bc660e003d1fd009ad11eae97b5061fc7718df616ebaeac7`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 May 2023 01:20:37 GMT
ADD file:2058e04b33179527a56999678c1c62dfcf76944675afcd77b5163141fb025f8c in / 
# Tue, 23 May 2023 01:20:37 GMT
CMD ["bash"]
# Tue, 23 May 2023 07:49:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 12 Jun 2023 22:27:46 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Mon, 12 Jun 2023 22:27:46 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Jun 2023 22:27:46 GMT
ENV LANG=C.UTF-8
# Mon, 12 Jun 2023 22:27:46 GMT
ENV JAVA_VERSION=22-ea+1
# Mon, 12 Jun 2023 22:28:00 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/1/GPL/openjdk-22-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='50bf6303955ea128be3eb7ad9bc10f5e7eeacf9d3f81349a4d60a164fe7d0318'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/1/GPL/openjdk-22-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='6ca14677cb2db094acbc9b084d0a85c9e004aff9826977e0b9b35e5f9a55b550'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 12 Jun 2023 22:28:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:99bf4787315b60d97d860ac6d006b7835b2241a601e93c2da4af6ca554be8704`  
		Last Modified: Tue, 23 May 2023 01:24:47 GMT  
		Size: 27.1 MB (27138577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d3bd9a38fff0436b5f052c2adf5d0e9922bd3810335f2e5d4bd7943e07d343e`  
		Last Modified: Tue, 23 May 2023 07:51:42 GMT  
		Size: 3.3 MB (3278972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbbccb517ccd3ed679e3b66fdaf068cfa3a2795cce027e53e431a18b3682c8f3`  
		Last Modified: Mon, 12 Jun 2023 22:32:09 GMT  
		Size: 205.1 MB (205102857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:22-ea-1-slim-buster` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:be3dd978537a66b4842979dac4b8cb85348862df6b75e933358f0d457d5f7d3f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232490440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4eed3c6040d0a87f9950cfbd866645939cea3777499714affb9a7c1f5102725`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 12 Jun 2023 23:40:52 GMT
ADD file:d4a87f28032264e15d38bdd7efb6ffca8deadeb5388758f243e4866b360324c2 in / 
# Mon, 12 Jun 2023 23:40:52 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 04:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 04:39:41 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Tue, 13 Jun 2023 04:39:41 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jun 2023 04:39:41 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jun 2023 04:39:42 GMT
ENV JAVA_VERSION=22-ea+1
# Tue, 13 Jun 2023 04:39:53 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/1/GPL/openjdk-22-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='50bf6303955ea128be3eb7ad9bc10f5e7eeacf9d3f81349a4d60a164fe7d0318'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/1/GPL/openjdk-22-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='6ca14677cb2db094acbc9b084d0a85c9e004aff9826977e0b9b35e5f9a55b550'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 13 Jun 2023 04:39:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d191be7a3c9fa95847a482db8211b6f85b45096c7817fdad4d7661ee7ff1a421`  
		Last Modified: Mon, 12 Jun 2023 23:45:21 GMT  
		Size: 25.9 MB (25921353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe99b33fb696947092a56e5426644d8a600f4e0bb528749a1da223574abdc9f0`  
		Last Modified: Tue, 13 Jun 2023 04:43:17 GMT  
		Size: 3.1 MB (3130090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b630d6c7b398bd2a00ff1a7ee82edc46e37a07fb9e56b879bbd9b47b565e037a`  
		Last Modified: Tue, 13 Jun 2023 04:43:29 GMT  
		Size: 203.4 MB (203438997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
