## `golang:latest`

```console
$ docker pull golang@sha256:a0679accac8685cc5389bd2298e045e570100940e6bdcca666a8ca7b32a1276c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
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
	-	windows version 10.0.20348.2527; amd64
	-	windows version 10.0.17763.5936; amd64

### `golang:latest` - linux; amd64

```console
$ docker pull golang@sha256:1d595b28cc70e922f4e35537d05537ae4d7f38459a9a5d80c6706d38a69a9862
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.3 MB (299317648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75192a99ad97136bd4ad98a32969041352c44c7936384d8ccd40cf22e19f8d58`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jun 2024 19:06:26 GMT
ADD file:b532f8e401e9a1fcc2ea1fc034adf820a5269c6ace45769f60a81fcb673f01b8 in / 
# Tue, 04 Jun 2024 19:06:26 GMT
CMD ["bash"]
# Tue, 04 Jun 2024 19:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jun 2024 19:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jun 2024 19:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOLANG_VERSION=1.22.4
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOPATH=/go
# Tue, 04 Jun 2024 19:06:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 19:06:26 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:fea1432adf0957427b45b0ef8e37cbfe045b7cf8c15e3f43e48f2f613e214d16`  
		Last Modified: Thu, 13 Jun 2024 01:25:07 GMT  
		Size: 49.6 MB (49576643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5651b5803b186603909f6c77cdff7bdd4ba7ab8ca4ebccb5a6b0be9037b4e5b6`  
		Last Modified: Thu, 13 Jun 2024 03:49:21 GMT  
		Size: 24.1 MB (24050013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3873416e6a335157d669c6193a256dfb289331d669d87f200e4eed1f19f9ebb9`  
		Last Modified: Thu, 13 Jun 2024 03:49:40 GMT  
		Size: 64.1 MB (64142031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b9d5ab122ef5810e4215d3fce52370bdbe1088b54b6557aa377ffadbc66536`  
		Last Modified: Thu, 13 Jun 2024 18:15:06 GMT  
		Size: 92.2 MB (92203259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69828e165440b00c6a6cf1cc039b1812b75b8604568728dccd4d39573d405e26`  
		Last Modified: Thu, 13 Jun 2024 18:15:06 GMT  
		Size: 69.3 MB (69345544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fdfa04b859ee7ea2c8d47b7fca00061b46eba2e041a10967f259f7ea37fffe0`  
		Last Modified: Thu, 13 Jun 2024 18:15:06 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:eabd6ce6a2762b2c90e0343ab7fe253c58c38feeebf4bcb20400882dc2c5ed86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87758aab50742421e7712604d25226e1bb3fd0cd3df48df657d89f651c3c0704`

```dockerfile
```

-	Layers:
	-	`sha256:5cce61e8d4262644a73a29e8f69e621e73e63fb6b17bf4c608422d013c71767b`  
		Last Modified: Thu, 13 Jun 2024 18:15:05 GMT  
		Size: 25.4 KB (25420 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; arm variant v7

```console
$ docker pull golang@sha256:d716390cc008272faa14647018840390ff92b53c278c1df497446e5d3c35478d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.1 MB (260119980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dfd16e2e3a18ec90bf4cfac1e16e39c948ffa0cedb1ca77ce9ba02d6e105560`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jun 2024 19:06:26 GMT
ADD file:4e983a5cb7d29543fc349746f45a7222e574dacf5a3c79841539a50f8c19121c in / 
# Tue, 04 Jun 2024 19:06:26 GMT
CMD ["bash"]
# Tue, 04 Jun 2024 19:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jun 2024 19:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jun 2024 19:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOLANG_VERSION=1.22.4
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOPATH=/go
# Tue, 04 Jun 2024 19:06:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 19:06:26 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6f5c0eaba00958485596d442de72c808c288b19cb6598afa423aefa8c1c93274`  
		Last Modified: Thu, 13 Jun 2024 01:01:14 GMT  
		Size: 45.2 MB (45175040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f43007e7b264595fb644d227437b5b5a40a08cf506f8905f388bee805d2e9ba`  
		Last Modified: Thu, 13 Jun 2024 01:33:04 GMT  
		Size: 22.0 MB (21953778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba09d7f8a9b10217e3ad0b9a640e8644b91701e59675c4e2443e6e4f8eb69c72`  
		Last Modified: Thu, 13 Jun 2024 01:33:24 GMT  
		Size: 59.2 MB (59217226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcad14c29da939d6f6f076d96d7ab4c9d669eda089a3ba0444a8916294ed435e`  
		Last Modified: Thu, 13 Jun 2024 19:29:07 GMT  
		Size: 66.1 MB (66060387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f2d60982f3278ca26e0dd4a91fb30e80076051e36da023e58e47681cc2934e`  
		Last Modified: Tue, 04 Jun 2024 20:20:28 GMT  
		Size: 67.7 MB (67713391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70aa5167231d74039147d6f52325b7cc1eb5b36d5e0724fa854ee78a9b058586`  
		Last Modified: Thu, 13 Jun 2024 19:29:05 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:8646f96566bd34a205b82ffe5f3dc309b16dcd7bc8d5cfc20c760dfdfdad8829
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6302419e273353b7283b43cbeb5c5a4336c632e652a09131c5aaa8be6d587606`

```dockerfile
```

-	Layers:
	-	`sha256:590e46e352536a4a72b4d7c5088ecf8e6543ef8732cb594a1d8c6f4bf1b57c51`  
		Last Modified: Thu, 13 Jun 2024 19:29:05 GMT  
		Size: 25.5 KB (25548 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:5880454888e91b887cc6c2a34f04509bf8f8a6b5495f958fa8a8882aa03013fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.7 MB (289713963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a525efafbbbc97bd17221476554ce7a6c6a30da2f67a8bb9ff7d123cc4522494`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jun 2024 19:06:26 GMT
ADD file:cfc8f76c8181d3ae6dda16ae894b184c69dbba114d446426e466126fe0ae62e5 in / 
# Tue, 04 Jun 2024 19:06:26 GMT
CMD ["bash"]
# Tue, 04 Jun 2024 19:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jun 2024 19:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jun 2024 19:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOLANG_VERSION=1.22.4
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOPATH=/go
# Tue, 04 Jun 2024 19:06:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 19:06:26 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1e60a453843e00d6f3d4242dbd696365f0894e3ca2f02f4ce1ab098d7ff7907f`  
		Last Modified: Thu, 13 Jun 2024 00:42:50 GMT  
		Size: 49.6 MB (49613402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dadad3edfd860d6d4fd52d4cbf17e7431a88d64161c62654786e60f331343a8`  
		Last Modified: Thu, 13 Jun 2024 01:30:17 GMT  
		Size: 23.6 MB (23586570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51cd5f8f608f832afd85dc82fbac4aea05183fd7fccf555dd4a53a4bbe06b013`  
		Last Modified: Thu, 13 Jun 2024 01:30:33 GMT  
		Size: 64.0 MB (63994737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1225016ec7f2e3ccd64f3abac1168bb39fb19ae42ba0a45c2bad0435fa2c0524`  
		Last Modified: Thu, 13 Jun 2024 18:03:00 GMT  
		Size: 86.2 MB (86248685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c0d35bf3e901b1024e7abc65a8b1332e085c592b5bdd1d9422364771935e1e`  
		Last Modified: Tue, 04 Jun 2024 20:19:51 GMT  
		Size: 66.3 MB (66270410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:138bdfe59823a5fd193bd18bc05200dd45906280a3de77c11734871a5422fb74`  
		Last Modified: Thu, 13 Jun 2024 18:02:58 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:bcc02d0b79c0ffbb90ef1375d42251d8b7b16ee9e7a7cc9bdf89b29c88d819ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 KB (25784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a3259b5b95e69ac28328b0ebc039b9d16ccd05aab4b194c3240f9318fe75091`

```dockerfile
```

-	Layers:
	-	`sha256:82b9d39573183603f980067c031d6f438bd46bc398045ef6277c5c0aaf98ecd9`  
		Last Modified: Thu, 13 Jun 2024 18:02:58 GMT  
		Size: 25.8 KB (25784 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; 386

```console
$ docker pull golang@sha256:209920f7d6fe838fb0bd824f80e67954be543a1863b68e79d90f3c085709064e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.4 MB (298435683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0b2f76688ebddb03945b6b4c418d4041d972639bc2ac9077f9bb494141ac399`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jun 2024 19:06:26 GMT
ADD file:1e1eac48c9d76a0aa3d81aa037ce0e962b5ddfce3364b10f3586db659d81188e in / 
# Tue, 04 Jun 2024 19:06:26 GMT
CMD ["bash"]
# Tue, 04 Jun 2024 19:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jun 2024 19:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jun 2024 19:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOLANG_VERSION=1.22.4
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOPATH=/go
# Tue, 04 Jun 2024 19:06:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 19:06:26 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:852c9038cb65e2e7439aa662ff4e286f79e1be04afd71b71b373c29c5611fcae`  
		Last Modified: Thu, 13 Jun 2024 00:42:59 GMT  
		Size: 50.6 MB (50602447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01cee71c1fc4977c82dc6f4660b13a8b8f1be5e2c7784dc4f73433486837241c`  
		Last Modified: Thu, 13 Jun 2024 01:18:48 GMT  
		Size: 24.9 MB (24888472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a9e5ec3fb52acd5155f108c6f26d0a120522c7123cc28a08b50ccc21286f53`  
		Last Modified: Thu, 13 Jun 2024 01:19:13 GMT  
		Size: 66.0 MB (65989018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40bf7ca866f244476aa69949ada067b3e5d968446931c087dcbd2eb90a540e67`  
		Last Modified: Thu, 13 Jun 2024 01:59:12 GMT  
		Size: 89.6 MB (89611031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2ea21d249fd26578d9c1a35b4416c66b4489c19f9c4d430e1a1b095529427e`  
		Last Modified: Thu, 13 Jun 2024 01:59:14 GMT  
		Size: 67.3 MB (67344557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ed70786cabcf70d74d7021f7908ce044adacedbc4e84a2fe88cf8fe42341bc`  
		Last Modified: Thu, 13 Jun 2024 01:59:10 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:31612c656ae18d1bdbe800716a20b28a1f2c573fe8bd415844bd1837dc6581fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7024921918efeaffdff917777e1697b8efec90f8a0e60046ae918e3d62e1b8b3`

```dockerfile
```

-	Layers:
	-	`sha256:1370cfab19d399fddafd607bc6f4dfb28e1854b6a99ad8181e094a8ea5e66d5d`  
		Last Modified: Thu, 13 Jun 2024 01:59:10 GMT  
		Size: 25.4 KB (25365 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; mips64le

```console
$ docker pull golang@sha256:a977a92a8cc1a1c216ab51a1ae997e845b9a527ed9a71608f245b1b1919dd091
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.9 MB (269881455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3db3e6993f9796cba9832f3cac7beb30e4de9e96188b45ab4efe4a97770c7e0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jun 2024 19:06:26 GMT
ADD file:c1871631a2828ac765a04bc2cf8d2d9709cd81730d4ce46e403f4d0dbeff9dbb in / 
# Tue, 04 Jun 2024 19:06:26 GMT
CMD ["bash"]
# Tue, 04 Jun 2024 19:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jun 2024 19:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jun 2024 19:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOLANG_VERSION=1.22.4
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOPATH=/go
# Tue, 04 Jun 2024 19:06:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 19:06:26 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6cf4285917f60eb7d02ed62b32504e18b0ca84bfd90c36a0b39f6eb520741b6a`  
		Last Modified: Thu, 13 Jun 2024 01:21:11 GMT  
		Size: 49.6 MB (49582735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9adc1137b694767cc0d09b98cc14d61f1a91b811b596506348d0673d092435b4`  
		Last Modified: Thu, 13 Jun 2024 02:36:03 GMT  
		Size: 23.4 MB (23438130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1c3c99bf43fc1ee7e418fa6f18cd0021306408228bbe2acf6511535380acad`  
		Last Modified: Thu, 13 Jun 2024 02:36:56 GMT  
		Size: 63.0 MB (62968443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d646a010c7e20cd99a8af56e967f1476d6890a1cf69c0ec4fb58347d9964f688`  
		Last Modified: Thu, 13 Jun 2024 23:10:02 GMT  
		Size: 69.8 MB (69776888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4e333f75cdf8d0faccff8152d9880003b584f6ce457e88161caf95ef6ba28e`  
		Last Modified: Thu, 13 Jun 2024 23:10:02 GMT  
		Size: 64.1 MB (64115100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7412c981dd7866e84d512748388bedc711316b0d9db068e883f726eb4bc33f53`  
		Last Modified: Thu, 13 Jun 2024 23:09:55 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:07f5e2908c399f89370b59e1854a775ba6328f5f40753d9b39c07336e34098e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dd5450134f0b24725e25e46d74a80ef8d65abf753ca1b910ce2955c8162c2dc`

```dockerfile
```

-	Layers:
	-	`sha256:faa8f9ed03c6688a68b1be698465942797e9475ba97589dd5ce031ade2baae3a`  
		Last Modified: Thu, 13 Jun 2024 23:09:55 GMT  
		Size: 25.5 KB (25519 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; ppc64le

```console
$ docker pull golang@sha256:41f8371a27ab24c14837f30f5efaea4d38641d1cfea35e365e6e0dbd0ab94fc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.5 MB (305491313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccfa0d3bde992cfc1fab1ad670d5a21e668e4acdb97171496aa2a9479f04df41`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jun 2024 19:06:26 GMT
ADD file:5b31953e08477fa1771514ef5fd326ae78b7c4ad417cbb64755ee493634ab392 in / 
# Tue, 04 Jun 2024 19:06:26 GMT
CMD ["bash"]
# Tue, 04 Jun 2024 19:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jun 2024 19:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jun 2024 19:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOLANG_VERSION=1.22.4
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOPATH=/go
# Tue, 04 Jun 2024 19:06:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 19:06:26 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7e04e800a5f6b106e3f1cb53c3677b55297b3841c160edc0f657f7a27ffb9ad0`  
		Last Modified: Thu, 13 Jun 2024 01:21:03 GMT  
		Size: 53.6 MB (53579678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4148242bae3618c54f03447132a7364c4a46c509d204908b4d8b569f2cbbf18d`  
		Last Modified: Thu, 13 Jun 2024 01:59:41 GMT  
		Size: 25.7 MB (25699643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0038ae14b2277791270ea7736f896040def15b2cfcc8a74ca0cfd14349e968`  
		Last Modified: Thu, 13 Jun 2024 02:00:03 GMT  
		Size: 69.6 MB (69583876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96adff8b61d9da6edc56f4c4d5ce3a64f681fa547a46d5b430a8cf1d24ba91c3`  
		Last Modified: Fri, 14 Jun 2024 00:18:51 GMT  
		Size: 90.2 MB (90187121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236cbdc316b6a948ffe0177ed252011a6646360d0cbcf8cbfc819b8774160a29`  
		Last Modified: Tue, 04 Jun 2024 20:19:26 GMT  
		Size: 66.4 MB (66440839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5ad756fa497a83b25c26022e1305d3c64e8fc08a876ba5d632ca4554a80a8c9`  
		Last Modified: Fri, 14 Jun 2024 00:18:48 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:5243ec7afe2e02fca26c9a84e198da21420214e128ddcb4022e02ca2ced15d32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d25d903b82d7e016e0735cb691bf5e1b3375633069d00181b31fc58f9610babd`

```dockerfile
```

-	Layers:
	-	`sha256:1cceaea9d85506d0ba8598624a81184ad79e53ac8e70836a694eee2d3585bb10`  
		Last Modified: Fri, 14 Jun 2024 00:18:48 GMT  
		Size: 25.5 KB (25486 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; s390x

```console
$ docker pull golang@sha256:abea61f43db71009a3ee493f022d01d4fad22acf211d77d2cb0592c7821e1512
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.3 MB (272300059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d99e89b9b4fdb49bcd0c7d974ede96dcaeb9a08bb3a4234d9b484a0fa433db0f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jun 2024 19:06:26 GMT
ADD file:4debdbf640f7b84de2c501cfcf8124343554f82fc2c8948149efc9e60c80c7f1 in / 
# Tue, 04 Jun 2024 19:06:26 GMT
CMD ["bash"]
# Tue, 04 Jun 2024 19:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jun 2024 19:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jun 2024 19:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOLANG_VERSION=1.22.4
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOPATH=/go
# Tue, 04 Jun 2024 19:06:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 19:06:26 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6d80f2b74ad971cfa89367f3157841bc726dd7cfbfd585d5aabbdac584178990`  
		Last Modified: Thu, 13 Jun 2024 00:47:26 GMT  
		Size: 47.9 MB (47942476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa12a6c3cf967133a8f0a30b6c3f3b164be42f75e34007b370d4c4ccbbe04993`  
		Last Modified: Thu, 13 Jun 2024 05:30:54 GMT  
		Size: 24.0 MB (24046768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562db015b7d28466453e6548a5b0b491293d13e90bdeea148e63c5fe7b505321`  
		Last Modified: Thu, 13 Jun 2024 05:31:09 GMT  
		Size: 63.1 MB (63130173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:063ea68ab09079e6198714013ff756d95ff435d4226ebb4df12acc526efa69c2`  
		Last Modified: Fri, 14 Jun 2024 04:38:23 GMT  
		Size: 68.8 MB (68775236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7fb824bc24fdc7f4fb089d47d141644e86949635714a893519e6ce56fa54e32`  
		Last Modified: Tue, 04 Jun 2024 20:22:15 GMT  
		Size: 68.4 MB (68405249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3be5ce3f08f316f672f2a28ca42f57f70700da5d8c95a563c126b044dd3a729a`  
		Last Modified: Fri, 14 Jun 2024 04:38:22 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:125237dd3365e40a590d546e1a8d7edf7d19aed01349530a89902644cf044a48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b195768d3c365020f5ba86a625a15f9fc0d2e1f6fee420ffad3c0a9a1c9622fd`

```dockerfile
```

-	Layers:
	-	`sha256:576dd1aa169807b9437cd2318df32f01525b50f900cc5a7a7fd02e3d62177bdb`  
		Last Modified: Fri, 14 Jun 2024 04:38:21 GMT  
		Size: 25.4 KB (25420 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - windows version 10.0.20348.2527; amd64

```console
$ docker pull golang@sha256:21e4cfffc0dd2debbf84777e12b283128ab8f85012f67ffb6e903ed212cf2ea4
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2215677544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77cc4051880c1c49d496de58570537e73e8ecc02b78ef302894c31e041db0fff`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 07 Jun 2024 09:02:12 GMT
RUN Install update 10.0.20348.2527
# Wed, 12 Jun 2024 18:09:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Jun 2024 18:09:22 GMT
ENV GIT_VERSION=2.23.0
# Wed, 12 Jun 2024 18:09:23 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 12 Jun 2024 18:09:24 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 12 Jun 2024 18:09:24 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 12 Jun 2024 18:09:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 12 Jun 2024 18:09:44 GMT
ENV GOPATH=C:\go
# Wed, 12 Jun 2024 18:09:50 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 12 Jun 2024 18:09:50 GMT
ENV GOLANG_VERSION=1.22.4
# Wed, 12 Jun 2024 18:10:55 GMT
RUN $url = 'https://dl.google.com/go/go1.22.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '26321c4d945a0035d8a5bc4a1965b0df401ff8ceac66ce2daadabf9030419a98'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 12 Jun 2024 18:10:57 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cedf08888525e83e4a050655b4ec0d81647e59a69f7007a560df774a656da9bb`  
		Last Modified: Tue, 11 Jun 2024 17:49:21 GMT  
		Size: 729.6 MB (729579921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0587398dd0c7678da17819ef86b03d0f03d5608d921ef1bd9dd041001aa46064`  
		Last Modified: Wed, 12 Jun 2024 18:11:02 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9adab2cbb6127c55064d7c9aa02c40af934b227b342e9ce0ed36ee98f1b4843`  
		Last Modified: Wed, 12 Jun 2024 18:11:02 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d69ff0b716a5ce8110bb53b45bd91710d820149130deed9c38472234a7e9afd9`  
		Last Modified: Wed, 12 Jun 2024 18:11:01 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96de8f0195629f8fc68326d735d8815462e97b6c76fbbf56e537824e83e8e4be`  
		Last Modified: Wed, 12 Jun 2024 18:11:01 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc335406a0dfe2ded2091ea3986516dfe4e922b476d834ddb8aec57c37e493c`  
		Last Modified: Wed, 12 Jun 2024 18:11:01 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d5e46457004c449858017460ecd124b76a51b6e5c4d75579bd0fed83a03b66b`  
		Last Modified: Wed, 12 Jun 2024 18:11:04 GMT  
		Size: 25.4 MB (25426639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a91a7cff7f3986c1704d0d0fc42da5934271de00dc73f1bbbb33c58179ae1d2`  
		Last Modified: Wed, 12 Jun 2024 18:10:59 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ffbe09e050d4b99a243d40d14a09182e015c0a0d40c056ecd2f2b196eb9d06`  
		Last Modified: Wed, 12 Jun 2024 18:11:00 GMT  
		Size: 325.4 KB (325417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342559014cfb73e966442ed88b5360904cd00c05a834f575b49596888e680792`  
		Last Modified: Wed, 12 Jun 2024 18:11:00 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bea1a9b1009e5fa7a44f4b39043515d74d2b1a71c21fa1252506b20c9d8d935`  
		Last Modified: Wed, 12 Jun 2024 18:11:10 GMT  
		Size: 71.7 MB (71736322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59599ecaa1eb84019e233b455deae710859ed0f0a323ec5689d820efaf55ff3f`  
		Last Modified: Wed, 12 Jun 2024 18:11:00 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:latest` - windows version 10.0.17763.5936; amd64

```console
$ docker pull golang@sha256:0d28936f1f3618fb15ca207e8bcd894e2798bdc25a1a360b9f6841ceb03325c1
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2318590683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc8024ccff21538acc48afa580b0f9300431ebac003ab469bc8c2e10597188ac`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jun 2024 11:19:50 GMT
RUN Install update 10.0.17763.5936
# Wed, 12 Jun 2024 18:13:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Jun 2024 18:13:33 GMT
ENV GIT_VERSION=2.23.0
# Wed, 12 Jun 2024 18:13:34 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 12 Jun 2024 18:13:34 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 12 Jun 2024 18:13:35 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 12 Jun 2024 18:14:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 12 Jun 2024 18:14:24 GMT
ENV GOPATH=C:\go
# Wed, 12 Jun 2024 18:14:41 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 12 Jun 2024 18:14:42 GMT
ENV GOLANG_VERSION=1.22.4
# Wed, 12 Jun 2024 18:16:03 GMT
RUN $url = 'https://dl.google.com/go/go1.22.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '26321c4d945a0035d8a5bc4a1965b0df401ff8ceac66ce2daadabf9030419a98'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 12 Jun 2024 18:16:05 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a5fd77f8cb6921d3e283f98213bf8c163d3502a75b4a8e4a809a15654f7d1a`  
		Last Modified: Tue, 11 Jun 2024 17:22:31 GMT  
		Size: 570.1 MB (570060810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae3c3ab4cd77fae9059354ee5b73b856f9ac9c22731d9dcf4e365268e08cd843`  
		Last Modified: Wed, 12 Jun 2024 18:16:10 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d86c37a0d0339c6b8b1c237b2c8250a774461350198b803d76982b65e45d102b`  
		Last Modified: Wed, 12 Jun 2024 18:16:09 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a3b2fa9fd4cc3f0df2f037d6653ea1cdb5b7f419bd99e0576a57dcdf4b1ace7`  
		Last Modified: Wed, 12 Jun 2024 18:16:08 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:856fdc06eea972eccedb4e2c6d528d9d6b992c971c4a29f289a88eac23a5d5a9`  
		Last Modified: Wed, 12 Jun 2024 18:16:08 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b2096b09fa3f4c724fcb42fe19a8a5b0dc61277e2e802b4674b64a58de93238`  
		Last Modified: Wed, 12 Jun 2024 18:16:08 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69169629162eb6e94b664ddd335d3d02ae4c7a356ec11557b77d6780bfb3bb04`  
		Last Modified: Wed, 12 Jun 2024 18:16:11 GMT  
		Size: 25.6 MB (25576657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78abdc0679bbe9abc0864ab9497cfb6767ad50cc06c121d874dd8a022821b892`  
		Last Modified: Wed, 12 Jun 2024 18:16:07 GMT  
		Size: 1.4 KB (1355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e6bc3316ec48d85e70aa2d8c21fa5ad4eb37113d651977b29d3b5495e034859`  
		Last Modified: Wed, 12 Jun 2024 18:16:07 GMT  
		Size: 336.9 KB (336919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5222f75d358e9b8e60fd785f40a7b8245f0cf6d634f64488172b55910395e1a2`  
		Last Modified: Wed, 12 Jun 2024 18:16:07 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e23068dc7ebfc095432cdb1e6af9726e3b10d959fb3635a24504c0e99a1a297`  
		Last Modified: Wed, 12 Jun 2024 18:16:18 GMT  
		Size: 72.0 MB (71984977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe4726c882b12bd6e005278f53050cd3de58b99ce5170e1d152a081dd3e8d6b`  
		Last Modified: Wed, 12 Jun 2024 18:16:07 GMT  
		Size: 1.5 KB (1501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
