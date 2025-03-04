## `openjdk:25-ea-slim`

```console
$ docker pull openjdk@sha256:48427463c6f31b757c2ce170b3ba162a491e283c902a9962c4a8a6426668562c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:b732b438a6a9f0b9c0fb446196e805d49ead2f16eb85b511c57de5906878e300
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244191611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cdc734e067f1b870eb153fc96b74212fe1e3b0c665f89ab9e2eddab2bba0b03`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Tue, 04 Mar 2025 01:48:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Mar 2025 01:48:17 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Tue, 04 Mar 2025 01:48:17 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Mar 2025 01:48:17 GMT
ENV LANG=C.UTF-8
# Tue, 04 Mar 2025 01:48:17 GMT
ENV JAVA_VERSION=25-ea+12
# Tue, 04 Mar 2025 01:48:17 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/12/GPL/openjdk-25-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='305d3cbac7f43dcb43c278417001c8759d9462722654a384d9f8a4182f095193'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/12/GPL/openjdk-25-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='8b950bcc42a84435edf559f93b411dc6f28c067bd78717b26a0195b692af4e20'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 04 Mar 2025 01:48:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fedb0e8a79f4eff771394067fb3d93ef765c299c3d74b0f0de5af3d0eb71a24`  
		Last Modified: Tue, 04 Mar 2025 21:57:03 GMT  
		Size: 4.0 MB (4018404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:861055d8048987f02c779b4fcf2b0946a38977a94dc0353a7f2f636615c4d83e`  
		Last Modified: Tue, 04 Mar 2025 21:57:08 GMT  
		Size: 212.0 MB (211953906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:ef51252e8f903ae5fc36ca91ddd612cef3abe9c278cf30a75a6b126cb6e0db9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2553349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77b0faf145aec6c1324f9fa88564e76aacc357f5c876d49f8b5f2e643a5c211a`

```dockerfile
```

-	Layers:
	-	`sha256:eb3b5f2640c37f34176e4c70cecb301fa6a6f60a634eb1be24a49219b94364c3`  
		Last Modified: Tue, 04 Mar 2025 21:57:03 GMT  
		Size: 2.5 MB (2533908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d37e48b84c4de796a6c80d1c476b551cd800ebd6e91b0823cdccd3dac529af40`  
		Last Modified: Tue, 04 Mar 2025 21:57:02 GMT  
		Size: 19.4 KB (19441 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:b0d5f0cdacbdbc42332641678764a60e0bf1170e8c2cd097a9eaf55dc0bd0448
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.8 MB (241764639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbcb0c8efd85cded08a6dcf887be62e2785d3632e0018dc3b73565169706e7d3`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Tue, 04 Mar 2025 01:48:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Mar 2025 01:48:17 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Tue, 04 Mar 2025 01:48:17 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Mar 2025 01:48:17 GMT
ENV LANG=C.UTF-8
# Tue, 04 Mar 2025 01:48:17 GMT
ENV JAVA_VERSION=25-ea+12
# Tue, 04 Mar 2025 01:48:17 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/12/GPL/openjdk-25-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='305d3cbac7f43dcb43c278417001c8759d9462722654a384d9f8a4182f095193'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/12/GPL/openjdk-25-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='8b950bcc42a84435edf559f93b411dc6f28c067bd78717b26a0195b692af4e20'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 04 Mar 2025 01:48:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24b764fefcf12f640abdda9274a0cb11d639b180f003a673e0766704dec6540`  
		Last Modified: Tue, 04 Mar 2025 22:00:24 GMT  
		Size: 3.8 MB (3833778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7101450c41e4433aafb28506c5327ece1387c8939104255204aa72df48612bb0`  
		Last Modified: Tue, 04 Mar 2025 22:00:32 GMT  
		Size: 209.9 MB (209882436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:25e60dc54d212c0e826f962db6e9d6c54b5f850364d0dce4ec72287f2a5c918a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2553295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cb8892779d105a87a3d3e3a0f4ea08af10e8230e2c02cd850ba189c0359ef37`

```dockerfile
```

-	Layers:
	-	`sha256:c5bd99ad25d0ac26d0c26bb9b8c4d8194bad1c9727893bbd32fd1578a0605262`  
		Last Modified: Tue, 04 Mar 2025 22:00:24 GMT  
		Size: 2.5 MB (2533638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bd014d58805ecfa6583765c019e38c07495fd89bc3fcdf429937fceea49603b`  
		Last Modified: Tue, 04 Mar 2025 22:00:23 GMT  
		Size: 19.7 KB (19657 bytes)  
		MIME: application/vnd.in-toto+json
