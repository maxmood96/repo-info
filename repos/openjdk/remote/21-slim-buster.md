## `openjdk:21-slim-buster`

```console
$ docker pull openjdk@sha256:d27afe9908eb01327a6198ba885ae063058c45e7f69a41481b69a628616f9cb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:21-slim-buster` - linux; amd64

```console
$ docker pull openjdk@sha256:bdfc1f71084153ec0bb73858615c8c91b310a641886fe3e0eefa2273f611b346
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.7 MB (229741667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c67bf0d3f17c70607b9c31a0f561ab12e3ed1408bc89fd0dea145e5b83608e2d`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 06 Dec 2022 01:21:18 GMT
ADD file:30180333dcb9028c0d2776f05042f6f309238b100863a050f3981fb80604e871 in / 
# Tue, 06 Dec 2022 01:21:18 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 05:06:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Dec 2022 00:34:17 GMT
ENV JAVA_HOME=/usr/local/openjdk-21
# Wed, 14 Dec 2022 00:34:17 GMT
ENV PATH=/usr/local/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Dec 2022 00:34:17 GMT
ENV LANG=C.UTF-8
# Wed, 14 Dec 2022 00:34:17 GMT
ENV JAVA_VERSION=21-ea+1
# Wed, 14 Dec 2022 00:34:31 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/1/GPL/openjdk-21-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='46d9f514e49067eebb9e3bf5033195e2ca1b834be98f3910ea1726c40e97dc22'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/1/GPL/openjdk-21-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='950a4a33ac9737bc7ecf824d2292f4fea92b1d9301a4f89d3c32e86f4d04bd23'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 14 Dec 2022 00:34:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6eab20599fab240a56b06125a77b4921dd39662d3b9f9008da7306531772a1d0`  
		Last Modified: Tue, 06 Dec 2022 01:25:52 GMT  
		Size: 27.1 MB (27140356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9669963fa8087b26171d843ba42c25760333a213b886c3b12289e827c22c574d`  
		Last Modified: Tue, 06 Dec 2022 05:12:29 GMT  
		Size: 3.3 MB (3275939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c356867abd9a05f65892bbb614c00bcc2e40d0519e7e13be6262b719e2eb2e`  
		Last Modified: Wed, 14 Dec 2022 00:41:03 GMT  
		Size: 199.3 MB (199325372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:21-slim-buster` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:a56fa131da0e47d209709bf56fe37fd4de8b2e104623a978c97461cf00d0167b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.9 MB (226857502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2905ade620ca346e9d0c92311ab27dd8586aed44bb423eb3bd5617d91a6c25d5`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:34 GMT
ADD file:764288ad3920160093c500e1a7277f174a656030bbe3a0511e7925e84495b6ee in / 
# Tue, 06 Dec 2022 01:40:34 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 04:28:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Dec 2022 00:54:47 GMT
ENV JAVA_HOME=/usr/local/openjdk-21
# Wed, 14 Dec 2022 00:54:47 GMT
ENV PATH=/usr/local/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Dec 2022 00:54:47 GMT
ENV LANG=C.UTF-8
# Wed, 14 Dec 2022 00:54:48 GMT
ENV JAVA_VERSION=21-ea+1
# Wed, 14 Dec 2022 00:54:59 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/1/GPL/openjdk-21-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='46d9f514e49067eebb9e3bf5033195e2ca1b834be98f3910ea1726c40e97dc22'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/1/GPL/openjdk-21-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='950a4a33ac9737bc7ecf824d2292f4fea92b1d9301a4f89d3c32e86f4d04bd23'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 14 Dec 2022 00:55:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b473b36a3d93c888196b326b1aad1f802bb6a9fa6fcbc5d2614d99a67899d587`  
		Last Modified: Tue, 06 Dec 2022 01:44:33 GMT  
		Size: 25.9 MB (25914951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198ebe9071c02f951926aefb5793b954b3398b0073a3c4a5b8ce0984c4f12050`  
		Last Modified: Tue, 06 Dec 2022 04:33:26 GMT  
		Size: 3.1 MB (3129343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992cb3b6d28c581fbb1fedfa142651fc84e950db390f659e082af93e4bbc4919`  
		Last Modified: Wed, 14 Dec 2022 01:01:33 GMT  
		Size: 197.8 MB (197813208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
