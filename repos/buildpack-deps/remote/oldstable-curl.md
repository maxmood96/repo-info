## `buildpack-deps:oldstable-curl`

```console
$ docker pull buildpack-deps@sha256:d5e93ca9e51d94c85c38320224dda2471b21db270753264f9050a8e9fcca90b0
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

### `buildpack-deps:oldstable-curl` - linux; amd64

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

### `buildpack-deps:oldstable-curl` - unknown; unknown

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

### `buildpack-deps:oldstable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:5630fcca33e0684c0951b41258e6f33395e3deecd22add756bcc16b069570e96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68737983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04f51df388ea120e81288e39378ac25c7bf72974aa42927873deba9efcb8aa53`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:57:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ec18a0651074f3ac740b1a061140a88c16cce1b8118aeae02a5868a4ebdd3ef3`  
		Last Modified: Fri, 08 May 2026 18:33:05 GMT  
		Size: 46.0 MB (46021587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6a0421f0b3bd4d0ba350f2693e0eb96a367c792e68487d0d1bd64fd9b90938`  
		Last Modified: Fri, 08 May 2026 20:57:12 GMT  
		Size: 22.7 MB (22716396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2509ed95a9e737e1e55e4b47f9d490221660f0e70557afc7249e02581d9163eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4525031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9af72968e7bb26a523b5a324a01224c90c7fc7bd4dda9932cc5e11be7e73e6d4`

```dockerfile
```

-	Layers:
	-	`sha256:cf972dda08cd8017db314bbddea1fb55f03e7c84e3d9711027aedc99e34cb693`  
		Last Modified: Fri, 08 May 2026 20:57:12 GMT  
		Size: 4.5 MB (4518150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d30e982bd7b00021eb4f77c43e04914ad046eb3be7c532f36aed559041ba175`  
		Last Modified: Fri, 08 May 2026 20:57:11 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:a793907c8684d7515553cab2325f3ba0c347db467d939264df96bdd9fe0e3744
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66154088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b3f8e02e99772793c2ff46790393eb243b71b390e70d52f9d2210e2d19cfee7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:44:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:752ba895535a5b96e621b623e0a11ff696fe28fb2110ab16de49e150423d0a89`  
		Last Modified: Fri, 08 May 2026 18:36:54 GMT  
		Size: 44.2 MB (44207696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0504388ca2bf72a5fec3556b58015e5dce736337a948976b22cd4cce283cb0`  
		Last Modified: Fri, 08 May 2026 19:44:39 GMT  
		Size: 21.9 MB (21946392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a3623ea668f104bbe56ae23492ebdc6797c30df4982733b717b880da2bd8bb6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4523504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eac639d42e9264e3736688bf471895a241f7724d8dd148c1b695959266c82da`

```dockerfile
```

-	Layers:
	-	`sha256:ec5a2d6060f1678fb2c09b88a8279d626cd5c1fec99a56f5745f286fc5f6cd9e`  
		Last Modified: Fri, 08 May 2026 19:44:38 GMT  
		Size: 4.5 MB (4516623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d128a8eaf060ce86644e21721c0ffee54d7fdc700bd57fd19a5add2e08cb344d`  
		Last Modified: Fri, 08 May 2026 19:44:38 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; arm64 variant v8

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

### `buildpack-deps:oldstable-curl` - unknown; unknown

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

### `buildpack-deps:oldstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:129f0964ce3fc4df567579bbe19efd96c0cfb85b670e07cd206b3d54e5ec9664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74353534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dded0424d5fb79ca750d4b8dc0f1c184aa5b4d94ea463bb152afac50f8eaae40`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:43:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e8fda93cd5bc3b53d403a41ac2e9a09760cd4b6b193c50e68ab6c1d07685411e`  
		Last Modified: Fri, 08 May 2026 18:30:42 GMT  
		Size: 49.5 MB (49477798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c4c78b842a600b86f5f6446efc3bd0e383975b503d9d424b2fa6514ef50eb2`  
		Last Modified: Fri, 08 May 2026 19:43:16 GMT  
		Size: 24.9 MB (24875736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9c3e82366acae6edffec21307f2a0a81f4f74aa1cabe0860c2628b53a194ab9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4518247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c38f9ef8a3b70a74f6dba95ef54ea8be75ce2c1ffddd414f6127221b62a75f23`

```dockerfile
```

-	Layers:
	-	`sha256:08bd0c4a72bf140698418a09dae7f9452d5884e9b7723ae6e70b481206245259`  
		Last Modified: Fri, 08 May 2026 19:43:16 GMT  
		Size: 4.5 MB (4511453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b875da942b581c01206d187c23e6fe1050540749d3e097d608f49debeba069b`  
		Last Modified: Fri, 08 May 2026 19:43:16 GMT  
		Size: 6.8 KB (6794 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; mips64le

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

### `buildpack-deps:oldstable-curl` - unknown; unknown

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

### `buildpack-deps:oldstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:24c8cca93477b3952bb9458a0cc577112e4cd10b6857b7b0c6c93475498efc6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (78016273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e77407bfc2faaf0d5e33b8dea5c726dbef7991034a6643ce3d3bbe8ccd94009`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 22:30:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:30ef9f53c997c6c1f1ab8f4cc559b32d9206d169c54ad5a0f0363076708fffef`  
		Last Modified: Fri, 08 May 2026 19:44:07 GMT  
		Size: 52.3 MB (52336787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76bedc371abd17d2a145cc444214f9d4db5b827f6b018dfa08217a285aa62a4`  
		Last Modified: Fri, 08 May 2026 22:30:50 GMT  
		Size: 25.7 MB (25679486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:452ea6a2aa98050f059f30cbae10439c7568a5c260ec55f8b9650e05aad9ec62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4525809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ef3f1d4f85ec95019ac4e261cc11180962b03b54eb7a709339ee7f7f29ffc5f`

```dockerfile
```

-	Layers:
	-	`sha256:cfed99ff6e4b7ab538a6361731f06dcda228b14e2da32c7bf94d9e545fe6a989`  
		Last Modified: Fri, 08 May 2026 22:30:49 GMT  
		Size: 4.5 MB (4518960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb0a97fd4c1fa933e564d8eae305a3106ffcdfced4cc67045a26c2a62deb328f`  
		Last Modified: Fri, 08 May 2026 22:30:49 GMT  
		Size: 6.8 KB (6849 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; s390x

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

### `buildpack-deps:oldstable-curl` - unknown; unknown

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
