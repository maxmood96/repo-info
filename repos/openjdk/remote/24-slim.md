## `openjdk:24-slim`

```console
$ docker pull openjdk@sha256:2a5a3f6f21d2e8ac10a22338d117134fd5b8dc7125007cfcffc024d370ca1500
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:5a1e04c65a8242e84cd113f0491715662450f50bbca079835f66afa6d6c67c9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.2 MB (245238568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b49c2d713f334b0a8d76f7336cbd69b00e4cc727fac0b26148c8cebe8d32443`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Tue, 04 Feb 2025 19:48:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 19:48:14 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Tue, 04 Feb 2025 19:48:14 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Feb 2025 19:48:14 GMT
ENV LANG=C.UTF-8
# Tue, 04 Feb 2025 19:48:14 GMT
ENV JAVA_VERSION=24-ea+35
# Tue, 04 Feb 2025 19:48:14 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/35/GPL/openjdk-24-ea+35_linux-x64_bin.tar.gz'; 			downloadSha256='bf5289b474e53b34a9ece42dcd3ae073e5ef7df63fcb9c44fbcac92496dedd99'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/35/GPL/openjdk-24-ea+35_linux-aarch64_bin.tar.gz'; 			downloadSha256='96e6ce86751c7aceb6e5f435be31ecbd0629592097abbd67d1c0f5c5b85c8f78'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 04 Feb 2025 19:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:084f4263b0081fac22e7a8ace1b27571f334d1ee8853ffcf9724057b6e4aeb95`  
		Last Modified: Tue, 04 Feb 2025 23:32:27 GMT  
		Size: 4.0 MB (4018426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551e58bd23cdc125d4bf1e1896abefc1a6c78e430d9b78b52ade4bfbf767a056`  
		Last Modified: Tue, 04 Feb 2025 23:32:30 GMT  
		Size: 213.0 MB (213007839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:6aef174058665c81df6224e02628b6e429ae7ec486bfe2985910b28982882616
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2557721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d3ddb50362ef0e66c5927ac1a6fbe02bc5e00378d2eab9b9bb91a7492880e89`

```dockerfile
```

-	Layers:
	-	`sha256:331f6634e7bf596c865eb6ce116d7d3d43759c75ea3b2ea76cd90388259402cf`  
		Last Modified: Tue, 04 Feb 2025 23:32:27 GMT  
		Size: 2.5 MB (2538279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba01fd3e4a63778ded036e2cebd49180c150a6967a2b1ea8c5e7cc17d1e8582a`  
		Last Modified: Tue, 04 Feb 2025 23:32:27 GMT  
		Size: 19.4 KB (19442 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-slim` - linux; arm64 variant v8

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

### `openjdk:24-slim` - unknown; unknown

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
