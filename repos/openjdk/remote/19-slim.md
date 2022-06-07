## `openjdk:19-slim`

```console
$ docker pull openjdk@sha256:611cb216ceb89c649f35204ffbcb5b0e5d191000e3ae9926dc6a6a967245a1d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:19-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:e5ff3190a597282196df90d272608a46995fe623338cd040dff473f51d8172ed
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.1 MB (229138634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c80b15097357228e478b41ec71a4065f4ce8406443e056af5b6095a44d962b5e`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 28 May 2022 01:20:23 GMT
ADD file:134f25aec8adf83cb940ba073a3409ca85dbb5ae592b704f95193e7d2539a3bc in / 
# Sat, 28 May 2022 01:20:23 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:16:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:16:35 GMT
ENV JAVA_HOME=/usr/local/openjdk-19
# Sat, 28 May 2022 02:16:35 GMT
ENV PATH=/usr/local/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 02:16:35 GMT
ENV LANG=C.UTF-8
# Mon, 06 Jun 2022 19:44:34 GMT
ENV JAVA_VERSION=19-ea+25
# Mon, 06 Jun 2022 19:44:47 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/25/GPL/openjdk-19-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='f03ae5efd6a8fe2211e9c3e0566289d405193244c67af680e202aa9f44473cb0'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/25/GPL/openjdk-19-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='f0c7f51bcf0bcca03127dd1dc7f9b59a88636714ea2bfd0707da665f98011237'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 06 Jun 2022 19:44:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:42c077c10790d51b6f75c4eb895cbd4da37558f7215b39cbf64c46b288f89bda`  
		Last Modified: Sat, 28 May 2022 01:25:19 GMT  
		Size: 31.4 MB (31379276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b062e78fd7c8f9370711c8b47595bc59fea38f7e04e22d887fbd3256f2324c`  
		Last Modified: Sat, 28 May 2022 02:27:46 GMT  
		Size: 1.6 MB (1582290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51a14ff25e4914cbb6ede5987bafa18f34edfe5c93871d9b44a321f39e9063c5`  
		Last Modified: Mon, 06 Jun 2022 19:52:32 GMT  
		Size: 196.2 MB (196177068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:75bb270ff6851edbb21364fc246dbf9cf954ab94d15a54cdac8c31ec46b2b927
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226281147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0629f9e2e7b5583b8c263c30be935f44e1fa25de31258d4ebab95b6d7a08dc36`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 28 May 2022 00:40:39 GMT
ADD file:55b4fe3115c684f545e4e4148c93745f12192976a08c37d090fcac708fb709a7 in / 
# Sat, 28 May 2022 00:40:39 GMT
CMD ["bash"]
# Sat, 28 May 2022 01:37:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 01:37:03 GMT
ENV JAVA_HOME=/usr/local/openjdk-19
# Sat, 28 May 2022 01:37:04 GMT
ENV PATH=/usr/local/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 01:37:05 GMT
ENV LANG=C.UTF-8
# Mon, 06 Jun 2022 22:46:18 GMT
ENV JAVA_VERSION=19-ea+25
# Mon, 06 Jun 2022 22:46:39 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/25/GPL/openjdk-19-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='f03ae5efd6a8fe2211e9c3e0566289d405193244c67af680e202aa9f44473cb0'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/25/GPL/openjdk-19-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='f0c7f51bcf0bcca03127dd1dc7f9b59a88636714ea2bfd0707da665f98011237'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 06 Jun 2022 22:46:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:dc1f00a5d701e86e2cd2568b860c61b393d66be1341e7267d07e6e57448ceeba`  
		Last Modified: Sat, 28 May 2022 00:47:35 GMT  
		Size: 30.1 MB (30065728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2c8727eedfb1755681add8fcb3c2c35d3b41f8231849edcec84588c6404f3b3`  
		Last Modified: Sat, 28 May 2022 01:54:41 GMT  
		Size: 1.4 MB (1361240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c234a43096215349cd5fcfaf23cea355a8bfb7560ffa364e27fae3023d6f1093`  
		Last Modified: Mon, 06 Jun 2022 23:00:03 GMT  
		Size: 194.9 MB (194854179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
