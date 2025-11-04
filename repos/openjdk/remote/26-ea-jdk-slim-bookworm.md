## `openjdk:26-ea-jdk-slim-bookworm`

```console
$ docker pull openjdk@sha256:ce12f30fb20f356e90099d2c954ca08f14b4be91fc6f2ea055bec1e012721bef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-jdk-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:9a074020fe4333f2134f87ea24bdaa9c3bef7b05e56996c5b7e0161c645d0221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.2 MB (258220647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5119668ca3c2652af656648de18c9ea18451e379e3ac3bde02be82fe256c72c`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:34:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:34:51 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Tue, 04 Nov 2025 00:34:51 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:34:51 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 00:34:51 GMT
ENV JAVA_VERSION=26-ea+22
# Tue, 04 Nov 2025 00:34:51 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/22/GPL/openjdk-26-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='b87eeeb2167b024e3e62fb5ab860c0e2ad004d2e04f716b9f885d1180ac97a03'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/22/GPL/openjdk-26-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='b401cd0d932a4b8fd19f44deb517bfe9441097f31a2bbdb247e3b8757772e147'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 04 Nov 2025 00:34:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec0800d3ac31ec8b30e79973206c5aba7b4d14c43c5a5290e2d2f98d835af38`  
		Last Modified: Tue, 04 Nov 2025 00:35:27 GMT  
		Size: 4.0 MB (4027372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aec63a6548e179403603db14a20d671c1f58da7da1857408ab2b5158a24b0f0a`  
		Last Modified: Tue, 04 Nov 2025 10:59:13 GMT  
		Size: 226.0 MB (225964708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:0949622694ce85b4ef92fd27af368316f7bf6adb6a5ee88d47ed37eed1617467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2667293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bc0d2febf5953ff390a57202622a90efde2481397c17a287e50a5b171aeefc0`

```dockerfile
```

-	Layers:
	-	`sha256:92f0a9fabd4e20218582eb97710c5b7b72eee6bccd352df93e758834c2a370d3`  
		Last Modified: Tue, 04 Nov 2025 10:23:39 GMT  
		Size: 2.7 MB (2650422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87c6f357179c54f4b9bc53071e5b20151316cea2648bf16aaaa00bb61e1577b4`  
		Last Modified: Tue, 04 Nov 2025 10:23:40 GMT  
		Size: 16.9 KB (16871 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-jdk-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:b0e38413a533f1a446b5a9200a5a95ac05589c44c7d71970a0dad4b0a8952281
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.8 MB (255771520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85097e87264d8db693cce2ae39e4375cbe137f7b0badde6696838cf4e3e9c041`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:35:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:35:52 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Tue, 04 Nov 2025 00:35:52 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:35:52 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 00:35:52 GMT
ENV JAVA_VERSION=26-ea+22
# Tue, 04 Nov 2025 00:35:52 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/22/GPL/openjdk-26-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='b87eeeb2167b024e3e62fb5ab860c0e2ad004d2e04f716b9f885d1180ac97a03'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/22/GPL/openjdk-26-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='b401cd0d932a4b8fd19f44deb517bfe9441097f31a2bbdb247e3b8757772e147'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 04 Nov 2025 00:35:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6a5f8426c819ac379f9c2419f47efe587f8a30bd20619aae624da779c0b012`  
		Last Modified: Tue, 04 Nov 2025 00:36:26 GMT  
		Size: 3.9 MB (3851362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d399c8632a55a8a4710d87462f267b75aaf5a8e85d3410f3b0e87b80924ab721`  
		Last Modified: Tue, 04 Nov 2025 16:26:49 GMT  
		Size: 223.8 MB (223817782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:5c620ab124c5ec6cf3bcd5f9ab020e9a80e5bf1347539112b5d8f04dc804dec8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2667046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7cf5c5286391df19eb294c6a316f0c73d71ce7229e67b597c2832e62d2a3805`

```dockerfile
```

-	Layers:
	-	`sha256:d4dd3d071bb4d08aed7b09f6cf066c75e29ea49b5e5436fbd64bf0335f9d588d`  
		Last Modified: Tue, 04 Nov 2025 10:23:57 GMT  
		Size: 2.7 MB (2650056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d97e67f73551bcc60a20002f82e735f8b1b554350333530f67e59cb1f9c129d5`  
		Last Modified: Tue, 04 Nov 2025 10:23:57 GMT  
		Size: 17.0 KB (16990 bytes)  
		MIME: application/vnd.in-toto+json
