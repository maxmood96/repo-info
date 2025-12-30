## `buildpack-deps:unstable-curl`

```console
$ docker pull buildpack-deps@sha256:2a94a6fb45f9ef6ffd53f2c7a74155ff2e4055439a76bd629a11e0155cce1264
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:unstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:788727afc0aa0024972f4007d5f5b429ba28eb32d1497f4b03e27e2c6a576e73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (75985059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bc0b6b6c120d2b01e51f7c580a4d38c5311f9132839038888af2ba1d6e82371`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1766966400'
# Mon, 29 Dec 2025 23:46:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:36a4985327850927961426bc6fcb1fb8dc1f9b5e7f69f8061c7daf2f4aee58a7`  
		Last Modified: Mon, 29 Dec 2025 22:29:41 GMT  
		Size: 48.8 MB (48821118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff00e9a4f0fade15b203525aaff92a3d5f8f8fc08fd83188ea3896aee735cf9`  
		Last Modified: Mon, 29 Dec 2025 23:46:39 GMT  
		Size: 27.2 MB (27163941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5c2618db211fc6bd348bc8d14b7a28fc9b5d05f5a3ee6c9e1ad0e9f7bd2a5770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4117590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e342d42f8ee0e8136c002911306e21d72b55507737b2a210190dfb8999f7724e`

```dockerfile
```

-	Layers:
	-	`sha256:2312e07e0adfeed611885610aed302795deb0cd06dcae45e108b3f6a111b62af`  
		Last Modified: Tue, 30 Dec 2025 02:21:56 GMT  
		Size: 4.1 MB (4110829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b54876f09adf69bb5690f607d815e3d7fa0cc72566b4fa2671e66b515292975f`  
		Last Modified: Tue, 30 Dec 2025 02:21:57 GMT  
		Size: 6.8 KB (6761 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0f45494f72dec15e3e7b05d951b36ddd6c08d3e0d400e729cf6e1b36ca8d8cf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70030117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5db353b6e5f294835a4b8b2032bf3204036154dd76cc49288a6b3bffbe0d75f7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1765152000'
# Tue, 09 Dec 2025 00:06:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:76f9334b2a3a315cfbd527ebf785350ccdf20f285fafcc4cb59b172a12b89d6f`  
		Last Modified: Mon, 08 Dec 2025 22:17:07 GMT  
		Size: 45.1 MB (45118376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a62720547143dbd3a73491454b89436c575e1d06808adc4a4d023be5d9947a`  
		Last Modified: Tue, 09 Dec 2025 00:07:27 GMT  
		Size: 24.9 MB (24911741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8ec9a2bbb333af99b53d91384aff852f82671210763b681bc6ded8a69cd071cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4121230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f2fe887954e1091518af91d07c34f8fc1810b411c3817c41153b5f37c5d1f54`

```dockerfile
```

-	Layers:
	-	`sha256:ec621ae4f6766eb5bdbf8ae841e5c3958a266ccd9bd77cedefd7a54f2f5beb58`  
		Last Modified: Tue, 09 Dec 2025 02:23:33 GMT  
		Size: 4.1 MB (4114405 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70b318128c15b9e2733b4ccec075ffbafd840592aae6b703acd88cb6bdf106c1`  
		Last Modified: Tue, 09 Dec 2025 02:23:34 GMT  
		Size: 6.8 KB (6825 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:27f7e16457e17e8651294c627a82738f899cd193b004d83e72e0d0bfd4b2b92e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75251686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1a724f25d5aff67d532d4d6b80b357627c80cc44799650ef75d97d36cdf1bc1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1766966400'
# Mon, 29 Dec 2025 23:47:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e81a19d37d9900498b0ca8a841e2e3fe3dfde06146f7d10d1e71e1df7a8ae8ab`  
		Last Modified: Mon, 29 Dec 2025 22:29:24 GMT  
		Size: 48.8 MB (48801029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ee77a5614dc66e1139efb80cfe733dbde2b288b1202ba35c49e9a008fab1f1`  
		Last Modified: Mon, 29 Dec 2025 23:47:42 GMT  
		Size: 26.5 MB (26450657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:97737ab380cf4a9dbfa79fd15e642a5a49f265dcb08e430729aedca3646bc696
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4118563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49cc6debe285c224f1ad68277dd03bf10b1cda17542655594bbe1ad42c5c2b1a`

```dockerfile
```

-	Layers:
	-	`sha256:280cd24fdbcf23b605cd600767ebce3020b26c9f6c5438056eedf9cda79c4c62`  
		Last Modified: Tue, 30 Dec 2025 02:22:04 GMT  
		Size: 4.1 MB (4111722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ed031e0537c1de2f9436f7c6aa13764bcb6b6f335945c63502844d6c5c53a61`  
		Last Modified: Tue, 30 Dec 2025 02:22:05 GMT  
		Size: 6.8 KB (6841 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:a558665615d57edecff0a7200dab3f911e54a259ae21856677f41ab70d505056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.4 MB (78378895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fb2c558514bdc315290cbd573d61f7acd9b17d5b0f029fa2e44164d01c543e1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1765152000'
# Mon, 08 Dec 2025 23:14:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:67f7fae0ea3bb931c627a66604e60b0a242047b0c8f9186d188cf96e0133593f`  
		Last Modified: Mon, 08 Dec 2025 22:16:33 GMT  
		Size: 49.9 MB (49947966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab9e94662795a8f26e5463a4bcfcaabfbdeca01c44b799e3fa96524d3ed5ff0a`  
		Last Modified: Mon, 08 Dec 2025 23:14:49 GMT  
		Size: 28.4 MB (28430929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1ce404e0be4733e988f1b3dba36abb81c3531a9aaf6f0859c06616f300ebbd1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4116757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2f7904fe20d5268d1805e80160377bba45ea079098f3a307b601230492a37ae`

```dockerfile
```

-	Layers:
	-	`sha256:649a20afee379b6d5b5b10ee1665f15853dc4e8542e82836c37f7d9ae5856e96`  
		Last Modified: Tue, 09 Dec 2025 02:23:44 GMT  
		Size: 4.1 MB (4110018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77ed27e30d604efef351bbeaaf5cc7d9d204166145245fe2d1b01ad34280ba1c`  
		Last Modified: Tue, 09 Dec 2025 02:23:47 GMT  
		Size: 6.7 KB (6739 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:ab407ce86262bb903a8c39cfafbcae7e9ade77e1d3168fcf54ec1bef806dad4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.4 MB (82379031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6c23035e3724d1373af288fea2407ee9cd98da23275de55542043f28296037e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1765152000'
# Mon, 08 Dec 2025 23:22:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:91f19749139bb2193587558635e0a320b0f29835fa1325bcb8c73b48ad8b72df`  
		Last Modified: Mon, 08 Dec 2025 22:50:49 GMT  
		Size: 53.5 MB (53494424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a82bf53318ee9ff50934cd5a455b97b8549b92db55df72cf410249ca6112c7`  
		Last Modified: Mon, 08 Dec 2025 23:23:07 GMT  
		Size: 28.9 MB (28884607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ed6c73e620ab65be333e696b72607ca0dc65fccaf2bcbf376623111783a88d93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4123559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aa7139b479c35e30590df9d1ad3484db2b5e26b6763728d80b6e171ed4a062b`

```dockerfile
```

-	Layers:
	-	`sha256:7300ab365639eecaa0d787f4edfc94d5c53521184a15da3a4fe4f3fa1b76a019`  
		Last Modified: Tue, 09 Dec 2025 02:23:51 GMT  
		Size: 4.1 MB (4116766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27ff7fce60e79db29b883b8fc488432f5b5a1e8a39d0960f2d65b890fab39861`  
		Last Modified: Tue, 09 Dec 2025 02:23:52 GMT  
		Size: 6.8 KB (6793 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:6461da12a936dd232362aedabd64c97b9229768325b040145e87de683d062879
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73330833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20e10de4184f2e940263049a5cb54c7b337e576dba24d657892fb368896b5cca`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1765152000'
# Thu, 11 Dec 2025 08:35:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:109a9388fb2c93203e12f30aeaef237cc88f26bdfe719e6c75ba4b856571d621`  
		Last Modified: Tue, 09 Dec 2025 01:53:48 GMT  
		Size: 46.9 MB (46917024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8c6713d289f87fadfcb1cc49dc5c1255a2e68dec8f35d177d80c213c8c3d375`  
		Last Modified: Thu, 11 Dec 2025 08:37:29 GMT  
		Size: 26.4 MB (26413809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ecbdec9195cf3ea0526af971e14a10177375840609688ba7ba84c8e8cd8cd061
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4106520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4628e0b9d16bba2aa08dd827cb92f9885fdb7fee56869c240c0c05c0258932ca`

```dockerfile
```

-	Layers:
	-	`sha256:8000e20bf930c8dac8c1d12e6b8057e89200ae673df5379917c6cb5f7cb46f87`  
		Last Modified: Thu, 11 Dec 2025 11:20:50 GMT  
		Size: 4.1 MB (4099727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf328b0be3090b5c062d4b02812a87562a205b7b481e12789df9e4a3e67de5b1`  
		Last Modified: Thu, 11 Dec 2025 11:20:51 GMT  
		Size: 6.8 KB (6793 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:2ff5aab76ba3d99eb137a8f697cb85ad20f3db52178a5b8ade1619c448d41ec0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.7 MB (76715816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aed0ec1e631e64286d98fd3ccd2f0da193258be0867d24e6e09aeabe149386e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1765152000'
# Tue, 09 Dec 2025 00:11:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9a7cba59687143fa1a3bde49b08caedd4592355c94693db34a36ceebea332a04`  
		Last Modified: Mon, 08 Dec 2025 22:15:38 GMT  
		Size: 48.4 MB (48404077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c41c2bc13ca9c32fc8ea3b0ee8862d2350cf32202664571fd15af30f5ab552`  
		Last Modified: Tue, 09 Dec 2025 00:11:46 GMT  
		Size: 28.3 MB (28311739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:48c37f71acbea82cb874daa5201172ddcdcebcddeaab59af58f3e4a036bb2f6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4121079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bbc7df9ee2312d2d7e532c1fba0051b475c0535b1222288f52a34044d204710`

```dockerfile
```

-	Layers:
	-	`sha256:c5f0a43412c58008bb7afb2b32b8b414bdfc170216e20013f0c8c5f339a3e57b`  
		Last Modified: Tue, 09 Dec 2025 02:23:59 GMT  
		Size: 4.1 MB (4114318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:faf4986f6ddf5c77971f1ec3a9a55f62ddd78c850be17f7eb8e8bea006d1e9e6`  
		Last Modified: Tue, 09 Dec 2025 02:24:00 GMT  
		Size: 6.8 KB (6761 bytes)  
		MIME: application/vnd.in-toto+json
