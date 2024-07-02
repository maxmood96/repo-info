## `openjdk:23-ea-29-jdk-slim-bookworm`

```console
$ docker pull openjdk@sha256:1dc7dea0b600743767501c6f1c190f3919cc0066e7997235ee7a0ca9feeda198
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:23-ea-29-jdk-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:da7da57b3895e4c97101427e367b7cbb45d8889da1b9222a1eef944436834615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244615470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8091003541829a01b4e3d85cf262fc18771893b1ec044bf78e2193942b46cd8b`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 29 Jun 2024 00:48:10 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
# Sat, 29 Jun 2024 00:48:10 GMT
CMD ["bash"]
# Sat, 29 Jun 2024 00:48:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Jun 2024 00:48:10 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Sat, 29 Jun 2024 00:48:10 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 29 Jun 2024 00:48:10 GMT
ENV LANG=C.UTF-8
# Sat, 29 Jun 2024 00:48:10 GMT
ENV JAVA_VERSION=23-ea+29
# Sat, 29 Jun 2024 00:48:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/29/GPL/openjdk-23-ea+29_linux-x64_bin.tar.gz'; 			downloadSha256='1ecb4977a7385dde5f7155e22cfdad0bec51afb8ff4dece08a061bab64be8aaa'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/29/GPL/openjdk-23-ea+29_linux-aarch64_bin.tar.gz'; 			downloadSha256='a14bddc20e706cf85f28b8cc360e3dc2506b51cff9a0e62125f3213de6c41f00'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 29 Jun 2024 00:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1755da18c51eaa543974a8ce431ada6d6f2fc67229dd6ce67989fc1f360f7b7a`  
		Last Modified: Tue, 02 Jul 2024 03:21:17 GMT  
		Size: 4.0 MB (4016774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59519207a269e43dc61a0b8a760c80decf53e8afa412aacb8c162ef9ac66f72a`  
		Last Modified: Tue, 02 Jul 2024 03:21:22 GMT  
		Size: 211.5 MB (211472418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-29-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:124607c280dcf8394472d0d5b7a67924a82e12ee8e1e518539821b5599811aa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2365575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3c9edc032b8a449c1138e138f7b6d10ccde40154f10020d74e1e1521157294a`

```dockerfile
```

-	Layers:
	-	`sha256:d6ecf81bd715da322a60a8815f6f83761ba626ac16b2d9c97d0c8e0c50a16b63`  
		Last Modified: Tue, 02 Jul 2024 03:21:17 GMT  
		Size: 2.3 MB (2346345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:035a080c35fd15450299e4c3c8145cbe16e890d69c3e5560e73d2b38531e1bfb`  
		Last Modified: Tue, 02 Jul 2024 03:21:17 GMT  
		Size: 19.2 KB (19230 bytes)  
		MIME: application/vnd.in-toto+json
