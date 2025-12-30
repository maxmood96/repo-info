## `buildpack-deps:unstable-curl`

```console
$ docker pull buildpack-deps@sha256:29f37e89dc95faa0c0e573faf6809513a67577aee80db9a64bd540a16b603962
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
$ docker pull buildpack-deps@sha256:757bf559162165b8395191cba8716a6e0b5b3df1cd0768ffba5a6cca44c8ced2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (69988556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5188b134377d4b648e7f3d174be6253346d61bd9aa07ec00fe81b6c509d75d4d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1766966400'
# Tue, 30 Dec 2025 00:35:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:fa37dcda97874915e8cdcc90ad670632c868d75ea88f3d100f667fda60d8b657`  
		Last Modified: Mon, 29 Dec 2025 22:27:31 GMT  
		Size: 45.1 MB (45112498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e4476f3007fecd22f80f4b20b480cc2969ce90429f8c85967f8e864a1ea4ea7`  
		Last Modified: Tue, 30 Dec 2025 00:35:29 GMT  
		Size: 24.9 MB (24876058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5a3683577060ff55dbbe7084c7b0780b630875e7be81b97531155d5f21daddcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4119150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f38573a99a69f4e444194a7ed6a896566d44a75c23cf0677fb4051af955f5f4`

```dockerfile
```

-	Layers:
	-	`sha256:8fac869a6ebf78f3e661460e9a01a2e8c76aa61e26a92e3c554076c12c38087d`  
		Last Modified: Tue, 30 Dec 2025 05:23:08 GMT  
		Size: 4.1 MB (4112325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca5a12760c1be5244253ef7581deaabeb1bc9850b45328c4772fb52383370e97`  
		Last Modified: Tue, 30 Dec 2025 05:23:09 GMT  
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
$ docker pull buildpack-deps@sha256:9b844e19e36eb49eed5fbc10584b4a63e393f1950610666aac563e8e48e3c1d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.3 MB (78346959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7062997ddb64c1e251cfa853d784889ea775a4e66206cb9a90eae259b03a9780`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1766966400'
# Mon, 29 Dec 2025 23:47:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f17a69092f61f8d721afcb2893fe3fd9f89bff73ba6442fc317604ef6ed50dce`  
		Last Modified: Mon, 29 Dec 2025 22:26:26 GMT  
		Size: 49.9 MB (49939146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217ad4932c84f70ed9491cf091cd8265fbcd5562d33475dc1380251ed82c8c60`  
		Last Modified: Mon, 29 Dec 2025 23:47:38 GMT  
		Size: 28.4 MB (28407813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7b394405b25389f4ba2ed4be515776ece02211bd061f86f47b45a34aae658e84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4114682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1af40efb0aaf93dd0dd235db6b9830e1608811fec7b2e18dd4da1371e596e966`

```dockerfile
```

-	Layers:
	-	`sha256:4c7282d73dfabdae772d4066e57863afb62ccb17ea4de97c487efbc597f551ad`  
		Last Modified: Tue, 30 Dec 2025 05:23:16 GMT  
		Size: 4.1 MB (4107943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:300c3c446d747cc82c94da57e602fd42d00a4110868efa8560f36dfd1480de26`  
		Last Modified: Tue, 30 Dec 2025 05:23:17 GMT  
		Size: 6.7 KB (6739 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:5981431738267961045a18683190cd44a1b312503b7c7269865fcfb69f0ee2e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.4 MB (82370131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ca09df6c9310d21d44dffee2f8a8990199ad1e014a4f2471f76825cd4b2751a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1766966400'
# Tue, 30 Dec 2025 17:38:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4751b9b2bc723252279cfc4495d1386aada5bcd65548da744f319db317b21560`  
		Last Modified: Tue, 30 Dec 2025 15:09:27 GMT  
		Size: 53.5 MB (53504917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2461812a9f73d501a89daf3b185dd9b6d6fb2e0eebe88b30b17f3f49a5419e7a`  
		Last Modified: Tue, 30 Dec 2025 17:38:54 GMT  
		Size: 28.9 MB (28865214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e4cb12744cfd7f558bcb298beeb5683b36b59489e5c0784fce8458b819bcc5af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4121469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ec386fe236a300607d3e63cadf658f7437c969c187c76cea16f0218dd58a77b`

```dockerfile
```

-	Layers:
	-	`sha256:1cc590d380a93c39448dcb0222b258e7000654c6523afe464ce609d9342d0988`  
		Last Modified: Tue, 30 Dec 2025 20:20:50 GMT  
		Size: 4.1 MB (4114676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b41be2dfa7471cb69b89908680c19959a57416c39cc0578eb7c000e0e20886fe`  
		Last Modified: Tue, 30 Dec 2025 20:20:50 GMT  
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
$ docker pull buildpack-deps@sha256:a7990240a1f43095e5aa4c5ef170ee5502880f4841c53f7fddb66e8f93474340
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76631997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f77d94d8e937ced250233ea6b749c888842227144ab709525d6b2ea72a537ef`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1766966400'
# Tue, 30 Dec 2025 04:13:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d1672feb37bf4d7307a6feb7cf62c56febe8495830b9f965806ad0a97fe6efac`  
		Last Modified: Tue, 30 Dec 2025 03:26:29 GMT  
		Size: 48.4 MB (48375355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d244417eb312e7e292025b53816a5625d309f746b46cf7d1aa0e277e78d585a2`  
		Last Modified: Tue, 30 Dec 2025 04:13:56 GMT  
		Size: 28.3 MB (28256642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a6451f3fd4e89798dfe16d3419a7ad2afe7bfe3d494a062fa672d138d180c1b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4118999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3abf6de4befe5bdc858c451e1a61c1f7b84e3103cc15c399158c35fcb15d036`

```dockerfile
```

-	Layers:
	-	`sha256:3824da6bf84ddbf8915e71f59abb2251dc2d69278198eb85e6e6996d49ef1e00`  
		Last Modified: Tue, 30 Dec 2025 05:23:26 GMT  
		Size: 4.1 MB (4112238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4503894c39d6664efb08c1d77c39c6d5318f9d51a93ebc94836b392f10791087`  
		Last Modified: Tue, 30 Dec 2025 05:23:27 GMT  
		Size: 6.8 KB (6761 bytes)  
		MIME: application/vnd.in-toto+json
