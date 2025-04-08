## `buildpack-deps:testing-curl`

```console
$ docker pull buildpack-deps@sha256:4e7ec7407765c0987f6a8044033a31c511e77101ed3fa4ede23c4016130b69f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 18
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
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:testing-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:f7b7027dc93a0d1c150cc99f76e40d4db980dd506bf736b092ac4393f891a70f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.9 MB (73887269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06211409eb33ac4947448465c64d937b978d504acbc4b15b49a449dbb502b2a6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1743984000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b43386f4a8eea1a35e7c4f34a0bb12426fd9b88216af22d7c3ee489419eb1bab`  
		Last Modified: Tue, 08 Apr 2025 00:23:13 GMT  
		Size: 47.5 MB (47545414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf061a9daba97c5d47244462ed42ef128857bde7ddf55699ef7e9fdc7b5705bb`  
		Last Modified: Tue, 08 Apr 2025 01:24:30 GMT  
		Size: 26.3 MB (26341855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d7cf43149634da56eea757638b0a4e55b99459bd5b8e2d730f8f3537a2c046e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3975415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc4ce4696b0e10d64fdcb47444656d9f04a15ba245f68a001d75c84ecb7bf46a`

```dockerfile
```

-	Layers:
	-	`sha256:e6dc07fe0fe1cd9a60cd6c44d68af06cec8bd70d4e9e29a4295972be71500f38`  
		Last Modified: Tue, 08 Apr 2025 01:24:30 GMT  
		Size: 4.0 MB (3968594 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0a15f9e2605a18b294f3c0cdad7bd6db319c95eccfb93c56024ba91b3902658`  
		Last Modified: Tue, 08 Apr 2025 01:24:29 GMT  
		Size: 6.8 KB (6821 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:126d37d6d10df132c25fe63e95ee99da19eead5c9f8e60571ecab888046af410
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70694640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7f225f120d8d054c68191211ad5d8910d443cd673e300cdfa082812caad1286`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1742169600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:43d6e898d3a5beca16572b1a502b9433116891c583ecdbd0b66dccfd8af9e4fe`  
		Last Modified: Mon, 17 Mar 2025 22:21:05 GMT  
		Size: 45.7 MB (45737144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:023a0e893b154d7d5e322d742da1db8537753d0cf777b8cb73ca869670a0c807`  
		Last Modified: Tue, 18 Mar 2025 03:08:29 GMT  
		Size: 25.0 MB (24957496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9d2aadf98769a4638a508440ae1ed8bfafa9bc7982416a6625884a934008e580
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3978762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73cdcf63b59ba1111705deff96d8bca68f00ffa910850e3a25d9cdbcf33ff283`

```dockerfile
```

-	Layers:
	-	`sha256:fcf6338a901175da227c1434a264821307dcc13623527d8ee5782c33e7892247`  
		Last Modified: Tue, 18 Mar 2025 03:08:28 GMT  
		Size: 4.0 MB (3971881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:183efb90a67a241d4c6a8a74a6a8dab0ea5b9784d3c58f308eae10af99079f56`  
		Last Modified: Tue, 18 Mar 2025 03:08:27 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:523b60e4300b2d1124101c19fb89251077205a49544eee56448e40432b8efd50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (68046514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c51b1926ff3ab7a990ca3a87cdee226dd834141af04ebe0280d134731627317`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1742169600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:344116a397737c11dc2811d8baccf64c6e4150467542a11a0c5572ed1b6038c9`  
		Last Modified: Mon, 17 Mar 2025 22:21:24 GMT  
		Size: 43.9 MB (43934171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d1689e965c6a71d99b5f45c9a0e5483f83d9ca9f7db740f0b984c85e463e9c`  
		Last Modified: Tue, 18 Mar 2025 07:20:09 GMT  
		Size: 24.1 MB (24112343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4552ad81f4db9c336ce36594286f666c239f4f9f1dd63030234ea6a9cbc0e416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3971352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:661c251d69def949a056f788ea3241229a58f1a245e2398c0c28908eb6eeeada`

```dockerfile
```

-	Layers:
	-	`sha256:95ae7c31ff76b5f60e15b92026505310073582a37d3cd3b80dcbc4fa4cc22058`  
		Last Modified: Tue, 18 Mar 2025 07:20:09 GMT  
		Size: 4.0 MB (3964471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34b3b0c07c992a913071c58ed1e531d87a8320e3e2d1a9c4bc35d5ed37bdd522`  
		Last Modified: Tue, 18 Mar 2025 07:20:08 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:84e50d66222d9b955d83f15462da3b6ab6de173f76561b909626dbc094673c12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73576789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5289af8d57fbb872b6d49da3987f2381809e166cc5ce455cedf8d6891a7616b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1742169600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f094fa2db11dac08419411aeaf2d9c561365872610ec591de05f23f2fadff3bd`  
		Last Modified: Mon, 17 Mar 2025 22:19:09 GMT  
		Size: 47.9 MB (47886359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a84822f7d47020ba3b073f3f8ebb18e27a90b8e25a519c2b492131234a060ca6`  
		Last Modified: Tue, 18 Mar 2025 04:59:07 GMT  
		Size: 25.7 MB (25690430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:10b16fdc84be9fadf4a455271418590007071ce8f98f0ce25ec584f6ad6511ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3972050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5f8763a0bc1af60ad3c9cc4b59006c9b90fab143124ce253611d5025e8d0ae1`

```dockerfile
```

-	Layers:
	-	`sha256:cc204fc8e5498a1af3b86bf0d74685fa9dbe7177e60caa0ea5f51751134fc6b4`  
		Last Modified: Tue, 18 Mar 2025 04:59:06 GMT  
		Size: 4.0 MB (3965149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b51c61e8ff3fb4057c754e494aa3c651b0f16fb1bf8ad14cc1286b385cf7bf66`  
		Last Modified: Tue, 18 Mar 2025 04:59:06 GMT  
		Size: 6.9 KB (6901 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:2ce9bb25f72d1db13f990ec9579b96039f0bcfe873b48f1254b8086b3f26556c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76319764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f69e3140767fcd1fb197300f9f49b523c8669b3618f3c9a65d2f0dcacdb5b74`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1743984000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:091329a1d6a6197a5d3e206472c088a0858ef7008c0ef0caa690ee6550acc80d`  
		Last Modified: Tue, 08 Apr 2025 00:23:22 GMT  
		Size: 48.9 MB (48867484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52fe46607c901c693e43f5e041d9582f12c310a5a19737459269da4c901faa70`  
		Last Modified: Tue, 08 Apr 2025 01:24:20 GMT  
		Size: 27.5 MB (27452280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e570ce3dbf1211d779e4cb42bfeb8d4cdf319d573bd81e4082c5e5f9900f06a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3971805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00b865202124d3a19aa3528540a5af74ff3f96ea88dc1802e29f916c31dda167`

```dockerfile
```

-	Layers:
	-	`sha256:2fbca0ff51f1d167e8e2c185870f43f76c846ddf4b2965ef9cfe91877fad1ad6`  
		Last Modified: Tue, 08 Apr 2025 01:24:19 GMT  
		Size: 4.0 MB (3965006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95df3d53b0112639245b468204f5d141859461261aec104904502e308b09db8d`  
		Last Modified: Tue, 08 Apr 2025 01:24:18 GMT  
		Size: 6.8 KB (6799 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:e67fde04bd3178a9887bdb8f3963628390dc388ff7ac17136a91d66ac88a0d4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (74005715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37b0f3b3f8271c3b6026b8da272f22b9688abdeae7c82b686250739db7a0649f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'mips64el' out/ 'trixie' '@1742169600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:46069a6fb0408c39827d84c4f957cdacbea0859425bc5cee1431cc570428f262`  
		Last Modified: Mon, 17 Mar 2025 22:19:48 GMT  
		Size: 47.7 MB (47726922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8024e8bce62fef1bb0a0244ed9a2bd73704dfdd7237b2039638682f562d4721e`  
		Last Modified: Tue, 18 Mar 2025 16:27:50 GMT  
		Size: 26.3 MB (26278793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:49c579f657beb3d6224f9e56656d2053ecdc7b62c77d5782cadc1ffe0673c983
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 KB (6653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:629566828865043b2acd1b8e5eb35c74118e39d6a0a6d8f8cda93ea446b2ce32`

```dockerfile
```

-	Layers:
	-	`sha256:d426e778648ee276cf0e377a3582173a73b86c0c4e55b0f2123a496418229eae`  
		Last Modified: Tue, 18 Mar 2025 16:27:47 GMT  
		Size: 6.7 KB (6653 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:b0804de94fd9bfc72d0af7b8efe7c7d7d245b97db6a389cca08f8001d369526d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.9 MB (78936095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e422c99cebdde0114fc3829984961cdad1f01b3d74a69bcf54909a01456e2b9a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1742169600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:895a5f19953067f7b5f8d8697fd370f37def792e6b968ea95a15dd11594bc1a6`  
		Last Modified: Mon, 17 Mar 2025 22:20:07 GMT  
		Size: 51.2 MB (51162729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aeaa0f265ddf4206f6d845d5494e3733ac72919e3d0329859f2ce1f44f19c11`  
		Last Modified: Mon, 17 Mar 2025 23:57:42 GMT  
		Size: 27.8 MB (27773366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e9ab5fe6e5b89b6db3ba486a8945d4ee1cff6a0c7bac392163eb6106901f6bbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3979751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04ace8fb0f20bf2bd27b658f7d79d48743823c3bd791894100ec997e93cc0dd4`

```dockerfile
```

-	Layers:
	-	`sha256:62e996d1150fcbef2aabc02e6df37c3d34d05ddf22eb450b8960fe8fbdad988b`  
		Last Modified: Mon, 17 Mar 2025 23:57:41 GMT  
		Size: 4.0 MB (3972899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6606af07ca7d99fdfd2d6fa3fa19c9a29d9a24563631a43fdb01a5c16fddd514`  
		Last Modified: Mon, 17 Mar 2025 23:57:40 GMT  
		Size: 6.9 KB (6852 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:85c2362950bfb2b6928a2341b3662d7ae95bdfe895f29fd5199dc0c4c54d4d13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71708104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6530ece883f52875c0a60311359a0bff116da3c786858d6da325e563ec2167e2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1743984000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6d049c0e21a4ad6e8db102828b8d03bcd0730a934f6305fa31bc0a4e2bc6af6d`  
		Last Modified: Tue, 08 Apr 2025 00:31:42 GMT  
		Size: 46.1 MB (46072980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9e23969c469610d4b7fd0c3d4fcdc71ebcf20493b72a3bb5e5f56295ca06c9`  
		Last Modified: Tue, 08 Apr 2025 01:25:33 GMT  
		Size: 25.6 MB (25635124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b51d5335324b30b83f11521113871dcb1650eeefa45e30dc4d3dc0a48156f5e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3967445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8990559324b6b35ccab57ada481b07ed116dc769cef274d5e60e989a046e9377`

```dockerfile
```

-	Layers:
	-	`sha256:f180b5dc93dc401cffce2f471bd7a3b315df859d743799d6effebf80d473f226`  
		Last Modified: Tue, 08 Apr 2025 01:25:30 GMT  
		Size: 4.0 MB (3960592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b60b945f4ed0404baa7dee4c5bdb123ff5a9376900b1c7709cbb927856113cef`  
		Last Modified: Tue, 08 Apr 2025 01:25:29 GMT  
		Size: 6.9 KB (6853 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:573ef29bccb79eaec4928df6314513445a44dbde01dbbe0a17a42a4adc71597e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75147204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce0f1da3bb4fe21aadc809b1f2da9c7b9f1c3ab6314e087fd3ae3b4fb0b3cdeb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1743984000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:19a5a2e5eb505d0c1814e6d65469ecbbf0abf7cbe214ddd85cb24c5fb088dc02`  
		Last Modified: Tue, 08 Apr 2025 00:27:13 GMT  
		Size: 47.6 MB (47577872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09a838b52d3c41c71c15b487ddc0ce4cada3e3fb6a44e40511f7176fd1633521`  
		Last Modified: Tue, 08 Apr 2025 03:45:39 GMT  
		Size: 27.6 MB (27569332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b4179cddd7310cccec4a3ebf9e792a2627069b5d88c64720840b5db961ebc5ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3982388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7c4fc928bba41ad00f0f0685300b5866fe8a3d2802cf273c8239331f5cc77b9`

```dockerfile
```

-	Layers:
	-	`sha256:98447d6a93689f01d31f72f8883c9ed7b8bb8eea46e4e025fe62081e94b0d540`  
		Last Modified: Tue, 08 Apr 2025 03:45:38 GMT  
		Size: 4.0 MB (3975567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afdeea108200648db8b0c67dd296c4512e3cdcb5901119e200ab1f3eaf9d25f6`  
		Last Modified: Tue, 08 Apr 2025 03:45:38 GMT  
		Size: 6.8 KB (6821 bytes)  
		MIME: application/vnd.in-toto+json
