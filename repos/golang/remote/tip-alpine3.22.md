## `golang:tip-alpine3.22`

```console
$ docker pull golang@sha256:d768232ac9b1b052a5ee8077fd6f3019f0d8642fc4caaeb0672580f815eb6e4d
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

### `golang:tip-alpine3.22` - linux; amd64

```console
$ docker pull golang@sha256:39afa90aad71807ba2b2ff3e991eff73b1a40df1453285ffca2782687240a21c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88691058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d732415f0bc3ca4ab0a892e852380b5c626aaa67829b34e3160c92e3ea71c27e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 06 Oct 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 06 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc33d4845d10c722bdd395df2999eb68ef9fa2e6905c86edeb5e660afc26f46c`  
		Last Modified: Mon, 06 Oct 2025 21:04:03 GMT  
		Size: 291.2 KB (291195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df330a3159ef2a0bf41805e9465d878d806cf4287e8fdd250ddbc3e024a94e45`  
		Last Modified: Mon, 06 Oct 2025 21:03:35 GMT  
		Size: 84.6 MB (84600016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:496cc362bc090866acb1fb74ae53330a58a1a1644c4b2343e83b62552e56c6ee`  
		Last Modified: Mon, 06 Oct 2025 21:04:02 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:784cdb859217a6211e4b35a1f6ffb476e1fadcbd93c967a5d4386840d5147bd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.4 KB (220361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85c81653a4f3bcf0c87cfbb8eff88047ddd39ca83e521a1943b4f66633777915`

```dockerfile
```

-	Layers:
	-	`sha256:1aa7357e4fdaa0ba434e076d657e23dc2b1261821f320057e4eb7ae40731d826`  
		Last Modified: Mon, 06 Oct 2025 23:23:56 GMT  
		Size: 195.2 KB (195223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d91a88a917e8422953a13f51c397bfadfccd454fe14dd76bb8f770d666f799e`  
		Last Modified: Mon, 06 Oct 2025 23:23:57 GMT  
		Size: 25.1 KB (25138 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm variant v6

```console
$ docker pull golang@sha256:63d2ed3b2a0ff3fe3a2b9710415d8ab89a27c44e520e1380017429f8706a93ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.6 MB (85594621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77bcb8e926955eeec029eab893db3fcf5a839b6ea5137ecaa1a3cdd2fd031873`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 06 Oct 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 06 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3433734b52fdb7dfb2758f7649e08a485be59bad4abd9775e53b13a3a592644e`  
		Last Modified: Mon, 06 Oct 2025 21:06:07 GMT  
		Size: 292.4 KB (292391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a4ca929e1e82e3da2a8d3fe64f9852116fdde16db4405daccb287d008513ea4`  
		Last Modified: Mon, 06 Oct 2025 21:06:14 GMT  
		Size: 81.8 MB (81801162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acda0015107a00ad8a0bc9ab75a093410f6d0baf75d6a606f222e9e89394f738`  
		Last Modified: Mon, 06 Oct 2025 21:06:06 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:dac3860dcf889eceb7c360d3d8d14e6a0a4a36c31de1466b4f22cec53fd67deb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 KB (25051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b5bc2e6a4b5413e819f3d7712dacad3515ceb8dcd7505413215841d21c06504`

```dockerfile
```

-	Layers:
	-	`sha256:c65c4f740b2975842cbc68c3afcf57722093a5aa5f24a593eb03d748e12ac515`  
		Last Modified: Mon, 06 Oct 2025 23:24:01 GMT  
		Size: 25.1 KB (25051 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm variant v7

```console
$ docker pull golang@sha256:8f422ee8721cee554c2dffcfe1b286ef98011e381363f593d0a5052a917e350c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.1 MB (85060340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1650402f9c7981d4cc8fe644c89d695db940ea3c5989336dd15d1457f2ba8b1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 06 Oct 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 06 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f334558efe263001eb816cfd50474f73300baff3311ad597f3d5cf40b03444`  
		Last Modified: Mon, 06 Oct 2025 21:04:18 GMT  
		Size: 291.3 KB (291252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113454a922f3bf5f9a74062c96cd1b1dd4f7636e5e5993fd895b9a087d38b9c4`  
		Last Modified: Mon, 06 Oct 2025 21:04:32 GMT  
		Size: 81.5 MB (81549892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecbe93d955dc37ac5f3c92eec475228192c16f2ad1c5abbec609a8f0e5b49230`  
		Last Modified: Mon, 06 Oct 2025 21:04:18 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:0b96d22b4d3f3410ace6145814d7f0d255aa1c782856e91a6df324c30dd09595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.5 KB (220511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:586788a2971669d69620fcbe5c741c2e7e37ec31441343370e3a553df254dc6c`

```dockerfile
```

-	Layers:
	-	`sha256:bbc09cf73e7b114cc166b91a9082b6cfa28b9e479bc037aa9e01e896e5e73973`  
		Last Modified: Mon, 06 Oct 2025 23:24:04 GMT  
		Size: 195.2 KB (195245 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7797e2ac47531df9cfe248592e0f7ff2ee4248db245dbe5e82094b4f6d03ce6`  
		Last Modified: Mon, 06 Oct 2025 23:24:05 GMT  
		Size: 25.3 KB (25266 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:52c402355bd4a667cb6037e99647926f4cd55a87a5a3a23113af0833f69360cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.0 MB (84956925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:056ff796f345d12879fcd8128417cf0624ee0233bcaf47a99f78299b09fa2f5c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 06 Oct 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 06 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:776d4bef33441e13dd9a81bd43fe94fffefaf18d1dd2a5e8e43cb59a9c4d239f`  
		Last Modified: Mon, 06 Oct 2025 21:06:02 GMT  
		Size: 294.2 KB (294167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ae6f3de502e34feaea64f03c33850b0abe91d2931d0f357546a0b84a633dd1`  
		Last Modified: Mon, 06 Oct 2025 21:03:39 GMT  
		Size: 80.5 MB (80531850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2884d7f05efd8c95c60981cc05a173587013bdc09319341f3543e93411d9e20a`  
		Last Modified: Mon, 06 Oct 2025 21:06:03 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:772446dfbfb0d071cb6caff245fdd954f6e3ab2c61b0d9c2ffbce6bdce499d3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.6 KB (220577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:634d2a4aa68037061c616e3ae882b4b09effc0b2696bee56152710e15e4c9933`

```dockerfile
```

-	Layers:
	-	`sha256:bf70888fd7dbf7795081ea30c85136cd3e3f5cb56e8450a5ffc01aba44ece975`  
		Last Modified: Mon, 06 Oct 2025 23:24:08 GMT  
		Size: 195.3 KB (195279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab048872bb35366ad4a6de6ea3d01624c304c27c9b4e1fd7ddb0458bd6b6d95c`  
		Last Modified: Mon, 06 Oct 2025 23:24:08 GMT  
		Size: 25.3 KB (25298 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; 386

```console
$ docker pull golang@sha256:568027671cc1272f7349d85eb02f71fb743aee2267c4a1798f23be80784240c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.1 MB (87052306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8277caa3848aaab483b546f6c396120f9b9c6af4606a22685c94a26fa8813ef5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 06 Oct 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 06 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6474bf2e1d942a7da2f4e9e771e763c414067963e70f12bdbc7a599c23ec639a`  
		Last Modified: Mon, 06 Oct 2025 21:04:18 GMT  
		Size: 291.7 KB (291676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1c0a8fc757d99c51188cdf4bad50d211862dd20e9507d39b31fbbec343ddd8`  
		Last Modified: Mon, 06 Oct 2025 21:03:40 GMT  
		Size: 83.1 MB (83145466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28efab3866de96b24e578fc3f9d5f331796099766265a02de99d6aabed15d3c8`  
		Last Modified: Mon, 06 Oct 2025 21:04:18 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:cd13b949a55d20a061d49e78d6992940280592f59adaf690de6190c741130e0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.3 KB (220279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b79b30e7919279945c0e559e9ba992d761352650a393970d0fcd11cbb54ccfa`

```dockerfile
```

-	Layers:
	-	`sha256:daff1d49faa16905e3c27feecfc48b5ad5819f81e5601429348ed3145fbab24f`  
		Last Modified: Mon, 06 Oct 2025 23:24:11 GMT  
		Size: 195.2 KB (195184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ae943fbf99c244ad924450029f8ad3a1319963966df2634df8732c1376569a5`  
		Last Modified: Mon, 06 Oct 2025 23:24:12 GMT  
		Size: 25.1 KB (25095 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; ppc64le

```console
$ docker pull golang@sha256:308392c3926ddcaa02a91b5d456438ffb3d88ab4443c22aecb473a18d3952f47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.9 MB (85889337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a0a68791cf82b50531d7761e173ff3bb1297d7aa634b16b2bb83f3d88dc4656`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 06 Oct 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 06 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaca2bbec3cff414f53adc5e9634f07a3fa7f1e3320dcbcc3b9d03910b13002d`  
		Last Modified: Mon, 06 Oct 2025 21:14:02 GMT  
		Size: 294.6 KB (294637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734f43290ecdfba214453228a07057302573d0be977b7f6d3aeae38f2799df4e`  
		Last Modified: Mon, 06 Oct 2025 21:05:37 GMT  
		Size: 81.9 MB (81867431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbfd394fa84c43756e3b1d3f6fefedf4bbd182e68f2f4c212c4542394e24c36d`  
		Last Modified: Mon, 06 Oct 2025 21:14:01 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:8750484a04a0f0d37d02c43f1bfea92bb94b3806031d049912aa12a697075044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.5 KB (218516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3276e87d84970331db7ba7dafcc4b454cf63d060f00d9a294b5e9fba8a07ee84`

```dockerfile
```

-	Layers:
	-	`sha256:23ec56506c7d1eeed941f38f8c225407e2711721295fe1611f6b5ef33b450a35`  
		Last Modified: Mon, 06 Oct 2025 23:24:16 GMT  
		Size: 193.3 KB (193320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:606af4b2a765a27efb55f08761a40df85fe43a4e9cb95f761cd646ccbd1dfab1`  
		Last Modified: Mon, 06 Oct 2025 23:24:16 GMT  
		Size: 25.2 KB (25196 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; riscv64

```console
$ docker pull golang@sha256:6c7a2e45e669e5b57373db7d2dfa54b60304f0a423ade4073ac8e397f1633290
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.0 MB (86038454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a6bdccfca802d3182be3e30763847e4106233e8b717c72dd725f65f3cfbd2cc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 06 Oct 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 06 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00cc4f79972d3401fde161bf76b9618d80cbd1ea7fcdbebdc630185f4cf612cd`  
		Last Modified: Tue, 07 Oct 2025 14:20:26 GMT  
		Size: 291.6 KB (291608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58fd0ce2ab28438bdf94f05f192ab71a6b801a6c5d6e3d4dc6d664c820e75f2c`  
		Last Modified: Tue, 07 Oct 2025 14:09:36 GMT  
		Size: 82.2 MB (82233887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7013078b33acf26229a2526e4fd4d754f4be2072520e015f94acacdb5d700e09`  
		Last Modified: Tue, 07 Oct 2025 14:20:26 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:a6ef833368e34b6643131442936f8f498a4154efba7c545be6669cf263e057a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.5 KB (218512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6638fccc74d44dfbcaf200a16b7af81f0a06f644c5f5be26c3334014a162344`

```dockerfile
```

-	Layers:
	-	`sha256:a8dea66ff75db5263ab3ce9367debbb6fe866857f2faef2439cef24156df59e8`  
		Last Modified: Tue, 07 Oct 2025 17:23:31 GMT  
		Size: 193.3 KB (193316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63ac3b061017071d10000332db9e6da10a706b96a5fce57e7dd2e1fcb5f098ff`  
		Last Modified: Tue, 07 Oct 2025 17:23:32 GMT  
		Size: 25.2 KB (25196 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; s390x

```console
$ docker pull golang@sha256:3853540cb0e8d4195754613553f7dfe2cab0fdbf7e0c59f2fb77e8ee26d5fa81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.0 MB (86991311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:205d9432a7206df62a8693dc69b9ae67c214a9943a0d1957e941fa476e22c4f4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 06 Oct 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 06 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a4b5681964cbbac71727dc93824660a7b57f0fcfeb79eaa856084f3c55796e`  
		Last Modified: Mon, 06 Oct 2025 21:12:02 GMT  
		Size: 292.2 KB (292182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b71ba158c27a4a233d289bf79be8c87a013b440db0421d74c9dff9585ea4d5`  
		Last Modified: Mon, 06 Oct 2025 21:06:07 GMT  
		Size: 83.1 MB (83054001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87385306f3120dbb385f788c69ed1c6525d9d09acede3a0976436ebd0a18a2c`  
		Last Modified: Mon, 06 Oct 2025 21:12:02 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:412145e19f35d2c01c0b85a65ca6697dcc02284073ef390c6ecfbd798441ac3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.4 KB (218410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:774398133c295041c166c2eb59edcbd88da616d96e2a5aaae160d897de7865c8`

```dockerfile
```

-	Layers:
	-	`sha256:68e5e406cc3bef05a63635f3ad13c9adddd955982f31468b49bdb7d4fa1265cf`  
		Last Modified: Mon, 06 Oct 2025 23:24:20 GMT  
		Size: 193.3 KB (193272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5afd3d083e225c8cb3d4405ac0d03f10e3a8bcb73d19bd98831b0733456249ba`  
		Last Modified: Mon, 06 Oct 2025 23:24:20 GMT  
		Size: 25.1 KB (25138 bytes)  
		MIME: application/vnd.in-toto+json
