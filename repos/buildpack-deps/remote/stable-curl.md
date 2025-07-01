## `buildpack-deps:stable-curl`

```console
$ docker pull buildpack-deps@sha256:0a69133564dc7004037d0545ebe5e72afee6c297d090bcd8cc9188a8cf1d3f3c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
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

### `buildpack-deps:stable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:7bf2f0e26c1abc0687aa80885244d2ee8beb3f1d7e4e529dd0de1ca8132b586d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72514976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6a75932823c7de703b2df11bfe23256fa75c001a615f191a89fa47a64098e78`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c1995213564325caf7e52ecd95fe4435c70b03eb94c674ac15706733986b86e0`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 48.5 MB (48494284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bbf972c6c2f5b7313ae3cb74e63888ab70931bcd9aefd960f9a38c540dbf2ca`  
		Last Modified: Tue, 01 Jul 2025 02:25:39 GMT  
		Size: 24.0 MB (24020692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2e1bc5782eecba09f662ef11c429519a43dc26b0b928a1cc6ea3b3e3178335a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4514386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:add32ba6d4444372f7db58f7e8a69a6db1e3a325f73d071225177ad3f87f23fe`

```dockerfile
```

-	Layers:
	-	`sha256:436cb3a9fe89cfb2e6467f882173ea4899d87bcea00ae238c6ea33a03dce0d6c`  
		Last Modified: Tue, 01 Jul 2025 04:09:18 GMT  
		Size: 4.5 MB (4507222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ca04b504391ead8c6487b71eeff6eecc5c09c6fb55ed5a8d6491144bffa3961`  
		Last Modified: Tue, 01 Jul 2025 04:09:17 GMT  
		Size: 7.2 KB (7164 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:7a3995ecb1168dd4c84e6816af68d5768fc12c04d28d20b00b9d83d4b822ef47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68723348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99e2e815e0ba8115bc440970f0fe3a973764b63e64b3ab6b92e09f97c80934ab`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:01d208698d30e75c289cb2ee99e5f2a75a42e11f8e1b4145f8fb1a881298b833`  
		Last Modified: Tue, 01 Jul 2025 01:14:18 GMT  
		Size: 46.0 MB (46026558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a3fc3e72f0d51d8e4d2ef852051b722d30ab0273006822b4317029f0c2f0082`  
		Last Modified: Tue, 01 Jul 2025 06:07:13 GMT  
		Size: 22.7 MB (22696790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c1c1f4b4e2b01fff6541074c76723c9baa93a3293fbf9be07db59be08a01b11e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4518278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d157755e1a9939f590d079e558407f52878433a59690e0bab339a2fe4390afa`

```dockerfile
```

-	Layers:
	-	`sha256:9d7c8127b536a89e3475a63da524d68390617a0b3e89c6373e53d116fe279514`  
		Last Modified: Tue, 01 Jul 2025 07:19:58 GMT  
		Size: 4.5 MB (4511046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:153396af94bc7910f7aaf6f1e0baf12fceced1a51d6bc2b906725facd31f2bfd`  
		Last Modified: Tue, 01 Jul 2025 07:19:59 GMT  
		Size: 7.2 KB (7232 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:22550593eaaab0dcbbc85bf5c2665382f0d8ad4ceb47c355090884f4fa7dbe9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.1 MB (66136515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c5190e6fb41ad39f343227d2a53b0af61e93f019981e8ad9c4bed7ec47b496f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:bc2e28ca8cdb751a10e1e014b374d783cdfa924e032e1f9eb674e7fae1220927`  
		Last Modified: Tue, 01 Jul 2025 01:14:29 GMT  
		Size: 44.2 MB (44208177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfcc606b1195a348c6a47399c1a54ab936d4477a526d62306ddce89fe76a2d22`  
		Last Modified: Tue, 01 Jul 2025 08:59:56 GMT  
		Size: 21.9 MB (21928338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9693539479c7c4147a7c63f0a5460023a3f300b680ad932db0075ff3761baf87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4516751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a37f7178ab6116a00efc43d7541b479d427439dd7276e5f32cb2eef4af871191`

```dockerfile
```

-	Layers:
	-	`sha256:01789ffa7eba26d8b58c3ffa7e0d3cfeadf0fa06a3fd8e06e68ae5e1957c4efc`  
		Last Modified: Tue, 01 Jul 2025 10:19:47 GMT  
		Size: 4.5 MB (4509519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6ad50502813a3fef25e73e211c2454de7fd93dd421b9ef2b7817fb0377f4330`  
		Last Modified: Tue, 01 Jul 2025 10:19:48 GMT  
		Size: 7.2 KB (7232 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:eaf4270d3cf8e9587f5ed7160bb85538835202dbe20dca3234b441d83567fa1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71896793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2f23d0598b4a6a8a1324f9909ef425526e48f7e9837090272aa75f576fa4cf4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1f8ab7c4e8b4178f5f2504f6c4b199268151b1fc958cd53bb861d8dbd9faa8c3`  
		Last Modified: Tue, 01 Jul 2025 01:15:08 GMT  
		Size: 48.3 MB (48338785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be9cdb9167a8712f78cfe8da9fdf771134a84b1ee0fdab42bace39b895aaa9d`  
		Last Modified: Tue, 01 Jul 2025 06:52:02 GMT  
		Size: 23.6 MB (23558008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f81ca6bd8d183f8f911773230a98ef23a2ba460b7545bba8a527ecbbec7bb6e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4514751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a4d9fc72454a97b5aba8d400e8a3d7cd8cce07ebc564c65c7f186d9057f38c6`

```dockerfile
```

-	Layers:
	-	`sha256:f6e2d39ad76c82b96c1a0020fb71637cfea86e42cd52d31658018472efff17ef`  
		Last Modified: Tue, 01 Jul 2025 07:20:07 GMT  
		Size: 4.5 MB (4507495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:032f9dc8d0fed19c2232606b7d89731b67fcd433dc81fdb124870abd7ca3a044`  
		Last Modified: Tue, 01 Jul 2025 07:20:08 GMT  
		Size: 7.3 KB (7256 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:0d5d9039e97ebfb72bc9ff59af54c2ef27e683c0b293c7b7a037d3e3b6a2a872
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74334354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3783bc1a5e4e2b535695dce3d6bb2b6bd73f2db0b2546c27c187a75aa7c46f6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:3477877077c4dd3cd4c5555fccaa126bf060154fdda28f3bd49fdf6b50940639`  
		Last Modified: Tue, 01 Jul 2025 01:14:34 GMT  
		Size: 49.5 MB (49477421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c8f46577375004356dcdcda0b1eb9cdda01e0943d00443270daca69a2ba1d0`  
		Last Modified: Tue, 01 Jul 2025 02:24:27 GMT  
		Size: 24.9 MB (24856933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e8a54ce59e0f5834e6f739421e0bc846fb58a9ee1605884c85e59a8d2424beac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4511479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a89b6c6534500a113eefc758391a8c2bde50735277efa579e4266acc8aa31f34`

```dockerfile
```

-	Layers:
	-	`sha256:ea0ba44531886cee0bc2591e756d71388e0d670cebd2bd1144505783289117c6`  
		Last Modified: Tue, 01 Jul 2025 04:19:57 GMT  
		Size: 4.5 MB (4504342 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3af7ac18d88b096ae45f9209c3c24f37be200945f0e7dea4195bcb913154657c`  
		Last Modified: Tue, 01 Jul 2025 04:19:58 GMT  
		Size: 7.1 KB (7137 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:d055d6ee47be487b7f4dc31e05ec05c20549b6a6c6e8c00454149cfab6f7011f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72374155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5131293c374f6185f23b044e10ad37ae446cf674048badb98ad8eaae64465799`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:348f1ed415b5b1e1f9982a78ffeb15637cbc5b41f93b83724c5938c2c226a58a`  
		Last Modified: Tue, 10 Jun 2025 22:47:59 GMT  
		Size: 48.8 MB (48775597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ad14aceadbd8dec6fff454480e4e098f48c504f528663aa483f102aed68047`  
		Last Modified: Wed, 11 Jun 2025 13:00:39 GMT  
		Size: 23.6 MB (23598558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e3f1d01814f8d9fd49c03a53d824d3245e364983b78d875b36ef41f5e4d30465
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 KB (7006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ce1c190af0bf09816783e843826c5ca545f432d1db34e4bd08e2dd19d8cd89f`

```dockerfile
```

-	Layers:
	-	`sha256:5742aef8fc40d6f81ed357cbf643e62f50f51f3764ece0260c92fb96345753c5`  
		Last Modified: Wed, 11 Jun 2025 13:19:56 GMT  
		Size: 7.0 KB (7006 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:102d3d5deb7d69808d5b23aefadb4a6b11f1c9f2941440bceafe32c3a72adcde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (78000910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5338bd4eb76eac2deac7c7cef947979448a440d70e6ba7bad90acbd786f04923`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2819217d87219cbf8b5ec7dfbc47c9a16195c7992a9fbe92da8723c42180b19b`  
		Last Modified: Tue, 01 Jul 2025 01:15:05 GMT  
		Size: 52.3 MB (52337243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7082fff0db11ec79e9a3c8fc9c05691e086d30ca51023010805fccbeac2b8dad`  
		Last Modified: Tue, 01 Jul 2025 05:07:55 GMT  
		Size: 25.7 MB (25663667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:367632ed672039086bbc362c5e28aa9cddf26fb0b89adab0d71546bf4a5e2263
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4519044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a4866ec9466342d4d2a01f49be4faa97fe418aa6e21567fb33555c0be167f20`

```dockerfile
```

-	Layers:
	-	`sha256:2bd51c8fdcb87423032884dbce5b78041501c543f9ec83d3536817fc584a17dd`  
		Last Modified: Tue, 01 Jul 2025 07:20:17 GMT  
		Size: 4.5 MB (4511842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a67cc44828a065b5b2edd928c989049dab8b5a0a70ca9556f6777ede775c1830`  
		Last Modified: Tue, 01 Jul 2025 07:20:18 GMT  
		Size: 7.2 KB (7202 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:e9ad8386be14c0712564024310a17a68bf9ed9ae456288746df82f9c79f67ddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71169828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7520a2d9f1d60865682a5b5a43cf5d6056c05f84c678a59c2ed7a11ae8ecd087`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f5e945529523ccd9610b7c0253cda59a29c297f0a697f3c402695e1c6ecf5e6c`  
		Last Modified: Tue, 01 Jul 2025 01:15:47 GMT  
		Size: 47.1 MB (47149287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72dca9cef3741351ad228dc4986e66f3e324bfb88d5cc9e2b190dd3a3abf7dcf`  
		Last Modified: Tue, 01 Jul 2025 05:30:26 GMT  
		Size: 24.0 MB (24020541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:011d566e7cafd246c1da5706a679ca026aaf9286a7a2daedbc284f87a6eae57e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4511190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:185d41e4debedd62c38eadff96a9d4690cabb1339b2db6261b1f6ecc701b7607`

```dockerfile
```

-	Layers:
	-	`sha256:5be8637bf114e268e8e602eb2afdc2854b20f0ca0cd48ef57415147a68e123e1`  
		Last Modified: Tue, 01 Jul 2025 07:20:23 GMT  
		Size: 4.5 MB (4504026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f27efc9eeba91b82787f0b0c4ee11b06e85253ea135c0a9c816880da0a531aa`  
		Last Modified: Tue, 01 Jul 2025 07:20:24 GMT  
		Size: 7.2 KB (7164 bytes)  
		MIME: application/vnd.in-toto+json
