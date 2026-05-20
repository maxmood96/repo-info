## `buildpack-deps:bookworm-scm`

```console
$ docker pull buildpack-deps@sha256:7983eef131af6d34fc22d6a0c954a1fdb591ef2fef4df2d12e6e8a7927354ba7
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

### `buildpack-deps:bookworm-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:8e8660bae78fdc4330c93f51a52fefdc94a1d8efeb475e7a9cc740ba55934433
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.9 MB (136943257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61c4a77e359ef2c8273f3ade3c6ad5a185533965d2b19c8965e1199728b2d19f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:23:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:26:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:a234579dfb0d2a4c7e869bc6c39c06f306aa019f90ec3e79f682671badaeb4f3`  
		Last Modified: Wed, 20 May 2026 00:26:20 GMT  
		Size: 64.4 MB (64404451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cbc37735691eb1eff8733c344fd5ee3f775f0e946629e653e0f6f94ef0cf874a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7973380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eef5bc94113435d4924974166c7563fe9ae06dfecd91ab49f4c61180d1b6137`

```dockerfile
```

-	Layers:
	-	`sha256:404d0865b655a0b394a43aa4c79d69952c3e50eec3d4ebffa2066e57c15b284c`  
		Last Modified: Wed, 20 May 2026 00:26:19 GMT  
		Size: 8.0 MB (7966070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:233eed0e0b99edf13b4bcee0b0617e28434d548662f3be335542625fd7c8d9a2`  
		Last Modified: Wed, 20 May 2026 00:26:18 GMT  
		Size: 7.3 KB (7310 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:b20c84efc0e8c692fe8c4f73e9f62f0b04f88d395b0772f053ec1515ad11b6ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.8 MB (130769954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b941c6929aea5352cf26282bf8db0ea87943f1a12fd3adabe558b8cbf5e8f8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:55:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 01:18:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:52365582c05b81346015516e0bbb5acc02f934e19a6b069d2bed29916f41c87f`  
		Last Modified: Wed, 20 May 2026 01:18:30 GMT  
		Size: 62.0 MB (62022824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:35747053d0b00c3ea903e341993dc1f3d9c204e62da8846eb200140c8fc07a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7975301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5faaf5372da1f5d5eb82088f2a325544908c485bd7ca36cf2532c0191a9e3b6d`

```dockerfile
```

-	Layers:
	-	`sha256:d22d28ba9e2399eb825b554147e433cd7cac794eabe0b92c9da8aa84cc06b5b3`  
		Last Modified: Wed, 20 May 2026 01:18:29 GMT  
		Size: 8.0 MB (7967928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3934241ae5eb4e18d7dec29ebfe477c5c9f1c95b1a4a9d406d96161020c8c3f`  
		Last Modified: Wed, 20 May 2026 01:18:28 GMT  
		Size: 7.4 KB (7373 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d6a75a21d250f27c177585f4d362c4cfc3c8f1ceb326bbe0f46e8e3311173c0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.8 MB (125821105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cea30331c92555bc0b3bb8be88a8f88bd09dd434e5ccaf43558d80b57270f98`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:02:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 01:33:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:c56a54e4354794da97ac9fe5173f689d775d13afa792e8b390e49425c3caa6b5`  
		Last Modified: Wed, 20 May 2026 01:34:11 GMT  
		Size: 59.7 MB (59661818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f42fce38a04236e9efc0b3ed599ced1ec71b037dd6ac6332a6a461fc35789c14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7974721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7af51ca975cf62b2dc8faf14482c1eb634c64c7ccca1d8b61d5a90a07bf37117`

```dockerfile
```

-	Layers:
	-	`sha256:b7ab81bb61b3589eb530f131e3974eb39e78e99f6002c4e588fa9a9c43ebb1a9`  
		Last Modified: Wed, 20 May 2026 01:34:10 GMT  
		Size: 8.0 MB (7967347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e095d4b0155de4346c1467589f7e191f65d35ef93dccabaa51ff6a6d50ee09a`  
		Last Modified: Wed, 20 May 2026 01:34:09 GMT  
		Size: 7.4 KB (7374 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:30e2b6b43cd08377e526ed123c365bdd36967225470f32d753fbea29fc91fe28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136480481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a66c105371d20e57791a549e7860d976bb9fe5400c1731f3621dd89a042432`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:26:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:26:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:35c669ec0346d48159cb837d6257098593cd53e61de677d9c0426474d36e1c5e`  
		Last Modified: Wed, 20 May 2026 00:27:16 GMT  
		Size: 64.5 MB (64487655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:63d2738bc8b46f79faf85ceff912807ae02070dd91d4941cb4ce45b5b2f3b6e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7979853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1fde0c0ff089864299180ac36f6a9cc606cd335d0e957b7dcc3acd20e7c0a98`

```dockerfile
```

-	Layers:
	-	`sha256:edf977c5c5164a2ca4fd96a1c792e9bf7d62deda1c8177946b7d1cc3ecc79878`  
		Last Modified: Wed, 20 May 2026 00:27:14 GMT  
		Size: 8.0 MB (7972463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8624a923fea03a8170bcffd3b6bd5674c5a92abc28bfa056e2fc6f1198612e6b`  
		Last Modified: Wed, 20 May 2026 00:27:14 GMT  
		Size: 7.4 KB (7390 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:67844d5fd368c5156f9e9e03b8cef80db703882cc64a4a490db15387f1c90909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.6 MB (140606467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441fd9d99ace3c56ccdd915fbb78073e259434eb6a69b1a8be96fac02d8e3101`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:24:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 02:44:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:b9e2a05321daf588afd8b06b380f7ea0a3d7c0de2097ec6f355a74453e7ec6af`  
		Last Modified: Wed, 20 May 2026 02:45:13 GMT  
		Size: 66.2 MB (66243865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a2a904385eeb95c4ce89cb07006b69964be87e10b61a3e921d5ebf4a5d04f48e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7969516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:857d5fc4bf9e59df6e41e8cf4ef1555d6483f509478670fc1def9b923460b40c`

```dockerfile
```

-	Layers:
	-	`sha256:27652ee5e492c8cf683cc13c3448160b641ddcbcc031e03e8c60b2c09df5be75`  
		Last Modified: Wed, 20 May 2026 02:45:12 GMT  
		Size: 8.0 MB (7962228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e7952fc59a7245583fb434e7cfbe0429116c277b676e3ae4820346af7d04184`  
		Last Modified: Wed, 20 May 2026 02:45:11 GMT  
		Size: 7.3 KB (7288 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:34b1af792f7fdab6cec21736a3d8933f1c8568e49d1e7d6e827c4643c3f1c931
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.7 MB (135708095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f66953e172c3c2a69fe4ec0900bfca2ecf59ffb485f24e9a71941455872b3230`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1777939200'
# Sat, 09 May 2026 06:28:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 11:38:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:5e6733e62261bdef4b105b9d3a88929418fe62b78559d54a4e8e5768eaa929d6`  
		Last Modified: Sat, 09 May 2026 11:39:51 GMT  
		Size: 63.3 MB (63309897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:07e4a00f5a62d43d7dc0170f5bdc0d120ebb46586f5ea10f9792e59b4b0461f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 KB (7143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2457ecef592e29cb7bd876955dda7412d2a9a264fedd325a318175d3e59ef93`

```dockerfile
```

-	Layers:
	-	`sha256:52bb62aac38be32c158220083efa0f0e0378a1823472be26a3a406df675462d4`  
		Last Modified: Sat, 09 May 2026 11:39:45 GMT  
		Size: 7.1 KB (7143 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:21f827cc13e1e92946de7cf3c243555d5f9cf1c02e013bc7d7682cbaa8e37645
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.9 MB (147862860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1dd0555a9615e9e0fc12a7d10f2074c38b3a5f7dca3cf42a01cf6276b69a66b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 22:30:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 03:26:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:d12437260b341898b5eafdacd454cf094e6357253f008361a2200d2d98887726`  
		Last Modified: Sat, 09 May 2026 03:27:08 GMT  
		Size: 69.8 MB (69846587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7950ea8e0e180a383dfa62ff54849994f83df348406a25d6af0fc33e040c4f61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7981263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9931ee641cbc7a5032f8c519d90a677251a4a7fb594f08282cb2130a37c04f74`

```dockerfile
```

-	Layers:
	-	`sha256:f9f8606a27be84fa8966956c0f8df916600b9a10c79414ba0ab698628cbd8e1e`  
		Last Modified: Sat, 09 May 2026 03:27:06 GMT  
		Size: 8.0 MB (7973921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:248cb891883aa319658608592bcf34f6cb3cd980e05c89f7020c72e7825d1828`  
		Last Modified: Sat, 09 May 2026 03:27:06 GMT  
		Size: 7.3 KB (7342 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:315bf839ee07b03b8053f5ba4ce56ea6891d055b8c507fd2754658991d2e1491
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134693111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92ccb46272d1b96d62c05027ee60e9248115d1415cbe47d9086e20233412d7bf`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:17:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 02:05:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:511ade0407a6db3c4a6853a735563e5fb22577aaaa32942a9458cc0c09942583`  
		Last Modified: Wed, 20 May 2026 02:05:37 GMT  
		Size: 63.5 MB (63498321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:11b4693a9d06972e8a3b3af277ac38cb0e603a963c73f66abb0c8e5a26410a4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7969691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1e7e3275904c5802b9b94a35ede78051067e2d760b087ca436148c2cd38da65`

```dockerfile
```

-	Layers:
	-	`sha256:ce74865a089147db0d599471b7d3e183b40df8c25800a927306b45b1c827491d`  
		Last Modified: Wed, 20 May 2026 02:05:36 GMT  
		Size: 8.0 MB (7962383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e13e594ba26e8edf7b84b17f9554ff886eb7efd94f7876f7f1958879a386195e`  
		Last Modified: Wed, 20 May 2026 02:05:35 GMT  
		Size: 7.3 KB (7308 bytes)  
		MIME: application/vnd.in-toto+json
