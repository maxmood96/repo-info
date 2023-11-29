## `openjdk:22-ea-25-slim-bookworm`

```console
$ docker pull openjdk@sha256:c6b82b10f67b95116e3c72a1e5b46d44778835f4039cf1f3628d0b8b857138d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `openjdk:22-ea-25-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:a218eb01668f11d434fc65cf0025baf84ed171ce5aafa12530fd8d4ee3b6f4fd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.9 MB (237855207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edfcb6ad365e8cbbe78f667f509b8f4d2d0e31c1305ff68795ddec0bc86d6d82`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:37 GMT
ADD file:d261a6f6921593f1e0b3f472ab1b1822e2c6deb0b369200f0b3370556bfad017 in / 
# Tue, 21 Nov 2023 05:21:37 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 09:20:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:20:39 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Tue, 21 Nov 2023 09:20:39 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 09:20:39 GMT
ENV LANG=C.UTF-8
# Wed, 29 Nov 2023 01:46:10 GMT
ENV JAVA_VERSION=22-ea+25
# Wed, 29 Nov 2023 01:46:40 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/25/GPL/openjdk-22-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='0f98721a88a1dd380773adbf29dd79df25be9b69045c3266f913ecacc5e74d3e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/25/GPL/openjdk-22-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='ea5fc28e7b6ed0a5da04b4740a35d8dd26bb68a48a516da2d002359d817ba35c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 29 Nov 2023 01:46:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1f7ce2fa46ab3942feabee654933948821303a5a821789dddab2d8c3df59e227`  
		Last Modified: Tue, 21 Nov 2023 05:25:58 GMT  
		Size: 29.1 MB (29149908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a71988e474766aa4283c8ac4ac023b8d3b00c2e51d23a0740e109345192d40`  
		Last Modified: Tue, 21 Nov 2023 09:21:54 GMT  
		Size: 4.0 MB (4017900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3665808d4fc1179d0e0ca7ef178238b4b38e2e84fa0f2709776c4e8d1102952a`  
		Last Modified: Wed, 29 Nov 2023 01:50:14 GMT  
		Size: 204.7 MB (204687399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
