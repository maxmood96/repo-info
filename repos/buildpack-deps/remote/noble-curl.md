## `buildpack-deps:noble-curl`

```console
$ docker pull buildpack-deps@sha256:49d74c64e5b49c9c01c1a75a49d67fcbd247e9113dd6015a418075d6a6cfd00c
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

### `buildpack-deps:noble-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:b623a159ed934a9e9e2935f4891633084485634a654940f2b9ad787f4dd87b78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.3 MB (43339567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba2286703615c56ac933f205ccb039bdba814c069fe24b61fc34672b036f2271`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7fdbabbfc2d2357c11d06b94c29d86f9283ba38506222a230cfe31c410f7d61`  
		Last Modified: Wed, 02 Jul 2025 03:09:59 GMT  
		Size: 13.6 MB (13621201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:38a66d03f2fd3e7255cbf7be9b38a372c5bbb2fdff6376a1eee956435df89aff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2614746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e5e04106c8726473c28a8e449263396225b0156f27052023058a38d5091f10d`

```dockerfile
```

-	Layers:
	-	`sha256:93ddda93fc370af354c87f1e401d2ec63d5c92e35f02809be638221f0afb4b3c`  
		Last Modified: Wed, 02 Jul 2025 04:20:24 GMT  
		Size: 2.6 MB (2607787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6156245fc78bf67bea435943243c3f996ab8f269fcf2a0bd6ba158ed8a8b0d5`  
		Last Modified: Wed, 02 Jul 2025 04:20:25 GMT  
		Size: 7.0 KB (6959 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:f3192ba8c82ad2c4ffe5d3f718a444b30fab76cc74099d3917eb7098af7974de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39622789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e34d60f48f6ad02053c45ee94cbb022ef419a5eeee321d60b0f019534b4059c8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:f5b71e3353c1f92a265c88e163d98b6fc00235db4d001763328933c4838f3576 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:76393e3f1626a318c4984c6e6d91f17fe6888451b277b6cc175eab3a1032ebf5`  
		Last Modified: Tue, 03 Jun 2025 13:33:19 GMT  
		Size: 26.8 MB (26842221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca74547492ebc6726e0a1ef9887a16bf144497b7eff9f2f4d1b9b96fd524d65`  
		Last Modified: Tue, 03 Jun 2025 17:00:56 GMT  
		Size: 12.8 MB (12780568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:72f179f4b14bbbffd1fd7cf070cf6d071d08e207068b7ed155bf3e396bcfe6a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2494643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5a7ea161697b5cf2afe72060c9da794edd1061d27c6499dd595c49982161de2`

```dockerfile
```

-	Layers:
	-	`sha256:be1fba116274223bb22b3c0c9b114786129d05e3f01ee5bad87633cdf1fc3ba3`  
		Last Modified: Tue, 03 Jun 2025 20:02:16 GMT  
		Size: 2.5 MB (2487624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c4a3fe4050198c96e5730f5890e4ac25aa8a9f46c8de76c31dc04f8617e02d9`  
		Last Modified: Tue, 03 Jun 2025 20:02:16 GMT  
		Size: 7.0 KB (7019 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:d9739e5666d66f010a910d32b0ff37b0328610097efa246208fcf96e4840825e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42312062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af9c0bd9cd19ca114377a8fbb3c791bafdcdb28c4ddf3f4a7ef738d87b0ce804`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:d3e5c3c7ed81035a9d3dc27dc9f7b63cca5f6bbbaa499c38e470d52b7e57817d in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3eff7d219313fd6db206bd90410da1ca5af1ba3e5b71b552381cea789c4c6713`  
		Last Modified: Fri, 20 Jun 2025 09:32:57 GMT  
		Size: 28.9 MB (28856018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b66004928f8c394a026eb75e60764cdc2913b001d64b1a1688836d025824ec3`  
		Last Modified: Wed, 02 Jul 2025 04:19:26 GMT  
		Size: 13.5 MB (13456044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ecde1e0dad706083e1d175ff94155f7e4e52a16631cfb6b2df59309e7d378f45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2615883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f32b33e6fdd855d46b8287789333b3fd752081458168edd96383e58ffd73359`

```dockerfile
```

-	Layers:
	-	`sha256:5b687d93fe99352679e766b2f9014b538a3a7a67be1914899de90638a1ec081a`  
		Last Modified: Wed, 02 Jul 2025 06:07:10 GMT  
		Size: 2.6 MB (2608845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bdf25322adc70a25f9c03d17427dda6c9000f0e25e1cac1eef9e505a3ac470b`  
		Last Modified: Wed, 02 Jul 2025 06:07:09 GMT  
		Size: 7.0 KB (7038 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:b413b8be2ff7e9e938a902aba788d403c5c87f64e2969b45b382b90d58c3f30e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50275637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5f1a78c17d7f6c78c3a33aa184f0228bdf7fc76dcd39ce537df782efb3d873e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:fca9cbe6eff6a6982a26900c08b4e2c5a46057e9e5386288e826ac4f2cb17b32 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:384c99c6e2b4660fd65fc9823f13a263fb87d4aec3b8f2bd813a7a255bcf46f3`  
		Last Modified: Fri, 20 Jun 2025 09:40:24 GMT  
		Size: 34.3 MB (34321506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22221e46c866dbeb7893d2cb7aad53cba8ff901b321833a29ce219ca59c94224`  
		Last Modified: Wed, 02 Jul 2025 03:10:27 GMT  
		Size: 16.0 MB (15954131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9c2f0c24196f4aa5a78599b3b0b250bcdbb17011af6fc30c7c8be8d6cf7a2a15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2619397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb337a06049c2753e8e9849f0e33c9ec6e314153ea999da71af7aa40e39b24cd`

```dockerfile
```

-	Layers:
	-	`sha256:5334df4f532f720cc8052f0458c673b7646cd9209fecc7bbecd4b4a74dc9b78f`  
		Last Modified: Wed, 02 Jul 2025 04:19:43 GMT  
		Size: 2.6 MB (2612406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:810daaf0e71b10d6f70d5e2f070018bcbc98fd7d3af52b026e25c10264564986`  
		Last Modified: Wed, 02 Jul 2025 04:19:43 GMT  
		Size: 7.0 KB (6991 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:a5bcf69ecd59db85638135327eaf19e73c75ce140a82fde440cf507017f1dc3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45279124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36f84e42b75edb9456280dd4ea2b3debc3c308eb84c19ac602ad5fcab3919b2d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:202c5a7a84e813495c089800398f2ba18952221717db2c10e042ce4179ee6fc0 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4ccdff8fdb11e14b8e0dab6804aeebce5855635c68b20f199dcf0efcd9b4c462`  
		Last Modified: Wed, 02 Jul 2025 01:17:14 GMT  
		Size: 31.0 MB (30951024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ce57c66749f825da8658484f946ccac9fb912f45d0ce0e0acba90acfe400d8`  
		Last Modified: Wed, 02 Jul 2025 03:14:22 GMT  
		Size: 14.3 MB (14328100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1ae18a0ebc8ba4580919fa2af16917ce01a019ec931050ccd7928bc9fefca388
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2608677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32e50699b0516182e5b8c0e34a53ef003a2a7cbbba39c9ba8bddd481f4de78bb`

```dockerfile
```

-	Layers:
	-	`sha256:9b4926a5e6469df7b5307b1f9df71bfffa9b60575a6c8fc84ad45cabd01402ad`  
		Last Modified: Wed, 02 Jul 2025 04:19:47 GMT  
		Size: 2.6 MB (2601686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6504f87702695d84496a6e8950d683a97afdfb7b02e86a147a3eaf614afed73`  
		Last Modified: Wed, 02 Jul 2025 04:19:48 GMT  
		Size: 7.0 KB (6991 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:ee6ed63a00738c07ce068def993b0ba0c897a5699206ee7b46593f20c65895cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44863716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:309615de4eebb18fcc36f905d2da871613182cf06923b88562879ab1288b9460`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:80b0b0c2a08a762cf6a520d8428a5c769c29e72f4a51630adb2231f2816c50c4 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:30d64ca13d9d94eb48bf3fece3e38a4e60931d72f1a8c633dec981e43a0515a4`  
		Last Modified: Fri, 20 Jun 2025 09:40:24 GMT  
		Size: 29.9 MB (29925630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e0a7472d36ac954b6ad8ae016bc95c96fed55c2a6dff7a2277fb2905ea71cd5`  
		Last Modified: Wed, 02 Jul 2025 04:13:00 GMT  
		Size: 14.9 MB (14938086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ffaa62d3af62ca13d9c48f8fc15044ef5fad5617f0321597decbb40c64f06cc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2617571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:465a68bfe6db23e262a4451dc7178843412a7293d1506c400c2ce0c7bc346bd5`

```dockerfile
```

-	Layers:
	-	`sha256:7cc9816379691cc060d715b899458a6f9da46380c5852d12cd26e8823bd1c490`  
		Last Modified: Wed, 02 Jul 2025 07:20:03 GMT  
		Size: 2.6 MB (2610612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e497243ce89ce15235f51365d1d00a53aaf55bc2a430d97296e1245a3b7b840`  
		Last Modified: Wed, 02 Jul 2025 07:20:04 GMT  
		Size: 7.0 KB (6959 bytes)  
		MIME: application/vnd.in-toto+json
