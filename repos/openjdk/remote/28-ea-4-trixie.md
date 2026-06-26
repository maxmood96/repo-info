## `openjdk:28-ea-4-trixie`

```console
$ docker pull openjdk@sha256:bbfb38e8724248ab8aee0d5674f1ac35f0ca54e6b306d75fd1d31baad820d519
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:28-ea-4-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:3dde65dd3ddf978f5d01e731a211359a26eef7809e9e5dd66a88a6f4de40a3aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.3 MB (386330904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3cc6f0324bf30ceb32fd9fe4a2a2adf0747db02486a0c8b2fb6317bcd343c49`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:41:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 02:28:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 26 Jun 2026 17:49:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jun 2026 17:50:02 GMT
ENV JAVA_HOME=/usr/local/openjdk-28
# Fri, 26 Jun 2026 17:50:02 GMT
ENV PATH=/usr/local/openjdk-28/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jun 2026 17:50:02 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jun 2026 17:50:02 GMT
ENV JAVA_VERSION=28-ea+4
# Fri, 26 Jun 2026 17:50:02 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/4/GPL/openjdk-28-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='3f349a9ae39761069b8132f7ba529bec7bf6c759376f77cb57520d3f21d4fa23'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/4/GPL/openjdk-28-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='a49e869b72df691c734d29e133fd15ae49bed271913327704c9bca6c2132525d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Jun 2026 17:50:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:aa3e9ef32f73c30e8b065800ee66429992d3bfea6a1fb8224afdd878ab5b994f`  
		Last Modified: Wed, 24 Jun 2026 00:28:33 GMT  
		Size: 49.3 MB (49317255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f59c84a786323367a79d4959142649bb24b16c989bbaae7f273550b47325959`  
		Last Modified: Wed, 24 Jun 2026 01:41:50 GMT  
		Size: 25.6 MB (25634938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d0db852850114cc79598cc8ab1ec19da54691d9e3267288bb3458d7488f125`  
		Last Modified: Wed, 24 Jun 2026 02:28:58 GMT  
		Size: 67.8 MB (67778134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee856833728ff02fee3dc5176347c2d0fbd582c4ef96efae6103fbfb349b9dd`  
		Last Modified: Fri, 26 Jun 2026 17:50:28 GMT  
		Size: 16.1 MB (16065709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14c741da00599b9e229a5183909737d768ff78ec4b0de202d44b8478983f50a1`  
		Last Modified: Fri, 26 Jun 2026 17:50:31 GMT  
		Size: 227.5 MB (227534868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:28-ea-4-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:308401ea143765a28b5b3fe364e42281fa14b16e24e930a39f03a4a930ed4a9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8526783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e03f273197cae80dd3901c3535bc048f38a0b91c14c3ed2e7538bebc39591721`

```dockerfile
```

-	Layers:
	-	`sha256:10a573ab890cf3a552f2ff2c6a826c78e8cba2f14ac6511f284e9e3cf0c0c836`  
		Last Modified: Fri, 26 Jun 2026 17:50:27 GMT  
		Size: 8.5 MB (8508887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dde63acb06ac4654f24895082b4f3280c3d01d45de73d2d7c7e90a86d48f610`  
		Last Modified: Fri, 26 Jun 2026 17:50:26 GMT  
		Size: 17.9 KB (17896 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:28-ea-4-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:0a121235fd6a429b25a2f99f9dbe6b559655d2b5f5b21be37322bbcefa86b185
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.9 MB (383949752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18467f3b075e1ddb4fa4fd916ec293ba6c466d8e3be8c643e92de49135b497bd`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:45:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 02:35:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 26 Jun 2026 17:54:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jun 2026 17:54:49 GMT
ENV JAVA_HOME=/usr/local/openjdk-28
# Fri, 26 Jun 2026 17:54:49 GMT
ENV PATH=/usr/local/openjdk-28/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jun 2026 17:54:49 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jun 2026 17:54:49 GMT
ENV JAVA_VERSION=28-ea+4
# Fri, 26 Jun 2026 17:54:49 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/4/GPL/openjdk-28-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='3f349a9ae39761069b8132f7ba529bec7bf6c759376f77cb57520d3f21d4fa23'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/4/GPL/openjdk-28-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='a49e869b72df691c734d29e133fd15ae49bed271913327704c9bca6c2132525d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Jun 2026 17:54:49 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c8a311258fd162f6aa0db134045a19154c81a2244ff9ed7620256c95ae5d6b69`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 49.7 MB (49678395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe059c57e3bc40ea8086d6be574927bed6c0a000b182f3354b758009265e197`  
		Last Modified: Wed, 24 Jun 2026 01:45:26 GMT  
		Size: 25.0 MB (25026863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cf605f6b62a65326644e598c84134d29702579734c83dfca4cedf5dad7fb6d3`  
		Last Modified: Wed, 24 Jun 2026 02:35:43 GMT  
		Size: 67.6 MB (67592645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d923d96d444f7a374f539c52cb844ef10bbc8a1ceadbabe8284e738258d522`  
		Last Modified: Fri, 26 Jun 2026 17:55:14 GMT  
		Size: 16.1 MB (16071437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bed1ca16131431d46f422b9e202280af853e51bd3113a6292b549bc2b3c10a1`  
		Last Modified: Fri, 26 Jun 2026 17:55:19 GMT  
		Size: 225.6 MB (225580412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:28-ea-4-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:f12e5c1bb380e1cded28a2a0938ca25f577f14f749c1048752aee3552f7fbe87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8721055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e8070311aa7a8d97e05bc553804bb5446e4afc9f1a685a8f50e35c30586e145`

```dockerfile
```

-	Layers:
	-	`sha256:ecde856890965a71fbd955d0c1ce0f8295e5a0087aedca057c3340603178a764`  
		Last Modified: Fri, 26 Jun 2026 17:55:14 GMT  
		Size: 8.7 MB (8703040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fbdbc8ace42a68a6bf1daaffa7066b7fb997a5688287c15e435242fa24fb6bc`  
		Last Modified: Fri, 26 Jun 2026 17:55:14 GMT  
		Size: 18.0 KB (18015 bytes)  
		MIME: application/vnd.in-toto+json
