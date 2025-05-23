## `golang:tip`

```console
$ docker pull golang@sha256:37cbca617bac78fb0d76a4119091fec4a884c980188a5025d675bc26318be37f
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

### `golang:tip` - linux; amd64

```console
$ docker pull golang@sha256:eb5d4233dddf2ff2f8415b4e313ed04c433ed32eaffae2e80947b4affac7973c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.9 MB (356862763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd1bfcb631b7c8e25b346e75afb61994309ead8e2e0e8d50fd0311739e842488`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 May 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 May 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 19 May 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 19 May 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 19 May 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 19 May 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 19 May 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3e6b9d1a95114e19f12262a4e8a59ad1d1a10ca7b82108adcf0605a200294964`  
		Last Modified: Wed, 21 May 2025 22:27:42 GMT  
		Size: 48.5 MB (48488245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37927ed901b1b2608b72796c6881bf645480268eca4ac9a37b9219e050bb4d84`  
		Last Modified: Wed, 21 May 2025 23:20:21 GMT  
		Size: 24.0 MB (24015635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b2f47ad4443652b9b5cc81a95ede249fd976310efdbee159f29638783778c0`  
		Last Modified: Wed, 21 May 2025 23:37:25 GMT  
		Size: 64.4 MB (64399858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2565bc9009fb96ce1c2cf5833a62a02cfc8c415ab0128c3751fc6bf2509c6f33`  
		Last Modified: Thu, 22 May 2025 01:14:13 GMT  
		Size: 92.3 MB (92344740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3152514912bccc29796b149fde0366f2c5aabf882d40321f8719bdbe9b9c2cb5`  
		Last Modified: Mon, 19 May 2025 23:28:50 GMT  
		Size: 127.6 MB (127614129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cc9ecc0f2be8495de632a500a7c59599e8cf7c3ef9470cbd1f0743212d8cc23`  
		Last Modified: Thu, 22 May 2025 01:14:12 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:52db730fe7c6994e6379cbd3cbe2b152a8ade07d6c3d4674dc4a34c6cb26b9cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10340784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6051f7b1dc780a8fe9cb75b5d5f5bc3d9cdf7f2bd2d927758c3064d383ace39a`

```dockerfile
```

-	Layers:
	-	`sha256:0dbb5f83ddf07e0f4742198afb0a15af00f330ab33a161f3c48de7115430b2e8`  
		Last Modified: Thu, 22 May 2025 01:14:12 GMT  
		Size: 10.3 MB (10313121 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2456d00b6f142c464e4529503102bb8077520fa21919d83cdda8dddb7ad776b`  
		Last Modified: Thu, 22 May 2025 01:14:12 GMT  
		Size: 27.7 KB (27663 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; arm variant v7

```console
$ docker pull golang@sha256:303644135d232706ece75a6963c1e8458ea7f224b7e386f6082e9f7493d925d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.5 MB (314502303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd062d8ea9fc60d7c7e74f9c26a4ea04ff7541595e3a4b333724ea34d2f7299c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 May 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 May 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 19 May 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 19 May 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 19 May 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 19 May 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 19 May 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3a781f536825e084b88c231841be4d1c7df016a4aa2ebdd27d7431b5f1ab3419`  
		Last Modified: Wed, 21 May 2025 22:27:37 GMT  
		Size: 44.2 MB (44202771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b02150b4002b569f2f9be5055a06c94a228e07937f6f39fd4d84b52042b2f01`  
		Last Modified: Thu, 22 May 2025 02:28:04 GMT  
		Size: 21.9 MB (21924635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c061a668a2586bc3366d21d8a069b30ac6fdff27bb5140a653d59b71241213`  
		Last Modified: Thu, 22 May 2025 12:11:29 GMT  
		Size: 59.7 MB (59656286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6769ccbcbb302e58183ef7d1b1458e5ec9e4e0e712cf266d56ddefb34341bfd`  
		Last Modified: Thu, 22 May 2025 15:40:09 GMT  
		Size: 66.2 MB (66210504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa57e96661f23b74a5007ca5b539e5d28d960192676ad8b6b38063081e7fce05`  
		Last Modified: Mon, 19 May 2025 23:31:19 GMT  
		Size: 122.5 MB (122507949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903bf6c3221c6aecb4bb6645e1a70e968f4c75eab5f4e0cb037d4f697384f7fc`  
		Last Modified: Thu, 22 May 2025 21:43:38 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:def77dda3ac2d5813748a414492fe03b50e11d7c48e90f96927540cccac537df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10147593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7134476456671c1c9d99873b51cffc7abdcea1604bf7d5a167cbb9bb916120bc`

```dockerfile
```

-	Layers:
	-	`sha256:07b08f8170f11dd6160b73b622f324a4d56eee4eb0c0607754ad30889b173bdc`  
		Last Modified: Thu, 22 May 2025 21:43:38 GMT  
		Size: 10.1 MB (10119806 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b5f87025bf8f8d2090ca0daf7dd1dc0d3d2901a6e24ed14be18a6fa1b590eb5`  
		Last Modified: Thu, 22 May 2025 21:43:38 GMT  
		Size: 27.8 KB (27787 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:18f4cb28bcd302b93bf2b90974994bca13d69bcea0f7f1e665ad4c43245231be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.9 MB (342915999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:677e2e4f98b826c3165ad063654240b5ac09572cb4f56163c96b60bbc38ad00a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 May 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 May 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 19 May 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 19 May 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 19 May 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 19 May 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 19 May 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1a12b4ea7c0ce04aa0e98be0a8c9942162bac71426f734fe6d3bf988bc9e2627`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 48.3 MB (48327181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280bbe393e788ced1dcb033580604b24de083601624337be66b3ec31781dae40`  
		Last Modified: Thu, 22 May 2025 02:47:26 GMT  
		Size: 23.6 MB (23551398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4f297e4f699ae0f384d5cc1ea42065f58a115aa0a634d427cbb186f91cb4d0`  
		Last Modified: Thu, 22 May 2025 09:17:58 GMT  
		Size: 64.4 MB (64361989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e45158653cee17fd0433bb95f654076603c1dace770784457d1f08ffc1f1bd`  
		Last Modified: Thu, 22 May 2025 12:32:49 GMT  
		Size: 86.4 MB (86409121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583af8027226f07cd540ce15387789410501e4b5b5d00ffa1a05fcb1dc81e7e9`  
		Last Modified: Mon, 19 May 2025 23:28:57 GMT  
		Size: 120.3 MB (120266151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:747173d44b3d280f66954cd12a50c319140d75bd8ae9c02e38eb5be156502d34`  
		Last Modified: Thu, 22 May 2025 15:25:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:583c87f167b97db77da00343fccffe91d523516eda34d112f7f47d5a6a0e2787
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10368791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ca81fd939d02b4102f6974627afbbe4bf88220d3eb29bf6c322a5d67cbbab95`

```dockerfile
```

-	Layers:
	-	`sha256:e36a29ee92551ac687cc2e75b76a6cd025d54fecab5c266d8bd00cd5349718b1`  
		Last Modified: Thu, 22 May 2025 15:25:10 GMT  
		Size: 10.3 MB (10340968 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ae58604a6bd43df4e6032f7637fb09fa7bf3b7e1a12b6d9227d310bdae32d28`  
		Last Modified: Thu, 22 May 2025 15:25:09 GMT  
		Size: 27.8 KB (27823 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; 386

```console
$ docker pull golang@sha256:f9d8ff189642bf8c7d2b4f8a4534bce054f178e0ef9530431c2deb54fd78cdff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.0 MB (356023931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:873041f0f8cbd65f98b0be09162c05a92c343bc64a8dcc2720db97897bd8745c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 May 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 May 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 19 May 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 19 May 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 19 May 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 19 May 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 19 May 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7bdd0d6ce898fe017a461e5f67ccf41a15f147063ffe1c496fb7e5f75037adfb`  
		Last Modified: Wed, 21 May 2025 22:27:49 GMT  
		Size: 49.5 MB (49471562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296134322e370a0aab10509f2b47d9ce416e7da5a792e7f8badd9284ecbabeb0`  
		Last Modified: Wed, 21 May 2025 23:20:06 GMT  
		Size: 24.9 MB (24855668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc8c7f8292580c2c70e8cb47ec957249f0882ee6ee3737bf3250e44650a38db`  
		Last Modified: Wed, 21 May 2025 23:37:30 GMT  
		Size: 66.2 MB (66224115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11465fbe6bfea0c967beb951cf984843e7b0a6e611b4b606d88f42e24ed43744`  
		Last Modified: Thu, 22 May 2025 01:15:03 GMT  
		Size: 89.8 MB (89774989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24d8be6f5d36fbc3aec81708ca11efa4fc67dbd10e5ba59a5e7c3fa29e59478`  
		Last Modified: Mon, 19 May 2025 23:29:26 GMT  
		Size: 125.7 MB (125697440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0472e4ae4663cb8fe1eb046e73d9dd313405c36f76d6d991e86a07797dc343e`  
		Last Modified: Thu, 22 May 2025 01:15:01 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:3276320439bb7e54a14cc68dad316d5f83410a3f151617537323350c93bce072
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10320294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d648dabcd42b3a77702686a6784d2968dc333d1ca4c4453885b2cdb7ee8bb44`

```dockerfile
```

-	Layers:
	-	`sha256:1c8f042a4f6249fa380bdd44d38e5f7260099d00d89cb399a4b6c7a09d21d265`  
		Last Modified: Thu, 22 May 2025 01:15:01 GMT  
		Size: 10.3 MB (10292675 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5683c239b0da1e5e8f62e3f0da054b7a84fb65164c53aef5e63ff4f94dc0bad4`  
		Last Modified: Thu, 22 May 2025 01:15:00 GMT  
		Size: 27.6 KB (27619 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; mips64le

```console
$ docker pull golang@sha256:e79bfb0f312bc4024a97bd1fb81f8ab53ac93e68fe8fcff061234530bd5b3886
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.4 MB (323433568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e457160701b464506a3bc36f708ef400c496036cd8004501e3e5b771e04f844f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 May 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 May 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 19 May 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 19 May 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 19 May 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 19 May 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 19 May 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:fa5acbf36757d3126014bc0e0a159fb5593a1d68ddba5992ef7ac9aa3e7db8dc`  
		Last Modified: Mon, 28 Apr 2025 21:10:59 GMT  
		Size: 48.8 MB (48775438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d3e6811de68483322bf4607ec4cf0620d9d7f95dc19ce670b2ee81bd283341`  
		Last Modified: Tue, 29 Apr 2025 12:43:07 GMT  
		Size: 23.6 MB (23595734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1d30b00e6e88ef455123e625951481f519a50849cb9e967c590e851c17b408`  
		Last Modified: Tue, 29 Apr 2025 21:16:09 GMT  
		Size: 63.3 MB (63308148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c420f992cbaa8d211ae04be243041a640a38dda712f3d832718a146e390dd6fb`  
		Last Modified: Wed, 30 Apr 2025 03:40:22 GMT  
		Size: 69.9 MB (69942341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3870f35f75c70770c13c8f4b7846de058ba02ecbae8c63862144379f0bc07cad`  
		Last Modified: Mon, 19 May 2025 23:48:02 GMT  
		Size: 117.8 MB (117811749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3bd239d44e58206511e32525857232f94bc5ff0f4fc8421fcbcd74fb4d815f`  
		Last Modified: Mon, 19 May 2025 23:47:51 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:0f77fbfeb32713d8b2accbd40033b6e6ca762f3f85afb5137e36f38a280f2954
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 KB (27534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e265e2183782a06e89c673b6079d7cfcf8b9b49211afc412d7ed5dd4304b5ff`

```dockerfile
```

-	Layers:
	-	`sha256:797f5959dba7b9c1d7b0079a81e2d5d2ddfdc25c2983f6f2561aded822a9a14d`  
		Last Modified: Mon, 19 May 2025 23:47:51 GMT  
		Size: 27.5 KB (27534 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; ppc64le

```console
$ docker pull golang@sha256:1a2ca311b8dd717c68286cda838b6df1f1031ab1e85b3f3b857b785b7c41c1b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.6 MB (360568700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f911f41be92efeae56f0f849872b24d7aeecd23415151f8cc991fc028e00c5db`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 May 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 May 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 19 May 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 19 May 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 19 May 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 19 May 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 19 May 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:996840ee350796081b3c80118ca1a58ce8212c6fdf88c454706a16457903a0c9`  
		Last Modified: Wed, 21 May 2025 22:27:49 GMT  
		Size: 52.3 MB (52331619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d82206e3ae1269ed70d5c84db92f6478d2de4719db96fab0f36254db269f0fa`  
		Last Modified: Thu, 22 May 2025 11:54:40 GMT  
		Size: 25.7 MB (25657297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c498d213a2aac9e38fe414de433d75bc8ba03faa40c2b4f0690897cf17174f58`  
		Last Modified: Thu, 22 May 2025 16:52:03 GMT  
		Size: 69.8 MB (69839678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc3651009f91cf27e970ae7dc7349e20fba94b97f4d2143617e748afd3d930d`  
		Last Modified: Thu, 22 May 2025 17:40:50 GMT  
		Size: 90.4 MB (90354720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3625dd3861bcafa29471847412cc81631c8096f3d258fbc027fee8d5eaf7e70a`  
		Last Modified: Mon, 19 May 2025 23:29:10 GMT  
		Size: 122.4 MB (122385228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e3569984752c4e09f1f0a821a1c3d06d6b41db2ce1961982266f64e63d3f8ed`  
		Last Modified: Thu, 22 May 2025 21:55:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:3962bf2c1c9af2bfd6c47dc741824c9ddc16435a5b2b51bbf7bb00c4fa5dacbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10313346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc2a53d911b4bb352597c0c2d44e5349d7a22ba0fe56c5df974b0141423ed66c`

```dockerfile
```

-	Layers:
	-	`sha256:3f3ece56bd134219fb10f6e8edb2c7180a415d92c1a0876b0c059e7184552394`  
		Last Modified: Thu, 22 May 2025 21:55:58 GMT  
		Size: 10.3 MB (10285625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd4f81a6028b3323aefd22af6292c18487af41fdb88fcd8e10428f6996f7e795`  
		Last Modified: Thu, 22 May 2025 21:55:54 GMT  
		Size: 27.7 KB (27721 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; s390x

```console
$ docker pull golang@sha256:d70f4a0c87687c8a774d079afd0cb1339504afffcd69d80d42b49335dfcb3408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.4 MB (328393588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b30db890b3522702e5126378d995c68b64add7c0982f36dc2af0215f0697f182`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 May 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 May 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 19 May 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 19 May 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 19 May 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 19 May 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 19 May 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:47f9a2c2279c9df9e222a4c8af501e43b0b5e2552eda9597a97162080b8f106b`  
		Last Modified: Wed, 21 May 2025 22:28:14 GMT  
		Size: 47.1 MB (47143842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86a43d043466908a6aee9cc569c707c9cb9b87fe3e55b5a27e7fe7f7f27d73c`  
		Last Modified: Thu, 22 May 2025 01:01:58 GMT  
		Size: 24.0 MB (24014856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85bf0b00f04b5784c02aa34bd5edd104e26e960d8480606e6f206c6a22330235`  
		Last Modified: Thu, 22 May 2025 04:37:16 GMT  
		Size: 63.5 MB (63498527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd113c317127acbfc86d7af2a1be3cb7e330fa8c58847cef98b51c46d4e19c94`  
		Last Modified: Thu, 22 May 2025 06:45:25 GMT  
		Size: 68.9 MB (68943692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd075cef311d6599616d573e5ef671ecd5f92da8e8f3aacdc51de2708883d635`  
		Last Modified: Mon, 19 May 2025 23:29:02 GMT  
		Size: 124.8 MB (124792513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b143f582acd076a1ac9a0dbc51225c98e95b36dec10e9bb537a51ea14837ed`  
		Last Modified: Thu, 22 May 2025 09:45:49 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:688e133b28ecfe8a6c922c3ccf215e0751dd0f4ecf391df38049961f88fa07ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10175435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7990e1b176e144979e3456b07e64b4444e0dfac8dd26ef6822ba30571117f16`

```dockerfile
```

-	Layers:
	-	`sha256:c8cdb2edf479f9eca9006bcdf0601fe70075fda36b76a15f63d08e32c7e0640d`  
		Last Modified: Thu, 22 May 2025 09:45:49 GMT  
		Size: 10.1 MB (10147772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4df35d1d91e99e28cf298f81f4f89cee21ab32d9a3a9fc65dd05643a0140ea40`  
		Last Modified: Thu, 22 May 2025 09:45:49 GMT  
		Size: 27.7 KB (27663 bytes)  
		MIME: application/vnd.in-toto+json
