## `openjdk:19-rc-slim-buster`

```console
$ docker pull openjdk@sha256:57d0f787479c6783724326fd1167be7591b8ae9248af7655bbb721cb49334013
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:19-rc-slim-buster` - linux; amd64

```console
$ docker pull openjdk@sha256:5d9241a0947897f2be3deb641df1e04e5a2bac3e45e123a6e5d59f9c1d42d4c3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.0 MB (226970422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:226611dc5bd5df352d2125e6dc1ba72fb437d95a397378c6bc403a6822d430af`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:48 GMT
ADD file:782d864aa72c2d5fb599311ebae56db4067d2e91ff532c1aaf1a291c3dbce5bb in / 
# Tue, 13 Sep 2022 00:56:49 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 07:02:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 07:04:15 GMT
ENV JAVA_HOME=/usr/local/openjdk-19
# Tue, 13 Sep 2022 07:04:15 GMT
ENV PATH=/usr/local/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 07:04:15 GMT
ENV LANG=C.UTF-8
# Tue, 13 Sep 2022 07:04:15 GMT
ENV JAVA_VERSION=19
# Tue, 13 Sep 2022 07:04:31 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk19/877d6127e982470ba2a7faa31cc93d04/36/GPL/openjdk-19_linux-x64_bin.tar.gz'; 			downloadSha256='f47aba585cfc9ecff1ed8e023524e8309f4315ed8b80100b40c7dcc232c12f96'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk19/877d6127e982470ba2a7faa31cc93d04/36/GPL/openjdk-19_linux-aarch64_bin.tar.gz'; 			downloadSha256='682bfb48158ca198393c4b7fd38f873e8d6316b0bc6511a07e917f7f0f3afb03'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 13 Sep 2022 07:04:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4b7b4a8876e2f677668e51b8473f97a237d3d4df201b9df4031bcaa8068370b1`  
		Last Modified: Tue, 13 Sep 2022 01:01:16 GMT  
		Size: 27.1 MB (27130552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99d52f2655b7c485e515b44593c5e3231a817180881565fc043f92bbbb0af57f`  
		Last Modified: Tue, 13 Sep 2022 07:10:47 GMT  
		Size: 3.3 MB (3273424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f509580f7ed33977ef77b74a3a9cb0e2fab6a98befee75bda55f65ef6edff6c4`  
		Last Modified: Tue, 13 Sep 2022 07:13:29 GMT  
		Size: 196.6 MB (196566446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-rc-slim-buster` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:8883ad55e99e271433ce872513fee6646f71f3dee3373ea5188c9e15c4851f4d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.2 MB (224226839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f270776abc8d10a1b6a06ff8af5c369b2177937c16142f74e5e7d6b71651a590`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Sep 2022 02:11:20 GMT
ADD file:18fa3591fcbf0c3e065dbe581a069fc2af6fab9e4446047348404881af960725 in / 
# Tue, 13 Sep 2022 02:11:21 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 14:39:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 14:41:29 GMT
ENV JAVA_HOME=/usr/local/openjdk-19
# Tue, 13 Sep 2022 14:41:30 GMT
ENV PATH=/usr/local/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 14:41:31 GMT
ENV LANG=C.UTF-8
# Tue, 13 Sep 2022 14:41:32 GMT
ENV JAVA_VERSION=19
# Tue, 13 Sep 2022 14:41:49 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk19/877d6127e982470ba2a7faa31cc93d04/36/GPL/openjdk-19_linux-x64_bin.tar.gz'; 			downloadSha256='f47aba585cfc9ecff1ed8e023524e8309f4315ed8b80100b40c7dcc232c12f96'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk19/877d6127e982470ba2a7faa31cc93d04/36/GPL/openjdk-19_linux-aarch64_bin.tar.gz'; 			downloadSha256='682bfb48158ca198393c4b7fd38f873e8d6316b0bc6511a07e917f7f0f3afb03'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 13 Sep 2022 14:41:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4c3f5cce277263c7aeaf67f83255af76927e03363e775f39d7587bc5036fcf1e`  
		Last Modified: Tue, 13 Sep 2022 02:17:10 GMT  
		Size: 25.9 MB (25904152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a215542ec2c1bdf2d159220f3e405dfdf14e3a6a874ba6b84cfd152bba34a4a8`  
		Last Modified: Tue, 13 Sep 2022 14:51:46 GMT  
		Size: 3.1 MB (3126014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbfcb6ed9cf55e0ae6bf0d6ad22d62f07fba6f920394c1337801a41d59ec0ab2`  
		Last Modified: Tue, 13 Sep 2022 14:54:56 GMT  
		Size: 195.2 MB (195196673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
