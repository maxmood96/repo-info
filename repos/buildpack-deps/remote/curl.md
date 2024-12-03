## `buildpack-deps:curl`

```console
$ docker pull buildpack-deps@sha256:b0286b27ab38d12725154c3bdab991834a6fd289ada63a2fd1cfc830286d75f0
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

### `buildpack-deps:curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:e4e69a8b7f9e04139295fb9dcdf37d823b148d1c112e36b0653d11ba96c6604e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72363086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d5ef6bc224b02787f00cbbce868ebbadc4fe38a2a978313291c878413ee721f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fdf894e782a221820acf469d425b802be26aedb5e5d26ea80a650ff6a974d488`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 48.5 MB (48497210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd71677db44bb63b94de61b6f1f95d5540b4ba2d6a8a6bc4d19f422b25e0c2b`  
		Last Modified: Tue, 03 Dec 2024 02:28:49 GMT  
		Size: 23.9 MB (23865876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7ff9434e13b1f41e3fdde66e19d17f3c35636e0cd182bf0bd4386e2af4124d9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4371222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43bd9c68c9fe0a5c3db25a9086681f8f9c104c591606a18bea36b7dad3af97b7`

```dockerfile
```

-	Layers:
	-	`sha256:996b54fd1b681c68f21142e93f996d2ce61d3345a3aacb49c85c12238b4a15e3`  
		Last Modified: Tue, 03 Dec 2024 02:28:49 GMT  
		Size: 4.4 MB (4364058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aef3835c1fc0e6916ee36bb9b108d4e0947caab9bf621401475a88e457ab409d`  
		Last Modified: Tue, 03 Dec 2024 02:28:48 GMT  
		Size: 7.2 KB (7164 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:9ca627c143143071812435f20a31d7ca4a98f8f69eb5772238d5ab4c289773e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.6 MB (68564756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d52aedd03a58bb0c09f5e307d64f49efd1f50d13619447fd27ad609070014374`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a8ab0b752e573ceb3480052f24bc5fe3f4f4665c13a338db39c1d51f749528e9`  
		Last Modified: Tue, 03 Dec 2024 01:27:04 GMT  
		Size: 46.0 MB (46024374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff6779451547ba3f0647f15a65068290fed53b6a4ac506257de98e02857bea6`  
		Last Modified: Tue, 03 Dec 2024 05:23:42 GMT  
		Size: 22.5 MB (22540382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2e2143039fd9074ac1c8fdaa9a11a3ffe40a93f547cf21b14da9b30f7dc7c54e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4374804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdf6d29be9af0b06c9bc426a0e4301f021a0d39b9c43f96faaf88c5fae8fdee9`

```dockerfile
```

-	Layers:
	-	`sha256:39e78f22f1d8edef86ca11b2156afabce6625a25d4fe1969f2b9b7fe1e12e885`  
		Last Modified: Tue, 03 Dec 2024 05:23:42 GMT  
		Size: 4.4 MB (4367573 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0f81f00ceef9b327ef81f33ce0ac9ef30236b95c3793935d843dbbae8791bbf`  
		Last Modified: Tue, 03 Dec 2024 05:23:41 GMT  
		Size: 7.2 KB (7231 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:4df85825662d4ccaf0c53f0b0f706602fca0555267dd2d31a62e8ef87e1d558d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67110580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3b88071c4591f6c7f807b8cad4c84e19227e69998bf7945120dfc8071b9014f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:46618ec96098836cac7950050ba554a969ebf8e9938d85d5f0d97015d3d25076`  
		Last Modified: Tue, 12 Nov 2024 00:56:14 GMT  
		Size: 45.2 MB (45150563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9660b2b46aa0c77f5dd078f4e57432faf3dbcda91672b9e3f8c1b7892e0ee2`  
		Last Modified: Tue, 12 Nov 2024 15:59:18 GMT  
		Size: 22.0 MB (21960017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:305784099f58635cead38aa11453521226000d86d85d52ee7848ca2c3be385c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4374834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a8010ae6e055d2fc8797a75c67215cd400f64870bba5fb87b2503a4bb2fd1ae`

```dockerfile
```

-	Layers:
	-	`sha256:54c117e288564eb3719195c06d6bc879daa602feb6e27a0feb1a1ec9e18bf464`  
		Last Modified: Tue, 12 Nov 2024 15:59:18 GMT  
		Size: 4.4 MB (4367602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fcbbc798229c876fdfad98f81fb68cc54fb00ac95a2c847e9e133d91ce28ce3`  
		Last Modified: Tue, 12 Nov 2024 15:59:17 GMT  
		Size: 7.2 KB (7232 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:757ecd28399473cce91e6be523aec8e79ca9f576cfed067466bcffa71ff9ac70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71731493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed0620fbee6bbd337320d030c3be4e71b8e2883828902bf89672a74d1a36278b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:82312fccb35f18983647c1ea71154b98ae9893fb61ca4febe12d584a3ea9ad6d`  
		Last Modified: Tue, 03 Dec 2024 01:29:57 GMT  
		Size: 48.3 MB (48325680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac722d9cf93b238dec2480278a2df5f8ccb672c97ec39f191191fd39f6721a8`  
		Last Modified: Tue, 03 Dec 2024 05:38:46 GMT  
		Size: 23.4 MB (23405813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:79739c087c54ec0d652199829c30eaba59e426e5edf317a72b3a318dd0cd8bb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4371586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc692a177ab4525e660f0d3f47205fd6ed2ad3a54e419ff10a28b6e48bc78535`

```dockerfile
```

-	Layers:
	-	`sha256:4816aacc299c61ab88c4e10c38abd2b3d51afb73adba3b8bb1debfd6846287a1`  
		Last Modified: Tue, 03 Dec 2024 05:38:46 GMT  
		Size: 4.4 MB (4364330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:913b8b80c5fa22b390e28ca34404e62e7d38090c8e99339fc5cdde2cf477b4ed`  
		Last Modified: Tue, 03 Dec 2024 05:38:45 GMT  
		Size: 7.3 KB (7256 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:5ddf951a80c7dec860666e1ff917ced4535353326c546dab88edcbab700e2345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74183048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:129a653e602a0fe253a2b069b2e2ab67f1ea9115e2fd72cc3ced51c193a26a5f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:53769c348e57d646b1ec110dabf9d81a3f570afdb3b8216d1178515e4ea4ce1f`  
		Last Modified: Tue, 03 Dec 2024 01:27:09 GMT  
		Size: 49.5 MB (49476152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b0c73f75a815ce87bbf2841b694fdc4c29bcd072480b8752e8e91f0b59097b`  
		Last Modified: Tue, 03 Dec 2024 03:23:49 GMT  
		Size: 24.7 MB (24706896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:eebaeeda8054688d6fd8c142a0fc0a9ccfa4fc3ca2b3499bfe916319c4994ca6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4368251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8937659e583da0ff6a76c8f743b3e42f34bd06dbbe6d065e151fb9bfada42aa`

```dockerfile
```

-	Layers:
	-	`sha256:729bb902df2997852a31087017dd8b75ede98123a831591b1b48e5519566d1b0`  
		Last Modified: Tue, 03 Dec 2024 03:23:48 GMT  
		Size: 4.4 MB (4361114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:310a36eb7785ee15a990c5d5843eb5ce31f673057b5dd6940687e2392aafaffb`  
		Last Modified: Tue, 03 Dec 2024 03:23:48 GMT  
		Size: 7.1 KB (7137 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:de1a2b9066af1286e9d8175eef66425cfbddc0251cbdc6e6263a68b742ee6437
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73211352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15b5e3786aaeddd9bd8e5b8cd2245dc5be46353f3dbe4aa169166a83607577e5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:17191dc8a469e4ef93330c5c8402fa0c0761218a5fa02ad2db7b34508d0e995c`  
		Last Modified: Tue, 12 Nov 2024 00:57:16 GMT  
		Size: 49.6 MB (49559181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf888157372a89189e8193ccb502b1003341993a439a6f526f90dc05a6100692`  
		Last Modified: Tue, 12 Nov 2024 18:00:45 GMT  
		Size: 23.7 MB (23652171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ee37e62e2a4f2b37b5059c26f65c50e79e8f12bede1551fe7c38dde1371e0e72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 KB (7005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:087a573000fee443714e51f8a22272ec23d27c5ef680d3b9f288f8ea41e63a91`

```dockerfile
```

-	Layers:
	-	`sha256:36da5312bc8de97460d5ca2df24b0a099c7af0db6158b101c163700559263cd6`  
		Last Modified: Tue, 12 Nov 2024 18:00:43 GMT  
		Size: 7.0 KB (7005 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:989e244c7923bf0590fb8ddd1cfda40228425477aed2564c4f1d68d5bf4c1211
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77852114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9269507941157f6d8c2a6aaf7d982955bbd6ad996a59aa0c335382fa56fedbf3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c84d784fe3c6c2bd95dea1c0d6eeba7c981bfb75bd53f81e83bcaadd87bba6f9`  
		Last Modified: Tue, 03 Dec 2024 01:28:03 GMT  
		Size: 52.3 MB (52328222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f0cfea13db30ebc69124696ada25182d1141398cd301a47a2cbf3c10d7fa9b`  
		Last Modified: Tue, 03 Dec 2024 04:36:57 GMT  
		Size: 25.5 MB (25523892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a45e69e0d085a116675b75a7b725f816d6446a3fb4ca0543c48e95c3f3fd3978
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4375753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83e3cdc76dad87b7234f6f31c723d08c241a2a7efa8c9039144506f957faabb9`

```dockerfile
```

-	Layers:
	-	`sha256:238d77a8b35e0e5b35ee3bdf19e0102de9c1fb1aa37b9dbc272bed8d60d9852c`  
		Last Modified: Tue, 03 Dec 2024 04:36:57 GMT  
		Size: 4.4 MB (4368551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec9892333b13de0bc61e2cdc3ecce83c24ed20bb5579e82cfaa2d4bbcfb85f33`  
		Last Modified: Tue, 03 Dec 2024 04:36:56 GMT  
		Size: 7.2 KB (7202 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:a0a6eb40a58c78dab49f2a7fbb55665c1a2af22ac7a1ac77580e07074365ec0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71014392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f68d8461201f6697d48a6322c9ab07b91a4490ee92e53b559914223bb89b0a6c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:53a5c0dbd93a4a7f540e18bbe49ba3d7fadaa390ebbce009c756e34c5b1ae048`  
		Last Modified: Tue, 03 Dec 2024 01:27:55 GMT  
		Size: 47.1 MB (47149767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ded5bb0b377b736e6c5f45164fe8916ada3485441e963fe2fc0671949650049`  
		Last Modified: Tue, 03 Dec 2024 04:07:42 GMT  
		Size: 23.9 MB (23864625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bae73931459a569e6aa2c77e5721402acdd0fa87c8499ac00c378f09da2b74e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4370919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb35bd02c831221f27c85d64464a87ff1e458b43c43e1a167b9614f44689a992`

```dockerfile
```

-	Layers:
	-	`sha256:9c310eee549867fde8b1fd56ec371ef6cbb8f19c03df6ec7b8c6a49b4dcd0703`  
		Last Modified: Tue, 03 Dec 2024 04:07:42 GMT  
		Size: 4.4 MB (4363755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e932d932ad0e9d02444cefa5146dd7acdbe99b89f0389f686355c2b3271a1eea`  
		Last Modified: Tue, 03 Dec 2024 04:07:41 GMT  
		Size: 7.2 KB (7164 bytes)  
		MIME: application/vnd.in-toto+json
