## `buildpack-deps:bookworm-curl`

```console
$ docker pull buildpack-deps@sha256:2ff813eea3a0911154b7bbe930a2f19eef3407fefde1a4a006e84e302b303380
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
$ docker pull buildpack-deps@sha256:3c27a5c578d74c1499c4d61a3894dd265aad5104dd06cf6bf75e3c3aa1073989
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72538806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25da6b4d07083d02e8a5938c7c12c66b63902b12dbade0391380d8be868a774f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:23:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:4887723d153cfd7fd9e356c8730311c36a64e4f9329f9d3ae1929e05715f2e73`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 48.5 MB (48495432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e51c50554dce9c9549d76c40bfea45780a8342aea81ba8b270ba1bf46a2aec5`  
		Last Modified: Tue, 19 May 2026 23:23:20 GMT  
		Size: 24.0 MB (24043374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8fb900b39c64fde65477f02d77824fd1c5d8ed22515c2b1efe789edbc2670212
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4521169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10cec41e507df102420c7c155125e35d8cf985787aa529f3c1f8e4d094ee2dde`

```dockerfile
```

-	Layers:
	-	`sha256:494f43e4237cfa18132237c26be36bb14e3c8e19ae9733bd72bcfc7c413485e5`  
		Last Modified: Tue, 19 May 2026 23:23:20 GMT  
		Size: 4.5 MB (4514352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02965b70413d0fdb0b9d3f5eea5ab5c8a27b3a81849971f839b4a7028e5b77ec`  
		Last Modified: Tue, 19 May 2026 23:23:19 GMT  
		Size: 6.8 KB (6817 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:dc88449e8114fffdcbb9c17ce056ca3204f9f8ea0073e8395cff883c02354525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68747130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc41aecba5ab0070254e596b1f1d33bad4ca629aaf6a0096cff03c8c22800450`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:55:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5de6cd71f4d67443f5513239f3846f94cf483b810583f2d4d2ba8423f1ec7fc3`  
		Last Modified: Tue, 19 May 2026 22:36:01 GMT  
		Size: 46.0 MB (46029503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37ec445b149b50947066418df58d379ecb3cbca1deae1f8b8054123d04c60e4d`  
		Last Modified: Tue, 19 May 2026 23:56:05 GMT  
		Size: 22.7 MB (22717627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:207793d3090a83d056d5cfb7ca65e2f7dbd158f1984544a36f76d4d4f5e2f21f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4525049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:266de8173203c2df6615e937c359ac620d29207571d18d02b317011f0050c0b8`

```dockerfile
```

-	Layers:
	-	`sha256:13216556668f988de1a2b964a8edfd868155a156cd629b0229309ad8167d5fdf`  
		Last Modified: Tue, 19 May 2026 23:56:05 GMT  
		Size: 4.5 MB (4518168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e43c606f1ec3d60201eb18ab74cedaca4e77ba326ba15c3ff14155e2a848bac`  
		Last Modified: Tue, 19 May 2026 23:56:04 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:aaa21bc173df72d972f33a8e086ac5a6e978e82ea65182b4f232b39bae3bb05f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66159287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59d9ef2d23b99f070d19dcbe2bea3767b0f6be847947e9e241a839032c1ac2f7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:02:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1af0b8b84389f4347663cc563bc1f6d59fe6d6f21081f428bafa1a09f6a276ce`  
		Last Modified: Tue, 19 May 2026 22:35:59 GMT  
		Size: 44.2 MB (44209154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a61246c0a5a0fe9fe8cdc1bfde0fdfa49ffafcc94cba31f4aecc0c34bc346064`  
		Last Modified: Wed, 20 May 2026 00:02:11 GMT  
		Size: 22.0 MB (21950133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:38766093b63d53414c84717200adb10428f14697011f5e5d3a6c692b2037dc05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4523522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2b62f5b81fb70cc5dbdb4f65c7b8d728d229df5d7fa876d89b9026701566c70`

```dockerfile
```

-	Layers:
	-	`sha256:bd38ec6d52bc66c3057bebf8dc71d1073006a81a89b8c8ff61844122476699f3`  
		Last Modified: Wed, 20 May 2026 00:02:11 GMT  
		Size: 4.5 MB (4516641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac551389b789fdd672ffbb781ba1fcfcd10cabfa030d13d0c2e97a079d53fb72`  
		Last Modified: Wed, 20 May 2026 00:02:10 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:e89d7129160e032bbcd1b05a20f99086c168da28d64fec0d63baeef64fa7377c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71992826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ac5508ff37f3ddd6fa1847f7a204a6b9ffbd5b9ba03141f4542fe52ad9326a7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:26:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1fbcdab7270278c1f989ae72190255d85d2117e990efb76cde6eb206b803672c`  
		Last Modified: Tue, 19 May 2026 22:36:02 GMT  
		Size: 48.4 MB (48379432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3daebbc198bd7b84bdd72840d7f4ded251896f03b9a9f880894e95e926bc543`  
		Last Modified: Tue, 19 May 2026 23:26:38 GMT  
		Size: 23.6 MB (23613394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7601cb1810ef46318d9481973fe2cb4b4c10e57dde6e06d1e820f60560fd9c4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4521510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77af731f8422a4f2cc479da864ea6444f24144276e3512904f39ed5aa8a0096e`

```dockerfile
```

-	Layers:
	-	`sha256:5524d780e995c69050174ce41123c1e1ab0483527b8adb22eec088ff6acec0bf`  
		Last Modified: Tue, 19 May 2026 23:26:38 GMT  
		Size: 4.5 MB (4514613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb735bcfed960d515b9e02005397a7921ccc8fe4f6ee16ec1cb2304cf32d7e0d`  
		Last Modified: Tue, 19 May 2026 23:26:38 GMT  
		Size: 6.9 KB (6897 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:c24d3c5445396b62c71e20432bcdf2487248369848ef1ee456aa5dac4d286fb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74362602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84497b809dce4baeaca5766b6cc6cabad5dd9e2449ea0e8531f5dcc4a0e799b3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:24:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8bf11fb6e89cfb8d682f511fb7d1b795e747af9c12a192f45f6e50ae7ca54f50`  
		Last Modified: Tue, 19 May 2026 22:36:20 GMT  
		Size: 49.5 MB (49483120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db105b3a1c2456422c428304ae93436fac4214751cb65053af119fa6d81d85dd`  
		Last Modified: Tue, 19 May 2026 23:24:59 GMT  
		Size: 24.9 MB (24879482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:460611f12778dad7692789ce01b1bc4c66c9b49d1903b6cd90a0491fa2a1629f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4518266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9cdada86d170b7a562af493d0db4816850f723b0e3ad74b8217573c181b513a`

```dockerfile
```

-	Layers:
	-	`sha256:aa8241ecb7a3195d94c2123dd67d94a60f959c2be0c33782b793ffd85a62855f`  
		Last Modified: Tue, 19 May 2026 23:24:58 GMT  
		Size: 4.5 MB (4511471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9aea4e11bf76f67c9de46f870c8d5970b67ff0b124384b6688bc3d91291bba04`  
		Last Modified: Tue, 19 May 2026 23:24:58 GMT  
		Size: 6.8 KB (6795 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:d1083d84294664d468a7d24cfd1063cc06e0d22da9fd64c84e9fa0856638452a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72398198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be838167bc6d428682f28fc8a6bf3af9c9bbe15b36bbff3ad400cfbb0915cce1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1777939200'
# Sat, 09 May 2026 06:28:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:08baa8fe1f531703c14c631b772a987ffc44ae832951ae77c2cf756cd9309b97`  
		Last Modified: Fri, 08 May 2026 18:19:35 GMT  
		Size: 48.8 MB (48782513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef35895719420bc7ff8be1345d21e6969bcbf53abcec5b59c476a0fa55636de`  
		Last Modified: Sat, 09 May 2026 06:28:59 GMT  
		Size: 23.6 MB (23615685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8be62c97b6ae9ba0a7f00c4344c6d72092222854d5c7e7d3987aa78f8c16b131
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 KB (6650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d0ef73f63c869e67f9d942c2c627936cb89e94de091e00bd96f729c023cedcf`

```dockerfile
```

-	Layers:
	-	`sha256:a68eab60b8a97d65731b2cc7fafa27691170c8011a059debe3633253cdef5b5b`  
		Last Modified: Sat, 09 May 2026 06:28:56 GMT  
		Size: 6.7 KB (6650 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:605f7cad340a1c65b7d8aca4fbf019f8b45600dc3157030c17ecc3e4b6c738c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (78026665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6de3eaf228a602681fe5ae3eadf5c42889ddaa702d01bd8d3abd76fc20d2ea9a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 01:13:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b3943e183051423c3dc79fa53ad6d50fff9621945bbfc636eec039b14ead2b66`  
		Last Modified: Tue, 19 May 2026 22:35:10 GMT  
		Size: 52.3 MB (52340199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f46c910cb3dd366a8b080c77b15459d7465da54412b3570454cddcaf0cdf40`  
		Last Modified: Wed, 20 May 2026 01:13:39 GMT  
		Size: 25.7 MB (25686466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ca9a10b011b986aa72f286cd55b8958c928275c27fe6e0dbc30a0b9de0b9e06a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4525827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c61b79c879fcef29065480968bf2bd03a8cbd401f74a1b7512c1f26dc8ee02b4`

```dockerfile
```

-	Layers:
	-	`sha256:62469d397464b3dd2b1afc5645c86966876fcc9f74c9f1dcade175d7b5b2e635`  
		Last Modified: Wed, 20 May 2026 01:13:39 GMT  
		Size: 4.5 MB (4518978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3562e529e883f7c3ffa6c9dbfffa8153ec67e1a4372978ae8c6d3e0a71605563`  
		Last Modified: Wed, 20 May 2026 01:13:38 GMT  
		Size: 6.8 KB (6849 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:2c89b551701972f7ff2bed472ffc8a3a0a9ec2a4b1b9d1631746b826fa0edcef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71194790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:904805285c438a54cd8842095ba2dce6b0c5a9b85d085f201547dcc9bf80a5d7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:17:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e0fc2c7a6bb12f7a9b333cc117b6ea5fa5cf251c5fa4dd298303beee01028f59`  
		Last Modified: Tue, 19 May 2026 22:35:39 GMT  
		Size: 47.2 MB (47155589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79feab17202415ba0b431eca0e903b1c895e662e755c4c9f1b5678ad8eb605f`  
		Last Modified: Wed, 20 May 2026 00:18:12 GMT  
		Size: 24.0 MB (24039201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:05696af47833f28b0f4526caec26c8624a7becdbf6124195a718ecfd87481b48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4517973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aafa63b9ea84c437329f710184dbc938429377d19e904a6068f4b5f79965799`

```dockerfile
```

-	Layers:
	-	`sha256:7df8ebf48427baef28858b778de343632442a5949bb461e655db5125d29f6cf9`  
		Last Modified: Wed, 20 May 2026 00:18:11 GMT  
		Size: 4.5 MB (4511156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67f1e8df9757a960c6be006c16ec590253c3cb9093f8dc43e02622788deb678b`  
		Last Modified: Wed, 20 May 2026 00:18:11 GMT  
		Size: 6.8 KB (6817 bytes)  
		MIME: application/vnd.in-toto+json
