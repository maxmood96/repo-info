## `golang:bookworm`

```console
$ docker pull golang@sha256:cbd59ce363d162d31192b1bcf928773b6f8490ffd529c51594fc4d4ba755b8a5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `golang:bookworm` - linux; amd64

```console
$ docker pull golang@sha256:cfacfe031d4eb1c1ad50593e4988cc9e8286ff1ca5f33bf357eb863fddc08073
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.5 MB (289468544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69e245162a1e8c394cb350e743daa23f3d4ef7e0391c75c49e195c84b98f77d2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:06:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:05:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:47:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:46:16 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 09 Dec 2025 00:46:16 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Dec 2025 00:46:16 GMT
ENV GOPATH=/go
# Tue, 09 Dec 2025 00:46:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 00:46:16 GMT
COPY /target/ / # buildkit
# Tue, 09 Dec 2025 00:47:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 09 Dec 2025 00:47:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c8443a297fa42e27cb10653777dd5a53f82a65fbc8b2d33f82b8722199f941d3`  
		Last Modified: Mon, 08 Dec 2025 22:16:25 GMT  
		Size: 48.5 MB (48480736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae8659f7a8d357662281a0f87eb293725bb75ffa6c7356c38567f557d8a1f11`  
		Last Modified: Mon, 08 Dec 2025 23:07:04 GMT  
		Size: 24.0 MB (24029335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c237534654fe7a5c118fcee78652af952e57a4a07cc322c0ae3c367839bb0ccc`  
		Last Modified: Tue, 09 Dec 2025 00:06:16 GMT  
		Size: 64.4 MB (64396522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b18210496c0a859458bb2304c5fd1c1e099de8c927f7030f1bce471f5361bf`  
		Last Modified: Tue, 09 Dec 2025 00:47:59 GMT  
		Size: 92.4 MB (92410480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c445a0e108b509dd422d6adce512f16cb7edd37814e8e3509850820377bcf06`  
		Last Modified: Tue, 02 Dec 2025 17:47:39 GMT  
		Size: 60.2 MB (60151314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a1aed72b746091f7129c5e483dae161d20c9f3092262292f6f8993779531c60`  
		Last Modified: Tue, 09 Dec 2025 00:47:52 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:87ae66b51171764a067baf15ec4feed14b7a5528f022cdaa2953b7b44fd0da3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10523536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:687d4ea612b261ce91ae6c255a984ae80bf3a7b6e54c3dc0d3ea633d68c2b47f`

```dockerfile
```

-	Layers:
	-	`sha256:c22df4569f017be27de20cc98ee8a0fef93b6aaee4a7a13e012855f442da6e73`  
		Last Modified: Tue, 09 Dec 2025 03:23:30 GMT  
		Size: 10.5 MB (10495740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4ddf431b12e9e281ec2da71a87f2042b612219afc37536fec5293968ed2c83b`  
		Last Modified: Tue, 09 Dec 2025 03:23:31 GMT  
		Size: 27.8 KB (27796 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:feed67d4ba9f2fcd25ebdaa381fdc8c58780eecd4fdaaaeb64af29ffd2757027
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.1 MB (251132315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba7b1d0d2d5ca1ec17b63e533b640edc3f34e686c9d64b664daf9b47b3788193`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 00:04:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 01:32:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 02:19:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 02:21:08 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 09 Dec 2025 02:21:08 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Dec 2025 02:21:08 GMT
ENV GOPATH=/go
# Tue, 09 Dec 2025 02:21:08 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 02:21:08 GMT
COPY /target/ / # buildkit
# Tue, 09 Dec 2025 02:21:11 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 09 Dec 2025 02:21:11 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c3d6a83e736aa77820543663b2d6579ddd98b0f465c0fcad8aa9bd98a5b72a9c`  
		Last Modified: Mon, 08 Dec 2025 22:16:46 GMT  
		Size: 44.2 MB (44196066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0a258ea9a718fb1bf2331996816ba335715a3c786bd79934d265fd78fb7f5a`  
		Last Modified: Tue, 09 Dec 2025 00:05:11 GMT  
		Size: 21.9 MB (21934635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a66aa6761aa99c557c882b6cb71cf839a06b4634c5e4d98e4a93d946b4554c6f`  
		Last Modified: Tue, 09 Dec 2025 01:33:23 GMT  
		Size: 59.7 MB (59652900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31b2100a598a6722918036327d75f87ea8162bf1e1af86997e4216e2b079c3ee`  
		Last Modified: Tue, 09 Dec 2025 02:21:46 GMT  
		Size: 66.3 MB (66276494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952f3ceca6918c986252a293f498004b3365bf2efd3e1b6be9d754f9e7c62cfe`  
		Last Modified: Tue, 02 Dec 2025 17:49:21 GMT  
		Size: 59.1 MB (59072062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242e2232780635bce49a179f1a956009dff8455a67fdbdf5028fcf2c79ed9815`  
		Last Modified: Tue, 09 Dec 2025 02:21:40 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:7f8f662583fad372bb6cb99e36c4865639df0ed5e49934254237e002863a30c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10330357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e7c096f489a30b62760ce15cd3ef93b4adecca827bde029ec8ed56f5e30e1f9`

```dockerfile
```

-	Layers:
	-	`sha256:707ed9fb7333f5f6685e38c631fd841560a263c2bef19ff41e2678df25d6af7f`  
		Last Modified: Tue, 09 Dec 2025 03:23:40 GMT  
		Size: 10.3 MB (10302454 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65132210f1d9dbd440a15fe0804365e6af1f230ad2c547665c6a0c077b45ffd8`  
		Last Modified: Tue, 09 Dec 2025 03:23:41 GMT  
		Size: 27.9 KB (27903 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:38f61e632fb494c99162aff0a04ca364c471f66da84d1e588bfefb143f06b52c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.5 MB (280470881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a623116632f708a04a469b04d8f15684e890b5fbee8f31b1f2bd5be3b099b593`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:10:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:10:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 01:17:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 01:17:05 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 09 Dec 2025 01:17:05 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Dec 2025 01:17:05 GMT
ENV GOPATH=/go
# Tue, 09 Dec 2025 01:17:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 01:17:05 GMT
COPY /target/ / # buildkit
# Tue, 09 Dec 2025 01:17:09 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 09 Dec 2025 01:17:09 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7f2b9668af76f73927725e2d1fb5d7224604d8c4c42cb8cdecb502257d9101c4`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 48.4 MB (48359071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0da1fc24a51c3ab23b5143a2c67b43348114c11a8029b3483be57ab9fe54eb6`  
		Last Modified: Mon, 08 Dec 2025 23:10:26 GMT  
		Size: 23.6 MB (23598247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a266a3916e0f2e8ff6996b219222479419b3dca87b3e3dfc3bd0108f509071`  
		Last Modified: Tue, 09 Dec 2025 00:11:40 GMT  
		Size: 64.4 MB (64371489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1d7b2841bed83e94cfc06e675eae22d6e1ccaf8af5c3432f5a731b73586622`  
		Last Modified: Tue, 09 Dec 2025 01:17:47 GMT  
		Size: 86.5 MB (86490999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b0562e970c9af953828c5cdc69b3e362c523c3064c669aa8dda79020032e840`  
		Last Modified: Tue, 02 Dec 2025 17:48:05 GMT  
		Size: 57.7 MB (57650917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925c9f644e5b0bca4a0dc6f08736ac4de9ebf80e4d45ab5df9500fe29747adcb`  
		Last Modified: Tue, 09 Dec 2025 01:17:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:38bf793e006e6e66fa8fa68efa6626ffb7f52e3f1fb1807158b704957c7f2085
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10551519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6818b1c899a413646dd4a14aaaad8c344805f189e70ee201bebb0baa0c35f8d`

```dockerfile
```

-	Layers:
	-	`sha256:c800f3e2ed304dc45527c10d6710eee5e5b7f36638db63d8f723deed82c4bdfc`  
		Last Modified: Tue, 09 Dec 2025 03:23:50 GMT  
		Size: 10.5 MB (10523588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a9a5d0b64d3207492cece84445bcfc5214e69eb797ebf481582f0f9a6b8e237`  
		Last Modified: Tue, 09 Dec 2025 03:23:51 GMT  
		Size: 27.9 KB (27931 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bookworm` - linux; 386

```console
$ docker pull golang@sha256:ed58ed33d706ff05d640f8c76eb6c8373af72ac58f2eb898c6669b31951260c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 MB (289276933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b143e57538fdac7ca7baad202b2618ecb20947824e4f98241637f96815cd0b18`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:14:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:23:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 01:17:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 01:17:54 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 09 Dec 2025 01:17:54 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Dec 2025 01:17:54 GMT
ENV GOPATH=/go
# Tue, 09 Dec 2025 01:17:54 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 01:17:54 GMT
COPY /target/ / # buildkit
# Tue, 09 Dec 2025 01:17:56 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 09 Dec 2025 01:17:56 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:5a0767b6533dfa923197197a2adf3860bde889326cc3199fec46ced873deb7e1`  
		Last Modified: Mon, 08 Dec 2025 22:16:44 GMT  
		Size: 49.5 MB (49466819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8c9cca3d9f455dde3fab1917d275b029f5f2978fcd1f8f1b757098b58abc9d`  
		Last Modified: Mon, 08 Dec 2025 23:14:28 GMT  
		Size: 24.9 MB (24864339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd442778352104a3bf918f8351b8ac2573f9aa7b0d9136092884f7f79017f9a2`  
		Last Modified: Tue, 09 Dec 2025 00:24:01 GMT  
		Size: 66.2 MB (66233858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f3cb927ee60d49a38f7fc43c4514c091528d26d20e4fb28d1f182afa36aa16d`  
		Last Modified: Tue, 09 Dec 2025 01:18:42 GMT  
		Size: 89.8 MB (89839821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b714db6db5fd611306e3219023556e73fccd367a39f79eb9eb020ec36684466f`  
		Last Modified: Tue, 02 Dec 2025 17:48:21 GMT  
		Size: 58.9 MB (58871938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616471cffbca7cc854e38ce35500c7517b635212dd0b259ea7a57d618617a6e1`  
		Last Modified: Tue, 09 Dec 2025 01:18:28 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:875c9387755cfa5204153d9ad795ddb29035e5c1889375b66fce2cab2e936af4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10503074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed856739195e55bf840bf05b7cf2b662186f50cdfb7a6dbaf795bf3ecab4e4ac`

```dockerfile
```

-	Layers:
	-	`sha256:e18d21d25f206f62eb94cd589ae299559fb9ed0f1e39bd7c58bb7b3c06abb08f`  
		Last Modified: Tue, 09 Dec 2025 03:24:01 GMT  
		Size: 10.5 MB (10475313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb0a3fc0bd92cbba0a8e9fafcb087719cdac3c12cfa392afe630e74080bfbb6f`  
		Last Modified: Tue, 09 Dec 2025 03:24:02 GMT  
		Size: 27.8 KB (27761 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:761ac7e26f737551e312d7892c66dc03b90f7c70df31c931e76a3d0b2092e0fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.3 MB (262275800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70b167ded7bf95732b9a1dcef243fff694d6f308c3bf2e8e5f5ce50ef9825f32`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 19:40:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 22:11:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 23:35:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 17:46:31 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 02 Dec 2025 17:46:31 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 17:46:31 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 17:46:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 17:46:31 GMT
COPY /target/ / # buildkit
# Tue, 02 Dec 2025 17:46:45 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Dec 2025 17:46:46 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6d4a3f53f449c0e9b84d889c71d1f21df5764d821465bd1337060660aa78c65e`  
		Last Modified: Tue, 18 Nov 2025 01:11:17 GMT  
		Size: 48.8 MB (48760956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754bf41c56cb3beefc6b6211c26bdc048d41c337f12bc0bbfcfa89dfb5de99b7`  
		Last Modified: Tue, 18 Nov 2025 19:40:58 GMT  
		Size: 23.6 MB (23614038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7a4cb619dbd7fcb3e0be3246f973ccbe692039c1fd01a193751c60045de0d3`  
		Last Modified: Tue, 18 Nov 2025 22:12:34 GMT  
		Size: 63.3 MB (63309296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:870c654cc97051b29e543234a565ca86980db6e2499d45b06d4424741a820d98`  
		Last Modified: Tue, 18 Nov 2025 23:38:02 GMT  
		Size: 70.0 MB (70016928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a811f73ff0cb3df64f15904472d8c052172a4266c947c138019cab5cd2bb575`  
		Last Modified: Tue, 02 Dec 2025 17:48:38 GMT  
		Size: 56.6 MB (56574424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8db03ee1eec28579922a5f9de30a7ddd80a30842e9bfaab86aaa5d32c2de5d4e`  
		Last Modified: Tue, 02 Dec 2025 17:48:33 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:ad348627e37d691609661e66e6a9e72929c5842fe122b3ee393e9f580e5f5993
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.7 KB (27653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28c09389455c8e6c19b04647e083d1c01dc747cbfd7e6c3f25305e4e4b6cd083`

```dockerfile
```

-	Layers:
	-	`sha256:ce8405d402b5eb07104a14ec9faf8abe87c644ccdda5d7d4a991eddee8746731`  
		Last Modified: Tue, 02 Dec 2025 18:10:53 GMT  
		Size: 27.7 KB (27653 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:7be8e0eb4743fe5ddea75f00797a0249e041a91f857803ce90dc0aec4d6a66e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.4 MB (296400242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e7843922480b6d0e44719be61547fb74ad98114a908936e1f5af6bc8f2499ec`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 22:28:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:21:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 02:12:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 02:12:05 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 09 Dec 2025 02:12:05 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Dec 2025 02:12:05 GMT
ENV GOPATH=/go
# Tue, 09 Dec 2025 02:12:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 02:12:05 GMT
COPY /target/ / # buildkit
# Tue, 09 Dec 2025 02:12:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 09 Dec 2025 02:12:25 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c088128ea77bb5c706bb00930020ea2fba147060275f49c5a7be6b54af5ca7c8`  
		Last Modified: Mon, 08 Dec 2025 22:17:06 GMT  
		Size: 52.3 MB (52326977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4109a037ac4c69c3ce26e6d14e10c867842083c363485abd63db45502611991`  
		Last Modified: Mon, 08 Dec 2025 22:28:59 GMT  
		Size: 25.7 MB (25672209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd2b93c70c0b05a907d16ae217d77a407e9aa88f69499ffbfee4375b49ab6c01`  
		Last Modified: Mon, 08 Dec 2025 23:22:14 GMT  
		Size: 69.8 MB (69846008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21fcf0300c06237c12ec60c09556f95a6b8c833ba82bfc5828beb977742de538`  
		Last Modified: Tue, 09 Dec 2025 02:13:29 GMT  
		Size: 90.4 MB (90419946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b0da503e4b3d4a624ac596179648e9a31a4f87f7d37fdb8c7bef57190d6ed7d`  
		Last Modified: Tue, 02 Dec 2025 17:48:12 GMT  
		Size: 58.1 MB (58134946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a20f8398526b7e32e5610cbaf93e2d1dc9ef12fe14e2f40d8981cbf322083f`  
		Last Modified: Tue, 09 Dec 2025 02:13:23 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:26f6b8379232a27c484820400b1d8f4aed4033968a8ea21ba0f8221e7d6f19eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10496078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63c6f5c90c55d3f98b3e3134a332c426d11b6cbfc21b5050509fc7e9bbb85dad`

```dockerfile
```

-	Layers:
	-	`sha256:a9cce1234d409d1894452021b7e8872ff49b9855f41f46b8e5079291672e81da`  
		Last Modified: Tue, 09 Dec 2025 03:24:12 GMT  
		Size: 10.5 MB (10468233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cc991258b0b5f35f2d2a8630acdfc640f89cdf40bb6fb47d6a78752739fa826`  
		Last Modified: Tue, 09 Dec 2025 03:24:13 GMT  
		Size: 27.8 KB (27845 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bookworm` - linux; s390x

```console
$ docker pull golang@sha256:da54e6a866547deb3c3fa8bc4fe77b540683cdc7292230b262ebfe3fc92b67af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.2 MB (263163415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83b636998ac43873427e196eeff14300ed60d3edd4c8b88789763d207e14c56c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 00:10:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 01:45:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 02:59:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 02:59:32 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 09 Dec 2025 02:59:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Dec 2025 02:59:32 GMT
ENV GOPATH=/go
# Tue, 09 Dec 2025 02:59:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 02:59:32 GMT
COPY /target/ / # buildkit
# Tue, 09 Dec 2025 02:59:34 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 09 Dec 2025 02:59:35 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f1896ba83f603ad81e0d8cb48b496e763b4b781a68efe11f1b6de9da929514ea`  
		Last Modified: Mon, 08 Dec 2025 22:15:09 GMT  
		Size: 47.1 MB (47137665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4635598f3b0f128359fc25d526138bfeb1cfd50aa2df3f8a5a9214cdae1551f`  
		Last Modified: Tue, 09 Dec 2025 00:10:58 GMT  
		Size: 24.0 MB (24027286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c85977b1427cc2c2afbab15cfdcc745e64492465bdc1299648a91c7787a768`  
		Last Modified: Tue, 09 Dec 2025 01:46:34 GMT  
		Size: 63.5 MB (63501228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe7c78d8ef4c672ad3a1b17951daa282f21316a1dab32f99d9430a850ba86084`  
		Last Modified: Tue, 09 Dec 2025 03:00:20 GMT  
		Size: 69.0 MB (69009858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036b6dba2ceabbb92eb6c9ebccd3e6b705dacf7cc4426156bbedfd17ad5dc53b`  
		Last Modified: Tue, 02 Dec 2025 17:49:47 GMT  
		Size: 59.5 MB (59487220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc9caad544c3834ba0a3a1c507df39d82fa12eda45b7621ee781a25f1640f424`  
		Last Modified: Tue, 09 Dec 2025 03:00:15 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:d63d532373ca382e3375a6e7fcbc47f9c086f0f7889cf700a12e1b42d81a4419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10355295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a8072f5902460707ad585de1b270ad06efb3e9b5941416d413e909eaabed2bc`

```dockerfile
```

-	Layers:
	-	`sha256:e7b02ac9ef323744c4f39980bce6f20f316f16dde9681f8a48d51adb5d45a928`  
		Last Modified: Tue, 09 Dec 2025 03:24:23 GMT  
		Size: 10.3 MB (10327498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fac87caa068e7bee2415443f00e7afdb38b73203596024d2a4c50585c3648349`  
		Last Modified: Tue, 09 Dec 2025 03:24:24 GMT  
		Size: 27.8 KB (27797 bytes)  
		MIME: application/vnd.in-toto+json
