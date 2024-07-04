## `golang:1-bookworm`

```console
$ docker pull golang@sha256:6c2780255bb7b881e904e303be0d7a079054160b2ce1efde446693c0850a39ad
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

### `golang:1-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:02ba164d64e0aee92ab808526e450dea546b5c59ee7d400d1c04c03c126cb59f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.3 MB (299325112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e1949e24b677ca35b6bbe1a7a7287f20e301b85d053fc70a8db1574d4c9e420`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 01:24:49 GMT
ADD file:e8aac9b1598114ead96b4038c19d915b87f662ef342291d69c7e5255c5d731fc in / 
# Tue, 02 Jul 2024 01:24:50 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:48:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:48:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 19:33:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOLANG_VERSION=1.22.5
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOPATH=/go
# Tue, 02 Jul 2024 19:33:45 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jul 2024 19:33:45 GMT
COPY /target/ / # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e9aef93137af6e967e7242f3b3c8ecd8e6f571d1e6fdd9e72db0befeeae3cf13`  
		Last Modified: Tue, 02 Jul 2024 01:28:26 GMT  
		Size: 49.6 MB (49554064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b365fa3e8dc16e70d89fab0e91f5242feb38ae3cfeb6655e654209ea109333`  
		Last Modified: Tue, 02 Jul 2024 02:00:17 GMT  
		Size: 24.0 MB (24049794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dbed71fc5444cf6889a21b002de3e7805e810aa88f91a9ca941b4e3880246d1`  
		Last Modified: Tue, 02 Jul 2024 02:00:35 GMT  
		Size: 64.1 MB (64142928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d214e0973057ab674eaed44f6892724e8d178b99bf21c7c9dc7534309d90ba59`  
		Last Modified: Tue, 02 Jul 2024 22:06:27 GMT  
		Size: 92.2 MB (92226073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a2f51ff3dde07bfa1ce35b5597b2d97295e64a461d98e696feda7b25a6dc5f`  
		Last Modified: Tue, 02 Jul 2024 22:06:15 GMT  
		Size: 69.4 MB (69352095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c363784b64c58e592fce332e559513453391a0a301bdc20b750139ad07688bbd`  
		Last Modified: Tue, 02 Jul 2024 22:06:20 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:157b268a13e7d7bf9bd5ee240015c9882196d628ee0767de81cf5dd2c886664b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 KB (27308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:576f83c6b48f9e141d03bdce58572d5639e2e6187a8eec0703420c9ce188569f`

```dockerfile
```

-	Layers:
	-	`sha256:1380681f3e9c3b5fb6f8dc06d706c57173bb9ea9779562180d19bef0dbc48a6c`  
		Last Modified: Tue, 02 Jul 2024 22:06:24 GMT  
		Size: 27.3 KB (27308 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:a5a68129d4ee3cac35083a9a43c59d294ce97f606f77fc78b8487a0745919f8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.1 MB (260122984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc2803e902afbdd522dc4dee48708bcc7741bcea3632f5422d9833a1d4af52b7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:59:52 GMT
ADD file:526dbb34ac449ae8f3c9025d71b3ffeb0e24fa5dc1a01da707f0a8b834eb4e33 in / 
# Tue, 02 Jul 2024 00:59:52 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:24:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:24:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 19:33:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOLANG_VERSION=1.22.5
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOPATH=/go
# Tue, 02 Jul 2024 19:33:45 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jul 2024 19:33:45 GMT
COPY /target/ / # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:335f2c484898b910fac13d5650ed3c78e5e673fe8dab1b06a071c71478a153d0`  
		Last Modified: Tue, 02 Jul 2024 01:02:57 GMT  
		Size: 45.1 MB (45148097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa30b2bcbde45c2fc67abf425197af3af3e67d55296f168143343ef1b0e2d3e`  
		Last Modified: Tue, 02 Jul 2024 01:39:04 GMT  
		Size: 22.0 MB (21954038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce4650a14deed524a46f7f7b410ff5d81e5ff66e51c7345e2b05887b6e3f4030`  
		Last Modified: Tue, 02 Jul 2024 01:39:24 GMT  
		Size: 59.2 MB (59222408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc7f2fe75a4daf18d1147e9f76c53bf858ad150b5ae53133d9d41e4b78a38ed`  
		Last Modified: Tue, 02 Jul 2024 13:02:43 GMT  
		Size: 66.1 MB (66081394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1377363fadc0bb3eb9a3cd846c096d02c646b0f4af9bef4893106284c049e37`  
		Last Modified: Wed, 03 Jul 2024 02:23:25 GMT  
		Size: 67.7 MB (67716891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ada05a606b6afd2eb4feeb70a1e736493f2d5a849489f2161737adaa303dcd`  
		Last Modified: Wed, 03 Jul 2024 02:23:23 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:2e9a78f527dd8ce9a01f885b74c6c3463608af31c154610012aa2bf4cc49862d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 KB (27435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:537a40775864191079802933694cde84847092fb43c0157daf0b1cec9d46c2a2`

```dockerfile
```

-	Layers:
	-	`sha256:e3dd38e175bb58f413e0fea0680903b61638e2593bcd2ffe5dee427efeb6c11a`  
		Last Modified: Wed, 03 Jul 2024 02:23:23 GMT  
		Size: 27.4 KB (27435 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:b2b1734fc70c4c5119b4e257fc558495bcd72e25b95c7ef2918eb705d9779211
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.7 MB (289708367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53e53bc1fdb43e59ff9b2ea3e71f05d3950ac4e396433b60e62c1848d47ec1f3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:29 GMT
ADD file:696648070a57689a69a184fda234045f7be4a8a9f3b2fff9031ff0a2d9914113 in / 
# Tue, 02 Jul 2024 00:39:29 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:50:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 03:51:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 19:33:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOLANG_VERSION=1.22.5
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOPATH=/go
# Tue, 02 Jul 2024 19:33:45 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jul 2024 19:33:45 GMT
COPY /target/ / # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0bd1f8180c504ba389021ce74895ed487ccd8c70e2d9af3707934bc801ba28d8`  
		Last Modified: Tue, 02 Jul 2024 00:42:03 GMT  
		Size: 49.6 MB (49588448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b16610496e73ba3d120d519598b53fa8a2db4c80ccc097a5016ad44aedd0654b`  
		Last Modified: Tue, 02 Jul 2024 04:01:41 GMT  
		Size: 23.6 MB (23591145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a6ab51b82df5ee608db374a16686eefb99bc53834af17064184653121729b3`  
		Last Modified: Tue, 02 Jul 2024 04:01:58 GMT  
		Size: 64.0 MB (63994637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d394a246346e2f7ec4919f14bacc627de6d4a2c15d2fb3b623218717c2c9c63b`  
		Last Modified: Wed, 03 Jul 2024 01:41:58 GMT  
		Size: 86.3 MB (86261753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad54470edeaca3376e9010d6ee8ae76847ce9900d3bfcdf32fc98cfd6fc2fa26`  
		Last Modified: Wed, 03 Jul 2024 01:41:58 GMT  
		Size: 66.3 MB (66272226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f1f84ca957ef7aee0a1d21dc51b26ffacf6b45448b5071963f73068df1cfc2f`  
		Last Modified: Wed, 03 Jul 2024 01:41:55 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:644a20a8c80cdd19bf9818bab76ed96bcad1362ae12ac48d63887d2ca7ed0bcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.7 KB (27672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73937b0f830edbe4f0e773e0472d2649b73b4429bb1ed9a31280c7d4cc1356fd`

```dockerfile
```

-	Layers:
	-	`sha256:f33aa2b0240ab74769830df12eb302495815be64aae0bf6491db1dafa5390090`  
		Last Modified: Wed, 03 Jul 2024 01:41:55 GMT  
		Size: 27.7 KB (27672 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; 386

```console
$ docker pull golang@sha256:c8715e797d0705204fdeeaf791773c80d5a036c021779984b4c817d84f9b19cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.4 MB (298426309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d43ddce9e0a98c7e126f0a474dc5c77f48b47aadfdc126b1660f26f93c864f09`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:38:40 GMT
ADD file:262529672396993121e97bbbdda3d91ce43c7548adf11a263b7ec53bb7cda4d2 in / 
# Tue, 02 Jul 2024 00:38:44 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:05:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:05:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 19:33:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOLANG_VERSION=1.22.5
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOPATH=/go
# Tue, 02 Jul 2024 19:33:45 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jul 2024 19:33:45 GMT
COPY /target/ / # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:04a42c358dbd9e835f8ae412589572f1bb5a19d9428a4854e4e845c88e34cb31`  
		Last Modified: Tue, 02 Jul 2024 00:42:16 GMT  
		Size: 50.6 MB (50579307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77fc07fa7086d431c647128f1beada8efce9ea5808c01b2bf497e7e85b1fda1b`  
		Last Modified: Tue, 02 Jul 2024 01:14:02 GMT  
		Size: 24.9 MB (24890132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bff6c9a28c036769727a4cf9dbe067b96273c0352a50922f6e950491245fc03`  
		Last Modified: Tue, 02 Jul 2024 01:14:24 GMT  
		Size: 66.0 MB (65988734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c92b42c8378d2b0b52ce5584ff022cd842a3dd919875e187c869609da41568`  
		Last Modified: Tue, 02 Jul 2024 22:06:30 GMT  
		Size: 89.6 MB (89626622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b75921c461b2ae6d1ff16df768b5e8ff34e9b73cf9704174903aa4e8c76f79`  
		Last Modified: Tue, 02 Jul 2024 22:06:19 GMT  
		Size: 67.3 MB (67341356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a906566c3569867c7f7087541c47967b96287d02282fe02f72ee191ffd5251`  
		Last Modified: Tue, 02 Jul 2024 22:06:28 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:f7fe9ab7b6e90a982f2d7e4aff5653c9f03690e46e1bb2e6d51e3099ddc8ed70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 KB (27255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d90a6932dd3a4f59b5076148d20c33ba91c1ccc0b136e6b5b67e826fffac2b3e`

```dockerfile
```

-	Layers:
	-	`sha256:e139a5a2b533c2c172c9329ecba61d447a96930c896817ae9b5e74917064fd18`  
		Last Modified: Tue, 02 Jul 2024 22:06:27 GMT  
		Size: 27.3 KB (27255 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:a6126aff0b85cfc4cd745867bb49a5ee39a78a89cbfe8920b062c34341ab47fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.1 MB (270084459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e3d2618453ca455e5568bad65928a522f7787e2edf863eb0dd612cd9bc36457`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 01:17:40 GMT
ADD file:7398b3272eb97d7c196f6072f2a25952abf995169e82ecb85361b7659b2fb005 in / 
# Tue, 02 Jul 2024 01:17:47 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:55:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:56:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 19:33:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOLANG_VERSION=1.22.5
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOPATH=/go
# Tue, 02 Jul 2024 19:33:45 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jul 2024 19:33:45 GMT
COPY /target/ / # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:827f475650f14eab4a6679f0e49d9155db82de1d5209a3817922c689f46adf08`  
		Last Modified: Tue, 02 Jul 2024 01:28:47 GMT  
		Size: 49.6 MB (49563118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c410c8d28a38525afd5f655d0e2d89727c34a9099ce124494526fbe8c30ef52c`  
		Last Modified: Tue, 02 Jul 2024 02:29:31 GMT  
		Size: 23.6 MB (23634676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0277124339cdea065e75bfae0dd207bb4e1d178268d7e5611472c2f31474deac`  
		Last Modified: Tue, 02 Jul 2024 02:30:24 GMT  
		Size: 63.0 MB (62965735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7213b1bee461c6c8b462f6111eda96f55dc07ee33fd06e19c73519ab099b16cb`  
		Last Modified: Wed, 03 Jul 2024 23:26:17 GMT  
		Size: 69.8 MB (69797658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7fcaebbd35ab2c899d9cd314218438d9bc23d7a6b5309c43bb0d51d8902f10a`  
		Last Modified: Wed, 03 Jul 2024 23:32:17 GMT  
		Size: 64.1 MB (64123113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4783f5b79a2c11f85ac9ee60e0ad70c6eb0080dd4c15f3a6d3f3c0b75e5b29dc`  
		Last Modified: Wed, 03 Jul 2024 23:32:11 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:0fc7654dde8f4bb9262bec407491aebd01bdee46fb41ad17164931ae7dc19622
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 KB (27407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bcabfcc57fd13b8fa25ae3437e12319ba98d339f100ded422deb5df3a889d7e`

```dockerfile
```

-	Layers:
	-	`sha256:1051e80ce591689860ee434b12bef7e5a52a3c89b0a64b76805056f6c280b756`  
		Last Modified: Wed, 03 Jul 2024 23:32:11 GMT  
		Size: 27.4 KB (27407 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:b9b98ee799bef76fa530223608655aa1f9cef2d7e5de4e22a8be96f7fe72659c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.5 MB (305488628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2a57eb3cc0dc956d348f9bdedcd5cf00100830819432f89164fe1365ca08265`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 01:17:20 GMT
ADD file:a02c311ba745dd8d5b3cc5585e2fe57a4aa9807b1ca2005815257da116010b54 in / 
# Tue, 02 Jul 2024 01:17:22 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:44:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:45:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 19:33:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOLANG_VERSION=1.22.5
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOPATH=/go
# Tue, 02 Jul 2024 19:33:45 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jul 2024 19:33:45 GMT
COPY /target/ / # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2ebe64104880a6a83eee169b12fbd82da8a0ddeac711670e50f30e975bcb92bc`  
		Last Modified: Tue, 02 Jul 2024 01:21:30 GMT  
		Size: 53.6 MB (53557015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf317c43d118e9cf38efabf9b1e93b406add8c26e307fde367e39a47a1c5821`  
		Last Modified: Tue, 02 Jul 2024 02:04:25 GMT  
		Size: 25.7 MB (25695092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e91f1c93d43f65ddb5b49fa7540ab263862ed9868139cb0bfc51bd8dffe47f60`  
		Last Modified: Tue, 02 Jul 2024 02:04:48 GMT  
		Size: 69.6 MB (69582302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8d7a11648763f65f8f31a28de4852a7a8071d08780307f9c0139b2f1ec04ab5`  
		Last Modified: Wed, 03 Jul 2024 09:51:54 GMT  
		Size: 90.2 MB (90204627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5442a44a1d407a5a3d1cba7a7a9b8820f3afe463e19c35ae36202ab5abc57af4`  
		Last Modified: Wed, 03 Jul 2024 09:51:53 GMT  
		Size: 66.4 MB (66449434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c6c6db8cd964ae0b519923a472c1298906dd905ffbe00713b395fc392bf7a0`  
		Last Modified: Wed, 03 Jul 2024 09:51:51 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:a54d17c773eaaa3e9a4918cf7fbb4e0857da5141b76ff93b7fff96db99369d07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 KB (27374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33acabdbe385622bc521db83e132f113113dabed1ad9a6cadbe17d616c1cd3ad`

```dockerfile
```

-	Layers:
	-	`sha256:3fe8f76c650f0a8ffaba6a0ae823e55b767aec7f605de8c0a5d84ac17320582b`  
		Last Modified: Wed, 03 Jul 2024 09:51:51 GMT  
		Size: 27.4 KB (27374 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:342a4710226a240fd0e90ee4aa1ff3d3f00c1e8b594ea7ff20bb11a52df056cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.3 MB (272309934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5166f807ee8da3d066cb88ce41336a52b983c1cf5c00287cb643e31c83ff298f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:43:28 GMT
ADD file:397aa43721bc5ca67ab359263843a05c62e131f07114e92f39927f59790c9a5b in / 
# Tue, 02 Jul 2024 00:43:30 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:32:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 03:33:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 19:33:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOLANG_VERSION=1.22.5
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOPATH=/go
# Tue, 02 Jul 2024 19:33:45 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jul 2024 19:33:45 GMT
COPY /target/ / # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1b8bfe08588d8939b4d39134c5c614351649e3890ceb7c234b7542f58d7bcc28`  
		Last Modified: Tue, 02 Jul 2024 00:48:16 GMT  
		Size: 47.9 MB (47931511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d37bf3d98ae5de59851adab45daeaaca9d29f76110a2923bd8937c4ad2e8cd52`  
		Last Modified: Tue, 02 Jul 2024 03:44:34 GMT  
		Size: 24.0 MB (24048872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6cb3bef78d7b20f095bd16b5a39e3ffec90c96f6d1307f8672edb9deef1c5f`  
		Last Modified: Tue, 02 Jul 2024 03:44:49 GMT  
		Size: 63.1 MB (63125178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2648ecceca5693703d9165456c226506a3e735223a1bd53a013c8e03b716bab5`  
		Last Modified: Wed, 03 Jul 2024 01:07:59 GMT  
		Size: 68.8 MB (68792642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36325bf1498477d36098ce5907eb7a794a2e7eb1ff088a91163f8cf4d9ca6b9`  
		Last Modified: Wed, 03 Jul 2024 01:08:00 GMT  
		Size: 68.4 MB (68411572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a71e214f2a43c6152071d87736a159592f13b5b39572b199e24f6124df7fce2b`  
		Last Modified: Wed, 03 Jul 2024 01:07:58 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:8d9d502648057240f83f7dbec1e7d0c4623ca67065a9fa0367e4a1709e29a68a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 KB (27308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccedb979d8e52571e036cba67f13f1f0295099a9427831f4cb63bedd9562b780`

```dockerfile
```

-	Layers:
	-	`sha256:f57f3612eceb839b6a92b6bc12d2a979af8c614502cf1c0cd1ff0e27e6c67b38`  
		Last Modified: Wed, 03 Jul 2024 01:07:58 GMT  
		Size: 27.3 KB (27308 bytes)  
		MIME: application/vnd.in-toto+json
