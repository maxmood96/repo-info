## `golang:latest`

```console
$ docker pull golang@sha256:9295ba678e3764d79ac0aeabdbcf281a91933c81c8de29387d8a2f557e256cdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.14393.3443; amd64
	-	windows version 10.0.17763.973; amd64

### `golang:latest` - linux; amd64

```console
$ docker pull golang@sha256:85f189a5bda8f1cf807fe77c50a231dffd7e7c955ece38feeed9e416e9676400
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.6 MB (308572529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:297e5bf50f50837ab5f136b3b0568b5890a5e03e3e2faf0abfdd3e10945ed440`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 17:20:38 GMT
ADD file:a5ec219cbfc4e0c31e7df48cc51abd9a5b92754e15403b2ab726e25042041680 in / 
# Sat, 01 Feb 2020 17:20:39 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 00:18:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 00:19:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sun, 02 Feb 2020 00:19:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 14:05:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Fri, 14 Feb 2020 01:21:40 GMT
ENV GOLANG_VERSION=1.13.8
# Fri, 14 Feb 2020 01:21:51 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='0567734d558aef19112f2b2873caa0c600f1b4a5827930eb5a7f35235219e9d8' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='75f590d8e048a97cbf8b09837b15b3e6b44e1374718a96a5c3a994843ef44a4d' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='b46c0235054d0eb69a295a2634aec8a11c7ae19b3dc53556a626b89dc1f8cdb0' ;; 		i386) goRelArch='linux-386'; goRelSha256='2305c1c46b3eaf574c7b03cfa6b167c199a2b52da85872317438c90074fdb46e' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='4c987b3969d33a93880a218064d2330d7f55c9b58698e78db6b56012058e91a9' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='994f961df0d7bdbfa6f7eed604539acf9159444dabdff3ce8e938d095d85f756' ;; 		*) goRelArch='src'; goRelSha256='b13bf04633d4d8cf53226ebeaace8d4d2fd07ae6fa676d0844a688339debec34'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url"; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		echo >&2; 		echo >&2 'error: UNIMPLEMENTED'; 		echo >&2 'TODO install golang-any from jessie-backports for GOROOT_BOOTSTRAP (and uninstall after build)'; 		echo >&2; 		exit 1; 	fi; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Fri, 14 Feb 2020 01:21:51 GMT
ENV GOPATH=/go
# Fri, 14 Feb 2020 01:21:51 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Feb 2020 01:21:52 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 14 Feb 2020 01:21:52 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:dc65f448a2e2f2ea557e69ed9ac65aa8ac0e16f1bce68f90de910b4d5a2f1ba1`  
		Last Modified: Sat, 01 Feb 2020 17:26:04 GMT  
		Size: 50.4 MB (50379770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:346ffb2b67d7b35729673ced818325ed0ea57284e69de67f8bbc48c2bf294716`  
		Last Modified: Sun, 02 Feb 2020 00:37:48 GMT  
		Size: 7.8 MB (7811673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dea4ecac934f71d68d4f5edb171f6cff42588edfa3f70ba8709be56e321eeddc`  
		Last Modified: Sun, 02 Feb 2020 00:37:49 GMT  
		Size: 10.0 MB (9996251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ac92ddf84b35dac36ef6632f8d5a0c9c2d7038f6018f2d4fa1be056d90bd366`  
		Last Modified: Sun, 02 Feb 2020 00:38:05 GMT  
		Size: 51.8 MB (51791113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca6053833076bc7bd2c5666a847913b0e00163e65c5267e9f5d6e427b9f2b10`  
		Last Modified: Sun, 02 Feb 2020 14:07:58 GMT  
		Size: 68.5 MB (68523253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f47e6cebc5126c53ef9c1635358e57ff7f11f5ad1689d43d105350519ec7531b`  
		Last Modified: Fri, 14 Feb 2020 01:33:24 GMT  
		Size: 120.1 MB (120070343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5303501560106b7786bf68a88b0ac18bb9479fbb16233f262510188f69c61110`  
		Last Modified: Fri, 14 Feb 2020 01:33:02 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:latest` - linux; arm variant v7

```console
$ docker pull golang@sha256:d08768065eae164ab50267442d30526b8cf12bf23db7dfa8f43c2fe12a7247a9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.9 MB (260892731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a37b9efe7b6972a445fe5c8ce8db47215778b75252881cab370a464e8922114`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 17:00:06 GMT
ADD file:a57a312731f174c4b03031908ff95f49d7055d8c196439f0ed07ed9c4834d993 in / 
# Sat, 01 Feb 2020 17:00:08 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 18:00:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 18:00:24 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 01 Feb 2020 18:01:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 14:30:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Fri, 14 Feb 2020 01:09:31 GMT
ENV GOLANG_VERSION=1.13.8
# Fri, 14 Feb 2020 01:09:54 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='0567734d558aef19112f2b2873caa0c600f1b4a5827930eb5a7f35235219e9d8' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='75f590d8e048a97cbf8b09837b15b3e6b44e1374718a96a5c3a994843ef44a4d' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='b46c0235054d0eb69a295a2634aec8a11c7ae19b3dc53556a626b89dc1f8cdb0' ;; 		i386) goRelArch='linux-386'; goRelSha256='2305c1c46b3eaf574c7b03cfa6b167c199a2b52da85872317438c90074fdb46e' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='4c987b3969d33a93880a218064d2330d7f55c9b58698e78db6b56012058e91a9' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='994f961df0d7bdbfa6f7eed604539acf9159444dabdff3ce8e938d095d85f756' ;; 		*) goRelArch='src'; goRelSha256='b13bf04633d4d8cf53226ebeaace8d4d2fd07ae6fa676d0844a688339debec34'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url"; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		echo >&2; 		echo >&2 'error: UNIMPLEMENTED'; 		echo >&2 'TODO install golang-any from jessie-backports for GOROOT_BOOTSTRAP (and uninstall after build)'; 		echo >&2; 		exit 1; 	fi; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Fri, 14 Feb 2020 01:09:56 GMT
ENV GOPATH=/go
# Fri, 14 Feb 2020 01:09:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Feb 2020 01:10:01 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 14 Feb 2020 01:10:02 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9bbb41bca8c6254da5088d03354297b1309dc75c2ccc738416025f89709ae5ee`  
		Last Modified: Sat, 01 Feb 2020 17:07:28 GMT  
		Size: 45.9 MB (45859700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:239e4acdbc2ab88c89aa359fbab11429ea6d7bd93ea589a22c6bbb833ff82b93`  
		Last Modified: Sat, 01 Feb 2020 18:25:50 GMT  
		Size: 7.1 MB (7096223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83d6b4707a3c3aff9cb939fc058b869c5412e78c37e43eb0b653565460495537`  
		Last Modified: Sat, 01 Feb 2020 18:25:50 GMT  
		Size: 9.3 MB (9343278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e096c4fc8c629edca6da3ce5a9e95288512cb11e3d3d01a6e49078d19c2acca`  
		Last Modified: Sat, 01 Feb 2020 18:26:13 GMT  
		Size: 47.3 MB (47315591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca29eebbe47938ede4b91d684551d2cd027b2947a5aa2dffb6b64aee43fef432`  
		Last Modified: Sun, 02 Feb 2020 14:36:25 GMT  
		Size: 53.0 MB (52996899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99c7cc2d18bd671763b1524bb2d3506acea5edefada1962983dc0f884e2a3c6e`  
		Last Modified: Fri, 14 Feb 2020 01:23:02 GMT  
		Size: 98.3 MB (98280883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41dd97565cd7536fc5119d87550e5ba1950a1737eefdebf98c0219a0bd882e49`  
		Last Modified: Fri, 14 Feb 2020 01:22:31 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:latest` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:07c4c45e00f98809aeb7d0efc29acfd439c26b76b96eaca41aeda038c109237b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.9 MB (278928303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d30259568cf3570cc71424ccc266a6a292c0353468169f1e235b90f120094e03`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:40:50 GMT
ADD file:b423f4b0ed41dfe1334031fe9b21f7e1c88ccb031d7e8f2ff165d618323424d7 in / 
# Sat, 01 Feb 2020 16:40:53 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:18:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 17:18:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 01 Feb 2020 17:19:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 11:08:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Fri, 14 Feb 2020 00:42:57 GMT
ENV GOLANG_VERSION=1.13.8
# Fri, 14 Feb 2020 00:43:10 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='0567734d558aef19112f2b2873caa0c600f1b4a5827930eb5a7f35235219e9d8' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='75f590d8e048a97cbf8b09837b15b3e6b44e1374718a96a5c3a994843ef44a4d' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='b46c0235054d0eb69a295a2634aec8a11c7ae19b3dc53556a626b89dc1f8cdb0' ;; 		i386) goRelArch='linux-386'; goRelSha256='2305c1c46b3eaf574c7b03cfa6b167c199a2b52da85872317438c90074fdb46e' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='4c987b3969d33a93880a218064d2330d7f55c9b58698e78db6b56012058e91a9' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='994f961df0d7bdbfa6f7eed604539acf9159444dabdff3ce8e938d095d85f756' ;; 		*) goRelArch='src'; goRelSha256='b13bf04633d4d8cf53226ebeaace8d4d2fd07ae6fa676d0844a688339debec34'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url"; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		echo >&2; 		echo >&2 'error: UNIMPLEMENTED'; 		echo >&2 'TODO install golang-any from jessie-backports for GOROOT_BOOTSTRAP (and uninstall after build)'; 		echo >&2; 		exit 1; 	fi; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Fri, 14 Feb 2020 00:43:12 GMT
ENV GOPATH=/go
# Fri, 14 Feb 2020 00:43:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Feb 2020 00:43:14 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 14 Feb 2020 00:43:15 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bc03a7ced18fc43ea9523dfb256d2c3fbb835dc0bb54bdb7fd309edf936a87e7`  
		Last Modified: Sat, 01 Feb 2020 16:46:06 GMT  
		Size: 49.2 MB (49171687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba9d528c1473d79c18b401d44ca06b9733d9c51a8699b98e8325c9de60b9739`  
		Last Modified: Sat, 01 Feb 2020 17:34:59 GMT  
		Size: 7.7 MB (7680993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:981400d5d268dc989681d5f308b7d2e381809f0bcc82429f443f7539cf6117ba`  
		Last Modified: Sat, 01 Feb 2020 17:34:59 GMT  
		Size: 10.0 MB (9983754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b2d547b8bc79a444406e56d724fb7d961c953e7f2797de4f55b29abee5605f`  
		Last Modified: Sat, 01 Feb 2020 17:35:22 GMT  
		Size: 52.1 MB (52102938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c84a606fada5847b27d4f74a29fdf4fb7b8ab9430f363c3f35669cabe7a0daf2`  
		Last Modified: Sun, 02 Feb 2020 11:13:40 GMT  
		Size: 62.4 MB (62390640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fec97dce1f46a010d480666405989eab1870ac992b90d2df4f3aaaec58ae46a9`  
		Last Modified: Fri, 14 Feb 2020 00:55:45 GMT  
		Size: 97.6 MB (97598135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc3212ac4c8545d3f4a7c7bc8a9dd86116d42a307f2e648b76019752ee1f3d5`  
		Last Modified: Fri, 14 Feb 2020 00:55:16 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:latest` - linux; 386

```console
$ docker pull golang@sha256:781664282d7607ad5d327a4f7aab62f91bcd61e11dc42a1d9989c30d835c883a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.6 MB (297555138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbcb567a713b912fd95c0fd1c33e0ae8e31f9c1d502c74fc357fcdf4e35771e6`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:39:21 GMT
ADD file:b637f96d557a570f8ab83b28f7b9cdd128958359dd30dc2e03df70b799e132aa in / 
# Sat, 01 Feb 2020 16:39:21 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:23:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 17:24:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 01 Feb 2020 17:24:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 10:42:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Fri, 14 Feb 2020 00:38:41 GMT
ENV GOLANG_VERSION=1.13.8
# Fri, 14 Feb 2020 00:38:52 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='0567734d558aef19112f2b2873caa0c600f1b4a5827930eb5a7f35235219e9d8' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='75f590d8e048a97cbf8b09837b15b3e6b44e1374718a96a5c3a994843ef44a4d' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='b46c0235054d0eb69a295a2634aec8a11c7ae19b3dc53556a626b89dc1f8cdb0' ;; 		i386) goRelArch='linux-386'; goRelSha256='2305c1c46b3eaf574c7b03cfa6b167c199a2b52da85872317438c90074fdb46e' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='4c987b3969d33a93880a218064d2330d7f55c9b58698e78db6b56012058e91a9' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='994f961df0d7bdbfa6f7eed604539acf9159444dabdff3ce8e938d095d85f756' ;; 		*) goRelArch='src'; goRelSha256='b13bf04633d4d8cf53226ebeaace8d4d2fd07ae6fa676d0844a688339debec34'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url"; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		echo >&2; 		echo >&2 'error: UNIMPLEMENTED'; 		echo >&2 'TODO install golang-any from jessie-backports for GOROOT_BOOTSTRAP (and uninstall after build)'; 		echo >&2; 		exit 1; 	fi; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Fri, 14 Feb 2020 00:38:53 GMT
ENV GOPATH=/go
# Fri, 14 Feb 2020 00:38:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Feb 2020 00:38:54 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 14 Feb 2020 00:38:54 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2b34644a479c82db66a603c0b0a1d990911345f8646498fa9b050f306d0e6bf2`  
		Last Modified: Sat, 01 Feb 2020 16:44:10 GMT  
		Size: 51.1 MB (51141949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2f611c9392c4fe86735b477d61fda0e95ea77486175a737114c51586ecce86`  
		Last Modified: Sat, 01 Feb 2020 17:42:17 GMT  
		Size: 8.0 MB (7981506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69713757cc2d87c3255331d40f5061a73ef412208961f1ddd67a59a375397fda`  
		Last Modified: Sat, 01 Feb 2020 17:42:17 GMT  
		Size: 10.3 MB (10338479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:956cf07a321afcfed99809a380a1905660e378188fd33d97f136551450be347a`  
		Last Modified: Sat, 01 Feb 2020 17:42:36 GMT  
		Size: 53.4 MB (53380753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:159d58090764ecf1adf8cab45ec531c80c784798e49d41a42e10b8738ef96ef6`  
		Last Modified: Sun, 02 Feb 2020 10:45:51 GMT  
		Size: 73.4 MB (73391925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562a978bbab15d2268a8a0209ede736161efe16d2eebdff53495c4466ce09ad8`  
		Last Modified: Fri, 14 Feb 2020 00:51:28 GMT  
		Size: 101.3 MB (101320400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ff7f773ae21c74163f123388d9e35799f4f2da79db0466d3bf5fb361e6eca6`  
		Last Modified: Fri, 14 Feb 2020 00:51:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:latest` - linux; ppc64le

```console
$ docker pull golang@sha256:036d5eb0fbdd7108d8ac224e17e013b60dc714286f3588a5de1d2d3798479937
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300362772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e2daee1bd32b83f075ac0dcd569f032b2d9e2140134897ba12d92591a44115a`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 17:17:37 GMT
ADD file:8e8c5417abc372541fe34cddec6fe8625ded93da51d1f5488e0aece309a3fd25 in / 
# Sat, 01 Feb 2020 17:17:45 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 18:37:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 18:38:16 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 01 Feb 2020 18:39:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 14:32:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Fri, 14 Feb 2020 01:17:08 GMT
ENV GOLANG_VERSION=1.13.8
# Fri, 14 Feb 2020 01:17:31 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='0567734d558aef19112f2b2873caa0c600f1b4a5827930eb5a7f35235219e9d8' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='75f590d8e048a97cbf8b09837b15b3e6b44e1374718a96a5c3a994843ef44a4d' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='b46c0235054d0eb69a295a2634aec8a11c7ae19b3dc53556a626b89dc1f8cdb0' ;; 		i386) goRelArch='linux-386'; goRelSha256='2305c1c46b3eaf574c7b03cfa6b167c199a2b52da85872317438c90074fdb46e' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='4c987b3969d33a93880a218064d2330d7f55c9b58698e78db6b56012058e91a9' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='994f961df0d7bdbfa6f7eed604539acf9159444dabdff3ce8e938d095d85f756' ;; 		*) goRelArch='src'; goRelSha256='b13bf04633d4d8cf53226ebeaace8d4d2fd07ae6fa676d0844a688339debec34'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url"; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		echo >&2; 		echo >&2 'error: UNIMPLEMENTED'; 		echo >&2 'TODO install golang-any from jessie-backports for GOROOT_BOOTSTRAP (and uninstall after build)'; 		echo >&2; 		exit 1; 	fi; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Fri, 14 Feb 2020 01:17:38 GMT
ENV GOPATH=/go
# Fri, 14 Feb 2020 01:17:40 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Feb 2020 01:17:45 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 14 Feb 2020 01:17:47 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a2d5a5ee40c1df8706e6db684b090e0e4297581ff38256a81222ea8be61180fc`  
		Last Modified: Sat, 01 Feb 2020 17:25:27 GMT  
		Size: 54.1 MB (54132833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f35d9825c38e7e0c3f571e8abe513b3b11599bd64a853ace5494e8c1ebe12a`  
		Last Modified: Sat, 01 Feb 2020 19:17:26 GMT  
		Size: 8.3 MB (8252196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e6d793f7577bc28e3d8da62385244985a340fe31c9eaa920a54185f9d46eb8`  
		Last Modified: Sat, 01 Feb 2020 19:17:26 GMT  
		Size: 10.7 MB (10727116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa97a0399500f41c90805413f9dd183cb0036f1446b766e62ad6310e2357d9b8`  
		Last Modified: Sat, 01 Feb 2020 19:18:21 GMT  
		Size: 57.4 MB (57392303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc0eec775fb25dc9e4e753c5a1513055bc30c10976f23b214a4963e8c62e384`  
		Last Modified: Sun, 02 Feb 2020 14:38:40 GMT  
		Size: 73.4 MB (73427259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b78ed60e5b8e2d43b304faab0ceff8aa8ae7bdc742475ac73326430905b7fba`  
		Last Modified: Fri, 14 Feb 2020 01:30:04 GMT  
		Size: 96.4 MB (96430908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c68fd9fd5e1aa09a18aa47c81f03427847d34e942da726f77b7aac21e7075121`  
		Last Modified: Fri, 14 Feb 2020 01:29:25 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:latest` - linux; s390x

```console
$ docker pull golang@sha256:efe05333fe6513ea9417db22a633d7c62c4347f3fa28b56969a7d7a990e114aa
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.3 MB (276254820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43c9994269926413cb0e0f93d8f74ae63cb74299f69e0fb5f435d040c0cdc09f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Oct 2019 23:42:27 GMT
ADD file:cacbc5a59bab479d85dfe3a5aec6e1ad9416d48e0e2f16b6033695dd2a83a853 in / 
# Wed, 16 Oct 2019 23:42:28 GMT
CMD ["bash"]
# Thu, 17 Oct 2019 00:21:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2019 00:21:30 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Oct 2019 00:22:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2019 17:07:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Fri, 01 Nov 2019 20:41:30 GMT
ENV GOLANG_VERSION=1.13.4
# Fri, 01 Nov 2019 20:41:54 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='692d17071736f74be04a72a06dab9cac1cd759377bd85316e52b2227604c004c' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='9f76e6353c9ae2dcad1731b7239531eb8be2fe171f29f2a9c5040945a930fd41' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='8b8d99eb07206f082468fb4d0ec962a819ae45d54065fc1ed6e2c502e774aaf0' ;; 		i386) goRelArch='linux-386'; goRelSha256='497934398ca57c7c207ce3388f099823923b4c7b74394d6ed64cd2d3751aecb8' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='815bf3c7100e73cfac50c4a07c8eeb4b0458a49ffa0e13a74a6cf7ad8e2a6499' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='efc6947e8eb0a6409f4c8ba62b00ae4e54404064bc221df1b73364a95945a350' ;; 		*) goRelArch='src'; goRelSha256='95dbeab442ee2746b9acf0934c8e2fc26414a0565c008631b04addb8c02e7624'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url"; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		echo >&2; 		echo >&2 'error: UNIMPLEMENTED'; 		echo >&2 'TODO install golang-any from jessie-backports for GOROOT_BOOTSTRAP (and uninstall after build)'; 		echo >&2; 		exit 1; 	fi; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Fri, 01 Nov 2019 20:41:55 GMT
ENV GOPATH=/go
# Fri, 01 Nov 2019 20:41:56 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Nov 2019 20:41:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 01 Nov 2019 20:41:58 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:aeaeeb43f723e2d6411dd54deca73da275af05abcbeaa06facfece152b7cc9f6`  
		Last Modified: Wed, 16 Oct 2019 23:48:15 GMT  
		Size: 48.9 MB (48949946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f716f569a549b2e83daadf9702956ea8c3147d4d0fd2a4c5c8f80b2fd26b7467`  
		Last Modified: Thu, 17 Oct 2019 00:36:20 GMT  
		Size: 7.4 MB (7380461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98ba6bcac41c3d29b1d4b7b541a18d8699f01e9cbcf2c25cf50da8d04e1fa1d3`  
		Last Modified: Thu, 17 Oct 2019 00:36:20 GMT  
		Size: 9.9 MB (9880236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d4f7797130be3fe685ad8e78ca714ccdcb83c6b93fb3edb74ac9c64b20f9325`  
		Last Modified: Thu, 17 Oct 2019 00:36:37 GMT  
		Size: 51.3 MB (51302006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:947785ae2d2a04c9d5a8b8735e36e89b60adebfc697ff3b9f2b058cda51dbce0`  
		Last Modified: Thu, 17 Oct 2019 17:11:42 GMT  
		Size: 56.6 MB (56588695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccd77785732ba7d252c3212e6cebb8dd0de1bd050f40dc1766a43f368f85b6ea`  
		Last Modified: Fri, 01 Nov 2019 20:53:08 GMT  
		Size: 102.2 MB (102153351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:681708f75f4151e2aec2a1aca3295553faebee704e00eaf19cbee061a57217ea`  
		Last Modified: Fri, 01 Nov 2019 20:52:50 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:latest` - windows version 10.0.14393.3443; amd64

```console
$ docker pull golang@sha256:719541ecf15e52844d081f901450429888fac02180dc8800f106037702845317
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5899874467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31d2a15890928d127a941d6a80e400324dac84549e0c3a85be4cff09219ec01a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Thu, 02 Jan 2020 15:48:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 14 Jan 2020 23:50:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jan 2020 13:12:27 GMT
ENV GIT_VERSION=2.23.0
# Wed, 15 Jan 2020 13:12:28 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 15 Jan 2020 13:12:29 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 15 Jan 2020 13:12:30 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 15 Jan 2020 13:14:08 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 15 Jan 2020 13:14:10 GMT
ENV GOPATH=C:\gopath
# Wed, 15 Jan 2020 13:15:21 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 14 Feb 2020 01:15:42 GMT
ENV GOLANG_VERSION=1.13.8
# Fri, 14 Feb 2020 01:24:26 GMT
RUN $url = ('https://golang.org/dl/go{0}.windows-amd64.zip' -f $env:GOLANG_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'aaf0888907144ca7070c8dad03fcf1308f77a42d2f6e4d2a609e64e9ae73cf4f'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Fri, 14 Feb 2020 01:24:28 GMT
WORKDIR C:\gopath
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:31f9df80631e7b5d379647ee7701ff50e009bd2c03b30a67a0a8e7bba4a26f94`  
		Size: 1.7 GB (1654613376 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f1c8c4c99f36cfcf87884a9382011e93fb05fa4002d8f4eca62a43e744db8e95`  
		Last Modified: Wed, 15 Jan 2020 01:46:47 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:928afb74ac8a072334bcabee201bfbc0936217d2fa1e8aba5d7e377cb995f48a`  
		Last Modified: Wed, 15 Jan 2020 14:17:15 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d950deb3f160624c0675efc8314222a7ebb6a525dc9b4c667a022a3d796aa8b9`  
		Last Modified: Wed, 15 Jan 2020 14:17:14 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12bab48f96d12c3da7ce1da86d0aaf6d30c4ea98ca0eee9c0a6f61ce03a143ad`  
		Last Modified: Wed, 15 Jan 2020 14:17:11 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ad2d905ad861e3648e8b50913912b3c9e5e82ba47963995a5b04eaea4b2d5a`  
		Last Modified: Wed, 15 Jan 2020 14:17:11 GMT  
		Size: 1.2 KB (1202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579b374cfb25041394c6240e13b17f10073fcbd5c0f48b368cbf62a60bce25df`  
		Last Modified: Wed, 15 Jan 2020 14:17:26 GMT  
		Size: 30.5 MB (30488416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2daa5fc01c4917b7d04ae05018cc91d5b73b43c628028ce489eb6e1b59e2415`  
		Last Modified: Wed, 15 Jan 2020 14:17:08 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91594379dcd19aa8896900708133e96d09286f185753d4f84e9e4b075f1077fb`  
		Last Modified: Wed, 15 Jan 2020 14:17:10 GMT  
		Size: 5.3 MB (5343427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa9cc665ad6e8ad23acad1678d6c6698631ba9fa43d4ac285d4e2b8b6f7b4a9`  
		Last Modified: Fri, 14 Feb 2020 02:41:16 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff05706977ea3a9d8c9dd77e821aa70e6b48d570220774a41dd3bb745115de39`  
		Last Modified: Fri, 14 Feb 2020 02:43:20 GMT  
		Size: 139.4 MB (139433630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30b1ee290fc25520988785de3972ebf5c9a00a19ca1795d7989f7ba583e01f9b`  
		Last Modified: Fri, 14 Feb 2020 02:41:17 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:latest` - windows version 10.0.17763.973; amd64

```console
$ docker pull golang@sha256:f05f285f5ff551bfc36f049591acfdbee5fe7fdcb80a3847db808a75919928a8
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2377238008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80cce7e7c5c091762aa6231cda32d1f2dd8c6a5acd684a23270387bdbaea71a6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 11 Jan 2020 05:23:25 GMT
RUN Install update 1809-amd64
# Tue, 14 Jan 2020 23:46:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jan 2020 13:22:49 GMT
ENV GIT_VERSION=2.23.0
# Wed, 15 Jan 2020 13:22:50 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 15 Jan 2020 13:22:52 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 15 Jan 2020 13:22:53 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 15 Jan 2020 13:23:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 15 Jan 2020 13:23:58 GMT
ENV GOPATH=C:\gopath
# Wed, 15 Jan 2020 13:24:21 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 14 Feb 2020 01:24:50 GMT
ENV GOLANG_VERSION=1.13.8
# Fri, 14 Feb 2020 01:32:06 GMT
RUN $url = ('https://golang.org/dl/go{0}.windows-amd64.zip' -f $env:GOLANG_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'aaf0888907144ca7070c8dad03fcf1308f77a42d2f6e4d2a609e64e9ae73cf4f'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Fri, 14 Feb 2020 01:32:08 GMT
WORKDIR C:\gopath
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:edbd72df76b46e904108d2f61a63c295b3e3d8092dbd5a03bbeb2fb4d34a3e55`  
		Size: 682.7 MB (682725872 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e9d323e253cb21832421dda4ec57dbd597bd4f934e62c162b9dec8b96e06e818`  
		Last Modified: Wed, 15 Jan 2020 01:45:20 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c34cd616875c2f9d033967e4516512eeda759d5d727381f68534f20a423fbc5`  
		Last Modified: Wed, 15 Jan 2020 14:19:45 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39f8f6402962aaf689f18fb7dc48707abd1442236650fa93feafdb8a0e62b884`  
		Last Modified: Wed, 15 Jan 2020 14:19:45 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2ccd2aa22967996e2db31a32fa197fe049385493a27f6cac5d28e147dc77a1`  
		Last Modified: Wed, 15 Jan 2020 14:19:42 GMT  
		Size: 1.2 KB (1204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b4005eb5a3fe7e59daa2cf4c83ef39ebc3b67aa33c077f34727270a45d08386`  
		Last Modified: Wed, 15 Jan 2020 14:19:41 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:123a2902604294d730658cf5b5098adc030395e96b276912489cd129282805d1`  
		Last Modified: Wed, 15 Jan 2020 14:19:55 GMT  
		Size: 29.6 MB (29634086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4b4abbf4635cc281d4995cae6e8ea73c4f2713f902bf6d5e500134413fc88da`  
		Last Modified: Wed, 15 Jan 2020 14:19:38 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57dc6850cb4055c8c383de6b662f37153a7fd9372a26c59bdd06bfb84f8220e3`  
		Last Modified: Wed, 15 Jan 2020 14:19:39 GMT  
		Size: 292.9 KB (292910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aea2b25ba84037b46e0c7efc812dec1c9c49785a7620eb16ab533970fd481e18`  
		Last Modified: Fri, 14 Feb 2020 02:44:08 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25877eac2722fb8cd2c329fbdfe3c3ef011132d1f020d6806c124249da6bba09`  
		Last Modified: Fri, 14 Feb 2020 02:46:06 GMT  
		Size: 129.9 MB (129890152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13b77e850ef1a28a28a18985ca45fa8ea900a60da55fa3ef29cebfe0bf08aadf`  
		Last Modified: Fri, 14 Feb 2020 02:44:08 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
