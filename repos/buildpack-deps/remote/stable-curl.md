## `buildpack-deps:stable-curl`

```console
$ docker pull buildpack-deps@sha256:0a2a746163737cfec31943ca15db79301cb17815c016d2a1a85adfcec874ab91
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

### `buildpack-deps:stable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:37086bd1cb0f375ae01a7017df90f10b556c1217cb9826f6d474650a07c98796
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72503880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38299b879606b5771d2dbc7de2f2957ecf832bf6d4b795f023f2308f06b43fc5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:3e6b9d1a95114e19f12262a4e8a59ad1d1a10ca7b82108adcf0605a200294964`  
		Last Modified: Wed, 21 May 2025 22:27:42 GMT  
		Size: 48.5 MB (48488245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37927ed901b1b2608b72796c6881bf645480268eca4ac9a37b9219e050bb4d84`  
		Last Modified: Wed, 21 May 2025 23:20:21 GMT  
		Size: 24.0 MB (24015635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:80acbc92f68e0ce1f3a74ffd4986f920942a85191c540740c08be937f310551d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4390882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:685ae3582fe122270948c00ef6b3844ef35f2ea5079c48117fd11247a55fdcd4`

```dockerfile
```

-	Layers:
	-	`sha256:47675d8bfa3fac3c333ca1afd4cae0d3ede278878c55d21719e5e12999850e82`  
		Last Modified: Wed, 21 May 2025 23:20:21 GMT  
		Size: 4.4 MB (4383718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ab686b173b6ce9915b4481a28311bc0049087db8997c929a7c47d3ccf26495f`  
		Last Modified: Wed, 21 May 2025 23:20:21 GMT  
		Size: 7.2 KB (7164 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:fd0a9191a7eb02b6c3bccbb1b41995236b2eabffc409be8c1d722a3d5e6730d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68716403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70f4cb1b2ed38e032cbecaca3941967d88c0a86095d2bf1bd31ac940c62c04e4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:41b62f0ff831a6d9573670f580122f67e27137902fa02ca0a3faf11fda42603f`  
		Last Modified: Mon, 28 Apr 2025 21:07:39 GMT  
		Size: 46.0 MB (46026796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933aa71bcd4cf4d4ade7e455a6a748ec9d00e74ad6f8b2dfd8f9c9b70593ba3a`  
		Last Modified: Tue, 29 Apr 2025 06:01:08 GMT  
		Size: 22.7 MB (22689607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:742876fac13ce544d8882de3eae68884a7d2fd99ff936ecbdcde548ae756534d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4370803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f32db5199791a1f1a7dd25d001bf795a8fceedbc17a2a7d8656286e2fbb0130`

```dockerfile
```

-	Layers:
	-	`sha256:f4f25b9a4c3bdd9e99998078c4774634ffc897a49e9e4eacc1d413d039d720fb`  
		Last Modified: Tue, 29 Apr 2025 06:01:07 GMT  
		Size: 4.4 MB (4363571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae4547fa1239e1de22e8bf2c80ce3697efa757edd69d0a9d87fe6d22bbae4050`  
		Last Modified: Tue, 29 Apr 2025 06:01:07 GMT  
		Size: 7.2 KB (7232 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:03be2117ca76816e60376f354f461f9ec41c9ecece12de0e912a17bcd08c750c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.1 MB (66115459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c9541b72dc9e642a552e24400d3aac522bbc6152f2a3b13f307c88796f47e79`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a735d4b4a53e8e11448d15bc50ce4670d54dff52e426cf0510c9b713d3a7ad09`  
		Last Modified: Mon, 28 Apr 2025 21:15:27 GMT  
		Size: 44.2 MB (44197079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b01e6436acd06b177253a4ba25e5179715088c2f493e89c91bbf6fdc41a2034`  
		Last Modified: Tue, 29 Apr 2025 03:37:10 GMT  
		Size: 21.9 MB (21918380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cf56165bd6609a96fa12ae543c98671c91f9f8589ec5da06865f400bcb82b76a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4369584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2b1c3e1c3fe5f913e5c1161a56390668f04f492b3941b7a142d2cdb7762c663`

```dockerfile
```

-	Layers:
	-	`sha256:9afe102eefb178dc1cc2e6d7d567d3f3bf5fd160ff2d64f6980b9aaff8a33cfc`  
		Last Modified: Tue, 29 Apr 2025 03:37:09 GMT  
		Size: 4.4 MB (4362352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e020a108c214db5ff60dbe30b35864032a33a7fe5a5162e50a50a5a3b9e0742`  
		Last Modified: Tue, 29 Apr 2025 03:37:09 GMT  
		Size: 7.2 KB (7232 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:0683af870983173bafa168a23035a91fe23b5bf2c5ccdc71a5a1c55dc3d1d916
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71871906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97df11a7fc7a751747ee399e5d51ab5c0fa0824735a501b4a14f86b4bfe4657c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:de07ba6f486e0ce29760ab32d4381edabbc660a04c493e95eb9a8056925d8955`  
		Last Modified: Mon, 28 Apr 2025 21:20:23 GMT  
		Size: 48.3 MB (48327644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84649bff67ea459549b6f371f7045d9968d6ebf370b815c922a625f3ab065724`  
		Last Modified: Tue, 29 Apr 2025 01:46:47 GMT  
		Size: 23.5 MB (23544262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a586350b4312a080d8aa2fecb652afc0964a4e8290c103034519c139558b2f0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4367584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b01cda863f04fa328fbbd0f9367ed1307f66f97e8729effe1c05b67a4a2e98b`

```dockerfile
```

-	Layers:
	-	`sha256:cfa1777d560a7c0edfecc0cd59ea47c83aed7cd3ca9455f2f96ee5f027b13128`  
		Last Modified: Tue, 29 Apr 2025 01:46:47 GMT  
		Size: 4.4 MB (4360328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efd65370d2e06f01caca66b553116ab9d0ecbdd03bb457a9de071c97de6725d1`  
		Last Modified: Tue, 29 Apr 2025 01:46:47 GMT  
		Size: 7.3 KB (7256 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:450ec8c29e3cd3fb464a5d3474a85c81e300ed8d050140b669f24b369c79facc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74327230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14dfd24c95c8905a9473dcb5dc5e0b357a44096f46459ec0a089a71e8fdea7eb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7bdd0d6ce898fe017a461e5f67ccf41a15f147063ffe1c496fb7e5f75037adfb`  
		Last Modified: Wed, 21 May 2025 22:27:49 GMT  
		Size: 49.5 MB (49471562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296134322e370a0aab10509f2b47d9ce416e7da5a792e7f8badd9284ecbabeb0`  
		Last Modified: Wed, 21 May 2025 23:20:06 GMT  
		Size: 24.9 MB (24855668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:93904a342fbe728e2e210c80bd5566ebb81edf095329b61a3a07b156feb25061
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4387974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:116f43ea8c731e93fdaca29dc317f7147fe78ab5d9da761a0189b1a5d0a1dc8f`

```dockerfile
```

-	Layers:
	-	`sha256:6c1df6a37ce3697feeca9c97964ad962e5c8f6dba298a1b5bda6ed06865ff660`  
		Last Modified: Wed, 21 May 2025 23:20:06 GMT  
		Size: 4.4 MB (4380838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e55f2ab8349ec97052a02ee29306c7f569c27e011d80f53eb26a34e2573915cc`  
		Last Modified: Wed, 21 May 2025 23:20:05 GMT  
		Size: 7.1 KB (7136 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:cb356d116a4a104ca1f758dc5f2feed606eb32efa6462ce92999ca3aa4ded131
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72371172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86d8a493bd40f7ed61fd101abcc6a3eb89861f539415b6f03f5d309605aea27a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fa5acbf36757d3126014bc0e0a159fb5593a1d68ddba5992ef7ac9aa3e7db8dc`  
		Last Modified: Mon, 28 Apr 2025 21:10:59 GMT  
		Size: 48.8 MB (48775438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d3e6811de68483322bf4607ec4cf0620d9d7f95dc19ce670b2ee81bd283341`  
		Last Modified: Tue, 29 Apr 2025 12:43:07 GMT  
		Size: 23.6 MB (23595734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8b81b39dfef5af9dc36de02aa1ed5ac9c4d2aba72eee5fad0298da6a76ea75b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 KB (7006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c17eadc4b49695cb90bb05b3daada4ab3d45ab822df17d67d2b92a001879f047`

```dockerfile
```

-	Layers:
	-	`sha256:a640a82e6746f646005a34771412d8f757bd27fd1a219bcde3ec57528a21d6e0`  
		Last Modified: Tue, 29 Apr 2025 12:43:04 GMT  
		Size: 7.0 KB (7006 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:397e3a744730470f2fc3e64dc07818c78c5eb0e2e055196071cf7436c3222191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (77982242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c8e20244762847dbfa5cfeca6ddd4f8eac6343b4a1a41ce79f0fc7f30e5731a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:33862e890d6c23fba01df0303b503e727dad5c72574fdf8af76d76dc3140d561`  
		Last Modified: Mon, 28 Apr 2025 21:21:34 GMT  
		Size: 52.3 MB (52332129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4617415431bf61f96c81d815cfb6cf010eef7bd0d8a8de24b02c1a7fe8407026`  
		Last Modified: Tue, 29 Apr 2025 07:46:58 GMT  
		Size: 25.7 MB (25650113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5856b90bd67a9f0a17ac7095de7a195af578be87a31978bcb1d52222dac36bf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4371749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:220d9acb963f8af1ddcbd847918d0eb02b3399ece16240a73d837928e0931f6c`

```dockerfile
```

-	Layers:
	-	`sha256:feb2296affa42ce46c4f7a2bed3dddc92edb61703dfbff0010c848279dd7833b`  
		Last Modified: Tue, 29 Apr 2025 07:46:57 GMT  
		Size: 4.4 MB (4364547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd8bd32208839f078b5ccd2fab2ea6e468d5d730d92c36b371355c027188eb50`  
		Last Modified: Tue, 29 Apr 2025 07:46:57 GMT  
		Size: 7.2 KB (7202 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:9f3b41f02ab360de65902e326908ac8a7e5a71789ee102ab377b36e4def63723
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71158698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8504d40974c221d20e9ae117c3e9ee41c2ead70dda2f9e23d33e84b56b52dc9f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:47f9a2c2279c9df9e222a4c8af501e43b0b5e2552eda9597a97162080b8f106b`  
		Last Modified: Wed, 21 May 2025 22:28:14 GMT  
		Size: 47.1 MB (47143842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86a43d043466908a6aee9cc569c707c9cb9b87fe3e55b5a27e7fe7f7f27d73c`  
		Last Modified: Thu, 22 May 2025 01:01:58 GMT  
		Size: 24.0 MB (24014856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5ca0532c045354fc9114cb4fe202274e477bdd9c8fa8f696b3b1237e3c19b166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4390578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce000f6b82d6c43621635313ae3ff9915997b423183bf297d1b2a90921c27c84`

```dockerfile
```

-	Layers:
	-	`sha256:dd82f7d8b79d27e9d4a03982373372d633092b8b7ebc71b8f1d6c27a981a348a`  
		Last Modified: Thu, 22 May 2025 01:01:58 GMT  
		Size: 4.4 MB (4383414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dda9c842d794f54ee63f1dbfa35205fefc38a1fb84dc369ed1847dd004c0db22`  
		Last Modified: Thu, 22 May 2025 01:01:58 GMT  
		Size: 7.2 KB (7164 bytes)  
		MIME: application/vnd.in-toto+json
