## `buildpack-deps:sid-curl`

```console
$ docker pull buildpack-deps@sha256:eeded0881bc4c279304096171220e8c5a60c9aab51068df33e5946749ed9e482
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

### `buildpack-deps:sid-curl` - linux; amd64

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

### `buildpack-deps:sid-curl` - unknown; unknown

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

### `buildpack-deps:sid-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d926c02fec9b208e3b2f95501de1f9b92eebd5a318dfc00f71eda35057175c45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70215223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab45a2e3f95c5d1a3d1cc90f13dea5b09e1a15618598930aa3758ac9d64714e5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1777939200'
# Fri, 08 May 2026 19:44:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:79db944cb324910e68326e7a22d4bc47bd01eb269d35b1d153975be52958d92f`  
		Last Modified: Fri, 08 May 2026 18:37:35 GMT  
		Size: 45.6 MB (45609975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ca5da1f5f4fb120cd7b2b40034ee2f9bf3ebf8737773b984403a970bf3e2fd`  
		Last Modified: Fri, 08 May 2026 19:45:01 GMT  
		Size: 24.6 MB (24605248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4e6b023584652bb7d2d77e5ad4c757a738d65a6a4cfd7e1369450056ae9ade03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4076271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4006636d2a1906810dd86e93d4ce884c7a6e94a6d37dff30ab7686b0872c0dfd`

```dockerfile
```

-	Layers:
	-	`sha256:d461c6361ff964a33a8b4b4655b4b485535a0ed3ab414340520743ef1d7c04e1`  
		Last Modified: Fri, 08 May 2026 19:45:01 GMT  
		Size: 4.1 MB (4069446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b04c6e96bb702751bea2d891b71df4a5f71d551cc56d30eea6265e3aee4d428a`  
		Last Modified: Fri, 08 May 2026 19:45:00 GMT  
		Size: 6.8 KB (6825 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; arm64 variant v8

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

### `buildpack-deps:sid-curl` - unknown; unknown

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

### `buildpack-deps:sid-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:737ae0f7cc4d7cd73f5fa85f443266e2585961bf1cc38b771a334981efe92d2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.2 MB (78216277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea8e86c5486cea9dc75613259b442618a113aa15f6258a0ec9e9567a026c110f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1777939200'
# Fri, 08 May 2026 19:44:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:673cf326009083501c3fabdd17567c937b894deb57d94461178ef18820adb917`  
		Last Modified: Fri, 08 May 2026 18:32:00 GMT  
		Size: 50.0 MB (50006715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e321fedc955b961c2c658a44d5ca3cbf39d67286d1387087c4563c14de6beaf2`  
		Last Modified: Fri, 08 May 2026 19:44:11 GMT  
		Size: 28.2 MB (28209562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0fadf9a19dbef48c9fef15c860f4aeabf316e2e14fcff00bbd9fbf2a020051ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4071801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afa0fa1b5352b762844d63347591375038b576343aa2151f609bc1b0fea48a34`

```dockerfile
```

-	Layers:
	-	`sha256:d91b8ee3f27825016e498ec85bb9797527d62f1127dc7b0e7f68fe7035e2034b`  
		Last Modified: Fri, 08 May 2026 19:44:10 GMT  
		Size: 4.1 MB (4065062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2509f9891fc4dceb2c88fff83dfad790637af9ffd5669415f19a740d7a0e1fbd`  
		Last Modified: Fri, 08 May 2026 19:44:10 GMT  
		Size: 6.7 KB (6739 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:160aa9cf692e522e9ae0589f5c44af8152479a9e9ef105e4fedb864cdef3e47e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83314825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe7c93d89e6542fa81d493336b0afa72d894c854e5ac15ddfea3293a8131ea0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1777939200'
# Fri, 08 May 2026 22:31:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9f402971e72fa142c9d15dd5eaca638787cb5c2e5a412bb3f2a7c4f896ed18ae`  
		Last Modified: Fri, 08 May 2026 19:45:34 GMT  
		Size: 54.0 MB (54028078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c14bf1fa31e28d06ce5dc3e4b127ed62c78c28290930f8041edab4719b7e2e73`  
		Last Modified: Fri, 08 May 2026 22:31:40 GMT  
		Size: 29.3 MB (29286747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:955600b26b12dcd06dff05cdbc4f20996def3b57c2861310473e500256cea7d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4078610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d49027fb10f9e8b4fce700431b4b01046dbb52e09ea739ff4259af058924473a`

```dockerfile
```

-	Layers:
	-	`sha256:fb4e78f905f682b850e23d193e756e6b2ea412f731d640d93cc92bfb7c77c340`  
		Last Modified: Fri, 08 May 2026 22:31:40 GMT  
		Size: 4.1 MB (4071817 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b43ee172202585c9151859e3eb4f2acf8e73d204b6317534660a07d1ae31ba57`  
		Last Modified: Fri, 08 May 2026 22:31:39 GMT  
		Size: 6.8 KB (6793 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; riscv64

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

### `buildpack-deps:sid-curl` - unknown; unknown

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

### `buildpack-deps:sid-curl` - linux; s390x

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

### `buildpack-deps:sid-curl` - unknown; unknown

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
