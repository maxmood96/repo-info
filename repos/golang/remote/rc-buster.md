## `golang:rc-buster`

```console
$ docker pull golang@sha256:f21051c52a0270568478946ccbe41ef6c98f0e4856ac49467ee6e3b19f4e307b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `golang:rc-buster` - linux; amd64

```console
$ docker pull golang@sha256:5e49e07fa5980b5ac708fc15bf3794deaa040c654d0dea641630e5a27a7ef192
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.1 MB (313107751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76123f92187f518039fe044ef11605eacf59fe83f71e3f61fffb9d4218499f0a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:20:39 GMT
ADD file:1ab357efe422cfed5e37af2dc60d07ccfd4bdee4d4a0c00838b5d68f19ff20c7 in / 
# Tue, 09 Jun 2020 01:20:39 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 01:46:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 01:46:41 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Jun 2020 01:47:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 21:13:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 00:29:05 GMT
ENV GOLANG_VERSION=1.15beta1
# Fri, 12 Jun 2020 00:29:19 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='11814b7475680a09720f3de32c66bca135289c8d528b2e1132b0ce56b3d9d6d7' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='d4da5c06097be8d14aeeb45bf8440a05c82e93e6de26063a147a31ed1d901ebc' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='2648b7d08fe74d0486ec82b3b539d15f3dd63bb34d79e7e57bebc3e5d06b5a38' ;; 		i386) goRelArch='linux-386'; goRelSha256='83d732a3961006e058f44c9672fde93dbea3d1c3d69e8807d135eeaf21fb80c8' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='33f7bed5ee9d4a0343dc90a5aa4ec7a1db755d0749b624618c15178fd8df4420' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='493b4449e68d0deba559e3f23f611310467e4c70d30b3605ff06852f14477457' ;; 		*) goRelArch='src'; goRelSha256='78cda84d4217ae0fdb8f87848474be28644bdc1aa16579055f852999a4793ac0'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url"; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		echo >&2; 		echo >&2 'error: UNIMPLEMENTED'; 		echo >&2 'TODO install golang-any from jessie-backports for GOROOT_BOOTSTRAP (and uninstall after build)'; 		echo >&2; 		exit 1; 	fi; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Fri, 12 Jun 2020 00:29:20 GMT
ENV GOPATH=/go
# Fri, 12 Jun 2020 00:29:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jun 2020 00:29:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 12 Jun 2020 00:29:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e9afc4f90ab09248d75c8081b6dfba749a7f7efdac704ced7e0ceb506e02fa4a`  
		Last Modified: Tue, 09 Jun 2020 01:25:37 GMT  
		Size: 50.4 MB (50389504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989e6b19a265d6b8b7934e7ddd7dc07f6e2fc945b3a28dda9b8aecb12cdb30e0`  
		Last Modified: Tue, 09 Jun 2020 01:59:52 GMT  
		Size: 7.8 MB (7811709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af14b6c2f8785723bceb5964c5dec1f0489b7750e9d4ec671e49bfba15d80a39`  
		Last Modified: Tue, 09 Jun 2020 01:59:52 GMT  
		Size: 10.0 MB (9996168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5573c4b3094956931fd68c310ae92c9eb1a787f0c77ac2730be9d16cce172d5e`  
		Last Modified: Tue, 09 Jun 2020 02:00:08 GMT  
		Size: 51.8 MB (51827493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4020e2aa747ca4d0ca2e87305f22f089fd57a696fd19bfa30182316d51b089a`  
		Last Modified: Tue, 09 Jun 2020 21:15:44 GMT  
		Size: 68.7 MB (68650396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d64d725e562efb8254123bc8836b3a0caa46ea40f118bc58f7a59693f8de0cd2`  
		Last Modified: Fri, 12 Jun 2020 00:33:52 GMT  
		Size: 124.4 MB (124432355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140e69854a7419389e60e3a8f42e4dc674617095a37d7ac833e76c49e01e609c`  
		Last Modified: Fri, 12 Jun 2020 00:33:21 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:rc-buster` - linux; arm variant v7

```console
$ docker pull golang@sha256:fedc38a6a2f72254a3fd0e9ad55f4c54f78e0f69b54414f6512cf909b6a88e21
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.3 MB (264276609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cbfc9fa38b3e0d39a13bc9651ecc0554903c644a7392233173a29be476f6a2a`
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
# Thu, 06 Feb 2020 01:22:46 GMT
ENV GOLANG_VERSION=1.14rc1
# Thu, 06 Feb 2020 01:23:44 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='69398d41e5f6b87cdf3969aae665be4dfd3cc2ef36a61ab47a261f96130ed788' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='bfe041f7d2a62f895f2d11703a29bdd31a48cca9a3c36418d59680bc1cbb8a6d' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='a5509448b06f02f5198fe8bbf5af88ab483af9c46f231c3f308748016fbc32c9' ;; 		i386) goRelArch='linux-386'; goRelSha256='831087aa0eba8b6dfa221036d00641613996ac66d7c635f1e34c53d5f0922623' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='fe1bf34d2b117d785f2fb33151c44ca8bc2188678c9e903fa0ad30573547b412' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='2302fa0e30144a969cb1879eed8aeb9a82c2b520fcda8aebbb20a539ad427c25' ;; 		*) goRelArch='src'; goRelSha256='76188ea84e95baa502d058c9598020c7654d6adaf40b82cabcf57c68df19963a'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url"; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		echo >&2; 		echo >&2 'error: UNIMPLEMENTED'; 		echo >&2 'TODO install golang-any from jessie-backports for GOROOT_BOOTSTRAP (and uninstall after build)'; 		echo >&2; 		exit 1; 	fi; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Thu, 06 Feb 2020 01:23:48 GMT
ENV GOPATH=/go
# Thu, 06 Feb 2020 01:23:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Feb 2020 01:23:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 06 Feb 2020 01:23:54 GMT
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
	-	`sha256:484bc6c7846d4e8a4f750cb73fc9cc4e086cc81a2d67f5a9929f969e54939413`  
		Last Modified: Thu, 06 Feb 2020 01:30:47 GMT  
		Size: 101.7 MB (101664762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb18321ce4e5e0c8d5b563982e189855c1f5d5431566cfc5dc2d159f8b3b628`  
		Last Modified: Thu, 06 Feb 2020 01:29:49 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:rc-buster` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:4c698ad68998a3a6f9fabdb9bb91354e8304990f75786db3212b3859a0d9d01d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.3 MB (282251561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2c5602da4b0978a97726fb0bc39626a6e6e8d81e322ed593f2468e0ece32760`
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
# Thu, 06 Feb 2020 01:40:08 GMT
ENV GOLANG_VERSION=1.14rc1
# Thu, 06 Feb 2020 01:40:37 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='69398d41e5f6b87cdf3969aae665be4dfd3cc2ef36a61ab47a261f96130ed788' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='bfe041f7d2a62f895f2d11703a29bdd31a48cca9a3c36418d59680bc1cbb8a6d' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='a5509448b06f02f5198fe8bbf5af88ab483af9c46f231c3f308748016fbc32c9' ;; 		i386) goRelArch='linux-386'; goRelSha256='831087aa0eba8b6dfa221036d00641613996ac66d7c635f1e34c53d5f0922623' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='fe1bf34d2b117d785f2fb33151c44ca8bc2188678c9e903fa0ad30573547b412' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='2302fa0e30144a969cb1879eed8aeb9a82c2b520fcda8aebbb20a539ad427c25' ;; 		*) goRelArch='src'; goRelSha256='76188ea84e95baa502d058c9598020c7654d6adaf40b82cabcf57c68df19963a'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url"; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		echo >&2; 		echo >&2 'error: UNIMPLEMENTED'; 		echo >&2 'TODO install golang-any from jessie-backports for GOROOT_BOOTSTRAP (and uninstall after build)'; 		echo >&2; 		exit 1; 	fi; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Thu, 06 Feb 2020 01:40:41 GMT
ENV GOPATH=/go
# Thu, 06 Feb 2020 01:40:44 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Feb 2020 01:40:50 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 06 Feb 2020 01:40:54 GMT
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
	-	`sha256:f930dfbaa1cf7b2092ecaeb4f4b4cc640e3667a209d0c48efed84fea4b4147ae`  
		Last Modified: Thu, 06 Feb 2020 01:45:38 GMT  
		Size: 100.9 MB (100921394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a2462e9ebdbcec6bb610cbb0178b28ccdb578548a4d35b05ad8e41f9eb8c58d`  
		Last Modified: Thu, 06 Feb 2020 01:41:06 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:rc-buster` - linux; 386

```console
$ docker pull golang@sha256:303a21bf91fdfc0ade6f5f05d5cf9ce60e61b6c0e7050064902bd8465c20115f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.3 MB (300274845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8731d52dafb9f1ae2d119cfb7ee57928e673c657d775213399f31d7db5ed34a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:39:33 GMT
ADD file:f95fda6e1e7823d93ca50dd67a1ab99bdc8a7dea372ef27426915702500d54a2 in / 
# Tue, 09 Jun 2020 01:39:33 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 02:11:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 02:11:46 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Jun 2020 02:12:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 19:49:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 01:45:58 GMT
ENV GOLANG_VERSION=1.15beta1
# Fri, 12 Jun 2020 01:46:16 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='11814b7475680a09720f3de32c66bca135289c8d528b2e1132b0ce56b3d9d6d7' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='d4da5c06097be8d14aeeb45bf8440a05c82e93e6de26063a147a31ed1d901ebc' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='2648b7d08fe74d0486ec82b3b539d15f3dd63bb34d79e7e57bebc3e5d06b5a38' ;; 		i386) goRelArch='linux-386'; goRelSha256='83d732a3961006e058f44c9672fde93dbea3d1c3d69e8807d135eeaf21fb80c8' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='33f7bed5ee9d4a0343dc90a5aa4ec7a1db755d0749b624618c15178fd8df4420' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='493b4449e68d0deba559e3f23f611310467e4c70d30b3605ff06852f14477457' ;; 		*) goRelArch='src'; goRelSha256='78cda84d4217ae0fdb8f87848474be28644bdc1aa16579055f852999a4793ac0'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url"; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		echo >&2; 		echo >&2 'error: UNIMPLEMENTED'; 		echo >&2 'TODO install golang-any from jessie-backports for GOROOT_BOOTSTRAP (and uninstall after build)'; 		echo >&2; 		exit 1; 	fi; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Fri, 12 Jun 2020 01:46:16 GMT
ENV GOPATH=/go
# Fri, 12 Jun 2020 01:46:17 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jun 2020 01:46:18 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 12 Jun 2020 01:46:18 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:ca172633df711443e1bcc46650b24074efa097045feee542ecbb4934ae3ae01b`  
		Last Modified: Tue, 09 Jun 2020 01:44:44 GMT  
		Size: 51.2 MB (51156157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91e4e2e742db8627ba5d7e0f076114e90c4fea4407cedd3599355e4c00828543`  
		Last Modified: Tue, 09 Jun 2020 02:32:03 GMT  
		Size: 8.0 MB (7981054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60ba43d083b56bb094a5bac45d723e9bec0fe65d033950b3c4dc392e890c7e41`  
		Last Modified: Tue, 09 Jun 2020 02:32:03 GMT  
		Size: 10.3 MB (10338453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac2391b0310a0be022e7ac6e202273ea7cc0ac5f16e862e5cb19c43c5db30b5b`  
		Last Modified: Tue, 09 Jun 2020 02:32:24 GMT  
		Size: 53.4 MB (53429728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6418909c851cb25d795df9db25552f37bd19b4f855e3f4390ac56df413186b7`  
		Last Modified: Tue, 09 Jun 2020 19:53:02 GMT  
		Size: 73.5 MB (73511520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:597607468db32db791abdfc3fc64217fdd350620168ef927a024ba22308c79d4`  
		Last Modified: Fri, 12 Jun 2020 01:50:53 GMT  
		Size: 103.9 MB (103857807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26cc78470afd717277aaffdc20ab60d094bcd8e2fd5a69dcd1c162377a74c6ff`  
		Last Modified: Fri, 12 Jun 2020 01:50:25 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:rc-buster` - linux; ppc64le

```console
$ docker pull golang@sha256:0bcfa39885d1de46d16d7e304d403c54a16595be6b57bed876a2f324322aa1ce
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.7 MB (303687751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7786772ab83dbd222dc8dfd077e473bb073d34e818787044ae41f453ef9ec6fe`
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
# Thu, 06 Feb 2020 00:37:52 GMT
ENV GOLANG_VERSION=1.14rc1
# Thu, 06 Feb 2020 00:38:24 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='69398d41e5f6b87cdf3969aae665be4dfd3cc2ef36a61ab47a261f96130ed788' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='bfe041f7d2a62f895f2d11703a29bdd31a48cca9a3c36418d59680bc1cbb8a6d' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='a5509448b06f02f5198fe8bbf5af88ab483af9c46f231c3f308748016fbc32c9' ;; 		i386) goRelArch='linux-386'; goRelSha256='831087aa0eba8b6dfa221036d00641613996ac66d7c635f1e34c53d5f0922623' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='fe1bf34d2b117d785f2fb33151c44ca8bc2188678c9e903fa0ad30573547b412' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='2302fa0e30144a969cb1879eed8aeb9a82c2b520fcda8aebbb20a539ad427c25' ;; 		*) goRelArch='src'; goRelSha256='76188ea84e95baa502d058c9598020c7654d6adaf40b82cabcf57c68df19963a'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url"; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		echo >&2; 		echo >&2 'error: UNIMPLEMENTED'; 		echo >&2 'TODO install golang-any from jessie-backports for GOROOT_BOOTSTRAP (and uninstall after build)'; 		echo >&2; 		exit 1; 	fi; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Thu, 06 Feb 2020 00:38:30 GMT
ENV GOPATH=/go
# Thu, 06 Feb 2020 00:38:33 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Feb 2020 00:38:42 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 06 Feb 2020 00:38:47 GMT
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
	-	`sha256:5af256a452250034bf0eed2b60c2c7eb23187e682dff40e21bc15c4fcaf97a0b`  
		Last Modified: Thu, 06 Feb 2020 00:43:45 GMT  
		Size: 99.8 MB (99755889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71cb146d553e59584fe48ad92219660bfce39b8d8bd909ce3f4ee5fc77d71a19`  
		Last Modified: Thu, 06 Feb 2020 00:42:32 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:rc-buster` - linux; s390x

```console
$ docker pull golang@sha256:e86db1228d835597e570c30d366161a26a7f8c697704ba23e12565c67528867d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.8 MB (278778052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7d9e0493f2a7ff3d0a92fa7df9d6995e78fd9a07219ae50447de857ef616e85`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:42:21 GMT
ADD file:525b5566f1fb9dfef74a4f49170a50bba0f0ed22a8bd627a8f802803236f1db8 in / 
# Tue, 09 Jun 2020 01:42:23 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 02:09:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 02:09:41 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Jun 2020 02:10:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 11:56:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Thu, 11 Jun 2020 22:55:05 GMT
ENV GOLANG_VERSION=1.15beta1
# Thu, 11 Jun 2020 22:55:17 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='11814b7475680a09720f3de32c66bca135289c8d528b2e1132b0ce56b3d9d6d7' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='d4da5c06097be8d14aeeb45bf8440a05c82e93e6de26063a147a31ed1d901ebc' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='2648b7d08fe74d0486ec82b3b539d15f3dd63bb34d79e7e57bebc3e5d06b5a38' ;; 		i386) goRelArch='linux-386'; goRelSha256='83d732a3961006e058f44c9672fde93dbea3d1c3d69e8807d135eeaf21fb80c8' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='33f7bed5ee9d4a0343dc90a5aa4ec7a1db755d0749b624618c15178fd8df4420' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='493b4449e68d0deba559e3f23f611310467e4c70d30b3605ff06852f14477457' ;; 		*) goRelArch='src'; goRelSha256='78cda84d4217ae0fdb8f87848474be28644bdc1aa16579055f852999a4793ac0'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url"; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		echo >&2; 		echo >&2 'error: UNIMPLEMENTED'; 		echo >&2 'TODO install golang-any from jessie-backports for GOROOT_BOOTSTRAP (and uninstall after build)'; 		echo >&2; 		exit 1; 	fi; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Thu, 11 Jun 2020 22:55:21 GMT
ENV GOPATH=/go
# Thu, 11 Jun 2020 22:55:22 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2020 22:55:22 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 11 Jun 2020 22:55:22 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:76dae9e9a8f2b69403c29a068363410a0b491d889452a410e1a846db24918418`  
		Last Modified: Tue, 09 Jun 2020 01:46:14 GMT  
		Size: 49.0 MB (48965925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ea4ddfd9cac861440dd774171c0df5d003bcf031cc856603f0dcc1a569a7614`  
		Last Modified: Tue, 09 Jun 2020 02:18:01 GMT  
		Size: 7.4 MB (7385198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b4340e9fce6caba0ffebdee007c25f4ed849de61e56dcee1ed7e081edbcf1e5`  
		Last Modified: Tue, 09 Jun 2020 02:18:06 GMT  
		Size: 9.9 MB (9882055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89446217dee5ed85681993c919acbdf28494151380677fdefa88b6b5e481573c`  
		Last Modified: Tue, 09 Jun 2020 02:18:19 GMT  
		Size: 51.4 MB (51366573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17d6d711085f1e16cb55dd6d39b0fa3cfe5a898d10c02f3fbb3a0c22180f588c`  
		Last Modified: Tue, 09 Jun 2020 12:02:26 GMT  
		Size: 56.7 MB (56714696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d9cc6d921b68bdf61fecdfdc8c210b6335fff14f5ee6ef71f0fc9184682d48d`  
		Last Modified: Thu, 11 Jun 2020 22:58:26 GMT  
		Size: 104.5 MB (104463449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2887361c17d23bd7167e07dd3f80082dd58f804f37949ebdf3f040534bafc1c1`  
		Last Modified: Thu, 11 Jun 2020 22:58:26 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
