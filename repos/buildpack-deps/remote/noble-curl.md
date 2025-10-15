## `buildpack-deps:noble-curl`

```console
$ docker pull buildpack-deps@sha256:3ceda7e3ff558d911572c36a98e511e50408541eca53b6a35b7c8f605ca609bc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:noble-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:65283ed5739471e7838089cd9a4594cec30204fbf1dfde35c144ed2253046360
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.3 MB (43348228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1b0597dfb91e5d4154c3ea5945826b2f6a5b9ceb5919e54e59d55a6812192f7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d4da1c38cd39a1dd115e9a6c26965a439c65b03d482b5fa7a24467582eadd75`  
		Last Modified: Thu, 09 Oct 2025 21:31:21 GMT  
		Size: 13.6 MB (13625081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:747061f698b15380189b9e1a410415eb2253eb97ca74ec350aded83fb2078c0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2614771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d262ca6d994ba9411efe9fbfd326115d3e649474bc500ad789ff2bfb9b056ea1`

```dockerfile
```

-	Layers:
	-	`sha256:722eb203e41b1cd180570fa0c680c85ef88b8bd8737adc3570c525d524368e1e`  
		Last Modified: Thu, 09 Oct 2025 22:19:31 GMT  
		Size: 2.6 MB (2607813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3a43c431dc49cd6c4d8f27f59a4781dc74b5bf6a566dc906d11780c17767602`  
		Last Modified: Thu, 09 Oct 2025 22:19:33 GMT  
		Size: 7.0 KB (6958 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:4a451b53d6dc0f21edfebdf39bba5fa0aab36f363f4cccb1a2befb8bd1686ddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39636138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a2846f3793fff4d6cc4ea40410a3232af0998ef0b3f3e12ba5a6a240d71fd99`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:1ccdd7fca45ec88ba0ddda07e5e5acb6b40ddcb3023e0cbc04ffffdf4e30fb0a in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4afa85c5883c0db62b02025c149edaaa237af5ba25ea48039e875a802d465ac7`  
		Last Modified: Wed, 01 Oct 2025 18:03:16 GMT  
		Size: 26.9 MB (26851732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:022ffe8d142b8dd5e375cb3bbf3b7f0d742fcf24654020fe40ada08aa8d2bfe4`  
		Last Modified: Thu, 09 Oct 2025 21:08:02 GMT  
		Size: 12.8 MB (12784406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ee2a988ffca1bfd6fbd1f41b860b66b73eafc9204f1463b963951e777c7d6f62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2617140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b22140d671da4a9b6ede4762d3f79fab569b484d13dcdb63ce16e51587976d7`

```dockerfile
```

-	Layers:
	-	`sha256:b866b3389d6c15a875cb7b04eb09daa187f5680e8aec33176ab68c5d4debecc6`  
		Last Modified: Thu, 09 Oct 2025 22:19:42 GMT  
		Size: 2.6 MB (2610117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24564c3da16820d0a1d7f95665d46ff00d90d028a08117f3419aec7992448abe`  
		Last Modified: Thu, 09 Oct 2025 22:19:45 GMT  
		Size: 7.0 KB (7023 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f8cafaf22330127a2c256b7b73b66321033a6a79eb871c086c1304e8f16bbeda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42322409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1391c41e25e42b9865122e5cb7f959f7014738b9e0ab782bf875191265ef23ec`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76cd70ea204ed4db7ba47a601ca9a11c75a0084d32a61213dd88df48189d57b7`  
		Last Modified: Thu, 09 Oct 2025 21:09:03 GMT  
		Size: 13.5 MB (13460697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:362d967dbab17ad33e0de7101862f340761b826906f60b65a9054d1c327956dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2615910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d7f2ec01fa98c8da2727fc0cc05db8d818bcdef29bbc3982a66db2a0e158f23`

```dockerfile
```

-	Layers:
	-	`sha256:ed6506976060ebd23eab5bfe76e62074aa1eac0cd34b16613507bdd26e2d5672`  
		Last Modified: Thu, 09 Oct 2025 22:19:50 GMT  
		Size: 2.6 MB (2608871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fac7d686ee48e28a56bf10f28f6a9136500876088a71dd52ebdde581ce1674f9`  
		Last Modified: Thu, 09 Oct 2025 22:19:51 GMT  
		Size: 7.0 KB (7039 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:71e6afaa6b8dd301a2daa7bcf03dfa2ce0ca85fb0afb4ef488f531cb38b7e163
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50256718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:835969ca596f33ef288a48d237a9c0447162fefebd6db8454ee75bb1497657ab`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:e06669c9bfb72bbbaf1c25efab4729831236db24361c42e37dbbc7b4eff7a82a in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:199e3830c89a37cc6980743d7c9e0e355251d050c55eb838183c9cf64fac375b`  
		Last Modified: Wed, 01 Oct 2025 17:22:52 GMT  
		Size: 34.3 MB (34303525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff2c43d036e8b55e943cd93e0bc732e1fdb6b9a5f8fec89a5e868148e6bf1fb`  
		Last Modified: Thu, 09 Oct 2025 21:09:03 GMT  
		Size: 16.0 MB (15953193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e5b4eefdf8d32ecbd612d77568509cd72c8b4f09395449ce07e1eab198c5873f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2619423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2db05ae2db64140ce6cf4c65878b94bd4a8a4c94b9cca901bceb06300e562a1`

```dockerfile
```

-	Layers:
	-	`sha256:102d10ad6c95d067f10668ce9658bbca476c1c4ffdd2055aaa9c0c7a9d0881d2`  
		Last Modified: Thu, 09 Oct 2025 22:20:16 GMT  
		Size: 2.6 MB (2612432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2081070866018ad3d6b35e64ab6a418ef9095b07998324d4a51dbe92f239cff`  
		Last Modified: Thu, 09 Oct 2025 22:20:30 GMT  
		Size: 7.0 KB (6991 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:70e9f075da189e496ac5f3806eba711a0e6f0d2547ecce749333dc4a3447f84d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45282436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeef43eea8956aa70e171334daf80cb61df9aee317f74291597a9fe362e718d9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:857dc87fbafae31881cff8c69aed267a033f5df226dd351ee89de918ad5678ce in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ff47a256ba51b80e9880bc96be4ac2f094c47e0fcd7eec71bab85787cfa54b8b`  
		Last Modified: Mon, 13 Oct 2025 04:10:18 GMT  
		Size: 31.0 MB (30951381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cfbce957852ea37a1a2c784ab77650af27478b8247917467797949fa28f5220`  
		Last Modified: Wed, 15 Oct 2025 03:32:31 GMT  
		Size: 14.3 MB (14331055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:86978cd598d563fc6ad811b982c465feddb4adeb9be53f08bc6e9528d95aa275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2608702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62b2acbc02b83abc38b99116c051d43e9625e0b6967fb0540b3983449dda613c`

```dockerfile
```

-	Layers:
	-	`sha256:a90215290c3b9df8bb4c18c349529d7e81d8c37c8ae6cdcdbd79840f7cbb34f7`  
		Last Modified: Wed, 15 Oct 2025 04:19:35 GMT  
		Size: 2.6 MB (2601712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34e5faf8ae08ff2aadd3c5b2142e0bd9cdb439ae9f6390b97b089fe6b558a717`  
		Last Modified: Wed, 15 Oct 2025 04:19:36 GMT  
		Size: 7.0 KB (6990 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:17e32572328f32b2ab3175ee19a0a6034742c30a8a5a15342d62028e38c22860
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44844222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db3c697940f1867d867e3afcf1a2ef3548f0598ea1422f617ef3bb9724cba4ac`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:1c921a1d937949898d3d4ba499ce8d41425fe6dd2c8fdbcddd0070f2699f05b2 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:67735b72a65d308a2c2c9505d0d6e8419b7f2654a16cbd56963d88e01202d507`  
		Last Modified: Wed, 01 Oct 2025 15:43:10 GMT  
		Size: 29.9 MB (29906151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fcae3965c70c7cb3a760d4160161a0695e258329f001c8a190e4c43e7741035`  
		Last Modified: Thu, 09 Oct 2025 21:09:01 GMT  
		Size: 14.9 MB (14938071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7d049bd281a67cda4c08d4341e53f82a4eea75e437d4beb422447e3cfb58d42e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2617597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d03f50bfd10b52dec1ff22b8c1cc5ae84e9a609558257ee021ed8f40fd7a226d`

```dockerfile
```

-	Layers:
	-	`sha256:6b810ae70c438ead71fbd80a3c2da046e2c13f645dc968cae5ac62f4de37fda0`  
		Last Modified: Thu, 09 Oct 2025 22:20:46 GMT  
		Size: 2.6 MB (2610638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edb5b4969c27b6c7cf31a44f011697a6ce02b9268c97b62d5ff170aa191dcd62`  
		Last Modified: Thu, 09 Oct 2025 22:20:48 GMT  
		Size: 7.0 KB (6959 bytes)  
		MIME: application/vnd.in-toto+json
