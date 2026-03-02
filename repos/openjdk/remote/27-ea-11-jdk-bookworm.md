## `openjdk:27-ea-11-jdk-bookworm`

```console
$ docker pull openjdk@sha256:ef007933ff43f2d34e3c97955ca500dd00b7c5424ee0c8797a60af77cceba224
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-11-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:a706bc3371841f519c320901f211eda0cc6b7fbc29fd0829ef2d9bf7021f0d1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.4 MB (382403619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4da0dd874efa24180ea08035d50c22995bc6f298d93ed1f5a2b8a9598f7570d5`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:18:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:03:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Mar 2026 21:25:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Mar 2026 21:26:05 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Mon, 02 Mar 2026 21:26:05 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 21:26:05 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 21:26:05 GMT
ENV JAVA_VERSION=27-ea+11
# Mon, 02 Mar 2026 21:26:05 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/11/GPL/openjdk-27-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='75a300b52539589c8c4b172ef292d5b58486de4d88d774be659975bc661767bf'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/11/GPL/openjdk-27-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='3bf27bc49545e677311a0eab8a838953f4726191499accef492c7feaf801e429'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 02 Mar 2026 21:26:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6a7e0620566c7dfbe5d3c9a7601d116556ec17a021b3e824f8ab09d12b0c25c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:43 GMT  
		Size: 48.5 MB (48488777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab3b37e4807fe48145826511e16a527bbc4695222ceb966669a4d16729b3b94`  
		Last Modified: Tue, 24 Feb 2026 19:18:52 GMT  
		Size: 24.0 MB (24038450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa27031269f0a970255d56a9e793fc2a9d6bb091463cd5e632af4ae274881601`  
		Last Modified: Tue, 24 Feb 2026 20:03:49 GMT  
		Size: 64.4 MB (64395853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8069537987d1b3ed823ac25e330a1fe04ee7ab7eaa4defdeee6d547a63798299`  
		Last Modified: Mon, 02 Mar 2026 21:26:29 GMT  
		Size: 16.9 MB (16945240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc506fa46c62e27b6649f6077e67c53a14f45d0cc9e9419c477409513fb8cc2`  
		Last Modified: Mon, 02 Mar 2026 21:26:32 GMT  
		Size: 228.5 MB (228535299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-11-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:00e1b1be2ad52d7c841221f4b3477e4acb71212e526a64aa446eca2bcb20bdba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8686824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:366d152809ce71eb211acbd797a870b7af74959e7c2160590d4e3c0d1bc871d0`

```dockerfile
```

-	Layers:
	-	`sha256:c28a9f4bfdc92d5ea7c3a705bba294b617b24d059f89675af7233467e1372e2e`  
		Last Modified: Mon, 02 Mar 2026 21:26:28 GMT  
		Size: 8.7 MB (8668885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25c30173470fc6915ce68a644c500e291569e3c756d7295c8f3aa0830a9435f1`  
		Last Modified: Mon, 02 Mar 2026 21:26:28 GMT  
		Size: 17.9 KB (17939 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-11-jdk-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:69617267c9e5baa77f1af60ffbfa61ae228d58f0797f81705cfaabb56cfd73b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.7 MB (380668210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c7d5d2fe80210b973a71f2a28f7f732661e17b323647472ec932247db6ac583`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:24:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:14:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Mar 2026 21:24:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Mar 2026 21:24:58 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Mon, 02 Mar 2026 21:24:58 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 21:24:58 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 21:24:58 GMT
ENV JAVA_VERSION=27-ea+11
# Mon, 02 Mar 2026 21:24:58 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/11/GPL/openjdk-27-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='75a300b52539589c8c4b172ef292d5b58486de4d88d774be659975bc661767bf'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/11/GPL/openjdk-27-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='3bf27bc49545e677311a0eab8a838953f4726191499accef492c7feaf801e429'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 02 Mar 2026 21:24:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8578011282ae3fef36307f7e3afb2265a96bada1a57648f07bea9cc1a11e7b7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:06 GMT  
		Size: 48.4 MB (48373210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443d4217b87aad21c6acb58313c9038eb24571a4e9f81de2463aaf19d403a640`  
		Last Modified: Tue, 24 Feb 2026 19:24:13 GMT  
		Size: 23.6 MB (23604736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d27b842bb73f4af595ce58848c4c53ae713ca5c649636d25b483ca63bccc52`  
		Last Modified: Tue, 24 Feb 2026 20:14:46 GMT  
		Size: 64.5 MB (64479406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0935ac5c1923f32e4cdd6f185ee215cf9357e77f7d68dde5de67412f0f9a1353`  
		Last Modified: Mon, 02 Mar 2026 21:25:24 GMT  
		Size: 17.7 MB (17729089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3adc76b08ed6ec952e2d6d53413f3b1f64ec7275adc3e4a3426000f369858cd9`  
		Last Modified: Mon, 02 Mar 2026 21:25:28 GMT  
		Size: 226.5 MB (226481769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-11-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:dc82c5a5fbe493222403755a0a1512bc8e035941f31eaaa6b414f92dc4c58559
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8823788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:041018201edcae73aae8c5eed0dd6d87e9b504fbf43a70051f4caa4feb89b1f0`

```dockerfile
```

-	Layers:
	-	`sha256:3ede78bbbf494d5c317bb89c919c7ca45a45839687d1cc9a922afeb28987bd2a`  
		Last Modified: Mon, 02 Mar 2026 21:25:24 GMT  
		Size: 8.8 MB (8805730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:913810fb3689aa88e2cda72fd4c7f157e782a710c8cede6431ad34a90ebcf6c8`  
		Last Modified: Mon, 02 Mar 2026 21:25:23 GMT  
		Size: 18.1 KB (18058 bytes)  
		MIME: application/vnd.in-toto+json
