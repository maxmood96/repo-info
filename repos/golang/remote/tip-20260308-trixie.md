## `golang:tip-20260308-trixie`

```console
$ docker pull golang@sha256:ddafe5cc4487fa9237d24c5f5e95cbe7401d076a4dfc39c841dab7f33cfde4cb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
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

### `golang:tip-20260308-trixie` - linux; amd64

```console
$ docker pull golang@sha256:76b14190ea942ae5f43a8c140c79b591f8352d2a80e1cda3ffb80828c0e5c728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.5 MB (338517127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1bcd9bc1bd02ad9d0b434886758cf61e91e156c1aa5a8d4e38f73d4fd732b2d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:20:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 20:04:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 09 Mar 2026 18:34:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Mar 2026 18:36:31 GMT
ENV GOTOOLCHAIN=local
# Mon, 09 Mar 2026 18:36:31 GMT
ENV GOPATH=/go
# Mon, 09 Mar 2026 18:36:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 18:36:31 GMT
COPY /target/ / # buildkit
# Mon, 09 Mar 2026 18:36:33 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 09 Mar 2026 18:36:33 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:866771c43bf5eb77362eeeb163c0c825e194c2806d0b697028434e3b9c02f59d`  
		Last Modified: Tue, 24 Feb 2026 18:43:22 GMT  
		Size: 49.3 MB (49293124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed881fbf1b07b42dd470cd5b56a8feb684d60879c6f8028a9e7a8715e0e72361`  
		Last Modified: Tue, 24 Feb 2026 19:20:17 GMT  
		Size: 25.6 MB (25614562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da421ddeb655bdfb3960e490b39373b0d1351e3eaba61d01978107920638392`  
		Last Modified: Tue, 24 Feb 2026 20:04:27 GMT  
		Size: 67.8 MB (67778971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee77ce036502de34d5a5c33e14a85c24a4b399e90aa001bb32bce65ebcf73d27`  
		Last Modified: Mon, 09 Mar 2026 18:36:58 GMT  
		Size: 102.2 MB (102166320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a04c034b447c8996669d72bbe0e1d2cec1d82755b44408c364d44c021efa7f7`  
		Last Modified: Mon, 09 Mar 2026 18:36:47 GMT  
		Size: 93.7 MB (93663992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c7e2a90d0245d1e137a18d5d06b530878bdd0030dd7472d0e8968e37439eda3`  
		Last Modified: Mon, 09 Mar 2026 18:36:55 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260308-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:8b909c8aec8c5d8c9774c14e98f58fe3634e0af52afb1b682f9f7f7c4210dd1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10814552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:849f353ca38a8929484a4b1cb12a3eb59bd219ce590b1b7aa1b479f6984205f5`

```dockerfile
```

-	Layers:
	-	`sha256:dcb1cbb555c629d4751b18920518d67dd5f53958f2b378f3e3e7a8f1d905384a`  
		Last Modified: Mon, 09 Mar 2026 18:36:56 GMT  
		Size: 10.8 MB (10785583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8946e18dfaeef05e48b10a2d4261b69363c88a5276038a95e41f31708bfefdd`  
		Last Modified: Mon, 09 Mar 2026 18:36:55 GMT  
		Size: 29.0 KB (28969 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260308-trixie` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:72a9d69dc349723c2bf80bd630faefbe10ddbacf2c09a1fbdcb663e6fa67bfbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.4 MB (329405559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cb3b07947a36f1548be857ddc383adff78802f9e876a55b6a82099ebb6ebd60`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:24:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 20:14:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 09 Mar 2026 18:36:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Mar 2026 18:37:51 GMT
ENV GOTOOLCHAIN=local
# Mon, 09 Mar 2026 18:37:51 GMT
ENV GOPATH=/go
# Mon, 09 Mar 2026 18:37:51 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 18:37:51 GMT
COPY /target/ / # buildkit
# Mon, 09 Mar 2026 18:37:54 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 09 Mar 2026 18:37:54 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:ac9148dc57ca750b09f3f3da6f16324e1a3b62432b2726734535ec610e1a9232`  
		Last Modified: Tue, 24 Feb 2026 18:42:56 GMT  
		Size: 49.7 MB (49652168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95da832d1713c4ed161275cd40c4161680fbdd97c6faf23e71654d26bb2e58d6`  
		Last Modified: Tue, 24 Feb 2026 19:25:09 GMT  
		Size: 25.0 MB (25023493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c46eec5989abc098640d80ee9b97658d4487864f3268219dadc63c0a047866`  
		Last Modified: Tue, 24 Feb 2026 20:15:09 GMT  
		Size: 67.6 MB (67585551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0966bbd83d0ca85b572b4e9b1b34f23706647722e1d201fac83b9eb4c01c73cd`  
		Last Modified: Mon, 09 Mar 2026 18:38:20 GMT  
		Size: 98.3 MB (98310508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1276795b08c8a192fe74bc0ca89800479d8cab1b3bb0e3b28f26af398b665fc3`  
		Last Modified: Mon, 09 Mar 2026 18:38:20 GMT  
		Size: 88.8 MB (88833682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bf3bdc5a9c6026ea59bc0d30cd967a92dd1f11461cf0b70ab40fe6dda55693`  
		Last Modified: Mon, 09 Mar 2026 18:38:16 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260308-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:7df862ef20d3c423f929acc9ed7b172b0f393b2fd05e70aaa7d5565820d01bd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10935162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:264be3d72a824678e6ca671cb5266e2aee023c585cfbd9cf7dabe20353e9201b`

```dockerfile
```

-	Layers:
	-	`sha256:a6dcf9c0b87b68c819c4696f4956593315375d671c0ae244bfdf3a327e00c712`  
		Last Modified: Mon, 09 Mar 2026 18:38:17 GMT  
		Size: 10.9 MB (10906038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a836edb99d53fc27558bc3d9bb42a3bad19ba7ed01f2ceecd8caf31dcdc0d6d7`  
		Last Modified: Mon, 09 Mar 2026 18:38:16 GMT  
		Size: 29.1 KB (29124 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260308-trixie` - linux; 386

```console
$ docker pull golang@sha256:e371147b394120e44a2aecb2dfa5cf0464836edc312802ba1613025d600c980f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.5 MB (339503771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:740dae54bea77ba9a11ce098735a3f32ba4486a0b24c91ae7c4ce29740ad391b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:24:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 19:57:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 09 Mar 2026 18:21:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Mar 2026 18:23:39 GMT
ENV GOTOOLCHAIN=local
# Mon, 09 Mar 2026 18:23:39 GMT
ENV GOPATH=/go
# Mon, 09 Mar 2026 18:23:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 18:23:39 GMT
COPY /target/ / # buildkit
# Mon, 09 Mar 2026 18:23:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 09 Mar 2026 18:23:41 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:cdaf5c618b8ff25cb29f813a6c008ca0cb7de6fe5f93f3ba4939cc9fc10fc6cc`  
		Last Modified: Tue, 24 Feb 2026 18:42:38 GMT  
		Size: 50.8 MB (50805272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c637225671ff7a033f6873454fdf6a539c15748206b024d30b37d32f91f3c21`  
		Last Modified: Tue, 24 Feb 2026 19:25:06 GMT  
		Size: 26.8 MB (26779652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15c73fe9d5e539e615e830926d2ddb692fd4ffb36bb2ea42d3131dcab6528d49`  
		Last Modified: Tue, 24 Feb 2026 19:57:28 GMT  
		Size: 69.8 MB (69794855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d144701cd965f1d258a3f5e55094c3a925f204fd137d6f9d08743d5bd22b4916`  
		Last Modified: Mon, 09 Mar 2026 18:24:06 GMT  
		Size: 100.6 MB (100607955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c8181476688ce59990f6e1b32458c610684950481d47bcb0583cc777042e4e2`  
		Last Modified: Mon, 09 Mar 2026 18:23:47 GMT  
		Size: 91.5 MB (91515879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3615a554a1ce9e4ec5084e924bdef392abd16abcac4c744c7e103138ce35f6`  
		Last Modified: Mon, 09 Mar 2026 18:24:04 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260308-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:4ed78062c95ea3ffda288b39da47ba0dca7653dfe9a673ad55275dfc01f01e04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10785772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:820f3dd176de5f2047ab18b7ce95e3b541749aa5a8891b1c35c425b727902029`

```dockerfile
```

-	Layers:
	-	`sha256:9293cbe7183fac9dbec1ded76e164380001c769171848c08b38f3ce9aeb784aa`  
		Last Modified: Mon, 09 Mar 2026 18:24:04 GMT  
		Size: 10.8 MB (10756846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4188cd16be52c882fcabac15841960ce38be1e659830eb5a2fa9c8320d01857`  
		Last Modified: Mon, 09 Mar 2026 18:24:04 GMT  
		Size: 28.9 KB (28926 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260308-trixie` - linux; ppc64le

```console
$ docker pull golang@sha256:2598dcae2e789b0054d6eea947022270d3b2aeb6f12a74ee9133defb3326ac41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.4 MB (336388581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0001e5e1394152f0aa37c4ee6989404fce09334ecb780da02bd8034dce6db491`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 21:23:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 25 Feb 2026 02:58:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 06 Mar 2026 01:10:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Mar 2026 20:29:53 GMT
ENV GOTOOLCHAIN=local
# Mon, 09 Mar 2026 20:29:53 GMT
ENV GOPATH=/go
# Mon, 09 Mar 2026 20:29:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:29:53 GMT
COPY /target/ / # buildkit
# Mon, 09 Mar 2026 20:30:01 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 09 Mar 2026 20:30:02 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:468eb7cd0e9ceb9e5b1c4c9daadd36c2fd1f1ee82c667dc1a7d70fa95600a20f`  
		Last Modified: Tue, 24 Feb 2026 18:45:11 GMT  
		Size: 53.1 MB (53112261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b88c878e5079331d2b0e1bf13313604e6e446232728ee7b159499795ff9def2`  
		Last Modified: Tue, 24 Feb 2026 21:23:39 GMT  
		Size: 27.0 MB (27004375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8078b8ed13f55a8d2e3bc098e87fe680e2a4289c11315d3e460db7bcd51cc93f`  
		Last Modified: Wed, 25 Feb 2026 02:59:03 GMT  
		Size: 73.0 MB (73022125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784245641f5583c22125d8b1795377396b0329cd3dddb9ca69cbe55bdfecb75d`  
		Last Modified: Fri, 06 Mar 2026 01:12:06 GMT  
		Size: 92.9 MB (92868135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd4a2e00fb2b423a29812f722692ff6df643271561859f95cff5536124a1105`  
		Last Modified: Mon, 09 Mar 2026 20:30:57 GMT  
		Size: 90.4 MB (90381527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a66106252fdbdd44e1470b3ea335b7f5820f3901394ae55deb5ed4f57dc6043f`  
		Last Modified: Mon, 09 Mar 2026 20:30:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260308-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:190475ee63ab7a200e5e3ccd1d9aaf619060be7f754e80f4b7ccde229f40bd66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10810220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31835309901addadb7b630beaad3ef64f14beefca63a0e83c94bcb24f1736e29`

```dockerfile
```

-	Layers:
	-	`sha256:5706589ee408f72d54fd0ec5b61ddfd9fd455fa170e64d5ff8561c5fd3b3e8e1`  
		Last Modified: Mon, 09 Mar 2026 20:30:54 GMT  
		Size: 10.8 MB (10781371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29374705caa576ed92f8fd76b3dab01bf44b9caecc263f96b9e4d8d6cbfca3ea`  
		Last Modified: Mon, 09 Mar 2026 20:30:53 GMT  
		Size: 28.8 KB (28849 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260308-trixie` - linux; riscv64

```console
$ docker pull golang@sha256:904db62631623b69a814a12d674554c616481f8ae648772182e8fa7e72d5a089
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.9 MB (361890384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f9d5e77bd73ef78664daa32d025e99ccdb0fee430f1dbe4d90dde689cf5b599`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Thu, 26 Feb 2026 21:43:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sat, 28 Feb 2026 19:58:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 03 Mar 2026 01:38:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Mar 2026 05:52:34 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Mar 2026 05:52:34 GMT
ENV GOPATH=/go
# Tue, 10 Mar 2026 05:52:34 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Mar 2026 05:52:34 GMT
COPY /target/ / # buildkit
# Tue, 10 Mar 2026 05:52:52 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 10 Mar 2026 05:52:52 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3be247472b67578a1d05739722d8adeca41098796e5d6210800176db58046fa7`  
		Last Modified: Tue, 24 Feb 2026 18:57:42 GMT  
		Size: 47.8 MB (47776936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115c3a1cec8ab5f3346656c92bb6a04391222dacf945336ca2f360cb9afa1d32`  
		Last Modified: Thu, 26 Feb 2026 21:45:21 GMT  
		Size: 25.0 MB (24951819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1aad3c88d849328eee587bd71226c07edf0e2f5081fc7ec8dc66c3ee7e1d0c`  
		Last Modified: Sat, 28 Feb 2026 20:02:17 GMT  
		Size: 66.7 MB (66662373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b37ae9709038f63e30e164a548c422deaa7a5733b337f89853b60db2fe5818b5`  
		Last Modified: Tue, 03 Mar 2026 01:47:15 GMT  
		Size: 131.7 MB (131650592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06c7e21ca679669eaa5e0dca220f9983edae380dc375409350bb3f1d989582ea`  
		Last Modified: Tue, 10 Mar 2026 05:59:32 GMT  
		Size: 90.8 MB (90848505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:021586a185c7023211a1fcd5f8f9573afa44f708231aae4ec4671a3c7e36b777`  
		Last Modified: Tue, 10 Mar 2026 05:59:16 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260308-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:25f9ef157e26fcbd290700f30c32f830bce75df739a566b6bf9fecbe147638ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10884230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a1c971ac4a9dbb8253de3508e4333d10561b01b2bb9f195d8c3fabbaf77eb97`

```dockerfile
```

-	Layers:
	-	`sha256:7cddbfb1968f463f617158e7e3b98d56a67ba87536050c65dcc37bc29cdf3c53`  
		Last Modified: Tue, 10 Mar 2026 05:59:19 GMT  
		Size: 10.9 MB (10855204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a102886fce3be24749565a22b5f449d4bf79f3ce4e7e03c8f8b4b648c2f00f9a`  
		Last Modified: Tue, 10 Mar 2026 05:59:16 GMT  
		Size: 29.0 KB (29026 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260308-trixie` - linux; s390x

```console
$ docker pull golang@sha256:1d32b700a003c3b16ca3575d6c457d26bb08e1e933c513907527b0e980b7f18a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.6 MB (313627055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05a7e4e7506268e3517903ca1d45449b6746eb0e94314946a89292044670acae`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 23:53:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 09 Mar 2026 19:01:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Mar 2026 19:04:47 GMT
ENV GOTOOLCHAIN=local
# Mon, 09 Mar 2026 19:04:47 GMT
ENV GOPATH=/go
# Mon, 09 Mar 2026 19:04:47 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 19:04:47 GMT
COPY /target/ / # buildkit
# Mon, 09 Mar 2026 19:04:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 09 Mar 2026 19:04:49 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:aba9aa950add2749194487d5c63a3069af6daf9dfe54d80cfbe32bfa7a5faa07`  
		Last Modified: Tue, 24 Feb 2026 18:43:53 GMT  
		Size: 49.4 MB (49354534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b9712b896509afe6ce616cc91aa36b272afd379950384122674a69ff7d6929`  
		Last Modified: Tue, 24 Feb 2026 20:59:42 GMT  
		Size: 26.8 MB (26801071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d62d9ba5f66f052b2790c9aa6ddd7ff161b24db86972e603be616bc922281de`  
		Last Modified: Tue, 24 Feb 2026 23:54:27 GMT  
		Size: 68.6 MB (68624526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2b92921af416762f12257eaa5ab48c7f1e1636c539686297562a82de5adfa2`  
		Last Modified: Mon, 09 Mar 2026 19:05:31 GMT  
		Size: 76.0 MB (75980200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdeaa76acf61a14d8cb194df2a407d1383d717722d6e254333be0cf42263af58`  
		Last Modified: Mon, 09 Mar 2026 19:05:28 GMT  
		Size: 92.9 MB (92866565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0049d49c7d7b1687d97393d9d79ded5d6659dc53e20117bc710f7377f8dd95`  
		Last Modified: Mon, 09 Mar 2026 19:05:27 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260308-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:f61d76a4564bd7d765ccc0e82ca74f3ada54780f7a0733a4a3c5680c4d407d78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10624947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efa8b1c2b12f6f8937f31f9011e6f00b3dd2e546e6240a44a8b05514a8b5d423`

```dockerfile
```

-	Layers:
	-	`sha256:a5428b5d1dc3ea2f32c63cce7a6b036dd21681b24b8cb4e36095d8b869cea976`  
		Last Modified: Mon, 09 Mar 2026 19:05:29 GMT  
		Size: 10.6 MB (10595983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b09e8e66f1566ca5e72e473ad64539bd331ea953fd564b425f178cbee9cc2ab9`  
		Last Modified: Mon, 09 Mar 2026 19:05:28 GMT  
		Size: 29.0 KB (28964 bytes)  
		MIME: application/vnd.in-toto+json
