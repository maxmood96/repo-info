## `openjdk:26-ea-22-jdk-slim-trixie`

```console
$ docker pull openjdk@sha256:fa76aba90e1cc433f0c3be1caadd44b8753f34a088b79965569d0664ddc87e54
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-22-jdk-slim-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:b8685e9b99ff74a194cd0c6ec879197aac6afe9bfcc2d90f06e89c034a44fe6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258121623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e06aa3d6d29025e45f250934a44d537557be496c8435b20254e8d68f7315ab0b`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:17:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:17:57 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Tue, 04 Nov 2025 04:17:57 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 04:17:57 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 04:17:57 GMT
ENV JAVA_VERSION=26-ea+22
# Tue, 04 Nov 2025 04:17:57 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/22/GPL/openjdk-26-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='b87eeeb2167b024e3e62fb5ab860c0e2ad004d2e04f716b9f885d1180ac97a03'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/22/GPL/openjdk-26-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='b401cd0d932a4b8fd19f44deb517bfe9441097f31a2bbdb247e3b8757772e147'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 04 Nov 2025 04:17:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8734a65e247b0e878e87411bf693cb564656296e8d032f75ec26d1d5ffb2b6bf`  
		Last Modified: Tue, 04 Nov 2025 04:18:27 GMT  
		Size: 2.4 MB (2371147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb064e5e41fec23180768addcef0bdab179c525b0891e2b9da23c61adcd82994`  
		Last Modified: Tue, 04 Nov 2025 10:24:39 GMT  
		Size: 226.0 MB (225972372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-22-jdk-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:549a28def2f9226339186c07d779c9c45fac4657d2a3ca53a0675d02e2fe6dee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2297537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faf6f0e0195c64d8253205141b7847be76a6a8dc28b693c9c79e503aab2fdf79`

```dockerfile
```

-	Layers:
	-	`sha256:f0680974ccc1012153cc1492b08fead143e79590c095c2a1bdc6d400ea7a3624`  
		Last Modified: Tue, 04 Nov 2025 10:23:33 GMT  
		Size: 2.3 MB (2279428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62355c03aa3dbfe4747565634cad045b3d406213df5e657557e64b336bb0cd52`  
		Last Modified: Tue, 04 Nov 2025 10:23:34 GMT  
		Size: 18.1 KB (18109 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-22-jdk-slim-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:da3ee8fa6173d623c3269d7f7a42aa8ec0489133fe7a7811a407dd6f8b1b0a1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.3 MB (256270393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bc996116b87bf247efd69a764c3b02b2c9cf27d4962f9303a30df1e2588a324`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:33:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:33:26 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Tue, 04 Nov 2025 01:33:26 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:33:26 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 01:33:26 GMT
ENV JAVA_VERSION=26-ea+22
# Tue, 04 Nov 2025 01:33:26 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/22/GPL/openjdk-26-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='b87eeeb2167b024e3e62fb5ab860c0e2ad004d2e04f716b9f885d1180ac97a03'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/22/GPL/openjdk-26-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='b401cd0d932a4b8fd19f44deb517bfe9441097f31a2bbdb247e3b8757772e147'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 04 Nov 2025 01:33:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b18def6151232edfc2c1b6b90c14ca1b5690008f652030c670f755da5293e70`  
		Last Modified: Tue, 04 Nov 2025 01:33:58 GMT  
		Size: 2.3 MB (2314246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde24d62b81ff17bfdeacf897a57a74dc1594320eef9e02b15fef2b13eb85b64`  
		Last Modified: Tue, 04 Nov 2025 10:27:15 GMT  
		Size: 223.8 MB (223813849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-22-jdk-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:25edcdf26cbc2ea4fd521ca79fe5e41d3e8ba0fd8442e2fa168be5acb068a74a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2297390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08d3f80288aa59f703085c36326ed291a8c1aebf07d032114214f1a241d8a790`

```dockerfile
```

-	Layers:
	-	`sha256:4576f6adc6847b85c9598bf508cc7c4e2c58186b88130905f70585ed3acc2704`  
		Last Modified: Tue, 04 Nov 2025 10:23:37 GMT  
		Size: 2.3 MB (2279114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:120e68b0a9e07b058d435d192cd6b1887e5b12813ad788da60899ed584bce439`  
		Last Modified: Tue, 04 Nov 2025 10:23:38 GMT  
		Size: 18.3 KB (18276 bytes)  
		MIME: application/vnd.in-toto+json
