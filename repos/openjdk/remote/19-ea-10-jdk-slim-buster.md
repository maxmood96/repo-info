## `openjdk:19-ea-10-jdk-slim-buster`

```console
$ docker pull openjdk@sha256:ffcc28127ab647b3ee07fb1b201338eed182c5888a7cb300899ab9ff3e2a6c96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:19-ea-10-jdk-slim-buster` - linux; amd64

```console
$ docker pull openjdk@sha256:a2a1829f54da917fbee85ff69cddec2a05ccee8698bad4c88459a0dc96e9e2ce
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.0 MB (220994597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64590b4ec7784adfd43bf9a95d3083e4e670df24246c4f48b6d45d2105e05b08`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:56 GMT
ADD file:702017714ad3e1567b4f60b688750f8b631d91088e4dcf41351c4bb07749c579 in / 
# Tue, 01 Mar 2022 02:13:56 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 14:22:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 14:22:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-19
# Tue, 01 Mar 2022 14:22:12 GMT
ENV PATH=/usr/local/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 14:22:12 GMT
ENV LANG=C.UTF-8
# Tue, 01 Mar 2022 14:22:12 GMT
ENV JAVA_VERSION=19-ea+10
# Tue, 01 Mar 2022 14:22:33 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/10/GPL/openjdk-19-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='21260b7e784c0e74c6730bdbaac70484fde42cf2839b2188dd2c4811d04660d8'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/10/GPL/openjdk-19-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='e41beaf49bdb16dc2eeec5e7e7c535f19444e221daf1cbb97d6e2b7981583156'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 01 Mar 2022 14:22:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:15115158dd02a1bf2fd28724e3c1024394033fb0e9a5d3e451ed2715b6ae312d`  
		Last Modified: Tue, 01 Mar 2022 02:20:08 GMT  
		Size: 27.2 MB (27153737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1727fec028eb22f37a4c93bbb31a582ebabb7664730fb7f93179214d45b7174`  
		Last Modified: Tue, 01 Mar 2022 14:42:23 GMT  
		Size: 3.3 MB (3269641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b8bd18db7dee986ca1861cd7b348e85b14bc99f5e8f146be98255f9c4dd9de`  
		Last Modified: Tue, 01 Mar 2022 14:42:43 GMT  
		Size: 190.6 MB (190571219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-ea-10-jdk-slim-buster` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:41525e6f40d26e0b5a4d42246df4e4abbfde71e5d38716c6f403ea18c5ef23ee
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.4 MB (218439399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91d440468e9d20ce0524343a36b898d570ed7275b5900af8eb57a1f0c82b1cb3`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 01 Mar 2022 02:11:57 GMT
ADD file:7d35162eea06441e7115c6fd9508802eafee00f64b11a7529a8f125bc67fa95e in / 
# Tue, 01 Mar 2022 02:11:57 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 13:49:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 13:49:24 GMT
ENV JAVA_HOME=/usr/local/openjdk-19
# Tue, 01 Mar 2022 13:49:25 GMT
ENV PATH=/usr/local/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 13:49:26 GMT
ENV LANG=C.UTF-8
# Tue, 01 Mar 2022 13:49:27 GMT
ENV JAVA_VERSION=19-ea+10
# Tue, 01 Mar 2022 13:49:41 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/10/GPL/openjdk-19-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='21260b7e784c0e74c6730bdbaac70484fde42cf2839b2188dd2c4811d04660d8'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/10/GPL/openjdk-19-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='e41beaf49bdb16dc2eeec5e7e7c535f19444e221daf1cbb97d6e2b7981583156'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 01 Mar 2022 13:49:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:69bf0018a85cc0775a59a4dbda1b2f2e71086a2d817473f72336bf4d0a83b9d0`  
		Last Modified: Tue, 01 Mar 2022 02:19:15 GMT  
		Size: 25.9 MB (25923140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1598aa0249d59bdc58f96c0187ae665625594bf9f256f5bca2c1b941fc493be2`  
		Last Modified: Tue, 01 Mar 2022 14:14:40 GMT  
		Size: 3.1 MB (3118853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7b8fe05524fc7770d08c3afc59104fc9c950d00502aa4506c36d1416d6b4738`  
		Last Modified: Tue, 01 Mar 2022 14:14:57 GMT  
		Size: 189.4 MB (189397406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
