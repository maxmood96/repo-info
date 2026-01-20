## `buildpack-deps:bookworm-curl`

```console
$ docker pull buildpack-deps@sha256:54d2b75069cb06d0800f28b8930663a7b5795da4b341730b48afa3c1e54bbb50
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

### `buildpack-deps:bookworm-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:b7cf8444dcf02675615bafdf78fdfd8ad49aeefe039a351259124dbeb9a7a596
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72518489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13fcb1bbd7ff78aa42bb32551603f988837d3b634f65a4356cf8bcb157f92176`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:08:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c1be109a62df95316ceac87ea501079f32e17f36b636865a860841b7db06100c`  
		Last Modified: Tue, 13 Jan 2026 00:41:40 GMT  
		Size: 48.5 MB (48481622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64538a062a61add8dc8b290fa69475e8902eb839c497a5f5dcd5a950422e493c`  
		Last Modified: Tue, 13 Jan 2026 02:09:06 GMT  
		Size: 24.0 MB (24036867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7065088be77b2f2de334f7259b2a8a2cc0287248c0aa9dc59b290c1927412a37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4521151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44cfa34a6b0e9a331cf9533d8c55dedbb92b54c73bab9a15307df9c3f24e336f`

```dockerfile
```

-	Layers:
	-	`sha256:9ce83997a374ecda2db2639504dded3617169a314d1b173a0c26eb57f7551e62`  
		Last Modified: Tue, 13 Jan 2026 03:36:20 GMT  
		Size: 4.5 MB (4514334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bad5112890ee25d0afb08ec3040f3395af4333b453f0ac4f44acaa83267e719b`  
		Last Modified: Tue, 13 Jan 2026 03:36:10 GMT  
		Size: 6.8 KB (6817 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:1995fdcd40940bd4017bf442a49958e8e7acfdb3b67e292fb05a709c83f6d9d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68729366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83719177188e21723994b3266aefd3c2638d40d229568ce3fec83b4f4417debd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:28:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:3328d590af06d44e564f37191fbae5238775007425643c6f6e4f3136ae883b75`  
		Last Modified: Tue, 13 Jan 2026 00:41:51 GMT  
		Size: 46.0 MB (46016731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5bceff052bbfb51ccdda1b71d208734d7536dbc22a0d2c8310def26afcb3273`  
		Last Modified: Tue, 13 Jan 2026 02:28:56 GMT  
		Size: 22.7 MB (22712635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:146ed2611e114791f55a0ad58d26c6da95f9cdabc8b96c1486e68693f4c43047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4525031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0d35df89de0f5907e06760d6e124ff76715a7be56bee50ba5fdf5130ca40b90`

```dockerfile
```

-	Layers:
	-	`sha256:1b24a16e99ea89ab093ef29cfee1651c37e9761758b9f6c138be33e9d8f8a098`  
		Last Modified: Tue, 13 Jan 2026 05:21:57 GMT  
		Size: 4.5 MB (4518150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08adaf4fd619c62e860d5eb7f25eb8cf8b2980e9d43b855e1ebe48e29676a1e6`  
		Last Modified: Tue, 13 Jan 2026 02:28:49 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c9a9fb650a7ce89f8958895175819c60fc58ff06cd834ff53036a40ff8c4bd0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.1 MB (66140333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42813fcb8311ce34da73e53a7e868834940864b0ea2c78f731a8eb0702acf80e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:57:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d1f8df344790c402ed8a818bba76e9111f5e212418c662cf0574919edf68933b`  
		Last Modified: Tue, 13 Jan 2026 00:42:02 GMT  
		Size: 44.2 MB (44198845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b61baedfd715aa7493fd2550daee1914be821a60dd0067158988236109172a`  
		Last Modified: Tue, 13 Jan 2026 02:57:20 GMT  
		Size: 21.9 MB (21941488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c57e72f835f0be7855b2c6f2c3060e78c5df19999fb650513c6bc2f91bd3f33e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4523504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b9c597a8057615a3717b6b989fced787c539c506878c7469bd079f4c3800dbd`

```dockerfile
```

-	Layers:
	-	`sha256:5cbd56c3e2362248a251a8167371e8412a98a9e66c9f35cd40f1125aaf3f0c0e`  
		Last Modified: Tue, 13 Jan 2026 02:57:19 GMT  
		Size: 4.5 MB (4516623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7483a22b5fce835c440ddaf7b858487f983886914b57403dee31dc7eddd58d0`  
		Last Modified: Tue, 13 Jan 2026 04:08:24 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:d9719bc658367d9f0bdb7dddf822b599be2aed96ef76494764cea8fbed7b4633
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71970886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63ccf0e71e266ced52bb15c0b90a521004f34a628f297aac45c18e1b82aace94`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:12:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1029f5ddc0d24726f1cefbb8def7a88f8ec819a1fdc4c05ce523011b4b73c72d`  
		Last Modified: Tue, 13 Jan 2026 00:41:14 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72c713ab317dd7f302a6ff5a345af5b61cddc864fca2d96a23e6ef3c90a6657`  
		Last Modified: Tue, 13 Jan 2026 02:12:51 GMT  
		Size: 23.6 MB (23604814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ef48b36960c432b0a017c954f19894ade53201b1dac05f17df1ddd87de8adb7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4521492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d224b034d04e51f5fce08dfedb4aeece2d3852bd038b8f08c76329be339b8bf`

```dockerfile
```

-	Layers:
	-	`sha256:636a39ae5ac4ce7a3a7c2aa2e86cf66bf070d2af14dea3c740e3d1dff1aae900`  
		Last Modified: Tue, 13 Jan 2026 02:12:45 GMT  
		Size: 4.5 MB (4514595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f062f3f11b69284fa942eab76a024545f6380c46de8286c49e56df0f8b7f12d`  
		Last Modified: Tue, 13 Jan 2026 04:08:25 GMT  
		Size: 6.9 KB (6897 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:45a24a5874d925916682f474845b6d69efa2ba40af901031995b821efc8d7408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74339924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c57cc7848e5fc3084ca9d256b9e3a4483b3e253702a9890e5b27da3a51bd7178`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:02:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2ec54d337d067729b748c8f421e417d2e02e79e9e0caf328deaa1b815a93c883`  
		Last Modified: Tue, 13 Jan 2026 00:41:57 GMT  
		Size: 49.5 MB (49468594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63ef3b5e8322d4c8e5ca6198e931fb91c384bac3ef8aafd81a71617e9534b7ab`  
		Last Modified: Tue, 13 Jan 2026 02:02:23 GMT  
		Size: 24.9 MB (24871330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2ccb2b55d92b63ebd8bb3d429d5d656e6b784fae2a0e4fab372c91470a54c93e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4518248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e00deab0c13b0447054cd9c4d2a45b0d39fa9d5b95d8099f12723ad2eaaee0a0`

```dockerfile
```

-	Layers:
	-	`sha256:bb1389d719b86749dfaed4e5724c99ece225c0cea1c75e610389d477f0bb9a97`  
		Last Modified: Tue, 13 Jan 2026 02:02:14 GMT  
		Size: 4.5 MB (4511453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:839d6a2b1d6aea6a9d731a28f8d0d5e52ebe7eefbf5a658b105f15f313160b94`  
		Last Modified: Tue, 13 Jan 2026 05:22:38 GMT  
		Size: 6.8 KB (6795 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:700a0d81a40eab7f328b882d254e1abbe3a4d6a319daa9ad44fe516728610bb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72378045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bb42b3606274f54ba866bf682c4e725aa68479f07a82057fddb5ca9566419ec`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 16:17:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b4c94e33bcdbce9a62a95be51a6e5f8ed2efc653e4be8f8f6722aa13d9d65461`  
		Last Modified: Tue, 13 Jan 2026 00:40:12 GMT  
		Size: 48.8 MB (48763393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3ebdc0d40ea56bd8ca0e23bf6a7db8ca22ab77cacf0ba126e24eb42d35c708`  
		Last Modified: Tue, 13 Jan 2026 16:17:52 GMT  
		Size: 23.6 MB (23614652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6e984defad129c8a78b4262cb42159c2f9e281150aa15b2038dcf0f1543753a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 KB (6650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fde7f297e821ab224eaec637513c02abc29a436f2e14a99ed04be0ba579413f`

```dockerfile
```

-	Layers:
	-	`sha256:c5470282f056a988706b5b9a8c9d3aad0653e23d3dc22cb5a4a3e5a186de779a`  
		Last Modified: Tue, 13 Jan 2026 17:19:57 GMT  
		Size: 6.7 KB (6650 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:5449b5ad9a18a8233fb697d7ef0cd6e54bb522e84d3304c8f245175147268fde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (77998079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a81aa13e629b42f19d31084d74dfd490a331541943c20cf21f627ae4b4af0a0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:34:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7fcf9f2b462d6af06c3ad2420b999e6b092984c4723ebac480c428a5d837d3b7`  
		Last Modified: Tue, 13 Jan 2026 00:40:39 GMT  
		Size: 52.3 MB (52327376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2769c4ec4b4d67e8059086401477839f8b9d5a5026dd27df50a3c7ce33b9db`  
		Last Modified: Tue, 13 Jan 2026 03:35:30 GMT  
		Size: 25.7 MB (25670703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ede9073f608b535421ead831dd63f44085f1d6d2ceceb99ea0b1deb96d4030f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4525808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8d06e073ec71f7dc861b4a5191ff89acd59148878647ee9304596032f3a2e2c`

```dockerfile
```

-	Layers:
	-	`sha256:623c70215bd360f0ac1243a876ad09b5bb5c5cf4aea40e1a7192fc8e6bb40a3d`  
		Last Modified: Tue, 13 Jan 2026 03:35:30 GMT  
		Size: 4.5 MB (4518960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99b0cb2633a75607ca0e52e27f299d1cc682cd0ed2401896847f594c3ee4a0c1`  
		Last Modified: Tue, 13 Jan 2026 03:35:29 GMT  
		Size: 6.8 KB (6848 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:aafd3a6e786ae512bfb25636b963a8ea303887ee75da44f16b8f4c470c261153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71170921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2002c77530b9e0ca5e7a947f8fa4b32803589aca901fa7bb0e7b0097203762c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:09:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:533e1723f6efd3a2dac5ef2d710062f1e6292bf061b83d41b908fe862b8922dc`  
		Last Modified: Tue, 13 Jan 2026 00:40:05 GMT  
		Size: 47.1 MB (47138430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8133db08df54d1100dff2f0259f057251959db22c09d939ae558af001aa8088c`  
		Last Modified: Tue, 13 Jan 2026 02:10:04 GMT  
		Size: 24.0 MB (24032491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ced73db595824188533e1814db5d3427622166273ed32aefd4b6fb18dcffb69c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4517955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2bc1cf356903159aa71a30b1b59edc158ccf20843d0e937db08b7771e7fafaa`

```dockerfile
```

-	Layers:
	-	`sha256:56436f1922519e0c2ce947cdc5db236d30b7fc6d09da06732b13a3f6c2c43b68`  
		Last Modified: Tue, 13 Jan 2026 02:09:57 GMT  
		Size: 4.5 MB (4511138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c54d20256e1149243e9cd7a542cc94f4f17e6a46b43bd02404c60bf39d42e36`  
		Last Modified: Tue, 13 Jan 2026 02:09:57 GMT  
		Size: 6.8 KB (6817 bytes)  
		MIME: application/vnd.in-toto+json
