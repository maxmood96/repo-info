## `openjdk:27-ea-jdk-slim-bookworm`

```console
$ docker pull openjdk@sha256:71e8554e00864cbca9898b18320a72aab8daf0db67d9e427b86ad7fb19ca33d1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-jdk-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:517cc3a38ec9a9b1f1193ecf7018d9d738af5728a5f63b3206c792b393c4dcf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.9 MB (260905844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b5d591b3f5816b652e7e217f6bddbbd2b885b81ecb9d8a2b8f1dccdc1e0bdec`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Tue, 05 May 2026 23:04:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 May 2026 23:04:57 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 05 May 2026 23:04:57 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:04:57 GMT
ENV LANG=C.UTF-8
# Tue, 05 May 2026 23:04:57 GMT
ENV JAVA_VERSION=27-ea+20
# Tue, 05 May 2026 23:04:57 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/20/GPL/openjdk-27-ea+20_linux-x64_bin.tar.gz'; 			downloadSha256='a7c288898b71578ab424b0234102cb576ac5cf71c31bbdacc5d610a36be3d9cb'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/20/GPL/openjdk-27-ea+20_linux-aarch64_bin.tar.gz'; 			downloadSha256='47a8c6fedd9b292e5b5a5ad9e4cd238eecfc4d1cf098f052d48e7b6f19a0b025'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 05 May 2026 23:04:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0a779f10e947d75f08ad6ec0c40f1985346a679a613ff0d2d02621c187d4b7`  
		Last Modified: Tue, 05 May 2026 23:05:16 GMT  
		Size: 4.0 MB (4030612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2413a6a9c83a28ba4a48a43a82daa8bcc13a5fecc4304819e1ec747ca88c087`  
		Last Modified: Tue, 05 May 2026 23:05:20 GMT  
		Size: 228.6 MB (228638980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:c7b1e79537bb766a1358e9cb6b5bd7fdc80ccdb4c5e1d2dd7d4943880fa5eb64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2665408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1dd1db3dbf8d72b531ab6c6afb747528ac32c05875778e9786bc8bc68c454ee`

```dockerfile
```

-	Layers:
	-	`sha256:e3f9ffe4e9387449e16c92c9c074ea902713e367825943204a15103219c97b8d`  
		Last Modified: Tue, 05 May 2026 23:05:16 GMT  
		Size: 2.6 MB (2648537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e71a1965f41c6845c42f5e6da345e71d9f2aa23fcfe4019b43dc242f6d4891f`  
		Last Modified: Tue, 05 May 2026 23:05:15 GMT  
		Size: 16.9 KB (16871 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-jdk-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:3a710b177ea7165f34af1ca818fea8cede78c6f28799ceb5b52807649c3f0214
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.6 MB (258574080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48c505b90b6d662a0d9d28e3a1e31b228615d52938e418d4f4b625570197af80`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Tue, 05 May 2026 23:04:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 May 2026 23:05:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 05 May 2026 23:05:13 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:05:13 GMT
ENV LANG=C.UTF-8
# Tue, 05 May 2026 23:05:13 GMT
ENV JAVA_VERSION=27-ea+20
# Tue, 05 May 2026 23:05:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/20/GPL/openjdk-27-ea+20_linux-x64_bin.tar.gz'; 			downloadSha256='a7c288898b71578ab424b0234102cb576ac5cf71c31bbdacc5d610a36be3d9cb'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/20/GPL/openjdk-27-ea+20_linux-aarch64_bin.tar.gz'; 			downloadSha256='47a8c6fedd9b292e5b5a5ad9e4cd238eecfc4d1cf098f052d48e7b6f19a0b025'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 05 May 2026 23:05:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:46ac7a0b9811e518f6b5a0d52940c913a1a560a8f78b82267804914e50244d2d`  
		Last Modified: Wed, 22 Apr 2026 00:16:03 GMT  
		Size: 28.1 MB (28116114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ec0f37d8ecd50c07e12862e2346f6f3677f3482c72e466e02b92d5214e6661`  
		Last Modified: Tue, 05 May 2026 23:05:34 GMT  
		Size: 3.9 MB (3852308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c465a5c0b92ed626883c65523f252f5f44c2511325b1356bb6d73e3ebf9b69d5`  
		Last Modified: Tue, 05 May 2026 23:05:39 GMT  
		Size: 226.6 MB (226605658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:a114b91ce224167897c629d20b73f934682ebdbf080e36a9cb6876eeb09ca780
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2665161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a44acfd5ccc643b3080dfc0ae316bcd06ef9adb0da492dd8e9b0afed843054de`

```dockerfile
```

-	Layers:
	-	`sha256:7cc731d241eef119ded1b70ce2fa5468b2cd13be74bcc5be8fc55e17e34b94c5`  
		Last Modified: Tue, 05 May 2026 23:05:34 GMT  
		Size: 2.6 MB (2648171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c644a67c2b78169e95ba736996552751b5d114c5a93bff13d802b7af85d11b4`  
		Last Modified: Tue, 05 May 2026 23:05:33 GMT  
		Size: 17.0 KB (16990 bytes)  
		MIME: application/vnd.in-toto+json
