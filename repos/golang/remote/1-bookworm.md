## `golang:1-bookworm`

```console
$ docker pull golang@sha256:8e4358fd54fe1c833af23b9a0b84eb5d41fc3dc67d23fde72cf3de5f6319b445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `golang:1-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:cac8fb1c85bf96316112f5dd2671c8da0c19d2dfce88af9551b3141499a59eaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.5 MB (299456709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77d6b4d7037e96d9ede7d94012f81ce9809dab27da16cebebc6672fd64f872f4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:34 GMT
ADD file:ca6d1f0f80dd6c91b8ba1d1adf77d7af6d0e5f2f493a2858e384c11874314395 in / 
# Wed, 10 Apr 2024 01:50:35 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 05:24:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:25:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 Apr 2024 16:03:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Apr 2024 16:03:48 GMT
ENV GOLANG_VERSION=1.22.2
# Wed, 03 Apr 2024 16:03:48 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Apr 2024 16:03:48 GMT
ENV GOPATH=/go
# Wed, 03 Apr 2024 16:03:48 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Apr 2024 16:03:48 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 03 Apr 2024 16:03:48 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Apr 2024 16:03:48 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:609c73876867487da051ad470002217da69bb052e2538710ade0730d893ff51f`  
		Last Modified: Wed, 10 Apr 2024 01:55:11 GMT  
		Size: 49.6 MB (49560360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7247ea8d81e671d079d67f3a9909315ef4641b45db90d62a1b18e3430c1937d4`  
		Last Modified: Wed, 10 Apr 2024 05:34:49 GMT  
		Size: 24.0 MB (24046793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be374d06f38273b62ddd7aa5bc3ce3f9c781fd49a1f5a5dd94a46d2986920d7a`  
		Last Modified: Wed, 10 Apr 2024 05:35:08 GMT  
		Size: 64.1 MB (64140565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e9047ca48689f6ef72c1a9fdf6f8c2b40e182222e7671fffa5d9d4952f75942`  
		Last Modified: Wed, 10 Apr 2024 17:14:22 GMT  
		Size: 92.4 MB (92374682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db43cacb95776c88f59c8b9c85e070a8fcaee5f7c46ef79b86b83958743a9f8e`  
		Last Modified: Wed, 10 Apr 2024 17:14:21 GMT  
		Size: 69.3 MB (69334102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e697ccba1347c99d13341011dabef5bc1162e52473acc09ce6e3248032b29e45`  
		Last Modified: Wed, 10 Apr 2024 17:14:09 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:997c3175e36dfc8561fd3675e375177d7aa8802d7dff73ad00622aab3ca13c3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.3 MB (260270499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e656d8709586ccea17fcc91d8984f02bb0b40fb87c0895a319deaa35d9f3d150`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:57:54 GMT
ADD file:30e85746fe77290a5de7286ebb7e2484b39554122eadc92de3df4ef4d95de9ff in / 
# Wed, 10 Apr 2024 00:57:55 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:42:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:43:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 Apr 2024 16:03:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Apr 2024 16:03:48 GMT
ENV GOLANG_VERSION=1.22.2
# Wed, 03 Apr 2024 16:03:48 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Apr 2024 16:03:48 GMT
ENV GOPATH=/go
# Wed, 03 Apr 2024 16:03:48 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Apr 2024 16:03:48 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 03 Apr 2024 16:03:48 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Apr 2024 16:03:48 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:debd7c42d7ee74277f743dba14187c21ed8be6cf4f57abbaeb7b88c779282f09`  
		Last Modified: Wed, 10 Apr 2024 01:03:59 GMT  
		Size: 45.2 MB (45158610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1564e42498f84ce1d5bb6808049f9c674335b23f95ba63cf15c09549e3990e59`  
		Last Modified: Wed, 10 Apr 2024 06:59:53 GMT  
		Size: 22.0 MB (21950348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea816b946832e576a6e2cfe5a7a28caeea429092724dc7daabb1e183ddd4817a`  
		Last Modified: Wed, 10 Apr 2024 07:00:21 GMT  
		Size: 59.2 MB (59213244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c1e020cf94cb4c7b32a9497074cc649337ef61681c907724722a0a993620194`  
		Last Modified: Wed, 10 Apr 2024 21:13:00 GMT  
		Size: 66.2 MB (66233705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62501d4567d3be645fae3f6a092380f0f72e88137839df0ea2613058c11605c8`  
		Last Modified: Wed, 10 Apr 2024 21:13:04 GMT  
		Size: 67.7 MB (67714387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bc62f2c7e243a0122c4c5b393ba838d473c5e3b6033ea65435972cd64ab100b`  
		Last Modified: Wed, 10 Apr 2024 21:12:43 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:85e4d8edfff508cc62dc53196303e2ad5e2f28d51b9a5d7691e4362837704734
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.8 MB (289848927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:824aa3c1d42cdad43ab6513830466315ccf281e8e1ca3f7a4af1c38585712734`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:12 GMT
ADD file:d795219dc83a41b5bb4106e62eebd31ceef0aae1b81541156eae5fe98e89337c in / 
# Wed, 10 Apr 2024 00:40:13 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:22:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 04:22:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 Apr 2024 16:03:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Apr 2024 16:03:48 GMT
ENV GOLANG_VERSION=1.22.2
# Wed, 03 Apr 2024 16:03:48 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Apr 2024 16:03:48 GMT
ENV GOPATH=/go
# Wed, 03 Apr 2024 16:03:48 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Apr 2024 16:03:48 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 03 Apr 2024 16:03:48 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Apr 2024 16:03:48 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1e92f3a395ff98a929e797a3c392bb6d0f05531068d34b81d3cd41ed6ce82ca4`  
		Last Modified: Wed, 10 Apr 2024 00:43:42 GMT  
		Size: 49.6 MB (49596265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:374850c6db1702573c7004d630027931be318b2d71cb28e890e2fcd0f0730712`  
		Last Modified: Wed, 10 Apr 2024 04:31:58 GMT  
		Size: 23.6 MB (23582868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:421c44fab18bc9f4c62ca481e074d50b3a036e7c95c7607b6d036c34d67c5264`  
		Last Modified: Wed, 10 Apr 2024 04:32:17 GMT  
		Size: 64.0 MB (63990996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cbe4bb4a0d8b43491c9cd09a1939fa98f6e0c6bb41b83b515758995342fc910`  
		Last Modified: Wed, 10 Apr 2024 13:33:59 GMT  
		Size: 86.4 MB (86408724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7b295dfee595cac7b77431a3c81dba172a0582f59e4603fcfaf178f88ac260`  
		Last Modified: Wed, 10 Apr 2024 13:33:59 GMT  
		Size: 66.3 MB (66269867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7318f984ad5d530058907ecd2f58af8f0b40ab4d227184a84491c13581155285`  
		Last Modified: Wed, 10 Apr 2024 13:33:50 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bookworm` - linux; 386

```console
$ docker pull golang@sha256:ca15446af8df325b01f516372d93bd7373eca19b3b82c80cb4a67b13ea9614d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.6 MB (298572496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4de53f0a58520718cd8cbcf8812457fcd4065964c4bedc84029f10e14b96e7f1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:56:58 GMT
ADD file:790f7a239f36cc7d8fd7fba66cd64aaff5f743c1c06e080820f865bae8f4a8c1 in / 
# Wed, 10 Apr 2024 00:56:59 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:52:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 07:53:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 Apr 2024 16:03:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Apr 2024 16:03:48 GMT
ENV GOLANG_VERSION=1.22.2
# Wed, 03 Apr 2024 16:03:48 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Apr 2024 16:03:48 GMT
ENV GOPATH=/go
# Wed, 03 Apr 2024 16:03:48 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Apr 2024 16:03:48 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 03 Apr 2024 16:03:48 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Apr 2024 16:03:48 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:417ba0ba1bcbb46434cbd64273ffc8edbe2c1921e58094e580e87c3b8e518701`  
		Last Modified: Wed, 10 Apr 2024 01:01:38 GMT  
		Size: 50.6 MB (50587234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3845b288d815c745f12b9d8f5713e916e9d585644e3574c14b698e39da51082a`  
		Last Modified: Wed, 10 Apr 2024 08:05:45 GMT  
		Size: 24.9 MB (24884730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0e5c516778392288fdc27cfc451916d0d1153e04fbb6687af2b9622dea744f5`  
		Last Modified: Wed, 10 Apr 2024 08:06:09 GMT  
		Size: 66.0 MB (65987074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e208b658b892b266e333d74ef17af5de71d6b81f873540ee16365b51bb30bbf3`  
		Last Modified: Wed, 10 Apr 2024 19:49:50 GMT  
		Size: 89.8 MB (89769228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e54c89b479d544755ab2f0a35b8a9ca5fceb27116f7bd12f9982c741169978b4`  
		Last Modified: Wed, 10 Apr 2024 19:49:48 GMT  
		Size: 67.3 MB (67344024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e00bf7d5c232e828a0bd5571a8105201b1e3cbdf7388c484d7eca85506b99de`  
		Last Modified: Wed, 10 Apr 2024 19:49:28 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:658fc239e9eec839fa1b5ef05c646337822501c641343dcb31ced0fbef0382d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.0 MB (270002546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:166b1f7d636022915f104858f7501423fe1a7b8a7eaa70811d4e3739bf2e4e1a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:05:38 GMT
ADD file:4d32a17a925fe03541568abf911d846953d3660b326987a74427b0262134b3c6 in / 
# Tue, 12 Mar 2024 01:05:41 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:05:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:06:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 Apr 2024 16:03:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Apr 2024 16:03:48 GMT
ENV GOLANG_VERSION=1.22.2
# Wed, 03 Apr 2024 16:03:48 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Apr 2024 16:03:48 GMT
ENV GOPATH=/go
# Wed, 03 Apr 2024 16:03:48 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Apr 2024 16:03:48 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 03 Apr 2024 16:03:48 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Apr 2024 16:03:48 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a1888556fef8803d385bcda912bec552fdbf67dbab0adac6cadf266d746cca55`  
		Last Modified: Tue, 12 Mar 2024 01:16:25 GMT  
		Size: 49.6 MB (49563114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f64944212b4456db3039905773dd6dea4c4590560c38ae7716d5dfa12559e8`  
		Last Modified: Tue, 12 Mar 2024 02:41:43 GMT  
		Size: 23.6 MB (23630647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638fdd2230a0e3b195fa0e78e24eb4739e6c5ad8a94c3bb93aedbaf4fad008ca`  
		Last Modified: Tue, 12 Mar 2024 02:42:36 GMT  
		Size: 63.0 MB (62965889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:365bc8351f6d18343711b7f0dbd1f883316f793a25f384be825519cefa76848e`  
		Last Modified: Tue, 12 Mar 2024 19:46:20 GMT  
		Size: 69.7 MB (69732738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d257ced73e7c6a3822c88aa6ee95d640c9c76b0bebd8965fb63bdca6aacbb59`  
		Last Modified: Wed, 03 Apr 2024 17:04:10 GMT  
		Size: 64.1 MB (64110000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf50e09713fbec9736e987f41a4458de0a72d4d0793cc9f2c380e6f68daeb4da`  
		Last Modified: Wed, 03 Apr 2024 17:03:18 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:5b78ae35b0f692718a78984d02c6d74b96c8827e7b26ffaf8c05d42de8bf479d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.6 MB (305627217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ba00df7aa3afb837796e1e20b8268b17d5a55eb0cc6108838a240c8daa34d98`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:26:15 GMT
ADD file:12519205a7ecc1a9b92b9b26c967bf9f7204f2e0b9c81cb9a147b10a29b0715c in / 
# Wed, 10 Apr 2024 01:26:17 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:28:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:29:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 Apr 2024 16:03:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Apr 2024 16:03:48 GMT
ENV GOLANG_VERSION=1.22.2
# Wed, 03 Apr 2024 16:03:48 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Apr 2024 16:03:48 GMT
ENV GOPATH=/go
# Wed, 03 Apr 2024 16:03:48 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Apr 2024 16:03:48 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 03 Apr 2024 16:03:48 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Apr 2024 16:03:48 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e6dcf23c0df5604eb9aa3050ab9c36d44dec4ab1448d2c229f4beaaf0f7fa503`  
		Last Modified: Wed, 10 Apr 2024 01:30:37 GMT  
		Size: 53.6 MB (53562477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e9a49dc2918c681cd1306002e0306d198b0ab9f74366235b251cb85c930eaaa`  
		Last Modified: Wed, 10 Apr 2024 07:16:20 GMT  
		Size: 25.7 MB (25696598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7558a95a0d29869e7f316194c1d23abcbbe4d8c3340f4d3103f670b9d4af3eef`  
		Last Modified: Wed, 10 Apr 2024 07:16:43 GMT  
		Size: 69.6 MB (69581154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d93f34748ff9beb28aaa2f23769cac11f7c2b258a4f287dbccbf5fc63b82d254`  
		Last Modified: Wed, 10 Apr 2024 16:18:33 GMT  
		Size: 90.4 MB (90359602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87d25f5782daac1ede046d4da5bff986d3ca5a32569f22c33c99d076e8d22732`  
		Last Modified: Wed, 10 Apr 2024 16:18:30 GMT  
		Size: 66.4 MB (66427180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e85fc22183644524b7e8a74e4138ccce53080379f6cad45c2840574d99b8069`  
		Last Modified: Wed, 10 Apr 2024 16:18:17 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:6b764de685b47c766e13da6a518156a4552e97c5133610871d9520ec94342217
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.4 MB (272427175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23cd16b0c49071c390d2fde72ead4ca2e27df7ace24d015b10c0917810998ed3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:11:40 GMT
ADD file:4b6b256d3328c1d19403b3eb0f375b5d33724b65f790edd27be4adca49c66e4b in / 
# Wed, 10 Apr 2024 01:11:45 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:50:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:51:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 Apr 2024 16:03:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Apr 2024 16:03:48 GMT
ENV GOLANG_VERSION=1.22.2
# Wed, 03 Apr 2024 16:03:48 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Apr 2024 16:03:48 GMT
ENV GOPATH=/go
# Wed, 03 Apr 2024 16:03:48 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Apr 2024 16:03:48 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 03 Apr 2024 16:03:48 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Apr 2024 16:03:48 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:17f5c0a7be3d447b0aca6569b534fabcb69c578072a0cdb81f078fd4872eba70`  
		Last Modified: Wed, 10 Apr 2024 01:48:11 GMT  
		Size: 47.9 MB (47922706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5a94fdcea32a650c77c01028838d670a5840f3ead5a1cf5526e922967f0df66`  
		Last Modified: Wed, 10 Apr 2024 07:30:52 GMT  
		Size: 24.0 MB (24043531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdaec0019454e24574ad418259f50f0d68508dcf92f31f05ca5d5ad33dcf43bb`  
		Last Modified: Wed, 10 Apr 2024 07:31:10 GMT  
		Size: 63.1 MB (63126889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c4dd9e04043c29cfd50046be55940ad30208cb9a11825d423bfe2259c7d1d7`  
		Last Modified: Wed, 10 Apr 2024 22:17:12 GMT  
		Size: 68.9 MB (68942212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb20841c255e3c90a0a0b8d74dc9e364ee9e9a4bceae619cc38aa7a00995f51`  
		Last Modified: Wed, 10 Apr 2024 22:17:13 GMT  
		Size: 68.4 MB (68391631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e26407130bad8dbcd5f7e871ae63bd230829da363eaa844729c0d262c78bfca1`  
		Last Modified: Wed, 10 Apr 2024 22:17:02 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
