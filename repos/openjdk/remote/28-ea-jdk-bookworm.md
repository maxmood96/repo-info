## `openjdk:28-ea-jdk-bookworm`

```console
$ docker pull openjdk@sha256:0afd581de3ea2cc6aff0b868bc9f0640b4c6376dc1a2e06809da21c57e1c22dc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:28-ea-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:5c6ab3a9bd15c759b1a3dd5d56d8d122ebda39b0990206411af04e3420f5ad1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.4 MB (381394179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f144d939269cf755b3617e94153b5fd8c7cdd87454618949d68bfd256629d7f1`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:42:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:24:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jun 2026 22:38:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jun 2026 22:39:05 GMT
ENV JAVA_HOME=/usr/local/openjdk-28
# Mon, 22 Jun 2026 22:39:05 GMT
ENV PATH=/usr/local/openjdk-28/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 22:39:05 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 22:39:05 GMT
ENV JAVA_VERSION=28-ea+3
# Mon, 22 Jun 2026 22:39:05 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/3/GPL/openjdk-28-ea+3_linux-x64_bin.tar.gz'; 			downloadSha256='44b5bc19b0533fb00a363915f15ee1c9a9514dca2fb5bd56d13c204676ceef67'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/3/GPL/openjdk-28-ea+3_linux-aarch64_bin.tar.gz'; 			downloadSha256='12d4698e60552120853334a624fd1d10ffca8386b1c52b0089fc9c607a9d46e8'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 22 Jun 2026 22:39:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:01cedcff86f879d042805360ecba268802bec3d8201484ff3ec54f4250a2d3b7`  
		Last Modified: Wed, 10 Jun 2026 23:39:39 GMT  
		Size: 48.5 MB (48502042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da31edd9efdb812e66d13819903973ea6b188d2e7358547676d33d1e3f706f2`  
		Last Modified: Thu, 11 Jun 2026 00:42:23 GMT  
		Size: 24.0 MB (24044000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fbaeeb62b9d03a1204b85c3b257aa3e1ce2c4ccfeea479fb2e659211019c29d`  
		Last Modified: Thu, 11 Jun 2026 02:24:43 GMT  
		Size: 64.4 MB (64404116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0037b773835ac3ff614dd9ffca0ce3416f470b31166b0aec837bc8a117894e02`  
		Last Modified: Mon, 22 Jun 2026 22:39:29 GMT  
		Size: 16.9 MB (16946435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc859f98642fe03b0690050ff0bab011affbbfb9957f0116f04314ac045e8ba2`  
		Last Modified: Mon, 22 Jun 2026 22:39:33 GMT  
		Size: 227.5 MB (227497586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:28-ea-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:fd4b7c6a74d84b5c9b0643e7f301bcddbe2cc3bc59da750e899d7c878a8b35c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8684288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c948e9909a86906618370845bd44c695eab2af668ad95378b9d1550a02659c8`

```dockerfile
```

-	Layers:
	-	`sha256:ba90f5a970643e9bf8fce9f1111c5085ad0a2e037e5f0b61ec85e485e02a26ca`  
		Last Modified: Mon, 22 Jun 2026 22:39:29 GMT  
		Size: 8.7 MB (8666366 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba8c1f2e62ef746fe9f83ca2ea6a9b4f0d80c6bc3fe0553613371a6e65c51882`  
		Last Modified: Mon, 22 Jun 2026 22:39:28 GMT  
		Size: 17.9 KB (17922 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:28-ea-jdk-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:19dddd80555521e0552fb94b17c0a79061bdd6fd41c2bd8a6ea1f47bd1914d62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.8 MB (379760172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49f0911ec2a89054fc247c50a3eaa5b33d01113d7da5002cd1dc019b4fbaac6e`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:43:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:24:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jun 2026 22:38:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jun 2026 22:38:55 GMT
ENV JAVA_HOME=/usr/local/openjdk-28
# Mon, 22 Jun 2026 22:38:55 GMT
ENV PATH=/usr/local/openjdk-28/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 22:38:55 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 22:38:55 GMT
ENV JAVA_VERSION=28-ea+3
# Mon, 22 Jun 2026 22:38:55 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/3/GPL/openjdk-28-ea+3_linux-x64_bin.tar.gz'; 			downloadSha256='44b5bc19b0533fb00a363915f15ee1c9a9514dca2fb5bd56d13c204676ceef67'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/3/GPL/openjdk-28-ea+3_linux-aarch64_bin.tar.gz'; 			downloadSha256='12d4698e60552120853334a624fd1d10ffca8386b1c52b0089fc9c607a9d46e8'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 22 Jun 2026 22:38:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c847f328095fb083f4a22895b90fe4226efa6458ac57362b64b6e5d99da9e4a3`  
		Last Modified: Wed, 10 Jun 2026 23:39:28 GMT  
		Size: 48.4 MB (48389016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f511b4c80a6e453785fbcd573c1bf1cb986c4e8d43ed4500ad1ac9a4719762b`  
		Last Modified: Thu, 11 Jun 2026 00:43:56 GMT  
		Size: 23.6 MB (23613296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b715a6712db064e97302c819acd7a39c0c72f8a315ff83c6ad1c27bfa1b275e`  
		Last Modified: Thu, 11 Jun 2026 02:25:01 GMT  
		Size: 64.5 MB (64487878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8622a63cd9dc39250c1636ec0a4a38d0847e4a76a0f400265d56d53844da72dc`  
		Last Modified: Mon, 22 Jun 2026 22:39:21 GMT  
		Size: 17.7 MB (17730431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e74af0004ce8d35474af7a2062cea1ce78ea6501cae152257a3b025a47167ee`  
		Last Modified: Mon, 22 Jun 2026 22:39:25 GMT  
		Size: 225.5 MB (225539551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:28-ea-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:82d5a766fde42027c8603a528c409c0ab59358450d985698290871083dd1d5b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8821252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84ce95f3b6f088e192fbab28ff481332b83d484ee1bb92c5bb871464d4f897ed`

```dockerfile
```

-	Layers:
	-	`sha256:c26f63074909ea416e2c39495fac0fbc134f0d243ccc48097e094c1d7240fff3`  
		Last Modified: Mon, 22 Jun 2026 22:39:21 GMT  
		Size: 8.8 MB (8803211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7cbc893fcf7e37d32cd3ede034df0e3a0f5df283e053c11e9a71066cdde09b2`  
		Last Modified: Mon, 22 Jun 2026 22:39:20 GMT  
		Size: 18.0 KB (18041 bytes)  
		MIME: application/vnd.in-toto+json
