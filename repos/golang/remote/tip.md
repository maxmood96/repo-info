## `golang:tip`

```console
$ docker pull golang@sha256:b81adacfbc4dc9f18eff7d9c1450825408e9082069b5bd017d860a9668172429
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
$ docker pull golang@sha256:e56a6f5c4dbc99d9eab0f0d687433daa36e8fdc01dfcfb86fa1b6c0d85c4ecff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.5 MB (314486247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed985e5da389f1c23b666d107ac142b6029f4362481ddb4c294b943b121afbb9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
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
	-	`sha256:a735d4b4a53e8e11448d15bc50ce4670d54dff52e426cf0510c9b713d3a7ad09`  
		Last Modified: Mon, 28 Apr 2025 21:15:27 GMT  
		Size: 44.2 MB (44197079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b01e6436acd06b177253a4ba25e5179715088c2f493e89c91bbf6fdc41a2034`  
		Last Modified: Tue, 29 Apr 2025 03:37:10 GMT  
		Size: 21.9 MB (21918380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3553b1499305feec4f182c1e2562e06daaecb3dc337d83b89b8c909f46c0a1`  
		Last Modified: Tue, 29 Apr 2025 13:22:56 GMT  
		Size: 59.6 MB (59640211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6442f47db55887d087c4346d5fccc35d5cd8441653b35deaf402943d7978ae1`  
		Last Modified: Tue, 29 Apr 2025 16:59:19 GMT  
		Size: 66.2 MB (66222470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa57e96661f23b74a5007ca5b539e5d28d960192676ad8b6b38063081e7fce05`  
		Last Modified: Mon, 19 May 2025 23:31:19 GMT  
		Size: 122.5 MB (122507949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19a6d43eaefa64fa103aee4321ee503de6f4fcebe15228a2850f1e2e40672275`  
		Last Modified: Mon, 19 May 2025 23:31:15 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:a1f3688f02f325daf31b710dac77ec4fc572da2c465212965f21c658ae389ab2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10148902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a46a1b5a738c8adb14f6d190eef31344304da94e7db703b2dfede69e1c8e11a1`

```dockerfile
```

-	Layers:
	-	`sha256:eb6a259a40f60588ebb2cf2000893aa2fbcb620e0bec8cb2f09937a7890ef6c7`  
		Last Modified: Mon, 19 May 2025 23:31:15 GMT  
		Size: 10.1 MB (10121115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28f8508a269534815fdd6d6858287c81f0fcad49a0b3fce8ecabb6c9b0fa07b7`  
		Last Modified: Mon, 19 May 2025 23:31:15 GMT  
		Size: 27.8 KB (27787 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:75afa3846048edd9f46c13e3a94437aad8d186c88ef8e230afc4110bd78b36b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.9 MB (342909302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd25702655178b10c7fab84d9baa8848b86bf37100c81d2ecbb11d912fa44f15`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:de07ba6f486e0ce29760ab32d4381edabbc660a04c493e95eb9a8056925d8955`  
		Last Modified: Mon, 28 Apr 2025 21:20:23 GMT  
		Size: 48.3 MB (48327644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84649bff67ea459549b6f371f7045d9968d6ebf370b815c922a625f3ab065724`  
		Last Modified: Tue, 29 Apr 2025 01:46:47 GMT  
		Size: 23.5 MB (23544262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a2a14f59a002f5ef50911a0687d30beadf65bbe35bde8bd3823c3496cbd465`  
		Last Modified: Tue, 29 Apr 2025 18:37:11 GMT  
		Size: 64.4 MB (64355683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:919170863bb5513bdfe1ce20b4f372538ef99b950b570408aa6aec57bfd91916`  
		Last Modified: Wed, 30 Apr 2025 02:34:40 GMT  
		Size: 86.4 MB (86415404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583af8027226f07cd540ce15387789410501e4b5b5d00ffa1a05fcb1dc81e7e9`  
		Last Modified: Mon, 19 May 2025 23:28:57 GMT  
		Size: 120.3 MB (120266151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef6ff84462a6e33d3265205e12a954726ed1a05fa32c33b0eda897a3835b89c0`  
		Last Modified: Mon, 19 May 2025 23:28:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:bedb325e8ec208c54ccf6f8a2a609e50e7fae8d20e95c24fb749aedea6bb07de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10370028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1feeeecd7fcf9dcb0844b232d541e7d5c7d10577c10ee9b1fcd610aaad2a6f91`

```dockerfile
```

-	Layers:
	-	`sha256:7189ca426d30a8f21e436602a28ef678aabd483cb2f4f8661714532394d2ba45`  
		Last Modified: Mon, 19 May 2025 23:28:55 GMT  
		Size: 10.3 MB (10342205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa4d83ed52a0db65c0da1ba06f90b5ce6db4892c0d41d555e8cb49bff7050c95`  
		Last Modified: Mon, 19 May 2025 23:28:54 GMT  
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
$ docker pull golang@sha256:fc1e57739b1606604ef1e94780a45e6dcc33ed47bb81c4d3971c8471edf42a6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.6 MB (360558441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc4cbdb39ee0aab8d520aa3e4269d093cd7f3693bfbe178cacbe8b539b73191c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
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
	-	`sha256:33862e890d6c23fba01df0303b503e727dad5c72574fdf8af76d76dc3140d561`  
		Last Modified: Mon, 28 Apr 2025 21:21:34 GMT  
		Size: 52.3 MB (52332129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4617415431bf61f96c81d815cfb6cf010eef7bd0d8a8de24b02c1a7fe8407026`  
		Last Modified: Tue, 29 Apr 2025 07:46:58 GMT  
		Size: 25.7 MB (25650113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae70f40efc6df1466aa415707fbf58268a1633e6ab2dde78f23ec024d7c1e42`  
		Last Modified: Tue, 29 Apr 2025 08:29:00 GMT  
		Size: 69.8 MB (69840424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d38985afc96fb14b472c445470120222b7866d3e3e26c3337d073be6739a829`  
		Last Modified: Mon, 05 May 2025 18:58:04 GMT  
		Size: 90.4 MB (90350389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3625dd3861bcafa29471847412cc81631c8096f3d258fbc027fee8d5eaf7e70a`  
		Last Modified: Mon, 19 May 2025 23:29:10 GMT  
		Size: 122.4 MB (122385228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4f4b399f8d7de7e5917c1bb3d00c399356b26bac3e428521428bd5c94baa16c`  
		Last Modified: Mon, 19 May 2025 23:29:06 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:f0055f1bfec9079017a3d03e5a8537ae043e6d55722488d9f940cf60ff342701
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10314587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:752122930254797e2393e709da094fa60c1f1148165ada96f8c831c8740ddc30`

```dockerfile
```

-	Layers:
	-	`sha256:e55375acc918c795abea11f0784dffb5a81fde9ced8f6b460c372295ed4f8364`  
		Last Modified: Mon, 19 May 2025 23:29:06 GMT  
		Size: 10.3 MB (10286866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae4f8ce2d2b71aeeba2b26baad72bb2009652db58b4d79e0de9591efa782531a`  
		Last Modified: Mon, 19 May 2025 23:29:06 GMT  
		Size: 27.7 KB (27721 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; s390x

```console
$ docker pull golang@sha256:e9786d461f280fe758a724e2d0eda6e2fa802544102a15cbe6df9164660763fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.4 MB (328387339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65a6e04b154ab05a3bed2bae05c2baf1d1012e9cd74aab3761e7087569e4d400`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
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
	-	`sha256:a5e7ec27bb28a531688c62bada8c4b448d8e280327ecabb8be798bc43be30c38`  
		Last Modified: Mon, 28 Apr 2025 21:07:54 GMT  
		Size: 47.2 MB (47151332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05c607354a47eba0ce7493f4dc26e0f40aaeea360944111a83eeeeb61083045`  
		Last Modified: Tue, 29 Apr 2025 00:01:21 GMT  
		Size: 24.0 MB (24008311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15250b46b7f7ffe8ad5ce0f3a2d64d0437e4fdf3d36b87579551846c0b2dd2bc`  
		Last Modified: Tue, 29 Apr 2025 02:58:48 GMT  
		Size: 63.5 MB (63496877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d09d77a76fd2957750185d2378dd52b653f61b03e2e717f3f19442ac80e377a3`  
		Last Modified: Mon, 05 May 2025 17:53:08 GMT  
		Size: 68.9 MB (68938149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd075cef311d6599616d573e5ef671ecd5f92da8e8f3aacdc51de2708883d635`  
		Last Modified: Mon, 19 May 2025 23:29:02 GMT  
		Size: 124.8 MB (124792513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2960be66c187f61c4a03c16477d8e7ff8d322dc742516357310c92ae7778e0c8`  
		Last Modified: Mon, 19 May 2025 23:28:58 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:3298bb53129599a69e5391d24cafca7f47866a042da04b1b4ab12fca7c8270fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10176726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa7231e02798b93a6cc5171c531646adde244306f72e69f1847e6b55878bdbb9`

```dockerfile
```

-	Layers:
	-	`sha256:77bb7d5a5d594f5f8515cb5dd9fb038754f6bff0905fff2e6a68419bf9ecc17f`  
		Last Modified: Mon, 19 May 2025 23:28:59 GMT  
		Size: 10.1 MB (10149063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67ed49994e1c6d27b1de8deccb2eced75e09ae4f3b93302d6bc8fca594f9bb73`  
		Last Modified: Mon, 19 May 2025 23:28:59 GMT  
		Size: 27.7 KB (27663 bytes)  
		MIME: application/vnd.in-toto+json
