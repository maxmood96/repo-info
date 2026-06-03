## `golang:tip-20260530-bookworm`

```console
$ docker pull golang@sha256:535271600eed5acff9c426e9ad7d9aabe0d1632adbb90bbe23624c9352eb9164
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

### `golang:tip-20260530-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:23760d9f005957e9575d1607e93b0ca7d0943b3f5a4e412e906e756e6b4f07e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.4 MB (331426576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfccba4b9dd6a3d6d29c2c30d9166b28bd0fb43aed94c8bd113bc592e5ca5c50`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:23:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:26:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 22:11:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 22:13:08 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 22:13:08 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 22:13:08 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 22:13:08 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 22:13:11 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 22:13:11 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:4887723d153cfd7fd9e356c8730311c36a64e4f9329f9d3ae1929e05715f2e73`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 48.5 MB (48495432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e51c50554dce9c9549d76c40bfea45780a8342aea81ba8b270ba1bf46a2aec5`  
		Last Modified: Tue, 19 May 2026 23:23:20 GMT  
		Size: 24.0 MB (24043374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a234579dfb0d2a4c7e869bc6c39c06f306aa019f90ec3e79f682671badaeb4f3`  
		Last Modified: Wed, 20 May 2026 00:26:20 GMT  
		Size: 64.4 MB (64404451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661469ac6453c54c2e44d28e7ed9ea64020f91b2f0322a8b23cf94c80a06efc7`  
		Last Modified: Tue, 02 Jun 2026 22:13:38 GMT  
		Size: 92.5 MB (92480999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23f29da6194068cf9bcb9d5261ce3db2ba9613e69bf068059cae42650df5c10`  
		Last Modified: Tue, 02 Jun 2026 16:41:24 GMT  
		Size: 102.0 MB (102002162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae23d8a856dc34b76778d000535d54002952a1a05d364092046fa3db0d67386`  
		Last Modified: Tue, 02 Jun 2026 22:13:35 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260530-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:82718947bdc1c60a7a64cc96aef8495ecf3a1643f6b7041138f0266cdf67aaa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10525445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5978d3288eadff30a793a8aa365663ad630e8b6c0089947f509401cc7850f3f`

```dockerfile
```

-	Layers:
	-	`sha256:47ae5b79eb32fdaa640c12a5ff6094a7476e969b16f957af5a889cbb42932f67`  
		Last Modified: Tue, 02 Jun 2026 22:13:35 GMT  
		Size: 10.5 MB (10497055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:566be07be14e663dbf0e9fbd9a747447172d0d9f91895b81ddfc09ab49fed700`  
		Last Modified: Tue, 02 Jun 2026 22:13:35 GMT  
		Size: 28.4 KB (28390 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260530-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:51cd4e4eb81111d8981da32445ea143b195769a31d02c8a6a24aba2cc65e0cb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289875287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89ab90de5856befff158993f333a8d7423c39e1c1c7facc9f9fc27c25be519fd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:02:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 01:33:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 22:09:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 22:12:09 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 22:12:09 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 22:12:09 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 22:12:09 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 22:12:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 22:12:12 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1af0b8b84389f4347663cc563bc1f6d59fe6d6f21081f428bafa1a09f6a276ce`  
		Last Modified: Tue, 19 May 2026 22:35:59 GMT  
		Size: 44.2 MB (44209154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a61246c0a5a0fe9fe8cdc1bfde0fdfa49ffafcc94cba31f4aecc0c34bc346064`  
		Last Modified: Wed, 20 May 2026 00:02:11 GMT  
		Size: 22.0 MB (21950133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56a54e4354794da97ac9fe5173f689d775d13afa792e8b390e49425c3caa6b5`  
		Last Modified: Wed, 20 May 2026 01:34:11 GMT  
		Size: 59.7 MB (59661818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6266089cad391c14c7fe8d8b5e69ff985f365c65554430dfb4862f12854bfe72`  
		Last Modified: Tue, 02 Jun 2026 22:12:37 GMT  
		Size: 66.3 MB (66338968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c820ebe5b5536b95e87912c5dc1f2663a3e9f184b88c7a174fffa610cef8238c`  
		Last Modified: Tue, 02 Jun 2026 16:42:07 GMT  
		Size: 97.7 MB (97715056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e890041bda4f91871b5d9b81173cdb0fcdafb50d170462876644d50f518e5a`  
		Last Modified: Tue, 02 Jun 2026 22:12:35 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260530-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:3fcac3aff16c00a65e6da36ba7609144cc498236ab1c555e0819816791a3a90c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10332249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d69d6a59d087d20a8dd6ed266bca8d03a21ec1f34bb025455d16fa4327a07ce`

```dockerfile
```

-	Layers:
	-	`sha256:94cadf792ba308e680e6077712c6452569e68c2ccfad1174b56afb8e64ea4c32`  
		Last Modified: Tue, 02 Jun 2026 22:12:35 GMT  
		Size: 10.3 MB (10303751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c52be411b09e8fea658856c4f032b45b2a6e2c5c3554fa75f2f067306122bb6f`  
		Last Modified: Tue, 02 Jun 2026 22:12:34 GMT  
		Size: 28.5 KB (28498 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260530-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:a7aeca8cda3971964c56b80be0544381601f1823f7e49c78841ca3d5e0906b82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.5 MB (319469778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a094622085442a7d4f5f0109f8b75cdb6638a5890688120a9935d59ad038225c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:26:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:26:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 22:10:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 22:12:34 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 22:12:34 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 22:12:34 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 22:12:34 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 22:12:37 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 22:12:37 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1fbcdab7270278c1f989ae72190255d85d2117e990efb76cde6eb206b803672c`  
		Last Modified: Tue, 19 May 2026 22:36:02 GMT  
		Size: 48.4 MB (48379432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3daebbc198bd7b84bdd72840d7f4ded251896f03b9a9f880894e95e926bc543`  
		Last Modified: Tue, 19 May 2026 23:26:38 GMT  
		Size: 23.6 MB (23613394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c669ec0346d48159cb837d6257098593cd53e61de677d9c0426474d36e1c5e`  
		Last Modified: Wed, 20 May 2026 00:27:16 GMT  
		Size: 64.5 MB (64487655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0521d35ecb06f5022abcb2e865919e95a9b6e0122a5ae8fee676bbe312466dc4`  
		Last Modified: Tue, 02 Jun 2026 22:13:03 GMT  
		Size: 86.6 MB (86554557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15ffb09d61853e3fb3628a4cb3b2d395b59e27aec015f8f1626a8b2ce9bb2f2`  
		Last Modified: Tue, 02 Jun 2026 16:41:30 GMT  
		Size: 96.4 MB (96434582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d80a19ddea9255babe68b3f60603e1f0de17645b48e9d84d1ce97e6a3e73a58c`  
		Last Modified: Tue, 02 Jun 2026 22:13:01 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260530-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:a13710275e71cdb1688c4ae2fd23982d69092c730bc567b7f2ff3ad2ae02192d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10553400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0119ab140a70ef4ade77b755601782c23bef52081d914033438a635afbb91bd9`

```dockerfile
```

-	Layers:
	-	`sha256:f4edace082ae6e9bea7e49ac50798c924935277788a67c27a2f3fb2f38a4fb45`  
		Last Modified: Tue, 02 Jun 2026 22:13:01 GMT  
		Size: 10.5 MB (10524879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92ac2b837f649db8750e4a88905f02d613a35d233d291e4661c9f75e4c1057fb`  
		Last Modified: Tue, 02 Jun 2026 22:13:01 GMT  
		Size: 28.5 KB (28521 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260530-bookworm` - linux; 386

```console
$ docker pull golang@sha256:170d9042d08cc5074e3daf938cd41d7b621ba4fb22f453e661a6653e992515e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.3 MB (330280129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bc4814c8e55370e363f0da7f0a431762954b463e226d1148fb4611054ed0f59`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:24:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 02:44:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 22:11:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 22:14:07 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 22:14:07 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 22:14:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 22:14:07 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 22:14:10 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 22:14:10 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:8bf11fb6e89cfb8d682f511fb7d1b795e747af9c12a192f45f6e50ae7ca54f50`  
		Last Modified: Tue, 19 May 2026 22:36:20 GMT  
		Size: 49.5 MB (49483120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db105b3a1c2456422c428304ae93436fac4214751cb65053af119fa6d81d85dd`  
		Last Modified: Tue, 19 May 2026 23:24:59 GMT  
		Size: 24.9 MB (24879482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9e2a05321daf588afd8b06b380f7ea0a3d7c0de2097ec6f355a74453e7ec6af`  
		Last Modified: Wed, 20 May 2026 02:45:13 GMT  
		Size: 66.2 MB (66243865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5764ce16551b42ce463330e94228c7690ef2e5d44757337ed5f81e0877a78502`  
		Last Modified: Tue, 02 Jun 2026 22:14:35 GMT  
		Size: 89.9 MB (89903975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f630b89f59dc6a4b85d53c6ab2696f0b52ea5d937a0bd9344e6c06fc5883a6`  
		Last Modified: Tue, 02 Jun 2026 16:42:33 GMT  
		Size: 99.8 MB (99769529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1c0bfb8d5cab4acf731f972f8b6e39035d75e433084e15fea96e48c6736936`  
		Last Modified: Tue, 02 Jun 2026 22:14:33 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260530-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:ed33e81f3c66ee9d8a362f9e849d1ff6a9a7106eaf4dbe3e8bb127200155daed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10504988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:824c7ccc41c35f61a67ffb329a77b5da2b12cc80207aef034dcee807defb61fe`

```dockerfile
```

-	Layers:
	-	`sha256:3709541337def8c3450ee5e4a0479a2bb280c932b55462c636f2e029eb13b909`  
		Last Modified: Tue, 02 Jun 2026 22:14:34 GMT  
		Size: 10.5 MB (10476635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cecc4a5de1507542206bdb1a786b016c688cc30baba9c7d9b186ed9d0e661758`  
		Last Modified: Tue, 02 Jun 2026 22:14:33 GMT  
		Size: 28.4 KB (28353 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260530-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:1e60bdc08a8180cc2d2fc656cac8e50f6ff9d323170396feece139ce41051f02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.2 MB (301203889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a93525eadef79c5fdbcdddd9716424d876f0c1790becf3c468e24d4b3694ffc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 10:04:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 15:11:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 16:19:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 17:02:47 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 17:02:47 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 17:02:47 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 17:02:47 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 17:03:02 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 17:03:04 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:813eaff938e8991b3dd16851af2c46dd2ffc5bb600e30ff866dd5a60502fbffa`  
		Last Modified: Tue, 19 May 2026 22:35:13 GMT  
		Size: 48.8 MB (48786239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2853b2ecd2cc91271c3528597da43fc45c41515894834d1de212a390afbf0ade`  
		Last Modified: Wed, 20 May 2026 10:05:32 GMT  
		Size: 23.6 MB (23621201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71bf4bd887b67ee95b1804bd893717310da36bddd5a598cce7e9b621ff52ee05`  
		Last Modified: Wed, 20 May 2026 15:12:43 GMT  
		Size: 63.3 MB (63316337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2d8edfd178bcf28b946d64eb3ad538d4ee96dacac854fd44ba3af295e68b368`  
		Last Modified: Wed, 20 May 2026 16:21:18 GMT  
		Size: 70.1 MB (70084514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:148b142c54d1b941c7d66610cd7d81d650defd945cece98d1cf8e78c64810a19`  
		Last Modified: Tue, 02 Jun 2026 17:05:09 GMT  
		Size: 95.4 MB (95395440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6b083f3b10354ecd6706af3be6a7c925f39002aba5104f12f55c91d99df3c4`  
		Last Modified: Tue, 02 Jun 2026 17:04:59 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260530-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:c28448a5bcabe2aa7f77e48cfcec1098f2686350383ea07a806bec34b233bcaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.2 KB (28240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5bcab44376a376e1dc74fe6ff52bc92919e5c1a68039b3bcfac237a38303d4a`

```dockerfile
```

-	Layers:
	-	`sha256:48cb1b66f6c28c634346d1c08fd52f9bdfc7a1edd9d46ba4e5136128314c65c6`  
		Last Modified: Tue, 02 Jun 2026 22:35:48 GMT  
		Size: 28.2 KB (28240 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260530-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:879a4e5e3912cd453fe2e9fbf46a94d19e87daae7475de781ad59504690a1740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.8 MB (336763049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3364976da63edea22dd3ef69e70be7b872b4a542835da5517d9d32c9a1f2f2a9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 01:13:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 06:50:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 16:42:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 16:41:50 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 16:41:50 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 16:41:50 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 16:41:50 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 16:42:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 16:42:16 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b3943e183051423c3dc79fa53ad6d50fff9621945bbfc636eec039b14ead2b66`  
		Last Modified: Tue, 19 May 2026 22:35:10 GMT  
		Size: 52.3 MB (52340199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f46c910cb3dd366a8b080c77b15459d7465da54412b3570454cddcaf0cdf40`  
		Last Modified: Wed, 20 May 2026 01:13:39 GMT  
		Size: 25.7 MB (25686466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67cb71cd5984ee53ab56bef57a29d3b0ef6e8939c352146b1efe66402d4c7ff`  
		Last Modified: Wed, 20 May 2026 06:51:27 GMT  
		Size: 69.9 MB (69853485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0548bbd70587587ebc4a21c63b5f4bd00f3fc220c1a3dc53c1a1b9debf81aa66`  
		Last Modified: Tue, 02 Jun 2026 16:43:17 GMT  
		Size: 90.5 MB (90495650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a76d2265265ac98a5752cfbf5ed880207c013050351547f0c225cf8c995ca0`  
		Last Modified: Tue, 02 Jun 2026 16:43:17 GMT  
		Size: 98.4 MB (98387092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0c71357c78f0cd543af45505a0c076218de1899f138e814aa5b496421765b2`  
		Last Modified: Tue, 02 Jun 2026 16:43:13 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260530-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:d462f8023ac2ff6c802250314ad6270131de69cc3d3103a18f82b45904bb62af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10497971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed33096086c684a59fa04ffb654ddc19be2c836cc40fb7d37cefb154c2977607`

```dockerfile
```

-	Layers:
	-	`sha256:05552bf3c16627ec7b02976fa7ef7a7ae52146a2ac0930aa1145dd3e9b9c8665`  
		Last Modified: Tue, 02 Jun 2026 22:14:11 GMT  
		Size: 10.5 MB (10469540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83685ca79044f121f4088e3b8eabf74324507f6bc4f1dc7fd37f743d183aae90`  
		Last Modified: Tue, 02 Jun 2026 22:14:11 GMT  
		Size: 28.4 KB (28431 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260530-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:b9fac94c52a217f7cd0cdf9ce6d96cab79f970e440dab093117f0fc11cd80675
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.2 MB (304234923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0694092e2892aa67e4937401bae8e59f5aa4d8b427600889bdec39ce8624168c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:17:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 02:05:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 16:42:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 16:41:57 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 16:41:57 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 16:41:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 16:41:57 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 16:42:09 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 16:42:10 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e0fc2c7a6bb12f7a9b333cc117b6ea5fa5cf251c5fa4dd298303beee01028f59`  
		Last Modified: Tue, 19 May 2026 22:35:39 GMT  
		Size: 47.2 MB (47155589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79feab17202415ba0b431eca0e903b1c895e662e755c4c9f1b5678ad8eb605f`  
		Last Modified: Wed, 20 May 2026 00:18:12 GMT  
		Size: 24.0 MB (24039201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:511ade0407a6db3c4a6853a735563e5fb22577aaaa32942a9458cc0c09942583`  
		Last Modified: Wed, 20 May 2026 02:05:37 GMT  
		Size: 63.5 MB (63498321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f90b46dcc8622719e19e9e04b1bcb5bc39309966d69636e349c233ba832e30`  
		Last Modified: Tue, 02 Jun 2026 16:42:45 GMT  
		Size: 69.1 MB (69088003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca767cc33ca0e2036ed1bd1b9a5ecdd963a3598306969640db0e92025a10887`  
		Last Modified: Tue, 02 Jun 2026 16:42:28 GMT  
		Size: 100.5 MB (100453651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b23dbe836c3f55f02add78bfdd7b4bfc8403faa6dd93ed0015a3ddb579acb6aa`  
		Last Modified: Tue, 02 Jun 2026 16:42:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260530-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:a91e68785be9042bdef25d68399399f07b6b9ba86e6630080a310cd022987069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10357950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a64bb64ea198528448737e294c55733691c14896c1c1ffbb0fe86e0f67fe94ce`

```dockerfile
```

-	Layers:
	-	`sha256:b411f221ae07b0cd3ff1277f7fbf4b6545af8ba76c801e4cdb6239b99c849015`  
		Last Modified: Tue, 02 Jun 2026 22:13:45 GMT  
		Size: 10.3 MB (10329561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52c1fbbbfc0fa8f1502b507c5d5f5d7768d86a297bc5e9dcead35f6dc056315b`  
		Last Modified: Tue, 02 Jun 2026 22:13:45 GMT  
		Size: 28.4 KB (28389 bytes)  
		MIME: application/vnd.in-toto+json
