## `openjdk:26-trixie`

```console
$ docker pull openjdk@sha256:347d385977c2ef6d22ca5fb72933a36e9fcaafcdc49af5af4804b2fcd23fdde9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:b35db6e2c53d310b77277fdce65651a5b9f91fb48203b33f95ce2dba9f010053
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.7 MB (384673200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3ccdc948e81352bc669345511efee2b562007eb4b165e5ed44b2f5c5d6ce804`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 31 Oct 2025 20:29:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Oct 2025 20:29:45 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Fri, 31 Oct 2025 20:29:45 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 20:29:45 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 20:29:45 GMT
ENV JAVA_VERSION=26-ea+22
# Fri, 31 Oct 2025 20:29:45 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/22/GPL/openjdk-26-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='b87eeeb2167b024e3e62fb5ab860c0e2ad004d2e04f716b9f885d1180ac97a03'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/22/GPL/openjdk-26-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='b401cd0d932a4b8fd19f44deb517bfe9441097f31a2bbdb247e3b8757772e147'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 31 Oct 2025 20:29:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:795dbedde24d2c72dafd2b71fe36643552e56859c0e29cdb095ed54b825fbaa2`  
		Last Modified: Tue, 21 Oct 2025 00:20:33 GMT  
		Size: 49.3 MB (49284971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d573bf42b377ce6a5a0451c15388849686fa4058efd68999f3b014daeb5b55`  
		Last Modified: Tue, 21 Oct 2025 01:42:47 GMT  
		Size: 25.6 MB (25615545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26dfe2fac1c486e9aaf41d1028ed30be2c442aa84af44462bc7bac8c148ffb13`  
		Last Modified: Tue, 21 Oct 2025 04:47:38 GMT  
		Size: 67.8 MB (67784857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c4361db36022577735b2522230b5123c3f029ae45d778c74384f0166e514a4`  
		Last Modified: Fri, 31 Oct 2025 20:30:23 GMT  
		Size: 16.1 MB (16061574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b1572c93c969abb0de0918e4d64422e72dcea6f75608284df6317a2cc429cce`  
		Last Modified: Fri, 31 Oct 2025 21:26:18 GMT  
		Size: 225.9 MB (225926253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:5da9607b40462fbcdf66534ac309b0503b1a6fdffd07ef50bbfd1bedb3baf347
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8529689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:508f2962908b330643fde9d961011a75a967ed017a90e5fd3beff1c9f482c74f`

```dockerfile
```

-	Layers:
	-	`sha256:16f5cf84235fcbdf281f8c3653cf523b59de29ee29c68e040f86d986116d9d53`  
		Last Modified: Fri, 31 Oct 2025 21:24:27 GMT  
		Size: 8.5 MB (8511148 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f6a6cf89e543af026b2be47cc476982476aa87017473095387aff5c8d322686`  
		Last Modified: Fri, 31 Oct 2025 21:24:28 GMT  
		Size: 18.5 KB (18541 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:fe19fcb65479f59aac0c15a3b4736f157b2d3c9ad4404dc1bc2fcaa248177e20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.1 MB (382087019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e423f3457fa6cd35d7d8c6d052bce3daf3091776d55d8b070a64c50844640f8`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 31 Oct 2025 20:09:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Oct 2025 20:09:42 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Fri, 31 Oct 2025 20:09:42 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 20:09:42 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 20:09:42 GMT
ENV JAVA_VERSION=26-ea+22
# Fri, 31 Oct 2025 20:09:42 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/22/GPL/openjdk-26-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='b87eeeb2167b024e3e62fb5ab860c0e2ad004d2e04f716b9f885d1180ac97a03'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/22/GPL/openjdk-26-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='b401cd0d932a4b8fd19f44deb517bfe9441097f31a2bbdb247e3b8757772e147'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 31 Oct 2025 20:09:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2a101b2fcb53d61db540cb76da094137d4f0291a93fa41357ab70c3debf4d3c3`  
		Last Modified: Tue, 21 Oct 2025 00:22:57 GMT  
		Size: 49.6 MB (49649743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f510ac7d6fe76c0362c0162daee6964c5b93b20f5ddf65021b0bf3bcce16f306`  
		Last Modified: Tue, 21 Oct 2025 01:47:21 GMT  
		Size: 25.0 MB (25017463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721433549fef8bfa398445abce4a12b5c7e64775b3de57bfc3ff37c8ed6fc0e4`  
		Last Modified: Tue, 21 Oct 2025 02:35:46 GMT  
		Size: 67.6 MB (67583109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0ad7839266a44d2b503b67b00972cbf7a4f2a7e5a05f6c9c42e811904d42ca0`  
		Last Modified: Fri, 31 Oct 2025 20:10:28 GMT  
		Size: 16.1 MB (16070754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b6cbd1bcec539d9adba51f7b04e3f62fe2e432ef1e2ba1094ff3a1c8b81af5`  
		Last Modified: Fri, 31 Oct 2025 21:26:06 GMT  
		Size: 223.8 MB (223765950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:2540f9ece9917205a4f2b2b4c940b5260d02341c0cc3dfb686aba8eafbb578d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8724646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d312b8f37017d3792520b2b4d6807884b281759883be3f4ab6cacc40a33c7e8`

```dockerfile
```

-	Layers:
	-	`sha256:83bc60e5356ffd6d53fea6aa2da0c2e92addbf76dda3ab0047a83a31ca41f85b`  
		Last Modified: Fri, 31 Oct 2025 21:24:34 GMT  
		Size: 8.7 MB (8705962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c02ec8bdf7fc2f9277a1aa6b84665368dac8828b08ff263943fe680de351dae1`  
		Last Modified: Fri, 31 Oct 2025 21:24:35 GMT  
		Size: 18.7 KB (18684 bytes)  
		MIME: application/vnd.in-toto+json
