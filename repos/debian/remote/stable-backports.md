## `debian:stable-backports`

```console
$ docker pull debian@sha256:cf34644735a345e02df84bd679d933ebf2aa0c80eb932cf392749a3967fca5c2
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `debian:stable-backports` - linux; amd64

```console
$ docker pull debian@sha256:18c965ca44e108cc98a645e0226bcc9dfe2bce2f5a5b6a30f8b8b6de3450f2d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49302540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c910f90ab053fce1add10b59715580baa46bb14c2db28e2c9323f4c6bcbab949`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'stable' '@1777939200'
# Fri, 08 May 2026 19:15:05 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:01b6660c38d77fbf44430ff66bda33a913d792a9f40578e2e2a18e39a6598e6b`  
		Last Modified: Fri, 08 May 2026 18:23:46 GMT  
		Size: 49.3 MB (49302320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f961faa108282b50913dc913d4728d194e4608ee97adc12ed7c402ab0f36d0d`  
		Last Modified: Fri, 08 May 2026 19:15:12 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:4ef2d1e229a02a67c31500178d89764f3a695252bd3a6ae5bda6cd5826e8dde8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3176697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d2e31bf5a459e979d5b12ffb2f23aec83b0af2b615fa098dbcbf1defef24267`

```dockerfile
```

-	Layers:
	-	`sha256:22e6907b797899371ea333d64db7dcc97bbb66c50ca393ba7e0aa3c66fe63cef`  
		Last Modified: Fri, 08 May 2026 19:15:12 GMT  
		Size: 3.2 MB (3170913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3001be807b0c6356399193100d21ecdb92336e71ddab7baea58ee54420b4e9bc`  
		Last Modified: Fri, 08 May 2026 19:15:12 GMT  
		Size: 5.8 KB (5784 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:54f19a0bede4d91f55cbd6a95fcfe99e445a94beec8572050b9afdfe400f1c35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 MB (47466512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73c73a1b5bd6ef05066ea321e64cd57041a9859b06235e03d8efd0694620219a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'stable' '@1777939200'
# Fri, 08 May 2026 20:25:41 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:9120ce8917e68c0f6ebbb3d27c1c84bf13510cf75e055e9976716bfb14d95e5e`  
		Last Modified: Fri, 08 May 2026 18:33:35 GMT  
		Size: 47.5 MB (47466292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:780b19d2a5c3baf38bce36aaafd89d1bf06e9a7eb6f8f3dc44a5a330c1ab50cc`  
		Last Modified: Fri, 08 May 2026 20:25:47 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:45185c11efffb62dd82558f148d4c8839848c5b295294f994dd2700d0a080bad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3179690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45075d81c41e53bb06e274c5fb00cee7787aa977434e036c19896706e7935922`

```dockerfile
```

-	Layers:
	-	`sha256:88de3fd500c2f54fd87e50c16fa4a71be0edb411cebb8068080a47722c1a2a8d`  
		Last Modified: Fri, 08 May 2026 20:25:48 GMT  
		Size: 3.2 MB (3173850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95ea5685483f737939fafe947f2957de51f810db4f1d124abf6597b46e300b5c`  
		Last Modified: Fri, 08 May 2026 20:25:48 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:1c8743686014e3142948d7b73f586e57584ba72be317aa1e32a353e7ab98d98d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45738648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2f9b50a525fd057a1c84e5b63b6770934d00f21f39a93785575a328c5dce5cd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'stable' '@1777939200'
# Fri, 08 May 2026 19:15:04 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:2f3eb0a7a2e97a23d5ec0ee52447565fdd68a8a063e90245ac86f420b6ec0076`  
		Last Modified: Fri, 08 May 2026 18:37:41 GMT  
		Size: 45.7 MB (45738425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8ed1df9e2b7c6f3c4a8774be9caac3ca827bb8937e624065b2ab4be7c13379`  
		Last Modified: Fri, 08 May 2026 19:15:11 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:c45dc90f7b927dfb378c2231cc63b46acc4bed6f2261e10821cb8857387b61d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90428345d01a1365fa5ee8523b49368134e1a85c1f171a17ba1f838597f9ec33`

```dockerfile
```

-	Layers:
	-	`sha256:154fb8d09a67a48d5bda695beecc90dcd4f730091d66a5a797189f48fb9b5a46`  
		Last Modified: Fri, 08 May 2026 19:15:11 GMT  
		Size: 3.2 MB (3172287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b554564fb37173252adf6114fa84c730afc0169f322903773148b2100b4baab`  
		Last Modified: Fri, 08 May 2026 19:15:11 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:6baae208077f9622acfb38f4cf11a881890703700486d005b0cc5ed6d2f2b523
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49669669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c11afc51a8402a4e1b72eb7a5675d1d03096a8efff9c6cc1480b8e43672ac9b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'stable' '@1777939200'
# Fri, 08 May 2026 19:14:57 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:71b6aac173cb36faed0570fd95debf8f4842a2c9a293f3e5a9d53b6b4753f294`  
		Last Modified: Fri, 08 May 2026 18:26:22 GMT  
		Size: 49.7 MB (49669446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bac502f3d53004930d4be0b649692587d32955841c67d13b5de571dd913250f`  
		Last Modified: Fri, 08 May 2026 19:15:03 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:e8c349edf492edd30d7862a041c85e817e819e9c96265a5a97c6b0b36a642230
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cddf7b5b694b5f975814ff3b523dc3f589eb57544719502ea818460f658fe8c5`

```dockerfile
```

-	Layers:
	-	`sha256:2088605a23f426a9f49d2582d134ad673c3aee55377e0f21a66778e517d26759`  
		Last Modified: Fri, 08 May 2026 19:15:03 GMT  
		Size: 3.2 MB (3172394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8004a0ebb07b7441469a42f0a5e7082734b151998ffc0637452dc45ad9bb764`  
		Last Modified: Fri, 08 May 2026 19:15:03 GMT  
		Size: 5.9 KB (5852 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:e42e530ccd1966e9b30c782834dcc7373163bd3e0ed0b694d62f2d5150e4f393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50825803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d15ac557990460e98f4295e2a90b30d91eab9054b67020e564bf544f80dbbca8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'stable' '@1777939200'
# Fri, 08 May 2026 19:14:55 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:f3147330e313b59b920d18fe21914aeeb3780a24ba2b22054d7fbd94155580b7`  
		Last Modified: Fri, 08 May 2026 18:32:15 GMT  
		Size: 50.8 MB (50825581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471ecfc13440950d9af9210a6851d80407c236372312454c462ecde11b6f78d1`  
		Last Modified: Fri, 08 May 2026 19:15:02 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:bf4d30161671f674e8f402dfef202f80c97aff504f30e8058847f4d8d2c00abe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3173881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:277829f973f924ded3cbeb5e2aed79e048f66c81fe9bc7161547f114d22f029a`

```dockerfile
```

-	Layers:
	-	`sha256:b9e5f1d0aec5a9a905f69b8010da27adcea316f8f77b213bfe07570816e8d732`  
		Last Modified: Fri, 08 May 2026 19:15:02 GMT  
		Size: 3.2 MB (3168115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4791c301b27ed8a54c3351a460d3f88d20e3b98e1d02f1dbe7726aa089e0503`  
		Last Modified: Fri, 08 May 2026 19:15:02 GMT  
		Size: 5.8 KB (5766 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:a6daf2b3153b579e8bdda4f6ea0dd13bc84dd7606eeff1b3d31018f5f988a72c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53123388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4fdf984bec58c6273d7833a27a1c33426d9f2959d02c4d3a7a2aa8c166f6d5f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'stable' '@1777939200'
# Fri, 08 May 2026 20:19:14 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:c5c7000b20709bd6dcbfab6759e1a149a2f26517a7a5a3e49b4dd1192694e999`  
		Last Modified: Fri, 08 May 2026 19:46:01 GMT  
		Size: 53.1 MB (53123165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c886cb32ed88615975c386907654f4d0a8feced0dbd759d042fd795c659991d`  
		Last Modified: Fri, 08 May 2026 20:19:29 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:61ab05127ae1c325c54d5b6bf56b15be7aea408e2f311566206db4657a79a07a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3180236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76025579986f0f06a34845fd7c5840925f6dec915ab1a3fc2707ce62375779cb`

```dockerfile
```

-	Layers:
	-	`sha256:49a2225730250163116660f22140316c6c0016dcd153fdb92eb8c84ca982efe0`  
		Last Modified: Fri, 08 May 2026 20:19:30 GMT  
		Size: 3.2 MB (3174426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6cc2cad7a47b7584f9fb9df990ba0891ce33d84a620f26d4423e3ae47e52d64`  
		Last Modified: Fri, 08 May 2026 20:19:29 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; riscv64

```console
$ docker pull debian@sha256:5ab685b344f51af6760f89a9d5f3af93a9843b96a94524c9eef4a3eaf12febee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47798436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:379f8c06d9be713a7c16995a3b2574d38c5a1fa2447f1fb10fbde5d3fbdd4c62`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'stable' '@1776729600'
# Wed, 22 Apr 2026 05:57:29 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:2ab831617597f10eeb4f7a268b6da17b3b268b5f758c1427c29fe3518be9d92f`  
		Last Modified: Wed, 22 Apr 2026 02:22:09 GMT  
		Size: 47.8 MB (47798214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c091eb731877297756e1c5972dab167cbee33dad18aaccc2e3c056680695c7`  
		Last Modified: Wed, 22 Apr 2026 05:58:22 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:56d4fedd3d12a883eee8df01ba0eff292cda4318de5d36f339c0f5806e383741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3169047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15e1ac14e4d48d06fe7ac4730897afc0c74aa3db90aadba50528c1beb067bc4f`

```dockerfile
```

-	Layers:
	-	`sha256:781a6c51caaca463b3e4d5216886b123977afb7343a0646ba27e65e7d3f035b6`  
		Last Modified: Wed, 22 Apr 2026 05:58:23 GMT  
		Size: 3.2 MB (3163238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05f11d2c3de42cf374410bbb573029cf19a8b8e7be6758e3cb832345baec703c`  
		Last Modified: Wed, 22 Apr 2026 05:58:23 GMT  
		Size: 5.8 KB (5809 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:44b9778a5a9dff8e167c6515f392f9368ccc53745d5e28e99a8ce7f8544d7ef8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49372531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ab5f46e7756eb91f1ef73820205809aa8184018993fd2a2b2d437d3480e4e1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'stable' '@1777939200'
# Fri, 08 May 2026 19:13:43 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:801534d0ec07c581c87b0f64a5f7dcb2cefe3755dbf1317865149ba4e97c1922`  
		Last Modified: Fri, 08 May 2026 18:28:31 GMT  
		Size: 49.4 MB (49372308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179685e0a944e4aaef021c92e01c86486b076cb8453f895973622d09171464a7`  
		Last Modified: Fri, 08 May 2026 19:13:53 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:569603087e89af079d2e37a06eae4ef6fec4f097916c763acbffb5fd507b9e78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cac0526840ef828ccbdc17a1f8b9ced6c32be53dcb5917926e4be8be9d9f401`

```dockerfile
```

-	Layers:
	-	`sha256:b6b138e5bd3b3c5bfdc89d3ac8ef4d9337791cf19c7c59029e0fff6a0a9e1b59`  
		Last Modified: Fri, 08 May 2026 19:13:54 GMT  
		Size: 3.2 MB (3172360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e360a4aebafbb3b7b81e359b2feb18190b6b7a8dfeb0fac6033b77fc7433a3f5`  
		Last Modified: Fri, 08 May 2026 19:13:53 GMT  
		Size: 5.8 KB (5784 bytes)  
		MIME: application/vnd.in-toto+json
