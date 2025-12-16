## `buildpack-deps:resolute-curl`

```console
$ docker pull buildpack-deps@sha256:3dc2b52543696ced2486e1f58eaa59d38c0a4fe4ff4032b02315a1985b49ad6d
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
$ docker pull buildpack-deps@sha256:c13cff76faa407713b9ef20c79c5b28c543bb5fd2a104e6cb88500f7a666467d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53171312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dbad511b761bbe428da8b146ade042bf58e56815fd68c5f77ce1b579487a5b2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 08 Dec 2025 03:12:22 GMT
ARG RELEASE
# Mon, 08 Dec 2025 03:12:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 08 Dec 2025 03:12:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 08 Dec 2025 03:12:22 GMT
LABEL org.opencontainers.image.version=26.04
# Mon, 08 Dec 2025 03:12:24 GMT
ADD file:20d5e915d0d393fcb7e648f66e92f60aae8aa4008ec9f474084335d6b517afe4 in / 
# Mon, 08 Dec 2025 03:12:25 GMT
CMD ["/bin/bash"]
# Mon, 15 Dec 2025 20:11:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1930ad95e8edfa40a67fed625a6b952de1df4b24c225dd737adb00346824f4ac`  
		Last Modified: Mon, 15 Dec 2025 20:02:05 GMT  
		Size: 33.7 MB (33742427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc032e9d150edca71ca527020eb733586080f7bda49bec4c3582b3f374be743`  
		Last Modified: Mon, 15 Dec 2025 20:11:39 GMT  
		Size: 19.4 MB (19428885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e4b93810198e1c0ee104d0ca51709aa685955fde978c78f25d722763822cf0da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2955758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bd66a683c9aa570c995d80077c12aa3098e4574424afc8872f740f5574fcca1`

```dockerfile
```

-	Layers:
	-	`sha256:ac4b372a86348d90bae2d99a580e64208f12201fc028987d441726db3a0c085d`  
		Last Modified: Mon, 15 Dec 2025 21:11:49 GMT  
		Size: 2.9 MB (2948824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a66b18460b72748855fa80d6b3d88155e44e9f1985af878f6cde5465770a3445`  
		Last Modified: Mon, 15 Dec 2025 21:11:48 GMT  
		Size: 6.9 KB (6934 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:7d9dd513d7459efb7b55861232fb9e974decbcc9e81e82e04b35f549bb69dcc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48901886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a26a57a7227971c03ba4434d071a63874e7c4570a9aefc33ab7dc386c6039b1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 08 Dec 2025 03:13:34 GMT
ARG RELEASE
# Mon, 08 Dec 2025 03:13:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 08 Dec 2025 03:13:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 08 Dec 2025 03:13:34 GMT
LABEL org.opencontainers.image.version=26.04
# Mon, 08 Dec 2025 03:13:39 GMT
ADD file:b61e9f94116cf2f68a6415698661ee2b700e7d672508b7326845bcf886232f85 in / 
# Mon, 08 Dec 2025 03:13:39 GMT
CMD ["/bin/bash"]
# Mon, 15 Dec 2025 20:10:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2bf29d7486c7e629372c92e4748c184d88f0e4e34b33e49f296e9c9c32039dec`  
		Last Modified: Mon, 15 Dec 2025 20:00:53 GMT  
		Size: 31.2 MB (31156573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df541f37757c7ee3123bb95436fe3a3bf9cac7e92450e3a3a87b55d80bf8aee`  
		Last Modified: Mon, 15 Dec 2025 20:10:55 GMT  
		Size: 17.7 MB (17745313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4e6adb51cfb784990263b4b9966365d366679986553b726ac66c044f6de404d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2957324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e86b82d494601638e2fba5af3719efe7ebd4417bc1d134caa785e83731df4c2`

```dockerfile
```

-	Layers:
	-	`sha256:be7c9a539d743b49edbc134a4cc9319773b73f7f04c2b6db530bbfb23e532fb4`  
		Last Modified: Mon, 15 Dec 2025 21:10:26 GMT  
		Size: 3.0 MB (2950326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e2292129015314585c066b6620a52c34626b6019f8367199bb9cd7241154c1d`  
		Last Modified: Mon, 15 Dec 2025 21:10:26 GMT  
		Size: 7.0 KB (6998 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:d6df87ae38466c3d4d6f2a7f51b7ee18cb23e3764a392c333b0205d1bce1d692
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52254337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f952083117b2fdadc74b1ef7fa1706a464395efdbdfcdf9e5cbb79e703ee5eec`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 08 Dec 2025 03:13:36 GMT
ARG RELEASE
# Mon, 08 Dec 2025 03:13:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 08 Dec 2025 03:13:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 08 Dec 2025 03:13:37 GMT
LABEL org.opencontainers.image.version=26.04
# Mon, 08 Dec 2025 03:13:40 GMT
ADD file:880dc0c9ea14ee504f2d3c0432440022eb7cb1d8e051e9c517689f394260958d in / 
# Mon, 08 Dec 2025 03:13:40 GMT
CMD ["/bin/bash"]
# Mon, 15 Dec 2025 20:10:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0196ed0ac4ca95d4c74a0629deb6468dc9b8d3f3bbe0834d244c1ef7c9bdd8b3`  
		Last Modified: Mon, 15 Dec 2025 20:01:51 GMT  
		Size: 33.3 MB (33300910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40970ea46a6648d5c0acf6872b257eeae96e2929f52e0a4991f153cd5c126ccb`  
		Last Modified: Mon, 15 Dec 2025 20:10:54 GMT  
		Size: 19.0 MB (18953427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9f1ca006735a97c7a57f4eed3992fda49788812f879468d63ab760f9897949b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2956097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78e222641f992437c938ee136172900a4c05d1cdc034117b5eec40f10249e92f`

```dockerfile
```

-	Layers:
	-	`sha256:12592a274b951a3c73910474840abbb8542d2536ad62ad3c4ad4a55667038fe3`  
		Last Modified: Mon, 15 Dec 2025 23:20:01 GMT  
		Size: 2.9 MB (2949082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d1367d2289e689fc9b90d288dafadd31395444aa7d54dd94da3a2805af7b047`  
		Last Modified: Mon, 15 Dec 2025 23:20:02 GMT  
		Size: 7.0 KB (7015 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:36a0f91a1b0831ee533a8dd21d659cb95b2546db6ad29e92d67d1f380e2bd50d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60715480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18c5d0a955b60eadcd5d8d8f669eab9c1ce357ca18770d5e70ac838c225463ad`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 08 Dec 2025 03:13:14 GMT
ARG RELEASE
# Mon, 08 Dec 2025 03:13:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 08 Dec 2025 03:13:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 08 Dec 2025 03:13:14 GMT
LABEL org.opencontainers.image.version=26.04
# Mon, 08 Dec 2025 03:13:20 GMT
ADD file:1ba64fcb8425d92e42a4dcd6299abe7ca1abca89c8ada8bca11d7804b715a1b7 in / 
# Mon, 08 Dec 2025 03:13:21 GMT
CMD ["/bin/bash"]
# Mon, 15 Dec 2025 20:10:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:99d2753c6e5d3b5e655cfd1b57108083b422a46cfe597843b023a4e2c7c000bd`  
		Last Modified: Mon, 15 Dec 2025 20:01:29 GMT  
		Size: 38.8 MB (38808598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e9c4708e4fcc9ce73471d9e3d813efeee0cfcd5a8afd3b763ae4d5927a0d5c`  
		Last Modified: Mon, 15 Dec 2025 20:11:35 GMT  
		Size: 21.9 MB (21906882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:774f63a38c814f82f41b30e73cd515feb92eda5dc21458676857d60e53692258
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2959614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87f4d851e4fa7e7543519c6acfd334da4dadf24c86a833a5867ca50bddb9651f`

```dockerfile
```

-	Layers:
	-	`sha256:214cd196d9805d2c12aa342fa88f50edebbe4be561d0592a4bce9d8fdc50075e`  
		Last Modified: Mon, 15 Dec 2025 23:20:06 GMT  
		Size: 3.0 MB (2952647 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:196ca5c981ef88ab1da4436b02981bff25601af04af2fae1644174339c904656`  
		Last Modified: Mon, 15 Dec 2025 23:20:06 GMT  
		Size: 7.0 KB (6967 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f75634e10f2ac2a0b9e5a0b2e742672bc30ad8a9299335544ef1b34a4b0da5f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53278204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6899e5d89aaae99304c098aa27b08e443381105f7eefbd9e7373e84bb717907a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 08 Dec 2025 03:12:49 GMT
ARG RELEASE
# Mon, 08 Dec 2025 03:12:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 08 Dec 2025 03:12:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 08 Dec 2025 03:12:49 GMT
LABEL org.opencontainers.image.version=26.04
# Mon, 08 Dec 2025 03:12:51 GMT
ADD file:9d8d73794e21475bdd8f856aa959b4a2af7fda40f696897caf099eefd5628d0b in / 
# Mon, 08 Dec 2025 03:12:51 GMT
CMD ["/bin/bash"]
# Mon, 15 Dec 2025 20:10:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9a53a9f36e89cb17b371244f4700e0e70e68c792d70ffa6f555d0497c602d741`  
		Last Modified: Mon, 15 Dec 2025 19:59:57 GMT  
		Size: 33.4 MB (33395288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32929a90664eb992dfded2cfe05892d67b8b30f3ec5f2a61699955dd20048079`  
		Last Modified: Mon, 15 Dec 2025 20:10:56 GMT  
		Size: 19.9 MB (19882916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1815416d028cab6c9f6833ad2413809b412dd80e9599f212b4afea69c0bbf622
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2957789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9aa19020d7e5e58806219823782d8943cb1d3fb5d8f9f13ccb8819dadf00dbf`

```dockerfile
```

-	Layers:
	-	`sha256:8e2917d831e2f92ef077ff0dbc5733cfbb41b86cdc5a0b8c9e84d01c8f6035d3`  
		Last Modified: Mon, 15 Dec 2025 23:20:10 GMT  
		Size: 3.0 MB (2950855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a68a598d0061b5767ecfdf699bd8ed830c43024d33860f4834498379cd6f9826`  
		Last Modified: Mon, 15 Dec 2025 23:20:11 GMT  
		Size: 6.9 KB (6934 bytes)  
		MIME: application/vnd.in-toto+json
