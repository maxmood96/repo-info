## `buildpack-deps:unstable-curl`

```console
$ docker pull buildpack-deps@sha256:f08c8a8d6c930bb21ebdb5cc22857f4f69d357030d0b55a17dabca3d2a3b06e7
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

### `buildpack-deps:unstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:8b17e971281e27f87a12ec4e748e962f1b7baba752cec24d87a381b914d86891
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74407236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59739316696b047a063f3456985a80d52f1f105747e6d32e3ae77b5986fd1771`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1736726400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:76be34fccf5c64699db16068e9e561c466873ad6fc8da852c8c21801ed35861d`  
		Last Modified: Tue, 14 Jan 2025 01:33:25 GMT  
		Size: 48.4 MB (48375138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81659ab3e6cea3ecbc9d772f851c94ca5f88bde45b2b1d558924da5b4ef5f256`  
		Last Modified: Tue, 14 Jan 2025 02:33:23 GMT  
		Size: 26.0 MB (26032098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e3b6fb81a38a113f3962dbb934f9b0670271e5b8a93f5908e441fe1e7425fff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4038575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71bbf5e0508dd4707bf6bb74846c218a7feb7b0fd27e0d0dad1e2b4287a48ce3`

```dockerfile
```

-	Layers:
	-	`sha256:8fee6fb6e21d36d0498d022db0a19f043de268e5ae42f3f8dd9cde34347aade8`  
		Last Modified: Tue, 14 Jan 2025 02:33:23 GMT  
		Size: 4.0 MB (4031771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c95a28e675d5a6c851cd32a95c43e82768d5ddded17ec26244d8eecee727b56c`  
		Last Modified: Tue, 14 Jan 2025 02:33:22 GMT  
		Size: 6.8 KB (6804 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:2e3d4c41173a65255d8e9f474f2645eb6b89cf3eb79c57f812131691c878722a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71263487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc55152d9e477751056fa8732484dce52295aac07c1464c0d15192a84b4fae23`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armel' out/ 'sid' '@1736726400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9d52a976a3fd7f28c8f846fa169d38eb4f52aab56f9ee1cb5fbdf7c3d31fa88d`  
		Last Modified: Tue, 14 Jan 2025 01:33:50 GMT  
		Size: 46.5 MB (46532542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f95931378232e134e2433bb5ceaf5ca525339c23b43efde26fa179c793eec5`  
		Last Modified: Tue, 14 Jan 2025 06:09:14 GMT  
		Size: 24.7 MB (24730945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:089b947caae554abea5bab72a05aa1e4404e8a76d8c4fca9253f7751474af292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4046262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5246254afe8778afae333f523a584d1226cb2a002cb1ef65a20002745f4c0a5`

```dockerfile
```

-	Layers:
	-	`sha256:9e4f27586755d5d450ab1167d0b495bc9fae51309cc905a39eb7893f08c1e94d`  
		Last Modified: Tue, 14 Jan 2025 06:09:14 GMT  
		Size: 4.0 MB (4039398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71d03db38b336ef73cc632bb04e76f0ab45ca7e36b821863789f827692ebc70f`  
		Last Modified: Tue, 14 Jan 2025 06:09:13 GMT  
		Size: 6.9 KB (6864 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d7a98462c8b2665ec5ed80d3719a6b961f7dc27be6a1e73b0d6955e27280adab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.4 MB (66372254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32f4c926a645700c6a60e137cbc517064f73cc493dc1f291b9db160493b7bf81`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1734912000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:fd381bc5446358c906dd1f7ac3878d03bb1e1267963891069c3e6e2c97919218`  
		Last Modified: Tue, 24 Dec 2024 21:35:32 GMT  
		Size: 46.8 MB (46763305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d419ccba1fe0df7cd0c879e1f8261dab91d1fe412b8df835212e60f95b90dbb7`  
		Last Modified: Wed, 25 Dec 2024 03:45:03 GMT  
		Size: 19.6 MB (19608949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e5b3c6617ddc7dfa5dea4d3466e8399618b939191fffa4e666881163ce473a40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4041932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:042a5ec05a2dbcecfd32ecd687fa246d4491292091e2d89c797d7af6f643785d`

```dockerfile
```

-	Layers:
	-	`sha256:b6aa0f1914b7a5871c3455f98cc4a855f772f57484729913ba9ea9074a616a84`  
		Last Modified: Wed, 25 Dec 2024 03:45:03 GMT  
		Size: 4.0 MB (4035068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:226f2c9463b01100e1886f2b39cd87877b091b38888e03a35733eb5434dca693`  
		Last Modified: Wed, 25 Dec 2024 03:45:02 GMT  
		Size: 6.9 KB (6864 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:c83c48975e59ec64bc91d3769c432a66500daca094b33ce44ab83be443c6a242
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74248184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab02be95b5da529e7fb4647e9b02754677606d263be1d7f8ac3df34880d7e218`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1736726400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7cef9546887caee4cb752860ee90de96728f638ede0f77bda226ca44ac3e04db`  
		Last Modified: Tue, 14 Jan 2025 01:37:16 GMT  
		Size: 48.8 MB (48760872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94fc550a04d72fdc48fc4716034190ede3de291a338b2c748b32584534d2c3f1`  
		Last Modified: Tue, 14 Jan 2025 07:00:48 GMT  
		Size: 25.5 MB (25487312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b5c55261db3e4295d506a8d30de535fd6ce1f4919b39b712c8ccd9a14182b880
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4039550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59e0cadce91856b71f7b39a1fc82a462194230047124231cb8f824187410c533`

```dockerfile
```

-	Layers:
	-	`sha256:84346bc302c355ba088ff6ca252478af992d79a3b271ea6c81a28c744a77f818`  
		Last Modified: Tue, 14 Jan 2025 07:00:47 GMT  
		Size: 4.0 MB (4032666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95e1cc850f1be00f65c60bc03d242d9a9ccdbf55ba096fa5e73e3ab32571ef0e`  
		Last Modified: Tue, 14 Jan 2025 07:00:47 GMT  
		Size: 6.9 KB (6884 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:3ad37b2dcd28f685646a6402d5b8adfe85ccfa8ac2c965d2fd0c51f00ba0d9ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76956374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:173b36d3b16eead41f1843f7ba041028b748b36625049ffb23e2ca42f2a3a95d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1736726400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c1e4243a6e921bf817bc744dbf559de39acec531c69436c119d566f9645bf931`  
		Last Modified: Tue, 14 Jan 2025 01:33:25 GMT  
		Size: 49.8 MB (49778367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4499f1145672c6dc66a0a48bab855b0052609dea7a87335a024adaf65cda0b10`  
		Last Modified: Tue, 14 Jan 2025 02:17:21 GMT  
		Size: 27.2 MB (27178007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f10e59deb4d2ab8d9eed6344c58b6190b8be764ae53b081205e229f04fcb04db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4034312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d11ed9d4a01bf3e2a3ab36bdfe85442826166ab920e3882547eb9b477c9185f`

```dockerfile
```

-	Layers:
	-	`sha256:ea766fe1d81e37e5d8cfdbf66578c790022af7cefe55aff47572b8dc44ce910e`  
		Last Modified: Tue, 14 Jan 2025 02:17:20 GMT  
		Size: 4.0 MB (4027531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b6e44ac56df603b73a8c9faa441eb3446866746891ec52de027c3f6741144a0`  
		Last Modified: Tue, 14 Jan 2025 02:17:20 GMT  
		Size: 6.8 KB (6781 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:50e70f2127c9f6e52940262154905830dffd9631db8473b38d0585a06e999163
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.5 MB (73512165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e647cc1399184363c56fcbb5caba756f2172cad8a5a00c2cef5ee01e7359bc4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'mips64el' out/ 'sid' '@1734912000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2225e4bf9a501ecd52da3f4301136a4a3ac3273d704acaffdf95ff67153847e7`  
		Last Modified: Tue, 24 Dec 2024 21:33:59 GMT  
		Size: 51.8 MB (51771333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8315cddf1f38d3ec912dd995fc72b7c70105918274b7bd71b5f66a9e8789a52c`  
		Last Modified: Wed, 25 Dec 2024 11:47:53 GMT  
		Size: 21.7 MB (21740832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5cc60a636a3bb6bef78af7f5c6312f9142ffa4b2ce3bac63639b71a25062fe38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 KB (6636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a41d5aa923e4bc77a98b55948f98024c6662e9c4aff1c2c79316455aa4959ecc`

```dockerfile
```

-	Layers:
	-	`sha256:a04c57573b2f348060f05c85d208a1e09720aff18837ff96060774daef4f3f0a`  
		Last Modified: Wed, 25 Dec 2024 11:47:50 GMT  
		Size: 6.6 KB (6636 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:81fd6b47b6a9247893fb056f51faf4cde94157077cb3b4b3752f2e26aeb98285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.7 MB (79743734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35c15ebee6a0c31867b3869424b8ca1ba4949f834988447a1fb70a2fe76130ee`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1736726400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:fca4ba78a63cac2994d6f3576656e907e3a130a20f935b6a1e2c945c9e7be3af`  
		Last Modified: Tue, 14 Jan 2025 01:38:04 GMT  
		Size: 52.2 MB (52151887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f2cddc488774629199c39c9010734d4be824e6ca934835a5e2d444a85e0075`  
		Last Modified: Tue, 14 Jan 2025 05:31:14 GMT  
		Size: 27.6 MB (27591847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:62592d47696bfb1aa608ecb264ff067d7593def38bc093ba3ca27d71840a87b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4047264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bcabf793dd2ebb49f6b028a126507532489143a60f7231ae912f42e518a66f7`

```dockerfile
```

-	Layers:
	-	`sha256:83b93f94e4e18e14bb892f3b235d9fb21ac4dc372b87fb0825b17d5915a855c2`  
		Last Modified: Tue, 14 Jan 2025 05:31:13 GMT  
		Size: 4.0 MB (4040428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81fd70a663d916019d7645c2b48be34186760dd87ab7eb4edabe23d366a8c7db`  
		Last Modified: Tue, 14 Jan 2025 05:31:12 GMT  
		Size: 6.8 KB (6836 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:50021e11eee76dba7ac182e699db82016047b4bfb03614b607e8f10dcf7f56a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.5 MB (71541258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85fd3d28d52f8c78f85479acfb52556916a6e52200a534c191dc24122d5dda25`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1734912000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:34dc7eee421e2547a72cc18fd960cb61e4cc000ae2301ebea5c1db40e2f928c9`  
		Last Modified: Tue, 24 Dec 2024 21:35:00 GMT  
		Size: 50.7 MB (50711803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b3be9202d049cfd8fab2840745aba862531c266ca24caab8785a1201a2bb14`  
		Last Modified: Tue, 24 Dec 2024 22:26:29 GMT  
		Size: 20.8 MB (20829455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f53b2ac9fed4061453562312e21afd15faad1577fb53f0b0f2cfb205f6a061f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4033707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aae945f46e3609de2dbefeb26f1a614dc9d20e61bc0b77b7045f2cc3d12d0cc5`

```dockerfile
```

-	Layers:
	-	`sha256:6bca95a5f4bd3c228815e0bd31fe5ff166763bd835d40040cef458ae93f390dc`  
		Last Modified: Tue, 24 Dec 2024 22:26:27 GMT  
		Size: 4.0 MB (4026874 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2de7857568615e172daa16b49de08a8ce618e0608088db6eeb7400677eff33a0`  
		Last Modified: Tue, 24 Dec 2024 22:26:26 GMT  
		Size: 6.8 KB (6833 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c82776b0a8fb114feaf3c2959bf03ca2f559d9b7775d86bbfb6e11576921f738
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75631494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c47bb0dda09920e142ff762fb7ee673f40cc3f13b258b49f107bc867ef7b260a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1736726400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:98a334b3a419c858b25979b9c4fcf97a87431d5b5cddfa6c4c566454b23fcf62`  
		Last Modified: Tue, 14 Jan 2025 01:35:18 GMT  
		Size: 48.4 MB (48434824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d732c90ca5b141c789480c7eea03644a6f254edf6c95ed1e124a245a18b8c3cf`  
		Last Modified: Tue, 14 Jan 2025 05:00:30 GMT  
		Size: 27.2 MB (27196670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4a78274b4f0de77d22c922b39498c0cf901859f071a4a9c1a2cc3172930bcd60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4044908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bfd129fa5d4d339837cdf52f27c7e2d548faa7cebe9271dad85ea1f7e1c28b2`

```dockerfile
```

-	Layers:
	-	`sha256:7068b7ae6551d459304e20445f3c3a39ab077ce28abfce1d057cd28ecaee93c5`  
		Last Modified: Tue, 14 Jan 2025 05:00:29 GMT  
		Size: 4.0 MB (4038104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cc84de5c62e5e35aaaf7377fea0264ac111304a1f3a90f2e312a3a9283843ee`  
		Last Modified: Tue, 14 Jan 2025 05:00:29 GMT  
		Size: 6.8 KB (6804 bytes)  
		MIME: application/vnd.in-toto+json
