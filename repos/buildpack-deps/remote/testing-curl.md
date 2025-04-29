## `buildpack-deps:testing-curl`

```console
$ docker pull buildpack-deps@sha256:0ab251cc7961d5874a61d63f6e1181f6d46124a54b96838b34991cd88d901f56
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

### `buildpack-deps:testing-curl` - unknown; unknown

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

### `buildpack-deps:testing-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:eba6adb31ab27c134cd3e27f6ea88cafd91fe39b8c9034438f7964a69614ee5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70800629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4923d53830587a77d539d025441178acac3af9e334c14b8af071e0e26bc675d2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1743984000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ec645b8b1764e458ae4d21700842e441d914fd80d6e0135fa393952e129298fd`  
		Last Modified: Tue, 08 Apr 2025 00:25:30 GMT  
		Size: 45.8 MB (45786687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd9068871a08a0535e32e79d1a45670b225b99f46bbc4e55433b3bc2d040fea9`  
		Last Modified: Tue, 08 Apr 2025 05:13:28 GMT  
		Size: 25.0 MB (25013942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:75641b758be26a086004e6464cb02aea26e9544f375942bf5e927adcbdb9fc0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3983737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0068093c6dc2be1c9ff8ad01e0964a5456f44bd558f9fbfae6b6c91b25ae74a9`

```dockerfile
```

-	Layers:
	-	`sha256:22aca250853d806519dc4970bc167babf6b63511d21b0363e4ba94e54df0d970`  
		Last Modified: Tue, 08 Apr 2025 05:13:26 GMT  
		Size: 4.0 MB (3976857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4127ebf8c8540e1ae5df709841a5524d5a73a2ea7dcc756999b375959e89eb8`  
		Last Modified: Tue, 08 Apr 2025 05:13:25 GMT  
		Size: 6.9 KB (6880 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:1b39c67bb7de548f2b5ad9f7ea0a0f211e2a8d1d50d48203278df043e10add50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.2 MB (68164605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61f1db77ac613e5e7c5068e2f38832a0c4e1ff13acddb7f13df9414d3b760871`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1743984000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7f935b3012df284a962222bcccf691a593747f69aa524b90eccdcf9bed048a7f`  
		Last Modified: Tue, 08 Apr 2025 00:26:28 GMT  
		Size: 44.0 MB (43962830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:625705c4ef1fc9cf5c68338bdc47ec99f95384a22547d22ce9113fa1a4477154`  
		Last Modified: Tue, 08 Apr 2025 07:39:55 GMT  
		Size: 24.2 MB (24201775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1983bcb28facf650db24f123adc1b418e69060aca10789cef6558114845fae0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3976328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:037b1de599320f27a86e0fc360b95bd62e6e062668fa5a5675de6c7b7edd895f`

```dockerfile
```

-	Layers:
	-	`sha256:ec2fe1ae0f8e7f9ae0a1669be7f0683afe72f9d73067f511ff5eceb1dc72c80e`  
		Last Modified: Tue, 08 Apr 2025 07:39:54 GMT  
		Size: 4.0 MB (3969447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c4755a57bbdb681e6cc9e3c28f17d98d5b012a0dc3d01d9c145e09325e986fb`  
		Last Modified: Tue, 08 Apr 2025 07:39:54 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:b039666763cddd0d240336958f4d49e81c541876e52b3afa0f51936550624686
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73650572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:225622767af9757b460bf48f06e944b54afd6eff198c4b578a2210ade3ba5316`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1743984000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:60dbfae895846be1589b057802d5cd4dd276320555a3dce75612dc628209cb7e`  
		Last Modified: Tue, 08 Apr 2025 00:25:57 GMT  
		Size: 47.9 MB (47922433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb7cce4b3d3d4958fcc2ffe1fbbf0181efd0f5febf1b3b140f3c5fb190e3e83`  
		Last Modified: Tue, 08 Apr 2025 06:04:42 GMT  
		Size: 25.7 MB (25728139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d46f4137be5ec8efab8adb9a4b49f234df59c4b79bace7973e5a254ac2ea2f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3977025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3aecb5977c07f20c0031f6528ff70dc9a272e056cf275b1788262441a73bdb6`

```dockerfile
```

-	Layers:
	-	`sha256:0e46af91437af27781429ccb51702ccb8b38e02093584db9bc61ea2367c0db85`  
		Last Modified: Tue, 08 Apr 2025 06:04:41 GMT  
		Size: 4.0 MB (3970125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c86dc51c723da2b5174b50f5a8cfe212e003f7d8e83a21d1e7576de08deb8a24`  
		Last Modified: Tue, 08 Apr 2025 06:04:40 GMT  
		Size: 6.9 KB (6900 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; 386

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

### `buildpack-deps:testing-curl` - unknown; unknown

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

### `buildpack-deps:testing-curl` - linux; mips64le

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

### `buildpack-deps:testing-curl` - unknown; unknown

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

### `buildpack-deps:testing-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:ca1e695bf0ea6c3ef638420576b9f2e1abcc88eb07c3910b45ab799ef057d515
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.0 MB (79046871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bff61944945065e54eaa71b7b31e51dd790a6517f4b0f772d6312e420661d01d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1743984000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2152bfaf5665d7c627f661d81f1ebb038ec9b798a3becef3f95f6ec6dfa2adf5`  
		Last Modified: Tue, 08 Apr 2025 00:27:27 GMT  
		Size: 51.2 MB (51205085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0924c3716841f5effee584d0edc58283639e6ed70d2000758424dcc55e8232c`  
		Last Modified: Tue, 08 Apr 2025 04:32:21 GMT  
		Size: 27.8 MB (27841786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:10bb5e5550cc8080be855d33233c3d2db101132dbb6b914e6bc29d77c89a3398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3984712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cca74621c6640202d32fc6f6d873a71eee688ef328335e47759792ee5b05581d`

```dockerfile
```

-	Layers:
	-	`sha256:50ea3e4675d041dda2312ef9e098a5fc2ba731bdfbebd7ad99a25fb1d6a3613b`  
		Last Modified: Tue, 08 Apr 2025 04:32:20 GMT  
		Size: 4.0 MB (3977859 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bb0da1a6696b27128ed4ff4f96fff15c1dadda054fd16bc727c1219527a7a42`  
		Last Modified: Tue, 08 Apr 2025 04:32:19 GMT  
		Size: 6.9 KB (6853 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; riscv64

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

### `buildpack-deps:testing-curl` - unknown; unknown

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

### `buildpack-deps:testing-curl` - linux; s390x

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

### `buildpack-deps:testing-curl` - unknown; unknown

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
