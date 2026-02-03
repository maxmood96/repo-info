## `buildpack-deps:bookworm-curl`

```console
$ docker pull buildpack-deps@sha256:e9a5f19946fd4f3051a5850b032115fa97b7cd1a029b386b28808f852f0b3497
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
$ docker pull buildpack-deps@sha256:d8879bc728ac7c0764e308f22ba436f8bad2b5bfa0b463684dd1d641706928c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72519929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f60f9f0ae8eeb825aa6b8a15a2ea60bc7b7139f7e72a695a8217a45e196d1d21`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:41:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89edcaae7ec479668d9bf0891145726173a305c809a8c4165723ceaf15b5a05f`  
		Last Modified: Tue, 03 Feb 2026 02:41:49 GMT  
		Size: 24.0 MB (24038446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:952bc903af6d7a9b5a7dd19afab8cc73d8170dedeb009c0f034b0b32521ea484
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4521151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42ee624a8f11b76d72ccfe31f4fb375e92e46d54edc8316a067060788a2c25b7`

```dockerfile
```

-	Layers:
	-	`sha256:256816d9208ebc4ad765cfdfae623b751d228d5e69bed7d06b0e3b397685c86c`  
		Last Modified: Tue, 03 Feb 2026 02:41:49 GMT  
		Size: 4.5 MB (4514334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:902762d96a20fe2435a3f137a7d9873b01a3be076223d73bf8b713861bc1e341`  
		Last Modified: Tue, 03 Feb 2026 02:41:48 GMT  
		Size: 6.8 KB (6817 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:4b3d1a3c35d0c2a8feae491795861cb3cf0942b8457b83a5ca828053db0539dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68730571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a83ffb1d7d4120e075c1964d643ff0e3533f8252f66336752a0186aa4e0734b6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:25:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:48989bca0bd1f08c49cfd2a8eae58c5ffcacc0f005e701953d88f28a5e398ee1`  
		Last Modified: Tue, 03 Feb 2026 01:13:21 GMT  
		Size: 46.0 MB (46016664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca8c031851c0852eda9cc103afa92ccd1ccefa07dd936a71f291d45de349d70b`  
		Last Modified: Tue, 03 Feb 2026 03:26:08 GMT  
		Size: 22.7 MB (22713907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:870a33044461421739ff5b4a869a872fbefc691cefd8696372286869f9180980
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4525029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09e8bcfd0f3724cf56727bbcf05b5fb45363544d8d193f0136a25f8e88d32e0b`

```dockerfile
```

-	Layers:
	-	`sha256:3f8096c1937d1063e8269f60b806128f1088b5c0dabf4ee38d808c835466d57b`  
		Last Modified: Tue, 03 Feb 2026 03:26:07 GMT  
		Size: 4.5 MB (4518150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aeda3a98452b7687e4f2084744f06111fdc68632c7f6acca7828484391283a95`  
		Last Modified: Tue, 03 Feb 2026 03:26:07 GMT  
		Size: 6.9 KB (6879 bytes)  
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
		Last Modified: Tue, 13 Jan 2026 02:57:19 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:12:45 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:12:45 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:02:14 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:02:13 GMT  
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
		Last Modified: Tue, 13 Jan 2026 16:17:50 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:40:14 GMT  
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
$ docker pull buildpack-deps@sha256:051c6df271106c663f36f059f90f7d1fda18978fd91bb431a9c91135e25028fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71171976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53fcacc610a385c3e9cc46470e493d709dc8f36d692bce3ad8e477fca012471d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:44:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:4c4c4621da5085342b3b0d8d8ef57e5e44004eedf5818268af30c41a02cb6cf2`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 47.1 MB (47138343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3072e3eb8c224dc593a4e18a3785b06d51467102b1cd9dd426d3d31d0e6831b8`  
		Last Modified: Tue, 03 Feb 2026 03:44:33 GMT  
		Size: 24.0 MB (24033633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2429be608bcc29adcf5c17641a47ba78b0d37a9f22bc24f66651f887fb42048a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4517955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cae194b262b784f67b07d1ce638abdbbac2fd60acddf1d85e52dffda32007df`

```dockerfile
```

-	Layers:
	-	`sha256:0eb34adfff78af64648b5457a9dc47c9d3a5103970c0bd5c5a92d2b6156696ed`  
		Last Modified: Tue, 03 Feb 2026 03:44:32 GMT  
		Size: 4.5 MB (4511138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e589c51cce89fd7922fe52b471df7049b467cf36b7567887cceb12fb3d8d81f1`  
		Last Modified: Tue, 03 Feb 2026 03:44:32 GMT  
		Size: 6.8 KB (6817 bytes)  
		MIME: application/vnd.in-toto+json
