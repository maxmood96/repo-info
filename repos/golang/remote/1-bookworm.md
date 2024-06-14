## `golang:1-bookworm`

```console
$ docker pull golang@sha256:27683a53606aaa5348431e529decc0fdcd89726db0d0fc5258a8103924b8f452
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

### `golang:1-bookworm` - unknown; unknown

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

### `golang:1-bookworm` - linux; arm variant v7

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

### `golang:1-bookworm` - unknown; unknown

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

### `golang:1-bookworm` - linux; arm64 variant v8

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

### `golang:1-bookworm` - unknown; unknown

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

### `golang:1-bookworm` - linux; 386

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

### `golang:1-bookworm` - unknown; unknown

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

### `golang:1-bookworm` - linux; mips64le

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

### `golang:1-bookworm` - unknown; unknown

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

### `golang:1-bookworm` - linux; ppc64le

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

### `golang:1-bookworm` - unknown; unknown

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

### `golang:1-bookworm` - linux; s390x

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

### `golang:1-bookworm` - unknown; unknown

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
