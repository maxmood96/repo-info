## `buildpack-deps:jammy-curl`

```console
$ docker pull buildpack-deps@sha256:fea23caf2a71decad8b2747461390259e794541d8da22af82faa6286de96adde
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:jammy-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:3cdde51163b639261032893517d180fe672d389e9281fa0cd03fe862d512beda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36841708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7affdb383e8b07a1d7d9781011f00398b51a5cc086dd8682f7a8d6ba52845f24`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:04:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0678f5d5bd853ac3377b342817069c80171f8554b28f23a90374f267e96ca3b6`  
		Last Modified: Wed, 01 Apr 2026 20:05:00 GMT  
		Size: 7.1 MB (7105295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:24ba93a7a4b684cf1c8523e4a611042fd11719bada13acaa86fbce384164749c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3212096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:808ec624a6ea8e201b31a31beeb9578f3f6b59e726f534ffee2d2b05b0682a7c`

```dockerfile
```

-	Layers:
	-	`sha256:32a4266c8198e58fae5c1eda2ef12f62b93c9d233d3eaebda714f62744837e71`  
		Last Modified: Wed, 01 Apr 2026 20:05:00 GMT  
		Size: 3.2 MB (3205215 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b229adb3206b2aa9a816b1cd2c8e5429147d0564fbb5b4a5d2245fe470223e4`  
		Last Modified: Wed, 01 Apr 2026 20:05:00 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:6ae6c8a97f86c0e534deeaaddad3ec8307646d92c2648a3e53474fbe9b91511d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33851507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ba9d4e419bcca431dd9fd519081fc855ff51a24b43df4923544dbbeaf8ce77f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:eaa1e345a925acc7b826effa9fb4c3dfb4aebe47807533938898d49afe7561cb in / 
# Sun, 22 Mar 2026 18:14:12 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:07:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e7c88f36edd2a67246005d083413bd656459d3b63bab8e6a05a1018c7658daae`  
		Last Modified: Sun, 22 Mar 2026 18:43:39 GMT  
		Size: 26.8 MB (26842286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea32eae6e70821cf7c87d1558f27873f18b23a676f23d22ea0004e4ffdc5f34b`  
		Last Modified: Wed, 01 Apr 2026 20:07:12 GMT  
		Size: 7.0 MB (7009221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e3ce7608b896ec0445d2ff2c9e21973a61df11afad44da5260c05f62edd1c5bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3214467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19015827469ed2879b9e64a4f1d7892192f8a13252fa447a2cacde8d357bb3c6`

```dockerfile
```

-	Layers:
	-	`sha256:958214f2bd5be73405e6d199bc2f0674f3daf43c8fbea4765bf8318126f3b1cc`  
		Last Modified: Wed, 01 Apr 2026 20:07:12 GMT  
		Size: 3.2 MB (3207522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16904ee2ac9a4f60f43c32a5c400bd5bdefb4d29aa12a6799b7dfeaa51293afa`  
		Last Modified: Wed, 01 Apr 2026 20:07:12 GMT  
		Size: 6.9 KB (6945 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:a3b4fad9ff470e2cac2ece4535fe1c85ffc730e002677ef743c0eedfb09fdc6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34666247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f884e6339106310c930cbf81de6a67687f541baa3cb65ac3248ebfbc5f0cbe95`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:05:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c9b1f87458950c0fcd1b5032f566542c2039fc1ae78138539563c4ff4c9be88`  
		Last Modified: Wed, 01 Apr 2026 20:05:12 GMT  
		Size: 7.1 MB (7059304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9adc5a4e1d4f828482f4847cd6e520c7b3f96f2ec03eba697125bce09e15fe80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3212442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:179dfb88b77d9fa35bb977682489450ea5da6d959318e57ddab77df1858027ac`

```dockerfile
```

-	Layers:
	-	`sha256:fa40598605bd687f3db6ccafc5ddd13a7e83aebc2c48c95f9a50963c8a9f2bc9`  
		Last Modified: Wed, 01 Apr 2026 20:05:12 GMT  
		Size: 3.2 MB (3205482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e64b0c234c9a6ce8dedda2b95102dd0c82e5ff1f3b1d78f3c0104f071140ea50`  
		Last Modified: Wed, 01 Apr 2026 20:05:11 GMT  
		Size: 7.0 KB (6960 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:06cbd914abd657596e74dfaf81440fae808b019b658a00cad585d78d477e7ac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.8 MB (42834412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:578ee84b4f713d8a368efed8f2fd047180d1ae05c17797d0d33363f133a02952`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:11:34 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:11:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:11:34 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:11:37 GMT
ADD file:268be611d24f69c3d8e480314cd587652e4c89a6032236737057c8b64f2379da in / 
# Sun, 22 Mar 2026 18:11:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:17:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6fb1b04a0a70d070de8a04181c7b855a46b1ea4f771660ae7f0783acd4569be2`  
		Last Modified: Sun, 22 Mar 2026 18:43:46 GMT  
		Size: 34.6 MB (34649660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0601ddb68d9444803d7b9a76e5d2436faf60ed8c2386c2a288e3a6cf2c5b1bd8`  
		Last Modified: Wed, 01 Apr 2026 20:18:04 GMT  
		Size: 8.2 MB (8184752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7a7bd108816951adc8c7d7894fb4b53ba4a2afeb7952b70341247544a4d7609d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3216764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7516d968b536a5a3b83545676ab0f48b2b19cb0b6e2d004b0b5b1f0d8526539`

```dockerfile
```

-	Layers:
	-	`sha256:014f5a8bd90213e749bfcb716cfdbf2600cb05949fafb4f4ed7081397eda91d9`  
		Last Modified: Wed, 01 Apr 2026 20:18:04 GMT  
		Size: 3.2 MB (3209851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b85578a1a4512236b060f484938e32d4aa7bdd800d80db2743c39b4db68597e`  
		Last Modified: Wed, 01 Apr 2026 20:18:04 GMT  
		Size: 6.9 KB (6913 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:903792f3bfb2c475ddff50434e77ba9d40bb2545e3ff9f482324fccd25b4cb35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 MB (34163417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d07ab397374c0da007740badd2869b1fac1ae5ef0bc55f8c1c8c45051179556c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 24 Feb 2026 07:58:19 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:58:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:58:20 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:59:01 GMT
ADD file:fe9bc101b444ec167a91ca8e26679867fc3481650b0a57dfbc71041252c52df3 in / 
# Tue, 24 Feb 2026 07:59:06 GMT
CMD ["/bin/bash"]
# Sat, 21 Mar 2026 03:03:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c32e08022022bb708d1470956136113ea37119623075e5019f555d270f225be6`  
		Last Modified: Tue, 24 Feb 2026 08:08:12 GMT  
		Size: 27.0 MB (27045961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064f5d3ba01514a8f2923c2d44171c1cae4e8eeb6cda3193e3b8b567ce709f7a`  
		Last Modified: Sat, 21 Mar 2026 03:04:18 GMT  
		Size: 7.1 MB (7117456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5add2175f92ebf189421da0346111833fcf182eccb7997afab404c970b14b701
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3206016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:308d06c49d8774fb9004e71d2b616987dc384017a6091bec3cdfb5f07bf83c2d`

```dockerfile
```

-	Layers:
	-	`sha256:f003fc2f4001a90382bac88c2e02da68668c47e0e01b0ee3d8b156c1f65037f6`  
		Last Modified: Sat, 21 Mar 2026 03:04:17 GMT  
		Size: 3.2 MB (3199103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9eddac2991b0e82978aea647240f8b4a01b7982da86a80a5937a4dc510d72432`  
		Last Modified: Sat, 21 Mar 2026 03:04:16 GMT  
		Size: 6.9 KB (6913 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:ab754108c77d0589bd152240fa370e3fb909e9863afa5586117c019bcc9171ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.2 MB (35219978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71e77c6056467187c3e3629caedb8a667567d04b6d99fc993f721c72e687c96f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:12:49 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:12:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:12:49 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:12:50 GMT
ADD file:e6d9716e3c60256d600998c1e662d7bc5ced705020e73df5a8f8327ed250efa1 in / 
# Sun, 22 Mar 2026 18:12:51 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:08:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7db076360428795a3bedb94abf5c7d3527328da728852f1fa3e28cc99bb96eba`  
		Last Modified: Sun, 22 Mar 2026 18:44:00 GMT  
		Size: 28.2 MB (28202727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390ee8e0bfba66d347e5a4dfdf7c3593fa25dad79673b32e42c9804ef0045bf7`  
		Last Modified: Wed, 01 Apr 2026 20:08:46 GMT  
		Size: 7.0 MB (7017251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f86ad6fd1354f8972530ef7d8e82e3d1773acb5aaf6af97b18e5c8130ecc773f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3214313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51fc9c4fee9fe8bfea3a6d74bc9858a3be103bfbd3a7d9edd9b42563e1735328`

```dockerfile
```

-	Layers:
	-	`sha256:5eadd9f8c56a27975deebadf8794097dc937070b4267fb1beec5a4a099c1e8d2`  
		Last Modified: Wed, 01 Apr 2026 20:08:46 GMT  
		Size: 3.2 MB (3207432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:155e23441031e969a60f03bff7c813a3973356aab35c3ad308545eea4a8a988a`  
		Last Modified: Wed, 01 Apr 2026 20:08:46 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json
