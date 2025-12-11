## `buildpack-deps:unstable-curl`

```console
$ docker pull buildpack-deps@sha256:cf4c91ca05bcb61f82b153efd8c4cb8693487bfb9a68decc005613ce01245426
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
$ docker pull buildpack-deps@sha256:70899c5e1a1563bb456490a4ad97038779b154d88d138e078d9294716a5cf1c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (76014973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ca226d2520497549b2227deb21bbd0a393241f349d511c9dbdc275e9363f7cb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1765152000'
# Mon, 08 Dec 2025 23:07:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:490e982b5e2060f5a5ea7e5f586ff8bb98bb61a953b4473631a9da94fd85fe11`  
		Last Modified: Mon, 08 Dec 2025 22:17:59 GMT  
		Size: 48.8 MB (48817523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff8ebe9a9fefe126b5d099857127577acadfabc1b7d98ce416ca0faff37c513`  
		Last Modified: Mon, 08 Dec 2025 23:07:36 GMT  
		Size: 27.2 MB (27197450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:eb526e709b6218fb7e0a325664b9486c1a7b95f19dfe8014c899ffda88b285a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4119670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f25b9d3f8e653407c2c1e4661ce9ce6b50daa6b961e49f2d9135b733bbb660e`

```dockerfile
```

-	Layers:
	-	`sha256:07f78dcee19ad97caf042f4317c6f668c99a68a69aa1228fcb70ea039ca15dff`  
		Last Modified: Tue, 09 Dec 2025 02:23:26 GMT  
		Size: 4.1 MB (4112909 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9eefceb76d525861787f750778826355ad72864bdca7f80ab02e102c34b23e0b`  
		Last Modified: Tue, 09 Dec 2025 02:23:27 GMT  
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
$ docker pull buildpack-deps@sha256:98ef71acd46432f62c19eaafe8fece401a60ac6a555e0434124ce381bc8507af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75336647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32fb9d9b0e5b2f46e83cdd28ee4fc1633f61f5ba3d26b7e41885bb42a83b48a8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1765152000'
# Mon, 08 Dec 2025 23:10:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2e5b290b66ba04e2259d84d677cc1c79191dcc391b2b9af44fa26a4735123220`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 48.8 MB (48838607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e861ca4e0892270da154f93f8077287d4c0bd0913eed59fe54c6514a5d7f1c`  
		Last Modified: Mon, 08 Dec 2025 23:11:15 GMT  
		Size: 26.5 MB (26498040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d96f6bf1e45f81cb84021d996deb93b7b68ec2a6ecf4ef0ad0c3c3434bc69539
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4120643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f36c7ea072fdf695f938850f61ce54ba99887b062d7f6108344fd737b11591b2`

```dockerfile
```

-	Layers:
	-	`sha256:31a9ba84d39e2a404d044cd73e72a9b2048b7ac11d01a97d4c4335e25cf716a7`  
		Last Modified: Tue, 09 Dec 2025 02:23:38 GMT  
		Size: 4.1 MB (4113802 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e300d3dc56057fc99d11cbabd9c53040ba1b1243d7a2bd2d8e41c2c9d6cb8e38`  
		Last Modified: Tue, 09 Dec 2025 02:23:39 GMT  
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
