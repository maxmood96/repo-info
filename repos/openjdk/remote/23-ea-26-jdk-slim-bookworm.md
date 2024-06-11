## `openjdk:23-ea-26-jdk-slim-bookworm`

```console
$ docker pull openjdk@sha256:c6a75ccef9ea261054b5ec551621c0ef5cf271ba931b93a4dabdbbbb5e90f907
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-26-jdk-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:fd3b3b9ed0d3a1a6b5426ab5c5c5b966ffa4d3e64485d134809058870570b2b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.4 MB (244410727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f61eda63ad222fe8fc6e24ed0a587bfbefe5b12a2cc92242c546f8836809714`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
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
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c48f51482250cb6a4b4ef95dc8a9b2521a974729fc0bb8e7c624a6632aa7a1`  
		Last Modified: Mon, 10 Jun 2024 22:33:01 GMT  
		Size: 3.8 MB (3821765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da20a11bb0dd1422b5be237004dfcb5d6718037423261d4ff9dc4af8d74edf9`  
		Last Modified: Mon, 10 Jun 2024 22:33:04 GMT  
		Size: 211.4 MB (211438551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-26-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:92bf832ebb8061cab4011f98dccb8460d0dc690d50aade9c0e2a92316c9fee35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2365546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db9827d3f2573728763077dd1812fb0c86d41ca9412cd07733a91cb2276ac6f8`

```dockerfile
```

-	Layers:
	-	`sha256:c2fb51f648588e5b0d426faa5d0b351c68746f61e26c0abea388dea22b081a95`  
		Last Modified: Mon, 10 Jun 2024 22:33:01 GMT  
		Size: 2.3 MB (2346316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1116c267a87aa74b06fb0442e8756f07c5fbdce3a33348778d35b51e5d0ad156`  
		Last Modified: Mon, 10 Jun 2024 22:33:01 GMT  
		Size: 19.2 KB (19230 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-26-jdk-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:2403cc2dd4382fc425a8c8439d0692e2cc626a33a867486d81ab7f57057b09d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.1 MB (242124125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4021603c53bf766599eda43c8e5f56be325c9445d5eed9b1b718805715985912`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 14 May 2024 00:39:40 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Tue, 14 May 2024 00:39:41 GMT
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
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0732eb3b5b85722cffae3ffea999285c5d487bdb7f396bc97253e6e0cad752e`  
		Last Modified: Tue, 04 Jun 2024 12:18:18 GMT  
		Size: 3.6 MB (3629763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5868fa799df0594d400ce3d63cd015ea8ee0f59856e7fcd226f7b06a1ddb4fce`  
		Last Modified: Tue, 11 Jun 2024 03:39:24 GMT  
		Size: 209.3 MB (209314859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-26-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:dfbb665bbdf108d6e47c62ab365e81b22ea2bb9a5aa74c349b30282b7217fa61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2366305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad528bc9d97f0484a508ec87b8b01c7ee74bce023c2969ae08ebbd3a43be6361`

```dockerfile
```

-	Layers:
	-	`sha256:1b69af725b90596577a4583a2375d232deced632405dd6d2e6e705f43bf40618`  
		Last Modified: Tue, 11 Jun 2024 03:39:15 GMT  
		Size: 2.3 MB (2346670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b7f198537d136b823b6d92dd3c035bed4a57d54f086a64e94716b51da79079a`  
		Last Modified: Tue, 11 Jun 2024 03:39:15 GMT  
		Size: 19.6 KB (19635 bytes)  
		MIME: application/vnd.in-toto+json
