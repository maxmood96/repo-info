## `openjdk:24-ea-16-jdk-slim-bullseye`

```console
$ docker pull openjdk@sha256:16136f45498df7532c28c4449341705b8c2b0e75a2fbe8d8422ccdcfd352ff42
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:24-ea-16-jdk-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:6b2bb5c63c818a81d863e678fea86697573e11bf4855b60492eee724113d7b0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.1 MB (245072036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1917bad0a82c6d7923b2727b080ac829669775dce313892669deeb86d42a8d73`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 04 Sep 2024 22:31:09 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Wed, 04 Sep 2024 22:31:09 GMT
CMD ["bash"]
# Fri, 20 Sep 2024 00:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 20 Sep 2024 00:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 20 Sep 2024 00:48:11 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Sep 2024 00:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 20 Sep 2024 00:48:11 GMT
ENV JAVA_VERSION=24-ea+16
# Fri, 20 Sep 2024 00:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/16/GPL/openjdk-24-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='46c9e29e1e700ac596a07ef1795142939bcfd687dcc7f959043886bf800a3bee'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/16/GPL/openjdk-24-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='f42ff15af07babf02cf4dc52c121b18be22bc6f54d6b041b424687f82cdd9919'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 20 Sep 2024 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3435ef3497303936851f2ccfe989afd81bbc91cb20089a31d04967aad9511482`  
		Last Modified: Fri, 20 Sep 2024 17:57:38 GMT  
		Size: 1.6 MB (1581762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6fafe2054366f8ac53b78e0b801dd29b22ed2ecd03aed3df059da34f2db29e0`  
		Last Modified: Fri, 20 Sep 2024 17:57:41 GMT  
		Size: 212.1 MB (212061597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-16-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:3d83a51ceaf574c142ab98834ac5928932fde43f6e9666e369077986ae224614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.4 KB (20381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7181ba760ce0a5ae958015a86cc7546a176582e1ca4017e77d37bf1517c8bd22`

```dockerfile
```

-	Layers:
	-	`sha256:b8d84c47bc8c11cc64cd8aeca58b624b1f4a64979d2a41d5e6f72e75c4de9239`  
		Last Modified: Fri, 20 Sep 2024 17:57:38 GMT  
		Size: 3.0 KB (3023 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:369b9d40563d00791147bc6338eaf70f39560dde4fa577855296fdef84b2c3cd`  
		Last Modified: Fri, 20 Sep 2024 17:57:38 GMT  
		Size: 17.4 KB (17358 bytes)  
		MIME: application/vnd.in-toto+json
