## `openjdk:19-jdk-slim-buster`

```console
$ docker pull openjdk@sha256:d1a208deca3d6a02c93673a174850bab9bd0952cc68bd84fb8153727494502b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:19-jdk-slim-buster` - linux; amd64

```console
$ docker pull openjdk@sha256:dfd3a3be050dd1ece611699e1db3e7b2b2caa0cb3cb6be1198538c0f0b59deac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.6 MB (226593036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbb4246bc92bef5b63b8c0bae9ab3510495bac0c3804e6483eafa8d91c6e9bcb`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 28 May 2022 01:20:43 GMT
ADD file:0513eda9512e010cb9459591b62e0c9d9319750923df091b64250ad6e98c2878 in / 
# Sat, 28 May 2022 01:20:43 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:17:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:17:27 GMT
ENV JAVA_HOME=/usr/local/openjdk-19
# Sat, 28 May 2022 02:17:27 GMT
ENV PATH=/usr/local/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 02:17:27 GMT
ENV LANG=C.UTF-8
# Mon, 06 Jun 2022 19:45:05 GMT
ENV JAVA_VERSION=19-ea+25
# Mon, 06 Jun 2022 19:45:19 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/25/GPL/openjdk-19-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='f03ae5efd6a8fe2211e9c3e0566289d405193244c67af680e202aa9f44473cb0'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/25/GPL/openjdk-19-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='f0c7f51bcf0bcca03127dd1dc7f9b59a88636714ea2bfd0707da665f98011237'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 06 Jun 2022 19:45:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c1ad9731b2c7bf7fddea67f2f3f553515179a375c489e591e2372700fcaca766`  
		Last Modified: Sat, 28 May 2022 01:26:05 GMT  
		Size: 27.1 MB (27140144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e02e4b83f9271ba56f1acb8a87f59b6f1a9e549bcf2da4d95261b153bc68d9f`  
		Last Modified: Sat, 28 May 2022 02:29:15 GMT  
		Size: 3.3 MB (3273373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f4432e3c5cb7ac2fcbb5cb0ad89638ddb04eac667d37561b8d665959b2d627a`  
		Last Modified: Mon, 06 Jun 2022 19:53:58 GMT  
		Size: 196.2 MB (196179519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-jdk-slim-buster` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:7342b43f0f9e1b2615725831017cb2484fb412f5ff907dc08172aa7c0b04837d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.9 MB (223903511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9351b645e1b084b430e47f9f5f9804bd34df1cd0acf41e19738f349cf5e74d7`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 28 May 2022 00:41:05 GMT
ADD file:d0e42d603f275c040783ec7b6c051200815492fc35b73110234dfcd584e6cdec in / 
# Sat, 28 May 2022 00:41:05 GMT
CMD ["bash"]
# Sat, 28 May 2022 01:38:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 01:38:02 GMT
ENV JAVA_HOME=/usr/local/openjdk-19
# Sat, 28 May 2022 01:38:03 GMT
ENV PATH=/usr/local/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 01:38:04 GMT
ENV LANG=C.UTF-8
# Mon, 06 Jun 2022 22:47:08 GMT
ENV JAVA_VERSION=19-ea+25
# Mon, 06 Jun 2022 22:47:21 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/25/GPL/openjdk-19-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='f03ae5efd6a8fe2211e9c3e0566289d405193244c67af680e202aa9f44473cb0'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/25/GPL/openjdk-19-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='f0c7f51bcf0bcca03127dd1dc7f9b59a88636714ea2bfd0707da665f98011237'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 06 Jun 2022 22:47:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4931fb8ba4223cb35034141162105ee5482122692b2931eb69eec912ce64606d`  
		Last Modified: Sat, 28 May 2022 00:48:26 GMT  
		Size: 25.9 MB (25914033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48fd49b058d9314bede6d26981edcf8cfa5f28eebce620889117829184769a12`  
		Last Modified: Sat, 28 May 2022 01:56:24 GMT  
		Size: 3.1 MB (3126023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a36a16bdc56c9d9aca5c21b7293815e16c3bc34dd20b709095679a4d9026923a`  
		Last Modified: Mon, 06 Jun 2022 23:01:45 GMT  
		Size: 194.9 MB (194863455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
