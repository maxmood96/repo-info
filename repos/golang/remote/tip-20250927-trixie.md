## `golang:tip-20250927-trixie`

```console
$ docker pull golang@sha256:83315cb833f04b550c924ae7c5298090bbb83b9c0e3af879e76f69378a3d7d71
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `golang:tip-20250927-trixie` - linux; amd64

```console
$ docker pull golang@sha256:61f68380f19f69f026b0594c4e1e668c2712f6efce85bf77d8ddadadcc486045
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.6 MB (328634462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f51f7f097d9709b57cd7e0fb3656c21a5627620e7558219afb7d78bdfff7115`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 29 Sep 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Sep 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:cae3b572364a7d48f8485d67baee38e4e44e299b8c8c4d020ff7fb5fdd97f88c`  
		Last Modified: Mon, 29 Sep 2025 23:35:29 GMT  
		Size: 49.3 MB (49284626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd090f42c4b7844c5846f9b4c719994f496fac3befe1d30f0ff20794e742370a`  
		Last Modified: Tue, 30 Sep 2025 03:17:21 GMT  
		Size: 25.6 MB (25614810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c9d6d993ac93f222ba87ca01097d40f632be9b48f6b5e399f2c5da1b3133d1`  
		Last Modified: Tue, 30 Sep 2025 03:18:12 GMT  
		Size: 67.8 MB (67784949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e6dc34717e6f37af20da5a04bf486914bfa4f495042c2e345cf2e7ec37a498`  
		Last Modified: Wed, 01 Oct 2025 14:29:59 GMT  
		Size: 102.1 MB (102088390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd392ccd6779e7a888cee1ecce65db01995a1886c75ae75a375deb44486fd071`  
		Last Modified: Mon, 29 Sep 2025 20:26:43 GMT  
		Size: 83.9 MB (83861530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c19a18780e9a1092f4f5810f8f50cf3b42a3e89e0abd88b51e8b48aec792c221`  
		Last Modified: Tue, 30 Sep 2025 09:57:07 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250927-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:c053478c7305c41ea0b39efd81166b46fb2b949494f594f51385e7e0092c1656
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10811946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f068786a5332447f3f5c37851a31f44f90ebab9faec380379da837a4c2a84206`

```dockerfile
```

-	Layers:
	-	`sha256:e189e49539bf8b222cbc9620e5e98ff380323e6a41ef9663069e27ce31876fd1`  
		Last Modified: Wed, 01 Oct 2025 14:23:50 GMT  
		Size: 10.8 MB (10782934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07f82f4b8352eb448d2a504f6e9e9e8934e9c816b3d77aa85f7005dd9d5d3ddd`  
		Last Modified: Wed, 01 Oct 2025 14:23:51 GMT  
		Size: 29.0 KB (29012 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250927-trixie` - linux; arm variant v7

```console
$ docker pull golang@sha256:c1f026c2c464928bd08287217dffed6d7a4606f53bb7d82ac91d5e11908b6ccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.7 MB (285673071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0cb5a7ba0790102e27d148adeadd09045a4fb9b752b8431e47dabf003918910`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1757289600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 29 Sep 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Sep 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:395f9ad3c9d37c6ea60897f33e8b189e9cd41fba6c60ab63882fd95de8ebb9f2`  
		Last Modified: Mon, 08 Sep 2025 21:15:43 GMT  
		Size: 45.7 MB (45711720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87266d99f84095bec303de1733ad218d485653dfb6da729b7a066c18810645f9`  
		Last Modified: Tue, 09 Sep 2025 00:02:54 GMT  
		Size: 23.6 MB (23614030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0847685b749ce0208c0ad2a407e89f30279b1c8515c5c33f13a9c9b4c5e3da02`  
		Last Modified: Tue, 09 Sep 2025 06:20:22 GMT  
		Size: 62.7 MB (62719599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c6e34baf9854c6853ac2dde4db477e6602af6c755e813036bc7e693ef5628c`  
		Last Modified: Mon, 29 Sep 2025 18:04:45 GMT  
		Size: 72.7 MB (72733729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eea36933200b5f141ab18c26e141eacf675fe2778fc8f3cca0727236a934dcf`  
		Last Modified: Mon, 29 Sep 2025 18:04:27 GMT  
		Size: 80.9 MB (80893837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e3534c65552e07990c7403bab56a0994ebfe6fc0e5bcecc9e35d004c7abc73`  
		Last Modified: Mon, 29 Sep 2025 18:04:23 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250927-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:c80f7dd8ca14c49359eeb2f8831fd55e60c5f9e90fd01348398adcb8fd4e240c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10607958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:522c6f48267eeeed20238474d9490ef67cbf86e8d395797f2c06cc8e5f7360bf`

```dockerfile
```

-	Layers:
	-	`sha256:d09412d2d3a1abf815ed4376cf9845e719043dfbdc9e838334b196bdd74f5483`  
		Last Modified: Mon, 29 Sep 2025 20:23:47 GMT  
		Size: 10.6 MB (10578823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d551033bf36384ebbfc545cd577b0bd4540c8b8028f0470e4edb8c593ac323f3`  
		Last Modified: Mon, 29 Sep 2025 20:23:49 GMT  
		Size: 29.1 KB (29135 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250927-trixie` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:6a7f7a6d98165cb27ff7162262fb42595cd6215594360059e693cd2ac5f50f9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.3 MB (320297413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:394f00bcfc62c54c0623c167150f550b130f1c5b2a1cac520c78d9571d87fd3a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 29 Sep 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Sep 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:28aec8b14b3eeacbf47ef38af72fab694b109fdcdf31581722750599baf1a932`  
		Last Modified: Mon, 29 Sep 2025 23:35:17 GMT  
		Size: 49.6 MB (49648695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:003e6ed58c0c6ddbc757cdcbd876d66b9b5eed39128088a0055c819ebe15d20d`  
		Last Modified: Tue, 30 Sep 2025 00:14:22 GMT  
		Size: 25.0 MB (25016370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390c9631087ef516f060328537d417f223e1f264c968e39186895696e78090b7`  
		Last Modified: Tue, 30 Sep 2025 01:20:15 GMT  
		Size: 67.6 MB (67582977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b6f8f6a2de4122e8804e1ab874cd2afb58e2965b68634cb3d4e81ed5cd6f494`  
		Last Modified: Tue, 30 Sep 2025 03:19:31 GMT  
		Size: 98.2 MB (98234442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e94a779ece8baaa3a2b9ccff68843c683bfb8ad46a4cbd1f1c29fcc7f5e6802e`  
		Last Modified: Mon, 29 Sep 2025 18:02:35 GMT  
		Size: 79.8 MB (79814772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c2dd131828e5953e6b47f46ecef4a0847412591bccd91483b7189702440edc3`  
		Last Modified: Tue, 30 Sep 2025 03:19:26 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250927-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:36515c70002610471644974efc97dcf01ffa50d69b9f4f49e8f25c400b6e56c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10932556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03f9252ad63ea08904b4f9d01146eb571a6d40d8d8a7fb04a6a41e1c15dd1d0b`

```dockerfile
```

-	Layers:
	-	`sha256:ad57a6f80ea8619fe353197440c02debb5039459cfb2baf38bbf9a3976ee6b55`  
		Last Modified: Wed, 01 Oct 2025 11:36:11 GMT  
		Size: 10.9 MB (10903389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29da3eb564c27c5c8428303a0d67c5072fb502efcbe692a69967a7acfcf84590`  
		Last Modified: Wed, 01 Oct 2025 11:36:12 GMT  
		Size: 29.2 KB (29167 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250927-trixie` - linux; 386

```console
$ docker pull golang@sha256:5bab7b8c9c2a8eb49a49ade14197a286406bd267158f5251de906391b8d2a14c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.4 MB (330433274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e199f50fd750713357ef08150f5d6c9e5ef4f405bb386203c7dcdbfa8187286`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 29 Sep 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Sep 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f1c1f592b5569b5e2093c3107a48f2929b609f05af6d24c06d41a7ec1ae5e0e1`  
		Last Modified: Mon, 29 Sep 2025 23:35:36 GMT  
		Size: 50.8 MB (50800229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e5d861644e3a43dbea9917a86fd0d6ccf184bc7514ee58118ffa521ac4bc61`  
		Last Modified: Tue, 30 Sep 2025 00:21:14 GMT  
		Size: 26.8 MB (26774670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acddf1ffebf58f05179a0e8a785ab62df40c7d1c75ee543282d404ca07d3ffec`  
		Last Modified: Tue, 30 Sep 2025 01:21:21 GMT  
		Size: 69.8 MB (69794474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:206045177115125ac225fb76203a77d776d0ff7231db3f81eca11a65137749c5`  
		Last Modified: Tue, 30 Sep 2025 15:11:18 GMT  
		Size: 100.5 MB (100533055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe29e58b8c06a986ae5ca92831db1a0d8e315d4140a28e6305b3b9513f262ee`  
		Last Modified: Mon, 29 Sep 2025 22:06:46 GMT  
		Size: 82.5 MB (82530689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f25d3907373d63764124f2d6cbcd0882bc26db4816c49da97f3465209db64912`  
		Last Modified: Tue, 30 Sep 2025 04:07:15 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250927-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:b5c722c2e4ec7e3c62303c33f12ac5b91385450eb88ce10bbc94d8653694a8ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10783169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6e90da440bc6e64ea2997ef29aa8fc4d070b19d49d19200f39a0f08402988fd`

```dockerfile
```

-	Layers:
	-	`sha256:b58b9548da16b71ebadb73a349c63d3bf18ea3356f1377732bc84a0c4f8926e7`  
		Last Modified: Tue, 30 Sep 2025 17:23:43 GMT  
		Size: 10.8 MB (10754200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e067fb4e06701509c8d90120f208f423d9a214205d1c50bb3da8148e36c5977`  
		Last Modified: Tue, 30 Sep 2025 17:23:44 GMT  
		Size: 29.0 KB (28969 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250927-trixie` - linux; ppc64le

```console
$ docker pull golang@sha256:13dc957c166649ec10cdfd12f55f3231cf8bca61d2d43d40ce77431dac41277d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.1 MB (327134545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff9f8ccb2b3d146b2a2a29242d0811be5dc8b8bc3994fc99429c186ad866e516`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 29 Sep 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Sep 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:4cb8224e7ffc22512c71f1cfc1042cb22342df02312e61cb1ab0c492c3369711`  
		Last Modified: Mon, 08 Sep 2025 21:18:07 GMT  
		Size: 53.1 MB (53104433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9bf3914a916f37a54163b2eb02b685f6e0d654680e02a5e51b78387e81e4077`  
		Last Modified: Tue, 09 Sep 2025 06:02:47 GMT  
		Size: 27.0 MB (26993871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31355a04af67dd51f580585ba523dfd2b5ad7d91e873cb7213748a572df48bb6`  
		Last Modified: Tue, 09 Sep 2025 15:30:51 GMT  
		Size: 73.0 MB (73033628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8672ea681bc1020ea13fedba257ffcddf80ac9064cc95839dafcc76d676aeca`  
		Last Modified: Mon, 29 Sep 2025 22:07:31 GMT  
		Size: 92.8 MB (92794864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c4682e6be6673e7aa33301c5b30874cd778044246d060f0fbf3c29475651b8b`  
		Last Modified: Mon, 29 Sep 2025 18:07:23 GMT  
		Size: 81.2 MB (81207592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa39ffd67e922714c103a86fa0b75372d24b05911527debb49f81cf45d1402f6`  
		Last Modified: Mon, 29 Sep 2025 18:07:18 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250927-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:ea57ea5b2589f5ac4e040154afbaaa70a749daa79a6c3160b02ae84cdac58316
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10807783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8931bbe1711f750eb1953636096afadcee1b76447aad4542fd66d53143b8366e`

```dockerfile
```

-	Layers:
	-	`sha256:c7f8f64844969ab78498d8497767e83f7f7954782d7b5f819305ca4ce840c511`  
		Last Modified: Mon, 29 Sep 2025 20:24:14 GMT  
		Size: 10.8 MB (10778718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73b17d1d9c73fd4e0ba2a8649185f3ee5744ef5f0d276aafbd32e821fefc0e00`  
		Last Modified: Mon, 29 Sep 2025 20:24:15 GMT  
		Size: 29.1 KB (29065 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250927-trixie` - linux; riscv64

```console
$ docker pull golang@sha256:f4da1ba9c9c7ad918101c26d0ac64f2310e6a162a5d506847c64dfecb25bb699
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.5 MB (352463360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5102795c9c08e1e1446eec4cb8f5e28028b6f387543784c19f96d53a44441347`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1757289600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 29 Sep 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Sep 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:8f913be5ecadf79e3ee9792194aaab366421c7e066487d572f285b293ff78a7a`  
		Last Modified: Tue, 09 Sep 2025 00:25:27 GMT  
		Size: 47.8 MB (47765447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b1afb27b72dabce7ba373ba8319bd1ccd2205d7724f23909527bd3da7476b1`  
		Last Modified: Thu, 11 Sep 2025 01:43:59 GMT  
		Size: 25.0 MB (24952790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32856986223852ec3f854d1a7c152bc97555c3c9e06114ce074d65dc96a8dee`  
		Last Modified: Fri, 12 Sep 2025 02:24:28 GMT  
		Size: 66.7 MB (66660361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32ccaac1efde5b5edf5e06fc7214fdc1986a9341055511d69b9c3f5e789f783`  
		Last Modified: Mon, 15 Sep 2025 06:09:44 GMT  
		Size: 131.6 MB (131561217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1abfcbaa70a0168de1aea7c77a550816bb9fc5ed593a95bf38e36239223dcc`  
		Last Modified: Mon, 29 Sep 2025 19:43:19 GMT  
		Size: 81.5 MB (81523388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e2c56556b49c578f23a92e42e210b7b13986f3cc8d56482663e5a031b815bd4`  
		Last Modified: Mon, 29 Sep 2025 19:43:13 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250927-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:27955e6ee5599c455ee98f250178a9b86b6e33d4cd3c94bbc5ae09c2b432b670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10881621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59eb908ff1722084c248fce56cf8ff20c2dc66f6cc4fb97d7f9fce23402039fc`

```dockerfile
```

-	Layers:
	-	`sha256:d0cbacb0b9b39856fcd5920eb5bd5895f0515c03993fcb93b9b36d09fc268c1d`  
		Last Modified: Mon, 29 Sep 2025 20:24:26 GMT  
		Size: 10.9 MB (10852551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de8c0d04ce966ad6a8b54cae50e03991573fc26651136658232cce5cb78fb74d`  
		Last Modified: Mon, 29 Sep 2025 20:24:27 GMT  
		Size: 29.1 KB (29070 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250927-trixie` - linux; s390x

```console
$ docker pull golang@sha256:e47f0341f62d628c69dc899d973f6e3c76912c1985e0f1fcbb9f4c3193377d71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.1 MB (303101229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9664e2226d6a42a612ae22049c0d9e7ff504279e3d9a8326c1fd337e981e93a7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 29 Sep 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Sep 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:28eee642962fd09c10ecf87da2d4b65d208f3d5c1bf3fcca21c105c0213f558a`  
		Last Modified: Mon, 08 Sep 2025 21:32:18 GMT  
		Size: 49.3 MB (49346327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e775d8e7868b319a235eef909d5a12163c48c579e84d18d78ed794653cb126a0`  
		Last Modified: Tue, 09 Sep 2025 06:02:49 GMT  
		Size: 26.8 MB (26780367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e76c2286bf1bfe1b0d2250435d28c0af55c645ac84ddeac003b9da9b68c9c87`  
		Last Modified: Tue, 09 Sep 2025 12:08:32 GMT  
		Size: 68.6 MB (68636032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891b0563252f214cb0223fbb0c0ce70a68fc283bcf28977ad8d51239efb3c4c3`  
		Last Modified: Mon, 29 Sep 2025 18:05:39 GMT  
		Size: 75.9 MB (75900343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02ed6e6981e4c029c9853a9bbba242bc2c9b41f236141c1f10c1334ce58549f0`  
		Last Modified: Mon, 29 Sep 2025 18:05:39 GMT  
		Size: 82.4 MB (82438002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08e9492694eea7934c1a9656013b19ea12ce898df57eb8858aefa7cece0ee72c`  
		Last Modified: Mon, 29 Sep 2025 18:05:31 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250927-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:7210ae2b04ac57337a9e696a9f2a6181763857900791bc95a2e696e5b477c9a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10622341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1df967678961939cbee59e6c296bf109500c374c9748e9ffba68a76a9d59c7b5`

```dockerfile
```

-	Layers:
	-	`sha256:545a6b6664528ac4446d89530b5f141a4bb2b39e9348f3d28acb27df7c423d94`  
		Last Modified: Mon, 29 Sep 2025 20:24:33 GMT  
		Size: 10.6 MB (10593334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a6fc86316a1ae632cd1de5b0f7977feaf993430eb36f6ea2418ce6ee0441b65`  
		Last Modified: Mon, 29 Sep 2025 20:24:34 GMT  
		Size: 29.0 KB (29007 bytes)  
		MIME: application/vnd.in-toto+json
