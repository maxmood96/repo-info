## `buildpack-deps:resolute-curl`

```console
$ docker pull buildpack-deps@sha256:3ea64a17a31d2c5c3ca1fb7ce5be416aa4b879e2471c995a3d8e047665fe3f09
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:resolute-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:bf8f0870153979e96719bf51666b921d1547ae9f03c6da2ecb72f9d3a1f87c23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63927502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8e17c2240d589cfd882ae294d638e51902839584c6bf481bbc752be876bb981`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Apr 2026 03:43:09 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-472e35e483a575a4515eb13f3fffa1eb/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-472e35e483a575a4515eb13f3fffa1eb/images/.temp_layer.4430.tar --tag 26.04
# Mon, 13 Apr 2026 03:43:09 GMT
RUN umoci config
# Mon, 13 Apr 2026 03:43:09 GMT
RUN umoci config
# Mon, 13 Apr 2026 03:43:09 GMT
RUN umoci config
# Mon, 13 Apr 2026 03:43:09 GMT
RUN umoci config
# Mon, 13 Apr 2026 03:43:09 GMT
RUN umoci config
# Mon, 13 Apr 2026 03:43:09 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-472e35e483a575a4515eb13f3fffa1eb/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-472e35e483a575a4515eb13f3fffa1eb/images/.temp_layer.control_data.4430.tar
# Wed, 15 Apr 2026 20:25:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5f528443f34699bfec0f2308065cd6e3542906dc651e44adcbc224911a068119`  
		Last Modified: Mon, 13 Apr 2026 04:42:47 GMT  
		Size: 41.5 MB (41456182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7db96ef8a1ff29f593a12f085ddc564d16b3924f6213bb6c978b9dbe40b304`  
		Last Modified: Mon, 13 Apr 2026 04:42:50 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c119d0c66c27f7d34953d535ece957fc04cc295f72889f2b773ff2b7ce656f6`  
		Last Modified: Wed, 15 Apr 2026 20:25:13 GMT  
		Size: 22.5 MB (22470928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0ee2481330b94c2f379795b82ec71f3a9f03a1b0ec5441ab1f3fc3fd8863b6e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4360254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8e99ec99431c4cde11072796969c40a2c9e76568c79716b4be6bd23111d464c`

```dockerfile
```

-	Layers:
	-	`sha256:e0588c7a7d3118c5ebd347b32d6ab6ba8b57146bbef7ee840b1fc939de8bdf54`  
		Last Modified: Wed, 15 Apr 2026 20:25:13 GMT  
		Size: 4.4 MB (4353011 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74c3cf196fc3a618d75253395729e6c358f3693c1fbc40fe5aadb49b08d53e33`  
		Last Modified: Wed, 15 Apr 2026 20:25:13 GMT  
		Size: 7.2 KB (7243 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:4c27963181803440f8a20615af092fb7476d382c54f77e9d9a163b21da1b0f98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.6 MB (58641148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4a97855cea4399636a0cb350ee7e115cd0d689c7f36c97c2b86ba649a8e0ca3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Apr 2026 03:44:21 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-472e35e483a575a4515eb13f3fffa1eb/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-472e35e483a575a4515eb13f3fffa1eb/images/.temp_layer.4467.tar --tag 26.04
# Mon, 13 Apr 2026 03:44:22 GMT
RUN umoci config
# Mon, 13 Apr 2026 03:44:22 GMT
RUN umoci config
# Mon, 13 Apr 2026 03:44:22 GMT
RUN umoci config
# Mon, 13 Apr 2026 03:44:22 GMT
RUN umoci config
# Mon, 13 Apr 2026 03:44:22 GMT
RUN umoci config
# Mon, 13 Apr 2026 03:44:22 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-472e35e483a575a4515eb13f3fffa1eb/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-472e35e483a575a4515eb13f3fffa1eb/images/.temp_layer.control_data.4467.tar
# Wed, 15 Apr 2026 20:16:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ad4da938cf0c0570f3f7d460c11d9db8ebf696978ae9b30e56bbbce569cbf516`  
		Last Modified: Mon, 13 Apr 2026 04:43:18 GMT  
		Size: 38.6 MB (38638847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86038324bc4115f9a18bd6bdea151513582b60ca3c9de1a881935f1beab04dcb`  
		Last Modified: Mon, 13 Apr 2026 04:43:20 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29851844ca92a399541c3a7a70f5c076de781b7bf6acd8369d547689815e304`  
		Last Modified: Wed, 15 Apr 2026 20:16:55 GMT  
		Size: 20.0 MB (20001894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a16e097530397cb765677870e6c3055ff3dfc997bf3fbc1a043761b5e1cb4b13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4361820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4594dfaf944a68d90e308a700d8c32a16999c3a1e394519be92503939acca2b7`

```dockerfile
```

-	Layers:
	-	`sha256:c981ebe53f5756588eb6e88158ed02db0fc78835f98b96446101038ee70fef59`  
		Last Modified: Wed, 15 Apr 2026 20:16:55 GMT  
		Size: 4.4 MB (4354513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4651ffddd3ff607b190bae6afdfffa71978544af3dd742dae3b8254668d700ef`  
		Last Modified: Wed, 15 Apr 2026 20:16:55 GMT  
		Size: 7.3 KB (7307 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:86b65aa21b901231e06cbf2fc02569e6e976907b564ccf93bfaaa1c512b1b61b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.0 MB (63046569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:060ab68a55d0081a51cf68ac0cc7ff7050c5511596bc9b91feb308bcaafda2b6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Apr 2026 03:44:27 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-472e35e483a575a4515eb13f3fffa1eb/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-472e35e483a575a4515eb13f3fffa1eb/images/.temp_layer.4512.tar --tag 26.04
# Mon, 13 Apr 2026 03:44:27 GMT
RUN umoci config
# Mon, 13 Apr 2026 03:44:27 GMT
RUN umoci config
# Mon, 13 Apr 2026 03:44:27 GMT
RUN umoci config
# Mon, 13 Apr 2026 03:44:27 GMT
RUN umoci config
# Mon, 13 Apr 2026 03:44:27 GMT
RUN umoci config
# Mon, 13 Apr 2026 03:44:27 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-472e35e483a575a4515eb13f3fffa1eb/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-472e35e483a575a4515eb13f3fffa1eb/images/.temp_layer.control_data.4512.tar
# Wed, 15 Apr 2026 20:24:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:86973008df0f4d84f186cd417b697dd89ad0500783a74fbdf846af4e31defe9d`  
		Last Modified: Mon, 13 Apr 2026 04:42:57 GMT  
		Size: 40.7 MB (40683787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1d2ed58370ae479dbd99563da5d88c6adecad662d756c0dbce31ca40162b95`  
		Last Modified: Mon, 13 Apr 2026 04:43:00 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca9312fd14283f97d0c5f184b060bf26f1bb507d6cfd80927c5d04bbd3cf5d9d`  
		Last Modified: Wed, 15 Apr 2026 20:24:43 GMT  
		Size: 22.4 MB (22362393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3dddf727d1f41059835cc6b7fa5b1a111b8463052b581683cc846dd574258bfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4360591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:845b65946021bb9270a889a8e992b96e5ff62ea4a513a796a8c9bbbfafd136f5`

```dockerfile
```

-	Layers:
	-	`sha256:5bfda7791b7620b48c5d4f20dc89348f5285b205f96369064246aac993477f3a`  
		Last Modified: Wed, 15 Apr 2026 20:24:42 GMT  
		Size: 4.4 MB (4353269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22046fc5cdf7d9b0d60a0652e8e89e107355d7fa0206504c6762a45ef09d48fd`  
		Last Modified: Wed, 15 Apr 2026 20:24:42 GMT  
		Size: 7.3 KB (7322 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:0b7bf00cbcef97e6d9b060b435f929f3c0de8a4f6235f1f9f4ca0bcb630c3be0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.1 MB (72149268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b048ac73b3f355ad844f6bd02ed1479566a5bd8b35ccc1dfcb085361101bfa8b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Apr 2026 03:45:01 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-472e35e483a575a4515eb13f3fffa1eb/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-472e35e483a575a4515eb13f3fffa1eb/images/.temp_layer.4413.tar --tag 26.04
# Mon, 13 Apr 2026 03:45:02 GMT
RUN umoci config
# Mon, 13 Apr 2026 03:45:02 GMT
RUN umoci config
# Mon, 13 Apr 2026 03:45:02 GMT
RUN umoci config
# Mon, 13 Apr 2026 03:45:02 GMT
RUN umoci config
# Mon, 13 Apr 2026 03:45:02 GMT
RUN umoci config
# Mon, 13 Apr 2026 03:45:02 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-472e35e483a575a4515eb13f3fffa1eb/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-472e35e483a575a4515eb13f3fffa1eb/images/.temp_layer.control_data.4413.tar
# Wed, 15 Apr 2026 21:13:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:552e200877d734356a4b71dd58b28d74d2f0e38f185d1b1703554ab98797da01`  
		Last Modified: Mon, 13 Apr 2026 04:43:08 GMT  
		Size: 46.7 MB (46732043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aefc2bbbefec401076a4cd9d45072e7a6665f87cc24af7d6f2e7d604dcccb3f`  
		Last Modified: Mon, 13 Apr 2026 04:43:10 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810d73d543773147ad0b723fe5a6a76ef3789ea37b15c708fa0d15284c3f4266`  
		Last Modified: Wed, 15 Apr 2026 21:13:34 GMT  
		Size: 25.4 MB (25416832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0693b3b9cd2cb5a0c87b2f13cf9b1e2d3715669b78bdeef281f05dc6731d477d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4364109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c73bd650bec39be23a468b637425839ea0d889c76f956494837a323e0a83b6a6`

```dockerfile
```

-	Layers:
	-	`sha256:c113473a6c50323ea2ed3125c1fc32dbd045116e104fd5ab67beb2d2dd6d2fdb`  
		Last Modified: Wed, 15 Apr 2026 21:13:34 GMT  
		Size: 4.4 MB (4356834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed8b92e93944678488b7dc91f2e38de6acfbb1a63dd8d8507dcfe122054fd581`  
		Last Modified: Wed, 15 Apr 2026 21:13:33 GMT  
		Size: 7.3 KB (7275 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:d89b354c8ce92510a9e745a912e641babc9529e445a420ee23b3cffd07704e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.7 MB (63743024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35da834ba68fd9ad8dfe925bbf708e6a6cb052038ae4972360f28fc53e2d5c98`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Apr 2026 03:44:06 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-472e35e483a575a4515eb13f3fffa1eb/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-472e35e483a575a4515eb13f3fffa1eb/images/.temp_layer.4487.tar --tag 26.04
# Mon, 13 Apr 2026 03:44:06 GMT
RUN umoci config
# Mon, 13 Apr 2026 03:44:06 GMT
RUN umoci config
# Mon, 13 Apr 2026 03:44:06 GMT
RUN umoci config
# Mon, 13 Apr 2026 03:44:06 GMT
RUN umoci config
# Mon, 13 Apr 2026 03:44:06 GMT
RUN umoci config
# Mon, 13 Apr 2026 03:44:06 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-472e35e483a575a4515eb13f3fffa1eb/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-472e35e483a575a4515eb13f3fffa1eb/images/.temp_layer.control_data.4487.tar
# Wed, 15 Apr 2026 20:43:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6a7f3c6c466d8b59f9a103cde6bc7628a0057e9d800bfdd5f06ee656d07ed9a7`  
		Last Modified: Mon, 13 Apr 2026 04:43:37 GMT  
		Size: 41.1 MB (41145053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b79f07b4f43f880fa2a19a5b25906c31b8fa10386bda422165111b0fa1f377c5`  
		Last Modified: Mon, 13 Apr 2026 04:43:39 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8ce8e664329b3e5cce2e99d01feecb396d0a720b4aadb5f84e0007779982f2`  
		Last Modified: Wed, 15 Apr 2026 20:44:03 GMT  
		Size: 22.6 MB (22597584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a43661138cb64cddee105568181da94234eb8888c75f9245567c21d183c79bde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4362284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc7caa6c02429c960db1ef87bb704f08a6555181079c2872685dadfb853b0e6`

```dockerfile
```

-	Layers:
	-	`sha256:758841ce30cdb71e5765dd274ffcb322468eef5bbfadf0fefa4b94d551742a05`  
		Last Modified: Wed, 15 Apr 2026 20:44:02 GMT  
		Size: 4.4 MB (4355042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9d3af3748029f055d366784998be356a992e52da095ae20dc53a24cf42106f3`  
		Last Modified: Wed, 15 Apr 2026 20:44:02 GMT  
		Size: 7.2 KB (7242 bytes)  
		MIME: application/vnd.in-toto+json
