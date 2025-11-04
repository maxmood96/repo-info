## `openjdk:26-ea-22-jdk-trixie`

```console
$ docker pull openjdk@sha256:e1dc3156500ec8b640e6954b6fcbf5ab9fefc78f5eff1d845f788af283de6f19
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-22-jdk-trixie` - linux; amd64

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

### `openjdk:26-ea-22-jdk-trixie` - unknown; unknown

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

### `openjdk:26-ea-22-jdk-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:d8cc9be90efe188b3aa9f410635cc112f52d376641f447d390a4720faf129007
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.1 MB (382088400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:900f0604c8f950499b5823e3fe347818422b4fc812337245aa3dcb2e6aa2d4d2`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 02:20:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 03:19:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:20:01 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Tue, 04 Nov 2025 03:20:01 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 03:20:01 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 03:20:01 GMT
ENV JAVA_VERSION=26-ea+22
# Tue, 04 Nov 2025 03:20:01 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/22/GPL/openjdk-26-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='b87eeeb2167b024e3e62fb5ab860c0e2ad004d2e04f716b9f885d1180ac97a03'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/22/GPL/openjdk-26-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='b401cd0d932a4b8fd19f44deb517bfe9441097f31a2bbdb247e3b8757772e147'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 04 Nov 2025 03:20:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:04077a68e2b807cad70ec4dfc0a2e8e1ff1ea6d9523e4c8f042b9a1ae8a54409`  
		Last Modified: Tue, 04 Nov 2025 00:13:46 GMT  
		Size: 49.7 MB (49650430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f766ef2ec48737a0f300405019c312acd667d14467b50c402750d1454e3591`  
		Last Modified: Tue, 04 Nov 2025 01:30:11 GMT  
		Size: 25.0 MB (25017577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:186d0d0b2411f880d1a385216013fead1acb2dee0584aac75da87dfdeb1202db`  
		Last Modified: Tue, 04 Nov 2025 02:21:20 GMT  
		Size: 67.6 MB (67583874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da9dabce176f02cb5c6c71242eba840398fa5705be876e1319c96495fa5be43a`  
		Last Modified: Tue, 04 Nov 2025 03:21:05 GMT  
		Size: 16.1 MB (16070586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7506b29b69ab71289f712c17887d0c782c72f54dfd04007375a74e35b8515065`  
		Last Modified: Tue, 04 Nov 2025 10:39:18 GMT  
		Size: 223.8 MB (223765933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-22-jdk-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:7b29b818db0afe4d4302ba851b13f35404f37848fe3b3b01357d042d6e5fb2be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8723350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e695d51fd4a46a03ece6cb9156a1629de21f8171a70a341836238f217cd13093`

```dockerfile
```

-	Layers:
	-	`sha256:74c220f43dce9720ff73d34e52296b7d2cdda51cc25b78263ec080b6a98651ea`  
		Last Modified: Tue, 04 Nov 2025 10:23:54 GMT  
		Size: 8.7 MB (8705318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e607b642c2a88ecbffad91e567dc5bbd12acd0f634122b08d5102d6e22f3fcd`  
		Last Modified: Tue, 04 Nov 2025 10:23:55 GMT  
		Size: 18.0 KB (18032 bytes)  
		MIME: application/vnd.in-toto+json
