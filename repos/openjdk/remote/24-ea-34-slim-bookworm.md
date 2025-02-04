## `openjdk:24-ea-34-slim-bookworm`

```console
$ docker pull openjdk@sha256:f048a836456a6d7107e6953e97201a3d6476510736b6777af163f28d34a829ad
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-34-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:94dfc74866befd4b6e6b7ff046a21abfc1c21ee3f043b88010ed2b41142981a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.2 MB (245216226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab688d9ad6de7052e9d1f16141afba02070ee184e4c4811eec756e25bc61f1e9`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 31 Jan 2025 01:48:14 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Fri, 31 Jan 2025 01:48:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 01:48:14 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 31 Jan 2025 01:48:14 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jan 2025 01:48:14 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 01:48:14 GMT
ENV JAVA_VERSION=24-ea+34
# Fri, 31 Jan 2025 01:48:14 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/34/GPL/openjdk-24-ea+34_linux-x64_bin.tar.gz'; 			downloadSha256='d49c0df93307a9bd06c9ca7b35ce6d068246a0938d0802933910b42574c173d3'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/34/GPL/openjdk-24-ea+34_linux-aarch64_bin.tar.gz'; 			downloadSha256='ffab3ade32683a348fbb81aef96107b38545d1df7daa4e7ca81fe0f6775002ea'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 31 Jan 2025 01:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c910fb362ec5716fd3f46d31fc4ab70cd62817d2e29508c976fd2f979e332faa`  
		Last Modified: Tue, 04 Feb 2025 04:43:41 GMT  
		Size: 4.0 MB (4018415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ac5bf3ea261a801f70ba1970cec5fca7e2996e7fa9c0a07eeaf018f42988da`  
		Last Modified: Tue, 04 Feb 2025 04:43:44 GMT  
		Size: 213.0 MB (212985508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-34-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:3e6ec863a60126355fc33575d13aac5bc0176e047cb685474dceaf775c36858c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2553961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc8d5e9bbde2689a1baabdc295047eaf0834680cc95b32eede4cbf1ebc83d99c`

```dockerfile
```

-	Layers:
	-	`sha256:ed8be9f23645167dad5fc47a8e3b5e1c6d6aa529cc3bec58dba6a17ea6a10a92`  
		Last Modified: Tue, 04 Feb 2025 04:43:41 GMT  
		Size: 2.5 MB (2534519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98cf717d0295e4a305f9ef75a9043fd6ad7f77a487de10cc594f00427f725129`  
		Last Modified: Tue, 04 Feb 2025 04:43:41 GMT  
		Size: 19.4 KB (19442 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-34-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:712de01a379889d36960f1468d1f687930420e4596682592df8e05b72a63d20d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.8 MB (242804132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45e3687fd646d3dd3b62cb7c9067780acad3e1ef99f244e6b71c501e84c32556`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 31 Jan 2025 01:48:14 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Fri, 31 Jan 2025 01:48:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 01:48:14 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 31 Jan 2025 01:48:14 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jan 2025 01:48:14 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 01:48:14 GMT
ENV JAVA_VERSION=24-ea+34
# Fri, 31 Jan 2025 01:48:14 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/34/GPL/openjdk-24-ea+34_linux-x64_bin.tar.gz'; 			downloadSha256='d49c0df93307a9bd06c9ca7b35ce6d068246a0938d0802933910b42574c173d3'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/34/GPL/openjdk-24-ea+34_linux-aarch64_bin.tar.gz'; 			downloadSha256='ffab3ade32683a348fbb81aef96107b38545d1df7daa4e7ca81fe0f6775002ea'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 31 Jan 2025 01:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:581a00b5a05c96a59ee2d9151f24d1e5a8071c04d7471e01bb3cda14fc06c99c`  
		Last Modified: Tue, 04 Feb 2025 10:44:12 GMT  
		Size: 3.8 MB (3833711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c10f679e287dba8623f628f385883af3eaf7f7ce6d7ad742ebe8da9c381ec9`  
		Last Modified: Tue, 04 Feb 2025 10:45:59 GMT  
		Size: 210.9 MB (210929540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-34-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:f6fcc8ca3b5aae1e52af96d2f8bb98f8392adbcb54aef33796c6433ca83e87c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2553906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7565b7dde9e72c94dda16d7d14d7642768632353b095407728fa74d4a4b0d3f6`

```dockerfile
```

-	Layers:
	-	`sha256:6d6b6a85aa90a349e1d7378751e8db6fd834415f7dd9bfaa5027bcff6f6377ee`  
		Last Modified: Tue, 04 Feb 2025 10:45:54 GMT  
		Size: 2.5 MB (2534249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d21f172dce45a9222089ef2c7c808e9fdc2a5daf708f8563a11d99e229d28c34`  
		Last Modified: Tue, 04 Feb 2025 10:45:54 GMT  
		Size: 19.7 KB (19657 bytes)  
		MIME: application/vnd.in-toto+json
