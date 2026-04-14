## `openjdk:27-ea-jdk-trixie`

```console
$ docker pull openjdk@sha256:0e14b1f90e6379b8fa772ab4405325cbb55191a808c56ef9d059a89263ec2a00
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-jdk-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:bf0849cd3d4b2a7ef4e2b466f3f78ea41e2aed0fba5e8dbd60eb0230fd53cdea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.7 MB (387737577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af8fe70cbc4aae2301d14d8f669bb96207660211ac21254988fe83e251fbb8a7`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:47:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 02:43:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 14 Apr 2026 00:00:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Apr 2026 00:01:06 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 14 Apr 2026 00:01:06 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 00:01:06 GMT
ENV LANG=C.UTF-8
# Tue, 14 Apr 2026 00:01:06 GMT
ENV JAVA_VERSION=27-ea+17
# Tue, 14 Apr 2026 00:01:06 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/17/GPL/openjdk-27-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='9052972f914c38a9c00c5d8104a0b58217438f9a672ae7abead7c12347bb0d7c'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/17/GPL/openjdk-27-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='c2be8295243785a5077e17817615b5f355a643367e44eef5972e58fcbd8bde4b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 14 Apr 2026 00:01:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a7730063fcfe708b222d34c4f07d633dfe087a28c05c4daaab2fa9943854c155`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 49.3 MB (49297833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33970743aee750df25f6c661132b7401c8fefe930e5f4803f4c8b6f567a6b55`  
		Last Modified: Tue, 07 Apr 2026 01:47:22 GMT  
		Size: 25.6 MB (25621678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5397da1d1537c4d725f3090c5688a582e14eeaf7743d75d9b38bad1649554987`  
		Last Modified: Tue, 07 Apr 2026 02:43:39 GMT  
		Size: 67.8 MB (67780708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2279e12dcec0bb20a22a837ced0c695a36ab7660a9ff1abf82ee158bcd38cdfc`  
		Last Modified: Tue, 14 Apr 2026 00:01:31 GMT  
		Size: 16.1 MB (16064952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d75e56b36f44fe523de816ba4437a2bbc16f00f4d7ab07df4fde4385fcf57632`  
		Last Modified: Tue, 14 Apr 2026 00:01:40 GMT  
		Size: 229.0 MB (228972406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:627f43f63b2cdb636b9c2d2e75db532d9867880edd0e4fc78cd74b0931603e51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8529049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4521b5e611916040684b4aef162cfc3fa3de688566a0f283c6463bf5e534039d`

```dockerfile
```

-	Layers:
	-	`sha256:8e9edb647e045e521ece716aa90fee63e2f68be3c03b65c64ca6632b1f0cb035`  
		Last Modified: Tue, 14 Apr 2026 00:01:32 GMT  
		Size: 8.5 MB (8511136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d6f828038b2203fb0aad1e3889efc00cd75b22a0a331a91cb8398caf5ae0faa`  
		Last Modified: Tue, 14 Apr 2026 00:01:31 GMT  
		Size: 17.9 KB (17913 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-jdk-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:1d487f127f4b2304c2eb8d6eceb56eb5ba25a96112b6809dcf2b9db820141621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.3 MB (385285423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a150c3c4772c38bc00d0f71566b5f32e2327f1e54c7322b5156ba2c02845b9`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:50:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 02:53:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 14 Apr 2026 00:02:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Apr 2026 00:02:33 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 14 Apr 2026 00:02:33 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 00:02:33 GMT
ENV LANG=C.UTF-8
# Tue, 14 Apr 2026 00:02:33 GMT
ENV JAVA_VERSION=27-ea+17
# Tue, 14 Apr 2026 00:02:33 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/17/GPL/openjdk-27-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='9052972f914c38a9c00c5d8104a0b58217438f9a672ae7abead7c12347bb0d7c'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/17/GPL/openjdk-27-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='c2be8295243785a5077e17817615b5f355a643367e44eef5972e58fcbd8bde4b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 14 Apr 2026 00:02:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:912041a7b9f63b6550d3a3949c43e45f74a36a2f80c727e70e41cbe851de2d20`  
		Last Modified: Tue, 07 Apr 2026 00:11:19 GMT  
		Size: 49.7 MB (49665256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277ee5883c1f173b0485b465221ddea5443b64c95935146f0bb3655baee3647d`  
		Last Modified: Tue, 07 Apr 2026 01:50:26 GMT  
		Size: 25.0 MB (25023654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6084ed286765ee022e8f8d9df76b9a2bd97a3224c379e905079f3bb11e1e48ca`  
		Last Modified: Tue, 07 Apr 2026 02:54:15 GMT  
		Size: 67.6 MB (67591915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6693161ab2fe7037bcfdda2798a5f9a048fef6a392a7933456fbc76cf85755b1`  
		Last Modified: Tue, 14 Apr 2026 00:03:00 GMT  
		Size: 16.1 MB (16071287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016bbab74d1793740ff273a6ede8e2d8f3bbca4aae77ef9c9b414f6e1f889143`  
		Last Modified: Tue, 14 Apr 2026 00:03:03 GMT  
		Size: 226.9 MB (226933311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:49453b316d44325c3c755da9f5481b9b7554117ca1f2e58c4b8acf9b4a6feeda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8723957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea86ce011ff5f78ec6e8d7a6a74e9111b0a96ee885c98a453425b3fa78bb6219`

```dockerfile
```

-	Layers:
	-	`sha256:8af0ceeae41a1d48c1cf05203778ff63e62012bdb09628708e8f8377cdd68149`  
		Last Modified: Tue, 14 Apr 2026 00:02:59 GMT  
		Size: 8.7 MB (8705926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36e1f0576d03167c95b1dd70604b1900f261d63ff674e5341cd751597422c213`  
		Last Modified: Tue, 14 Apr 2026 00:02:59 GMT  
		Size: 18.0 KB (18031 bytes)  
		MIME: application/vnd.in-toto+json
