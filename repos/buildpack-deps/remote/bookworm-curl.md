## `buildpack-deps:bookworm-curl`

```console
$ docker pull buildpack-deps@sha256:bd8d2f40f799480a1d9fb994929e007a8f2146045051354f64bd3956827f2c72
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
$ docker pull buildpack-deps@sha256:4398849e4d31dde66064c521d81d9eef86947f97f51b98654b58605ba230c1d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72530856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cf9827fcfa82c20888968898168b19da0c07e2bc456e225a8e7d70c75afbbe2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:40:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d055cea50c88c57fc27fcd44845ebabfe5b830ea8a0a621b89d38a2b650b7ff3`  
		Last Modified: Fri, 08 May 2026 19:40:29 GMT  
		Size: 24.0 MB (24042180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:898964d505c2c555bea0de77c980bbb14ae3f71c0538e341faefe4e71606b9ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4521151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1f3eeb3158fbfada8ac82188e95ab2c01c3556714ac03b16176c3b8394f518c`

```dockerfile
```

-	Layers:
	-	`sha256:63de7da5adf980228b85c6bf0f1cd601ce3b13636b934eda6f34360ee6328016`  
		Last Modified: Fri, 08 May 2026 19:40:29 GMT  
		Size: 4.5 MB (4514334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71e3d6b0cd2779ed9037ee511299d50c0a4b76d4219f51b5e1d4ae986efd8e25`  
		Last Modified: Fri, 08 May 2026 19:40:28 GMT  
		Size: 6.8 KB (6817 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; arm variant v5

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

### `buildpack-deps:bookworm-curl` - unknown; unknown

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

### `buildpack-deps:bookworm-curl` - linux; arm variant v7

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

### `buildpack-deps:bookworm-curl` - unknown; unknown

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

### `buildpack-deps:bookworm-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:65a01ac71df874de734395caf1ed84560884dccf6d13922133f22c7e00e39b70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71982507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90242a192312af09a4141db9817ed4990b69d8a3b9074203f730ac46f19b997d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:42:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8eda28c6ece628fdff982fd6c7c1cd1f5eeccc51cfd0a3ee9155b2ccbdcc68a3`  
		Last Modified: Fri, 08 May 2026 18:24:51 GMT  
		Size: 48.4 MB (48373150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f56578c9577bd69a05b2319baacd770a986ae61a8568047ddd91db1a1893b4`  
		Last Modified: Fri, 08 May 2026 19:42:30 GMT  
		Size: 23.6 MB (23609357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:86a101a77c4549a60366efb42ff9575ed7f2873607d267e49b770c7d2ee37684
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4521492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d60ad0d7cce4d7cbd1533a7281e6d172e20a0138cb88428c942f7057e422e954`

```dockerfile
```

-	Layers:
	-	`sha256:aa72194d626c00a07438f8e8cdef39ea13d7e17c5506e9eb0e85dfd50203c6ea`  
		Last Modified: Fri, 08 May 2026 19:42:29 GMT  
		Size: 4.5 MB (4514595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:358edf62aa24a344b295fe51d05f6eb3e6e3249a31a19199b5ca805ef8db7ea7`  
		Last Modified: Fri, 08 May 2026 19:42:29 GMT  
		Size: 6.9 KB (6897 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; 386

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

### `buildpack-deps:bookworm-curl` - unknown; unknown

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

### `buildpack-deps:bookworm-curl` - unknown; unknown

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

### `buildpack-deps:bookworm-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:db3021f8e528f01a92a53b5a925c7a3945bd3705fd010dc9b61c5a511c9af9f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71184444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61c7c2e7ca833ddbe52f6e3d2ec87c49b370f8c3ca36cf5a2ac6a3c23dab1938`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:52:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:124dbe049873037f973f01d877ec004bf4cd3ce5723d0b8f2067c58ad98137d6`  
		Last Modified: Fri, 08 May 2026 18:27:29 GMT  
		Size: 47.1 MB (47148023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ff8edb12d0e4a9c32ee4c3e2a16590b1236e70a297fedfff3debbb7297bb6e`  
		Last Modified: Fri, 08 May 2026 20:52:47 GMT  
		Size: 24.0 MB (24036421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b82238b9570cb20c8d9a483573f05f54eca3b888d02457d2ec77ab3980fe5242
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4517955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87d923ac062bcf53fd53a49c4036202852f8f3a1ac8e2479e1fe314b774bcf82`

```dockerfile
```

-	Layers:
	-	`sha256:e1aa2d2685e405350f1e2a0734fb97db6e9eb4927b3f3c60fd458ac6944509e6`  
		Last Modified: Fri, 08 May 2026 20:52:46 GMT  
		Size: 4.5 MB (4511138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e36f63c88bc096ec4b3e8dc20e6963ebe6f1d89d2524f62d2893d2ca4b127f4`  
		Last Modified: Fri, 08 May 2026 20:52:46 GMT  
		Size: 6.8 KB (6817 bytes)  
		MIME: application/vnd.in-toto+json
