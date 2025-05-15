## `buildpack-deps:noble-curl`

```console
$ docker pull buildpack-deps@sha256:e33d3b2a883b09dfb80ee43debc905b2bcde03a1bf0697c312c412dd3a2e2f93
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
$ docker pull buildpack-deps@sha256:3b517ebb8f54574e39a8f7ddf3f199d0c79edbcc30e0b8e86477b5c6ff088398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.3 MB (43337990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fbc6c469a6c7f82b7ffe4d2b17faf6f0c5860e6e5d817537a8dda418e420d11`
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
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Mon, 28 Apr 2025 10:53:49 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9eaace9b65900e696e96e472a957b7da3924a1f1e20b735931fd210783d02c2`  
		Last Modified: Mon, 05 May 2025 16:34:38 GMT  
		Size: 13.6 MB (13620461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a0601561746f7636587c186503cc60a07c291a0b41de0c551cd81194508c4fd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2467472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3e66fbea0cf48ebe471737c45ece61f3ad7033da6392489e239d790ed794b3b`

```dockerfile
```

-	Layers:
	-	`sha256:113cc119a2a8d6ae868496e4f380a2032c450024f4ab2654e5327deed0bb1af9`  
		Last Modified: Mon, 05 May 2025 16:34:38 GMT  
		Size: 2.5 MB (2460513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61c95f17675c02ea6234f9c0355aaa1e809c72f728b60dbc7945ee4be68fe81f`  
		Last Modified: Mon, 05 May 2025 16:34:37 GMT  
		Size: 7.0 KB (6959 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0cec0e3d4e4261ffb2670d0df97438a75e00e1ae845625c5031252190fd44a62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39617337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c94d73f29fde49371853da67626303271b85c19fed1a9369ce1f757ad32b4644`
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
ADD file:0a4f443ceea6f2d38d4cd9140cd3ff090f97e81996d29997f71a7e6267915f64 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d5afef7cc6686ed2d24ed4bfcb591ca82e697ea35b656a63f79d222cf1271caa`  
		Last Modified: Mon, 28 Apr 2025 10:54:02 GMT  
		Size: 26.8 MB (26837779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44336f57998ec8ec9b6b393b0377c2fceec78d81e9802b43bbe7cc354461c26b`  
		Last Modified: Mon, 05 May 2025 16:35:26 GMT  
		Size: 12.8 MB (12779558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8fbfd355389feff276734942fe423bd31cd931c9ce9858bfabc91e4dddf5e4ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2469836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:515874de2b3cc5827d16d2cccce6d85d92ff1fb20f14af9320c1e8cb921747f3`

```dockerfile
```

-	Layers:
	-	`sha256:42cd50c3a838698e2786e92b395c43cb35b4be9186e6941810fcb920494f434e`  
		Last Modified: Mon, 05 May 2025 16:35:26 GMT  
		Size: 2.5 MB (2462817 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d08f58f8d4ad222b6be10cba87ea3e488eaff1c5427030626f100777be71a66`  
		Last Modified: Mon, 05 May 2025 16:35:25 GMT  
		Size: 7.0 KB (7019 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:e28011fa4031ee0c64b88a6ce8a54908741e33008b4d8e02409047d62f16480a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42302310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e32bfc5d6b8c98f7a1e0b4987b83e8b17348df9b14d71f417c822bcf28cab95`
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
ADD file:1bafcbb31dbbcfab5d15f474524e7fdd408a80128ddb9f1743e9f39cfa86ce33 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2f074dc76c5da961ce13817b02fa1e3c3070ad4b94970aa7f52f6c0d63b07696`  
		Last Modified: Mon, 28 Apr 2025 10:53:55 GMT  
		Size: 28.8 MB (28846876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4a0cc72f6ea7fe79563bee33bdcb1c9b244a1c5ab3c0f32fd003cd207327808`  
		Last Modified: Mon, 05 May 2025 16:36:26 GMT  
		Size: 13.5 MB (13455434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cf6bd53f992a452f32130ab6b47dd3ebcad7dd6b60db88c17073752c0f5e40bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80933d0b90aa281906c944f68796a3aa98dbad671ad1de35927da772336fb292`

```dockerfile
```

-	Layers:
	-	`sha256:00df4cd2bb37cb8b6197334a53557998335129fe89176ee436a6b294f26b8588`  
		Last Modified: Mon, 05 May 2025 16:36:26 GMT  
		Size: 2.5 MB (2461571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fdfa0704e65dc07056d6b55d2b2831ab1d2d2e4c4bf5ad180313c64ab2e6cea`  
		Last Modified: Mon, 05 May 2025 16:36:25 GMT  
		Size: 7.0 KB (7039 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:dfae48ad0c845cc76182607aa1a7cef3aed396bf00140adc6b88c160e50d5e30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50292848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b6b6e8a52480c9b7375d71893313bc4d935b8f1c5549f80819e75f170ee0f6`
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
ADD file:d4d363297b0bc97147d6215ececd915564f3540c035d4c68fcdd781acaf0e4e7 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:fd7ce82c353803b69e06046e91345d15e766766fa395e4fb8e9f652834cddb32`  
		Last Modified: Mon, 28 Apr 2025 10:54:08 GMT  
		Size: 34.3 MB (34340838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb01c615e0adf803fa55fc78bc3041600f2aa0ce1f245aedb53d467d5681ff9`  
		Last Modified: Mon, 05 May 2025 16:35:45 GMT  
		Size: 16.0 MB (15952010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:18804b9e8722dab638e09e0b1bda761a058391afe6c40048d89f871e3ecc901a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2471991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3037081d1349dce40870f77e9330ed814bd53a5bf32000f5a08fc39838ec28a`

```dockerfile
```

-	Layers:
	-	`sha256:bfe84aedb96c640e68f8555b887446c2f7cd146ae77c108233cdefc00cb31f8a`  
		Last Modified: Mon, 05 May 2025 16:35:44 GMT  
		Size: 2.5 MB (2465000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d83ea0dafdbb4d3fe5a572c03d104de81f4b4fe902860e4f716b38cc031c068`  
		Last Modified: Mon, 05 May 2025 16:35:44 GMT  
		Size: 7.0 KB (6991 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:ed3d4f8bff159ebe1d0fd7654398157a76f54045ef39bcc5de50651dc13b3406
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45271585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f79b6333e39c1432d7c3aa708faeff2567320ce7dedc493e37ecd899656408f7`
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
ADD file:a7f5e3a8aff782c57aa8346238f9dd99048f1bf1a67260c5949ae9396a429340 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:617ff4840b8ccb0dd209aefc32c58a25fc5e72effac2d6267be2d5e4f07db22b`  
		Last Modified: Mon, 28 Apr 2025 10:54:15 GMT  
		Size: 30.9 MB (30943987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77fb2de0b2f49e76302577d112d09b1cc04109df7d10f98098395265b9951f9`  
		Last Modified: Mon, 05 May 2025 17:09:44 GMT  
		Size: 14.3 MB (14327598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cec2e686f44aff270c80995cf5cf65d7bde915b68a5c0de64903c0a5c45a35e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2461563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8ac1e6e24a96db3bb1835d3a1346308c3d310691f897a456f460e322e9ecdd8`

```dockerfile
```

-	Layers:
	-	`sha256:00b0c2716a5582414d949c0d4db490324849ac717df4040e1740faa4e4390cdd`  
		Last Modified: Mon, 05 May 2025 17:09:43 GMT  
		Size: 2.5 MB (2454572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a35ea22dc3cbf6a8b7a74829d3b198d700222fa252ccab1b19e7a5cbc518e07b`  
		Last Modified: Mon, 05 May 2025 17:09:42 GMT  
		Size: 7.0 KB (6991 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:0cf780e6b2669dd747978c88710bf95c72e99b4f31bb7311f73aeacd2f0b8270
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44893710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbbd89cbe54debe1c63eaa3f3742e2559e0e840420aa4deaf26ffcd988153675`
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
ADD file:486993225aeae656f8d559f5c296f6c3164966e35f4b628d26e1da1b75592143 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:52a1750d5fddc355cdc90a83890b7d582c7f145aa5d114d9582cd010b8ead145`  
		Last Modified: Mon, 28 Apr 2025 10:54:21 GMT  
		Size: 30.0 MB (29956186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01143edc1a4246e16888451bfef82ed89787f53271c5fa4fe7b59706ba37dd16`  
		Last Modified: Mon, 05 May 2025 16:35:09 GMT  
		Size: 14.9 MB (14937524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:640d59a96f138d58a745a77a252127763fd78fc500c46cf1850ebf6647f8a870
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2470297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1641803c7715b474f1e73793accba31cd705ef271df8af4a8e9fdf661512455b`

```dockerfile
```

-	Layers:
	-	`sha256:3cc86ef499cc330effdc33b2e7241b9b0bc70a58ee627637f67eba70c8233a49`  
		Last Modified: Mon, 05 May 2025 16:35:08 GMT  
		Size: 2.5 MB (2463338 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3e84b605535a22d1a0b0b9d6dd646424bec9b612cb0f7d90c2c2b07707fbacf`  
		Last Modified: Mon, 05 May 2025 16:35:08 GMT  
		Size: 7.0 KB (6959 bytes)  
		MIME: application/vnd.in-toto+json
