## `buildpack-deps:trixie-curl`

```console
$ docker pull buildpack-deps@sha256:affa20a37e9753583bb0a66db828ca9da62d67e53fadcba2f9c96a95603148d1
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

### `buildpack-deps:trixie-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:02e88f09cab49f1e5efa8c0002169b6ed35ae5eaf972fc54e96f0225ec9b90dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (74992725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:150ffa7444c79da890d684c7938d703ce1dabe28c76fb856ca7cb6e4d941147c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1745798400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f8c8542523ef5c08ca9bd5ab7d7265d12930a45ccc7c8364e909fde03c894479`  
		Last Modified: Mon, 28 Apr 2025 21:08:35 GMT  
		Size: 49.2 MB (49248239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8723664ae2848fca92e9c796c763cdd28a6906becf75b0bfcfbb3c85be887d97`  
		Last Modified: Mon, 28 Apr 2025 21:56:17 GMT  
		Size: 25.7 MB (25744486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:febd9f2fac2bf0af4cdc9e95f57281741e0c53a64cbe71f0c4f8164cc38295d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3990569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61d805fe30942b76c3241ece9afcb6c299eb34dfb3bb5781230e9f04a579d808`

```dockerfile
```

-	Layers:
	-	`sha256:aadc341352e3b68a2c270792f08b8ddf0e5997e2fef3fd133f80f16208d09ab0`  
		Last Modified: Mon, 28 Apr 2025 21:56:16 GMT  
		Size: 4.0 MB (3983748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc79bc2034dc7d759fa47e9d01b6d996b5fdbefd1e98dcda812f406e5ea3f3a4`  
		Last Modified: Mon, 28 Apr 2025 21:56:16 GMT  
		Size: 6.8 KB (6821 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:8960c0f06be814ca30bf209481d443b22a3cdf78dfe0ed92f4a75faec94d7193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71903058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55cd09141dbce9640390f777b90f7604b24d90c47e6945081ee2ca3ece0b59d5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1745798400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:15a0811b2608aa97b4e0811060ffea557de20e605122f0c38825f47469947704`  
		Last Modified: Mon, 28 Apr 2025 21:10:19 GMT  
		Size: 47.4 MB (47428611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b453de73db44edcda29182f13881db794c74b0f335096c735f5f88ffb61b994b`  
		Last Modified: Tue, 29 Apr 2025 06:01:51 GMT  
		Size: 24.5 MB (24474447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d92826e7ca33d9783680b60f07cd8a3d048e3c5d49d3b08b4fb2c8d8f98a675c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3999534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad4354b6fe53b29d5f1ed02bc6d1ffdc3d9437842a9decdd0d41dd263a76c0c`

```dockerfile
```

-	Layers:
	-	`sha256:d7f3a7f9244ef309ac89251fdeaaf694e68f2fa0597bf5ebd0c7ee76ebce05ae`  
		Last Modified: Tue, 29 Apr 2025 06:01:51 GMT  
		Size: 4.0 MB (3992655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:443dbd55c7b01b5a59785c65a175ffeac150c102421426802730040e70380fb8`  
		Last Modified: Tue, 29 Apr 2025 06:01:50 GMT  
		Size: 6.9 KB (6879 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:1a5ffa9b745ddb1d6bcd09c6ae59256668d44a08b2e7a7820979c9157d6c1fc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69422195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:471eae3a39a8277efa0354b33ff1f02a006719efe607952a3306797b1a7efd10`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1745798400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d877c043ab6ec52d6d4eaeab7dea355ef83893e584af00854b55ca611a3bcd99`  
		Last Modified: Mon, 28 Apr 2025 21:19:08 GMT  
		Size: 45.7 MB (45683821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785865296d03ccb31a01d56e5adab53e0c986bcfdc0c9920d48d9b1d2d93eda8`  
		Last Modified: Tue, 29 Apr 2025 03:39:17 GMT  
		Size: 23.7 MB (23738374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e32f482c1e7ddda785eb21e00672991a91f24fa6b40840f6a5d0a5fecec7c602
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3992127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c88f6d685463df5d4702ed0131cb5e440a8a1ca41ea2979bdd646a7b485af7d`

```dockerfile
```

-	Layers:
	-	`sha256:580b68f14d149fb86296e5923407fe32efa5ed0349d6bbdcc273a0741f769a99`  
		Last Modified: Tue, 29 Apr 2025 03:39:16 GMT  
		Size: 4.0 MB (3985247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b9b708cfc28c5ed42f414d8d9d6e4dc15f3af639bba424d5ccb02bc32ed42e9`  
		Last Modified: Tue, 29 Apr 2025 03:39:16 GMT  
		Size: 6.9 KB (6880 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:3f2fe02448f330b74da14b4c094bfc7e92e087bdc753fbe07d1e41b689307aad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74741086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a059c5a9f9b224518e93cffe75d6d5e9592876e9fd09319ed2c54177d3eb0e05`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1745798400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:288a1cecb0ea762427d39b072c1ca965d193e927e04da652f7b21eb12e9b2acd`  
		Last Modified: Mon, 28 Apr 2025 21:23:23 GMT  
		Size: 49.6 MB (49624118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6faa4d9377738e3cc52e5d3cadb55bd77d367fb6439d9d14741079130dc9e4e`  
		Last Modified: Tue, 29 Apr 2025 01:48:13 GMT  
		Size: 25.1 MB (25116968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5452c96a4e99b734ebb51a784d38378a97839d67e8390f0ef4ff4a82682b0102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3992181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6506ac17edf4d0d4371021db856acbff14b4f54fe6c07d92cd543d5050ebc5c3`

```dockerfile
```

-	Layers:
	-	`sha256:b22328473e8a24afb96ea50af42494dbb5f4c96c3297da3b6c6ccbdfec89f7fd`  
		Last Modified: Tue, 29 Apr 2025 01:48:13 GMT  
		Size: 4.0 MB (3985280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8ad75105e0a5aedec033bc639fef39a7f18c7890a2b757153623f80874d1f55`  
		Last Modified: Tue, 29 Apr 2025 01:48:12 GMT  
		Size: 6.9 KB (6901 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:53886413f6e20e3d644423aa61bd2d3eb19618f534fa2d30782a22c2826c12ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.5 MB (77518197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd5bf565c3956692540431e6eb759808aa9976274d2b0d1f0c6bb9924dd0c53c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1745798400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ed5e8397bb7752a7889fc6f59947b41ffcc3d3218435299a473ce5a254d892f0`  
		Last Modified: Mon, 28 Apr 2025 21:08:18 GMT  
		Size: 50.7 MB (50743157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec898d3c3ebd3311a66f69a4e126ef0cd8c4ca8f645a36cd5ded8a3f3b5c9e6e`  
		Last Modified: Mon, 28 Apr 2025 21:54:00 GMT  
		Size: 26.8 MB (26775040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:749776567a5f05e29d2132db6b411e7e49b2dd2e2217d71c66e1ad230714dff4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3987601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3884a2eb55f51f495863c7c680ddccc110ad889397764c42a22c0b09a0979baa`

```dockerfile
```

-	Layers:
	-	`sha256:486bed4a7403cc8ec6f8ffa2a97ee92c60a2f410842debd7ad1a00d3b1fda099`  
		Last Modified: Mon, 28 Apr 2025 21:53:59 GMT  
		Size: 4.0 MB (3980802 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13d65214d145fee33ab70a527152c87e5ff8ebf5f379eee238fc93723e9a1614`  
		Last Modified: Mon, 28 Apr 2025 21:53:59 GMT  
		Size: 6.8 KB (6799 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:ac9346d3d9404f556e027e80844f2a990def7eb7c0706830aedfd00dba114fab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.1 MB (74141628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d27d4c6cf99f147c8be3a1375bf89ab01e519bc2f369ab680b72fce7bcbb6fb7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'mips64el' out/ 'trixie' '@1743984000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:574fdf9455a60a8eef233edb482713c5b89d1180e8a134426313714c5369a364`  
		Last Modified: Tue, 08 Apr 2025 00:25:55 GMT  
		Size: 47.8 MB (47767083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6009983b77d9776ab3b7d6cb770b45be9311a22590aa9a6de0b4730c3af4ac0e`  
		Last Modified: Tue, 08 Apr 2025 16:35:37 GMT  
		Size: 26.4 MB (26374545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:239f1c745504b3508573705801f2ab2b5cb671f572e58d3ea15976eb7230b82f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 KB (6652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7ac0cebc8481d42a9afcb2e442188ed0b411abf604760f3ae9eb24ed377d50e`

```dockerfile
```

-	Layers:
	-	`sha256:734bd752033fe327a3bc3369191c4de482a9072c79747129de3779429201a33b`  
		Last Modified: Tue, 08 Apr 2025 16:35:34 GMT  
		Size: 6.7 KB (6652 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:99c920ed3667ad19ce9dc6ac05ada03cf590245fe6904488767732f2fe270ddb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.2 MB (80216129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c643720b45d30c7f78fe7a4ff36e10416b3c9451543049529d38b664272a172`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1745798400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:03ebb30bb37cd398ea8ab1a268c301664089cf5a54d23466e4338782afb5f9cf`  
		Last Modified: Mon, 28 Apr 2025 21:25:28 GMT  
		Size: 53.1 MB (53072552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed88abda34c2c7766794d61fd8b43cac1ab4eeadc9f85398417820583a09e36d`  
		Last Modified: Tue, 29 Apr 2025 07:48:18 GMT  
		Size: 27.1 MB (27143577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:85932e4f10825d37ae274cfad3afceca00b017aca41b71275643c5d8109dcbbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4000512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:314a19d49ef6458643de65026856a1737810f9fe505d64791db36f84db0d6856`

```dockerfile
```

-	Layers:
	-	`sha256:dff5d12bcbabbaa3dc2e00e2b759be583d6703021b58fd1a6cd7d3d6a1f3f93a`  
		Last Modified: Tue, 29 Apr 2025 07:48:17 GMT  
		Size: 4.0 MB (3993659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:464151fc98e170a8303bb29d01aa714ae6a4895f6f15002e30d4fc88bae7724c`  
		Last Modified: Tue, 29 Apr 2025 07:48:16 GMT  
		Size: 6.9 KB (6853 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:6a909fd7894a12b32cad28eb84199cd62ac4afca0e72cc488153ca30d7e39982
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.8 MB (72803070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d8571512feff2df2cbcc72d36dce7bdb6d5a638adb221c0028c9290b26f9ec4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1745798400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3e87a3ef7201dacec1e06fe511cdfaa924c5bf89f4f022c082b59ff14eb11b6f`  
		Last Modified: Mon, 28 Apr 2025 21:16:24 GMT  
		Size: 47.7 MB (47740349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b410971d43e4d351db365aaa47795c79f72faf119ac6c217623f17c39d9714c9`  
		Last Modified: Mon, 28 Apr 2025 21:56:29 GMT  
		Size: 25.1 MB (25062721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0b944dfe8475e5406d8c1882a6077bb231958a578e00cf415d65b23766d0befb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3983241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e1a32970ffd979924bb50fd0491b4b100c09827a01d03f84a460fc08bc40d8a`

```dockerfile
```

-	Layers:
	-	`sha256:0c8672ca3286aad2154217cd514fd981a8b37aed68a655ba77a291bd99ad442c`  
		Last Modified: Mon, 28 Apr 2025 21:56:26 GMT  
		Size: 4.0 MB (3976388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86fe80e164064ab918d1811dd576b3654c740e170cab90c30c85f6d6cb38a574`  
		Last Modified: Mon, 28 Apr 2025 21:56:25 GMT  
		Size: 6.9 KB (6853 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:5820a67474d034358b6caf0386bd23e2bcab7da5278632f22954fb9b1cbea3f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76249228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e6d6f639e10969e64e384ecea52e7653c37967d93a8fcd463ea414ea2224476`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1745798400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e1ec3b1570f7d822c5a6aa013529484429ad99bde8495d827b56c3603992fd3c`  
		Last Modified: Mon, 28 Apr 2025 21:11:06 GMT  
		Size: 49.3 MB (49316646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc2dfe09dce90ef60478379ac93bf4db4640c14411109c4ddd5060ffa49cdfa1`  
		Last Modified: Tue, 29 Apr 2025 00:02:32 GMT  
		Size: 26.9 MB (26932582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:23173a8276c63798a63a116632b62645d8a60a9fe4173f3eb4d610387208bc0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3998184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdd182ab547d39fa0df3e8d6dc3f422aa5bb4dae5c3811420aa98c1a22c01a9a`

```dockerfile
```

-	Layers:
	-	`sha256:82fde6137e5db77528718b4718bb55c20b3fe7da9d1499edb35fd23363500336`  
		Last Modified: Tue, 29 Apr 2025 00:02:31 GMT  
		Size: 4.0 MB (3991363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36b3ce78a8c29c921369cfc4d406e12627370d91de940f16e73274ca9f37d7e1`  
		Last Modified: Tue, 29 Apr 2025 00:02:31 GMT  
		Size: 6.8 KB (6821 bytes)  
		MIME: application/vnd.in-toto+json
