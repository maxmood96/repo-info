## `openjdk:24-ea-bookworm`

```console
$ docker pull openjdk@sha256:6e7b424ab31e7c2291b8f63900903a484d83503ce3f463f2a36cb081f4c9a4ad
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:6df4a8f6ded10ce2e5036a1e940d9e4877d04f05a587b0a1d17ce1ed02f2c21c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.5 MB (366544573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a50a2c429a3ce497d9e75ad622273ac8770c86c37c8f5914ade1f4c657ae4a68`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Dec 2024 01:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Dec 2024 01:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Sat, 07 Dec 2024 01:48:13 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Dec 2024 01:48:13 GMT
ENV LANG=C.UTF-8
# Sat, 07 Dec 2024 01:48:13 GMT
ENV JAVA_VERSION=24-ea+27
# Sat, 07 Dec 2024 01:48:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/27/GPL/openjdk-24-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='99196f78561dace922e06c52af4d33157ded8ae02a8009f35ea2fb7075dda452'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/27/GPL/openjdk-24-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='e78b5c2b599fd835fb88bfe9155b27e16dfcab3e0488bb63051c073acabd5cba'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 07 Dec 2024 01:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fdf894e782a221820acf469d425b802be26aedb5e5d26ea80a650ff6a974d488`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 48.5 MB (48497210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd71677db44bb63b94de61b6f1f95d5540b4ba2d6a8a6bc4d19f422b25e0c2b`  
		Last Modified: Tue, 03 Dec 2024 02:28:49 GMT  
		Size: 23.9 MB (23865876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551df7f94f9c131f2fec0e8063142411365f0a1c88b935b9fac22be91af227e0`  
		Last Modified: Tue, 03 Dec 2024 03:17:14 GMT  
		Size: 64.4 MB (64391508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63eac54fb665b58115841aaf36d446a2444debc63a9bba40a6c5c9aa6123e1fd`  
		Last Modified: Mon, 09 Dec 2024 23:30:46 GMT  
		Size: 16.9 MB (16943079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e499609f6a1d124be30e0e11d199cd4fb16e98924ea26cbf577c789564e29126`  
		Last Modified: Mon, 09 Dec 2024 23:30:50 GMT  
		Size: 212.8 MB (212846900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:478b267068f70747281cfb3d4ec0e77191d7f4481c06ba1df8b021a32372ce47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8466427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2e3dda4aefb349841fbb3eded6993869bdf8ff5cc18fe52f01c83987786e128`

```dockerfile
```

-	Layers:
	-	`sha256:79647507a6dc4a08cceb91937b177dfea7f0009111d6f769cce0f542db6a6365`  
		Last Modified: Mon, 09 Dec 2024 23:30:45 GMT  
		Size: 8.4 MB (8447809 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2aa72e0b64ff2e445fbbc63c6691e7c7d901ccfcd7cf270668ca74c4989acc7a`  
		Last Modified: Mon, 09 Dec 2024 23:30:45 GMT  
		Size: 18.6 KB (18618 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:968d8e56c2f3990e52244ca5a2748ec69a5b9ed507d1082f75c671861a845024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.6 MB (364604347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e357eb102d9238ad9ace1429e9b9847fe5258f1625f2c61a889a6e88c084141b`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Dec 2024 01:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Dec 2024 01:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Sat, 07 Dec 2024 01:48:13 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Dec 2024 01:48:13 GMT
ENV LANG=C.UTF-8
# Sat, 07 Dec 2024 01:48:13 GMT
ENV JAVA_VERSION=24-ea+27
# Sat, 07 Dec 2024 01:48:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/27/GPL/openjdk-24-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='99196f78561dace922e06c52af4d33157ded8ae02a8009f35ea2fb7075dda452'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/27/GPL/openjdk-24-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='e78b5c2b599fd835fb88bfe9155b27e16dfcab3e0488bb63051c073acabd5cba'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 07 Dec 2024 01:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:82312fccb35f18983647c1ea71154b98ae9893fb61ca4febe12d584a3ea9ad6d`  
		Last Modified: Tue, 03 Dec 2024 01:29:57 GMT  
		Size: 48.3 MB (48325680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac722d9cf93b238dec2480278a2df5f8ccb672c97ec39f191191fd39f6721a8`  
		Last Modified: Tue, 03 Dec 2024 05:38:46 GMT  
		Size: 23.4 MB (23405813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:261351ed796deb9fdad22dc734919eaf6726dd79a8dea99327d9e1376ecdcbce`  
		Last Modified: Tue, 03 Dec 2024 11:50:22 GMT  
		Size: 64.3 MB (64347852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133b2b6add979b2154435e8ffa765b9f6bf91b9c32635e0e18067f8505b1f4e3`  
		Last Modified: Tue, 10 Dec 2024 01:28:50 GMT  
		Size: 17.7 MB (17726651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a737195788f083cc4ae770d0f8cd78efde75b2fda3d3659569731529e1598284`  
		Last Modified: Tue, 10 Dec 2024 01:34:04 GMT  
		Size: 210.8 MB (210798351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:a3a6980cc401f49ab808d4ffdc11862459215771c1a7fa27225c0738ea8da7e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8603605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55fd104ebb2e26b9c04952ebaf1e67bc7285029ce23cd588e4b81b9a8117e28a`

```dockerfile
```

-	Layers:
	-	`sha256:fd7b57597c9b76815701f4831b49836d2d3f619ffaef30f41f0e75cee1ea0016`  
		Last Modified: Tue, 10 Dec 2024 01:33:59 GMT  
		Size: 8.6 MB (8584844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3231bd1e46049cd2a3f5bb4c70b50825e0c083028fb9a439b3b95d0fa54b5a1b`  
		Last Modified: Tue, 10 Dec 2024 01:33:59 GMT  
		Size: 18.8 KB (18761 bytes)  
		MIME: application/vnd.in-toto+json
