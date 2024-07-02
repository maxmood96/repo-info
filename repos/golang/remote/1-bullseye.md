## `golang:1-bullseye`

```console
$ docker pull golang@sha256:94979407a177c0ce8df18345968f9c797d291fc0fc09b76b2daa0ca85a975556
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

### `golang:1-bullseye` - linux; amd64

```console
$ docker pull golang@sha256:994abcfeaa8dde427ab7621b5ae4d48f4b6d05f5a96d64df7bc191178d9b42ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.7 MB (280708009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0a7ceae7c3a3b80b4213ff80a4143715d9bf11cf817e3078beb9f0ebf7e23a3`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 20:46:13 GMT
ADD file:b8d066bbda2d783c3ca81ab100fc5e45550234b68fde96332f303f669256842e in / 
# Thu, 13 Jun 2024 20:46:13 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 20:46:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 20:46:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 20:46:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Jun 2024 20:46:13 GMT
ENV GOLANG_VERSION=1.22.4
# Thu, 13 Jun 2024 20:46:13 GMT
ENV GOTOOLCHAIN=local
# Thu, 13 Jun 2024 20:46:13 GMT
ENV GOPATH=/go
# Thu, 13 Jun 2024 20:46:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 20:46:13 GMT
COPY /target/ / # buildkit
# Thu, 13 Jun 2024 20:46:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 13 Jun 2024 20:46:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c1c1a7d83fb1e16686c4e98df3d6f88b37beb4d65daae1ddd715f95d7ac4db5c`  
		Last Modified: Tue, 02 Jul 2024 01:29:07 GMT  
		Size: 55.1 MB (55081360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a305f523084f0a28b5daf532a5216d9be05d863c6bd3f5bd2969965eb7e9a27`  
		Last Modified: Tue, 02 Jul 2024 02:01:21 GMT  
		Size: 15.8 MB (15764174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da238dd9d1f579bf4f3cd6589e3ab75747f8ea35be2bf50403f8f3fafa942eea`  
		Last Modified: Tue, 02 Jul 2024 02:01:35 GMT  
		Size: 54.6 MB (54588637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ee7c47da974d1d239691559eb9eef2ffc1fae27bd1ea3396f3330f7714d5bf`  
		Last Modified: Tue, 02 Jul 2024 03:17:09 GMT  
		Size: 85.9 MB (85928132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:060aaf7efd0676cdf56165fe26e63a047d7f3c483ab1043d530db9370e6c28e7`  
		Last Modified: Fri, 14 Jun 2024 17:54:07 GMT  
		Size: 69.3 MB (69345548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48866d98b46eba4dc71d6655937077b331e2b63d8df094d1c150b874d1596a7`  
		Last Modified: Tue, 02 Jul 2024 03:17:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:a41484716f5f955a944cfc5720cd42640db0a39ca9b4eb489330ecd52f4547b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cd17d761cff0d8e88536c632a699c79bd41a278a997bbb8ebf914e0ee95ba88`

```dockerfile
```

-	Layers:
	-	`sha256:7f4b111e9f5b1a17a8c27bd941aca9c295b3e840c31a7dc295cd611908e89615`  
		Last Modified: Tue, 02 Jul 2024 03:17:08 GMT  
		Size: 26.1 KB (26130 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bullseye` - linux; arm variant v7

```console
$ docker pull golang@sha256:f7538b0cb8e8411a2d6d4b4ce1869c565c2bc8ed1de8781a67b6d184e155763c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.1 MB (248055288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5735b9214b1724339a792359572228f1a674c8208659aad17fdccb900f0e16ad`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:57:50 GMT
ADD file:4993add96e8cc180b89e1b978fddc0b0876a303bce87dc08120edbe9513432bd in / 
# Thu, 13 Jun 2024 00:57:51 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:24:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:24:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 20:46:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Jun 2024 20:46:13 GMT
ENV GOLANG_VERSION=1.22.4
# Thu, 13 Jun 2024 20:46:13 GMT
ENV GOTOOLCHAIN=local
# Thu, 13 Jun 2024 20:46:13 GMT
ENV GOPATH=/go
# Thu, 13 Jun 2024 20:46:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 20:46:13 GMT
COPY /target/ / # buildkit
# Thu, 13 Jun 2024 20:46:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 13 Jun 2024 20:46:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:45c5e98886f73bd45565e271bba1de66ffee1cfe17345d38a8e7179841133d4f`  
		Last Modified: Thu, 13 Jun 2024 01:01:59 GMT  
		Size: 50.3 MB (50256430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d823c90ec6db52ee3c5a3a116b21e47442be8c0e35cc53f6f7f4db398ba08fe`  
		Last Modified: Thu, 13 Jun 2024 01:34:16 GMT  
		Size: 14.9 MB (14880170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:738fc6141957592e4d069a8fcb0615b3f6dd757c25ee58dd7023fb923a7a4ecc`  
		Last Modified: Thu, 13 Jun 2024 01:34:36 GMT  
		Size: 50.4 MB (50359459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f01173d5f6faf378a963c968221828a841ef7d84c2d9b13c9e62f759c681f143`  
		Last Modified: Fri, 14 Jun 2024 17:55:09 GMT  
		Size: 64.8 MB (64845661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8d8376f429e08832ffbb91ed771b1b953556865415b4e4c37033a89a2f8aca`  
		Last Modified: Fri, 14 Jun 2024 17:54:08 GMT  
		Size: 67.7 MB (67713411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:305e802f91198699ef588e5033b1e0a2f433c89e60218ea4a5c1373cb74ee8af`  
		Last Modified: Fri, 14 Jun 2024 17:55:07 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:8d7fe0f81d66d422d4ec8d57bc01ed20a6217dd152e4040c30a928152008e275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7718b23ca3c49e9c86d8f0ddf1bbc824862ca390cad27ddf87d3624bf6d2bce`

```dockerfile
```

-	Layers:
	-	`sha256:38abe1615910e7f11b03913e3dd781b676d50431a6980659c15cd0c818d42766`  
		Last Modified: Fri, 14 Jun 2024 17:55:06 GMT  
		Size: 26.2 KB (26226 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bullseye` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:7133eef0d37635670f208bf1db27b9b727f754bf4e7d7ae7c00998ae783d45a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.8 MB (271794125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bb9bf56ebd2e2f85b5635b6a308f13d613bf3f6fb1db19dc70101b2fb064b43`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:39:57 GMT
ADD file:cd3edc79f93d09aa5daffba99cc698c3fe0e02348e8dc284ef466b7e6596e68c in / 
# Thu, 13 Jun 2024 00:39:58 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:22:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:23:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 20:46:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Jun 2024 20:46:13 GMT
ENV GOLANG_VERSION=1.22.4
# Thu, 13 Jun 2024 20:46:13 GMT
ENV GOTOOLCHAIN=local
# Thu, 13 Jun 2024 20:46:13 GMT
ENV GOPATH=/go
# Thu, 13 Jun 2024 20:46:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 20:46:13 GMT
COPY /target/ / # buildkit
# Thu, 13 Jun 2024 20:46:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 13 Jun 2024 20:46:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f975e52008de385eb513258b4912477b214cddf1c8e87877f85028d940bfcdae`  
		Last Modified: Thu, 13 Jun 2024 00:43:32 GMT  
		Size: 53.7 MB (53739581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859b5bb8f5d471015f3add7e778bc507fc4a6f1fce8561c2b0a336734a55a365`  
		Last Modified: Thu, 13 Jun 2024 01:31:15 GMT  
		Size: 15.8 MB (15750467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a7ca076c1ea04622ddf9f43ff2f138f6c50a40118747a45d2618cc64591d6b`  
		Last Modified: Thu, 13 Jun 2024 01:31:29 GMT  
		Size: 54.7 MB (54696375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87b18aaeabff49201298710a8143baffcde2c6bca3b90ba16eb1d1e3bbacb2a`  
		Last Modified: Fri, 14 Jun 2024 19:46:05 GMT  
		Size: 81.3 MB (81337221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2259e4bd2629c850a0f37f6d3351f44770f5d4afee65aac3cddcb3bf2a735031`  
		Last Modified: Fri, 14 Jun 2024 19:43:41 GMT  
		Size: 66.3 MB (66270325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71fd0c5459c9f42e6a30209858cda3e789e4a9464604a443efea263a8cad970d`  
		Last Modified: Fri, 14 Jun 2024 19:46:02 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:f229b0cfa3f2d99a070ba3c5eed119695ee8d1ae39db1a425de75e63e80d300b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 KB (26444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e36f3bc40a68d086d933369fd72652ba2fb941f8a31963689bb7111e75eb0b8`

```dockerfile
```

-	Layers:
	-	`sha256:75a8a70f1b9aeae6e812e3cf0436777c19ddf87426a1fb9d97dcbcf72d20e37b`  
		Last Modified: Fri, 14 Jun 2024 19:46:02 GMT  
		Size: 26.4 KB (26444 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bullseye` - linux; 386

```console
$ docker pull golang@sha256:15ec9a6e1253e1fbd09043a03976fc3b9c8ac486dae564f8576862557b247c02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.0 MB (282956293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:611e4820f376adb76e5d49e1bacb82349837619d67a57467c21e69b4f9f161a6`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 20:46:13 GMT
ADD file:e6fa59569d6234c463e39f7c2465f2984240a5e8cd613c1ffdc14ab3abb4a7ad in / 
# Thu, 13 Jun 2024 20:46:13 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 20:46:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 20:46:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 20:46:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Jun 2024 20:46:13 GMT
ENV GOLANG_VERSION=1.22.4
# Thu, 13 Jun 2024 20:46:13 GMT
ENV GOTOOLCHAIN=local
# Thu, 13 Jun 2024 20:46:13 GMT
ENV GOPATH=/go
# Thu, 13 Jun 2024 20:46:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 20:46:13 GMT
COPY /target/ / # buildkit
# Thu, 13 Jun 2024 20:46:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 13 Jun 2024 20:46:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:72a2b38d7f88bb9b0be6097180e8f8261c31815017cb512a158422c2bfba6973`  
		Last Modified: Tue, 02 Jul 2024 00:43:02 GMT  
		Size: 56.1 MB (56064975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:003014d72f23a9e0b16eb59708032ad565fe8e24244a34ae5b65e72f56314d8d`  
		Last Modified: Tue, 02 Jul 2024 01:15:23 GMT  
		Size: 16.3 MB (16267863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f8e3ef3e76ff601cae23732babfc202314066da48aedac550440cd3cdf72f2c`  
		Last Modified: Tue, 02 Jul 2024 01:15:41 GMT  
		Size: 55.9 MB (55927528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b12e0b2625bd5f4f6a84e407f7c9fd36b955470d2babc10786f511e70d285db9`  
		Last Modified: Tue, 02 Jul 2024 03:17:49 GMT  
		Size: 87.4 MB (87351252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d423f142b846e34cad754942d9961e223ceeaa092ba25d1bfbe95eb1364c405`  
		Last Modified: Fri, 14 Jun 2024 17:54:03 GMT  
		Size: 67.3 MB (67344518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9ff673974585edd6c0f38d712f6c5455ae72705dd0fad372a8b1d2b412207e2`  
		Last Modified: Tue, 02 Jul 2024 03:17:46 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:ffd9fa4726a33265196e8a6e943c48ae275d78b1c11e7699cea2d3161c4db7f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24e404b51b26d968a2c7ca88a40bada2245e8aca3e88ca0a9738a814b127c07a`

```dockerfile
```

-	Layers:
	-	`sha256:612fc66a7ae24b15766ce5c3904a3ec3cdec2d5c34b7e4e66ebe098eb84f7a92`  
		Last Modified: Tue, 02 Jul 2024 03:17:46 GMT  
		Size: 26.1 KB (26097 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bullseye` - linux; mips64le

```console
$ docker pull golang@sha256:e5105c47bf0cee49086d4a970d5acfe0a85042d5960ec852d8ae7c3ced2c5c41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.3 MB (253307845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47dd311c38bb01f1906089bc367aacff2ffbd4f543b356fdb2b06e0aeac7cf19`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:11:08 GMT
ADD file:2fd9c13efc7b13ca68928f53acc0c79d5841bd49e5aea46b2e1906120bba2a4f in / 
# Thu, 13 Jun 2024 01:11:14 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 02:08:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 02:10:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 20:46:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Jun 2024 20:46:13 GMT
ENV GOLANG_VERSION=1.22.4
# Thu, 13 Jun 2024 20:46:13 GMT
ENV GOTOOLCHAIN=local
# Thu, 13 Jun 2024 20:46:13 GMT
ENV GOPATH=/go
# Thu, 13 Jun 2024 20:46:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 20:46:13 GMT
COPY /target/ / # buildkit
# Thu, 13 Jun 2024 20:46:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 13 Jun 2024 20:46:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6c9f7b7d6baf92c8cec25b325ea14db33b8c298218a5bcd368bb24184c5645b6`  
		Last Modified: Thu, 13 Jun 2024 01:22:39 GMT  
		Size: 53.3 MB (53322503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f62fa3097190d71f8c07279b0414992956a17136d2040113e1f4910937c092`  
		Last Modified: Thu, 13 Jun 2024 02:39:25 GMT  
		Size: 15.5 MB (15530528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd553a7e4abf06bba101ca3a36c88140dd098954e94bafce76ee81b84c8c57ea`  
		Last Modified: Thu, 13 Jun 2024 02:40:14 GMT  
		Size: 53.3 MB (53313183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c365ac3444c0e416e7c1335e004f0fc31d520e7a7c18bf2bfd2133deba12426`  
		Last Modified: Sat, 15 Jun 2024 10:22:18 GMT  
		Size: 67.0 MB (67026433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a2a7c9f38944ddb0920b3c53f4ef6c7648ad7253bdc801ba491412f8469094`  
		Last Modified: Sat, 15 Jun 2024 10:18:46 GMT  
		Size: 64.1 MB (64115039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a229aff97ae6034fbfa99dbd6c9b54f0940f078e3b333f46881f549b01ff42b`  
		Last Modified: Sat, 15 Jun 2024 10:22:11 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:6313d7d036ff554d665655db1db03c09cb3b26bc2e9c7e81069d2e111b5376d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8232df5e0930583324e67a3f509d1f40da062c63147bfe031848aff12e828c72`

```dockerfile
```

-	Layers:
	-	`sha256:cac33a4d7ed206bb40790f41eefaf407423c956f3e7a7f44ff587b739d03af5e`  
		Last Modified: Sat, 15 Jun 2024 10:22:11 GMT  
		Size: 26.2 KB (26193 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bullseye` - linux; ppc64le

```console
$ docker pull golang@sha256:522994b5907f6c5e10492c5052b871de14869bc2366f2b1e0483d444ea086e18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.4 MB (281408885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c621e26be2dc700f435625bff02bab7d6b038508886b3c4f7ecf56328d48f995`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 20:46:13 GMT
ADD file:288859e020cf9178f55732ac2eaa62400e2c2d66b3ca500ac7df69c8025abba9 in / 
# Thu, 13 Jun 2024 20:46:13 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 20:46:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 20:46:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 20:46:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Jun 2024 20:46:13 GMT
ENV GOLANG_VERSION=1.22.4
# Thu, 13 Jun 2024 20:46:13 GMT
ENV GOTOOLCHAIN=local
# Thu, 13 Jun 2024 20:46:13 GMT
ENV GOPATH=/go
# Thu, 13 Jun 2024 20:46:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 20:46:13 GMT
COPY /target/ / # buildkit
# Thu, 13 Jun 2024 20:46:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 13 Jun 2024 20:46:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:202e493da11eac96a36d754afa396feec67f46e0492e70c0cc4d61dfb06d6a75`  
		Last Modified: Tue, 02 Jul 2024 01:22:20 GMT  
		Size: 59.0 MB (58950397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8661ff02529d6818e558d6049a746391403c023c68ac6d75816221bd99e3244c`  
		Last Modified: Tue, 02 Jul 2024 02:05:47 GMT  
		Size: 16.8 MB (16765868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b93f0edb37745f21593aefba0898d81dbc780a39dfe73cf03491e10c88480878`  
		Last Modified: Tue, 02 Jul 2024 02:06:04 GMT  
		Size: 58.9 MB (58872635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ab42523d892e2717971e783ff4165589cde8d035d88a63982681c46daebb3f`  
		Last Modified: Tue, 02 Jul 2024 10:08:38 GMT  
		Size: 80.4 MB (80379014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2210b2be98c546d98d20cd631f014745f73d191238d22c5e439478550b6727b8`  
		Last Modified: Fri, 14 Jun 2024 17:54:36 GMT  
		Size: 66.4 MB (66440814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4ddc703d1b8399b8c36c38e47726232410cead673218c50cd567e5fdc326dd9`  
		Last Modified: Tue, 02 Jul 2024 10:10:08 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:670d0d81657f0a26650a626487d9d3f80e78c751f6657cdd7bca27d419b501bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28234b7abcc5eb875f596681d4efddf636b9b4063ab9bc584f6529b207935fd6`

```dockerfile
```

-	Layers:
	-	`sha256:b2c128a4493a3fc3e837fd14ee9b7fc15971cda17387bc5e8ce5e2858ee1a428`  
		Last Modified: Tue, 02 Jul 2024 10:10:08 GMT  
		Size: 26.2 KB (26172 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bullseye` - linux; s390x

```console
$ docker pull golang@sha256:c4579954b41a36785c46b7e0fe65d77185d9889864c1e0df02908ab941c62be4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.1 MB (257089193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b688816c539aabd844071d03699e1b497c86a34f03d6506bf12f2f6e3d9e17d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:42:50 GMT
ADD file:1f0333c084fe60bf682ad64dd7db93b2ca069c7e1d09bf26e7e65dedbd65b0f3 in / 
# Thu, 13 Jun 2024 00:42:53 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 05:23:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 05:24:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 20:46:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Jun 2024 20:46:13 GMT
ENV GOLANG_VERSION=1.22.4
# Thu, 13 Jun 2024 20:46:13 GMT
ENV GOTOOLCHAIN=local
# Thu, 13 Jun 2024 20:46:13 GMT
ENV GOPATH=/go
# Thu, 13 Jun 2024 20:46:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 20:46:13 GMT
COPY /target/ / # buildkit
# Thu, 13 Jun 2024 20:46:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 13 Jun 2024 20:46:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:db300ed0c60856815a390ef84dc7c5441283ec11483c9da25ac0daf34bac6e83`  
		Last Modified: Thu, 13 Jun 2024 00:47:59 GMT  
		Size: 53.3 MB (53337540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b507bf58c92373ad020c252404bcc63be7764e5ba99e1b46dbe95f2fb0d32531`  
		Last Modified: Thu, 13 Jun 2024 05:31:46 GMT  
		Size: 15.6 MB (15642492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be3e3e4d728c88a0a3906e1d03b1ffe00d8ceb7ae7abbf81186d2f281bcbf540`  
		Last Modified: Thu, 13 Jun 2024 05:32:00 GMT  
		Size: 54.1 MB (54076476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bbf2e59aa4aa2007d77ab35e59a703309b306b1d41f05fb4e2e91477f4d28c5`  
		Last Modified: Fri, 14 Jun 2024 19:35:08 GMT  
		Size: 65.6 MB (65627304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d54ac55846ff64482893d22cd74289e959d60007f939ee44a6905370f9611de2`  
		Last Modified: Fri, 14 Jun 2024 19:31:27 GMT  
		Size: 68.4 MB (68405222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55342d48a24477240aff86c3e672a44c2437e624b5da2be5d814c096eedbff83`  
		Last Modified: Fri, 14 Jun 2024 19:35:07 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:d5971f7c4518a9852ead30feddddcf68246aeb081746eda81b6868e3c111a286
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23bf4f3f5ef2bc8f767c8923ff80bf975aef37d6056a89677cf21eb77fa0d512`

```dockerfile
```

-	Layers:
	-	`sha256:9fd063daea8183bcb4ed189f1e0225dab29ffb62d14379cdc36c219bee7b4178`  
		Last Modified: Fri, 14 Jun 2024 19:35:07 GMT  
		Size: 26.1 KB (26130 bytes)  
		MIME: application/vnd.in-toto+json
