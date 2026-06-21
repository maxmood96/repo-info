## `golang:tip-alpine3.23`

```console
$ docker pull golang@sha256:72f934705908ab2f1755f453088ccb1474ef799b6a8b002115427e3fac887cea
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `golang:tip-alpine3.23` - linux; amd64

```console
$ docker pull golang@sha256:4e6f8bea2e3535e4971f1fb9dbf9aba5f6bca18a9dad86c59e05a3b2d6a6781b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.3 MB (106259197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5516b0b7012269c5d9bfb21be32a7a8c88cfb3ec0aa649dab8bf78ba18fe535b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2026 23:29:43 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 15 Jun 2026 23:29:04 GMT
ENV GOTOOLCHAIN=local
# Mon, 15 Jun 2026 23:29:04 GMT
ENV GOPATH=/go
# Mon, 15 Jun 2026 23:29:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2026 23:29:04 GMT
COPY /target/ / # buildkit
# Mon, 15 Jun 2026 23:31:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 15 Jun 2026 23:31:53 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed4cfe03586436ef332cc8fbe663987503b5e69c45dc0135f401ecf8d0c7971`  
		Last Modified: Mon, 15 Jun 2026 23:32:01 GMT  
		Size: 290.2 KB (290242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f299e0e3bd5e6acb73b7c4b5cab40f1e2dfe3ddb2a4bbbe05ceba99d84f0fdf`  
		Last Modified: Mon, 15 Jun 2026 23:29:20 GMT  
		Size: 102.1 MB (102104608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e0b12436dbbd6d3337138862919dc8117793c6ea7cc1c8424d0e668fa53686`  
		Last Modified: Mon, 15 Jun 2026 23:32:01 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:6b877696135010eebb356b298b58b7a9028edeac6b86705e4892f4cfb668c39a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.5 KB (217487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2542276694a61e7b6d631d57cc70b437ae9ba423a4de551ac997aedfd1876ec3`

```dockerfile
```

-	Layers:
	-	`sha256:3157a2ecc5924b43f292984b79766286b3fc6dc8a22b6c99e9fa2b528d8dc218`  
		Last Modified: Mon, 15 Jun 2026 23:32:01 GMT  
		Size: 193.0 KB (193018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b693e5ec33c8f616c509a8a6e442f045fb5d08362ab54187c5d9b22c6b6e08a4`  
		Last Modified: Mon, 15 Jun 2026 23:32:00 GMT  
		Size: 24.5 KB (24469 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.23` - linux; arm variant v6

```console
$ docker pull golang@sha256:bed442a481b1327cbc8bc3d3e16d4019b3d7cbc0a11aaa693ad3e4358c2adc41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.0 MB (102006303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43b11fc1fbe24b2b468604af9c96222adbd9689bac68e1789b99f1051accea30`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2026 23:22:06 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 15 Jun 2026 23:25:11 GMT
ENV GOTOOLCHAIN=local
# Mon, 15 Jun 2026 23:25:11 GMT
ENV GOPATH=/go
# Mon, 15 Jun 2026 23:25:11 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2026 23:25:11 GMT
COPY /target/ / # buildkit
# Mon, 15 Jun 2026 23:25:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 15 Jun 2026 23:25:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1579ac7741cb0cd6799da57cb7ce998907a2a6bfc26b34410bab5380ed283134`  
		Last Modified: Mon, 15 Jun 2026 23:25:26 GMT  
		Size: 291.0 KB (291023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7348edabd82bf14cb4cd059795ea4686f60d5bc93e843f47bf9e71da8ef5c5`  
		Last Modified: Mon, 15 Jun 2026 23:25:28 GMT  
		Size: 98.1 MB (98143261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3771c2201905311eb5f975489e6eeeb9cc931b014d7cf4ed305795e6f7fadb`  
		Last Modified: Mon, 15 Jun 2026 23:25:26 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:c8ba72fec20d6ede9619d8093344ead811a9b6028930828a4860c20af553a997
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 KB (24362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b3a524dae9ea82ce495a40fd4fefb5b883f889df74874e764b87a46240b2e0c`

```dockerfile
```

-	Layers:
	-	`sha256:a02396b5fa341b0ba2790cd41829ddb521ef509f2fd79574639d43286298e8be`  
		Last Modified: Mon, 15 Jun 2026 23:25:25 GMT  
		Size: 24.4 KB (24362 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.23` - linux; arm variant v7

```console
$ docker pull golang@sha256:5ebc2643170aded1d53424a98dc9286337c65d7567b32a89d65bd4f709fd2d16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.4 MB (101409637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4552c35f4ceb3d6890bcc058e880ebffac4dfaeb511b7bd4038201c4d07adb40`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2026 23:25:54 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 15 Jun 2026 23:28:58 GMT
ENV GOTOOLCHAIN=local
# Mon, 15 Jun 2026 23:28:58 GMT
ENV GOPATH=/go
# Mon, 15 Jun 2026 23:28:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2026 23:28:58 GMT
COPY /target/ / # buildkit
# Mon, 15 Jun 2026 23:29:01 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 15 Jun 2026 23:29:01 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855eebcfef508c160873ae802ef7f77d21c748d3a02ca5e81f8a322758d75998`  
		Last Modified: Mon, 15 Jun 2026 23:29:17 GMT  
		Size: 290.2 KB (290176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f3afb2b46cd31bb80c259a8638a98ac035a8bd800ea0d4d4395dd90003ea00`  
		Last Modified: Mon, 15 Jun 2026 23:27:30 GMT  
		Size: 97.8 MB (97836180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c470351abc8e28af78ba273bc39556c6adbbfe0ce1bbd07d0a7ad747ef09bd`  
		Last Modified: Mon, 15 Jun 2026 23:29:17 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:75f66e726ca5c07c412ffcb4df7633bdad1f40936b5866b58f554ee2a80da279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.9 KB (216949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ad4028ccd8d1d8d688de53713b947e49cc3373a23c998b7f6c0b1f14532b7a2`

```dockerfile
```

-	Layers:
	-	`sha256:efd5c6f3a04e81c4393104fa6a0c6028ab5ab9f0f2800ec9fc476c0f4837cb76`  
		Last Modified: Mon, 15 Jun 2026 23:29:17 GMT  
		Size: 192.4 KB (192372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcc3fd3cc893c0de7443568d9c76039a2350542efa09ca47066dda5ec399907b`  
		Last Modified: Mon, 15 Jun 2026 23:29:17 GMT  
		Size: 24.6 KB (24577 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:33a580d56ec8d45910fa302fd6372753956f15cc7e13f0ccbf5015acd4c4ba2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.0 MB (101038909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be42d254e4a5974edb8b27339f2d04b158f529144152b3a16ba8dd33ffedc064`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2026 23:24:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 15 Jun 2026 23:26:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 15 Jun 2026 23:26:20 GMT
ENV GOPATH=/go
# Mon, 15 Jun 2026 23:26:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2026 23:26:20 GMT
COPY /target/ / # buildkit
# Mon, 15 Jun 2026 23:26:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 15 Jun 2026 23:26:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77e8de4a86a3f66a63a97c66c8b1b060c220e56e18f5258cf5f4a9e046fd336`  
		Last Modified: Mon, 15 Jun 2026 23:26:38 GMT  
		Size: 292.9 KB (292856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecdc6f594300f89ac123e28e6396b82aeb7db11414dbbf3d120d335b23be9022`  
		Last Modified: Mon, 15 Jun 2026 23:26:34 GMT  
		Size: 96.5 MB (96546025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0cd0c865d8f9fc35349499eceb1a756a3e93b74ba17e66afb98962d3f82216`  
		Last Modified: Mon, 15 Jun 2026 23:26:38 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:7da5805eb07b5472f3fe3cbc7a291241efd82151708ac3b33ba56d4fa60d76f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.0 KB (217001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9650eba49d3cfedf34533ce0f1cf3df77daa1f11bac29400460982f012d0ef93`

```dockerfile
```

-	Layers:
	-	`sha256:9f0574447859df09b9380c4f0ccc032df5f499963b7957e3dd7f648e0cc8e743`  
		Last Modified: Mon, 15 Jun 2026 23:26:38 GMT  
		Size: 192.4 KB (192400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:487145946a8671bb68e16f34bb8fde0a7db47f5a8b7e9116357b1a9299fd0d4e`  
		Last Modified: Mon, 15 Jun 2026 23:26:38 GMT  
		Size: 24.6 KB (24601 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.23` - linux; 386

```console
$ docker pull golang@sha256:cfd1ea7c73fcc706315b2a70d5e3eb5130ce23019f32646af8f0dfc954c4c601
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.9 MB (103856380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13b48eba366e2cb9002a5e4f514745fc32607b26de6bd4770922bf832abe3adf`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2026 23:25:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 15 Jun 2026 23:24:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 15 Jun 2026 23:24:24 GMT
ENV GOPATH=/go
# Mon, 15 Jun 2026 23:24:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2026 23:24:24 GMT
COPY /target/ / # buildkit
# Mon, 15 Jun 2026 23:27:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 15 Jun 2026 23:27:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba89734a71650643bb077ddd31817a46891664cfc67262e442b5afc6c2e05a2`  
		Last Modified: Mon, 15 Jun 2026 23:27:37 GMT  
		Size: 290.6 KB (290634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1792fe3654cd71494db1238d388e796cd8a11c55f4bdc3626b4c71f43b9583c8`  
		Last Modified: Mon, 15 Jun 2026 23:24:36 GMT  
		Size: 99.9 MB (99875141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aed2f76f2b438dfaa541405849a9259b409b12e5decbf31adf5a3399b16018d`  
		Last Modified: Mon, 15 Jun 2026 23:27:37 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:77f99d43cb68484323772e90b4c73b117ac479dd30b2404b4f5516bc04da12b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.4 KB (217419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85c9f54d64847213ea23841e2ed2d6f9ca482ec50d34c672748623bba66b2f24`

```dockerfile
```

-	Layers:
	-	`sha256:8b69777e6ff54b5695ee76f91dfccfbb771ece5f6343f21f98659043dda64888`  
		Last Modified: Mon, 15 Jun 2026 23:27:37 GMT  
		Size: 193.0 KB (192987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:929007f1d1956fc4febbe90807bb9986f161aaaa76849b31f9925cc217fe9e81`  
		Last Modified: Mon, 15 Jun 2026 23:27:37 GMT  
		Size: 24.4 KB (24432 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.23` - linux; ppc64le

```console
$ docker pull golang@sha256:88f02cdcb5d5fb633c1c71cc6883cd6be196f7661b7def0a8c34d1e6d924046e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.6 MB (102623956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a61a21db416faa51aee5753728267c8198c6fd5e6ffa97629fe0f0849dd39411`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 16:47:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 15 Jun 2026 23:35:08 GMT
ENV GOTOOLCHAIN=local
# Mon, 15 Jun 2026 23:35:08 GMT
ENV GOPATH=/go
# Mon, 15 Jun 2026 23:35:08 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2026 23:35:08 GMT
COPY /target/ / # buildkit
# Mon, 15 Jun 2026 23:40:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 15 Jun 2026 23:40:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77dfc45c5906cb105fa1bde6a534e8e48deced0c4556f99056c2f76204caa5c2`  
		Last Modified: Tue, 02 Jun 2026 16:47:39 GMT  
		Size: 293.4 KB (293393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f89039b34d27b51562a15e0375b32ce61f3263152969c65f76567c3ed39aa8a9`  
		Last Modified: Mon, 15 Jun 2026 23:36:20 GMT  
		Size: 98.5 MB (98499477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1894ba4f3a36482ba26c63087fba31112a473471f9b965ab58153cf85e57a8`  
		Last Modified: Mon, 15 Jun 2026 23:40:46 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:149ba8de411f9d860ab831de40601be5cc348345fa7bf79eb3e54c9bd254e66c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.7 KB (216742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ba3d20632272d066bad3e7cc8d9ccba7576f756b2fcf03295fe41abec38a1b7`

```dockerfile
```

-	Layers:
	-	`sha256:43cf9416e47ee65a83f92791d56643d87fda129afbc7c3014fa64d401299c021`  
		Last Modified: Mon, 15 Jun 2026 23:40:46 GMT  
		Size: 192.4 KB (192405 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9266e1b6b108891a632c2fb72f11d6b0e95c0b5b6934f7ab66652cd1da4cb493`  
		Last Modified: Mon, 15 Jun 2026 23:40:46 GMT  
		Size: 24.3 KB (24337 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.23` - linux; riscv64

```console
$ docker pull golang@sha256:fc2e6f2c4e4597942df69c72746017f0bd631f37a37d3d660764e3e7acb18d83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.3 MB (103303060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d973965110e8e28ddb05f3684cf96c94258fe688e9a855ed26ae47f6f976a888`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2026 16:18:44 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 16 Jun 2026 06:42:10 GMT
ENV GOTOOLCHAIN=local
# Tue, 16 Jun 2026 06:42:10 GMT
ENV GOPATH=/go
# Tue, 16 Jun 2026 06:42:10 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 06:42:10 GMT
COPY /target/ / # buildkit
# Sat, 20 Jun 2026 20:43:33 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Sat, 20 Jun 2026 20:43:33 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3257359d78e33ee12c186b4248dac6627cb8e26d6fd747ad8f46ed2b4fb8e1`  
		Last Modified: Thu, 16 Apr 2026 16:19:53 GMT  
		Size: 290.6 KB (290553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7dbe4000f17519e4596fa5552054546772fb32ed45b8efd349e760fdf7b0b1f`  
		Last Modified: Tue, 16 Jun 2026 06:49:17 GMT  
		Size: 99.4 MB (99424689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fae6a539de4737d28660d7d5796e2edac12d409e21a0f90a1b43db5c9f2ef05`  
		Last Modified: Sat, 20 Jun 2026 20:44:51 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:d4e0ac4d8f6c05ff6488d9faa790ff26674f1bc2a3bdb1f65a86c94c95f21921
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.9 KB (216912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81438a3e012cb0bfc330eb5b07d2a41dbd79f1f845aa66377ed7fcad1c51bb1c`

```dockerfile
```

-	Layers:
	-	`sha256:2aad3509b9918d09fd7f08c31113f2ee51b920b8020581d26baccc285b49a62f`  
		Last Modified: Sat, 20 Jun 2026 20:44:52 GMT  
		Size: 192.4 KB (192401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af412b89472bd743021402bcca717511727f382c1977aff785c28cdc8b118b63`  
		Last Modified: Sat, 20 Jun 2026 20:44:52 GMT  
		Size: 24.5 KB (24511 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.23` - linux; s390x

```console
$ docker pull golang@sha256:a317e0d3c16defeee4d49bfd7b88760fcca84bf89c4f67eec8d7fd96072bfadc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104571603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ea18d39bd020063aab4ce965faaa8654fb4d5ad5f6fe4a7574a2ea95de7cb54`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2026 23:19:31 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 15 Jun 2026 23:23:59 GMT
ENV GOTOOLCHAIN=local
# Mon, 15 Jun 2026 23:23:59 GMT
ENV GOPATH=/go
# Mon, 15 Jun 2026 23:23:59 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2026 23:23:59 GMT
COPY /target/ / # buildkit
# Mon, 15 Jun 2026 23:24:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 15 Jun 2026 23:24:12 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77b3cbbbacd79703b76753144e4ab92538aafc451b67ab51d5a4288335025f4`  
		Last Modified: Mon, 15 Jun 2026 23:24:37 GMT  
		Size: 291.2 KB (291156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0ac3a6fe312cf44641985605a72c55cfb44387624bfcf4ae9738ab565d3ad9`  
		Last Modified: Mon, 15 Jun 2026 23:24:39 GMT  
		Size: 100.6 MB (100553757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb2ff2f51f0ecaa382a90a5a5676e1320d14fe18c970d6e512bec34972c0649`  
		Last Modified: Mon, 15 Jun 2026 23:24:37 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:207a274da22e10e49bfcdecf8957018eec3b4794acd94bbb95fb57bd65164999
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.4 KB (217410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeca937045914150504b0f98c80460310acaf455f96b7c75ba0aed4db3dae352`

```dockerfile
```

-	Layers:
	-	`sha256:417d539b948e965cc8bda8b1374cd2e4826a869f72b3630e6093372acb7aea4f`  
		Last Modified: Mon, 15 Jun 2026 23:24:37 GMT  
		Size: 193.1 KB (193115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86f4e270bd0fefdfc3b8edbcd10712444cf855a0adb2c3a414740c961866a516`  
		Last Modified: Mon, 15 Jun 2026 23:24:36 GMT  
		Size: 24.3 KB (24295 bytes)  
		MIME: application/vnd.in-toto+json
