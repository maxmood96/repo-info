## `buildpack-deps:unstable-curl`

```console
$ docker pull buildpack-deps@sha256:2e93e54a1ce670180e3fb9fc540ad017727bb83aae25cfbef8599a6c5b2f2881
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
$ docker pull buildpack-deps@sha256:8137e324fbff6b11faceb0b1afabbd11c1c7678fc64ce73b0f8148fb187c8cce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75605109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d547671ba8b02b2cf4e39599c8e04b07c20445d6b95abd4d4219712b4acedbe4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1779062400'
# Tue, 19 May 2026 23:23:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:02991db6507c0026c404c68dc35ba4f9c80895d9d7fc4576cc1507337d1b4eb7`  
		Last Modified: Tue, 19 May 2026 22:36:41 GMT  
		Size: 48.7 MB (48712012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaab406cee21a5226773a482e38ac91869a010b6b5a398856bb12cca4e8f5c66`  
		Last Modified: Tue, 19 May 2026 23:23:35 GMT  
		Size: 26.9 MB (26893097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:55814a8a30633d8ae9fbf2878be7c7edc07ed3339ef5ea5f42532e7c5eb99233
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4068610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ba63ad5e871c869cbb5dd35d6782b8a3810fdfbce48baaa6fb18690472d062`

```dockerfile
```

-	Layers:
	-	`sha256:b8d5c5b6b2a31c25fec245c1033e763816c3f62bb5accda7236847e8c51b9f6e`  
		Last Modified: Tue, 19 May 2026 23:23:34 GMT  
		Size: 4.1 MB (4061849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca34d729c701e127725e2e66651426d16144a5940ebe9f4dc85ac4a88b67a02a`  
		Last Modified: Tue, 19 May 2026 23:23:34 GMT  
		Size: 6.8 KB (6761 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:5df6ba36d8c156aa2eb3e12de93defe080adea52437f03ccbab8b0db9f6db12a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70222070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d00a391a33730d0d8e5bbb4953d745a86c042a1e0f9b1a65d97ca50b1a9ae47b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1779062400'
# Wed, 20 May 2026 00:04:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1c98d9ac4796e25c1d81c99407f882de7bda76effb4d3c6a5d937bf755cc2313`  
		Last Modified: Tue, 19 May 2026 22:36:23 GMT  
		Size: 45.6 MB (45618956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af1515c975babc2c0d71d5cf9a3ec0808ae1a576e22e50913d437d07a60ef65f`  
		Last Modified: Wed, 20 May 2026 00:04:13 GMT  
		Size: 24.6 MB (24603114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3bdfc35f79dd5bfa0730a44014dacae9399d3a01ed51b0fe8fe60d77647faefc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4070160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a72b74c5e46288e195813dbce45c26f7e4972fd0f8be0cf772ec6c4d197af245`

```dockerfile
```

-	Layers:
	-	`sha256:a2b3db00d1b06c2eb955d9d486d6f836b6790ccfe08535a08bc448cc880d623e`  
		Last Modified: Wed, 20 May 2026 00:04:11 GMT  
		Size: 4.1 MB (4063336 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f61cd2d46fae31cdb34c4a8164d5fc735305d8cb08339a9804ec83718251d8d`  
		Last Modified: Wed, 20 May 2026 00:04:11 GMT  
		Size: 6.8 KB (6824 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:05f85f590cefaa71bcc1d77db419ce526b872aecf6321edc218a809bb972121c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74908347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08662d4407120e4b69810c8e27a9fee5b8bd01492f6b7863760950e1a7f938b5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1779062400'
# Tue, 19 May 2026 23:26:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c2bc0682b6790aa6b6a3a5a7933e32ea4a35d72d531a3c53509cd76aae83fc88`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 48.7 MB (48737609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab26ead8a9a9779bd1e4fbb72a954ed83ffbb2d9d0e5d585eb545c5b6270c442`  
		Last Modified: Tue, 19 May 2026 23:27:06 GMT  
		Size: 26.2 MB (26170738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9a270b5858436e13e50d74c54b5e3f611f43ff52fa744565a9d5b09f48bc7a74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4074048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d6762f569fb28b8e14246b477d67e2c960e9ed55faec2aece7a06426da14259`

```dockerfile
```

-	Layers:
	-	`sha256:2dcb5be9dfadc745b581962a164e2b04b6b468568b7e42b81547a36acdcfb513`  
		Last Modified: Tue, 19 May 2026 23:27:05 GMT  
		Size: 4.1 MB (4067208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31ce976dca19364e23722177494b4c555493bba1a8315a814a99029dffc66ba7`  
		Last Modified: Tue, 19 May 2026 23:27:05 GMT  
		Size: 6.8 KB (6840 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:0409263217e9886083e2565b487f9054a507dd3ebbb92a7b62ab76828813afae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.2 MB (78225483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a439fea09a07816f794ae94ab1035c3b21f3bc4565309d4996d0489ac979ce7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1779062400'
# Tue, 19 May 2026 23:25:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:506409f9b5466021b987fde6d84a8bc529520e50798929836cef94e3223d354c`  
		Last Modified: Tue, 19 May 2026 22:37:32 GMT  
		Size: 50.0 MB (50016004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1f3d5431169cdd29adb39f5cf26f13e071f7217f28223b49e250857b02be6d`  
		Last Modified: Tue, 19 May 2026 23:25:28 GMT  
		Size: 28.2 MB (28209479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:229793405d66a94c04b0584ed3cba918cb7570659966b449baebd77384600dc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4065698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d580ef5fb7b82ee065179410a4b791e3b5cc55ff1af362da54810c6725ed142`

```dockerfile
```

-	Layers:
	-	`sha256:7822bd9cdb000d91530ca710caed45c90e91f6f6b3c8c455ff8718276b865e6f`  
		Last Modified: Tue, 19 May 2026 23:25:27 GMT  
		Size: 4.1 MB (4058959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a996f61c39d11b423719c2cbaf86ae9da2174e08ab80dd339066ea0bfe49d92`  
		Last Modified: Tue, 19 May 2026 23:25:27 GMT  
		Size: 6.7 KB (6739 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:57bd51c546bfc13f4e79649f65ccd2a1038c4afbf9572c121e8353f94ce8e299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83331652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61c9655743205644a3453c19fc8cdaa0109b277f00de3316e525126a3885a532`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1779062400'
# Wed, 20 May 2026 01:14:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0bda88a8fa865607f7a3bfe01b25fa99681c2572077bbfaf6b7e16e1f51b5b50`  
		Last Modified: Tue, 19 May 2026 22:36:39 GMT  
		Size: 54.0 MB (54046122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ac92e3c123ea205d76f5d82b79747aea7ae5197399f942393a1c3ea0ec0034`  
		Last Modified: Wed, 20 May 2026 01:14:34 GMT  
		Size: 29.3 MB (29285530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7870940223067223dd0be75342a0ff8999dab849d96e90f167d39350927d787b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4072486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16eeec580f689fb4209abd37b3f1f9fa9e59e348999d771c661661d103aa1f2e`

```dockerfile
```

-	Layers:
	-	`sha256:a04a81230acd06b8d54bc9e45c2bdf4bfcdf0064da02deaec5ddc203e4ba8a9c`  
		Last Modified: Wed, 20 May 2026 01:14:33 GMT  
		Size: 4.1 MB (4065693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99e253c2552d29f76e0692737dae4d9a8120f5ab2b79ce6e59cfb0921023e68f`  
		Last Modified: Wed, 20 May 2026 01:14:32 GMT  
		Size: 6.8 KB (6793 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:0c00682c6ff2598f9f32b8f879ca65894d2c43492b2bde6eedc90b7859d4fe60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73292007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:500a21f01fd577386280d234e1ab10db0b0f5be95935ec05624201d0f7d69779`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1777939200'
# Mon, 11 May 2026 00:52:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:291921d355da34dfbce324263312328392c6a6c78ee971f9b4d7d37f1527cd2e`  
		Last Modified: Fri, 08 May 2026 20:26:01 GMT  
		Size: 46.8 MB (46838649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340855859b1344ded89a6e027caa6be811a60e26a4f08013b27235c463879b0e`  
		Last Modified: Mon, 11 May 2026 00:53:36 GMT  
		Size: 26.5 MB (26453358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3a416daaacc1722697125455fdb52c0c4be2fc7203b61ab6fa520bab5a09dfff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4066457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c12a27be6bb0922620a9513ea0cbf5d5584969f53252b2b8c203f82e83bc067`

```dockerfile
```

-	Layers:
	-	`sha256:8bf8e8999479568e023e249a98ff58774e7faad36b273162f2cbdb341cbe0d35`  
		Last Modified: Mon, 11 May 2026 00:53:33 GMT  
		Size: 4.1 MB (4059664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:089157629e8a35d8b0e8d79870e867a180d5be43fb8ca0842d8b4e58ea078127`  
		Last Modified: Mon, 11 May 2026 00:53:32 GMT  
		Size: 6.8 KB (6793 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f356f8b31e613906746839737dae8f975d2f3e56dd71363ca1517afba930c1fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75145068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d63b1df2844066cca05fb03b9c67637b3e3cbddb4852740ec9291d5aa63b463`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1779062400'
# Wed, 20 May 2026 00:18:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b2de0004fb71a1e4abdd27d0619b3567a865a43b4039f4f3ca7e11b6e7bf8ca5`  
		Last Modified: Tue, 19 May 2026 22:36:09 GMT  
		Size: 48.5 MB (48454253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:558e98e58fdd0e7e9d312d1df7e45d14fcbde914744efb8b87cc091a75f459ef`  
		Last Modified: Wed, 20 May 2026 00:18:56 GMT  
		Size: 26.7 MB (26690815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fef33a60fbbea1d1168df19d074fc93db1ac613b02972c4b2f25072302fbdc11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4070022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebf9942fb1fd905ca42251453cbb8cd5426d8be4897e3f0ca9e461105bc6c583`

```dockerfile
```

-	Layers:
	-	`sha256:70882327a02350ed47bbb23951fa1d854cd48588ec75ffecd5437268c83118d6`  
		Last Modified: Wed, 20 May 2026 00:18:56 GMT  
		Size: 4.1 MB (4063261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d88594689e86f4926dcf852f68a8abdb170c20a08e48a08299f6d229a3b0c1c`  
		Last Modified: Wed, 20 May 2026 00:18:56 GMT  
		Size: 6.8 KB (6761 bytes)  
		MIME: application/vnd.in-toto+json
