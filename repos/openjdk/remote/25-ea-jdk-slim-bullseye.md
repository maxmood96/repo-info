## `openjdk:25-ea-jdk-slim-bullseye`

```console
$ docker pull openjdk@sha256:40a4d1fe65ca32418afaf3e9f3fc37384d9b28d6696c295994f0e811720ce26b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-jdk-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:255f08cc099c2036fdfc2e6a8629bbff39bd54925b297ca98b8e64ba5231ae61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.8 MB (244840568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a504a7c81ae555381ac8f167e2d203203e40256eca75aa4d5ef0661266ab6f3d`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Sat, 10 May 2025 00:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 10 May 2025 00:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Sat, 10 May 2025 00:48:12 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 10 May 2025 00:48:12 GMT
ENV LANG=C.UTF-8
# Sat, 10 May 2025 00:48:12 GMT
ENV JAVA_VERSION=25-ea+22
# Sat, 10 May 2025 00:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/22/GPL/openjdk-25-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='ce6d616a09c8fb4391dbe165428d33b1751a228581faf829ac0610db8120ddbf'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/22/GPL/openjdk-25-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='76b4d96328978d3ba01a6970ff47dd1f368e42e94a8ba51fb3260e07230de663'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 10 May 2025 00:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c8e1eb8ab3b017bd9e33ddec83ebdd8292c542bbd14a8d5a6cfa2edc3ad3b8eb`  
		Last Modified: Thu, 08 May 2025 17:04:40 GMT  
		Size: 30.3 MB (30254604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef5c4718b544f6184abc15cf2e13a176e24e276b00bee989665976997ff5af7`  
		Last Modified: Fri, 16 May 2025 13:12:57 GMT  
		Size: 1.6 MB (1581759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e95bdc0923bef5e21be3b9eb6b57af5fc26ea052c55476c39f61cf2739b63988`  
		Last Modified: Fri, 16 May 2025 13:13:03 GMT  
		Size: 213.0 MB (213004205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:ca17f8b00406a43846c857c429277f2916eb05a2235b108ac52615b5502e1af4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2846830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d8a08ecdbef2b1ca9d1c388a1cf49c59c4cf05854341e245fda470348afadd2`

```dockerfile
```

-	Layers:
	-	`sha256:db81fc9aa6baa5fb15436764f338fa3876c494514a4f8372fa8231152338e1af`  
		Last Modified: Mon, 12 May 2025 19:12:41 GMT  
		Size: 2.8 MB (2829261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:855419081d143ef1d9b5fc5fd80f310418abef2b520b2f820e9528f4d025ab84`  
		Last Modified: Mon, 12 May 2025 19:12:41 GMT  
		Size: 17.6 KB (17569 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-jdk-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:08f088d0adf262168ebbb2c59f75277aaaf677ec6ea54bc7d5f6327baffaf905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.1 MB (241121905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c33f70abd675c1179304acb80082de49beb886e8ceb9945d7a0c36f38725279`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Sat, 10 May 2025 00:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 10 May 2025 00:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Sat, 10 May 2025 00:48:12 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 10 May 2025 00:48:12 GMT
ENV LANG=C.UTF-8
# Sat, 10 May 2025 00:48:12 GMT
ENV JAVA_VERSION=25-ea+22
# Sat, 10 May 2025 00:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/22/GPL/openjdk-25-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='ce6d616a09c8fb4391dbe165428d33b1751a228581faf829ac0610db8120ddbf'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/22/GPL/openjdk-25-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='76b4d96328978d3ba01a6970ff47dd1f368e42e94a8ba51fb3260e07230de663'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 10 May 2025 00:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5d3a81360c5bb9281a4f735a1468429a1898f1a4fc24a2581dde4cf28ace4488`  
		Last Modified: Thu, 08 May 2025 17:04:53 GMT  
		Size: 28.7 MB (28744645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d1d03c9692493694719245e4b5b02ab0a2a3800faca912a034232dbda85c83`  
		Last Modified: Thu, 08 May 2025 17:37:25 GMT  
		Size: 1.6 MB (1565931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71066890245ccb6411b2ffe851c4cc1cdc96a1a5a161e7dc30ce0cc45f8a63f6`  
		Last Modified: Mon, 12 May 2025 19:25:28 GMT  
		Size: 210.8 MB (210811329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:9b287cb6acddac496c6174b2c748004c94e9bbc45906ef82b6802e26c400b643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2846626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1959ec62cfdf9e098d71f544085cb2f410c14c2efc9b0e3f452fee678ec91feb`

```dockerfile
```

-	Layers:
	-	`sha256:2888914954e5025b931afaf916757d72861b7b8e0f41d9411f6485ce54b3e884`  
		Last Modified: Mon, 12 May 2025 19:25:21 GMT  
		Size: 2.8 MB (2828913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b216b979e68f2b3e558952a7a931140ec985909e15fd34471f7350e11bf04313`  
		Last Modified: Mon, 12 May 2025 19:25:21 GMT  
		Size: 17.7 KB (17713 bytes)  
		MIME: application/vnd.in-toto+json
