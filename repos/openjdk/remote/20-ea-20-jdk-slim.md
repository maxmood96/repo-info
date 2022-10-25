## `openjdk:20-ea-20-jdk-slim`

```console
$ docker pull openjdk@sha256:ac8adfe1f9547d043a35aa4269b53b296672eba51fc387bdca69bc0b9eb94b4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:20-ea-20-jdk-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:762ee4c3f35af60cd3323f25f29e6fca4ed8553b3f9cd68ae5db0f29a2cefd68
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230500473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d6c600603310a13c46fbfe3abb0eaebc44ba61ac8543ca93e993fa203b9390c`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 04:28:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 04:28:36 GMT
ENV JAVA_HOME=/usr/local/openjdk-20
# Tue, 25 Oct 2022 04:28:36 GMT
ENV PATH=/usr/local/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Oct 2022 04:28:36 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 04:28:36 GMT
ENV JAVA_VERSION=20-ea+20
# Tue, 25 Oct 2022 04:28:50 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/20/GPL/openjdk-20-ea+20_linux-x64_bin.tar.gz'; 			downloadSha256='0cb0f79bee2e61134a86049952a1e572bb3e2dad49aa200a20f18c697715a402'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/20/GPL/openjdk-20-ea+20_linux-aarch64_bin.tar.gz'; 			downloadSha256='4db7319dfbfb4a3561e9707c0178d0ba8d6413bc94f13d8c9ce406fd7445e000'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 25 Oct 2022 04:28:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb0c51c853f1ed357ae3b43810ec22a04514f065ef40f23f55eb8ab9bae73ed6`  
		Last Modified: Tue, 25 Oct 2022 04:32:27 GMT  
		Size: 1.6 MB (1584028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bebbca6df7e919ba96907edda1beca04ee6ec77712d368060cd7a225e92514ef`  
		Last Modified: Tue, 25 Oct 2022 04:32:41 GMT  
		Size: 197.5 MB (197496407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:20-ea-20-jdk-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:8f18fbf59379f839d7772200d821a0a1fc9d79be65bafa773233b48598a97f11
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.3 MB (227262034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74da3128fc6b4a9b151ff4248ea6ef04dbd78213f9340106471dc2c011515dcf`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:42 GMT
ADD file:dcb96c5906228cc8195f87d079b2a65ab49cde56edd7f0ccd238cdc65f9b693c in / 
# Tue, 04 Oct 2022 23:44:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 04:26:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 04:26:36 GMT
ENV JAVA_HOME=/usr/local/openjdk-20
# Wed, 05 Oct 2022 04:26:37 GMT
ENV PATH=/usr/local/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 04:26:38 GMT
ENV LANG=C.UTF-8
# Thu, 20 Oct 2022 20:43:49 GMT
ENV JAVA_VERSION=20-ea+20
# Thu, 20 Oct 2022 20:44:03 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/20/GPL/openjdk-20-ea+20_linux-x64_bin.tar.gz'; 			downloadSha256='0cb0f79bee2e61134a86049952a1e572bb3e2dad49aa200a20f18c697715a402'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/20/GPL/openjdk-20-ea+20_linux-aarch64_bin.tar.gz'; 			downloadSha256='4db7319dfbfb4a3561e9707c0178d0ba8d6413bc94f13d8c9ce406fd7445e000'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 20 Oct 2022 20:44:03 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:df8e44b0463f16c791d040e02e9c3ef8ec2a84245d365f088a80a22a455c71e8`  
		Last Modified: Tue, 04 Oct 2022 23:50:23 GMT  
		Size: 30.1 MB (30064395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d821c68cde68fc1dabd765433a7ae82e1dfd40ceab9795c047d424959096651c`  
		Last Modified: Wed, 05 Oct 2022 04:35:25 GMT  
		Size: 1.4 MB (1361242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39fb21d021c43d67554797ffeef086c103f664cd4950ac464f7d314082705f6`  
		Last Modified: Thu, 20 Oct 2022 20:52:15 GMT  
		Size: 195.8 MB (195836397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
