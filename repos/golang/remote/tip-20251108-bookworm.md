## `golang:tip-20251108-bookworm`

```console
$ docker pull golang@sha256:50a9e80dd8dedd57bd9f9592128c36d14ceda417fc418dd299e8942064af791f
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

### `golang:tip-20251108-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:89c73db5127b7f7dc835b3c2db5f5700a78dc464ee40f35bf761f1f886afe1e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.0 MB (320985718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9adca349564e2927cb280419bbe8d70902991afc3d3e75f6d52b2d3079baea2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:27:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:14:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Nov 2025 21:25:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Nov 2025 21:27:10 GMT
ENV GOTOOLCHAIN=local
# Mon, 10 Nov 2025 21:27:10 GMT
ENV GOPATH=/go
# Mon, 10 Nov 2025 21:27:10 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 21:27:10 GMT
COPY /target/ / # buildkit
# Mon, 10 Nov 2025 21:27:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 10 Nov 2025 21:27:12 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:5d93aea697980315f27f81c68582d14f63dd3579c2d3a27dc495a588279eda20`  
		Last Modified: Tue, 04 Nov 2025 00:12:20 GMT  
		Size: 48.5 MB (48481056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb445e472b1bad54f5a28edd51b11aec79eca8513394866a261891be9da6a343`  
		Last Modified: Tue, 04 Nov 2025 00:28:00 GMT  
		Size: 24.0 MB (24029301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2123190679e81d983648da92f1bb9ddc74383512edb00ad64f93d24d00d8807a`  
		Last Modified: Tue, 04 Nov 2025 04:14:49 GMT  
		Size: 64.4 MB (64396145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79da27cee6b4f0fdf751dd58d18bc54b5b33b316079756547a6443f03b9b5de2`  
		Last Modified: Mon, 10 Nov 2025 21:28:06 GMT  
		Size: 92.4 MB (92402013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feaf52c0c17111119e1092b7027d6d86d20ff4880cb34ac8f9ccc8cf394dc978`  
		Last Modified: Mon, 10 Nov 2025 21:26:54 GMT  
		Size: 91.7 MB (91677046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae5f06624625e0072879f3dd1938ce5ea342e0748c5a698f05fc9616dbceba4c`  
		Last Modified: Mon, 10 Nov 2025 21:27:47 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251108-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:8c0d33d5c1e38cc454748b3372009795888de28c58852c992af132befbd000fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10524774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d8593c2351a6acf8f48784399a156fcdbae73e58446800ad1837c723d9832c4`

```dockerfile
```

-	Layers:
	-	`sha256:e79a87480e31d708aceda9bfb414a765ee7dbb50144eaf9912f25541a0706008`  
		Last Modified: Tue, 11 Nov 2025 00:24:44 GMT  
		Size: 10.5 MB (10496388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e63122af1b0f9d669381c61e22e277ed11c565f40073f375c9108a6428233a1`  
		Last Modified: Tue, 11 Nov 2025 00:24:45 GMT  
		Size: 28.4 KB (28386 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251108-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:86a199487ecb0aa3708ac61d095676996f51e05a4888e9614530dc2d9eccd4bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.9 MB (279881831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e00fde10a0aa880d5cc2b76d422c890d1861020a7e46fa95cebd7281771a2d4b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:38:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 02:17:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Nov 2025 21:25:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Nov 2025 21:27:31 GMT
ENV GOTOOLCHAIN=local
# Mon, 10 Nov 2025 21:27:31 GMT
ENV GOPATH=/go
# Mon, 10 Nov 2025 21:27:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 21:27:31 GMT
COPY /target/ / # buildkit
# Mon, 10 Nov 2025 21:27:34 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 10 Nov 2025 21:27:34 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:461f215c759f019a0fb4d33c976a91c4c2e4b033762b07a2f81bac66dee9e613`  
		Last Modified: Tue, 04 Nov 2025 00:12:30 GMT  
		Size: 44.2 MB (44196437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad602f359c1ad647108cc57270e592fc1f62f8ffd947a100fecee62a4a0d017`  
		Last Modified: Tue, 04 Nov 2025 00:39:15 GMT  
		Size: 21.9 MB (21934879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4c6c96cff86026dfac835fc2d229a348ec06ff2d2c520014ac2aeb4555bd9e`  
		Last Modified: Tue, 04 Nov 2025 02:18:15 GMT  
		Size: 59.7 MB (59652141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460af16387b27431ee8e4eff388ded2e73f4cdc294bdd12794a20cd3f31efb5b`  
		Last Modified: Mon, 10 Nov 2025 21:28:13 GMT  
		Size: 66.3 MB (66255243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80af05985c341b2243144191457637b935a05afcbc1ddf3359092401ff8e5eb3`  
		Last Modified: Mon, 10 Nov 2025 21:27:35 GMT  
		Size: 87.8 MB (87842973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77e082f49c597b039679100433085d80354533f9c86f0dc982fb8929bfef520`  
		Last Modified: Mon, 10 Nov 2025 21:28:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251108-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:4f01063450d56f478d721576f341f1fea52f9b6d89de7a9c2da4f21dc2413675
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10331582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61311506e690284cb1af0824d9bcaa7bfed11220c3b26f3b2c4e188f4f8c4ac4`

```dockerfile
```

-	Layers:
	-	`sha256:e2f0d5870308679b4b385081af0bb790a940ea3f15534092d88e0b6482588814`  
		Last Modified: Tue, 11 Nov 2025 00:24:53 GMT  
		Size: 10.3 MB (10303084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a8029dc0748d7bd293b7b27f6fd039e419e06cedbb30a0e42c1d73a53ebb7ba`  
		Last Modified: Tue, 11 Nov 2025 00:24:54 GMT  
		Size: 28.5 KB (28498 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251108-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:9e8a2b1f709189f41fa963db9d30d4820cdfc2ec5ccc9d3e4970f4d387f988a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.7 MB (309720406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1d77f44a65cad122d2e3d93f23f77696e4e807bc9118ea873fe9691c7fbc740`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:30:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:29:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Nov 2025 21:25:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Nov 2025 21:27:09 GMT
ENV GOTOOLCHAIN=local
# Mon, 10 Nov 2025 21:27:09 GMT
ENV GOPATH=/go
# Mon, 10 Nov 2025 21:27:09 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 21:27:09 GMT
COPY /target/ / # buildkit
# Mon, 10 Nov 2025 21:27:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 10 Nov 2025 21:27:12 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b81c3047c0240876c5be21e30ab0bb3930d31a1fc064a5cfe3b73eaec871a74c`  
		Last Modified: Tue, 04 Nov 2025 00:12:55 GMT  
		Size: 48.4 MB (48359478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5463896571d3ff5317461a64229e9e4cb27d6d877114079419cf8b4fc96b0c02`  
		Last Modified: Tue, 04 Nov 2025 00:30:33 GMT  
		Size: 23.6 MB (23598514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:020f0f7f102dcd1ca7603a86d7398adbe5369a820cc6f32954c0b3b5e2ac7403`  
		Last Modified: Tue, 04 Nov 2025 01:30:05 GMT  
		Size: 64.4 MB (64371335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38b1fec3ec2451d2adc75dd1423c967869bdc90b8143b266b4f199c4340ea84`  
		Last Modified: Mon, 10 Nov 2025 21:27:51 GMT  
		Size: 86.5 MB (86472473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdfc394c4671e4765368842b5021bb1bdf0fc1fb8ea3eb886019790f8b58e10a`  
		Last Modified: Mon, 10 Nov 2025 21:27:06 GMT  
		Size: 86.9 MB (86918448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e45425f065452776e10efe7681a4c5ae85693be84b775745ac79149ac90703`  
		Last Modified: Mon, 10 Nov 2025 21:27:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251108-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:d40e42e247141b3f756aa57726bf87f3f51a18e48083ce04773ddc99e0415880
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10552734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:862b2ff50713f008a04e336a83aaa8ea95d545d461fe234de87e12fe1843fb06`

```dockerfile
```

-	Layers:
	-	`sha256:b5fb26ab6f00b1a80a2a0585174a9da540a08e80b98f488aad655e87a8052d7c`  
		Last Modified: Tue, 11 Nov 2025 00:25:03 GMT  
		Size: 10.5 MB (10524212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e6bbb38e68579cf480b59c086e869d4c97158aa22fedd5b7a64a5170624faf6`  
		Last Modified: Tue, 11 Nov 2025 00:25:04 GMT  
		Size: 28.5 KB (28522 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251108-bookworm` - linux; 386

```console
$ docker pull golang@sha256:0d035f21e3065e601923b1ec0f9a9e2885220d58b03751d1210b68e26862f365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.1 MB (320050218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a3c9359aadb3c69ef31814f68b556eacee87c01d0c657bbe8969dc80a334672`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:26:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:31:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Nov 2025 21:26:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Nov 2025 21:28:02 GMT
ENV GOTOOLCHAIN=local
# Mon, 10 Nov 2025 21:28:02 GMT
ENV GOPATH=/go
# Mon, 10 Nov 2025 21:28:02 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 21:28:02 GMT
COPY /target/ / # buildkit
# Mon, 10 Nov 2025 21:28:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 10 Nov 2025 21:28:05 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3a9907ae02a89d2535bb875a11c05038e0be4fa333c35747cd42f6f7b49e018d`  
		Last Modified: Tue, 04 Nov 2025 00:12:58 GMT  
		Size: 49.5 MB (49467114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce6be8e6c76b859a7e1808f7c9de22684a829f5386b5bf2011b85482d4d192f`  
		Last Modified: Tue, 04 Nov 2025 00:26:27 GMT  
		Size: 24.9 MB (24864369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b596182a9b4836dc17a3bc5eadc1e2798b0aa5aa0c8f50fec56b60d802ddb375`  
		Last Modified: Tue, 04 Nov 2025 01:32:07 GMT  
		Size: 66.2 MB (66233815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac7b45ae73050aa28f0c5c64e54314d6a95cdb8610a373ea907cfc16fee139e2`  
		Last Modified: Mon, 10 Nov 2025 21:28:48 GMT  
		Size: 89.8 MB (89823350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6760ff784f4cb90e20d85ded90c45e254a2af1adc9c4a815538370e9b9f35c`  
		Last Modified: Mon, 10 Nov 2025 21:27:48 GMT  
		Size: 89.7 MB (89661412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb69062010d878847b31fe3410541dca5c0c24720d1f4f621b407e697aa27718`  
		Last Modified: Mon, 10 Nov 2025 21:28:36 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251108-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:876a0c8ca07869da2da67dfdaf33b8c8e9a446df8f6c8be5250d1fbbf61dfb80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10504322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a27b9c72654412e8fc30b819f2bdc49673ddcf51a76884da732a47266dc7416`

```dockerfile
```

-	Layers:
	-	`sha256:841da1a1408ba79c7269df6e4791b86cc8e7b5d449f7adfc36c8654f45a63177`  
		Last Modified: Tue, 11 Nov 2025 00:25:13 GMT  
		Size: 10.5 MB (10475969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ac563fc7a449e1af396664322a9a2061a3e5bb436dd87a56eb21b8fb6ec75a2`  
		Last Modified: Tue, 11 Nov 2025 00:25:13 GMT  
		Size: 28.4 KB (28353 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251108-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:bd28ac57ab11e61f3677498b1fd2084672ed17630a6b044c1a48dae2019af93f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.3 MB (291336394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e1259f342c8a975b35d81775160011cddf9bea88680c51477f3a186e464322e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 14:04:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 19:49:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 20:51:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Nov 2025 21:43:35 GMT
ENV GOTOOLCHAIN=local
# Mon, 10 Nov 2025 21:43:35 GMT
ENV GOPATH=/go
# Mon, 10 Nov 2025 21:43:35 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 21:43:35 GMT
COPY /target/ / # buildkit
# Mon, 10 Nov 2025 21:43:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 10 Nov 2025 21:43:54 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:4dda2a1b7438becfe8c22a70ae85ee418f80df0feba9ce91b9ffc92338d47792`  
		Last Modified: Tue, 04 Nov 2025 00:11:16 GMT  
		Size: 48.8 MB (48761282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6492253d4f5d673ee74abc9e254c218714a0737c4c244dcc729821fb543170`  
		Last Modified: Tue, 04 Nov 2025 14:04:51 GMT  
		Size: 23.6 MB (23614047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:305f9457e9c1a9cba16fc581959f009772a1561916f3cc0ea635018606420380`  
		Last Modified: Tue, 04 Nov 2025 19:50:51 GMT  
		Size: 63.3 MB (63309635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96817f9c963b6341e1b5f5447538613cbea1464e6f61848ae7af7c6e1ea82e01`  
		Last Modified: Tue, 04 Nov 2025 20:53:40 GMT  
		Size: 70.0 MB (69997094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1738b2bd40f760f9e3bfd7ea3a19025ac4af989b45b237cc475aab370ad0297d`  
		Last Modified: Mon, 10 Nov 2025 21:46:03 GMT  
		Size: 85.7 MB (85654178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541456e018f1fab4b5adde966d0f1716be906040e7f4f0666cca52adeaf0ce9d`  
		Last Modified: Mon, 10 Nov 2025 21:45:52 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251108-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:d43e2d2d3d47ed9c5e6f11b9c55f013bc2abf656d6e96ea63bcb5a6dde6e0c1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 KB (27124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c893648393fd054df1b8cd614dfe683e684070f973b52118e249ce9139b43a39`

```dockerfile
```

-	Layers:
	-	`sha256:0b8add480aae2ea72a4f355f9e9816dbacd04a0e934f1f22b4a2b89734999858`  
		Last Modified: Tue, 11 Nov 2025 00:25:20 GMT  
		Size: 27.1 KB (27124 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251108-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:d9bf28ef697835f2c70ad432829d6886bf890997ae9d94e66666463943e26bbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.6 MB (326635942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a30229c0670e7d93c0570cf6e1d92e27279a427146725db527e60b9ddab0cfa`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:24:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 06:24:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Nov 2025 22:35:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Nov 2025 22:33:11 GMT
ENV GOTOOLCHAIN=local
# Mon, 10 Nov 2025 22:33:11 GMT
ENV GOPATH=/go
# Mon, 10 Nov 2025 22:33:11 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 22:33:11 GMT
COPY /target/ / # buildkit
# Mon, 10 Nov 2025 22:37:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 10 Nov 2025 22:37:59 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:dcdb26575d996c21e1eb1166ca8252365548a95e0791c754c1a66e3abe07a271`  
		Last Modified: Tue, 04 Nov 2025 00:12:39 GMT  
		Size: 52.3 MB (52327280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a69074b98f99ca928580ca93ef45b80d247ceb89abd2c09f9515ba7ef4ea70`  
		Last Modified: Tue, 04 Nov 2025 00:24:46 GMT  
		Size: 25.7 MB (25672054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:229f89c76b3026966e039b432e1b66b1655c47c97f236438dc626e5acdead5cd`  
		Last Modified: Tue, 04 Nov 2025 06:25:48 GMT  
		Size: 69.8 MB (69845633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:169ad2bb3a7f0ccdd68a9383e27c20afc67c3e94ab263e295a008c5d536fe223`  
		Last Modified: Mon, 10 Nov 2025 22:39:24 GMT  
		Size: 90.4 MB (90417692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f48426cabbc07e67f83c1cda5c24171abce6e81b7fca3ad79e01d21f527b41`  
		Last Modified: Mon, 10 Nov 2025 22:34:40 GMT  
		Size: 88.4 MB (88373126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a67b813aa8eb80ca299d1bf355052ee54c88bcd66ca05f0012988ed549bdbc`  
		Last Modified: Mon, 10 Nov 2025 22:39:08 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251108-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:a7e7045853d7e15ab8580ba4fbc022193dcb081c95dd625159a1d82186b3d35d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10497303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e9af78d0ccda1f2d67e7023d601e3309f58bb7c2dcaa89d1e5b6f1371bacf0d`

```dockerfile
```

-	Layers:
	-	`sha256:45a613557978a1e4544bf5b9624d8b13da8ae8c332d003677a442e093ba128be`  
		Last Modified: Tue, 11 Nov 2025 00:25:26 GMT  
		Size: 10.5 MB (10468871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a7fd430c50b05c3d93fab66837a47928940e3aa75e8e202dd68ae0919cd94ae`  
		Last Modified: Tue, 11 Nov 2025 00:25:26 GMT  
		Size: 28.4 KB (28432 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251108-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:b93e897caacbb3d9d2436d40a8ff2713299ec32c63129535edd1126493edec3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.6 MB (293563271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d17408d104d5998f67daf0f8707fadd99d04517796eab2c1f487f9712569fe`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 03:16:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 09:59:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Nov 2025 23:08:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Nov 2025 23:05:52 GMT
ENV GOTOOLCHAIN=local
# Mon, 10 Nov 2025 23:05:52 GMT
ENV GOPATH=/go
# Mon, 10 Nov 2025 23:05:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 23:05:52 GMT
COPY /target/ / # buildkit
# Mon, 10 Nov 2025 23:11:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 10 Nov 2025 23:11:12 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0a071bbc557d9d42732d58a1d6434bf94baf5f06b391c076c996395c193e41bf`  
		Last Modified: Tue, 04 Nov 2025 00:12:11 GMT  
		Size: 47.1 MB (47138093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a580bca43f6d623617841d967d82ecc7cf55ebeb22ce79064b23dd0b4a10ce0`  
		Last Modified: Tue, 04 Nov 2025 03:16:55 GMT  
		Size: 24.0 MB (24027417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaba91dbdb50f511980482385b36987be0332dae93638fc6697a70724b1e1e5c`  
		Last Modified: Tue, 04 Nov 2025 10:00:10 GMT  
		Size: 63.5 MB (63501365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce15e774ad3bada7dd910f12a50bd8367d0c5aeda4e6908b556b92bcb6f5e4c5`  
		Last Modified: Mon, 10 Nov 2025 23:12:13 GMT  
		Size: 69.0 MB (69006948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e64f47020d1f3aeb3d5d5264472a9b269aff1c59728387c987b54097fe8c0fe`  
		Last Modified: Mon, 10 Nov 2025 23:07:54 GMT  
		Size: 89.9 MB (89889290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a922706880d77907b1a3b10e207480a2de9671c4dbefafc1e495d4410a9e3f64`  
		Last Modified: Mon, 10 Nov 2025 23:11:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251108-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:46840d0488e7c760c539c2403f62b2968634026e3eb130130e61342f12932504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10356532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf5c3847df40c754845c52daa5f67491b7dde690d3ee8f61cc1a772836cff914`

```dockerfile
```

-	Layers:
	-	`sha256:2731c54331e8d4647bbc0625b95b044e17f82e2186808b3c1a5e0b1d75e721be`  
		Last Modified: Tue, 11 Nov 2025 00:25:34 GMT  
		Size: 10.3 MB (10328146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55d9fb605bacffbbf8f47bb31f5f476b90b30e46b1b644eb528d3a03c9105a34`  
		Last Modified: Tue, 11 Nov 2025 00:25:35 GMT  
		Size: 28.4 KB (28386 bytes)  
		MIME: application/vnd.in-toto+json
